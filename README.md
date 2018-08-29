# Spring-Boot Camel QuickStart

This example demonstrates how you can use Apache Camel with Spring Boot.

This example create a basic REST api using camel with a hard coded backend.

### Building

The example can be built with

    mvn clean install

### Running stand alone 
Run the example using spring boot

    mvn spring-boot:run

### Running the example in OpenShift
This assume you already have an OpenShift environment and you know the basics.

The example can be built and run on OpenShift using a single goal:

    oc login ...
    mvn fabric8:deploy
    oc expose svc/fuse-camel-sb-rest

### Accessing the application

Swagger API definition

    curl http://localhost:8080/people-service/api-docs

Listing all the users

    curl http://localhost:8080/people-service/user/findall

Accessing a user
 
    curl http://localhost:8080/people-service/user/456    

Create a user
    curl -X PUT -H "Content-Type: application/json" -d '{"id":"1","name":"Wild Bill Novak"}' http://localhost:8080/people-service/user

Ping

    curl http://localhost:8080/people-service/echo/ping 
