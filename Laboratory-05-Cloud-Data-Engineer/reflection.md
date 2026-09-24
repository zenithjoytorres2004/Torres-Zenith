
# Mission Reflection

Object storage is better suited for storing millions of photos because it is designed for large amounts of unstructured data. Unlike traditional block storage, object storage organizes data as objects with metadata and unique identifiers. This makes it easier to manage large collections of images and allows the storage system to scale as the number of files increases. Object storage is also commonly used for photos, videos, backups, and other files that do not require a traditional file system.

Docker made it easier to deploy the MinIO storage server because the required application and its environment could be started using a single Docker command. Instead of manually installing and configuring MinIO and its dependencies, Docker created a container with the necessary settings. The port mappings and environment variables also allowed the server to be configured quickly and consistently.

A bucket is a container used by object storage to organize and store objects. In this activity, the bucket named `client-photos` was used to store the uploaded test file. The bucket provides a logical location where the application's images can be managed.

Large enterprise companies can protect object storage data from physical server failures by using redundancy and replication. Data can be stored across multiple physical servers, disks, or locations. If one server fails, another copy of the data can remain available. Backup systems, replication, monitoring, and data recovery processes can also help prevent permanent data loss.

My confidence in navigating the Linux command line is growing because I am becoming more familiar with commands and terminal-based tasks. In this activity, I used Docker commands to deploy MinIO and used `docker ps` to verify that the container was running. These tasks helped me understand how command-line tools are used to manage cloud infrastructure.
