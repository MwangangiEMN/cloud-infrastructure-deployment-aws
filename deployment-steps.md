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

## Deployment Commands (Terminal Execution)

These commands were executed sequentially in a Linux-based EC2 environment.
```bash
# Connect to EC2 instance
ssh -i key.pem ubuntu@your-ec2-public-ip

# Update system packages
sudo apt update
sudo apt upgrade -y

# Install Nginx web server
sudo apt install nginx -y

# Start Nginx service
sudo systemctl start nginx

# Enable Nginx to start on boot
sudo systemctl enable nginx

# Check status of Nginx
sudo systemctl status nginx
