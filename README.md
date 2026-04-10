# Kubernetes CI/CD Pipeline with AWS EKS 🚀

This project demonstrates a production-grade CI/CD pipeline that automatically builds, containerizes, and deploys a Spring Boot application to AWS EKS using GitHub Actions and secure OIDC authentication.


## 🧠 Architecture

Code → GitHub Actions → Docker Build → Docker Hub → AWS EKS → Kubernetes Deployment

- GitHub Actions handles CI/CD automation  
- Docker Hub stores versioned images  
- AWS EKS runs the application  
- Kubernetes performs rolling updates  


## 🔄 CI/CD Flow

1. Push code to main branch  
2. GitHub Actions builds Spring Boot app  
3. Docker image is created and tagged with commit SHA  
4. Image is pushed to Docker Hub  
5. GitHub Actions authenticates to AWS using OIDC  
6. Deployment is updated in EKS using kubectl  
7. Kubernetes performs rolling update (zero downtime)


## 🔐 Security

- Uses GitHub OIDC for AWS authentication (no static credentials)  
- IAM role assumption with temporary credentials  
- No AWS secrets stored in GitHub  


## 📸 Proof of Deployment

### CI/CD Pipeline Success
![Pipeline](screenshots/04-ci-cd-eks-success.png)

### Rolling Update
![Pods](screenshots/05-eks-rolling-update.png)

### Application Running on EKS
![App](screenshots/03-eks-app.png)


## ⚙️ Tech Stack

- Java (Spring Boot)
- Docker
- Kubernetes (AWS EKS)
- GitHub Actions
- AWS IAM (OIDC)

## 💡 Key Features

- Automated CI/CD pipeline  
- Secure AWS authentication using OIDC  
- Versioned Docker images (commit SHA)  
- Zero-downtime deployment with rolling updates  
- Optimized pipeline triggers using path filters  


## 🚀 How It Works

Any change in application or Docker configuration automatically triggers the pipeline, builds a new image, and deploys it to AWS EKS without manual intervention.


## 👨‍💻 About Me

I am a DevOps and Cloud Engineer specializing in Kubernetes, CI/CD automation, and AWS infrastructure.

This project demonstrates my ability to build secure, production-ready deployment pipelines.