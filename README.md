# Nginx
NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers.







# How Does Nginx Work?

Nginx is built to offer low memory usage and high concurrency. Rather than creating new processes for each web request, Nginx uses an asynchronous, event-driven approach where requests are handled in a single thread.

With Nginx, one master process can control multiple worker processes. The master maintains the worker processes, while the workers do the actual processing. Because Nginx is asynchronous, each request can be executed by the worker concurrently without blocking other requests.

Some common features seen in Nginx include:

    Reverse proxy with caching
    IPv6
    Load balancing
    FastCGI support with caching
    WebSockets
    Handling of static files, index files, and auto-indexing
    TLS/SSL with SNI



# layer 4 , 7




https://ubuntu.com/tutorials/install-and-configure-nginx#2-installing-nginx  Good one



# Resources
https://phoenixnap.com/kb/nginx-reverse-proxy


https://www.netguru.com/codestories/nginx-tutorial-basics-concepts




## Install Nginx
https://ubuntu.com/tutorials/install-and-configure-nginx#2-installing-nginx

sudo apt update
sudo apt install nginx
After installing it, you already have everything you need.
      ip addr

You can point your browser to your server IP address. You should see this page:









## web server 
https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04 
https://www.tecmint.com/install-nginx-on-ubuntu-20-04/


Nginx Configuration

     cd /etc/nginx


serve static content
 Proxy pass 
location / {
    try_files $uri $uri/ @backend;
}

location @backend {
    proxy_pass http://backend.example.com;
}


https://docs.nginx.com/nginx/admin-guide/web-server/serving-static-content/

## Layer 7 Proxy 
Check docker 
https://www.nginx.com/resources/glossary/layer-7-load-balancing/



Proxy to 4 Backend NoseJs



 
Split load to multiple Backends 
Block certain Request
## Nginx Layer 4 
## Enable HTTPS on Nginx Lets Encrypt
## TLS 
## HTTP/2



## Setup 

sudo apt update
sudo apt install nginx


![image](https://user-images.githubusercontent.com/46167070/117722546-7befc080-b1e1-11eb-8968-7781108c0f28.png)

Before testing Nginx, the firewall software needs to be adjusted to allow access to the service. Nginx registers itself as a service with ufw upon installation, making it straightforward to allow Nginx access.

List the application configurations that ufw knows how to work with by typing:


![image](https://user-images.githubusercontent.com/46167070/117723121-47c8cf80-b1e2-11eb-81de-94a5a61a645e.png)


As you can see, there are three profiles available for Nginx:

    Nginx Full: This profile opens both port 80 (normal, unencrypted web traffic) and port 443 (TLS/SSL encrypted traffic)
    Nginx HTTP: This profile opens only port 80 (normal, unencrypted web traffic)
    Nginx HTTPS: This profile opens only port 443 (TLS/SSL encrypted traffic)

It is recommended that you enable the most restrictive profile that will still allow the traffic you’ve configured. Since we haven’t configured SSL for our server yet in this guide, we will only need to allow traffic on port 80.

You can enable this by typing:


![image](https://user-images.githubusercontent.com/46167070/117724668-5fa15300-b1e4-11eb-95f2-64eb221b723d.png)



Checking your Web Server


sudo systemctl status nginx

# change ports 
from configration files

![image](https://user-images.githubusercontent.com/46167070/117734174-34723000-b1f3-11eb-832c-ab5d0526bf2a.png)



![image](https://user-images.githubusercontent.com/46167070/117734407-af3b4b00-b1f3-11eb-85bb-df66b290ddfe.png)




![image](https://user-images.githubusercontent.com/46167070/117737574-6c30a600-b1fa-11eb-9a7f-6359924db424.png)


![image](https://user-images.githubusercontent.com/46167070/117737701-b1ed6e80-b1fa-11eb-9134-13626cfd301e.png)


![image](https://user-images.githubusercontent.com/46167070/117737735-c7fb2f00-b1fa-11eb-9ce3-e878ad5a4c00.png)


![image](https://user-images.githubusercontent.com/46167070/117737872-0f81bb00-b1fb-11eb-8f68-cca21df04cd2.png)





![image](https://user-images.githubusercontent.com/46167070/117737907-22948b00-b1fb-11eb-933a-6d19bd683ea9.png)



![image](https://user-images.githubusercontent.com/46167070/117737957-350ec480-b1fb-11eb-9f9a-13380644ea0f.png)








![image](https://user-images.githubusercontent.com/46167070/117738014-58d20a80-b1fb-11eb-8837-c72e763d4fac.png)




Load Balancing IP Hash





![image](https://user-images.githubusercontent.com/46167070/117774619-0237f100-b23a-11eb-9299-a4cc04abe173.png)

![image](https://user-images.githubusercontent.com/46167070/117774839-2d224500-b23a-11eb-9c35-0f02b40eec21.png)













