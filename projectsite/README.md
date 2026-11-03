# Dockerized Django Application Setup

This repository provides full containerization setup for Django projects using Docker and Docker Compose.

## 🚀 Quickstart Guide

### 1. Build and Run Locally
To build the Docker image from scratch and start the application locally:
```bash
docker-compose up --build -d
```
Access the running server at `http://localhost:8000`.

### 2. Push Image to Docker Hub
1. Authenticate with Docker Hub:
   ```bash
   docker login
   ```
2. Tag your image:
   ```bash
   docker tag my-django-app:latest yourusername/django-app:latest
   ```
3. Push to Docker Hub:
   ```bash
   docker push yourusername/django-app:latest
   ```

### 3. Client / Remote Setup Instructions
To run using the pre-built image from Docker Hub on a target machine:
1. Navigate to the `for_client/` folder.
2. Run:
   ```bash
   docker-compose up -d
   ```
3. Create an admin superuser (first-time setup only):
   ```bash
   docker-compose exec web python manage.py createsuperuser
   ```
