# Containerization of .NET Core Application with SSL Enabled

This repository demonstrates how to containerize a .NET Core application with SSL enabled using Docker. The Dockerfile consists of multiple stages to build, publish, and run the application securely. A full video of this is available on my YouTube channel [NandiTechBytes](https://youtube.com/@nanditechbytes?si=VAYw-lOAddK1vyB-).


## Dockerfile Overview

The Dockerfile is divided into five stages:

1. **Generate Development Certificate**
2. **Set Up Base Image**
3. **Build the Application**
4. **Publish the Application**
5. **Create Final Image**

## Pre-Requisite
1. **Docker installed**

## How to Use

1. **Fork and clone the Repository**
2. **Navigate inside the repository**
3. **Command to build the image**
```
docker build -t your-app-name --build-arg  CERT_PASSWORD=yourpassword .
```
4. **Command to run the container**
```
docker run -d -p 443:443 --name your-container-name your-app-name
```
5. **Access the app on your browser using
```
https://localhost:443
```