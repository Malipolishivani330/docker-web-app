# 🐳 Docker Web Application with CI/CD

A containerized web application built with **HTML and Nginx**, packaged using **Docker**, managed with **Docker Compose**, and automatically validated through a **GitHub Actions CI/CD pipeline**.

## 📌 Project Overview

This project demonstrates a complete containerization and CI/CD workflow:

**Source Code → Dockerfile → Docker Image → Docker Container → Docker Compose → GitHub Actions → Application Verification**

The application is served using **Nginx inside a Docker container**. GitHub Actions automatically builds the Docker image, starts the container, checks its status and logs, and verifies that the web application is responding successfully.

---

# 🚀 Module 4 — Docker & Containerization

## Technologies Used

- Docker
- Docker Compose
- Nginx
- HTML

## 📂 Project Structure

```text
docker-web-app/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml
│
├── Screenshots/
│
├── index.html
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── README.md
🐳 Dockerfile

The application uses the lightweight nginx:alpine image and copies the custom HTML page into Nginx's web root.
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
⚙️ Run Locally
1. Clone the repository
Command:- git clone https://github.com/Malipolishivani330/docker-web-app.git
2. Navigate to the project
Command:- cd docker-web-app
3. Build and start the application
Command:-docker compose up -d --build
4. Check the running container
Command:-docker ps
5. Access the application

Open:
http://localhost:8080
🐳 Docker Commands Used
docker build -t docker-web-app .
docker images
docker ps
docker compose up -d
docker compose down
docker logs docker-web-container
🔄 Module 5 — DevOps, CI/CD & Monitoring
GitHub Actions CI/CD Pipeline

The project includes a GitHub Actions workflow located at:
.github/workflows/ci-cd.yml
Pipeline Workflow
GitHub Push
     ↓
Checkout Code
     ↓
Build Docker Image
     ↓
Run Docker Container
     ↓
Wait for Application
     ↓
Check Container Status
     ↓
Check Container Logs
     ↓
Verify Application
🔧 CI/CD Pipeline Tasks

The pipeline automatically:

Checks out the latest source code.
Builds the Docker image.
Runs the Docker container.
Waits for the application to start.
Checks container status.
Reviews container logs.
Verifies the application using curl.

🛠️ Troubleshooting & Problem Solving

During CI/CD implementation, the application verification stage initially failed with:
curl: (56) Recv failure: Connection reset by peer
Troubleshooting approach
Reviewed GitHub Actions workflow logs.
Identified the failing application verification step.
Confirmed that the Docker image built successfully.
Confirmed that the container started successfully.
Added an application startup wait period.
Added container status and log checks.
Improved the HTTP verification using retry logic.
Re-ran the pipeline and validated the successful deployment.

This demonstrated a systematic approach to CI/CD troubleshooting, Docker debugging, log analysis, and application health verification.

✅ Final Result

The Docker application is successfully containerized and the GitHub Actions CI/CD workflow completes successfully.

Application
http://localhost:8080
GitHub Repository

https://github.com/Malipolishivani330/docker-web-app

📚 Key Learning Outcomes
Docker images and containers
Dockerfile creation and optimization
Nginx web server
Docker Compose
Container networking and port mapping
Container lifecycle management
Docker logs and troubleshooting
Git and GitHub workflows
GitHub Actions
CI/CD automation
Application health verification
Debugging pipeline failures
👩‍💻 Author

Malipolishivani

GitHub:
https://github.com/Malipolishivani330
