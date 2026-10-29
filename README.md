# Dockerized Web Application on AWS EC2

## Project Overview
This project demonstrates containerization and deployment of a web application using Docker on AWS EC2.

## Technologies
- AWS EC2
- Ubuntu Linux
- Docker
- Nginx
- Git and GitHub

## Infrastructure
- EC2 Instance: t3.micro
- RAM: 1 GiB
- Storage: 8 GiB
- Application Port: 8081

## Build the Docker Image
```bash
sudo docker build -t task-app:1.0 .
sudo docker run -d --name task-app-container --restart unless-stopped -p 8081:8081 task-app:1.0

## Access the Application
Open:
http://YOUR-EC2-PUBLIC-IP:8081

## Project Files
- Dockerfile: Docker image configuration
- index.html: Web application
- nginx.conf: Nginx server configuration

## Deployment
The application is deployed on AWS EC2 using Docker. TCP port 8081 is allowed through the EC2 security group for public access.
