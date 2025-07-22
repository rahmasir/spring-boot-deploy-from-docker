# Spring Boot Docker Demo 🚀

This project is a simple demonstration of how to containerize a **Spring Boot** application using **Docker**. It includes a minimal Spring Boot application with a single REST endpoint and a multi-stage `Dockerfile` for building an optimized and lightweight Docker image.

## Prerequisites

Before you begin, ensure you have the following software installed on your machine:

-   **Docker**: Docker Desktop or Docker Engine installed and running.
    

## How to Run the Application

Follow these steps to build the Docker image and run the application in a container.

### 1. Build the Docker Image

Navigate to the root directory of the project in your terminal and run the following command. This will build the application using Maven and create a Docker image named `docker-demo`.

```bash
docker build -t docker-demo .

```

### 2. Run the Docker Container

Once the image is successfully built, run it as a container with this command. This command also maps port 8080 on your local machine to port 8080 in the container.

```bash
docker run -p 8080:8080 docker-demo
```

The application will now start inside the Docker container.

> **Tip**: To run the container in the background (detached mode), add the `-d` flag: `docker run -d -p 8080:8080 docker-demo`

----------

## Accessing the Application

To verify that the application is running correctly, open your web browser and go to:

`http://localhost:8080`

Alternatively, you can use a command-line tool like `curl`:

```bash
curl http://localhost:8080
```

You should see the following response: `Hello from Spring Boot in Docker! 👋`