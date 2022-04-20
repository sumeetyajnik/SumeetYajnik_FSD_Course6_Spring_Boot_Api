## Overview

Project to demonstrate:

* how to create a Spring Boot REST API
* how to run Spring Boot in Docker and publish to Docker Hub
* how to deploy the Spring Boot application to AWS with CloudFormation

## Pre-requisites

* JDK 8+
* Docker

## Building

### Testing

`./gradlew test`

### Building (no tests)

`./gradlew assemble`

### Building (with tests)

`./gradlew build`

### Running in Docker

`./gradlew assemble docker dockerRun`

### Stopping Docker container

`./gradlew dockerStop`

### Deploying to AWS

`./gradlew awsCfnMigrateStack awsCfnWaitStackComplete -PsubnetId=<your-subnet-id> -Pregion=<your-region>`

### Deleting AWS deployment

`./gradlew awsCfnDeleteStack awsCfnWaitStackComplete`

## Using API

* get all rides - GET [/ride](http://44.200.181.64:8080/ride) to get a list of all the rides
* get specific ride - GET [/ride/${id}](http://44.200.181.64:8080/ride/1) to get a specific ride
* create ride - POST JSON to [/ride](http://44.200.181.64:8080/ride) to create a new ride
