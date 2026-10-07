


# Mission Reflection

This laboratory helped me understand how Docker Compose can make cloud deployment easier and more organized. Instead of manually typing many Docker commands for every container, I can place the configuration in a `docker-compose.yml` file. This allows the services, images, ports, and environment variables to be defined in one place. Once the file is ready, the whole application can be deployed using a single command. This makes the process faster and reduces the chance of forgetting an important configuration.

I also learned that YAML is very sensitive to indentation. Spaces are used to show the relationship between different parts of the configuration. If I use the wrong indentation or use a Tab instead of spaces, Docker Compose may not be able to read the file correctly. This can result in an error and prevent the application from starting.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` are important because they provide configuration information to the containers. They allow the Nextcloud application to know which database credentials and database name to use. The `MYSQL_HOST` variable also allows Nextcloud to find the MariaDB container through its service name.

It was interesting to see a complete cloud storage application being deployed in only a few minutes. Seeing the Nextcloud setup page through the browser made the concepts more practical and easier to understand.

Since Mission 1, my understanding of Cloud Computing has improved. I now understand that cloud computing is not only about using online services. It also involves infrastructure, containers, networking, automation, deployment, and documentation. This mission showed me how Infrastructure as Code can make cloud environments easier to deploy, manage, and repeat.
