# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without having to know more than its name. 

## Embedding Eureka
To have a **registry  and discovery service** we just need a *Spring Boot Application* with its `pom` having the appropriate depedency:
```
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
```
 and its main-class annotated with `@EnableEurekaServer`. 
 ```
 
 ```
This is sufficient to let the application have an embedded `Eureka Server`. 
## 
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NjA0NDQzNDUsLTY2MjE0MjQzNyw3Mj
Y5MzM2MDQsLTE2NzA4MjE0NDMsMTUyNDA5NzMsLTExMjk3NzQz
NDcsMzI3MTY2MDUyLC0yNTAwODU5NTUsODQ5Nzg3MjAsLTE0NT
c2NDk2MjldfQ==
-->