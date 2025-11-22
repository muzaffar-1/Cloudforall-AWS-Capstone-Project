# 🌩️ Cloudforall AWS Capstone Project  
### Multi-Tier, Highly Available & Highly Scalable Architecture on AWS

This project demonstrates how to design and deploy a **production-grade multi-tier architecture** on AWS.  
It includes a VPC, public/private subnets, load balancer, Auto Scaling Group, RDS, S3, CloudFront, IAM, SSM and follows real AWS best practices.

---

# 🏗️ Architecture Diagram & Setup Screenshots

## **1️⃣ VPC & Subnets**

### VPC
![VPC](screenshots/screenshot_page1_Image9.png)

### Subnets
![Subnets](screenshots/screenshot_page1_Image10.png)

---

## **2️⃣ Internet Gateway & Route Tables**

### Internet Gateway
![IGW](screenshots/screenshot_page2_Image13.png)

### Public Route Table
![Public RT](screenshots/screenshot_page2_Image14.png)

---

## **3️⃣ NAT Gateway & Private Route Table**

### NAT Gateway  
![NAT](screenshots/screenshot_page3_Image17.png)

### Private Route Table  
![Private RT](screenshots/screenshot_page3_Image18.png)

---

## **4️⃣ Security Groups & EC2 Instances**

### Security Groups  
![Security Groups](screenshots/screenshot_page4_Image21.png)

### EC2 Instances  
![EC2 Instances](screenshots/screenshot_page4_Image22.png)

---

## **5️⃣ Systems Manager (SSM) Access**

### Fleet Manager / SSM  
![SSM](screenshots/screenshot_page5_Image25.png)

### SSM Role  
![SSM Role](screenshots/screenshot_page5_Image26.png)

---

## **6️⃣ Target Group & Launch Template**

### Target Group  
![Target Group](screenshots/screenshot_page6_Image29.png)

### Launch Template  
![Launch Template](screenshots/screenshot_page6_Image30.png)

---

## **7️⃣ Auto Scaling Group (ASG)**

### ASG  
![ASG](screenshots/screenshot_page7_Image33.png)

### ASG Activity  
![ASG Activity](screenshots/screenshot_page7_Image34.png)

---

## **8️⃣ CloudFront CDN**

### CloudFront Distribution  
![CloudFront](screenshots/screenshot_page8_Image37.png)

### CloudFront Settings  
![CloudFront Settings](screenshots/screenshot_page8_Image38.png)

---

# 📌 Project Summary

### ✔️ VPC Design
- CIDR: 10.0.0.0/16  
- **Public Subnets:** For ALB + NAT  
- **Private Subnets:** For EC2 + RDS  
- Public RT → IGW  
- Private RT → NAT  

---

### ✔️ Web Tier
- EC2 Amazon Linux 2023  
- ALB forwards traffic to EC2  
- Auto Scaling based on CPU  
- Launch Template for consistency  
- NGINX configured  

---

### ✔️ Database Tier
- Amazon RDS MySQL  
- Hosted in private subnets  
- Accessible ONLY from WebApp SG  

---

### ✔️ Static Storage + CDN
- S3 bucket for images  
- CloudFront distribution for global low-latency  
- OAC configured to secure bucket  

---

### ✔️ Security
- No SSH access  
- Access through SSM only  
- SG follows least privilege  
- DB not exposed to internet  

---

### ✔️ Monitoring
- CloudWatch CPU alarms  
- Auto Scaling events  
- ALB health checks  

---

# 📝 Author  
**Md Muzaffar Qureshi**  
Capstone Project – Cloud & DevOps  

---

