
# .NET 7 Blazor App Integrated with Redis

This repository contains an example application built with .NET 7 and Blazor, integrated with Redis. The purpose of this application is to demonstrate the capabilities of Redis as a data store for a Blazor application. 

## Overview

The application uses a Redis instance running in a Docker container. The container listens for requests from the Blazor application. This setup allows us to explore and test all that Redis has to offer in a contained and controlled environment.

## Getting Started

To get started with this application, you will need to have Docker installed on your machine. Once Docker is installed, you can use the following commands to manage your Docker containers and images.

### Docker and Redis CLI Commands

- `docker run --name my-redis -p 5002:6379 -d redis` 
  - This command runs the Redis docker container named my-redis. The container listens on port 6379 internally and port 5002 externally.

- `docker ps -a` 
  - This command lists all Docker containers.

- `docker exec -it my-redis sh` 
  - This command opens a shell inside the Redis container.

- `docker stop 22a` 
  - This command stops the Docker container with the id that starts with "22a".

- `docker rm 22a` 
  - This command removes the Docker container with the id that starts with "22a".

- `docker images` 
  - This command lists all available Docker images.

### Redis Commands

- `ping` 
  - This command checks the connection to the Redis server. If the server is running and accessible, it will return "PONG".

- `select 0` 
  - This command selects the database instance 0.

- `dbsize` 
  - This command returns the size of the selected database.

- `scan 0` 
  - This command retrieves key/value pairs from database instance 0.

- `hgetall "<key>"` 
  - This command displays all the fields and values of the hash stored at `<key>`.