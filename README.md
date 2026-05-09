# Lab Manual 1: Introduction to Docker Containerization

## 🎯 Objective
At the end of this laboratory exercise, I was able to:
*   Understand the basics of Docker containerization.
*   Create a functional Dockerfile.
*   Build a custom Docker image.
*   Run and verify a Docker container locally.

## 🛠️ Tech Stack
*   **Language:** Python 3.10
*   **Tool:** Docker Desktop
*   **Environment:** Windows (CMD / Terminal)

---

## 🚀 Step-by-Step Implementation

### 1. Verification
I started by verifying that Docker was correctly installed and accessible via the command line.
![Docker Version Verification](./screenshots/01_verify_docker.png)

### 2. Building the Image
After setting up the `app.py` and `Dockerfile`, I executed the build command to create the `docker-lab1-app` image.
![Docker Build Process](./screenshots/02_build_image.png)

### 3. Verification of Image and Container Run
I verified that the image was created successfully and then ran the container to see the expected output: **"Hello from Docker Container!"**.
![Terminal Run and Output](./screenshots/04_run_and_verify_output.png)

### 4. Docker Desktop Monitoring
I used the Docker Desktop GUI to monitor the container status and inspect the logs to ensure the application executed correctly.
![Docker Desktop Containers](./screenshots/03_docker_desktop_containers.png)
![Container Logs Verification](./screenshots/05_docker_desktop_logs.png)

### 5. Cleanup and Resource Management
As per Step 8 of the lab manual, I performed a full cleanup to reclaim system resources. This involved stopping the container, removing the instance, and deleting the Docker image.
![Cleanup Verification](./screenshots/06_cleanup_verification.png)

---

## 🧠 Guide Questions

### 1. What role does the Dockerfile play in containerization?
The Dockerfile acts as the blueprint or manifest for the container. It contains the exact instructions (base image, environment setup, file copying, and start command) needed to recreate the application environment consistently on any machine.

### 2. Why are Docker containers lighter than virtual machines?
Containers are lighter because they share the host system's kernel instead of virtualizing a full operating system. This reduces overhead, saves disk space, and allows for near-instant startup times.

### 3. What happens when the container finishes execution?
Once the primary process (the Python script) finishes, the container enters an "Exited" state. It stops consuming CPU and RAM but remains in the system's record until it is manually removed.