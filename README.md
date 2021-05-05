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
## web server 
https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04 
https://www.tecmint.com/install-nginx-on-ubuntu-20-04/


Nginx Configuration
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





