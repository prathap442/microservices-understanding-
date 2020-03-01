# the chap5 on data
 One of the most common problems that are being faced by the developers when developing the microservices with the databases that depends upon the system and its interaction with the databse


# Shared Database System
Let us suppose a system that interacts with a single database and all the microservices that exist in that network also get the same database then the this kind of the system is called as the shared database system 


Example: As shown in the chap5-data/shop8.png where the multiple microservices interact with a single database


pros:
  - the joins queries could easily be performed when the data needs to be accessed .
  - the database can even be sharded but the sharding has also got some side effects on a large scale .



cons:
  - At the same time the wait time for getting the data also tries to increase .


# Database per service


There is another way of designing the microservice based system entirely by means of seperating one service data from another service data as shown in the shot7.png .


pros:
  - The data can be accessed at a faster rate - the load on the system gets reduced as the requests tend to get segregated in this kind of the system arrangement .
  - Every Service can be writtten in various languages and can communicate with the different kinds of the databases .

cons:
 - the distributed kind of the system makes the things complex when the request needs some kind of data where the data from all of the 3 services required then the wait time rises.

  - Database joins types of queries would be difficult to concat .

# The above problems can also resolved to some extent by opting for the techniques as: 



# Api Composition

  the api composition service is the kind of the service in which the main service takes care of the two requests needs to the sent to 2 different kind of the services and then there exist and the resultant of the querires made from the 2 of the microservices is being compositionised in the mcs3 from which the response is being obtained 


# Event Sourcing
  Is the kind of the concept that gets generated when there needs to be a track change to be kept on the changes that happen in the system .


  Let us taken an example of the event drive architecture as shown .

  the shot11.png here shows the process of the taking up of the snapshots of a particular product to keep track on the changes 


  In the shot10.png we see how the communication takes place through the event driven architecture .


  When ever there is a change in the product price then at that the product service publishes a message to the event store and this eventstore inturn triggers the product search service and the product recommendation service .


  so here the update will take place at 2 of the places at a stretch 




  What happens if there is a system where one service has different databae and the other service too has got the different database where the process goe on shown in the shot12.png 



-----------------------------------
# Two Phase DataBase Commit .


Two phase commit is used for the sakeof the provision of the data integrity 

where the database transactions happen at the respective microservices where the child microservices take their COMMIT transactions based on the trigger given by the main service .


Where let us describe the scenario by a diagram as shown in the `shot13.png`  where the coordinator exists as a central manager to coordinate the transactions and see that all the transactions are pucca and have clear acknowledgement of the yes from all the 3 microservices then only the transaction gets committed. 


Pros:
  Dataintegrity is not lost. A surity that the transaction is pucca

  And no failures in the process of the actions that need to take places for a process .

Cons:
  The system becomes complex
  Timelocking would be a problem where the other requests are kept on hold for the current request to get processed .


This type of the mechanism can be overcomed by using the SAGA kind of the system of the mciroservice .





-----------------------------------

 

