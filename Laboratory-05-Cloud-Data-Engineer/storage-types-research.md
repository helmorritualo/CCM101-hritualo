# Checkpoint 2: Research – Types of Cloud Storage

## Cloud Storage Comparison Table

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Breaks data into fixed-sized blocks, each with a unique identifier. Data does not contain higher-level metadata and is managed directly by an operating system as raw storage volumes. | Operating system boot drives, transactional databases (e.g., MySQL, PostgreSQL), and virtual machine disks requiring low-latency, high-IOPS performance. | **AWS:** Amazon EBS (Elastic Block Store)<br>**Azure:** Azure Managed Disks<br>**GCP:** Google Cloud Persistent Disk |
| **File Storage** | Stores data in a hierarchical tree structure using files and folders, accessible through shared network protocols (NFS/SMB). Multiple compute instances can mount and access the same files concurrently. | Shared network file systems, content management systems (CMS), code repositories, and collaborative enterprise file shares. | **AWS:** Amazon EFS (Elastic File System)<br>**Azure:** Azure Files<br>**GCP:** Google Cloud Filestore |
| **Object Storage** | Stores data as distinct, discrete objects within a flat address space (no folders). Each object includes the raw data, an extensive set of customizable metadata, and a globally unique identifier (accessible via REST/HTTP APIs). | Unstructured data at massive scale, user-uploaded multimedia (photos, videos), static website hosting, log archives, and automated disaster recovery backups. | **AWS:** Amazon S3 (Simple Storage Service)<br>**Azure:** Azure Blob Storage<br>**GCP:** Google Cloud Storage |

---

## Storage Recommendation for Client

Dear Client,

Object Storage is the ideal solution for your photo-sharing application because it is designed to store massive volumes of unstructured media efficiently without the structural bottlenecks or storage limits of traditional hierarchical file systems. Unlike block or file storage, object storage scales virtually limitlessly and allows you to attach custom metadata (such as user ID, resolution, and upload timestamp) directly to each image file. Furthermore, photos are served directly and securely over the web via simple HTTP/REST API endpoints, drastically simplifying access for your web front-end and mobile apps while significantly lowering hosting costs.