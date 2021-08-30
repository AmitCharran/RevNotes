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

13. How would you send text or objects back in the body of the HTTP response from a servlet?

14. What is the difference between getParameter() and getAttribute() methods?

15. Explain the front controller design pattern

### Spring

1.  What are Spring Projects and Spring Modules?
2.  What is IOC and what does the IOC Container do?
3.  What is dependency injection and what are some of the benefits of using dependency injection?
4.  What types of dependency injection does Spring support?
5.  What are some differences between BeanFactory and ApplicationContext? Which one eagerly instantiates your beans?
6.  What is the Spring Bean lifecycle?
7.  What is bean wiring? What about autowiring?
8.  What are the different ways that Spring can wire beans?
9.  What are the scopes of Spring beans? Which is default?
10. What is the concept of component scanning and how would you set it up?

11. What are the benefits and limitations of Java configuration?

12. What does the @Configuration and @Bean annotations do?

13. What is @Value used for?

14. What is Spring Expression Language? What can you reference using SpEL? What is the difference between $ and # in @value expressions?

### Spring MVC

15. Explain the MVC architecture and how HTTP requests are processed in the architecture

17. List some stereotype annotations. What are the differences between these?

18. How would you declare which HTTP requests you’d like a controller to process?

19. What is the difference between @RequestMapping and @GetMapping?

20. How to declare the data format your controller expects from requests or will create in responses?

22. How would you extract query and path parameters from a request URL in your controller?

23. What concerns is the controller layer supposed to handle vs the service layer?

24. How would you specify HTTP status codes to return from your controller?

25. How do you handle exceptions thrown in your code from your controller? What happens if you don’t set up any exception handling?

26. How would you consume an external web service using Spring?

27. What are the advantages of using RestTemplate?

### Spring AOP

28. What is “aspect-oriented programming”? Define an aspect.

29. Give an example of a cross-cutting concern you could use AOP to address

30. Define the following:

- Join point
- Pointcut
- Advice

31. What are the different types of advice? What is special about the @Around advice? How is the ProceedingJoinPoint used?

32. Explain the pointcut expression syntax

33. What visibility must Spring bean methods have to be proxied using Spring AOP?

### Spring Data

34. What is Spring ORM and Spring Data?

35. What is the Template design pattern and what is the JDBC template?

36. What does @Transactional do? What is the PlatformTransactionManager?

37. What is a PersistenceContext?

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