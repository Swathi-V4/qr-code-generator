# QR Code Generator

## Overview

This project is a Python-based QR Code Generator that creates QR codes from a user-provided URL. The application uses environment variables for configuration, generates QR code images, and stores them in a designated output folder. The project has been containerized using Docker for portability and ease of deployment.

---

## Features

- Generate QR codes from URLs
- Save generated QR code images automatically
- Uses environment variables for configuration
- Dockerized application for consistent deployment
- GitHub Actions workflow for automated Docker image builds

---

## Technologies Used

- Python 3.12
- Docker
- Git
- GitHub
- GitHub Actions
- qrcode
- Pillow
- python-dotenv

---

## Project Structure

```
qr-code-generator/
│
├── .github/
│   └── workflows/
│       └── docker.yml
├── qr_codes/
├── Dockerfile
├── docker-compose.yml
├── main.py
├── requirements.txt
├── .dockerignore
├── .gitignore
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Swathi-V4/qr-code-generator.git
cd qr-code-generator
```

Create a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Run the application locally:

```bash
python main.py
```

The generated QR code will be saved in the **qr_codes** folder.

---

## Running with Docker

Build the Docker image:

```bash
docker build -t qr-code-generator-app .
```

Run the Docker container:

```bash
docker run -d --name qr-generator qr-code-generator-app
```

View the container logs:

```bash
docker logs qr-generator
```

Stop and remove the container:

```bash
docker stop qr-generator
docker rm qr-generator
```

---

## DockerHub

Docker image:

https://hub.docker.com/r/swathi638/qr-code-generator-app

---

## GitHub Repository

https://github.com/Swathi-V4/qr-code-generator

---

## Continuous Integration

This project uses GitHub Actions to automatically build the Docker image whenever changes are pushed to the **main** branch.

---

## Author

**Swathi Veerapalli**