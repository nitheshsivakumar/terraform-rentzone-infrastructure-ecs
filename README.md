# 🚗 RentZone - Containerized Web App Deployment on AWS with Terraform, Docker, Amazon ECR, and ECS

## 📌 Project Overview

RentZone is a **containerized car rental web application** deployed on **AWS** using **Terraform, Docker, Amazon ECR, and ECS with AWS Fargate**. This project automates **infrastructure provisioning, container orchestration, and database restoration** from a previous snapshot for efficiency and scalability.

## 🎯 Problem Solved

- **Automated Infrastructure**: Provisioned cloud resources using **Terraform** instead of manual setup.
- **Scalability & High Availability**: Used **AWS Fargate and Auto Scaling** to handle increasing traffic.
- **State Management & Locking**: Implemented **Amazon S3 for Terraform state storage** and **DynamoDB for state locking**.
- **Efficient Containerization**: Used **Docker** to containerize the application and pushed images to **Amazon ECR**.
- **Database Restoration**: Restored the **Amazon RDS (MySQL) database from a snapshot**, eliminating manual migration efforts.
- **Security & Access Control**: Configured **IAM roles, security groups, and HTTPS using AWS Certificate Manager**.
- **Automated Deployment**: Used **Terraform to define infrastructure as code (IaC)**, making the deployment repeatable and version-controlled.

---

## 🏗️ Architecture Overview

### 🔹 Key AWS Services Used
- **Terraform** - Infrastructure as Code for automated provisioning.
- **Amazon S3** - Storing Terraform state files.
- **Amazon DynamoDB** - Locking Terraform state to prevent concurrent modifications.
- **Amazon ECR** - Storing and managing Docker container images.
- **AWS Fargate** - Running containers without managing EC2 instances.
- **Amazon ECS** - Orchestrating containerized workloads.
- **Amazon RDS (MySQL)** - Restoring database from a snapshot.
- **Application Load Balancer** - Distributing traffic to containers.
- **VPC** - Custom networking with private and public subnets.
- **NAT Gateway** - Enabling internet access for private instances.
- **Bastion Host** - Secure SSH access to internal resources.
- **AWS Certificate Manager** - Encrypting web traffic with HTTPS.
- **Amazon Route 53** - Managing DNS records for domain resolution.
- **IAM** - Managing permissions and access control.

📌 **Reference Architecture:**  
![Architecture](RentZone-Terraform.jpg)

---

## 🚀 What I Did

1️⃣ **Infrastructure as Code (IaC) with Terraform**  
- Used **Terraform** to provision all AWS resources, making deployments repeatable.  
- Stored Terraform **state in Amazon S3** and locked it using **DynamoDB**.  

2️⃣ **Containerized the Web App with Docker & ECR**  
- Built a **Docker image** for the application.  
- Pushed the image to **Amazon ECR** for centralized container management.  

3️⃣ **Deployed the Application on AWS ECS & Fargate**  
- Created an **ECS Cluster** and defined **Task Definitions** for running containers.  
- Used **AWS Fargate** to deploy the application without managing servers.  

4️⃣ **Database Restoration from an RDS Snapshot**  
- Instead of manually setting up a new database, **restored an Amazon RDS (MySQL) instance from a snapshot**.  
- Ensured data consistency while minimizing downtime.  

5️⃣ **Implemented High Availability & Security**  
- Configured an **Application Load Balancer** to distribute traffic across containers.  
- Used **Amazon Route 53** for domain name resolution.  
- Secured traffic using **AWS Certificate Manager** for SSL/TLS encryption.  
- Restricted access with **IAM roles and security groups**.  

6️⃣ **Automated Scaling & Monitoring**  
- Set up **Auto Scaling** to dynamically adjust ECS container instances based on demand.  
- Used **Amazon CloudWatch** and **SNS notifications** for monitoring and alerts.  

---

## 📊 Key Benefits

✅ **Automated Deployment** - Infrastructure and application deployment fully managed via Terraform.  
✅ **Scalability** - Fargate automatically scales based on demand, reducing downtime.  
✅ **Secure & Efficient** - IAM roles, VPC isolation, and HTTPS encryption.  
✅ **Cost-Optimized** - Serverless containers with pay-as-you-go pricing.  
✅ **State Management** - Terraform state stored in **S3**, with **DynamoDB locking**.  
✅ **Reliable Database** - Restored **Amazon RDS (MySQL)** from a snapshot for seamless migration.  

---
