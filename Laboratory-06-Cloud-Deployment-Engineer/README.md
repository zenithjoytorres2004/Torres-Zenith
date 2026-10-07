# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

This laboratory focused on deploying a multi-tier private cloud storage application using Docker Compose. The application used Nextcloud as the web/application tier and MariaDB as the database tier.

## Objectives

- Explain two-tier application architecture.
- Understand the purpose of a `docker-compose.yml` file.
- Create a YAML configuration using Nano.
- Deploy Nextcloud and MariaDB using Docker Compose.
- Access the Nextcloud web interface.
- Document Infrastructure as Code concepts using Markdown.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
