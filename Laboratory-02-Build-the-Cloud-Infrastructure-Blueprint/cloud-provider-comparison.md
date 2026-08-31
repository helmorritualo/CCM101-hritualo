# Cloud Provider Comparison

## Checkpoint 4: Research the Major Cloud Providers

## Objective

The objective of this checkpoint is to compare the core infrastructure services offered by **Amazon Web Services (AWS)**, **Microsoft Azure**, and **Google Cloud Platform (GCP)**. Although these providers offer similar cloud capabilities, they use different product names and organize their services differently.

## Core Infrastructure Service Comparison

| Infrastructure component           | Amazon Web Services (AWS)                                                                  | Microsoft Azure                                                             | Google Cloud Platform (GCP)                          | General purpose                                                                                                                   |
| ---------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- | ---------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Compute**                        | Amazon Elastic Compute Cloud (**Amazon EC2**)                                              | **Azure Virtual Machines**                                                  | **Compute Engine**                                   | Provides resizable virtual machines for running operating systems, applications, and workloads in the cloud.                      |
| **Storage**                        | Amazon Simple Storage Service (**Amazon S3**); Amazon Elastic Block Store (**Amazon EBS**) | **Azure Blob Storage**; **Azure Managed Disks**                             | **Cloud Storage**; **Persistent Disk**               | Object storage holds files and unstructured data, while block storage supplies persistent disks for virtual machines.             |
| **Networking**                     | Amazon Virtual Private Cloud (**Amazon VPC**)                                              | **Azure Virtual Network (VNet)**                                            | **Virtual Private Cloud (VPC)**                      | Creates logically isolated cloud networks and supports subnets, routing, security controls, private addressing, and connectivity. |
| **Identity and Access Management** | **AWS Identity and Access Management (AWS IAM)**                                           | **Microsoft Entra ID** and **Azure role-based access control (Azure RBAC)** | **Cloud Identity and Access Management (Cloud IAM)** | Controls authentication and authorization by defining who can access cloud resources and which actions they may perform.          |

## Component Discussion

### Compute

All three providers offer virtual-machine services that allocate processing power and memory on demand. AWS calls its main virtual-machine service **Amazon EC2**, Azure provides **Azure Virtual Machines**, and GCP provides **Compute Engine**. These services allow organizations to select machine configurations, install operating systems, and scale computing capacity according to workload requirements.

### Storage

Each provider offers object storage for files and unstructured data as well as block storage for virtual machines. AWS provides **Amazon S3** for object storage and **Amazon EBS** for block storage. Azure provides **Azure Blob Storage** and **Azure Managed Disks**, while GCP provides **Cloud Storage** and **Persistent Disk**.

### Networking

AWS, Azure, and GCP allow customers to create isolated virtual networks. These services are named **Amazon VPC**, **Azure Virtual Network**, and **Google Cloud VPC**, respectively. They support core networking functions such as IP addressing, subnets, routes, security rules, and connections between cloud resources.

### Identity and Access Management

Each platform provides identity and access controls based on users, groups, roles, permissions, and policies. AWS uses **AWS IAM**; Azure uses **Microsoft Entra ID** for identity services together with **Azure RBAC** for access to Azure resources; and GCP uses **Cloud IAM**. These controls support the principle of least privilege by allowing administrators to grant only the permissions required for a task.

## Guide Questions

### 1. Which cloud provider offers the broadest range of services? Explain your answer.

AWS is generally considered to offer the broadest and most mature range of cloud services across compute, storage, databases, networking, analytics, security, application integration, and other categories. It has an extensive service portfolio and supports many workload types, although the best provider still depends on an organization's technical and business requirements.

### 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?

Microsoft Azure is the most natural recommendation for an organization that primarily uses Microsoft products. Its integration with services and technologies in the Microsoft ecosystem can provide a more consistent approach to identity, administration, hybrid infrastructure, and application deployment.

### 3. Which platform is widely recognized for Artificial Intelligence, Machine Learning, and Kubernetes services?

Google Cloud Platform is widely recognized for its capabilities in artificial intelligence, machine learning, data analytics, and Kubernetes. Google originated Kubernetes and offers managed Kubernetes through **Google Kubernetes Engine (GKE)**, while its cloud platform also provides services for developing and deploying machine-learning solutions.

### 4. What similarities did you observe among the three cloud providers?

All three providers offer comparable foundational services for compute, storage, networking, and identity and access management. They also provide on-demand resource provisioning, scalability, security controls, monitoring, global infrastructure, and usage-based service models, but their product names, interfaces, and implementation details differ.

## Overall Comparison

| Consideration             | AWS                                      | Microsoft Azure                                                  | Google Cloud Platform                                |
| ------------------------- | ---------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------- |
| Notable general strength  | Broad and mature cloud service portfolio | Integration with the Microsoft ecosystem and hybrid environments | AI, machine learning, data analytics, and Kubernetes |
| Virtual-machine service   | Amazon EC2                               | Azure Virtual Machines                                           | Compute Engine                                       |
| Object-storage service    | Amazon S3                                | Azure Blob Storage                                               | Cloud Storage                                        |
| Virtual-network service   | Amazon VPC                               | Azure Virtual Network                                            | Google Cloud VPC                                     |
| Access-management service | AWS IAM                                  | Microsoft Entra ID and Azure RBAC                                | Cloud IAM                                            |

## Conclusion

AWS, Microsoft Azure, and Google Cloud Platform provide the same major categories of cloud infrastructure under different service names. AWS stands out for the breadth and maturity of its portfolio, Azure is a strong fit for organizations centered on Microsoft technologies, and GCP is widely recognized for AI, machine learning, data analytics, and Kubernetes. Selecting a provider should ultimately depend on workload requirements, existing technologies, staff expertise, governance needs, and organizational priorities.
