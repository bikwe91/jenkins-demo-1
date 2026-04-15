# 🚀 Jenkins CI/CD Pipeline with Docker & AWS

This project demonstrates a complete CI/CD pipeline using Jenkins, Docker, Docker Hub, and AWS EC2.

## 📌 Project Overview
This pipeline automatically builds, pushes, and deploys a Dockerized web application whenever code is pushed to GitHub.

## 🛠️ Tech Stack
- Jenkins (CI/CD)
- Docker
- Docker Hub
- AWS EC2
- GitHub Webhooks

## ⚙️ Pipeline Workflow

1. Developer pushes code to GitHub  
2. GitHub webhook triggers Jenkins  
3. Jenkins pulls the latest code  
4. Docker image is built  
5. Image is tagged and pushed to Docker Hub  
6. Application is deployed on AWS EC2  
7. App is accessible via public IP  

## 🧪 Pipeline Stages
- Checkout
- Build Docker Image
- Login to Docker Hub
- Push Image
- Deploy Container
- Verify Deployment

## 🌐 Live Application
http://3.238.144.218:8081

## 📦 Docker Image
https://hub.docker.com/r/bikwe1991/my-app

## 💡 Key Features
- Automated CI/CD pipeline  
- Dockerized deployment  
- Real-time deployment on EC2  
- GitHub webhook integration  

## 📸 Screenshots
(Add Jenkins, Docker Hub, and app screenshots here)

---

## 👨‍💻 Author
Fabrice Bikwe
