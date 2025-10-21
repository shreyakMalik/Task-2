pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '🔧 Building Docker image...'
                sh 'docker build -t myapp:latest .'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Testing Docker container...'
                sh 'docker run --rm myapp:latest'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying container...'
                sh '''
                    docker stop myapp || true
                    docker rm myapp || true
                    docker run -d -p 8080:80 --name myapp myapp:latest
                '''
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline executed successfully!'
        }
        failure {
            echo '❌ Pipeline failed. Check logs.'
        }
        always {
            echo '🧹 Cleaning up temporary resources...'
        }
    }
}
