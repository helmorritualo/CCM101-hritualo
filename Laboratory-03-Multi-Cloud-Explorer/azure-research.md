# Microsoft Azure Research

## 1. Brief Overview

Microsoft Azure is Microsoft's public cloud platform for building, deploying, managing, and monitoring applications and infrastructure. Azure provides services for computing, storage, networking, identity, databases, analytics, security, and many other cloud workloads.

For this research, the four core Azure services selected are **Azure Virtual Machines** for compute, **Azure Blob Storage** for object storage, **Azure Virtual Network** for networking, and **Microsoft Entra ID** for identity and access management.

## 2. Global Infrastructure

Azure organizes its global infrastructure into **geographies and regions**. Microsoft describes an Azure geography as containing one or more regions and using high-capacity networking while helping organizations meet data residency and compliance requirements.

Azure's official region list provides the physical location, geography, paired-region information, and Availability Zone support for public-cloud regions. Availability Zones, where supported, provide additional separation for workloads that need higher availability.

This infrastructure allows organizations to select Azure locations based on requirements such as latency, data residency, compliance, availability, and disaster recovery.

## 3. Cloud Management Console

The **Azure portal** is a web-based, unified console for creating, managing, and monitoring Azure resources. It provides a graphical user interface for working with resources such as virtual machines, databases, and applications.

The portal also supports custom dashboards, resource organization, filtering, favorites, and access to Azure management capabilities. Administrators can manage subscriptions and monitor cloud resources from the same interface.

## 4. Four Core Services

### 4.1 Azure Virtual Machines — Compute

**Azure Virtual Machines (VMs)** provide virtualized compute resources for running workloads in Azure. Azure supports both Linux and Windows-based virtual machines and provides a broad range of VM configurations.

Azure documentation also describes migration and management scenarios for Windows Server, SQL Server, .NET applications, Microsoft Entra ID, and related Microsoft technologies.

**Typical role:** Running application servers, Windows Server workloads, Linux workloads, development systems, and workloads that require VM-level control.

### 4.2 Azure Blob Storage — Object Storage

**Azure Blob Storage** is Microsoft's object storage solution for the cloud. It is optimized for storing large amounts of unstructured data.

**Typical role:** Storing documents, images, videos, logs, backups, archives, distributed files, and data used for analysis.

### 4.3 Azure Virtual Network — Networking

**Azure Virtual Network (VNet)** provides private network infrastructure in Azure. It can be used to build isolated network environments for virtual machines and applications.

Azure Virtual Network also supports connections to on-premises environments and provides networking features such as IP addressing, DNS configuration, VPN, ExpressRoute, routing, filtering, and network peering.

**Typical role:** Connecting application components securely, designing private network topologies, and integrating cloud workloads with existing data centers.

### 4.4 Microsoft Entra ID — Identity and Access Management

**Microsoft Entra ID** is a cloud-based identity and access management service. It provides authentication, policy enforcement, and protection for users, devices, applications, and resources.

Entra ID also supports capabilities such as multifactor authentication, Conditional Access, role-based access control, user and group management, and application management.

**Typical role:** Managing workforce identities, controlling access to cloud applications, enforcing authentication policies, and supporting enterprise identity management.

## 5. Three Advantages

### 5.1 Strong Microsoft ecosystem integration

Azure is closely integrated with Microsoft technologies. Microsoft's Azure Virtual Machines documentation specifically describes migration and support scenarios for Windows Server, SQL Server, .NET applications, Microsoft Entra ID, and System Center.

### 5.2 Hybrid and enterprise networking capabilities

Azure Virtual Network can connect Azure resources with on-premises networks using technologies such as VPN and ExpressRoute. This supports hybrid architectures where organizations keep some systems in their own facilities while moving other workloads to the cloud.

### 5.3 Centralized web-based management

The Azure portal provides a unified graphical interface for creating, managing, monitoring, and organizing Azure resources. This reduces the need to manage every service through separate interfaces.

## 6. Typical Enterprise Use Cases

Azure can be used for enterprise workloads such as:

- Hosting Windows Server and Linux applications with Azure Virtual Machines.
- Migrating Microsoft-based workloads such as Windows Server, SQL Server, and .NET applications.
- Storing documents, media, backups, logs, and analytical datasets using Azure Blob Storage.
- Building private cloud networks and hybrid connections with Azure Virtual Network.
- Managing users, applications, authentication, and access policies using Microsoft Entra ID.
- Designing regional and availability-zone architectures for applications that require resilience and geographic distribution.
