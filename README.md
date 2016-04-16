## Eureka-Server
This a example of a eureka server with DS Replicas.

## How to run the two replicas (using profiles):

mvn spring-boot:run -Dspring.profiles.active="eureka1"

mvn spring-boot:run -Dspring.profiles.active="eureka2"

## Eureka client
The eureka client should specify the following in its application.yml:

eureka:

    client:
  
      serviceUrl:
    
        defaultZone: http://eureka1:8762/eureka/,http://eureka2:8763/eureka/
      
      
## To build the Docker image run:
package docker:build
