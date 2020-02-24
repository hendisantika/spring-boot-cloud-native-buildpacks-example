# Sample Cloud Native  - Spring Boot application
The purpose of this project is to demonstrate how we can use cloud native buildpacks to create docker image.

# How to build and run

Java 8 lambdas are used here and there and thus the project can be compiled only with JDK 8 `javac`.

To compile just do `mvn clean install`.

**Prerequisites**

Docker needs to be installed

To Build the Cloud native image for the Spring Boot application execute the following:
```
./mvnw spring-boot:build-image
```
When the build succeeds, we should be able to see the image using below Docker command :
```
docker images | grep cloud-native
```
To run the application using Docker image 
```
docker run -d -p 8080:8080 --name springbootcontainer sumand/cloud-native-buildpacks:latest
```

Check the application
```
curl http://localhost:8080/Suman
```

for more detailed technical information please check my medium post :
