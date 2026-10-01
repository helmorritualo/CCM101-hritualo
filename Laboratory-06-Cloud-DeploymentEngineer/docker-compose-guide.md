# Docker Compose Guide

## Introduction

Docker Compose is used to define and manage multiple containers as a single application stack. In this laboratory activity, Docker Compose was used to deploy a two-tier private cloud storage system consisting of a Nextcloud application container and a MariaDB database container.

## The `services:` Block

The `services:` block defines the containers that make up the application.

In the Compose file, two services were defined:

- `database` — uses the `mariadb:10.6` image and provides the database for Nextcloud.
- `app` — uses the `nextcloud` image and provides the Nextcloud web application.

Each service contains its own configuration, including the Docker image, environment variables, and, for the application service, the port mapping.

## How Nextcloud Finds the Database

The Nextcloud application uses the following environment variable:

```yaml
- MYSQL_HOST=database
```

The value `database` refers to the name of the MariaDB service defined in the `services:` block. This allows the Nextcloud application container to identify and communicate with the database container using the service name.

The other database-related environment variables provide the information required for the connection:

```yaml
- MYSQL_PASSWORD=cloudnova_pass
- MYSQL_DATABASE=nextcloud_db
- MYSQL_USER=nextcloud_user
```

The database service uses the corresponding configuration:

```yaml
- MYSQL_PASSWORD=cloudnova_pass
- MYSQL_DATABASE=nextcloud_db
- MYSQL_USER=nextcloud_user
```

This allows the two containers to work together as part of the same application stack.

## `docker run` vs `docker-compose up -d`

`docker run` is used to create and start an individual Docker container by providing the required options directly in a command. This approach is useful for running a single container, but managing several related containers can require multiple commands and repeated configuration.

`docker-compose up -d` uses the configuration written in `docker-compose.yml` to create and start the services defined in the file. In this activity, one command was used to deploy both the Nextcloud application and MariaDB database in the configured stack.

The `-d` option starts the services in detached mode, allowing them to continue running in the background while the terminal remains available.

## Port Mapping

The Nextcloud application uses the following port configuration:

```yaml
ports:
    - 8080:80
```

Port `8080` on the host is mapped to port `80` inside the Nextcloud container. This allows the Nextcloud web interface to be accessed through port `8080` in the KillerCoda environment.

## Summary

The Compose file acts as a deployment blueprint for the multi-container application. Instead of manually configuring each container separately, the services and their required settings are defined together in one YAML file, making the deployment process more organized and repeatable.
