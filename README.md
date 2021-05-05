# IOT SERVICE - EUREKA SERVER
Service for the registration and discovery of services. This service uses the Netflix Eureka library for Spring Boot.

## Basic configuration
By default, this service can already be executed without any configuration.

## Run service
Execute the following command to run this service:

```
./mvnw package && java -jar target/eureka-service-0.0.1-SNAPSHOT.jar
```

Go to http://localhost:8761 to view the Eureka dashboard in the browser.

## Run with Docker

**Note:** The target .jar must be generated with the above command `./mvnw package`. 

Build image for service:

```
docker build --pull --rm -f "Dockerfile" -t iot-eurekaservice "."
```

Run the container:
```
docker run -p 8761:8761 --name iot-eurekaservice iot-eurekaservice
```