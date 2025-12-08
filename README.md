🚀 DevOps CI/CD Automation for Containerized Web Application
A fully automated CI/CD DevOps project that builds, tests, and deploys a containerized FastAPI application using GitHub Actions + Docker + Docker Hub.
📌 Project Overview

This project demonstrates a real-world DevOps pipeline:

Stage	Tool	Purpose
CI (Continuous Integration)	GitHub Actions	Automatically test & build application
Containerization	Docker	Run app in isolated container
CD (Continuous Deployment)	Docker Hub	Store and deploy Docker images
Application	FastAPI	Lightweight backend API

Whenever new code is pushed to the main branch:

CI runs automated tests (pytest)

Docker image is built

image is pushed automatically to Docker Hub

🌐 Application Endpoints
Endpoint	Method	Description
/	GET	Returns a message confirming CI/CD success
/docs	GET	Swagger UI for testing the API

Example response:

{
  "message": "CI/CD pipeline is working!"
}

🧱 Project Structure
devops-ci-cd-app
 ├ main.py
 ├ test_main.py
 ├ requirements.txt
 ├ Dockerfile
 └ .github/workflows/ci-cd.yml

🐳 Docker
Build Image
docker build -t devops-ci-cd-app:local .

Run Container
docker run -p 8000:8000 devops-ci-cd-app:local

Access Application
http://localhost:8000/
http://localhost:8000/docs

⚙️ CI/CD Workflow

The GitHub Actions pipeline automatically:

✔ Installs dependencies
✔ Runs tests using pytest
✔ Builds Docker image
✔ Logs in to Docker Hub
✔ Pushes image to Docker Hub

Docker Hub Repository
docker pull abhaychaudhary7/devops-ci-cd-app:latest

🎯 Technologies Used
Category	Tool
Backend	FastAPI
Testing	PyTest
Containerization	Docker
CI/CD	GitHub Actions
Registry	Docker Hub
IDE	VS Code
🚀 How to Run This Project
Without Docker
uvicorn main:app --reload

With Docker (recommended)
docker run -p 8000:8000 abhaychaudhary7/devops-ci-cd-app:latest

🔥 What This Project Demonstrates

Continuous Integration (automated testing & build)

Continuous Deployment using container registry

Containerized microservice deployment

End-to-end DevOps workflow used by modern companies

🧑‍💻 Author

Abhay Chaudhary
B.Tech CSE — Lovely Professional University (2024–2025)
Project: DevOps CI/CD Automation for Containerized Web Application
