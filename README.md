# CI/CD Pipeline with Jenkins, Docker, and Node.js

## 📌 Project Overview

This project demonstrates a CI/CD pipeline using Jenkins to automate the build, test, and deployment of a simple Node.js application using Docker. The pipeline is triggered from GitHub and automatically builds and runs the application inside a Docker container.

## 🛠️ Tech Stack

- Node.js  
- Jenkins  
- Docker  
- Git & GitHub  

## 📁 Project Structure

.  
├── Jenkinsfile  
├── Dockerfile  
├── server.js  
├── package.json  
├── package-lock.json  
└── README.md  

## ⚙️ How the CI/CD Pipeline Works

1. Code is pushed to GitHub  
2. Jenkins detects changes using Pipeline from SCM  
3. Jenkins pulls the latest code from the repository  
4. Dependencies are installed using npm install  
5. Docker image is built from the Dockerfile  
6. A Docker container is created and the application is run  

## 🚀 Setup Instructions

### 1. Clone the Repository

git clone https://github.com/Abbas-Hussein/my-ci-cd-app.git  
cd my-ci-cd-app  

### 2. Install Dependencies

npm install  

### 3. Build Docker Image

docker build -t my-ci-cd-app .  

### 4. Run Docker Container

docker run -d -p 8081:8080 --name my-container my-ci-cd-app  

## 🔧 Jenkins Setup

- Use Pipeline from SCM  
- Repository URL: https://github.com/Abbas-Hussein/my-ci-cd-app.git  
- Branch: main  
- Script Path: Jenkinsfile  

## 🌐 Access the Application

Open your browser and visit:  
http://localhost:8081  

## ⚠️ Important Notes

- Ensure port 8081 is free before running the container  
- Jenkins runs on port 8080, so the app uses 8081 to avoid conflicts  
- Docker must be installed and running  
- Jenkins must have permission to run Docker commands  

## 📈 Future Improvements

- Add automated testing  
- Deploy to cloud platforms (AWS, Azure, etc.)  
- Implement monitoring and logging  
- Use multi-stage Docker builds  

## 👨‍💻 Author

Abbas Hussein  

## 📜 License

This project is for educational purposes.