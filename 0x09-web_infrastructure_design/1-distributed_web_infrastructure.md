
# Explanation for a three-server web infrastructure

For a design a three-server web infrastructure that hosts the website www.foobar.com. Here's what I came up with:

* Server 1: Web Server (Nginx)
The first server will be a web server running Nginx, which will handle incoming requests from users and serve static content such as HTML, CSS, and JavaScript files. Nginx is a popular and efficient web server that is known for its ability to handle high traffic loads.

* Server 2: Application Server
The second server will be an application server that runs the website's codebase. This server will be responsible for generating dynamic content and interacting with the database.

* Server 3: Database (MySQL)
The third server will be a MySQL database server that stores all the website's data. This database will be used by the application server to read and write data.

* Load Balancer (HAproxy)
To distribute the incoming traffic evenly across the two servers, we will use a load balancer called HAproxy. HAproxy is a fast and reliable open-source load balancer that can handle high traffic loads. The load balancer will be configured with a round-robin distribution algorithm to distribute traffic evenly across the two servers.

## Load Balancer Setup:
HAproxy will be configured to enable an Active-Active setup. In this setup, both servers will be active and will receive traffic from the load balancer. If one server fails, the other server will continue to handle traffic.

## Database Primary-Replica (Master-Slave) Cluster:
To ensure that the database is highly available and can handle a high volume of traffic, we will set up a primary-replica (master-slave) cluster. In this setup, the primary database server will handle all write requests, and the replica database server will replicate the primary server's data and handle all read requests.

## Difference between Primary and Replica nodes in regard to the application:
The primary node is responsible for handling all write requests, while the replica node is responsible for handling all read requests. This setup allows the application to scale horizontally and handle a high volume of traffic.

# Issues with this infrastructure:

* Single Point of Failure (SPOF): Since we only have one instance of each server, there is a single point of failure. If any server fails, the website will be unavailable until the server is restored.
* Security Issues: There is no firewall or HTTPS configured in this infrastructure, which can leave the website vulnerable to attacks.
* No Monitoring: Without proper monitoring in place, it will be difficult to identify and troubleshoot any issues that may arise with the infrastructure

The link to the screenshot of the infrastructure is here https://imgur.com/a/JHBgXow
