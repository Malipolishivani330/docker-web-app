# Docker Web Application

A simple web application containerized using Docker and deployed locally using Docker Compose and Nginx.

## 📌 Project Overview

This project demonstrates how to containerize and run a web application using Docker.

The application is built with HTML and served through an Nginx web server inside a Docker container. Docker Compose is used to simplify container management and deployment.

## 🛠️ Technologies Used

- Docker
- Docker Compose
- Nginx
- HTML

## 📂 Project Structure

```text
docker-web-app/
│
├── index.html
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── README.md
🚀 Application Workflow
Source Code
     ↓
Dockerfile
     ↓
Docker Image
     ↓
Docker Container
     ↓
Docker Compose
     ↓
Running Web Application

⚙️ How to Run the Application
1. Clone the repository
Command:- git clone https://github.com/Malipolishivani330/docker-web-app.git
2. Navigate to the project directory
Command:- cd docker-web-app
3. Build and start the container
Command:- docker compose up -d --build
4. Verify the running container
Command:- docker ps
5. Access the application

Open your browser and visit:
http://localhost:8080

🐳 Docker Commands Used:_-

docker build -t docker-web-app .
docker images
docker ps
docker compose up -d
docker compose down
docker logs docker-web-container

✅ Project Status

Successfully completed Docker containerization of a web application using Nginx and Docker Compose.

The application is running successfully inside a Docker container and can be accessed through:

http://localhost:8080

📚 Key Learning Outcomes:-
Understanding Docker images and containers
Creating and using a Dockerfile
Building Docker images
Running containers
Using Nginx inside Docker
Managing containers with Docker Compose
Understanding container networking
Using .dockerignore to optimize Docker builds

👩‍💻 Author

Malipolishivani

GitHub: https://github.com/Malipolishivani330
