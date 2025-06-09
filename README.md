# ICT171 Cloud Server Project – 2025

**Student Name:**   TABITHA MUKUYU
**Student Number:** 35402328 
**Unit Code:** ICT171 

---

## 🌐 Live Site & Video

- **Website (HTTPS):** https://tabbyyy.click  
- **GitHub Repo:**   https://github.com/Mukuyu1/PetView-Showcase
- **Video Explainer:https://youtu.be/tEiSOzdtB78

- 

---

## 📄 Project Overview

This project involved designing and deploying a secure cloud server hosted on AWS EC2 using Ubuntu 24.04. The server hosts a basic HTML/CSS website, secured with HTTPS using Certbot, and is accessible through a registered domain `tabbyyy.click`.

The server was manually configured using IaaS principles, and setup steps were documented and automated using a Bash script. The goal is to demonstrate real-world skills in cloud deployment, Linux administration, scripting, and technical documentation.

---

## 🔧 Technologies Used

- AWS EC2 (Ubuntu 24.04)
- Apache2 Web Server
- Bash scripting
- Git & GitHub
- Let's Encrypt (Certbot)
- Route 53 (DNS)
- HTML/CSS

---

## 🚀 Setup Instructions

### 1. Launch Ubuntu EC2 Instance (AWS)
- Use `t2.micro` under Free Tier
- Open ports: **22 (SSH)**, **80 (HTTP)**, and **443 (HTTPS)**

### 2. SSH into the Instance
```bash
ssh -i pet.pem ubuntu@54.173.233.107

3. Run Setup Script
chmod +x setup.sh
./setup.sh

4. Deploy HTML/CSS Files
sudo cp index.html /var/www/html/
sudo cp style.css /var/www/html/

5. Point Domain to EC2 IP (Route 53)

    Create A records for @ and www pointing to 54.173.233.107

6. Enable SSL with Certbot

sudo apt install certbot python3-certbot-apache -y
sudo certbot --apache -d tabbyyy.click -d www.tabbyyy.click

Bash Script: setup.sh
#!/bin/bash
sudo apt update -y
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
Purpose: Automates installation and configuration of the Apache web server on a fresh Ubuntu instance.

🧠 Learning Outcomes Demonstrated

    Linux CLI usage for server administration

    Hosting and configuring an IaaS-based server

    Bash scripting for automation

    Git and GitHub for version control and documentation

    SSL configuration with Certbot

    DNS linking via Route 53

    Writing reusable technical documentation

https://github.com/Mukuyu1/PetView-Showcase/blob/main/ICT171%20Assignment%202%20documentation.pdf






