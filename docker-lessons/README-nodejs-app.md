# Containerized Node.js Application

This is a simple Node.js application that can be containerized and accessed through a web browser. It's part of the AWS DevOps Zero to Hero learning journey.

## Prerequisites

- Node.js (for local development)
- Docker
- Docker Compose (optional)

## Running Locally (without Docker)

**Note** : you have to install nodejs locally if you want to test the application locally on your host machine.

to check if nodejs is installed, do the command
```node --version``` or just ```node -v```

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the application:
   ```bash
   npm start
   ```

3. Access the application in your browser at http://localhost:3000

## Running with Docker

### Build and run using Docker commands

1. Build the Docker image:
   ```bash
   docker build -t nodejs-app .
   ```

2. Run the container in the background (detached mode):
   ```bash
   docker run -p 3000:3000 -d nodejs-app
   ```

   Or run in the foreground (interactive mode):
   ```bash
   docker run -p 3000:3000 nodejs-app
   ```

3. Access the application in your browser at http://localhost:3000

### Using Docker Compose

1. Build and start the container in the background:
   ```bash
   docker-compose up -d
   ```

   Or build and start in the foreground:
   ```bash
   docker-compose up
   ```

2. Access the application in your browser at http://localhost:3000

3. Stop the container:
   ```bash
   docker-compose down
   ```

## Deploying to AWS

This application can be deployed to various AWS services:

- AWS ECS (Elastic Container Service)
- AWS ECR (Elastic Container Registry) for storing the Docker image
- AWS Fargate for serverless container deployment
docker - AWS App Runner for simplified container deployment

Follow the AWS DevOps Zero to Hero course for detailed instructions on deploying this application to AWS services.

## LESSONS QUESTIONS
1. Modify the application port to 3500 in the app.js file and also in the Docker file 
2. Build your own application image and name it __**my-app-image**__ using the steps outlined in the README_nodejs-app.md
3. Run the application container on ```hostport:container-port``` using this format 2000:3500 and show on the browser.