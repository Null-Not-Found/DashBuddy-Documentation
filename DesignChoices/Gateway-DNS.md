# Gateway and DNS design Choices
## Contents
 - [Gateway](#gateway)
 - [DNS](#dns)

## Gateway
For the gateway we used Node.js with Express. 
The gateway makes, when a call is made to it, connection to the DNS to retrieve the current location of a specified Microservice and then makes a call to that microservice based on the endpoint that was called.
We didnt use Apollo because of two reasons: 
1. Apollo has more use when you have multiple GraphQL microservices
2. Time constraints caused it to not be worth the effort to rebuild the gateway to function with Apollo

## DNS
For the DNS we used Node.js with Express.
The DNS listens for calls made by microservices to its registration endpoint. When a call is made it saves the IP and name of the microservice in memory. 
It then occasionally pings the microservice to check if its still alive and healthy. If this call fails it removes the microservice and its IP from its memory.
If a call is made to retrieve the IP of a specific microservice it will return a random IP from the list of IPs that match the name for the needed microservice. 
