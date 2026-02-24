🚀 Kubernetes Microservices with GitOps
End-to-End DevOps Implementation on AWS EKS
<p align="center"> <img src="https://img.shields.io/badge/AWS-EKS-orange?style=for-the-badge&logo=amazonaws"> <img src="https://img.shields.io/badge/Kubernetes-Orchestration-blue?style=for-the-badge&logo=kubernetes"> <img src="https://img.shields.io/badge/Docker-Containerization-blue?style=for-the-badge&logo=docker"> <img src="https://img.shields.io/badge/Jenkins-CI%2FCD-red?style=for-the-badge&logo=jenkins"> <img src="https://img.shields.io/badge/ArgoCD-GitOps-orange?style=for-the-badge&logo=argo"> <img src="https://img.shields.io/badge/Helm-Package%20Manager-0F1689?style=for-the-badge&logo=helm"> <img src="https://img.shields.io/badge/Prometheus-Monitoring-E6522C?style=for-the-badge&logo=prometheus"> <img src="https://img.shields.io/badge/Grafana-Visualization-F46800?style=for-the-badge&logo=grafana"> </p>
📌 Project Overview

This project demonstrates a Production-Grade Microservices Deployment Pipeline using modern DevOps practices.

It covers the complete workflow from:

💻 Local Development → 📦 Docker → 🔁 CI/CD → ☸️ Kubernetes → 🌐 Ingress → 📊 Monitoring → 🔄 GitOps Automation

The application is deployed on AWS EKS, monitored using Prometheus & Grafana, and managed using ArgoCD (GitOps model).

🏗️ Architecture Flow
Developer
   ↓
GitHub Repository
   ↓
Jenkins CI/CD Pipeline
   ↓
Docker Image Build & Push
   ↓
AWS EKS Cluster
   ↓
Kubernetes Deployment + Ingress
   ↓
Users Access Application
   ↓
Prometheus → Grafana (Monitoring)
   ↓
ArgoCD (GitOps Continuous Deployment)


🛠️ Tech Stack
🔹 Category	        🚀 Tools Used
☁️ Cloud	            AWS EC2, AWS EKS
🔁 CI/CD	            Jenkins
🐳 Containerization	    Docker
☸️ Orchestration	    Kubernetes
🔄 GitOps	            ArgoCD
📦 Package Manager	    Helm
📊 Monitoring	        Prometheus
📈 Visualization	    Grafana
🌐 Networking	        NGINX Ingress Controller


🚀 Key Features

✔️ Automated CI/CD Pipeline
✔️ Docker Image Versioning
✔️ Path-Based Routing with Ingress
✔️ GitOps Continuous Deployment
✔️ Real-Time Cluster Monitoring
✔️ Production-Level Troubleshooting Setup
✔️ Load Balancer Exposure

🔁 CI/CD Pipeline Workflow

Code pushed to GitHub

Jenkins triggers pipeline

Docker image build & push to DockerHub

AWS EKS kubeconfig updated

Kubernetes deployment updated

Ingress configured

Application URL generated

Health check validation

📊 Monitoring Setup
🔹 Prometheus

Scrapes metrics from:

Kubernetes cluster

Node Exporter

Jenkins

🔹 Grafana Dashboards

Node Exporter Dashboard (ID: 1860)

Jenkins Performance Dashboard (ID: 9964)

🔄 GitOps with ArgoCD

ArgoCD deployed using Helm

Application linked to GitHub repository

Automatic synchronization enabled

Self-healing and auto-deployment supported

📂 Repository Structure
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── argocd/
│   └── application.yaml
│
├── helm/
│
├── Dockerfile
├── Jenkinsfile
└── README.md
🌐 Application Access

After deployment:

Home Page:     http://<LoadBalancer-URL>/
About Page:    http://<LoadBalancer-URL>/about
Services Page: http://<LoadBalancer-URL>/services
Contact Page:  http://<LoadBalancer-URL>/contact
🎯 Interview Highlights

During interviews, this project demonstrates:

Practical Kubernetes deployment knowledge

Real-time CI/CD automation

GitOps workflow understanding

Cloud-native monitoring setup

Production troubleshooting skills

Infrastructure management using CLI tools

🧠 Challenges Solved

Image version conflicts

Kubernetes rollout failures

LoadBalancer pending state

Prometheus target configuration

Jenkins credential handling

ArgoCD service exposure