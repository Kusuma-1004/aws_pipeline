# aws_pipeline
A Simple Jenkins CI/CD pipeline hosted on EC2 Instance
# Jenkins CI/CD Python + Docker Project

A simple Flask app deployed using a Jenkins CI/CD pipeline on AWS EC2.

## Features
- Python Flask App
- Dockerized build
- Jenkinsfile CI/CD pipeline
- Hosted on AWS EC2

## How to Run (Locally)
```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```

## URL
App runs at: http://<EC2_PUBLIC_IP>:5000
