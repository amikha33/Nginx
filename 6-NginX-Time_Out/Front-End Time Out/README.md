# Time header Out 


Syntax: client_header_timeout time;
Default: client_header_timeout 60s;
Context: http, server

Defines a timeout for reading client request header. If a client does not transmit the entire header within this time, the request is terminated with the 408 (Request Time-out) error. 

Syntax: send_timeout time;
Default:send_timeout 60s;

Context: http, server, location

Sets a timeout for transmitting a response to the client. The timeout is set only between two successive write operations, not for the transmission of the whole response. If the client does not receive anything within this time, the connection is closed. 





# client_body_timeout

Context: http, server, and location

Defines the inactivity timeout while reading a client request body. A connection becomes inactive the moment the client stops transmitting data. If the delay is reached, Nginx returns a 408 Request timeout HTTP error.

Syntax: Time value (in seconds)

Default value: 60





# keepalive_timeout

Syntax:keepalive_timeout timeout [header_timeout];
Default:keepalive_timeout 75s;

Context:http, server, location

The first parameter sets a timeout during which a keep-alive client connection will stay open on the server side. The zero value disables keep-alive client connections. The optional second parameter sets a value in the “Keep-Alive: timeout=time” response header field. Two parameters may differ.

The “Keep-Alive: timeout=time” header field is recognized by Mozilla and Konqueror. MSIE closes keep-alive connections by itself in about 60 seconds. 


# lingering_timeout

Context: http, server, and location

This directive defines the number of time that Nginx should wait between two read operations before closing the client connection.

Syntax: Numeric value (time)

Default value: 5 seconds

# resolver_timeout

Context: http, server, and location

Timeout for a hostname resolution query.

Syntax: Time value (in seconds)

Default value: 30

