Setup and directory to local host by IP 
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
