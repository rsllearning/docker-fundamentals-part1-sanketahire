# Docker Fundamentals — Part 1

This repository contains the practical implementation and documentation for **Docker Fundamentals (Part 1)**. The objective of this training assignment is to establish hands-on proficiency in containerization concepts and Docker CLI operations for day-to-day software development.

> 💡 **Assignment Submission Report:** For the complete step-by-step walkthrough, theoretical principles, command-output pairings, and evidence deliverables, please refer directly to [SOLUTION.md](SOLUTION.md).

---

## Overview

Modern software development requires consistent, reproducible, and isolated runtime environments to eliminate the traditional *"it works on my machine"* problem. This project demonstrates how to containerize and manage a web server using the official **Nginx** image from Docker Hub, applying core containerization principles, configuration management, and lifecycle controls.

---

## Assignment Tasks

1. **Task 1: Obtain the Docker Image**
   * Search for and pull the official Nginx image from Docker Hub.
   * Verify the image's presence and integrity in the local image cache.

2. **Task 2: Run the Web Server**
   * Deploy an Nginx container named `training-web` in detached background mode (`-d`).
   * Bridge host port `8080` to container port `80` (`-p 8080:80`).
   * Verify HTTP accessibility via browser and curl.

3. **Task 3: Configure the Container Using an Environment Variable**
   * Demonstrate runtime configuration decoupling by launching a container with `APP_ENV=development`.
   * Verify the environment variable directly inside the container namespace without rebuilding the image.

4. **Task 4: Explore the Running Container**
   * Inspect stdout/stderr container logs.
   * Execute in-container inspection commands without stopping the service.
   * Query and document the 5 critical metadata properties: Container ID, Image Used, Port Mapping, Environment Variables, and Assigned Bridge IP.

5. **Task 5: Container Lifecycle Management**
   * Methodically transition the container through all four lifecycle states:
     $$\text{Running} \longrightarrow \text{Stopped (Exited)} \longrightarrow \text{Started (Up)} \longrightarrow \text{Removed}$$
   * Verify state persistence and complete cleanup.

---

## Repository Structure

```text
.
├── .gitignore                          # OS and IDE artifact exclusion rules
├── README.md                           # Repository overview and assignment roadmap
├── docs/                               # Training resources and reference specifications
│   ├── Training.Material.Docker.Part1.pdf
│   └── Training.Assignment.Docker.Part1.pdf
├── screenshots/                        # Visual verification deliverables for all tasks
└── SOLUTION.md                         # Comprehensive assignment submission report and verification logs
```

---

## Prerequisites & Environment

* **Docker Engine:** `29.x` / Docker Desktop for Mac
* **Container Base Image:** Official `nginx:latest` from Docker Hub
* **Host Operating System:** macOS (darwin/amd64)
* **Default Port Allocation:** Host `8080` $\rightarrow$ Container `80`
