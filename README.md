# 🏨 Hotel Coupon App

[![PyPI version](https://badge.fury.io/py/hotel-coupon-app-package-alexandermamani.svg)](https://pypi.org/project/hotel-coupon-app-package-alexandermamani/)

**Hotel Coupon App** is a cloud-native platform that enables hoteliers to create, manage, and distribute discount coupons in real time, while users can search, redeem, and receive instant notifications.  
The project leverages **serverless** and **event-driven architectures** on AWS, combining **Angular**, **Django REST API**, **AWS Lambdas**, and a **custom Python PDF reporting library**.

---

## 📂 Repositories

- 🌐 [**Angular GUI**](https://github.com/alexandermamaniy/ccp-hotel-coupon-frontend) — User and hotelier web interface.  
- ⚙️ [**Django REST-API**](https://github.com/alexandermamaniy/ccp-hotel-coupon-backend) — Backend and main API service.  
- ☁️ [**AWS Lambdas & Deployment**](https://github.com/alexandermamaniy/ccp-hotel-coupon-deploy) — Serverless functions and deployment scripts.  
- 📑 [**Python PDF Report Library**](https://pypi.org/project/hotel-coupon-app-package-alexandermamani/) — Custom library for generating PDF reports.  

📖 [**Full Project Report (PDF)**](https://github.com/alexandermamaniy/hotel-coupon-app/blob/main/document/hotel_coupon_app_document.pdf)

---

## 🚀 Features

### 👤 Users
- Search coupons by title, discount, or hotel name.  
- Redeem coupons and automatically subscribe to future offers from the same hotelier.  
- View redeemed coupons, use them via unique QRcodes, and receive real-time notifications.  

### 🏨 Hoteliers
- Create, edit, and track coupon usage.  
- Notify subscribed users about new coupons instantly.  
- Generate PDF reports with insights into coupon performance and user interactions.  

---

## ⚡ Architecture

The system combines **AWS Serverless** and **Event-Driven Design**:

- **Amazon S3** → Store images & reports.  
- **Amazon RDS (PostgreSQL)** → Business data storage.  
- **Amazon DynamoDB** → Manage WebSocket connections.  
- **Amazon SNS** → Real-time publish/subscribe notifications.  
- **Amazon SQS** → Batch processing of user interactions.  
- **AWS Lambda** → Serverless execution of tasks.  
- **Amazon API Gateway (WebSockets)** → Real-time communication.  

📌 Simplified flow:  
**Users/Hoteliers ↔ Angular SPA ↔ Django REST API ↔ AWS Lambdas ↔ (RDS / DynamoDB / SQS / SNS / S3)**

---

## 🛠️ CI/CD

The project uses **GitHub Actions + Docker + AWS**:

1. **CI (Continuous Integration)**  
   - Build containers for each repo.  
   - Run automated tests.  
   - Push images to Docker Registry.  

2. **CD (Continuous Delivery & Deployment)**  
   - `staging/***` branches for feature releases.  
   - `main` branch for production deployments.  
   - Deployment on **AWS EC2** with **Docker Compose**.  

---
