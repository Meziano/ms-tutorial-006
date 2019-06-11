# Microservices Tutorial 006
# Introducing Eureka 
Until now we have hard-coded the hostnames and the port numbers of our microservices to enable the communication between them.
In this tuturial we will introduce a **Discovery mechanism** in order to let any microservice find any other just with its name.

With a **Registry and Discovery mechanism**, there is a **Registry Service** a kind of `phone book`, each microservice must register itself with it and tells it where it lives (hostname, port, ..). 
A microservice can communicate with any other registered one without having to know more than its name.   
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjY4MTU4NDYxLC0xNjcwODIxNDQzLDE1Mj
QwOTczLC0xMTI5Nzc0MzQ3LDMyNzE2NjA1MiwtMjUwMDg1OTU1
LDg0OTc4NzIwLC0xNDU3NjQ5NjI5XX0=
-->