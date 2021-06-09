# Nginx
NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers.

![image](https://user-images.githubusercontent.com/46167070/118860256-77ab5d80-b8db-11eb-9104-9a0c9f1ce84d.png)


### What are load balancers and how do they work?

A load balancer may be:

1-physical device, a virtualized instance running on specialized hardware or a software process. <br>

2-Incorporated into application delivery controllers (ADCs) designed to more broadly improve the performance and security of three-tier web and microservices-based applications, regardless of where they’re hosted. <br>

3-Able to leverage many possible load balancing algorithms, including round robin, server response time and the least connection method to distribute traffic in line with current requirements.


![image](https://user-images.githubusercontent.com/46167070/118860874-2c457f00-b8dc-11eb-8fa7-064c8b7b4d2f.png)




# NGINX as a Web Server

The goal behind NGINX was to create the fastest web server around, and maintaining that excellence is still a central goal of the project. NGINX consistently beats Apache and other servers in benchmarks measuring web server performance. Since the original release of NGINX, however, websites have expanded from simple HTML pages to dynamic, multifaceted content. NGINX has grown along with it and now supports all the components of the modern Web, including WebSocket, HTTP/2, gRPC, and streaming of multiple video formats (HDS, HLS, RTMP, and others).




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
    TLS/SSL


# Advnced Topics
https://www.youtube.com/watch?v=xZrOjmAkFC8

https://www.nginx.com/blog/smart-efficient-byte-range-caching-nginx/
https://www.nginx.com/blog/dynamic-bandwidth-limits-nginx-plus-key-value-store/

chapter 5 
Massively Scalable Content Caching
chapter 6 
Sophisticated Media Streaming
nginx Authentication senstive pages
https://www.javatpoint.com/nginx-content-caching

How to check Zipping https://stackoverflow.com/questions/9140178/how-can-i-tell-if-my-server-is-serving-gzipped-content
https://www.linode.com/docs/guides/how-to-configure-nginx/
