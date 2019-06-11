# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without having to know more than its name. 

## Embedding Eureka
To have a **registry  and discovery service** we just need a *Spring Boot Application* with its `pom` having the appropriate depedency `pring-cloud-starter-eureka-server` and its main-class annotated with `@EnableEurekaServer`. This is sufficient to let the application  
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NjQ2NjgwMTMsLTE2NzA4MjE0NDMsMT
UyNDA5NzMsLTExMjk3NzQzNDcsMzI3MTY2MDUyLC0yNTAwODU5
NTUsODQ5Nzg3MjAsLTE0NTc2NDk2MjldfQ==
-->