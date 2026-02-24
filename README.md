<div align="center">

# 🚀 Kubernetes Microservices with GitOps  
### 🌩️ End-to-End DevOps Implementation on AWS EKS

<p align="center">
  <img src="https://img.shields.io/badge/AWS-EKS-orange?style=for-the-badge&logo=amazonaws">
  <img src="https://img.shields.io/badge/Kubernetes-Orchestration-blue?style=for-the-badge&logo=kubernetes">
  <img src="https://img.shields.io/badge/Docker-Containerization-blue?style=for-the-badge&logo=docker">
  <img src="https://img.shields.io/badge/Jenkins-CI/CD-red?style=for-the-badge&logo=jenkins">
  <img src="https://img.shields.io/badge/ArgoCD-GitOps-orange?style=for-the-badge&logo=argo">
  <img src="https://img.shields.io/badge/Prometheus-Monitoring-E6522C?style=for-the-badge&logo=prometheus">
  <img src="https://img.shields.io/badge/Grafana-Visualization-F46800?style=for-the-badge&logo=grafana">
</p>

</div>

---

## 📌 Project Overview

This project demonstrates a **production-ready DevOps pipeline** implementing:

- 🔁 CI/CD with Jenkins  
- 🐳 Docker containerization  
- ☸️ Kubernetes orchestration on AWS EKS  
- 🔄 GitOps deployment using ArgoCD  
- 📊 Monitoring with Prometheus & Grafana  
- 🌐 Path-based routing using NGINX Ingress  

The system follows **GitOps principles**, ensuring automated, scalable, and self-healing deployments.

---

## 🏗️ Architecture Diagram

```mermaid
flowchart TD
    Dev[👨‍💻 Developer] -->|git push| GitHub[🐙 GitHub Repository]

    GitHub -->|Webhook Trigger| Jenkins[🔧 Jenkins CI/CD]
    Jenkins -->|Build Image| Docker[🐳 Docker Build]
    Docker -->|Push Image| DockerHub[📦 DockerHub]

    GitHub -->|K8s Manifests| ArgoCD[🔄 ArgoCD GitOps]
    ArgoCD -->|Auto Sync| EKS[☸️ AWS EKS Cluster]

    EKS --> Deployment[📦 Kubernetes Deployment]
    Deployment --> Service[🌐 Service]
    Service --> Ingress[🚦 NGINX Ingress]
    Ingress --> Users[🌍 End Users]

    EKS --> Prometheus[📊 Prometheus]
    Prometheus --> Grafana[📈 Grafana Dashboard]

    style Dev fill:#e3f2fd
    style GitHub fill:#f3e5f5
    style Jenkins fill:#ffebee
    style Docker fill:#fff3e0
    style DockerHub fill:#fff3e0
    style ArgoCD fill:#e8f5e9
    style EKS fill:#f1f8e9
    style Prometheus fill:#fbe9e7
    style Grafana fill:#ede7f6
```

### ☸️ AWS EKS Cluster Overview

<div align="center">
<img src="Screenshot/EKS_Dashboard.png" width="1000"/>
</div>

📌 Shows:
- Worker nodes
- Node group status
- Cluster health
- Running workloads

---

## 🛠️ Tech Stack

| Category | Tools Used |
|----------|------------|
| ☁️ Cloud | AWS EC2, AWS EKS |
| 🔁 CI/CD | Jenkins |
| 🐳 Containerization | Docker, DockerHub |
| ☸️ Orchestration | Kubernetes |
| 🔄 GitOps | ArgoCD |
| 📦 Package Manager | Helm |
| 📊 Monitoring | Prometheus, Node Exporter |
| 📈 Visualization | Grafana |
| 🌐 Networking | NGINX Ingress Controller |

---

## ☁️ AWS Infrastructure Setup

### 🖥️ EC2 Instance Dashboard

<div align="center">
<img src="Screenshot/EC2_Dashboard.png" width="1000"/>
</div>

📌 EC2 Configuration:
- Ubuntu Server
- Jenkins Installed
- Docker Installed
- kubectl & eksctl configured
- Connected to AWS EKS cluster

---

## 🔁 CI/CD Workflow

### 1️⃣ Code Commit
- Developer pushes code to GitHub
  
---

### 2️⃣ Jenkins Pipeline Execution
<div align="center">
<img src="Screenshot/jenkins_pipeline.png" width="1000"/>
</div>

📌 Pipeline Stages:
- Source Code Checkout  
- Docker Image Build  
- Docker Image Push to DockerHub  
- Kubernetes Manifest Update  
- Deployment to AWS EKS  

---
---

### 🐳 DockerHub Repository

<div align="center">
<img src="Screenshot/DockerHub_Dashboard.png" width="900"/>
</div>

📌 Displays:
- Versioned Docker images
- Immutable tagging strategy
- Image push from Jenkins pipeline

