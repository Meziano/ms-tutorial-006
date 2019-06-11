# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without having to know more than its name. 

## the discovery-service
To have a **registry  and discovery service** we just need a *Spring Boot Application* that we name **discovery-service** with its `pom` having the appropriate depedency and and its main-class annotated with `@EnableEurekaServer`.
### Embedding Eureka

#### The dependency``
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
```
 #### The annotation
 ```
 package de.meziane.ms;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.netflix.eureka.server.EnableEurekaServer;

@EnableEurekaServer
@SpringBootApplication
public class DiscoveryApplication {
  public static void main(String[] args) {
    SpringApplication.run(DiscoveryApplication.class, args);
  }
}
 ```
This is sufficient to let the application have an embedded `Eureka Server`.  
 ## A central configuration file for discovery-service
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTMwNTAyMDQ3LC0xMzU4NzA0NjI1LC0xNz
I0NTQzOTQ5LC02NjIxNDI0MzcsNzI2OTMzNjA0LC0xNjcwODIx
NDQzLDE1MjQwOTczLC0xMTI5Nzc0MzQ3LDMyNzE2NjA1MiwtMj
UwMDg1OTU1LDg0OTc4NzIwLC0xNDU3NjQ5NjI5XX0=
-->