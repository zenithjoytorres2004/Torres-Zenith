
# Docker Compose Guide

## Introduction

Docker Compose is a tool used to define and run multi-container Docker applications. Instead of manually creating each container separately, Docker Compose uses a YAML file to describe the services, configuration, ports, and environment variables required by the application.

For this mission, Docker Compose was used to deploy a Nextcloud application container and a MariaDB database container.

## The `services:` Block

The `services:` block defines the containers or services that make up the application.

In this deployment, there are two services:

```yaml
services:
  database:
    image: mariadb:10.6

  app:
    image: nextcloud
```

The `database` service runs the MariaDB container, while the `app` service runs the Nextcloud container.

Each service can have its own image, environment variables, ports, and other configuration settings.

## Database Service

The database service uses the MariaDB 10.6 image:

```yaml
database:
  image: mariadb:10.6
```

It also contains environment variables used to configure the database:

```yaml
environment:
  - MYSQL_ROOT_PASSWORD=cloudnova_root
  - MYSQL_PASSWORD=cloudnova_pass
  - MYSQL_DATABASE=nextcloud_db
  - MYSQL_USER=nextcloud_user
```

These variables create the database credentials and database name required by Nextcloud.

## Nextcloud Application Service

The application service uses the Nextcloud image:

```yaml
app:
  image: nextcloud
```

The application is exposed through port 8080:

```yaml
ports:
  - 8080:80
```

This allows the Nextcloud web interface to be accessed through port 8080.

## How Does Nextcloud Find the Database?

The Nextcloud application knows where to find the MariaDB container because of the following environment variable:

```yaml
- MYSQL_HOST=database
```

The value `database` matches the service name of the MariaDB container:

```yaml
database:
  image: mariadb:10.6
```

Docker Compose creates a network for the services, allowing containers to communicate with each other using their service names. Therefore, Nextcloud can connect to MariaDB using `database` as the hostname.

## Docker Run vs Docker Compose Up

The `docker run` command is normally used to create and start an individual Docker container. When an application requires several containers, each container may need to be configured and started separately.

Docker Compose uses a YAML configuration file to define multiple services. The command:

```bash
docker-compose up -d
```

can create and start all the services defined in the Compose file at the same time.

The `-d` option runs the containers in detached mode, allowing the terminal to be used for other commands while the containers continue running.

## Deployment Commands

The following commands were used:

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Infrastructure as Code

Infrastructure as Code (IaC) means defining infrastructure and its configuration using code instead of manually configuring every component. The `docker-compose.yml` file acts as a blueprint for the application because it contains the configuration needed to deploy the Nextcloud and MariaDB services.

Using IaC makes deployments more consistent, repeatable, and easier to manage.
