# Docker Technical Questions

## What is Docker?
### Docker is a platform that enables developers to develop, deploy, and run applications in containers.

## Docker's most notable features:
### Portability, lightweight, scalability, isolation, and version control.

## Why use Docker?
### Docker simplifies the process of creating, deploying, and managing applications by using containers, which are portable and efficient.

## Difference between a Docker container and a virtual machine:
### A Docker container shares the host OS kernel, making it lightweight and faster to start compared to a virtual machine, which runs a full OS.

## How to create a Docker image:
### Create a Dockerfile with instructions to build the image, then use the `docker build` command to create the image.

## What is a Dockerfile and how is it used:
### A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.

## How to run a Docker container:
### Use the `docker run` command followed by the image name to run a Docker container.

## Difference between Docker run and Docker create:
### `docker run` creates and starts a container in one operation, while `docker create` creates a container but does not start it.

## How to link containers in Docker:
### Use Docker networks or Docker Compose to link containers.

## What is Docker Compose and how is it used:
### Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to configure the application’s services.

## How to scale Docker containers:
### Use Docker Swarm or Kubernetes for container orchestration to scale containers horizontally.

## What is Docker Swarm and its purpose:
### Docker Swarm is a native clustering tool for Docker that allows you to create and manage a cluster of Docker nodes.

## How to manage Docker volumes:
### Use the `docker volume` command to manage Docker volumes, which are used to persist data generated by and used by Docker containers.

## Concept of Docker networking:
### Docker networking allows containers to communicate with each other and the outside world.

## Difference between an image and a container in Docker:
### An image is a template for creating containers, while a container is a running instance of an image.

## How to update a Docker image:
### Modify the Dockerfile, rebuild the image with a new tag, and then redeploy the updated image.

## Purpose of Docker registry:
### Docker registry is a repository for Docker images where you can store and retrieve images.

## How to remove a Docker container:
### Use the `docker rm` command followed by the container ID or name to remove a Docker container.

## Difference between Docker restart and Docker stop/start:
### `docker restart` restarts a container, keeping its configuration, while `docker stop/start` stops and starts a container from its last state.

## How to troubleshoot issues in Docker containers:
### Check container logs, inspect container configuration, and use `docker exec` to access a running container for troubleshooting.