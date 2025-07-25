# Host-Website-on-EC2-using-Apache

# AWS EC2 Website Hosting with Apache

This project demonstrates how to host a static HTML website on an AWS EC2 instance using Apache HTTP Server.

## 💡 What You'll Learn
- Launching an EC2 instance
- Installing Apache
- Hosting static files (HTML, CSS)

## 🧰 Prerequisites
- AWS account
- SSH key pair (.pem file)
- Basic knowledge of terminal/command line

## 🚀 Steps to Deploy

### 1. Launch an EC2 Instance
- Go to EC2 Console > Launch Instance
- Choose Amazon Linux 2 AMI (free tier)
- Choose t2.micro
- Add a new key pair (download `.pem`)
- Allow inbound HTTP (port 80) in security group

### 2. Connect to EC2 via SSH

bash
ssh -i "your-key.pem" ec2-user@<EC2-PUBLIC-IP>

### 3. Install Apache Server

sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

### 4. Upload Your Website

cd /var/www/html
sudo rm -f index.html
sudo nano index.html  # or upload via SCP

### 5. Visit the Site

Open a browser and go to:
http://<EC2-PUBLIC-IP>

<>
<img width="2880" height="1614" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/8da9b964-c396-4bc1-9785-af0420e3329f" />



