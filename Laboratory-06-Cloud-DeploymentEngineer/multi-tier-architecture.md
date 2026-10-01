# Multi-Tier Architecture

## What is Two-Tier Architecture?

A two-tier architecture is an application design that separates a system into two main layers: the **Web/Application Tier** and the **Database Tier**. In this laboratory activity, Nextcloud serves as the web/application tier, while MariaDB serves as the database tier. The two containers work together, with Nextcloud handling user requests and MariaDB storing the application's persistent data.

## The Web/Application Tier

The Web/Application Tier is responsible for providing the application's interface and handling requests from users. It receives HTTP requests through the web server, processes application logic, and communicates with the database when information needs to be stored or retrieved.

In this activity, the **Nextcloud container** acts as the Web/Application Tier. It provides the private cloud storage web application that users access through a browser.

## The Database Tier

The Database Tier is responsible for storing and managing the application's persistent data. This includes information such as user accounts, configuration data, and file-related metadata required by the application.

In this activity, the **MariaDB container** acts as the Database Tier. Nextcloud communicates with MariaDB to store and retrieve the information it needs to operate.

## Why Separate Them?

Separating the web/application server and database into different containers makes the system easier to manage, maintain, and scale. Each container has a specific responsibility, so changes or updates to one tier can be performed without placing both parts of the application inside the same container.

This separation also follows a multi-tier architecture, where different components communicate through defined connections instead of being tightly combined. In this laboratory, Docker Compose is used to define and deploy both containers as one application stack.