---

### 3️⃣ GitOps Deployment
- ArgoCD monitors repository
- Auto-syncs changes to cluster
- Maintains desired state

### 4️⃣ Monitoring
- Prometheus scrapes metrics
- Grafana visualizes dashboards
- Alerts configured for failures

---

## 🌐 Application Access

### 📸 Live Application Preview

<div align="center">

### 🏠 Home Page
<img src="Screenshot/Using_ingress_home_page.png" width="900"/>

### ℹ️ About Page
<img src="Screenshot/Using_ingress_About_page.png" width="900"/>

### 🛠️ Services Page
<img src="Screenshot/Using_ingress_Module_page.png" width="900"/>

### 📞 Contact Page
<img src="Screenshot/Using_ingress_Contact_Page.png" width="900"/>

</div>




To retrieve LoadBalancer:

```bash
kubectl get svc -n ingress-nginx
```

---

## 📊 Monitoring & GitOps Dashboards

### 🔥 Prometheus Dashboard

<div align="center">
<img src="Screenshot/Prometheus_Dashboard.png" width="900"/>
</div>

📌 Displays:
- Kubernetes pod metrics  
- CPU & Memory usage  
- Target health status  
- Node metrics  

---

### 📈 Grafana Dashboard

<div align="center">
<img src="Screenshot/Grafana_Dashboard.png" width="900"/>
</div>

📌 Shows:
- Cluster resource utilization  
- Node Exporter metrics  
- Application performance graphs  
- Real-time monitoring visualization  

---

### 🔄 ArgoCD Dashboard

<div align="center">
<img src="Screenshot/ArgoCd_Sync_with_K8s.png" width="900"/>
</div>

📌 Provides:
- Application sync status  
- Health status (Healthy / Degraded)  
- Auto-sync configuration  
- GitOps deployment tracking  

---

## 🔄 GitOps Implementation

- ArgoCD installed via Helm
- Auto-sync enabled
- Self-healing deployments
- Rollback capability
- Declarative infrastructure

---

## 🎯 Key Features

✅ Automated CI/CD Pipeline  
✅ Immutable Docker Image Tagging  
✅ Kubernetes Rolling Updates  
✅ Path-Based Routing  
✅ Horizontal Pod Autoscaling  
✅ Cluster Autoscaler  
✅ Production Monitoring  
✅ GitOps Workflow  
✅ Self-Healing Deployments  

---

## 📖 Getting Started

### Clone Repository

```bash
git clone https://github.com/VishakhaPatil-03/Kubernetes-Microservices-with-GitOps.git
cd Kubernetes-Microservices-with-GitOps
```

### Deploy via ArgoCD

```bash
kubectl apply -f argocd/application.yaml
```

---

## 🔐 Network & Security Group Configuration

To ensure proper communication between services, the following ports were configured in the AWS Security Group attached to the EC2/EKS instances.

### 📍 How to Configure Security Group

1. Go to AWS Console  
2. Navigate to **EC2 → Instances**  
3. Select your instance  
4. Click **Security** tab  
5. Click on the attached **Security Group**  
6. Edit **Inbound Rules**  
7. Add the required ports listed below  

---

## 🌐 Required Inbound Ports

| Port | Protocol | Purpose |
|------|----------|----------|
| 22 | TCP | SSH Access |
| 80 | TCP | HTTP Web Application |
| 443 | TCP | HTTPS Secure Access |
| 8080 | TCP | Jenkins Server |
| 6443 | TCP | Kubernetes API Server |
| 9090 | TCP | Prometheus Dashboard |
| 9100 | TCP | Node Exporter Metrics |
| 30000-32767 | TCP | Kubernetes NodePort Services |
| 1000-10000 | TCP | Custom Application Ports |
| 25 | TCP | SMTP (Email Sending) |
| 465 | TCP | SMTPS (Secure Email) |

---

## 🧠 Port Explanation

- **80 / 443** → Application access via Ingress  
- **8080** → Jenkins UI  
- **6443** → Kubernetes API communication  
- **30000–32767** → Kubernetes NodePort range  
- **9090** → Prometheus monitoring  
- **9100** → Node Exporter metrics collection  
- **SMTP / SMTPS** → Email notifications from Jenkins or Alertmanager  

---

⚠️ **Important Security Note**

For production environments:
- Restrict SSH (22) to your IP only  
- Avoid opening wide port ranges to `0.0.0.0/0`  
- Use IAM Roles and private networking where possible  
- Prefer Load Balancer instead of exposing NodePort publicly  

---

## 🎯 Interview Highlights

This project demonstrates:

- End-to-End DevOps Automation
- Kubernetes Production Deployment
- Jenkins Pipeline as Code
- Docker Image Optimization
- AWS EKS Cluster Management
- GitOps Methodology
- Monitoring & Observability
- Infrastructure Security Best Practices

---
