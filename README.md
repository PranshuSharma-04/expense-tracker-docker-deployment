
# Expense Tracker – AWS EC2 Deployment

## Overview

This repository documents the deployment of an existing Expense Tracker web application on AWS EC2 using Docker and Docker Compose.

The application uses Java Spring Boot for the backend and MySQL for database management.

## Technology Stack

- AWS EC2 (Ubuntu)
- Docker
- Docker Compose
- Java Spring Boot
- MySQL
- Docker Hub

## Deployment Architecture

The application runs using two Docker containers:

1. **Spring Boot Application** – Runs the Expense Tracker web application on port 8080.
2. **MySQL Database** – Stores application data in the `expenses_tracker` database.

Both containers communicate through a custom Docker network named `appbridge`.

## My Contributions

My primary contribution was deploying and configuring the existing application on AWS EC2.

- Deployed the application on an AWS EC2 Ubuntu instance.
- Configured application and database containers using Docker Compose.
- Configured communication between containers using a custom Docker network.
- Configured persistent database storage.
- Set up database healthchecks and container restart policies.
- Exposed the application through port 8080.

## Repository Structure

```text
expense-tracker-docker-deployment/
│
├── README.md
└── docs/
    ├── Dockerfile
    ├── docker-compose.yml
    └── deployment-guide.md
```

## Documentation

- [Deployment Guide](docs/deployment-guide.md)
- [Docker Compose Configuration](docs/docker-compose.yml)
- [Dockerfile Reference](docs/Dockerfile)

## Original Application

This deployment is based on the original project:

[Expenses-Tracker-WebApp](https://github.com/LondheShubham153/Expenses-Tracker-WebApp)

The original application was developed by its respective author. This repository documents my deployment work and configuration.

## Disclaimer

This repository is intended as a deployment portfolio and documentation reference. It does not contain the original application source code or a complete standalone deployment environment.

