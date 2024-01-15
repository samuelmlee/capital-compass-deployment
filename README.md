# Capital Compass Services Deployment

This repository contains Docker Compose configurations for deploying the Capital Compass microservices. There are two
deployment configurations: one for deployment on an Amazon EC2 instance and another for local deployment.

## Prerequisites

- Docker and Docker Compose installed on your system.
- For EC2 deployment, an AWS EC2 instance set up with Docker.
- For local deployment, ensure AWS credentials are configured on your machine and update the path to your .aws
  credentials.

## Structure

The repository includes the following key files:

- `docker-compose-ec2.yml`: Docker Compose configuration for deploying services on an EC2 instance.
- `docker-compose-local.yml`: Docker Compose configuration for deploying services locally.

## Deployment on EC2 Instance

The `docker-compose-ec2.yml` file is configured for deployment on an Amazon EC2 instance. It includes services like
user-service, stock-service, gateway, and Redis.

### EC2 Deployment Steps:

1. SSH into your EC2 instance.
2. Clone this repository to your EC2 instance.
3. Navigate to the directory containing `docker-compose-ec2.yml`.
4. Run the following command to start the services:
   `docker-compose -d -f docker-compose-ec2.yml up`

### Local Deployment

The `docker-compose-local.yml` file is configured for deployment on your local machine and includes volume mappings for
local AWS credentials.

### Local Deployment Steps:

1. Ensure your AWS credentials are configured correctly on your machine.
2. Clone this repository to your local machine.
3. Navigate to the directory containing docker-compose-local.yml
4. Run the following command to start the services:
   `docker-compose -d -f docker-compose-local.yml up`


