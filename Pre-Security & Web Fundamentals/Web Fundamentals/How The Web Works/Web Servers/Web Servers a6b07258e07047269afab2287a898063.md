# Web Servers

# Other Components

Here are some extra key components of web servers

### Load Balancers

Ensures high traffic websites can handle the high demand, and it provides a failover if a server becomes unresponsive. Performs a **health check**, meaning if a server doesn't respond appropriately or doesn't respond, the load balancer will stop sending traffic until it responds appropriately again

Request a website with a load balancer, the balancer will receive the request and forward it to one of multiple servers behind it using an algorithm like:

- Round Robin - sends it to each server in turn
- Weighted - checks how many request a server is currently dealing with and sends it to the least busy server.
    
    ![Untitled](Web%20Servers%20a6b07258e07047269afab2287a898063/Untitled.png)
    

### Content Delivery Networks (CDN)

Cuts down traffic to a busy website, allows you to host static files from your website (JavaScript, CSS, images, videos) and host them across thousands of servers all over the world (instead of just one server in one location). When a user request one of the hosted files, the CDN finds the nearest physical server and sends the request there instead of a random location in the world.

### Databases

Stores user information. Common databases are MySQL, Postgres, etc. Webservers communicate with databases to store and recall data.

### Web Application Firewall (WAF)

Sits between web request and web server, its purpose is to protect the webserver from DDoS attacks or hacking. WAF analyses the request for common attack techniques, if the browser is real (not a bot), and limits request being sent (for DDoS) meaning it only allows a certain amount of request from an IP per second. If it deems the request is an attack it will be dropped. 

# How Web Servers Work

### What is a Web Server?

A web server is software that listens for incoming connections and then utilizes HTTP protocol to deliver web content to its clients. Common web servers are: Apache, Nginx, IIS, and NodeJS. 

NOTE* Web server delivers files from its root directory (unless configured otherwise):

- Apache and Nginx the default location is /var/www/html in Linux
- ISS uses C:\inetpub\wwwroot in Windows

For example, if we requested “http://exaple.com/picture.jpg”, an Apache server would fetch “/var/www/html/picture.jpg” from its local drive

### Virtual Hosts

Are used to host multiple websites with different domain names. Web server checks the hostname being request from the HTTP header and matches it against its virtual host, if it finds a match the correct website will be provided, if no match then the default website will be provided instead

NOTE* Have their root directory mapped to different locations on the hard drive and there’s no limit to the number of different websites you can host on a web server.

For example: “one.com” is mapped to /var/www/website_one and “two.com” is mapped to /var/www/website_two

### Static Vs Dynamic Content

Static content - files directly served from the webserver with no changes made to them (JavaScript, CSS, HTML) associated with front-end programming

Dynamic content - Content changes depending on request, (User accounts, user customization, etc) associated with backend programming