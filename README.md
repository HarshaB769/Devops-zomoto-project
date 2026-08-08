Zomoto DevOps Project

A complete DevOps CI/CD, containerization, security, monitoring, and Kubernetes deployment project for a Zomato-inspired web application.
The project demonstrates how a frontend application can be taken from source code through automated quality checks and security scans, packaged into a Docker image, pushed to Docker Hub, deployed as a container, and then deployed to an AWS EKS Kubernetes cluster with monitoring and GitOps tooling.


📌 Project Overview

This project combines a React-based web application with a complete DevOps workflow using:

Git / GitHub – source-code management

Jenkins – CI/CD automation

SonarQube – static code-quality analysis

OWASP Dependency-Check – dependency vulnerability scanning

Trivy – filesystem/container security scanning

Docker – application containerization

Docker Hub – container image registry

Docker Scout – container image vulnerability analysis and recommendations

AWS EC2 – Jenkins and monitoring infrastructure

Prometheus – metrics collection

Node Exporter – host-level metrics

Grafana – monitoring dashboards

Amazon EKS – Kubernetes cluster

kubectl / eksctl / Helm – Kubernetes administration and deployment

Argo CD – Kubernetes deployment/GitOps workflow

The supplied project resources describe the complete flow from provisioning Ubuntu servers and installing the DevOps tools through EKS deployment and monitoring.


🏗️ Project Structure

Zomoto-devops-project/
│
├── Kubernetes/
│   ├── deployment.yml
│   ├── node-service.yml
│   └── service.yml
│
├── public/
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
│
├── src/
│   ├── assets/
│   │   └── images/
│   │       ├── App-Store.png
│   │       ├── BackGround.png
│   │       ├── Dine-Out.png
│   │       ├── Favicon.png
│   │       ├── Google-Play.png
│   │       ├── Iphone.png
│   │       ├── Night-Life.png
│   │       ├── Online-Food.png
│   │       ├── Zomato-Logo.png
│   │       ├── blackLogo.webp
│   │       ├── collection1.webp
│   │       ├── collection2.webp
│   │       ├── collection3.webp
│   │       └── collection4.webp
│   │
│   ├── components/
│   │   ├── AccContainer/
│   │   ├── Accordian/
│   │   ├── CTA/
│   │   ├── Card/
│   │   ├── Cities/
│   │   ├── Collections/
│   │   ├── Footer/
│   │   └── Header/
│   │
│   ├── App.js
│   ├── app.scss
│   ├── data.js
│   └── index.js
│
├── .gitignore
├── Dockerfile
├── Jenkinsfile
├── package.json
└── package-lock.json


🔄 DevOps Workflow

Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ├── Clean Workspace
    ├── Git Checkout
    ├── SonarQube Analysis
    ├── Quality Gate
    ├── npm install
    ├── OWASP Dependency Check
    ├── Trivy File Scan
    ├── Docker Image Build
    ├── Push Image to Docker Hub
    ├── Docker Scout Analysis
    ├── Deploy Docker Container
    └── Email Notification
             │
             ▼
       Docker Container
             │
             ▼
       Kubernetes / AWS EKS
             │
             ├── Argo CD
             │
             └── Prometheus + Node Exporter
                         │
                         ▼
                      Grafana
                      

🎓 What This Project Demonstrates

1. By completing this project, you demonstrate practical experience with:

2. Building and running a frontend application.

3. Creating a Docker image.

4. Automating CI/CD using Jenkins.

5. Performing static code analysis with SonarQube.

6. Scanning dependencies with OWASP Dependency-Check.

7. Scanning files/images with Trivy.

8. Analyzing container images with Docker Scout.

9. Publishing images to Docker Hub.

10. Deploying applications using Docker.

11. Creating an AWS EKS Kubernetes cluster.

12. Deploying an application to Kubernetes.

13. Managing Kubernetes workloads with Argo CD.

14. Collecting metrics with Prometheus.

15. Monitoring infrastructure using Node Exporter.

16. Visualizing metrics using Grafana.


⭐ Project Highlights

CI/CD → Security → Containerization → Kubernetes → GitOps → Monitoring

This project brings together the major stages of a modern DevOps workflow and demonstrates how an application can move from source code to a monitored Kubernetes deployment.
