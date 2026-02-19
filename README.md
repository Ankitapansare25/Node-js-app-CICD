# 🚀 Node.js CI/CD Pipeline using Jenkins & AWS EC2

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline for deploying a Node.js application using Jenkins and AWS EC2.

The pipeline automatically:

- Clones the repository from GitHub
- Uploads application files to AWS EC2
- Installs dependencies
- Starts or restarts the Node.js app using PM2

This project showcases a real-world DevOps deployment workflow.

---

## 🛠️ Tech Stack

- Node.js
- Jenkins (Declarative Pipeline)
- GitHub
- AWS EC2 (Ubuntu)
- PM2
- SSH

---

## 📂 Project Architecture

```
Developer → GitHub → Jenkins → AWS EC2 → PM2 → Node.js App
```

### Workflow:

1. Developer pushes code to GitHub
2. Jenkins pipeline triggers
3. Code is deployed to EC2 via SSH
4. PM2 starts or restarts the application

---

## ⚙️ Jenkins Pipeline Stages

### 1️⃣ Clone Repository
Clones the `main` branch from GitHub.

### 2️⃣ Upload Files to EC2
Uses Jenkins SSH credentials and transfers files using `scp`.

### 3️⃣ Install Dependencies & Start App
Executes the following commands on EC2:

- `npm install`
- `pm2 start app.js --name node-app`
- If already running → `pm2 restart node-app`
---

## 🧩 Jenkinsfile

This project uses **Pipeline as Code** with Declarative Syntax.

Features included:

- Environment configuration
- Multiple pipeline stages
- SSH Agent integration
- Post-build success and failure handling

---

## 📦 Setup Instructions

### Step 1: Launch AWS EC2
- Create Ubuntu instance
- Install Node.js
- Install PM2

### Step 2: Install Jenkins
- Configure SSH credentials
- Create a new Pipeline job
- Connect to GitHub repository

### Step 3: Run Pipeline
- Click **Build Now**
- Application will deploy automatically

---

## 🌐 Access the Application

Open in browser:

```
http://<EC2-Public-IP>:3000
```

---

## 🎯 Key Learning Outcomes

- CI/CD Automation
- Jenkins Declarative Pipeline
- SSH-based Deployment
- PM2 Process Management
- Real-world DevOps Workflow

---

## 👩‍💻 Author

**Ankita Pansare**  

---
