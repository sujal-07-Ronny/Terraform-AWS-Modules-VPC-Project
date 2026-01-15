# Terraform AWS VPC Module Project

This project demonstrates how to provision a **custom AWS VPC using Terraform modules** following Infrastructure as Code (IaC) best practices.  
The goal of this project is to build a reusable, clean, and production-ready VPC module instead of writing all resources in a single Terraform file.

---

## 📌 Project Overview

The Terraform module creates a complete VPC networking setup on AWS, including public and private subnets, routing, and outputs that can be reused across environments.

This project helped me understand real-world AWS networking concepts and how Terraform modules improve scalability and maintainability.

---

## 🧱 Architecture Components

The following AWS resources are created using Terraform:

- Custom VPC with CIDR block
- Public and Private Subnets across Availability Zones
- Internet Gateway
- Public Route Table
- Route Table Associations
- Terraform Outputs for VPC and Subnet IDs

---

## 📂 Project Structure

Terraform-AWS-Modules-VPC-Project/
│
├── main.tf
├── variables.tf
├── outputs.tf
├── versions.tf
├── .gitignore
│
└── modules/
└── vpc/
├── main.tf
├── variables.tf
├── outputs.tf
├── versions.tf
└── README.md


---

## ⚙️ Prerequisites

- Terraform >= 1.x
- AWS CLI configured
- AWS account with required permissions
- Git

---

## 🚀 How to Use

### 1️⃣ Initialize Terraform
```bash
terraform init
terraform plan
terraform apply

📤 Outputs

After successful execution, Terraform provides:

VPC ID

Public Subnet IDs with Availability Zones

Private Subnet ID with Availability Zone

These outputs can be reused in other modules like EC2, ALB, or EKS.
