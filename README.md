# ☁️ AWS : Secure and Highly Available Web App Architecture

## 🚀 Overview

This project demonstrates a foundational AWS architecture for a scalable and highly available web application using core AWS services. It includes a load-balanced EC2 web tier and a secure S3-backed static asset layer, adhering to best practices in cloud architecture and IAM security.

---

## 📐 Architecture Diagram



---

## 🧱 Architecture Components

| Component                | Purpose                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| **VPC (Default)**        | Provides isolated networking space for AWS resources                   |
| **2 Public Subnets**     | Host EC2 instances across different Availability Zones (AZs) for HA     |
| **EC2 Instances**        | Host the web application (Apache/Nginx)                                |
| **IAM Role for EC2**     | Grants secure, temporary access to S3 without exposing credentials      |
| **Application Load Balancer** | Distributes user traffic across EC2 instances for scalability & HA |
| **S3 Bucket**            | Stores static assets (CSS, JS, images)                                 |
| **Internet Gateway**     | Provides public internet access to the app                             |

---

## 💡 Why This Architecture?

This design reflects AWS best practices for beginner-level cloud engineers and demonstrates:

- ✅ **High Availability**: Multi-AZ architecture ensures fault tolerance
- ✅ **Security**: Uses IAM Roles (not keys), and public subnetting with scoped access
- ✅ **Separation of Concerns**: Static assets are served from S3, logic from EC2
- ✅ **Scalability**: Load Balancer enables horizontal scaling
- ✅ **Cost Awareness**: Uses Free Tier-friendly services

---

## 🔧 Tech Stack

- AWS EC2
- Amazon S3
- AWS IAM (Roles & Policies)
- Application Load Balancer (ALB)
- Apache or Nginx (on EC2)
- Optional: Route 53, CloudWatch for logging and health checks

---



