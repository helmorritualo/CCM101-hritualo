# AWS Research

## 1. Brief Overview

Amazon Web Services (AWS) is a public cloud platform that provides a large collection of cloud services for computing, storage, networking, databases, security, analytics, and application development. AWS allows organizations to provision infrastructure and managed services without owning and maintaining the underlying physical data center infrastructure.

For this research, the four core AWS services selected are **Amazon EC2** for compute, **Amazon S3** for object storage, **Amazon VPC** for networking, and **AWS Identity and Access Management (IAM)** for identity and access control.

## 2. Global Infrastructure

AWS organizes its infrastructure into **Regions** and **Availability Zones (AZs)**. An AWS Region is a separate geographic area, while Availability Zones are isolated locations within a Region. AWS documentation explains that Availability Zones within a Region are connected using low-latency, high-bandwidth, redundant networking, and AWS recommends distributing applications across multiple Availability Zones when high availability is required.

AWS also provides **Local Zones** for placing selected resources closer to end users and **Wavelength Zones** for workloads that need very low latency to 5G devices and networks. The AWS Regions documentation provides the current list of available Regions and their geographic locations.

This regional structure allows organizations to choose deployment locations according to latency, availability, regulatory, and operational requirements.

## 3. Cloud Management Console

The **AWS Management Console** is a web-based interface that provides centralized access to AWS service consoles. From the console, users can search for services, manage resources, access notifications and account information, configure console settings, and use AWS CloudShell.

AWS Console Home also supports customizable widgets and application-management views for areas such as service health, cost and usage, security posture, and performance.

## 4. Four Core Services

### 4.1 Amazon EC2 — Compute

**Amazon Elastic Compute Cloud (Amazon EC2)** provides resizable compute capacity as virtual servers. It supports different instance types and configurations for workloads such as web applications, enterprise applications, high-performance computing, machine learning, and Windows workloads.

**Typical role:** Running application servers, APIs, backend systems, development environments, and other workloads that need virtual machines.

### 4.2 Amazon S3 — Object Storage

**Amazon Simple Storage Service (Amazon S3)** is an object storage service designed to provide scalable storage, data availability, security, and performance. S3 stores data as objects inside buckets.

**Typical role:** Storing application files, images, videos, backups, archives, logs, datasets, and other unstructured data.

### 4.3 Amazon VPC — Networking

**Amazon Virtual Private Cloud (Amazon VPC)** lets organizations create a logically isolated virtual network in AWS. Administrators can define IP address ranges, subnets, route tables, gateways, and other network controls.

**Typical role:** Building private cloud networks for EC2 instances, databases, application tiers, and other AWS resources.

### 4.4 AWS IAM — Identity and Access Management

**AWS Identity and Access Management (IAM)** controls authentication and authorization for AWS resources. Administrators use IAM permissions and policies to specify who can access resources and what actions they can perform.

**Typical role:** Managing users, roles, permissions, and least-privilege access to AWS resources.

## 5. Three Advantages

### 5.1 Flexible and distributed infrastructure

AWS provides a multi-Region and multi-Availability-Zone infrastructure model. This gives organizations flexibility in selecting deployment locations and designing workloads for resilience and geographic distribution.

### 5.2 Broad range of infrastructure services

AWS provides services covering computing, storage, networking, identity, databases, analytics, application development, and other cloud requirements. This allows an organization to combine multiple managed services into one cloud architecture.

### 5.3 Strong control over networking and access

Services such as Amazon VPC and IAM provide detailed control over network boundaries and resource permissions. This helps organizations separate workloads and apply access policies based on their security requirements.

## 6. Typical Enterprise Use Cases

AWS can be used for many enterprise workloads, including:

- Hosting web applications, APIs, and backend systems on Amazon EC2.
- Storing backups, archives, application files, and large datasets in Amazon S3.
- Building isolated enterprise network environments with Amazon VPC.
- Managing identity and least-privilege access with AWS IAM.
- Supporting high-availability systems by distributing workloads across multiple Availability Zones.
- Supporting machine learning, high-performance computing, and other specialized workloads through scalable compute resources.
