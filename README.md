# 🚀 Django Notes App with CI/CD Pipeline
This is a simple notes app built with React and Django.

## 📌 Project Overview
This project is a Django-based Notes Application integrated with a complete CI/CD pipeline using Jenkins and Docker. The pipeline automates the process of building, testing, containerizing, and deploying the application on an AWS EC2 instance.

## Requirements
1. Python 3.9
2. Node.js
3. React

## 🏗️ Architecture
Developer → GitHub → Jenkins Pipeline → Docker Build → DockerHub → AWS EC2 Deployment

## ⚙️ Tech Stack

- Backend: Django (Python)
- CI/CD: Jenkins (Pipeline as Code)
- Containerization: Docker, Docker Compose
- Cloud: AWS EC2
- Version Control: Git & GitHub
- OS: Linux (Ubuntu)

## 📂 Important Files

- Jenkinsfile → Defines CI/CD pipeline stages
- Dockerfile → Builds application image
- docker-compose.yml → Manages multi-container setup
- requirements.txt → Python dependencies

## 🔐 Features

- Automated CI/CD pipeline
- Dockerized Django application
- Cloud deployment on AWS EC2
- Scalable and production-ready structure
## 🚀 Future Improvements

- Add automated testing stage
- Implement Kubernetes deployment
- Add monitoring (Prometheus + Grafana)
