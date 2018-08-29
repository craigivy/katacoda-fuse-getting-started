# Spring-Boot Camel QuickStart

This example demonstrates how you can use Apache Camel with Spring Boot.

The quickstart uses Spring Boot to configure a little application that includes a Camel route that triggers a message every 5th second, and routes the message to a log.

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

Listing all the users

    http://localhost:8080/people-service/user/findall

Accessing a user
 
    http://localhost:8080/people-service/user/456    