<div align="center">

# RuleEngine

</div>


This repository contains a full-stack project developed using the MERN stack (MongoDB, Express.js, React, and Node.js) that fetches local weather data from weather API and displays it on the dashboard. Moreover it includes following features as well :-

● Error handling for invalid rule strings or data formats (e.g., missing operators, invalid comparisons).

● Validations for attributes to be part of a catalog.


## Frontend

The frontend is built using Next.js with TypeScript, providing server-side rendering and static site generation. It includes pages for managing rules and visualizing rule evaluations.

Next.js: Handles routing and rendering of components.
TypeScript: Ensures type safety and better development experience.
Styled Components: For styling the application with ease.

## Backend

The backend is developed using Node.js with TypeScript, acting as the core engine for rule evaluation and management. It interacts with the PostgreSQL database using Prisma.

Node.js: Provides a robust and scalable runtime environment.
TypeScript: Ensures type safety and maintainability.
Express.js: Handles API requests and serves the frontend.
Prisma: ORM for PostgreSQL, enabling efficient data querying and management.

## Database

The project uses PostgreSQL for reliable and efficient data storage. Prisma ORM is used to interact with the database, providing a type-safe and intuitive API for database operations.

## Installation and Setup


# Running App

**Frontend-side Application**

```bash
  cd frontend
```

```bash
  npm install
```

```bash
  npm run dev
```

**Backend-side Application**

```bash
  cd backend
```

```bash
  npm install
```

```bash
  npm start
```


## Tech Stack

**Frontend:** Next.js, TypeScript

**Backend:** Node.js, TypeScript, Express.js

**Database:** PostgreSQL, Prisma
Deployment Instructions
Overview
This section provides step-by-step instructions on how to deploy the application using Docker and AWS EC2 for a cloud-based deployment.

Prerequisites
Before proceeding with the deployment, ensure you have the following:

AWS EC2 instance (Ubuntu or any other Linux distribution with Docker installed)
Docker and Docker Compose installed on the EC2 instance
GitHub repository links for both applications
DockerHub account to store the Docker images
Step 1: Setup the EC2 Instance
Launch an EC2 instance:

Choose an Ubuntu AMI or any other preferred Linux distribution.
Select an instance type (e.g., t2.micro for testing).
Configure the Security Group:
Allow HTTP (port 80) and Custom TCP Rule (port 5100) for accessing the applications.
Allow SSH (port 22) for accessing the server.

Connect to the EC2 instance:

Use SSH to connect:

```bash
  ssh -i /path/to/your-key.pem ubuntu@your-ec2-public-ip
```
Step 2: Install Docker and Docker Compose
Update the package manager:
```bash
  sudo apt update
```
Install Docker:
```bash
  sudo apt install -y docker.io

```
Install Docker Compose:
```bash
  sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

```
Verify the installations:
```bash
  docker --version
docker-compose --version

```
Step 3: Clone the Repositories
Clone the repositories for both applications:
```bash
  git clone https://github.com/your-username/rule-engine-with-ast.git
git clone https://github.com/your-username/real-time-weather-monitoring.git

```
Navigate to each project directory to deploy the applications.

Step 4: Configure Docker Compose for Multi-Container Deployment
Ensure the docker-compose.yml file is correctly configured in each project directory.

Build and run the containers using Docker Compose:
```bash
  docker-compose up --build -d
```
Step 5: Verify Deployment
Access the applications:

Rule Engine: http://your-ec2-public-ip:5100
Weather Monitoring: http://your-ec2-public-ip:3000 (or configured port)
Verify the services are running using:



## Feedback

If you have any feedback, please reach out to me at mk9355297@gmail.com
