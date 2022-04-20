## Overview
DESCRIPTION

As a Full Stack Developer, you have to build a CI/CD pipeline to demonstrate continuous deployment and host the application on AWS EC2 instance.

 

Background of the problem statement: 

As the project is in the final stage, management has asked you to automate the integration and deployment of the web application. You are required to set up an environment where the application will be hosted and accessed by users. The source code is supposed to be fetched from a GitHub repository.

 

You must use the following: 

    Eclipse

    GitHub

    Jenkins

    AWS EC2/ Virtual machine

 

Following requirements should be met: 

    A part of the source code should be tracked on the GitHub repository. You need to document the tracked files that are ignored during the final push to the GitHub repository.

    The submission of your GitHub repository link is mandatory. In order to track your task, you need to share the link of the repository in the document.

    The step-by-step process involved in completing this task should be documented.

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
