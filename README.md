# My AWS Web App



## 🚀 Project Overview
This project demonstrates a simple web application deployed on AWS using EC2 and Apache Web Server.
It was created to practice real hands‑on cloud and Linux server skills.

## 🛠 Stack
- AWS EC2 (Amazon Linux)
- Apache HTTP Server
- Linux commands (via PuTTY SSH)
- Git & GitHub

## 📌 Steps

### 1. Network Setup
- Created a custom VPC and public subnet
- Attached Internet Gateway
- Configured Security Group to allow:
  - SSH (port 22 from my IP)
  - HTTP (port 80 from anywhere)

### 2. Launch EC2 Instance
- Amazon Linux 2 (t2.micro – Free Tier)
- Enabled Public IPv4 for web access
- Attached Security Group
- Created Key Pair (`MyWebAppKey`) for SSH

### 3. Connect via PuTTY

```bash

ssh -i MyWebAppKey.pem ec2-user@<Public-IP>

4. Update Server

sudo yum update -y

5. Install Apache

sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

6. Create Web Page
echo "<h1>My AWS Web App</h1>" | sudo tee /var/www/html/index.html

7. Test in Browser

Open in browser:

http://<Public-IP>


📁 Git & Deployment

Repo on GitHub:

git add .
git commit -m "Add README with steps"
git push
