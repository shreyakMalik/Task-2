# DevOps Task 2 — Jenkins CI/CD Pipeline

## Objective
Develop a basic Jenkins pipeline that builds, tests, and deploys a Dockerized web application automatically.

---

## Tools Used
- **Jenkins** — CI/CD automation tool
- **Docker** — Containerization platform
- **GitHub** — Version control and code hosting

---

## ⚙️ Pipeline Stages

| Stage | Description |
|--------|--------------|
| **Build** | Builds a Docker image from the `Dockerfile`
| **Test** | Executes a container to confirm the image functions properly |
| **Deploy** | Publishes the container on port `8080` |

---

## Running Instructions

1. Install **Jenkins** and **Docker**
2. Create a new **Pipeline Job** within Jenkins
3. In "Pipeline from SCM", choose **Git** and provide your GitHub repository URL
4. Click **Build Now**
5. Go to: `http://localhost:8080` → Your deployed app will be visible

---

## ✅ Result
This project builds, tests, and deploys automatically using Jenkins in a CI/CD pipeline.

---

## Example Stages in Jenkins
- **Build** → ✅
- **Test** → ✅
- **Deploy** → ✅

Each stage will be displayed in Jenkins with green check marks if all goes well.
