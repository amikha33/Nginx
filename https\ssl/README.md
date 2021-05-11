
Certificate


 To configure an HTTPS server, the ssl parameter must be enabled on listening sockets in the server block, and the locations of the server certificate and private key files should be specified: 


![image](https://user-images.githubusercontent.com/46167070/117837677-ef451100-b279-11eb-9647-c913cdfc8080.png)




 The server certificate is a public entity. It is sent to every client that connects to the server. The private key is a secure entity and should be stored in a file with restricted access, however, it must be readable by nginx’s master process. The private key may alternately be stored in the same file as the certificate:

    ssl_certificate     your_domain.crt; # The certificate file
    ssl_certificate_key your_domain.key; # The private key file


## How To Generate Certificate


        sudo yum install openssl

Chances are that you already have it available on your system – it should now be installed regardless. Once the package is confirmed to be installed on your system, generate the keypair using the following command:


     openssl genrsa -des3 -passout pass:x -out keypair.key 2048
     
 

     sudo openssl req -new -days 365 -key your_domain.key -out your_domain.csr

    
     
     
     Country Name (2 letter code) [AU]:US
     State or Province Name (full name) [Some-State]:New York
     Locality Name (eg, city) []:New York City
     Organization Name (eg, company) [Internet Widgits Pty Ltd]:Bouncy Castles, Inc.
     Organizational Unit Name (eg, section) []:Ministry of Water Slides
     Common Name (e.g. server FQDN or YOUR name) []:server_IP_address
     Email Address []:admin@your_domain.com
     
  

![image](https://user-images.githubusercontent.com/46167070/117841704-8bbce280-b27d-11eb-8aa1-d302fba0ff2c.png)


   
     
     
     
 Creating the Certificate “.crt” File   
             
             sudo nano your_domain.csr
    

![image](https://user-images.githubusercontent.com/46167070/117845993-51eddb00-b281-11eb-8dff-27e1fded5213.png)







![image](https://user-images.githubusercontent.com/46167070/117784053-6d39f580-b243-11eb-9667-8ecadbeb67a5.png)


