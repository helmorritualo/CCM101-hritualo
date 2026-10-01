# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

This laboratory activity introduced multi-tier application deployment using Docker Compose. A private cloud storage proof of concept was created using Nextcloud as the web/application tier and MariaDB as the database tier.

The two services were defined in a `docker-compose.yml` file and deployed together as a single application stack. The Nextcloud web interface was then accessed through port `8080` in the KillerCoda environment.

## Objectives

- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use a Linux command-line text editor to create a configuration file.
- Deploy a multi-container application using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- Continue developing a professional Cloud Computing portfolio.

## Commands Executed

### Create the project directory

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
```

### Create the Docker Compose file

```bash
nano docker-compose.yml
```

### Deploy the application stack

```bash
docker-compose up -d
```

### Verify the running services

```bash
docker-compose ps
```

### Inspect the application logs when necessary

```bash
docker-compose logs
```

### Shut down the application stack

```bash
docker-compose down
```

### Git commands used for documentation and evidence

```bash
git add .
git commit -m "docs(lab06): complete technical documentation"
git push
```

## Skills Learned

### Multi-Tier Architecture

Learned how a web/application tier and database tier can work together as separate components of an application.

### Docker Compose

Learned how a `docker-compose.yml` file can define multiple related services and their configuration in one deployment blueprint.

### YAML Configuration

Practiced creating a YAML configuration file and learned that correct spacing and indentation are important because YAML is space-sensitive.

### Container Networking

Learned how the Nextcloud application can identify the MariaDB service through the Compose service name specified by `MYSQL_HOST`.

### Infrastructure as Code

Learned how infrastructure configuration can be represented as code instead of relying entirely on manually typed deployment commands.

### Deployment and Verification

Practiced deploying a multi-container application, verifying the containers, accessing the application through a browser, and gracefully removing the deployed stack.

## Evidence

The deployment and access process is documented through the screenshots stored in the `screenshots/` directory.

```text
screenshots/
├── compose-deployment.png
├── nextcloud-web.png
└── compose-teardown.png
```
