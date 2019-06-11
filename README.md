# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

Spring Cloud provides **Netflix Eureka**-based Service Registry and Discovery support with just minimal configuration. 
Each microservice must register itself  
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI1MDA4NTk1NSw4NDk3ODcyMCwtMTQ1Nz
Y0OTYyOV19
-->