# Checkpoint 4 – Cloud Platform Recommendation Challenge

## Client A – Startup Company

**Recommended cloud platform:** Amazon Web Services (AWS)

A startup with a limited budget should use AWS because AWS documents pay-as-you-go cloud infrastructure, which lets the company pay for compute and storage as it uses them instead of buying servers in advance. Amazon EC2 can host the mobile application backend with a small number of instances at launch, and Amazon EC2 Auto Scaling can add or remove instances automatically when traffic grows. Amazon S3 can store application files, images, and backups without the team having to manage physical storage. Because AWS officially describes itself as having the broadest cloud service catalog, the startup can add databases, identity, and delivery services later on the same platform as the product grows.

**Services the client could use:**
- Amazon Elastic Compute Cloud (Amazon EC2)
- Amazon Simple Storage Service (Amazon S3)
- Amazon EC2 Auto Scaling

## Client B – University

**Recommended cloud platform:** Microsoft Azure

The university already uses Windows Server, Microsoft 365, and Active Directory, and Azure is the cloud platform built to extend that Microsoft environment. Azure Virtual Machines can host Windows Server workloads in the cloud, so the university can migrate selected servers without changing the operating system it already manages. Microsoft Entra ID is the identity service for Microsoft 365, and Microsoft Entra Connect can synchronize the university’s on-premises Active Directory accounts so users keep the same credentials. Azure Virtual Network can connect those cloud resources to the existing campus network, which supports a partial migration instead of a full cutover.

**Services the client could use:**
- Azure Virtual Machines
- Microsoft Entra ID
- Azure Virtual Network (VNet)

## Client C – AI Research Company

**Recommended cloud platform:** Google Cloud Platform (GCP)

This company needs high-performance computing for artificial intelligence and machine learning, which is a documented strength of Google Cloud. Vertex AI provides a managed platform for training, hosting, and generating predictions from machine learning models, including popular frameworks such as TensorFlow and PyTorch. Cloud TPU provides specialized accelerators for training and running models faster than general-purpose servers. Compute Engine can also host high-performance virtual machines and GPU-based workloads when the research team needs custom environments around those AI services.

**Services the client could use:**
- Vertex AI
- Cloud TPU
- Compute Engine

## Client D – Global E-Commerce Company

**Recommended cloud platform:** Amazon Web Services (AWS)

A multinational online store needs infrastructure that is available in many locations and can scale automatically, and AWS documents the most extensive global cloud infrastructure among the three providers, with many Regions and Availability Zones. Amazon EC2 can run the shopping application, while Amazon EC2 Auto Scaling keeps the correct number of instances available and can launch replacements in other Availability Zones if one zone becomes unhealthy. Amazon CloudFront can deliver product pages, images, and APIs from edge locations around the world so customers experience lower latency. This combination matches the client’s need for high availability and automatic scaling across a worldwide customer base.

**Services the client could use:**
- Amazon Elastic Compute Cloud (Amazon EC2)
- Amazon EC2 Auto Scaling
- Amazon CloudFront

# Checkpoint 6 – Multi-Cloud Decision Matrix

| Business Requirement | Recommended Platform | Justification |
| --- | --- | --- |
| Startup Company | Amazon Web Services (AWS) | AWS documents pay-as-you-go pricing and Amazon EC2 Auto Scaling, so a small team can start with limited resources and grow capacity as demand increases. |
| Enterprise Organization | Amazon Web Services (AWS) | AWS officially serves enterprises and governments with the broadest cloud service catalog and a large global infrastructure for governed, multi-workload environments. |
| Microsoft Environment | Microsoft Azure | Azure Virtual Machines, Microsoft Entra ID, and Microsoft 365 directory synchronization are designed to extend Windows Server and Active Directory environments into the cloud. |
| AI / Machine Learning | Google Cloud Platform (GCP) | Google Cloud provides Vertex AI for training and deploying models and Cloud TPU accelerators for high-performance machine learning workloads. |
| Kubernetes Deployment | Google Cloud Platform (GCP) | Kubernetes was developed by Google, and Google Kubernetes Engine is Google Cloud’s managed Kubernetes service with automated cluster operations. |
| Global Web Application | Amazon Web Services (AWS) | AWS documents the most extensive global infrastructure, and Amazon CloudFront with Amazon EC2 Auto Scaling supports low-latency delivery and automatic scaling worldwide. |
