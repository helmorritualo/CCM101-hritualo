# Security Audit Report

### 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving users and applications only the permissions they need to perform their assigned tasks. In cloud environments, this helps prevent unauthorized access and limits the damage that could occur if an account is compromised.

### 2. Attack Surface

An attack surface is the collection of points through which an attacker could attempt to access or compromise a virtual machine. These may include open network ports, running services, exposed applications, and accounts with weak security. Reducing unnecessary services and access points makes the server more difficult to attack.

### 3. Default Deny Policy

A Default Deny policy blocks incoming network traffic unless a specific rule allows it. This is safer than trying to block individual attackers because unknown or unwanted connections are denied automatically, while only approved services can receive traffic. For example, a server can allow SSH for administration and port 8080 for its web application while blocking other incoming connections.
