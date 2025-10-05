# Dockerized Firefox GUI Browser

This project demonstrates how to deploy a Docker container running a firefox GUI based browser. This setup allows you to run Firefox in an isolated environment with a graphical interface, suitable for testing, development or secure browsing. 

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Setup Instructions](setup-instructions)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

 ## Overview
- This project creates a Docker container that runs Firefox with a graphical user interface (GUI). The container uses a lightweight desktop environment (e.g., XFCE) and exposes the GUI via VNC, allowing you to access Firefox remotely or locally using a VNC client. This is useful for:
- Running Firefox in an isolated environment.
- Testing web applications in a clean browser instance.
- Experimenting with containerized GUI applications.

## Prerequisites 
Before setting up the project, ensure you have the following installed:
- [Docker](https://www.docker.com/get-started) (version 20.10 or higher recommended)
- A VNC viewer (e.g., [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/)
- A system with sufficient resources (at least 2GB RAM for the container)

## Setup Instructions 
Follow these steps to set up and run the Dockerized Firefox browser:
- Download docker by using the following command: sudo apt-get update && sudo apt-get install -y docker.io
- Now run this command:
- docker run -d \
- --name=firefox \
- -p 3000:3000 \
- -p 3001:3001 \
- -e PUID=$(id -u) \
- -e PGID=$(ID -g) \
- -e TZ=Europe/Dublin \
- -v /path/to/config:/config \
- --shm-size="1gb" \
- linuxserver/firefox

- To make sure container is running use the docker ps command.
- Next navigate to your browser and enter https://localhost:3000
- This will bring up your browser being run from your Docker container.
- To check firefox logs for any issues use the following command: docker logs firefox --tail20

## Usage
Run the container installation command:
![Container Installation](Screenshot (36).png)

## Benefits of using a Dockerized browser:

- Isolation and Security
- Cross Platform Portability
- Great for Testing and Development




