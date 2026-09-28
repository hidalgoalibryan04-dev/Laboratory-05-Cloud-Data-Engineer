# Mission 5 Reflection

This laboratory activity helped me understand why object storage is commonly used for applications that need to store a very large amount of unstructured data. For a photo-sharing application, object storage is more suitable than a traditional block storage hard drive because it is designed to handle large collections of files such as images, videos, documents, and backups. Instead of managing individual disk blocks, applications can store and retrieve objects through a storage service. This makes object storage useful for applications that may continue to grow to millions of photos.

Docker also made deploying MinIO easier because I did not need to manually install and configure all of the software required by the storage server. The Docker command downloaded the MinIO image and started the service inside a container. I also learned how port mapping allows a service running inside a container to be accessed from outside the container. In this activity, port 9001 was used to access the MinIO Web Console.

A bucket is a storage container used to organize objects in an object storage system. In this activity, I created a bucket called `client-photos` and used it to store a test file. This helped me understand how cloud applications can organize uploaded files.

Large enterprise companies can protect object storage data from physical server failures by using redundancy, replication, backups, and multiple storage servers or locations. If one physical server fails, copies of the data can remain available on other systems. Cloud providers can also use distributed storage systems to reduce the risk of losing data from a single hardware failure.

My confidence in using the Linux command line is also improving. I became more comfortable running Docker commands, checking containers, working with ports, and verifying whether a service was running. This activity showed me that command-line skills are important for cloud computing because many cloud services and deployment tasks require terminal commands.
