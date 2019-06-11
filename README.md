# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

Spring Cloud provides **Netflix Eureka**-based Service Registry and Discovery support with just minimal configuration. 
Each microservice must register itself with the service registry and tells the registry where it lives (host, port, node name) and perhaps other service-specific metadata - things that other services can use to make informed decisions about it. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzI3MTY2MDUyLC0yNTAwODU5NTUsODQ5Nz
g3MjAsLTE0NTc2NDk2MjldfQ==
-->