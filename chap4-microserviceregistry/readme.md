# In this chapter we are going to see about the registries for the microservices.

- How the microservices get registered for the sake of the newer communications and connections to happen .

* The microservice need to be registered with the registered when it is about to joins in the network and when it gets registered then it can do its own process of communicating either by itself or by communication with the othere microservices .



* As shown as in the chap4-microserviceregistry/shot1.png the service first gets registered wit the hte registry and then makes the following connections

 - When the service dies the service sends a trigger to the registry about its crash and then
 - The service which is newly about to get added needs to have a health check at the regular intervals


There Are Two types of microservice communications that can take place

- Client Side Discovery
- Serverside Discovery

# ClientSideDiscovery
  - this is the microservice network in which the new microservice that is about to come gets registered with the register microservice .

  - When mcs1 needs to communicate with the mcs2(microservice2) then the mcs1 first asks to the mcs-registery on getting the point address for the sake of the communication with the registry the registry then gives the address back and then this mcs1 can communicate with the mcs2 with the help of the address obtained from the services registery .

# Server Side Discovery

  - When mcs1 needs to communicate with the mcs2 then the mcs1 first speaks with the load balancer then the load balancer speaks with the mcs-registery and then the load balancer speaks on behalf of the mcs1 to the mcs2
   - This kind of the microservice design is the server side discovery .

# 