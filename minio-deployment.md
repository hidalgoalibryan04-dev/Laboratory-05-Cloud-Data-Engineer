# MinIO Deployment

## Overview

For this mission, I deployed **MinIO**, an S3-compatible object storage server, using Docker in the KillerCoda Ubuntu Playground. MinIO provides a web-based console that can be used to manage buckets and uploaded objects.

## Docker Deployment Command

The following Docker command was used to deploy the MinIO server:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
minio/minio server /data --console-address ":9001"
```

### Explanation of the Command

| Command/Option | Purpose |
|---|---|
| `docker run -d` | Creates and starts the container in detached mode. |
| `-p 9000:9000` | Maps port 9000 of the MinIO container to port 9000 on the host for the MinIO API. |
| `-p 9001:9001` | Maps port 9001 of the MinIO container to port 9001 on the host for the MinIO Web Console. |
| `--name minio-server` | Gives the Docker container the name `minio-server`. |
| `-e "MINIO_ROOT_USER=cloudadmin"` | Sets the MinIO administrator username through an environment variable. |
| `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` | Sets the MinIO administrator password through an environment variable. |
| `minio/minio` | Specifies the MinIO Docker image to use. |
| `server /data` | Starts MinIO as an object storage server using `/data` as its storage location. |
| `--console-address ":9001"` | Configures the MinIO Web Console to listen on port 9001. |

## Verifying the Container

After starting MinIO, I verified that the container was running using:

```bash
docker ps
```

The running container should appear with the name:

```text
minio-server
```

## MinIO Web Console

The MinIO Web Console was accessed through the KillerCoda port forwarding feature.

**Web Console Port:**

```text
9001
```

The credentials used for the laboratory deployment were:

```text
Username: cloudadmin
Password: CloudNova2026!
```

> **Security Note:** These credentials are laboratory credentials provided for this exercise. In a real production environment, administrator credentials should be stored securely and should not be committed to a public GitHub repository.

## Bucket Created

A bucket named:

```text
client-photos
```

was created through the MinIO Web Console.

The bucket was used to store a test image or text file, demonstrating that the object storage server was working correctly.

## Screenshots

### MinIO Deployment

The screenshot below should show the successful MinIO deployment and the running Docker container.

**File:** `screenshots/minio-deployed.png`

### Bucket and Uploaded Object

The screenshot below should show the MinIO Web Console with the `client-photos` bucket and the uploaded test file.

**File:** `screenshots/minio-bucket-upload.png`

## Result

The MinIO deployment successfully demonstrated how Docker can be used to run an S3-compatible object storage service. The server was accessed through port 9001, a bucket named `client-photos` was created, and a test object was uploaded successfully.
