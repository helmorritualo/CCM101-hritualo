# Mission Reflection

This laboratory helped me understand why object storage is useful for applications that need to handle a large amount of unstructured data. Object storage is better suited for storing millions of photos because photos are individual objects that can be stored and accessed without depending on a traditional file system or fixed disk structure. It is designed for large-scale storage and works well for data such as images, videos, and backups. In comparison, block storage is more like a traditional hard drive where data is organized into blocks and is commonly attached to a server.

Docker also made deploying MinIO much easier because I did not have to manually install and configure every component of the storage server. A single Docker command downloaded the image, created the container, configured the required environment variables, and exposed the ports needed for the MinIO API and Web Console. This made the deployment process more repeatable and easier to manage.

A bucket in object storage can be understood as a logical container used to organize and store objects. In this activity, the `client-photos` bucket was created to hold the sample file representing user-uploaded photos.

For large enterprise systems, data can be protected from physical server failures by keeping multiple copies of data and distributing them across different storage devices or servers. Organizations can also use replication and backups so that data remains available even when hardware fails. These approaches help reduce the risk of permanent data loss.

My confidence in navigating the Linux command line is also improving through this activity. I was able to use Docker commands to deploy and verify a container, inspect its status, and work with a cloud storage service. This showed me that the command line can be an efficient way to manage cloud infrastructure and containerized services.