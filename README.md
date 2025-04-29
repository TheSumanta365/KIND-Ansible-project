# KIND + Ansible Kubernetes Deployment Project

![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Ansible](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

Automates deployment of a Java application to a local Kubernetes cluster using Kind and Ansible.

## 📌 Features

- **Local Kubernetes Cluster**: Creates a single-node cluster using Kind
- **Ansible Automation**: Handles Docker build and Kubernetes deployment
- **Java Application**: Simple Spring Boot demo app containerization
- **Service Exposure**: NodePort service for local access

## 🚀 Quick Start

### Prerequisites
- Docker
- Kind
- Ansible
- kubectl

### Deployment
```bash
# 1. Clone repository
git clone https://github.com/TheSumanta365/KIND-Ansible-project.git
cd KIND-Ansible-project

# 2. Run Ansible playbook
ansible-playbook ansible/deploy.yml

# 3. Access application
kubectl port-forward svc/java-app 8080:80
curl http://localhost:8080
