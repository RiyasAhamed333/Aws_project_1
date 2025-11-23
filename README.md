🚀 AWS Three-Tier Web Architecture – Production-Ready Deployment

📌 Project Overview

This project demonstrates a highly available, scalable, and secure three-tier web architecture on AWS, following real-world cloud engineering and DevOps best practices.
The system is designed to mimic production-grade enterprise applications commonly used in modern web platforms.

The architecture includes:

Web Tier (Presentation Layer) – Public-facing Nginx servers behind an Application Load Balancer

Application Tier (Logic Layer) – Node.js backend behind a private/internal Load Balancer

Database Tier (Data Layer) – Amazon Aurora MySQL Multi-AZ cluster

This project showcases your practical ability to design, deploy, and configure end-to-end cloud infrastructure on AWS.

🏗️ Architecture Diagram

![AWS 3-Tier Architecture](images/3TierArch.png)


🔹 Component Overview

| Layer                | AWS Services Used                         | Purpose                                          |
| -------------------- | ----------------------------------------- | ------------------------------------------------ |
| **Web Tier**         | ALB (public), EC2 (Nginx), Auto Scaling   | Serves frontend, handles client traffic          |
| **Application Tier** | Internal ALB, EC2 (Node.js), Auto Scaling | Processes API requests, business logic           |
| **Database Tier**    | Amazon Aurora MySQL Multi-AZ              | Stores and retrieves data with high availability |
| **Networking**       | VPC, Subnets, Route Tables, NAT, IGW, SGs | Secure, isolated, production-ready network       |

🔥 Key Features
✔ Production-Grade Networking

Custom VPC with public, private, and DB subnets

Internet Gateway & NAT Gateway

Routing for secure traffic flow

✔ Scalable EC2 Architecture

Auto Scaling Groups for web and app tiers

Health checks at both load balancers

Automated instance replacement

✔ Secure Multi-Tier Design

Web → App → DB communication only

Security Groups and NACLs configured with least privilege

No direct internet exposure for the app and DB layers

✔ High Availability & Fault Tolerance

ALB + Internal ALB for distribution

Multi-AZ Aurora MySQL deployment

Redundant infrastructure across AZs

🧩 How the Architecture Works

Clients connect to a public Application Load Balancer.

The ALB forwards traffic to Web Tier EC2 instances running Nginx + React.js.

Web tier routes backend requests to internal Load Balancer.

Internal ALB forwards traffic to Application Tier EC2 instances running Node.js.

Application tier interacts with Aurora MySQL Multi-AZ for data operations.

Responses propagate back through the tiers to the client.

This layered approach improves security, scalability, fault tolerance, and manageability.

🏁 Skills Demonstrated

AWS VPC Design (Subnets, IGW, NAT, Route Tables)

EC2, Auto Scaling, and Load Balancers

Aurora MySQL Multi-AZ Deployment

Secure multi-tier architecture

Nginx + React.js (frontend deployment)

Node.js (backend API logic)

Cloud Networking & Infrastructure as Architecture

High Availability & Scalability Best Practices

📦 Project Structure
aws-three-tier-app/
│── web-tier/
│── app-tier/
│── db-tier/
│── architecture-diagram.png
└── README.md

🔐 Security

Principle of least privilege applied

Security groups restrict communication between tiers

Database is only accessible from application tier

No public exposure of backend or database

📄 License

MIT-0 License – free to use for learning and professional purposes.
