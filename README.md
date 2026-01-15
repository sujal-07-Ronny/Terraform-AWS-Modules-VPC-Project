# Terraform AWS VPC Module Project

This project demonstrates how to provision a custom AWS VPC using Terraform modules by following Infrastructure as Code (IaC) best practices. Instead of defining all resources in a single Terraform file, the project focuses on building a reusable and maintainable VPC module suitable for real-world DevOps use cases.

The project helped me gain practical understanding of AWS networking concepts and how Terraform modules improve scalability, consistency, and code reuse.

## Project Overview

The Terraform configuration creates a complete AWS VPC networking setup including public and private subnets, routing, and clean outputs that can be reused by other infrastructure components.

## Architecture Components

Custom VPC with CIDR block  
Public and private subnets across Availability Zones  
Internet Gateway  
Public route table  
Route table associations  
Terraform outputs for VPC and subnet IDs  

## Project Structure

Terraform-AWS-Modules-VPC-Project  
│  
├── main.tf  
├── variables.tf  
├── outputs.tf  
├── versions.tf  
├── .gitignore  
│  
└── modules  
    └── vpc  
        ├── main.tf  
        ├── variables.tf  
        ├── outputs.tf  
        ├── versions.tf  
        └── README.md  

## Prerequisites

Terraform version 1.x or above  
AWS CLI configured with valid credentials  
AWS account with required permissions  
Git installed  

## How to Use

Initialize Terraform  
terraform init  

Review execution plan  
terraform plan  

Apply infrastructure changes  
terraform apply  

## Outputs

After successful execution, Terraform provides the VPC ID, public subnet IDs along with availability zones, and the private subnet ID with its availability zone. These outputs can be consumed by other modules such as EC2, Load Balancer, or EKS.

## Security Best Practices

Terraform state files are excluded using .gitignore  
No AWS credentials are hardcoded  
Modular and reusable infrastructure design  

## Learning Outcomes

Hands-on experience with Terraform modules  
Strong understanding of AWS VPC networking  
Practical exposure to Infrastructure as Code  
Real-world DevOps project structuring  

## Future Enhancements

NAT Gateway for private subnets  
Multi-AZ support  
Environment-based configurations such as dev, stage, and prod  
Module versioning  

## Author

Sujal Shaha  
