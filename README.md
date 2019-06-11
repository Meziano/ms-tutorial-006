# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without having to know more than its name. 

## The discovery-service
To have a **registry  and discovery service** we just need a *Spring Boot Application* that we name **discovery-service** with its `pom` having the appropriate depedency and and its main-class annotated with `@EnableEurekaServer`.
### Embedding Eureka

#### The dependency``

 ```
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
```
#### The annotation


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
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQzNjE3MDI1MCwtMTM1ODcwNDYyNSwtMT
cyNDU0Mzk0OSwtNjYyMTQyNDM3LDcyNjkzMzYwNCwtMTY3MDgy
MTQ0MywxNTI0MDk3MywtMTEyOTc3NDM0NywzMjcxNjYwNTIsLT
I1MDA4NTk1NSw4NDk3ODcyMCwtMTQ1NzY0OTYyOV19
-->