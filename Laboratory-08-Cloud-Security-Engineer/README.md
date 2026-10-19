# Laboratory 08: The Cloud Security Engineer

## Mission Overview

This laboratory focuses on securing an Ubuntu server using a host-based firewall. Using the KillerCoda playground and Docker, an Nginx web application was deployed on port 8080, and UFW was configured to control incoming network traffic.

## Objectives

- Understand the Principle of Least Privilege and the concept of an attack surface.
- Apply a Default Deny policy to incoming network traffic.
- Allow SSH access for remote administration.
- Configure an explicit firewall rule for the web application on TCP port 8080.
- Verify firewall configuration and application availability.
- Document the security configuration and maintain a GitHub cloud computing portfolio.

## Commands Executed

### Docker Application Deployment

```bash
docker --version
docker ps
docker run -d --name secure-web-app -p 8080:80 nginx:alpine
docker ps
curl http://localhost:8080
curl -I http://localhost:8080
```

### Firewall Configuration

```bash
sudo ufw status verbose
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

### Skills Learned

- Basic Linux server administration using an Ubuntu environment.
- Deploying and verifying an Nginx container using Docker.
- Understanding network ports, services, and server attack surfaces.
- Configuring UFW firewall rules and default traffic policies.
- Applying least-privilege principles to network access.
- Documenting technical procedures using Markdown.
- Managing laboratory documentation and evidence through GitHub.

## Evidence

Screenshots documenting the application deployment and firewall configuration are stored in the `screenshots/` directory.

- `screenshots/vulnerable-app-running.png`
- `screenshots/firewall-activated.png`
- `screenshots/firewall-port-allowed.png`
