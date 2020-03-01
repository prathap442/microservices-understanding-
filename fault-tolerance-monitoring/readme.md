# A failover Mechanism


As we have discussed in the earlier approaches that if there exists a registry that tries to act as the medium of truth for the perfect endpoint microservice addresss answers it is always good in a system to have the redundancy at the places of the cruciality.


- Let's say that tommorrow something has gone wrong at the registry level then the microservice should have the alternate for the registry that is the redundant one should be available so that there is a high uptime for the availability.

- the additional services act as supportives and copy all of the data that exists in the microservice registry-1 to the microservice-registry-2 that is they should be in touch and hand to hand everytime like a master slave to have the perfect changes being replicated .


-----------------------------------

# Logging

   > keeping in consideration with the shot1.png
- here we discuss on the logging checks.
When ever a request is being originated from the outerworld to the service and when that service tries to communicate across the distributed network to get the response then, during this process if there exists a failure at some or the othe point then it would be difficult to trace out and this could be traced out by the keeping track on the log files.


- Manually keeping track on the log files makes a tedious task that if a request has come to one service in another service log file where does it perfectly gets paired up to for the sake of the tracking and this can be done by using `aggregated logging techniques` by using the tools like

   - LogStashKibanaElasticSearch Stack

   or such log stashing files .


- When the request gets originated to identity the flow of the request over the network the request is being tagged with the request id so that when it travels over the entire network it could easily be traced with its moves through out the network.


- This can be done by unique GUID



