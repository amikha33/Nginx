Occasionally, there may be a need to adjust a server timeout value for the CA Secure Proxy Server (now CA Access Gateway), in order to allow a backend request to complete if there is a requirement for a longer connection time, i.e. 2 minutes.  The default timeout value for the timeout value is 60000 ms (60 seconds) as default. 


# Nginx Backend Timeout 

1- Proxy_coneect_timeout  <br>
2-Proxy_send_timeout <br>
3-Proxy_read_timeout <br>
4-proxy_next_upstream_timeout


## 1- Proxy_coneect_timeout 

    Syntax:proxy_read_timeout time;
    Default:proxy_read_timeout 60s;
    Context:http, server, location 

Defines a timeout for reading a response from the proxied server. The timeout is set only between two successive read operations, not for the transmission of the whole response. If the proxied server does not transmit anything within this time, the connection is closed. 


## 2-Proxy_send_timeout

    proxy_send_timeout time;
    Default:proxy_send_timeout 60s;
    Context:http, server, location

Sets a timeout for transmitting a request to the proxied server. The timeout is set only between two successive write operations, not for the transmission of the whole request. If the proxied server does not receive anything within this time, the connection is closed. 

## 3-Proxy_read_timeout

    Syntax:proxy_read_timeout time;
    Default:proxy_read_timeout 60s;
    Context:http, server, location

Defines a timeout for reading a response from the proxied server. The timeout is set only between two successive read operations, not for the transmission of the whole response. If the proxied server does not transmit anything within this time, the connection is closed. 



## 4-proxy_next_upstream_timeout

    Syntax:proxy_next_upstream_timeout time;
    Default:proxy_next_upstream_timeout 0;
    Context:http, server, location


Limits the time during which a request can be passed to the next server. The 0 value turns off this limitation. 



