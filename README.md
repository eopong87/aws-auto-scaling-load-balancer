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

## Load Balancing Verification

The Application Load Balancer successfully distributed traffic across multiple EC2 instances.

By refreshing the ALB DNS endpoint, the response alternated between different instance hostnames:

Hello from ip-172-31-2-107  
Hello from ip-172-31-28-46 

This confirms that traffic is being routed dynamically across healthy targets.

---

## Issues Encountered & Fixes

### Unhealthy Instance

Issue:  
One EC2 instance was marked as unhealthy in the target group.

Cause:  
The application was not running properly on the instance.

Fix:  
Connected to the instance and manually started the application.

---

### Port 80 Permission Error

Error:  
EACCES: permission denied 0.0.0.0:80  

Cause:  
Linux restricts ports below 1024 to root users.

Fix:  
Ran the application with elevated privileges:

sudo node app.js

---

## Key Learnings

- Application Load Balancers distribute traffic across multiple targets  
- Target Groups perform health checks to determine instance availability  
- Auto Scaling Groups maintain desired capacity automatically  
- Launch Templates define how instances are created  
- Applications must start automatically for true fault tolerance  
- Linux requires elevated privileges for ports below 1024  

---

## Future Improvements

- Automate application startup using User Data scripts  
- Run application on port 3000 with reverse proxy  
- Implement CI/CD pipeline for deployments  
- Add CloudWatch alarms for scaling events  
- Improve fault tolerance with full automation  
