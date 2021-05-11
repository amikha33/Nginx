




 Generally, the configuration file may include several server blocks distinguished by ports on which they listen to and by server names. Once nginx decides which server processes a request, it tests the URI specified in the request’s header against the parameters of the location directives defined inside the server block. 
 
  Add the following location block to the server block:

    location / {
        root /data/www;
    }

This location block specifies the “/” prefix compared with the URI from the request. For matching requests, the URI will be added to the path specified in the root directive, that is, to /data/www, to form the path to the requested file on the local file system. If there are several matching location blocks nginx selects the one with the longest prefix. The location block above provides the shortest prefix, of length one, and so only if all other location blocks fail to provide a match, this block will be used. 
 
 






![image](https://user-images.githubusercontent.com/46167070/117737574-6c30a600-b1fa-11eb-9a7f-6359924db424.png)


![image](https://user-images.githubusercontent.com/46167070/117737701-b1ed6e80-b1fa-11eb-9134-13626cfd301e.png)


![image](https://user-images.githubusercontent.com/46167070/117737735-c7fb2f00-b1fa-11eb-9ce3-e878ad5a4c00.png)


![image](https://user-images.githubusercontent.com/46167070/117737872-0f81bb00-b1fb-11eb-8f68-cca21df04cd2.png)





![image](https://user-images.githubusercontent.com/46167070/117737907-22948b00-b1fb-11eb-933a-6d19bd683ea9.png)


