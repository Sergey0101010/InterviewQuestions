[Вопросы для собеседования](README.md)
# Microservices

### What is microservice architecture?
It is an architectural style that structures an application as a collection of two or more
services that are:
- Independently deployable
- Loosely coupled

### What is monolith architecture?
A monolithic application is build as single unified unit. Application is build as a 
unified unit that is self-contained and independent of other applications.
A monolithic architecture is a singular, large computing network with one codebase
that couples all the business concerns together.

Monoliths can be convenient early on a project's life for erase of code management,
cognitive overhead, and deployment. This allows everything in the monolith to be
released at once.

### What are advantages/disadvantages of monolith architecture?
Primary advantage is fast development lifecycle due to the simplicity of having one 
codebase of the application. 
Also, it has some other advantages:
- **Easy deployment** - one executable file makes deployment easier
- **Easier development** - when app build in one codebase it is easier to develop
- **Performance** - Because all data is in one place, you don't have to call other services to get some data
- **Simplified testing** End-to-end testing can be performed faster than with a distributed app
- **Easy debugging** 

Disadvantages:
- **Scalability** Can't scale individual components
- **Reliability** if there is an error in any module, it could affect entire app
- **Barrier to technology adoption** change in framework requires update on the whole app
- **Deployment** a small change in monolith application requires redeployment of the entire monolith

### What are advantages/disadvantages of microservice architecture?
Advantages:
- **Deployability** more agility to roll out new versions of a service due to shorter build deploy test cycle
- **Reliability** a fault in microservice affects only service itself and its consumers
- **Availability** rolling out new version of a microservice requires little downtime
- **Scalability** each service can be scaled independently
- **Modifiablility** more flexibility in using new frameworks, libraries, data sources

Disadvantages:
- **Deployability** more complexity in deployment because far more deployment units,
more deployment jobs, scripts etc
- **Performance** very likely that services will need to communicate over network
- **Modifiability** if one endpoint has a lot of consumers it is harder to change API

### What types of communication between services do you know?
Synchronous(http, gRPC, TCP) and async(kafka, RabbitMQ, other)

### What microservice design patterns do you know?

- **API gateway.** It is a single entry point of entry for any 
microservice call
- **Aggregator** pattern. 
- **Database per service** 
- **Command Query Responsibility Segregation(CQRS)** to create 
- **SAGA** helps to make transactions through multiple services
- **Log aggregation** combines all logs from services to one place
- **Health check** usually done through `/health` endpoint which allows to check status of service
- **Externalized configuration** allow to configure service params depend on environment
- **Service discovery** 
- **Circuit breaker**

### What is service discovery?
It is a design pattern of microservice application which helps to improve horizontal
scalability of microservice application, because service consumers are abstracted
away from the physical location of the actual service instances.
It also allows to increase application resiliency. When service instance becomes 
unhealthy, service discovery component removes it from internal list of available services
Key components of service discovery:
- _Service registration_ - how service register with a service discovery agent
- _Client lookup of service address_
- _Information sharing_ how service information is shared across nodes?
- _Health monitoring_ 

1. Client application never have direct knowledge of the IP address of a service. They get 
it from service discovery agent
2. When service comes online it registers its IP address with a service discovery agent
3. Service discovery nodes share instance health information among each other
4. Services send a heartbeat to the service discovery agent. 

It is usually implemented in Spring using spring netflix - eureka
### What is load balancing?
### How authentication through JWT works?
### How logging in microservices works?





