# Deployment Steps

## Overview
This document outlines the steps used to deploy a simple application environment on AWS and demonstrates the setup of compute, storage, security, and monitoring services.

---

## Step 1: Launch an EC2 Instance
- Logged into AWS Management Console  
- Navigated to EC2 dashboard  
- Created a new EC2 instance  
- Selected Ubuntu as the operating system  
- Created or selected an SSH key pair  
- Allowed inbound traffic for:
  - SSH (Port 22)
  - HTTP (Port 80)

---

## Step 2: Connect to the EC2 Instance

Used SSH to connect to the instance securely from a terminal.

Example command:
```bash
ssh -i key.pem ubuntu@your-ec2-public-ip

```markdown
## Step 3: Update the Server

Updated package lists and system packages.

```bash
sudo apt update
sudo apt upgrade -y

---


```markdown
## Step 4: Install Web Server

Installed Nginx to host the web application.

```bash
sudo apt install nginx -y

---

```markdown
## Step 5: Start Web Server

Started and enabled Nginx service.

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
