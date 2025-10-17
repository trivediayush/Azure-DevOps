# Azure DevOps – Automated Voting Application CI/CD Pipeline

## Overview
This project demonstrates an end-to-end **Continuous Integration (CI)** and **Continuous Deployment (CD)** setup using **Azure DevOps** for a distributed, containerized voting application.  
The application enables users to vote between two options and view real-time results, integrating multiple microservices built with **Python**, **.NET**, **Redis**, **PostgreSQL**, and **Node.js**.  
It implements industry-grade DevOps practices with automation, scalability, and cloud-native deployment through **Azure Kubernetes Service (AKS)**.

---

# Project Link:
👉 `https://ayushtrivedi890@dev.azure.com/ayushtrivedi890/Voting-app/_git/Voting-app` 👈

## Architecture
The solution consists of the following components:
- **Front-End (Python):** Web interface for users to vote.
- **Redis:** Collects and caches incoming votes.
- **Worker (.NET):** Processes votes and stores them in the database.
- **Database (PostgreSQL):** Persistent data layer backed by Docker volumes.
- **Results App (Node.js):** Displays live voting results.

All services are containerized via **Docker** and orchestrated through **Azure Kubernetes Service (AKS)**.

---

## Key Features
- **Automated CI pipeline** using Azure DevOps for building, testing, and integrating services.
- **Automated CD pipeline** deploying containers to AKS with VM Scale Sets.
- **Containerized microservices** ensuring environmental consistency.
- **Scalable and reliable** deployment using cloud-native infrastructure.
- **Real-time processing** of votes through Redis and .NET worker service.

---

## Technology Stack
| Component    | Technology Used |
|---------------|----------------|
| CI/CD         | Azure DevOps |
| Front-End     | Python (Flask) |
| Worker        | .NET Core |
| Data Store    | Redis |
| Database      | PostgreSQL (Docker volume) |
| Result App    | Node.js |
| Containerisation | Docker |
| Deployment    | Azure Kubernetes Service (AKS) |
| Scaling       | Azure Virtual Machine Scale Sets (VMSS) |

---

## Pipeline Workflow

### Continuous Integration (CI)
1. **Code Commit:** Developers push changes to Azure Repos.
2. **Build Trigger:** Azure DevOps pipeline builds each service.
3. **Testing:** Automated unit and integration tests executed.
4. **Image Build:** Docker images created and pushed to Azure Container Registry (ACR).

### Continuous Deployment (CD)
1. **Deployment:** Updated images deployed to AKS.
2. **Scaling:** VM Scale Sets handle horizontal scaling.
3. **Validation:** Application monitored and verified post-deployment.

---

## Setup Instructions

### Prerequisites
- Active **Azure Subscription**
- **Docker** and **Kubernetes CLI** installed locally
- Access to **Azure Container Registry (ACR)**
- **Azure CLI** configured
