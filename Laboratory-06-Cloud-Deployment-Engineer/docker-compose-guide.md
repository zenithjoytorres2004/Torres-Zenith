
# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the containers that will be created and managed by Docker Compose. In this project, there are two services: `database` for MariaDB and `app` for Nextcloud.

## How Does Nextcloud Find the Database?

The Nextcloud container uses the `MYSQL_HOST` environment variable to find the database container. The value is set to `database`, which is the service name of the MariaDB container.

```yaml
- MYSQL_HOST=database
