[Вопросы для собеседования](README.md)

# Spring framework
## What are Spring and Spring Boot and what are the differences between them?
Spring is open-source lightweight framework that allows developers to build different enterprise 
applications. It's main feature is Dependency Injection container which allows you to manage your business
objects. 

Spring Boot is built on top of Spring framework, it provides all the features of Spring and has key 
feature often called "convention over configuration" so it configure a lot of things in your app by default, but
you always can configure them.

## What are key features of Spring?
**Inversion of Control(IoC)** - Spring container takes care of wiring dependencies
of various objects and creating them

**Aspect oriented programming(AOP)** supports AOP to separate business logic from
system services

**MVC Framework** used to create RESTful web services

## What is dependency injection?
Dependency Injection is one of the realizations of Inversion of Control(IoC) - principle in which 
control over object(spring component/bean) lifecycle is managed by Spring, not by a programmer. 
It allows to have loose coupling of components. 

## What types of bean injection might be?
**Setter injection**
```java
@Autowired
public setComponent(ComponentInterface component){
    this.component = component;
}
```

**Constructor injection**
```java
@Autowired
public MyClass(Component1 comp1, Component2 comp2) {
    this.comp1 = comp1;
    this.comp2 = comp2;
}

```
**Field injection**
```java
@Component
public class MyClass {
    @Autowired
    Component classField;
}
```

## What type of bean injection is more preferable?
Field injection is the least preferred because it has drawbacks:
- You can't create immutable objects
- Your classes have tight coupling with DI container.
- Classes can't be instantiated(for example in unit tests) without reflection. You need DI container to
instantiate them
- Very easy to have a lot of dependencies, when using constructor injection, you would have constructor 
with many dependencies and this will signal you about bad design

Both constructor and setter injections are good practice, so you should use each one in different scenarios.
A good rule of thumb is to use constructors for _mandatory_ dependencies and setter methods or configuration methods 
for _optional dependencies_. 

Constructor injection is more preferable in most situations because allows to implement _immutable objects_, ensure
that required dependencies are not `null` and if your class have too many dependencies your more likely to notice it.

