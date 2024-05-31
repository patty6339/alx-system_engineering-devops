# This repo is for the web infrastructure task

Here are some of the concepts covered in the task

### What is a Database?
A **database** is an organized collection of structured information or data, typically stored electronically in a computer system. A database is managed by a database management system (DBMS). Together, the data and the DBMS, along with the applications associated with them, are referred to as a database system. Databases are used to store, manage, and retrieve information efficiently.

### Difference Between a Web Server and an App Server
- **Web Server**: 
  - **Primary Function**: Serves static content like HTML, CSS, JavaScript, and images to the web browser.
  - **Common Examples**: Apache HTTP Server, Nginx.
  - **Protocol**: Primarily HTTP/HTTPS.
  - **Usage**: Handles requests from clients (browsers) and delivers web pages.

- **App Server**:
  - **Primary Function**: Serves dynamic content and executes business logic. It can also serve static content, but it is designed to create dynamic content on the fly.
  - **Common Examples**: Apache Tomcat, JBoss, WebSphere.
  - **Protocol**: Supports multiple protocols including HTTP, but also more complex protocols such as RMI/IIOP.
  - **Usage**: Manages application operations between users and back-end business applications or databases.

### DNS Record Types
- **A (Address) Record**: Maps a domain to an IPv4 address.
- **AAAA (IPv6 Address) Record**: Maps a domain to an IPv6 address.
- **CNAME (Canonical Name) Record**: Alias of one name to another. The DNS lookup will continue by retrying the lookup with the new name.
- **MX (Mail Exchange) Record**: Specifies the mail server responsible for receiving email on behalf of a domain.
- **TXT (Text) Record**: Holds text information for various purposes. Often used for SPF, DKIM, and DMARC policies.
- **NS (Name Server) Record**: Specifies the authoritative DNS servers for a domain.
- **SRV (Service) Record**: Specifies a port for specific services.
- **PTR (Pointer) Record**: Used for reverse DNS lookups.

### Single Point of Failure
A **single point of failure (SPOF)** is a part of a system that, if it fails, will stop the entire system from working. SPOFs are undesirable in any system with a goal of high availability or reliability, such as a production environment or critical infrastructure.

### How to Avoid Downtime When Deploying New Code
- **Blue-Green Deployment**: Maintain two identical production environments (Blue and Green). Deploy new code to the Blue environment while Green serves the current production traffic, then switch.
- **Canary Release**: Gradually roll out the new code to a small subset of users before a full-scale deployment.
- **Rolling Update**: Gradually update instances of the application, ensuring some instances are always available.
- **Feature Toggles**: Deploy new code with features turned off, and enable them gradually or instantly once verified.
- **Automated Testing**: Extensive unit, integration, and end-to-end tests to catch issues before deployment.
- **Zero-Downtime Deployment Tools**: Use of CI/CD tools that support zero-downtime deployments, like Kubernetes, which allows rolling updates and rollbacks.

### High Availability Cluster (Active-Active / Active-Passive)
- **Active-Active Cluster**: All nodes are active and handle traffic simultaneously. If one node fails, the others continue to handle the load.
- **Active-Passive Cluster**: Only one node is active at a time. The passive node(s) remain on standby and take over if the active node fails.

### What is HTTPS
**HTTPS (HyperText Transfer Protocol Secure)** is the secure version of HTTP. It uses SSL/TLS to encrypt the data sent between the client and server, ensuring data integrity and privacy. HTTPS is essential for protecting sensitive data such as login credentials and payment information.

### What is a Firewall
A **firewall** is a network security device or software that monitors and controls incoming and outgoing network traffic based on predetermined security rules. Firewalls establish a barrier between trusted internal networks and untrusted external networks, such as the internet. There are different types of firewalls, including packet-filtering firewalls, stateful inspection firewalls, proxy firewalls, and next-generation firewalls (NGFW).

Feel free to ask if you need more details on any of these topics!