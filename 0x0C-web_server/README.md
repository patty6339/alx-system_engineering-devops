This is the repo for web-server project

### How the Web Works

The web operates on the client-server model. Clients (usually web browsers) send HTTP requests to servers, which respond with the requested resources, such as HTML pages, images, or other data. The process involves DNS resolution to translate domain names into IP addresses, establishing a TCP/IP connection, and using protocols like HTTP or HTTPS to communicate.

### Nginx

Nginx (pronounced "engine-x") is a high-performance web server, reverse proxy, and load balancer. It's known for its scalability and ability to handle a large number of concurrent connections efficiently. Nginx can serve static content quickly and manage dynamic content by acting as a reverse proxy for applications running on other servers.

### How to Configure Nginx

Configuring Nginx involves editing its configuration files, primarily `nginx.conf`. Key directives include:

- `server`: Defines a server block to handle requests.
- `location`: Specifies how to process specific request URIs.
- `listen`: Sets the port and address for Nginx to listen on.
- `root`: Defines the root directory for serving files.
- `proxy_pass`: For reverse proxy configurations.

After editing the configuration, restart Nginx to apply changes.

### Child Process Concept

In computing, a child process is a process created by another process (the parent). The child process inherits most of its attributes from the parent and can execute concurrently. This concept is crucial for multitasking and efficient resource management.

### Root and Subdomain

- **Root Domain**: The primary domain name (e.g., example.com).
- **Subdomain**: A domain that is part of a larger domain (e.g., blog.example.com). Subdomains are used to organize and navigate different sections of a website.

### HTTP Requests

HTTP requests are messages sent by the client to request resources from a server. An HTTP request consists of:

- Request line (method, URI, HTTP version)
- Headers (metadata)
- Body (optional, for methods like POST)

### HTTP Redirection

HTTP redirection occurs when a server responds to a request with a status code indicating the client should make a new request to a different URL. Common status codes for redirection include:

- 301 (Moved Permanently)
- 302 (Found)
- 307 (Temporary Redirect)

### Not Found HTTP Response Code

The 404 Not Found HTTP response code indicates that the server cannot find the requested resource. This often occurs when a user tries to access a URL that doesn't exist on the server.

### Log Files on Linux

Linux systems use log files to record system, service, and application activities. Key log files include:

- `/var/log/syslog` or `/var/log/messages`: General system logs.
- `/var/log/auth.log` or `/var/log/secure`: Authentication logs.
- `/var/log/nginx/access.log` and `/var/log/nginx/error.log`: Nginx access and error logs.

Logs are essential for monitoring system health, troubleshooting issues, and ensuring security.

### DNS

DNS stands for **Domain Name System**. It is a hierarchical and decentralized naming system used to translate human-friendly domain names (like www.example.com) into IP addresses (like 192.0.2.1), which computers use to identify each other on the network.

### What DNS Stands For

**Domain Name System**

### What is DNS's Main Role

The main role of DNS is to resolve domain names into IP addresses, enabling users to access websites using easy-to-remember names instead of numerical IP addresses. DNS ensures that users can access resources by typing domain names into their web browsers, while the system handles the translation behind the scenes.

### DNS Record Types

#### A Record

**Address Record (A)** maps a domain name to an IPv4 address. It's used to find the IP address of a hostname.

Example:
```plaintext
example.com.   IN   A   192.0.2.1
```

#### CNAME Record

**Canonical Name Record (CNAME)** maps a domain name to another domain name, effectively creating an alias.

Example:
```plaintext
www.example.com.   IN   CNAME   example.com.
```

#### TXT Record

**Text Record (TXT)** allows domain administrators to store text information in the DNS. It's often used for domain verification and email security (e.g., SPF, DKIM).

Example:
```plaintext
example.com.   IN   TXT   "v=spf1 include:_spf.google.com ~all"
```

#### MX Record

**Mail Exchange Record (MX)** specifies the mail servers responsible for receiving email on behalf of a domain. It includes a priority value, with lower numbers indicating higher priority.

Example:
```plaintext
example.com.   IN   MX   10   mail.example.com.
```
