# Flask Backend

## Project Overview
This project is a Flask backend deployed on an Amazon EC2 instance.

## Part 1 – Deployment
- Deployed Flask on EC2
- Flask runs on port 5000
- Used Python virtual environment
- Used PM2 to keep the application running

## Part 2 – CI/CD
- Created Jenkins job: `flask-app`
- Jenkins pulls code from this GitHub repository
- Installs Python dependencies
- Restarts the Flask application using PM2
- Configured GitHub webhook to trigger Jenkins after a push

## Technologies
- Python
- Flask
- Git/GitHub
- Jenkins
- PM2
- AWS EC2
