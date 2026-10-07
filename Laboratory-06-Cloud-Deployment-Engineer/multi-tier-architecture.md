

### 2. `multi-tier-architecture.md`


# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture is a system that separates an application into two main parts: the application tier and the database tier. In this activity, Nextcloud serves as the application while MariaDB works as the database.

## The Web/Application Tier

The web/application tier is responsible for providing the user interface and handling requests from users. In this activity, the Nextcloud container runs the web application and allows users to access the private cloud storage through a web browser.

## The Database Tier

The database tier is responsible for storing persistent information used by the application. MariaDB stores data such as user accounts, settings, and other Nextcloud information.

## Why Separate Them?

Separating the web application and database into different containers makes the system easier to manage and maintain. Each container has its own responsibility, so one part can be updated or managed without putting everything into a single container.
