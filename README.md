# AWS Auto-Scaling Web Application

## Project Overview

This project demonstrates how to build a highly available and scalable web application architecture on AWS using EC2, Application Load Balancer, and Auto Scaling Group.

The infrastructure automatically distributes traffic across multiple servers and dynamically scales instances based on traffic load.

---

# Architecture

Users → Application Load Balancer → Auto Scaling Group → EC2 Instances

---

# AWS Services Used

* Amazon EC2
* Application Load Balancer (ALB)
* Auto Scaling Group (ASG)
* Amazon Machine Image (AMI)
* Launch Templates
* Target Groups
* Amazon VPC

---

# Features

✅ Auto Scaling based on CPU utilization
✅ Load balancing across multiple servers
✅ High availability architecture
✅ Fault tolerance
✅ Health checks for instances
✅ Dynamic scaling (scale in / scale out)
✅ Apache web server deployment

---

# Project Workflow

## 1. EC2 Instance Creation

* Launched Amazon Linux EC2 instance
* Installed Apache Web Server
* Hosted sample web page

## 2. AMI Creation

* Created custom AMI from configured EC2 instance
* Used AMI for future auto-scaled instances

## 3. Launch Template

* Configured launch template using custom AMI
* Defined instance type and security group

## 4. Target Group

* Created target group for EC2 instances
* Configured HTTP health checks

## 5. Application Load Balancer

* Created internet-facing load balancer
* Distributed traffic across EC2 instances

## 6. Auto Scaling Group

* Configured dynamic scaling policy
* Automatically launched and terminated instances

---

# Scaling Policy

| Setting          | Value           |
| ---------------- | --------------- |
| Desired Capacity | 2               |
| Minimum Capacity | 1               |
| Maximum Capacity | 4               |
| Scaling Metric   | CPU Utilization |
| Target CPU       | 50%             |

---

# Security Configuration

| Port | Purpose          |
| ---- | ---------------- |
| 22   | SSH Access       |
| 80   | HTTP Web Traffic |

---

# Testing

## Load Balancer Testing

* Accessed application using Load Balancer DNS
* Verified traffic distribution across instances

## Auto Scaling Testing

* Generated CPU load using stress tool
* Verified automatic instance creation

Command used:

```bash
stress --cpu 2 --timeout 300
```



# Learning Outcomes

Through this project, I learned:

* AWS EC2 deployment
* Load balancing concepts
* Auto Scaling implementation
* Cloud infrastructure architecture
* High availability systems
* Fault tolerance
* AWS networking basics

---

# Future Improvements

* HTTPS using AWS Certificate Manager
* AWS WAF integration
* CloudWatch monitoring dashboards
* CI/CD pipeline integration
* Terraform automation

---

# Author

Rushikesh Pawar

---

# Tags

AWS • EC2 • Auto Scaling • Load Balancer • Cloud Computing • DevOps • Cloud Architecture
