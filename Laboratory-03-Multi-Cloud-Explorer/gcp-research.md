# Google Cloud Platform (GCP) Research

## 1. Brief Overview

Google Cloud is Google's public cloud platform for computing, storage, networking, data analytics, artificial intelligence, security, and application development. It provides infrastructure and managed services that organizations can use to build and operate applications and large-scale workloads.

For this research, the four core Google Cloud services selected are **Compute Engine** for compute, **Cloud Storage** for object storage, **Virtual Private Cloud (VPC)** for networking, and **Cloud Identity and Access Management (IAM)** for identity and access control.

## 2. Global Infrastructure

Google Cloud organizes its infrastructure into **regions and zones**. Google Cloud's current global locations documentation states that regions and zones are distributed across the world to support performance, availability, and data-residency requirements.

As of the official Google Cloud locations page updated **August 31, 2026**, Google Cloud lists **43 regions and 130 zones**, with its global network connecting more than 200 countries and territories. Google Cloud also states that regions consist of three or more zones, subject to exceptions described in the documentation.

Google Cloud provides regional, multi-region, and global resources so organizations can design systems according to latency, availability, and data-location requirements.

## 3. Cloud Management Console

The **Google Cloud console** is a web-based graphical interface for managing Google Cloud projects and resources. Google Cloud documentation identifies it as one of the main ways to interact with cloud resources.

The Google Cloud environment can also be managed through the Google Cloud CLI and APIs. In addition, Cloud Shell provides a browser-based shell that can be accessed from the Google Cloud console.

## 4. Four Core Services

### 4.1 Compute Engine — Compute

**Compute Engine** is an Infrastructure as a Service (IaaS) offering that provides self-managed virtual machines and bare metal instances on Google infrastructure. It supports Linux and Windows workloads and provides different machine configurations.

Google Cloud documents Compute Engine use cases ranging from web and application servers to databases, ecommerce applications, high-performance computing, and AI/ML workloads using specialized hardware.

**Typical role:** Running virtual machines for applications, databases, web servers, enterprise workloads, and compute-intensive workloads.

### 4.2 Cloud Storage — Object Storage

**Cloud Storage** is a scalable managed storage service that stores data as objects in buckets. It can be used for storing and retrieving data across applications and services.

Google Cloud documents use cases including backups, archives, disaster recovery, media storage, application data, and data used for analytics and machine learning.

**Typical role:** Storing files, backups, datasets, media, archives, and other object-based data.

### 4.3 Virtual Private Cloud (VPC) — Networking

**Google Cloud VPC** provides networking functionality for Compute Engine VMs, Google Kubernetes Engine clusters, serverless workloads, and other Google Cloud services.

A Google Cloud VPC network is a global resource containing regional subnets connected through Google's network. VPC networks are logically isolated from one another.

**Typical role:** Designing private cloud network architectures and controlling connectivity among workloads and services.

### 4.4 Cloud IAM — Identity and Access Management

**Google Cloud Identity and Access Management (IAM)** provides fine-grained authorization for Google Cloud resources. It controls who can perform which actions on which resources.

Google Cloud IAM uses concepts such as principals, roles, permissions, and resources to define access. This allows organizations to apply detailed access-control policies.

**Typical role:** Managing permissions for users, groups, service identities, applications, and cloud resources.

## 5. Three Advantages

### 5.1 Strong global network and geographic coverage

Google Cloud operates a large global infrastructure with regions, zones, network edge locations, and a global network spanning many countries and territories. This supports architectures that need global distribution and low-latency access.

### 5.2 Strong support for data, AI, and high-performance workloads

Google Cloud provides infrastructure designed for workloads such as analytics, AI/ML, high-performance computing, and large-scale data processing. Compute Engine supports specialized machine configurations and accelerators for demanding workloads.

### 5.3 Flexible and fine-grained resource management

Google Cloud provides several ways to manage resources, including the Google Cloud console, CLI, and APIs. Its IAM system also provides fine-grained authorization so organizations can define what principals can do with specific resources.

## 6. Typical Enterprise Use Cases

Google Cloud can be used for enterprise workloads such as:

- Hosting websites, APIs, ecommerce systems, and business applications with Compute Engine.
- Running databases, analytics, and other compute-intensive workloads on flexible VM configurations.
- Storing backups, archives, media, datasets, and application objects in Cloud Storage.
- Building globally distributed private networks with Google Cloud VPC.
- Managing resource permissions with Cloud IAM.
- Supporting AI/ML, data analytics, and high-performance computing workloads.
- Deploying workloads across regions and zones to improve geographic availability and reduce latency.
