# Docker Configuration

This project contains the necessary configuration files for setting up the development environment using Docker. The configuration includes a `docker-compose.yml` file to create and manage the containers.

## Configuration Overview

1. **Docker Compose**  
   The project utilizes Docker Compose to define and run multi-container Docker applications. The `docker-compose.yml` file describes the services required for the application, including PHP, MySQL, Nginx, and phpMyAdmin.

2. **Root Connection**  
   The configuration sets up a single connection, referred to as `root_connection`, which groups multiple containers (phpMyAdmin, MySQL, etc). This allows for seamless communication between the services within the same Docker network.

## Services

- **MySQL**: A MySQL database is used for storing application data.
- **phpMyAdmin**: Provides a web interface for managing the MySQL database.

## Usage

To start the application, run the following command:

```bash
docker network create root_connection
```

```bash
docker-compose up -d
```
