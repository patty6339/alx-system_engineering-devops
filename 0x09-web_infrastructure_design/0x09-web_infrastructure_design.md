
# Explanation

* Three firewalls: The firewalls are used to secure the network infrastructure by controlling incoming and outgoing traffic. They are also responsible for blocking any malicious traffic.

* SSL certificate: An SSL certificate is used to encrypt the traffic between the client's browser and the web server, making it difficult for attackers to intercept and read sensitive information.

* Monitoring clients: Three monitoring clients are added to collect data and send it to Sumologic or other monitoring services to track the performance, availability, and health of the web infrastructure.

* Load Balancer: A load balancer is used to distribute incoming requests evenly among the web servers. It also performs SSL termination, decrypting the traffic before it reaches the web servers.

* MySQL servers: Two MySQL servers are used, with one acting as the master and the other two slaves. This setup provides redundancy and ensures high availability of the database.

* Different server components: Each server has different components, such as the web server, application server, and database, to prevent a single point of failure.

## Why Firewalls are important

 Firewalls are important to secure the network infrastructure from unauthorized access and prevent malicious traffic from entering the network.

## Why HTTPS is important

 HTTPS is important to encrypt the traffic between the client's browser and the web server, making it difficult for attackers to intercept and read sensitive information.

## Why Monitoring is important

Monitoring is important to track the performance, availability, and health of the web infrastructure. It helps to identify and resolve issues before they affect the users.

## How Monitoring works

The monitoring tool collects data from the web servers, load balancer, and database servers, and sends it to Sumologic or other monitoring services for analysis. It helps to track the number of requests, response time, and error rate.

* How to monitor web server QPS: To monitor web server QPS, you can set up a monitoring tool to track the number of requests per second to each web server. This data can help to identify if any server is overloaded and needs to be scaled up.

# Issues with this infrastructure:

* Terminating SSL at the load balancer level: Terminating SSL at the load balancer level can be an issue because it increases the load on the load balancer and reduces the security of the web infrastructure.

* Having only one MySQL server capable of accepting writes: Having only one MySQL server capable of accepting writes can be an issue because it can create a single point of failure and affect the availability of the web infrastructure.

* Having servers with all the same components: Having servers with all the same components can be a problem because it can create a single point of failure, and any issue with one component can affect the entire web infrastructure. It is recommended to use different components on each server to avoid this issue.

The link to the screenshot of the architecture can be found here https://imgur.com/yprM9ps
