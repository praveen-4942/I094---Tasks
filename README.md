# DevOps Internship Tasks 🚀

This repository contains the implementation of Task 01 and Task 02 completed as part of the DevOps Internship Program using Ansible and AWS Cloud services.

---

# 👨‍💻 Intern Details

| Field | Details |
|---|---|
| Name | Praveenkumar G |
| Intern ID | I094 |
| Status | Completed ✅ |

---

# 🛠️ Tools & Technologies Used

- AWS EC2
- AWS Application Load Balancer (ALB)
- AWS Security Groups
- Ansible
- Docker
- Nginx
- Linux
- Git & GitHub

---

# 📂 Repository Structure

```text
.
├── Task-01/
├── Task-02/
├── screenshots/
├── outputs/
└── README.md
```

---

# ⚙️ Pre-Requisites

A provisioning server named `praveen-server` was configured in the AWS test account.

The following setup was completed before starting the tasks:

- Configured Security Group allowing SSH only from personal IP
- Installed Ansible
- Installed boto & botocore
- Installed required Ansible Galaxy collections
- Configured AWS authentication

---

# 🚀 Task 01 — ALB with Private EC2 Instances & Nginx

## 📌 Task Description

Create Ansible playbooks such that it:

- Creates 2 EC2 instances in private subnets
- Creates an Application Load Balancer (ALB) in a public subnet
- Routes traffic from ALB to EC2 instances
- Installs Nginx in the EC2 instances
- Displays the Nginx page when accessing the ALB DNS

---

# 🏗️ Architecture

```text
Internet
   │
   ▼
Application Load Balancer
   │
   ▼
Private EC2 Instance 1
Private EC2 Instance 2
```

---

# ✅ What Was Done

- Created separate Ansible roles for modular automation
- Created Security Groups:
  - `alb-sg`
  - `ec2-sg`
- Provisioned 2 private EC2 instances
- Created Application Load Balancer
- Created Target Group and Health Checks
- Registered EC2 instances into Target Group
- Installed and configured Nginx
- Verified ALB routing successfully

---

# 📁 Important Files

| File | Purpose |
|---|---|
| `playbook.yml` | Main orchestration playbook |
| `vars.yml` | Stores reusable variables |
| `inventory.ini` | Inventory configuration |
| `ansible.cfg` | Ansible configuration |
| `roles/` | Contains all modular roles |

---

# 📸 Outputs Verified

- EC2 instances created successfully
- ALB created successfully
- Nginx installed in private instances
- ALB DNS displaying Nginx page
- Health checks showing healthy targets

---

# 🐳 Task 02 — Dockerized Application with Nginx Reverse Proxy

## 📌 Task Description

Instead of showing the default Nginx page:

- Install Docker using Ansible
- Run a sample containerized application
- Configure Nginx as reverse proxy to the container

---

# 🏗️ Architecture

```text
Internet
   ▼
Nginx Reverse Proxy
   ▼
Docker Container (nginxdemos/hello)
```

---

# ✅ What Was Done

- Modified existing Ansible roles
- Installed Docker in backend instances
- Pulled and ran `nginxdemos/hello` container
- Configured Nginx reverse proxy
- Verified containerized application through ALB DNS

---

# 📸 Outputs Verified

- Docker installed successfully
- Container running successfully
- Nginx reverse proxy configured
- Application accessible through ALB DNS

---

# 🔐 Security Measures

- SSH restricted only to personal IP
- Backend EC2 instances deployed in private subnet
- ALB deployed in public subnet
- Infrastructure isolated inside VPC

---

# 📚 Learning Outcomes

- Infrastructure Automation using Ansible
- AWS EC2 & ALB provisioning
- Security Group configuration
- Nginx installation and reverse proxy setup
- Docker container deployment
- Role-based Ansible project structure

---

# 🎯 Result

Successfully automated AWS infrastructure provisioning, Nginx configuration, Docker deployment, and ALB integration using Ansible.

---
