# Mission 6 Reflection

Writing a `docker-compose.yml` file makes a cloud engineer’s job easier because the configuration for multiple containers can be defined in one place instead of requiring many manual commands. In this activity, the Nextcloud application and MariaDB database were described as services and deployed together using `docker-compose up -d`. This approach makes the deployment more organized, repeatable, and easier to manage.

An indentation error in a YAML file can prevent Docker Compose from correctly reading the configuration. YAML depends on proper spacing to represent relationships between settings, so using a Tab instead of spaces or placing a line at the wrong level can result in a syntax or configuration error. This shows why careful formatting is important when writing Infrastructure as Code.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` were used to provide the database connection and configuration information required by Nextcloud and MariaDB. The `MYSQL_HOST=database` variable also allowed the Nextcloud application to identify the database service by its Compose service name.

Deploying Nextcloud and its database in just a few minutes showed how Docker Compose can simplify the deployment of a multi-container application. Instead of setting up each component separately, the required services and settings were defined together and started as one stack. Accessing the Nextcloud interface through port 8080 also demonstrated how a containerized application can be made available to users.

Since Mission 1, my understanding of Cloud Computing has developed from learning basic cloud concepts into understanding how actual cloud infrastructure can be deployed and managed. This mission helped connect concepts such as containers, multi-tier architecture, networking, configuration, and Infrastructure as Code into one practical deployment workflow.
