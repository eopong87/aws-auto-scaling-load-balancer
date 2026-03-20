# AWS Auto Scaling Web Architecture

## Overview
This project demonstrates a highly available and scalable web architecture using AWS services including EC2, Application Load Balancer (ALB), Target Groups, and Auto Scaling.

The system automatically distributes traffic and replaces unhealthy instances while maintaining availability.

---

## Architecture
- Application Load Balancer routes traffic
- Target Group monitors instance health
- Auto Scaling Group maintains desired capacity
- EC2 instances run Nginx web server

---

## Features
- Load balancing across multiple instances
- Health checks and automatic replacement
- Auto Scaling group with dynamic capacity
- High availability across multiple Availability Zones

---

## Screenshots

### Load Balancer
ALB

### Target Group (Healthy)
Target Group

### Auto Scaling Group
ASG

### Live Application
App

---

## Verification

The Application Load Balancer DNS successfully served traffic to Auto Scaling instances.

Result:
Auto Scaling Server

This confirms:
- Load balancer is routing traffic
- Instances are healthy
- Auto Scaling is functioning correctly

---

## Lessons Learned
- Infrastructure must be automated using launch templates
- Manual configuration does not scale
- Health checks are critical for system reliability
- Auto Scaling ensures system resilience under failure

---

## Future Improvements
- Add HTTPS using ACM
- Deploy a real web application (Node.js)
- Add monitoring with CloudWatch dashboards
- Implement CI/CD pipeline

---
