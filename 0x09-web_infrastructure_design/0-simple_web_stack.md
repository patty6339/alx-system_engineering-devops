 # Explanation of the Concepts  

* Server : A server is a computer system that provides services or resources to other computers or devices on a network. In this case, we have one server that will host our website.

* Domain name : The domain name is a unique name that identifies a website on the internet. It is used to translate human-readable domain names into machine-readable IP addresses. In this case, the domain name is foobar.com, and we have configured a DNS record with a www subdomain that points to the server's IP address 8.8.8.8.

* DNS record: The www in www.foobar.com is a subdomain that is used to specify a particular service or resource on a domain. In this case, it indicates the web server that will handle HTTP requests for the website.

* Web server: The web server's role is to handle incoming HTTP requests from users' web browsers and serve the appropriate HTML, CSS, and JavaScript files that make up the website. We will use Nginx as our web server in this infrastructure.

* Application server: The application server's role is to run the code that powers the website, including any business logic or data processing. We will use an application server like Gunicorn or uWSGI to serve our Python application.

* Application files: The application files are the code base that powers the website. They will be stored on the server and executed by the application server.

* Database: The database's role is to store and manage the website's data, such as user accounts, blog posts, or product information. We will use MySQL as our database management system.

* Communication: The server will use the HTTP protocol to communicate with the user's computer, sending and receiving data over the internet.

# Issues:

* SPOF: The infrastructure we have designed has a single point of failure, which is the server. If the server goes down, the website will be inaccessible.

* Downtime during maintenance: When deploying new code or performing maintenance on the web server, the website will need to be taken down, resulting in downtime for users.

* Scalability: This infrastructure is not easily scalable, and it may become overwhelmed by incoming traffic during periods of high demand.


Link to the diagram's screenshot https://imgur.com/a/hEl6Zvp