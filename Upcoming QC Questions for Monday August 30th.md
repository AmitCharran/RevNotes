# Upcoming QC Questions for Monday August 30th:

> Topics: <br>
>
> - [Servlets](#servlets)
> - [AWS](#aws)
> - [DevOps/SDLC](#devops)
> - [Docker](#docker)
> - [Spring Core](#spring)

<br>

## Docker

1. What is Docker?

   * Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your application infrastructure so you can deliver software quickly.
2. What's a Dockerfile? Image? Container?
   * Dockerfile - a text document that contains all the commands a user could call on the command line to assemble an image
   * Image - a file used to execute code in a Docker container. It's like a set of instruction to build a docker container.
     * It contains application code, libraries, tools, and dependencies to make the application run
   * Docker container - the virtualized runtime environment used in the application development. It creates run and deploy the application.
3. What is Containerization? How is it different from Virtualization?
   * Containerization - A Docker container image is **a lightweight, standalone, executable package of software** that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.
4. List some docker commands that you've used.
   * https://docs.docker.com/engine/reference/commandline/docker/
   * docker build
5. What is the _first_ line in a `Dockerfile`?
   * FROM - 
6. What is the command you run to `build` and image from a `Dockerfile`.

   * docker build
7. What is the command you run to `run` a container from an image?
   * docker run

## AWS

1. What are the [benefits of cloud services](https://www.salesforce.com/in/products/platform/best-practices/benefits-of-cloud-computing/)?

   * Cost Savings, Security, Flexibility, Mobility, Insight, Auality Control, Increased Collaboration, Disaster Recovery, Loss Prevention, Automatic Software Updates, and Sustainability
2. What are the [3 models of Cloud computing](https://edge.siriuscom.com/cloud/the-top-3-cloud-computing-service-models)?
   * IaaS - infrastructure as a service - provides virtualized computer resource (hardware)
   * PaaS -  Platform as a Service - manage application without IT infrastructure. 
     * Developers can focus on writing code and creating apps without dealing with an infrastructure like provisioning servers, storage and backup.
     * It is  easier innovate and scale your service  on demand
   * SaaS - Software as a Service - Allows access to software without downloading or installing anything. But they do require plugins
3. What is AWS RDS? What type of service is this? Iaas, Paas, Saas?
   * RDS -  Relational Database Service - its allows you to operate add, scale, relational database in the cloud
     * PaaS - it's a tool to setup and manage database
4. What is the relationship between a Region and an Availability Zone?
   * Region - a physical location around the world where they cluster data centers
   * Availability Zones - a cluster of data center
   * Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area
   
5. What are Security Groups?
   * As as virtual firewalls for EC2 instances to restrict incoming and outgoing traffic
     * Inbound rules and outbound rules
6. Explain what an EC2 is.
   * Elastic Compute Cloud - a web service that is secure and resizable and can compute capacity in the cloud
7. What is EBS?
   * service for deploying and scaling web applications
8. What's am AMI?
   * Amazon machine images - provides information to launch an instance
     * You can launch multiple instance from a single AMI
9. What is an RDS?
   * Relational Database Service - Its how users set up operate and scale relational database in the cloud
10. What's the difference between Horizontal and Vertical Scaling?
    * Horizontal Scaling - Adding additional of the same resource to current environment
    * Vertical Scaling - Adding new resources to current environment

<br>

## Servlets

1. What is a servlet? What about a servlet container? Which servlet container have you worked with?

   * Servlet - used to extend capabilities of servers. It accesses information through request/response programming models
   * [Servlet container](https://dzone.com/articles/what-servlet-container) - is used to dynamically generate the web page on the server side.
   * Java-Servlet-EE

2. Describe the servlet class inheritance hierarchy. What methods are declared in each class or interface?

   * Servlet Interface

   * Generic Servlet

     * init

   * Http Servlet

     * doXXXX methods

   * MyServlet

     

3. How would you create your own servlet?

   * extend HttpServlet

4. What is the deployment descriptor? What file configures your servlet container?

   * The deployment descriptor is the file used by the servlet container to define which servlets match up with which URLs.
   * WEB-INF??

5. Explain the lifecycle of a servlet - what methods are called and when are they called?

   1.  init() - initialize servlet
   2.  service() - called to process a clients request
   3.  destroy() - terminated servlet

6. Is eager or lazy loading of servlets the default? How would you change this?

   1.  Eager Loading - loads everthing in the beginning
       1.  Default
   2.  Lazy Loading - load when needed
       1.  <load-on-startup> 0 </load-on-startup>

7. What are some tags you would find in the web.xml file?

   1.  display name
   2.  welcome file

8. What is the difference between the [ServletConfig and ServletContext](https://www.geeksforgeeks.org/difference-between-servletconfig-and-servletcontext-in-java-servlet/) objects? How do you retrieve these in your servlet?

   1.   ServletConfig is for a specific servlet, while information shared by ServletContext is available for all servlets in the web application.

9. What is the purpose of the [RequestDispatcher](https://www.javatpoint.com/requestdispatcher-in-servlet)?

   1.  dispatch requests to another resource. Only way of Servlet collaboration

10. Explain the difference between RequestDispatcher.forward() and HttpServletResponse.sendRedirect()

    1.  Forwards a request from a servlet to another resource (servlet, JSP file, or HTML file) on the server.
    2.  Redirects the client to a specified URL

11. What are some different ways of [tracking a session with servlets](https://en.ryte.com/wiki/Session_Tracking?

    1.  Cookies
    2.  Hidden From Field
    3.  URL Rewriting
    4.  HttpSession

12. What is object mapping? Any Java libraries for this?

    1. Object Mapping -- convert data between incompatible types
    2. 

13. How would you send text or objects back in the body of the HTTP response from a servlet?

    1. `response.getOutputStream.println()`

14. What is the difference between getParameter() and getAttribute() methods?

    1. `getParameter` = recieves input from requests
    2. `getAttributes` = can be used for any object in the request scope.

15. Explain the front controller design pattern

    1. The front controller design pattern means that **all requests that come for a resource in an application will be handled by a single handler and then dispatched to the appropriate handler for that type of request**

### Spring

1.  What are Spring Projects and Spring Modules?
    1.  Spring Projects - Projects that uses the modules JDBC, AOP, BEANS, or CONTEXT
    2.  Spring Modules - JDBC, AOP, BEANS, Context
2.  What is IOC and what does the IOC Container do?
    1.  IOC - Inversion of Control - Transfer control of objects
    2.  IOC Container - Core of spring framework - using meta data it will create  objects, wire them together and configure them.
3.  What is dependency injection and what are some of the benefits of using dependency injection?
    1.  [Dependency Injection](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html) - objects define their own dependency through headers, arguments and other properties
    2.  Code is more readable and reusable and testable
4.  What types of dependency injection does Spring support?
    1.  Constructor
    2.  Setter
    3.  Field -- member variables
5.  What are some differences between BeanFactory and ApplicationContext? Which one eagerly instantiates your beans?
    1.  BeanFactory - lazy loading
    2.  ApplicationFactory - eagerly instantiate
6.  What is the Spring Bean lifecycle?
    1.  
7.  What is bean wiring? What about autowiring?
    1.  wiring - declaring a bean using XML configuration
    2.  auto wiring - implicitly declaring beans thorugh annotation
8.  What are the different ways that Spring can wire beans?
    1.  no
    2.  byName
    3.  byType
    4.  constructor
    5.  autoDetect
9.  What are the scopes of Spring beans? Which is default?
    1.  Singleton
    2.  Prototype
    3.  Request
    4.  Session
    5.  application
    6.  web socket
10.  What is the concept of component scanning and how would you set it up?
     1.  Annontating classes in order to make them into beans
         1.  Spring can auto scan, detect, and instantiate components from predefined packages
     2.  You would set it up through annotations
         1.  @ComponentScan()
11.  What are the benefits and limitations of Java configuration?
     1.  Java config, Its type safe, 
     2.  however, autowiring is not precise 
12.  What does the @Configuration and @Bean annotations do?
     1.  @Configuration - generate bean definition and service request for the beans in the class at runtime
     2.  @Bean - declare beans object.
13.  What is @Value used for?
     1.  Used for injecting values into Bean fields
14.  What is Spring Expression Language? What can you reference using SpEL? What is the difference between $ and # in @value expressions?

### Spring MVC

15. Explain the MVC architecture and how HTTP requests are processed in the architecture
    1. MVC architecture -- separates application into three main components
       1. Model - corresponds to all data related object that theuser works with
       2. View - used for UI logic of the application
       3. Controller - Interface between model and view.Manipulating data and interacting with requests
16. List some stereotype annotations. What are the differences between these?
    1. Component - generic stereotype - it means all three
    2. Repository - the classes that access the data in some database
    3. Service -  This class handles the logic between the endpoint and database
    4. Controller - interacts with the endpoint
17. How would you declare which HTTP requests you’d like a controller to process?
    1. Map request with @RequestMapping
18. What is the difference between @RequestMapping and @GetMapping?
    1. @GetMapping is a shortcut for @RequestMapping(method = RequestMethod.GET)
    2. @RequestMapping is a generic sort of mapping for all html verbs
19. How to declare the data format your controller expects from requests or will create in responses?
    1. @RequestMapping(value = 'getjson')
20. How would you extract query and path parameters from a request URL in your controller?
    1. @RequestParam("param")
21. What concerns is the controller layer supposed to handle vs the service layer?
    1. controller layer retrieves data from the endpoint and pass it on to the service layer
    2. Service performs some logic on those data it recieved from the controller layer
22. How would you specify HTTP status codes to return from your controller?
    1. @ResponseStatus annotation
23. How do you handle exceptions thrown in your code from your controller? What happens if you don’t set up any exception handling?
    1. Using @ExceptionHandler annotation
    2. If no ExceptionHandling annotation it goes to predefined exceptions you didnt write
24. How would you consume an external web service using Spring?
    1. 
25. What are the advantages of using RestTemplate?
    1. It simplifies the interaction between HTTP servers and supports RESTful systems.
    2. It is able to consume RESTful Web Services

### Spring AOP

28. What is “aspect-oriented programming”? Define an aspect.
    1. Aspects enable the modularization of concerns such as transaction management that cut across multiple types and objects.
       1. Modularity - emphasizes separation of functionality of a program to make things interchangeable 
       2. For example, logging can be interchangeable 
29. Give an example of a cross-cutting concern you could use AOP to address
    1. Logging can be interchangable
    2. Caching
    3. Memory Management
    4. Persistece layer
30. Define the following:

- Join point
  - a point during the execution of a program, such as the execution of a method or the handling of an exception. In Spring AOP, a join point *always* represents a method execution.
- Pointcut
  - a predicate that matches join points. Advice is associated with a pointcut expression and runs at any join point matched by the pointcut (for example, the execution of a method with a certain name). The concept of join points as matched by pointcut expressions is central to AOP, and Spring uses the AspectJ pointcut expression language by default.
- Advice
  - action taken by an aspect at a particular join point. Different types of advice include "around," "before" and "after" advice. (Advice types are discussed below.) Many AOP frameworks, including Spring, model an advice as an *interceptor*, maintaining a chain of interceptors *around* the join point.

31. What are the different types of advice? What is special about the @Around advice? How is the ProceedingJoinPoint used?

    1. *Before advice*: Advice that executes before a join point, but which does not have the ability to prevent execution flow proceeding to the join point (unless it throws an exception).
    2. *After returning advice*: Advice to be executed after a join point completes normally: for example, if a method returns without throwing an exception.
    3. *After throwing advice*: Advice to be executed if a method exits by throwing an exception.
    4. *After (finally) advice*: Advice to be executed regardless of the means by which a join point exits (normal or exceptional return).
    5. *Around advice*: Advice that surrounds a join point such as a method invocation. This is the most powerful kind of advice. Around advice can perform custom behavior before and after the method invocation. It is also responsible for choosing whether to proceed to the join point or to shortcut the advised method execution by returning its own return value or throwing an exception.

32. Explain the pointcut expression syntax

    1. ```java
       @Pointcut("execution(* transfer(..))")// the pointcut expression
       private void anyOldTransfer() {}// the pointcut signature
       ```

    2. 

33. What visibility must Spring bean methods have to be proxied using Spring AOP?

    1. public methods
    2. Calling those public methods must be form outside the bean

### Spring Data

34. What is Spring ORM and Spring Data?
    1. Spring ORM - API that integrates Spring with ORMs like Hiberate and JPA
       1. Advantages
          1. Less Coding
          2. Easy to Test
          3. Better exception handling
          4. Integrated transaction management
    2. Spring Data
       1. Provides easy to use data access tools
       2. @Components stereotypes
35. What is the Template design pattern and what is the JDBC template?
    1. JDBCTemplate
36. What does @Transactional do? What is the PlatformTransactionManager?
    1. @Transactional allows frameworks to add transactional logic
    2. Platform Transaction Manager - Extends transaction manager
       1. Used for transaction infrastructure
37. What is a PersistenceContext?
    1. 
38. Explain how to integrate Spring and Hibernate using ContextualSession
39. What interfaces are available in Spring Data JPA?
40. What is the difference between JPARepository and CrudRepository?
41. What is the naming conventions for methods in Spring Data repositories?
42. How are Spring repositories implemented by Spring at runtime?
43. What is @Query used for?

### Spring Boot

44. How is Spring Boot different from legacy Spring applications? What does it mean that it is “opinionated”?

45. What does “convention over configuration” mean?

46. What annotation would you use for Spring Boot apps? What does it do behind the scenes?

47. How does Boot’s autoconfiguration work?

48. What is the advantage of having an embedded Tomcat server?

49. What is the significance of the Spring Boot starter POM?

50. What is the Spring Boot actuator? What information can it give you?

51. What files would you use to configure Spring Boot applications?

52. What is the benefit of using Spring Boot profiles?