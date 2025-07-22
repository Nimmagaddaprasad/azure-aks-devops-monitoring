# Azure AKS Deployment with Terraform, Azure DevOps, Prometheus & Grafana

## 🧩 Project Overview

This project demonstrates end-to-end infrastructure automation using:
- **Terraform** to provision Azure AKS
- **Azure DevOps Pipelines** for CI/CD
- **Kubernetes** to deploy a sample app
- **Prometheus & Grafana** for monitoring

Designed for DevOps/SRE interviews, this mini-project highlights Infrastructure as Code, container orchestration, CI/CD automation, and observability.

---

## ⚙️ Tech Stack

- Azure AKS (Kubernetes Service)
- Terraform
- Azure DevOps (Pipelines)
- Prometheus & Grafana (via Helm)
- Kubernetes manifests (YAML)
- NGINX sample app

---

## 🚀 Deployment Stages

### 1️⃣ Infrastructure Provisioning (Terraform)
- Creates:
  - Azure Resource Group
  - AKS Cluster with 2 nodes
  - System-assigned identity
- Run manually or via Azure DevOps pipeline

### 2️⃣ Kubernetes Deployment
- NGINX app deployed via `kubectl`
- Service of type `LoadBalancer` exposed
- Prometheus + Grafana deployed via Helm charts

### 3️⃣ Monitoring Stack
- Prometheus scrapes AKS metrics
- Grafana dashboards for cluster observability
- Optional alerts can be configured

---

## 🗂️ Folder Structure

```bash
.
├── terraform/           # Terraform code for Azure infra
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
├── manifests/           # K8s deployment YAMLs
│   ├── deployment.yaml
│   ├── service.yaml
├── pipelines/
│   └── azure-pipelines.yml
└── README.md
