# Architecture

## Overview
This project demonstrates a cloud-based infrastructure architecture built on AWS to host and support a web application securely and efficiently.

The design applies core cloud engineering principles including compute provisioning, storage management, network segmentation, access control, and monitoring.

---

## Architecture Components

### 1. Compute Layer
**Amazon EC2**
- Used to host the web application
- Acts as the main application server
- Processes incoming user requests

---

### 2. Storage Layer
**Amazon S3**
- Used for storing static assets and files
- Supports scalable and durable storage
- Can be used to offload non-dynamic content from the application server

---

### 3. Identity and Access Layer
**AWS IAM**
- Controls access to AWS resources
- Uses users, roles, and policies
- Ensures only authorised actions are permitted

---

### 4. Networking Layer
**Amazon VPC**
- Provides isolated cloud networking environment
- Supports subnet configuration and routing

**Security Groups**
- Control inbound and outbound traffic
- Allow access only on required ports such as SSH and HTTP/HTTPS

---

### 5. Monitoring Layer
**Amazon CloudWatch**
- Used to monitor resource performance
- Tracks logs and system metrics
- Helps identify issues and monitor health

---

## System Flow
1. A user accesses the application through the internet  
2. Requests are routed to the EC2 instance  
3. The application processes requests  
4. Static files or assets can be served from S3  
5. CloudWatch monitors system activity and performance  

---

## Security Considerations
- IAM policies restrict access to AWS resources  
- Security groups allow only required traffic  
- Least-privilege access principles are applied  
- Monitoring helps detect issues and unusual behaviour  

---

## Networking Concepts Applied
- Virtual private cloud design  
- Secure access through controlled ports  
- Traffic flow between public access and compute resources  
- Network segmentation and access control  

---

## Scalability Considerations
- Architecture supports future expansion  
- Can be improved with load balancing and auto-scaling  
- S3 supports scalable storage  
- Monitoring supports performance tuning and growth planning  

---

## Conclusion
This architecture reflects practical AWS cloud engineering concepts and demonstrates how infrastructure can be designed to support secure, scalable, and monitored application deployment.
