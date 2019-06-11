# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without  

Spring Cloud provides the **Netflix Eureka**-based **Service Registry** and **Discovery** support with just minimal configuration. 
Each microservice must register itself with the service registry and tells the registry where it lives (host, port, node name) and perhaps other service-specific metadata - things that other services can use to make informed decisions about it. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM5OTk3NzU2MiwtMTY3MDgyMTQ0MywxNT
I0MDk3MywtMTEyOTc3NDM0NywzMjcxNjYwNTIsLTI1MDA4NTk1
NSw4NDk3ODcyMCwtMTQ1NzY0OTYyOV19
-->