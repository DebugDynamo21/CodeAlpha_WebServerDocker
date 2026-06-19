# CodeAlpha Web Server Using Docker

## Project Overview

This project demonstrates the deployment of a simple static web server using Docker and Nginx. The objective is to understand Docker containerization, image creation, container management, and web server deployment inside a Docker container.

This project was completed as part of the **CodeAlpha DevOps Internship Program**.

---

## Objectives

* Learn the fundamentals of Docker containerization.
* Create and build a custom Docker image.
* Deploy a web server using Nginx inside a Docker container.
* Understand Docker image and container lifecycle.
* Monitor container performance and health.
* Explore container-based application deployment.

---

## Technologies Used

* Docker
* Nginx
* HTML

---

## Project Structure

```text
CodeAlpha_WebServerDocker/
│
├── Dockerfile
├── index.html
└── README.md
```

---

## Application Files

### index.html

A simple web page that is served by the Nginx web server running inside the Docker container.

### Dockerfile

The Dockerfile is used to create a custom Docker image based on the official Nginx image and copy the web page into the Nginx web root directory.

---

## Dockerfile

```dockerfile
FROM nginx:latest

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80
```

---

## Build Docker Image

Run the following command inside the project directory:

```bash
docker build -t codealpha-webserver .
```

---

## Run Docker Container

```bash
docker run -d -p 8080:80 codealpha-webserver
```

---

## Verify Deployment

Open the following URL in your browser:

```text
http://localhost:8080
```

If the deployment is successful, the custom web page will be displayed.

---

## Docker Commands Used

### Check Running Containers

```bash
docker ps
```

### View Container Statistics

```bash
docker stats
```

### Stop Container

```bash
docker stop <container_id>
```

### Remove Container

```bash
docker rm <container_id>
```

### Remove Image

```bash
docker rmi codealpha-webserver
```

---

## Screenshots

Add screenshots of:

1. Docker image build process
2. Running Docker container (`docker ps`)
3. Browser output (`http://localhost:8080`)
4. Container monitoring (`docker stats`)

Example:

```text
Screenshots/
├── build-image.png
├── docker-ps.png
├── browser-output.png
└── docker-stats.png
```

---

## Learning Outcomes

Through this project, I learned:

* Docker image creation and management
* Container deployment and execution
* Nginx web server configuration
* Port mapping between host and container
* Container monitoring and troubleshooting
* Best practices for containerized application deployment

---

## Internship Information

**Internship Program:** CodeAlpha DevOps Internship

**Task:** Web Server Using Docker

**Submitted By:** Hardik Bhardwaj

---

## Author

**Hardik Bhardwaj**

GitHub: https://github.com/DebugDynamo21
