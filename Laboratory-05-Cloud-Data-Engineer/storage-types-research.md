# Cloud Storage Types Research

## Comparison of Cloud Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Stores data in fixed-size blocks that can be attached to virtual machines as storage volumes. | Best for operating systems, databases, and applications that require fast and direct storage access. | AWS EBS |
| File Storage | Stores data as files organized in folders and directories. | Best for shared files and applications that need a traditional file system. | AWS EFS |
| Object Storage | Stores data as objects together with metadata and a unique identifier inside containers called buckets. | Best for large amounts of unstructured data such as photos, videos, documents, and backups. | AWS S3 |

## Why Object Storage?

Object Storage is the best choice for the client's photo-sharing application because it is designed to store large amounts of unstructured data such as images. It can scale to millions of files while providing easy access, durability, and metadata management.
