# consul-demo
Demonstration of a springboot app using consul for service/dependency discovery.

## Getting started
Make sure you have the necessary dependencies for Docker installed.

1.Change your directory to the local docker directory

    cd <PATH_TO_GIT_DIR>/docker/local
  
2.Start up the docker container.

    docker-compose up -d
    
3.Build the Spring Boot project in the root directory of the project
    
    gradle clean build
    
4.Run the application

    gradle bootRun
    
5.You will see a message similar to below if everything is in working order

    Registering service with consul: NewService{id='consul-demo', name='consul-demo', tags=[], address='0.0.0.0', port=8080, enableTagOverride=null, check=Check{script='null', interval='10s', ttl='null', http='http://0.0.0.0:8080/health', tcp='null', timeout='null', deregisterCriticalServiceAfter='null', tlsSkipVerify=null, status='null'}, checks=null}

## Useful Links
Spring Cloud Consul https://cloud.spring.io/spring-cloud-consul/

Consul https://www.consul.io/

Installing Docker https://docs.docker.com/install/


## Managing Docker
To manage the docker container for consul, you should change to the directory of the local docker directory

    cd <PATH_TO_GIT_DIR>/docker/local

To start up, run:
    
    docker-compose up -d
    
To shut down, run:

    docker-compose stop
    
To re-create, run:

    docker-compose up -d --force-recreate
