# Automate Dynamic Web App Deployment with Terraform Modules, Docker, Amazon ECR, and ECS

**Terraform Modules referenced**: https://github.com/nitheshsivakumar/terraform-modules

## 📌 Project Overview

This project involves deploying the **RentZone car rental application** on **AWS** using **Terraform Modules, Docker, Amazon ECR, and ECS with AWS Fargate**. The goal was to modularize the Terraform codebase for better reusability, maintainability, and automation.

## 🎯 Problem Solved

- **Infrastructure Reusability**: Used **Terraform modules** to create reusable components for networking, compute, security, and storage.
- **Automated Container Deployment**: Deployed **Dockerized application** on **Amazon ECS with Fargate**.
- **State Management & Locking**: Managed Terraform state in **Amazon S3** and **DynamoDB** to prevent conflicts.
- **Database Automation**: Created and managed **Amazon RDS (MySQL)** via Terraform modules.
- **Scalability & High Availability**: Ensured **load balancing and auto-scaling** with ECS and ALB.
- **Security & Best Practices**: Implemented **IAM roles, security groups, and HTTPS encryption**.

---

## 🏗️ Architecture Overview

### 🔹 Key AWS Services Used
- **Terraform Modules** - Modularized infrastructure as code (IaC) for reusable deployments.
- **Amazon S3** - Storing Terraform state files.
- **Amazon DynamoDB** - Locking Terraform state to prevent concurrent modifications.
- **Amazon ECR** - Storing and managing Docker container images.
- **AWS Fargate** - Running containers without managing EC2 instances.
- **Amazon ECS** - Orchestrating containerized workloads.
- **Amazon RDS (MySQL)** - Managed relational database for storing rental records.
- **Application Load Balancer (ALB)** - Distributing traffic to ECS tasks.
- **Amazon Route 53** - Managing domain and DNS resolution.
- **AWS Certificate Manager (ACM)** - Enabling HTTPS encryption.
- **IAM Roles & Policies** - Managing permissions for security.

---

## 🚀 What I Did

1️⃣ **Modularized Infrastructure Deployment using Terraform Modules**  
- Created reusable **Terraform modules** for:
  - **VPC & Networking**
  - **ECS & Fargate Deployment**
  - **Amazon RDS (MySQL)**
  - **IAM & Security Groups**
  - **Load Balancer & Auto Scaling**
  - **Amazon Route 53 for DNS**  

2️⃣ **Containerized the Application with Docker & Pushed to ECR**  
- Built a **Docker image** for the application.  
- Pushed the image to **Amazon ECR** for centralized management.  

3️⃣ **Provisioned Scalable Infrastructure on AWS**  
- Used **Terraform to deploy ECS with AWS Fargate**, making it **serverless and scalable**.  
- Configured **Application Load Balancer (ALB)** to distribute traffic to containers.  
- Deployed **Auto Scaling Groups** for dynamic scaling.  

4️⃣ **Integrated Terraform State Management with S3 & DynamoDB**  
- Stored Terraform state in **Amazon S3** for tracking infrastructure changes.  
- Enabled **DynamoDB state locking** to prevent concurrent deployments.  

5️⃣ **Automated Database Deployment & Configuration**  
- Created an **Amazon RDS (MySQL) instance** via Terraform.  
- Applied **database snapshots** for restoration and high availability.  

6️⃣ **Implemented Security & Compliance**  
- Restricted access using **IAM roles, security groups, and ACLs**.  
- Secured HTTPS connections via **AWS Certificate Manager (ACM)**.  
- Configured **Amazon CloudWatch** for monitoring ECS tasks and system performance.  

---

## 📊 Key Benefits

✅ **Fully Modularized Infrastructure** - Reusable Terraform modules for efficient deployments.  
✅ **Automated Deployment & Scaling** - ECS, ALB, and Auto Scaling ensure high availability.  
✅ **Secure & Compliant** - IAM roles, private networking, and SSL encryption.  
✅ **Optimized Performance** - Containers run on AWS Fargate with no server management.  
✅ **Version-Controlled & Repeatable** - Terraform state management ensures predictable deployments.  

---