[stackoverflow](https://stackoverflow.com/a/39892204/22463602)
[spring docs](https://docs.spring.io/spring-framework/docs/4.2.x/spring-framework-reference/html/beans.html#beans-constructor-injection)

## What is Spring bean?
Spring bean is java object instantiated and managed by Spring IoC container.

## What bean scopes exist and which one is default one?
You can define bean scope by using annotations. Existing scopes:
- Singleton(Default scope) one bean per application context.
- Prototype(`@Scope("prototype")`) - one bean per object instance in application context.

Other types of scopes are web scopes, 
specific for web applications(only valid in the context of web-aware Spring `ApplicationContext`)
- Request scope(`@RequestScope`) - spring container creates a new instance of bean for each request.
- Session scope(`@SessionScope`) - spring container creates a new instance of bean for each http session.
- Application scope(`@ApplicationScope`) - spring container creates a new instance of bean for entire web application
- WebSocket scope(`@Scope(scopeName = "websocket"`) - scopes single bean definition to the lifecycle of a `WebSocket
`
 
[Spring docs](https://docs.spring.io/spring-framework/reference/core/beans/factory-scopes.html)

## How we can configure some business logic before destruction or after init of Spring bean?
We may use annotation `@PostConstruct` to declare some actions which should be done
instantly after bean creation and annotation `@PreDestroy` to perform some actions 
before bean destruction  

## Please describe bean lifecycle

[//]: # (// todo )

## What do you know about Spring Aware interfaces?

[//]: # (todo )

## Can we have multiple Spring Configuration files in one project?
Yes, it is possible, usually done to increase maintainability and modularity

## What's difference between lazy and eager bean initialization?
**Eager** initialization means that beans are created during start of an application context its default initialization
for all _singleton_ beans.
**Lazy** initialization means that bean is created and dependencies injected only when bean is needed its default
initialization for all _prototype_ beans.

## When to use _lazy_ initialization and when to use _eager_?
In most cases eager initialization is more preferable because its **fail-fast** and you will find most of bean's 
wiring-related problems during your application startup. Also, such initialization have only startup performance 
overhead. 
Lazy initialization might be helpful when we have, for example we have large monolith application and some parts of it are 
rarely used, so we make beans used in this part lazily-initialized so our app doesn't consume so many resources. 

## How to inject lazy beans?
```java
@Lazy
@Service
public class EmployeeManagerImpl implements EmployeeManager {
  //
}

@Controller
public class EmployeeController {

    @Lazy
    @Autowired
    EmployeeManager employeeManager;
}
```

## What is dispatcher servlet?

`DispatcherServlet` is a central servlet that dispatches requests to controllers  

[Spring docs](https://docs.spring.io/spring-framework/docs/3.0.0.M4/spring-framework-reference/html/ch15s02.html)

## What is Controller in Spring?
Controller is a class which contains methods for processing requests from `DispatcherServlet` all controller 
classes are annotated with `@Controller` or `@RestController` annotations and all such classes are beans.

## What's the difference between `@Controller` and `@RestController`
These annotations are the same but `@RestController` is simply combination of `@Controller` and `@ResponseBody` 
annotations. 

## What's the difference between @Component, @Repository & @Service annotations in Spring?

`@Repository` annotation contains `@Component` annotation and this annotation also marker for automatic translation 
of exceptions.

`@Service` is have the same functionality as `@Component` but in future Spring releases it might have some additional
functions

[StackOverflow](https://stackoverflow.com/a/38549461/22463602)

## What is `@SpringBootApplication`?
This annotation is combination of 3 annotations `@Configuration` `@EnableAutoConfiguration` `@ComponentScan` with 
their default attributes.

## What if Spring context contains more than one bean of the same type to inject in some place?
1. You can use `@Primary` annotation to mark your component as primary for injecting in such situations.
```java
@Component
@Primary
public class MyPrimaryComponent implements MyComponentInterface {
    
}
```
2. Use `@Qualifier("name")` you should put this annotation in place where you declare component and in place where
you inject it.
```java

@Component
@Qualifier("NAME")
public class MyQualifiedComponent implements MyComponentInterface {
    
}
```

```java
public class MyServiceImpl implements MyService {
    public MyServiceImpl(@Qualifier("NAME") MyComponentInterface componentInterface) {
        this.componentInterface = componentInterface;
    }
}  
```

## How to enable transactions in Spring and how they work?
You can make method in some class transactional by putting on top of it `@Transactional` annotation 
and set up level of transaction isolation by `@Transactional(isolation=TransactionDefinition.ISOLATION_READ_UNCOMMITTED)`

Spring uses transactional proxy of class where you declare transaction. 
The proxy has access to a transaction manager and will ask it to open and close transactions/connections
The transaction manager itself will simply manage simple JDBC connection.

## What is transactional propagation levels?
Transactional propagation level is parameter which regulates what Spring should do if inside 
`@Transactional` method other `@Transactional` method called.
 Spring has 7 propagation types:
- **Required(default)** if method called in already existing transaction it won't require the new one, 
otherwise it will create a new one.
- **Supports** don't care if transaction exist or not it will work in any case
- **Mandatory** If method doesn't called inside transaction then will throw exception.
- **Require_new** Method always require its own separate transaction
- **Not_Supported** Can't been called inside transaction, suspend transaction if called inside it and execute 
method
- **Never** throws an exception if called inside transaction
- **Nested** Spring checks if transaction exists and if so, creates a savepoint, if no transaction exist
it will work as _REQUIRED_

## How many transactions we will have if inside class we will have transactional method which calls other `@Transactional` method of this class?
```java
@Service
public class UserService {

    @Transactional
    public void invoice() {
        createPdf();
        // send invoice as email, etc.
    }

    @Transactional(propagation = Propagation.REQUIRES_NEW)
    public void createPdf() {
        // ...
    }
}
```
In this code we will have one transaction even if method `createPdf()` has propagation set to `REQUIRES_NEW`
This happens because Spring will create only one proxy object of your class and because of this 
only one transaction will be created. 

## What is Aspect-Oriented Programming(AOP)?
AOP is another way of thinking about program structure, key unit in OOP is the class and in AOP the 
unit of modularity is Aspect. Aspects enable modularization of concerns that cut across multiple types of 
objects. 

## What are Aspect, Advice, Pointcut and JoinPoint in AOP?
**Aspect** - a class that implements cross-cutting concerns, such as transaction management
**Advice** - the methods that get executed when a specific _JoinPoint_ with mathing _Pointcut_ is reached 
in the application.
**Pointcut** a set of regular expressions that are matched with _JoinPoint_ to determine whether _Advice_
needs to be executed
**JoinPoint** - a point during the execution of a program, such as the execution of a method or the 
handling of an exception.

 ## How to create log aspect for some class with business logic?
```java
@Service
public class MyService {
 public String publishComment(Comment comment) {
  log.info("publishComment0");
  return "Some value";
 }
}
```

```java
@Component
@Aspect
@EnableAspectJAutoProxy
public class LoggingAspect {
 @Around("execution(* services.*.*(..))")
 public void log(ProceedingJoinPoint joinPoint) {
  logger.info("Method will execute");
  joinPoint.proceed(); //call intercepted method
  logger.info("Method executed");
 }
    
    
}
```
## What is reactive programming?
Reactive programming is programming paradigm where we focus on developing asynchronous and non-blocking components. 
Reactive programming is usually event-driven and often follow reactive manifesto, these systems have four important
characteristics.
- **Responsive** the system should respond in a timely manner
- **Resilient** in case of system failure it should stay responsive
- **Elastic** reactive systems can react to changes and stay responsive under different workloads
- **Message-Driven** reactive systems need to establish a boundary between components by relying on asynchronous
message passing

## What is Spring WebFlux?
Spring WebFlux is Spring's reactive-stack web framework it's alternative to Spring MVC.



