# load balancer 

Load balancing across multiple application instances is a commonly used technique for optimizing resource utilization, maximizing throughput, reducing latency, and ensuring fault‑tolerant configurations.


## Proxying HTTP Traffic to a Group of Servers

To start using NGINX Plus or NGINX Open Source to load balance HTTP traffic to a group of servers, first you need to define the group with the upstream directive. The directive is placed in the http context,Servers Are Deployed By AWS EC2

Servers in the group are configured using the server directive (not to be confused with the server block that defines a virtual server running on NGINX). For example, the following configuration defines a group named **allbackend** and consists of three server configurations (which may resolve in more than three actual servers):
![image](https://user-images.githubusercontent.com/46167070/117737957-350ec480-b1fb-11eb-9f9a-13380644ea0f.png)



Round Robin – Requests are distributed evenly across the servers, with server weights taken into consideration. This method is used by default (there is no directive for enabling it):




![image](https://user-images.githubusercontent.com/46167070/118540602-08096700-b751-11eb-9732-6046aab5b40b.png)

















Load Balancing IP Hash

IP Hash – The server to which a request is sent is determined from the client IP address. In this case, either the first three octets of the IPv4 address or the whole IPv6 address are used to calculate the hash value. The method guarantees that requests from the same address get to the same server unless it is not available.





![image](https://user-images.githubusercontent.com/46167070/117774619-0237f100-b23a-11eb-9299-a4cc04abe173.png)

