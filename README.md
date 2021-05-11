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


Certificate

![image](https://user-images.githubusercontent.com/46167070/117781932-71651380-b241-11eb-8ecf-69a4a28fdc74.png)






![image](https://user-images.githubusercontent.com/46167070/117784053-6d39f580-b243-11eb-9667-8ecadbeb67a5.png)






