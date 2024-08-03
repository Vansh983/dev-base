# Docker Commands

## Overview
- [Docker Commands](#docker-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing Docker](#installing-docker)
  - [Checking Docker Version](#checking-docker-version)
  - [Pulling an Image](#pulling-an-image)
  - [Listing Docker Images](#listing-docker-images)
  - [Running a Container](#running-a-container)
  - [Listing Running Containers](#listing-running-containers)
  - [Stopping a Container](#stopping-a-container)
  - [Starting a Container](#starting-a-container)
  - [Removing a Container](#removing-a-container)
  - [Removing an Image](#removing-an-image)
  - [Viewing Container Logs](#viewing-container-logs)
  - [Executing Commands in a Container](#executing-commands-in-a-container)
  - [Docker Compose](#docker-compose)
  - [Docker Networking](#docker-networking)
  - [Docker Volumes](#docker-volumes)

## Introduction

Docker is a platform for developing, shipping, and running applications in containers. Containers allow you to package an application with all its dependencies into a standardized unit for software development.

## Installing Docker

To install Docker, follow the instructions for your operating system on the [official Docker website](https://docs.docker.com/get-docker/).

## Checking Docker Version

To check the version of Docker installed:

```sh
docker --version
```

## Pulling an Image

To pull an image from Docker Hub:

```sh
docker pull image-name
```

Replace `image-name` with the name of the image you want to pull, for example, `docker pull nginx`.

## Listing Docker Images

To list all Docker images on your system:

```sh
docker images
```

## Running a Container

To run a container from an image:

```sh
docker run -d --name container-name image-name
```

Replace `container-name` with the name you want to assign to the container and `image-name` with the name of the image.

## Listing Running Containers

To list all running containers:

```sh
docker ps
```

To list all containers, including stopped ones:

```sh
docker ps -a
```

## Stopping a Container

To stop a running container:

```sh
docker stop container-id
```

Replace `container-id` with the ID or name of the container you want to stop.

## Starting a Container

To start a stopped container:

```sh
docker start container-id
```

Replace `container-id` with the ID or name of the container you want to start.

## Removing a Container

To remove a container:

```sh
docker rm container-id
```

Replace `container-id` with the ID or name of the container you want to remove.

## Removing an Image

To remove an image:

```sh
docker rmi image-id
```

Replace `image-id` with the ID or name of the image you want to remove.

## Viewing Container Logs

To view logs from a container:

```sh
docker logs container-id
```

Replace `container-id` with the ID or name of the container whose logs you want to view.

## Executing Commands in a Container

To execute a command in a running container:

```sh
docker exec -it container-id command
```

Replace `container-id` with the ID or name of the container and `command` with the command you want to run.

## Docker Compose

To use Docker Compose, create a `docker-compose.yml` file and run:

```sh
docker-compose up
```

To stop the services:

```sh
docker-compose down
```

## Docker Networking

To list all Docker networks:

```sh
docker network ls
```

To create a new network:

```sh
docker network create network-name
```

Replace `network-name` with the name of the network you want to create.

To connect a container to a network:

```sh
docker network connect network-name container-id
```

To disconnect a container from a network:

```sh
docker network disconnect network-name container-id
```

## Docker Volumes

To list all Docker volumes:

```sh
docker volume ls
```

To create a new volume:

```sh
docker volume create volume-name
```

Replace `volume-name` with the name of the volume you want to create.

To remove a volume:

```sh
docker volume rm volume-name
```