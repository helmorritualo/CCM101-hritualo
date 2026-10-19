# Firewall Configuration

## Overview

This document records the firewall commands used to secure the Ubuntu server during Laboratory Activity 8. UFW was configured to deny incoming traffic by default, allow outgoing traffic, and permit only the explicitly authorized incoming services required by the lab.

## 1. Allow SSH

```bash
sudo ufw allow ssh
```

This rule allows incoming SSH connections so administrators can remotely manage the server.

## 2. Configure the Default Deny Policy

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming connections unless an applicable rule permits them. The second allows outgoing connections initiated by the server.

## 3. Enable the Firewall

```bash
sudo ufw enable
```

This activates UFW and applies the configured firewall rules.

## 4. Allow the Web Application on Port 8080

```bash
sudo ufw allow 8080/tcp
```

This rule allows incoming TCP traffic on port 8080, which is used by the Nginx web application in this laboratory.

## 5. Verify the Configuration

```bash
sudo ufw status verbose
sudo ufw status numbered
```

The verbose status command displays the firewall's active state and default policies. The numbered status command displays the configured rules and their rule numbers.

## Why SSH Must Be Allowed Before Enabling UFW

If UFW is enabled before SSH is explicitly allowed, incoming SSH connections may be blocked by the default deny policy, potentially locking remote administrators out of the server until they regain access through another method.

## Security Note

Because the application uses Docker with a published host port, Docker's networking rules may affect how UFW filters incoming traffic. A successful application request alone does not prove that the firewall is blocking every unauthorized external connection.

## Conclusion

The configuration applies the principle of least privilege by allowing the incoming services required by the lab while denying other incoming traffic by default. Firewall status checks help verify that the intended policy and rules are configured.
