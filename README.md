# Containerizing a Simple Web App

## Overview
This project demonstrates how to containerize a basic Flask web application using Docker. It includes a `Dockerfile` for building the container and instructions for running it locally.

## Technologies Used
- **Python** (Flask framework)
- **Docker** (Containerization)

## Project Structure
```
📂 Containerizing-a-Simple-Web-App/
├── 📄 app.py            # Flask application
├── 📄 Dockerfile        # Docker configuration
├── 📄 requirements.txt  # Python dependencies
└── 📄 README.md         # Project documentation
```

## Prerequisites
Ensure you have the following installed on your system:
- **Docker**: [Install Docker](https://docs.docker.com/get-docker/)
- **Python 3** (only required for local development, not for running the container)

## Getting Started
### 1️⃣ Clone the Repository
```bash
git clone git@github.com:MustafaMuk/Containerizing-a-Simple-Web-App.git
cd Containerizing-a-Simple-Web-App
```

### 2️⃣ Build the Docker Image
```bash
docker build -t flask-docker-app .
```

### 3️⃣ Run the Container
```bash
docker run -p 5000:5000 flask-docker-app
```

### 4️⃣ Access the Application
Once the container is running, open a web browser and visit:
```
http://localhost:5000
```
You should see the web application running inside the Docker container.

## Modifying the Application
To make changes, modify `app.py`, then rebuild and restart the container:
```bash
docker build -t flask-docker-app .
docker run -p 5000:5000 flask-docker-app
```

## Pushing the Image to Docker Hub (Optional)
If you want to share your image on **Docker Hub**, follow these steps:
```bash
docker login  # Log in to Docker Hub

# Tag the image (replace 'your-username' with your Docker Hub username)
docker tag flask-docker-app your-username/flask-docker-app:v1

# Push the image
docker push your-username/flask-docker-app:v1
```

## Conclusion
This project serves as a starting point for containerizing web applications. By using Docker, we ensure the application runs consistently across different environments.

## Author
**Mustafa Mukhtar**
- GitHub: [MustafaMuk](https://github.com/MustafaMuk)

