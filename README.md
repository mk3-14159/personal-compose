<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/mk3-14159/personal-compose">
    <img src="docs/kraken.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Personal Compose</h3>

  <p align="center">
    list of compose files for testing, development and staging projects
    <br />
    <br />
    <br />
    <a href="https://github.com/mk3-14159/personal-compose">View Demo</a>
    ·
    <a href="https://github.com/mk3-14159/personal-compose/issues">Report Bug</a>
    ·
    <a href="https://github.com/mk3-14159/personal-compose/issues">Request Feature</a>
  </p>
</div>

> **Note**
> These are my personal configurations for use in local development / experiments. These samples must not be deployed in production environments.

## Introduction
These instructions will get you through the bootstrap phase of creating and deploying samples of containerized applications with Docker Compose.

## Prerequisites
1. Docker and Docker Compose installed
    - Windows / Macos - Install latest Docker Desktop
    - Linux - Install Docker and Docker Compose 
2. Download samples from the repository

## Running a sample 
The root directory should contain the *compose.yml* which describes the configurations of the service components. Use the following commands to:

Start and run inside the container environment, (--rm) tell the Docker Daemon to clean up the container and remove the file system after the container exits
```bash 
docker compose run --rm <USER>
```

Start all services in the background and run in (-d) detached mode 
```bash
docker compose up -d 
```

Attach yourself to the logs of the running services, (-f) to follow the logs, (-t) to specify the timestamps 
```bash
# for all container logs
docker compose logs -f -t

# for a single container log
docker compose logs -f -t <name-of-service>
```

Stop and remove all containers
```bash 
docker compose down
```

TODO:
  get compose for windows image


