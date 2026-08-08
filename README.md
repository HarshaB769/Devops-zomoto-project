# 🍽️ Zomoto DevOps Project

<p align="center">
  <strong>A complete DevOps CI/CD, containerization, security, monitoring, and Kubernetes deployment project for a Zomato-inspired web application.</strong>
</p>

<p align="center">
  <em>
    Source Code → CI/CD → Security → Docker → Kubernetes → GitOps → Monitoring
  </em>
</p>

---

## 📌 Project Overview

<p>
This project demonstrates how a frontend application can be taken from source code through
automated quality checks and security scans, packaged into a Docker image, pushed to Docker Hub,
deployed as a container, and then deployed to an AWS EKS Kubernetes cluster with monitoring and
GitOps tooling.
</p>

<p>
The project combines a React-based web application with a complete modern DevOps workflow.
</p>

---

## 🛠️ Technologies Used

<table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Technology</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Source Control</td>
      <td>Git / GitHub</td>
      <td>Source-code management</td>
    </tr>
    <tr>
      <td>CI/CD</td>
      <td>Jenkins</td>
      <td>Continuous integration and deployment automation</td>
    </tr>
    <tr>
      <td>Code Quality</td>
      <td>SonarQube</td>
      <td>Static code-quality analysis</td>
    </tr>
    <tr>
      <td>Dependency Security</td>
      <td>OWASP Dependency-Check</td>
      <td>Dependency vulnerability scanning</td>
    </tr>
    <tr>
      <td>Security</td>
      <td>Trivy</td>
      <td>Filesystem and container security scanning</td>
    </tr>
    <tr>
      <td>Containerization</td>
      <td>Docker</td>
      <td>Application containerization</td>
    </tr>
    <tr>
      <td>Container Registry</td>
      <td>Docker Hub</td>
      <td>Docker image storage</td>
    </tr>
    <tr>
      <td>Container Security</td>
      <td>Docker Scout</td>
      <td>Image vulnerability analysis and recommendations</td>
    </tr>
    <tr>
      <td>Cloud</td>
      <td>AWS EC2</td>
      <td>Jenkins and monitoring infrastructure</td>
    </tr>
    <tr>
      <td>Monitoring</td>
      <td>Prometheus</td>
      <td>Metrics collection</td>
    </tr>
    <tr>
      <td>Monitoring</td>
      <td>Node Exporter</td>
      <td>Host-level metrics collection</td>
    </tr>
    <tr>
      <td>Visualization</td>
      <td>Grafana</td>
      <td>Monitoring dashboards</td>
    </tr>
    <tr>
      <td>Container Orchestration</td>
      <td>Amazon EKS</td>
      <td>Managed Kubernetes cluster</td>
    </tr>
    <tr>
      <td>Kubernetes Tools</td>
      <td>kubectl / eksctl / Helm</td>
      <td>Kubernetes administration and deployment</td>
    </tr>
    <tr>
      <td>GitOps</td>
      <td>Argo CD</td>
      <td>Kubernetes deployment management</td>
    </tr>
  </tbody>
</table>

---

## 🏗️ Project Structure

<details>
<summary><strong>📂 View Project Structure and 🔄 Devops Workflow</strong></summary>

```text
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


Devops Workflow
                    ┌─────────────────┐
                    │    Developer    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ GitHub Repository│
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ Jenkins Pipeline│
                    └────────┬────────┘
                             │
             ┌───────────────┴────────────────┐
             │                                │
             ▼                                ▼
     ┌──────────────────┐             ┌──────────────────┐
     │ Clean Workspace  │             │   Git Checkout   │
     └──────────────────┘             └──────────────────┘
             │
             ▼
     ┌──────────────────┐
     │    SonarQube     │
     │     Analysis     │
     └────────┬─────────┘
              │
              ▼
     ┌──────────────────┐
     │  Quality Gate    │
     └────────┬─────────┘
              │
              ▼
     ┌──────────────────┐
     │   npm install    │
     └────────┬─────────┘
              │
              ▼
     ┌────────────────────────┐
     │ OWASP Dependency Check │
     └───────────┬────────────┘
                 │
                 ▼
          ┌──────────────┐
          │ Trivy Scan   │
          └──────┬───────┘
                 │
                 ▼
        ┌──────────────────┐
        │ Build Docker     │
        │     Image        │
        └────────┬─────────┘
                 │
                 ▼
        ┌──────────────────┐
        │ Push to Docker   │
        │      Hub         │
        └────────┬─────────┘
                 │
                 ▼
        ┌──────────────────┐
        │  Docker Scout    │
        │     Analysis     │
        └────────┬─────────┘
                 │
                 ▼
        ┌──────────────────┐
        │ Deploy Container │
        └────────┬─────────┘
                 │
                 ▼
        ┌──────────────────┐
        │   AWS EKS /      │
        │   Kubernetes     │
        └────────┬─────────┘
                 │
        ┌────────┴─────────┐
        │                  │
        ▼                  ▼
 ┌──────────────┐   ┌──────────────────┐
 │   Argo CD    │   │    Prometheus    │
 │   GitOps     │   │ + Node Exporter │
 └──────────────┘   └────────┬─────────┘
                              │
                              ▼
                       ┌─────────────┐
                       │   Grafana   │
                       │  Dashboard  │
                       └─────────────┘
