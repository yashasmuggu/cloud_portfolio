# Task 2 – Containerization Using Docker & AWS EC2

## 📌 Overview

This task focused on containerizing a web application using Docker and deploying the containerized application on an AWS EC2 virtual machine.

## 🛠️ Technologies Used

- Docker
- Docker Desktop
- Nginx
- AWS EC2
- Ubuntu
- Git
- GitHub
- VS Code

## 🐳 Dockerfile

The Dockerfile uses the Nginx Alpine image:

```dockerfile
FROM nginx:alpine

COPY portfolio/ /usr/share/nginx/html/

EXPOSE 80

💻 Local Docker Deployment

From the repository root, build the Docker image:

docker build -f Task-2/Dockerfile -t portfolio-website .

Run the container:

docker run -d -p 8080:80 --name portfolio-container portfolio-website

The portfolio can then be accessed at:

http://localhost:8080
☁️ AWS EC2 Deployment

The application was deployed on an Ubuntu AWS EC2 instance.

Deployment Workflow
GitHub Repository
       ↓
AWS EC2
       ↓
Docker Image
       ↓
Docker Container
       ↓
Nginx
       ↓
Portfolio Website
Docker Commands Used on EC2
git clone https://github.com/yashasmuggu/cloud_portfolio.git
cd cloud_portfolio

docker build -f Task-2/Dockerfile -t portfolio-website .

docker run -d -p 80:80 --name portfolio-container portfolio-website

Verify the running container:

docker ps

Test the application:

curl http://localhost
🔐 EC2 Security Configuration

HTTP traffic was allowed through:

TCP Port: 80
Source: 0.0.0.0/0

SSH access was configured for EC2 Instance Connect.

📸 Screenshots

Task 2 screenshots are stored in:

../screenshots/Task-2/
📚 Learning Outcomes

Through this task, I gained practical experience with:

Docker image creation
Docker containers
Nginx
Linux commands
AWS EC2
Security Groups
Cloud deployment
Git and GitHub