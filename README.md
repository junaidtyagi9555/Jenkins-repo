# 🚀 Node.js Todo App – CI/CD with Jenkins on AWS

This project demonstrates a **complete CI/CD pipeline** using **Jenkins** deployed on an **AWS EC2 (Free Tier) Ubuntu instance**, integrated with **GitHub** and **Docker**. Every code push automatically triggers Jenkins to build and deploy the application.

---

## 📌 Project Overview

- Node.js based Todo List application
- Jenkins installed on AWS EC2 (Ubuntu)
- Source code hosted on GitHub
- Docker used for containerization
- Jenkins Freestyle Job for CI/CD automation

Application is accessible via browser after deployment.

---

## 🛠️ Tech Stack

- **Cloud**: AWS EC2 (Free Tier)
- **OS**: Ubuntu 22.04 LTS
- **CI/CD Tool**: Jenkins
- **Containerization**: Docker
- **Runtime**: Node.js
- **Source Control**: GitHub

---

## 🔁 CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pulls latest code from repository
3. Jenkins executes shell commands:
   - Stops old container
   - Removes old container
   - Builds new Docker image
   - Runs a new container
4. Updated application is deployed automatically

---

## ⚙️ Jenkins Job Configuration

### Build Step – Execute Shell

```bash
docker stop node-todo-app || true
docker rm node-todo-app || true
docker build -t node-app .
docker run -d --name node-todo-app -p 8000:8000 node-app
```


## 📸 Screenshots

| Description | Screenshot |
|--------------|-------------|
| jenkins(build) | ![jenkins build](jenkins(build).jpg) |
| jenkins(Execute-shell) | ![Execute shell](execute(shell).jpeg) |
| Final Website Result | ![Website Result](auto-build(result).jpg) |

---

## ✅ Key Learnings

- Jenkins installation and configuration on AWS EC2
- GitHub integration with Jenkins
- Docker-based application deployment
- Automating build and deployment using Jenkins
- Real-world CI/CD pipeline implementation

---

## 📄 Resume Description

**CI/CD Pipeline using Jenkins on AWS**
- Deployed Jenkins on AWS EC2 (Ubuntu Free Tier)
- Integrated Jenkins with GitHub for automated builds
- Containerized Node.js application using Docker
- Implemented automated deployment using Jenkins Freestyle Job

---

## 👤 Author

**Junaid Tyagi**  
Aspiring DevOps / Cloud Engineer

---

⭐ If you like this project, don’t forget to star the repository!

