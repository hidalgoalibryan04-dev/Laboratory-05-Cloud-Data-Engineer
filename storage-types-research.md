# Storage Types Research

## Comparison of Cloud Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Stores data in fixed-size blocks that can be attached to a virtual server and accessed like a traditional disk. | Best for operating systems, databases, and applications that require fast and low-latency disk access. | **AWS EBS (Elastic Block Store)** |
| **File Storage** | Stores data as files organized into folders and directories. Multiple systems can access the same file system over a network. | Best for shared files, documents, media directories, and applications that require a traditional file system. | **AWS EFS (Elastic File System)** |
| **Object Storage** | Stores data as objects containing the file, metadata, and a unique identifier inside containers called buckets. | Best for large amounts of unstructured data such as photos, videos, backups, documents, and logs. | **AWS S3 (Simple Storage Service)** |

## Why Object Storage Is Suitable for the Client

Object Storage is the best choice for the client's photo-sharing application because it is designed to store large amounts of unstructured data such as millions of images. Objects can be organized in buckets and accessed through APIs, making the storage suitable for applications that need scalable and accessible image storage.
