
## **Multi-Layer Docker Application**

A multi-layer Docker application consisting of a **Flask backend** and an **NGINX-based frontend**. The application is containerized and managed using Docker Compose, with a CI/CD pipeline set up using GitHub Actions for automated builds and deployments to Docker Hub.

---

## **Table of Contents**

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Directory Structure](#directory-structure)
4. [Setup Instructions](#setup-instructions)
5. [Usage](#usage)
6. [CI/CD Pipeline](#cicd-pipeline)
7. [Contributing](#contributing)

---

## **Project Overview**

This project demonstrates a multi-layer application architecture using Docker:

- **Backend**: A Python Flask application serving a simple API.
- **Frontend**: NGINX acts as a reverse proxy to route traffic to the backend.
- **Orchestration**: Docker Compose is used to orchestrate the services.

---

## **Technologies Used**

- **Python 3.9** (Flask Framework)
- **NGINX** (Frontend and reverse proxy)
- **Docker & Docker Compose**
- **GitHub Actions** (CI/CD pipeline for Docker image builds and deployment)

---

## **Directory Structure**

```
multi-layer-docker-app/
├── backend/
│   ├── app.py                 # Flask backend application
│   ├── Dockerfile             # Dockerfile for the backend
├── nginx/
│   ├── default.conf           # NGINX configuration file
│   ├── Dockerfile             # Dockerfile for the frontend
├── docker-compose.yml         # Orchestrates services
└── .github/workflows/
    └── pipeline.yml     # GitHub Actions pipeline
```

---

## **Setup Instructions**

### **Prerequisites**
1. Install [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/).
2. Clone this repository:
   ```bash
   git@github.com:amishaprashar/multi-layer-docker-app.git
   cd multi-layer-docker-app
   ```

---

### **Build and Run Locally**

1. Build and start the services:
   ```bash
   docker-compose up --build
   ```

2. Access the application:
   - **Frontend**: [http://localhost](http://localhost)
   - **Backend (API)**: [http://localhost:5000](http://localhost:5000)

3. Stop the services:
   ```bash
   docker-compose down
   ```

---

## **Usage**

The application provides the following functionality:

- **Frontend (NGINX)**: Acts as a reverse proxy to route API requests to the backend.
- **Backend (Flask)**: Returns a simple JSON response:
  ```json
  {
    "message": "Welcome to the Flask Backend!"
  }
  ```

---

## **CI/CD Pipeline**

A GitHub Actions workflow automates the CI/CD process:

1. **Triggers**:
   - On every push to the `main` branch.

2. **Pipeline Steps**:
   - Checkout the code.
   - Build Docker images for the backend and frontend.
   - Push the images to Docker Hub.

3. **Docker Hub Setup**:
   - Add `DOCKER_USERNAME` and `DOCKER_PASSWORD` as secrets in your GitHub repository.

---

## **Contributing**

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes and push:
   ```bash
   git push origin feature-name
   ```
4. Submit a pull request.

---

## **Contact**

For any questions or feedback, feel free to reach out:

- **Name**: Sunidhi Pandey
- **Email**: sunidhipandey9999@gmail.com
- **GitHub**: [https://github.com/Sunidhi1994/docker-app]


