
# MinIO Deployment

## Docker Command

The MinIO Object Storage server was deployed using Docker in the KillerCoda Ubuntu Playground.

The following Docker command was used:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
quay.io/minio/minio server /data --console-address ":9001"
```

## Web Console Port

The MinIO Web Console was accessed using port:

**9001**

Port **9000** is used for the MinIO API, while port **9001** is used for the MinIO Web Console.

## Bucket Name

The bucket created for the client photo-sharing application was:

**client-photos**

A test file was uploaded to the bucket to verify that the object storage system was working correctly.

## Environment Variables

The `-e` flags in the Docker command are used to set environment variables inside the MinIO container.

### MINIO_ROOT_USER

```text
MINIO_ROOT_USER=cloudadmin
```

This sets the administrator username used to log in to the MinIO Web Console.

### MINIO_ROOT_PASSWORD

```text
MINIO_ROOT_PASSWORD=CloudNova2026!
```

This sets the administrator password used to access the MinIO server.

## Deployment Verification

The MinIO container was verified using the following command:

```bash
docker ps
```

The command confirmed that the MinIO container was running successfully and that ports **9000** and **9001** were exposed.
