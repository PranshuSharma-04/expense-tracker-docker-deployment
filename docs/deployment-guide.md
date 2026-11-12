
# Expense Tracker – Deployment Guide

## 1. Project Overview

This project documents the deployment of an existing Expense Tracker web application on an AWS EC2 instance using Docker Compose.

The application is built with Java Spring Boot and uses MySQL as its database.

**Original application repository:**  
https://github.com/LondheShubham153/Expenses-Tracker-WebApp

## 2. Deployment Architecture

The deployment consists of two Docker containers:

- **Main Application:** Runs the Expense Tracker application using a prebuilt Docker Hub image.
- **MySQL:** Provides database storage for the application.

Both containers communicate through a custom Docker network named `appbridge`.

## 3. Technologies Used

- AWS EC2
- Ubuntu
- Docker
- Docker Compose
- Java Spring Boot
- MySQL
- Docker Hub

## 4. Container Configuration

### MySQL Container

- Image: `mysql:latest`
- Container name: `mysql`
- Database: `expenses_tracker`
- Persistent storage: `./mysql-data`
- Healthcheck configured to verify database availability.

### Application Container

- Image: `snehcreate/expensetracker_v3`
- Container name: `Expensetracker`
- Application port: `8080`
- Database connection through the `appbridge` network.

## 5. Deployment Configuration

The Docker Compose configuration defines:

- Two application services.
- A custom bridge network for container communication.
- MySQL data persistence using a host bind mount.
- Environment variables for database credentials.
- Automatic container restart policies.
- A MySQL healthcheck.

The application is exposed on port `8080` of the EC2 instance.

## 6. My Contribution

My work focused on deploying and configuring the existing application rather than developing its original source code.

My deployment work included:

- Deploying the application on AWS EC2.
- Configuring Docker containers using Docker Compose.
- Connecting the Spring Boot application with MySQL.
- Configuring container networking and database storage.
- Exposing the application through port `8080`.
- Configuring database healthchecks and restart policies.

## 7. Configuration Reference

The Docker Compose and Dockerfile references are available in this repository under the `docs/` directory.

**Note:** These files document the deployment configuration. This repository does not contain the original application source code or a complete standalone deployment environment.

