# AWS Auto Scaling + Application Load Balancer (High Availability Project)

## 🚀 Project Overview

This project demonstrates how to build a **scalable, highly available web architecture** on AWS using:

- EC2 (Compute)
- Application Load Balancer (ALB)
- Target Groups (Health Checks)
- Auto Scaling Groups (ASG)
- Launch Templates

The goal was to simulate a real-world production setup where traffic is distributed across multiple servers and infrastructure can scale automatically.

---

## 🧠 Architecture Summary

Client Request → ALB → Target Group → EC2 Instances (ASG)

- **ALB** distributes incoming traffic
- **Target Group** monitors instance health
- **Auto Scaling Group** maintains desired capacity
- **Launch Template** defines instance configuration

---

## 🛠️ Technologies Used

- AWS EC2
- AWS Application Load Balancer
- AWS Auto Scaling
- Node.js
- Linux (Ubuntu)

---

## ⚙️ Application

A simple Node.js web server was deployed to each EC2 instance:
