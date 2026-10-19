# Mission Reflection: The Cloud Security Engineer

Completing Laboratory Activity 8 helped me understand why server security is important, especially when hosting applications in a cloud environment. I learned that deploying an application is not enough; the server must also be configured to control who can access its services.

A host-based firewall protects a server by filtering network traffic directly on the machine. Even if an organization's external network security is breached, the firewall can provide another layer of protection by allowing authorized connections and blocking unauthorized incoming traffic. This demonstrates the principle of defense in depth, where multiple security measures help reduce the risk of compromise.

Managing open network ports is also important because every unnecessary service can create another potential entry point for attackers. By allowing only the ports required by the application and server administrators, an organization can reduce its attack surface. In this activity, SSH was allowed for remote administration, while TCP port 8080 was allowed for the Nginx web application.

Leaving a database port such as 3306 for MySQL open to the public internet is dangerous because attackers could repeatedly attempt to exploit vulnerabilities, guess credentials, or gain unauthorized access to sensitive information. Database access should instead be restricted to trusted application servers or authorized administrators, with authentication and other security controls in place.

This mission changed how I view server deployment and security. I now better understand why default firewall policies, carefully selected access rules, and regular verification are important. I also learned that a successful application request does not automatically prove that every firewall rule is working as intended, especially when Docker manages its own network rules.

Finally, having eight laboratory missions organized in my GitHub cloud computing portfolio gives me a structured record of my learning and technical activities. The portfolio can help demonstrate my developing skills in cloud computing, deployment, operations, and security. Maintaining clear documentation and screenshots also makes it easier to review my work, identify areas for improvement, and prepare for more advanced cloud computing tasks.
