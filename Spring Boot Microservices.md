**Spring Core Framework**
1. What is the Spring framework? Why should Java programmers use the Spring framework?
2. What is the Dependency Injection design pattern?
3. What is the Inversion of Control concept, how does Spring support IOC?
4. How do you configure Spring Framework?
5. Can we use more than one configuration file for our Spring project?
6. What types of dependency injection are supported by Spring Framework? When do you use Setter and Constructor Injection, the pros and cons? 
7. Difference between the setter and constructor injection in Spring? 
8. Difference between Factory Pattern and Dependency Injection in Java?
9. What are the different modules in spring? 
10. What is the difference between Spring MVC and Spring core? 
11. What is AOP? How is it implemented in Spring? 
12. What is Advice in AOP? 
13. What are the joint Point and point cut? 
14. What is component scanning in Spring Framework? 

**Container, Dependency, and IOC**
1. What is dependency injection and what are the advantages of using it? 
2. What is an interface and what are the advantages of making use of them in Java? 
3. What is an ApplicationContext in Spring? 
4. How are you going to create a new instance of an ApplicationContext? 
5. Can you describe the lifecycle of a Spring Bean in an ApplicationContext? 
6. How are you going to create an ApplicationContext in an integration test? 
7. What is the preferred way to close an application context? Does Spring Boot do this for you? 
8. What is Dependency injection using Java configuration? 
9. What is Dependency injection using annotations (@Autowired)?–Component scanning, Stereotypes?–Scopes for Spring beans? 
10. What is the default scope? 
11. Are beans lazily or eagerly instantiated by default? How do you alter this behavior?
12. What is a property source? How would you use @PropertySource? 
13. What is a BeanFactoryPostProcessor and what is it used for? When is it invoked? 
14. Why would you define a static @Bean method when creating your own BeanFactoryPostProcessor? 
15. What is a PropertySourcesPlaceholderConfigurer used for? 
16. What is a BeanPostProcessor and how is it different to a BeanFactoryPostProcessor? What do they do? When are they called? 
17. What is an initialization method and how is it declared on a Spring bean?
18. What is a destroy method, how is it declared and when is it called? 
19. Consider how you enable JSR-250 annotations like @PostConstruct and @PreDestroy? When/how will they get called?
20. How else can you define an initialization or destruction method for a Spring bean?
21. What does component-scanning do? 
22. What is the behavior of the annotation @Autowired with regards to field injection, constructor injection and method injection? 
23. How does the @Qualifier annotation complement the use of @Autowired? 
24. What is a proxy object and what are the two different types of proxies Spring can create? 
25. What are the limitations of these proxies (per type)? 
26. What is the power of a proxy object and where are the disadvantages? 
27. What is the difference between @Autowired and @Inject annotation in Spring? 

**Spring Bean Lifecycle **
1. What is a bean in Spring Framework? 
2. What is the default scope of bean in the Spring framework? 
3. Do Spring singleton beans are thread- safe? 
4. What is the difference between a singleton and prototype bean? 
5: Explain the Spring Bean-LifeCycle? 
6. What is Bean Factory, have you used XMLBeanFactory? 
7. What is the difference between ApplicationContext and BeanFactory in Spring framework? 
8. What does the @Bean annotation do in Spring? 
9. What is the default bean id if you only use @Bean? 
10. How can you override this? 
11. Why are you not allowed to annotate a final class with @Configuration? 
12. How do @Configuration annotated classes support singleton beans? 
13. Why can’t @Bean methods be final either? 
14. How do you configure profiles? 
15. What are possible use cases where they might be useful? 
16. Can you use @Bean together with @Profile? 
17. Can you use @Component together with @Profile annotation? 
18. How many profiles can you have? 
19. How do you inject scalar/literal values into Spring beans? 
20. What is @Value used for? 
21. What is Spring Expression Language (SpEL for short)? 
22. What is the Environment abstraction in Spring? 
23. Where can properties in the environment come from? 
24. What can you reference using SpEL? 
25. What is the difference between $ and # in @Value expressions? 

**Aspect Oriented Programming (AOP) **
1. What is the concept of AOP? 
2. Which problem AOP solves? 
3. What is a cross-cutting concern? 
4. Can you name three typical cross-cutting concerns? 
5. What two problems arise if you don’t solve a cross-cutting concern via AOP? 
6. What is a pointcut, a join point, advice, an aspect, weaving? 
7. How does Spring solve (implement) a cross-cutting concern? 
8. What are the two proxy-types used in Spring AOP? 
9. What are the limitations of the two proxy-types used in Spring AOP? 
10. What visibility must Spring bean methods have to be proxied using Spring AOP?
11. How many advice types do Spring support? Can you name each one? 
11. What are they used for? 
12. Which types of advice you can use to try and catch exceptions? 
13. What is the JoinPoint argument used for? 
15. What is a ProceedingJoinPoint? Which advice type is it used with? 
16. Can you name some popular Aspect-oriented programming libraries?
17. What are the different types of Weaving which is available in AOP? 

**Spring MVC **
1. MVC is an abbreviation for a design pattern. What does it stand for and what is the idea behind it? 
2. Do you need spring-mvc.jar in your classpath or is it part of spring-core? 
3. What is the DispatcherServlet and what is it used for? 
4. Is the DispatcherServlet instantiated via an application context? 
5. What is the root application context in Spring MVC? How is it loaded? 
6.What is the @Controller annotation used for? How can you create a controller without an annotation? 
7. What is the ContextLoaderListener and what does it do? 
8. What are you going to do in the web.xml? Where do you place it? 
9. How is an incoming request mapped to a controller and mapped to a method? 
10. What is the @RequestParam used for? 
11. What are the differences between @RequestParam and @PathVariable?
12. What are some of the valid return types of a controller method? 
13. What is a View and what’s the idea behind supporting different types of View? 
14. How is the right View chosen when it comes to the rendering phase? 
15. What is the Model in Spring MVC Framework? 
16. Why do you have access to the model in your View? Where does it come from? 
17. What is the purpose of the session scope? 
18. What is the default scope in the web context? 
19. Why are controllers testable artifacts? 
20. What does the InternalResourceViewResolver do? 
21. What is Spring MVC? Can you explain How one request is processed? 
22. What is the ViewResolver pattern? how it works in Spring MVC 
23. Explain Spring MVC flow with a simple example like starting from Container receives a request and forward to your Java application? 
24. If a user checked in CheckBox and got a validation error in other fields and then he unchecked the CheckBox, what would be the selection status in the command object in Spring MVC? How do you fix this issue? 
25. What are the different implementations of the View interface you have used in Spring MVC? 
26. What is the use of DispatcherServlet in Spring MVC? 
27. What is the role of InternalResourceViewResolver in Spring MVC 
28. Difference between @RequestParam and @PathVariable in Spring MVC? 
29. Difference between @Component, @Service, @Controller, and @Repository annotations in Spring MVC?

**REST **
1. What does REST stand for?
2. What is a resource?
3. What are safe REST operations?
4. What are idempotent operations? Why is idempotency important?
5. Is REST scalable and/or interoperable?
6. What are the advantages of the RestTemplate?
7. Which HTTP methods does REST use?
8. What is an HttpMessageConverter in Spring REST?
9. How to create a custom implementation of HttpMessageConverter to support a new type of request/response?
10. Is REST normally stateless?
11. What does @RequestMapping annotation do?
12. Is @Controller a stereotype? Is @RestController a stereotype?
13. What is the difference between @Controller and @RestController?
14. When do you need @ResponseBody annotation in Spring MVC?
15. What does @PathVariable do in Spring MVC? Why is it useful in REST with Spring?
16. What is the HTTP status return code for a successful DELETE statement?
17. What does CRUD mean?
18. Where do you need @EnableWebMVC annotation?
19. When do you need @ResponseStatus annotation in Spring MVC?
20. Is REST secure? What can you do to secure it?
21. Does REST work with transport layer security (TLS)?
22. Do you need Spring MVC in your classpath for developing RESTful Web Service?

**Spring Boot Intro **
1. What is Spring Boot? Why should you use it?
2. What is the advantage of using Spring Boot? 
3. What is the difference between Spring Boot and Spring MVC?
4. What is the difference between Core Spring and Spring Boot?
5. What are some important features of using Spring Boot?
6. What is auto-configuration in Spring boot? How does it help? Why is Spring Boot called opinionated?
7. What is starter dependency in Spring Boot? How does it help?
8. What is the difference between @SpringBootApplication and @EnableAutoConfiguration annotation?
9. What is Spring Initializer? why should you use it?
10. What is a Spring Actuator? What are its advantages?
11. What is Spring Boot CLI? What are its benefits? 
12. Where do you define properties in Spring Boot application?
13. Can you change the port of the Embedded Tomcat server in Spring boot? If Yes, How?
14. What is the difference between an embedded container and a WAR?
15. What embedded containers does Spring Boot support?
16. What are some common Spring Boot annotations?
17. Can you name some common Spring Boot Starter POMs?
18. Can you control logging with Spring Boot? How?
19. Difference between @SpringBootApplication and @EnableAutoConfiguration annotations in Spring Boot?
20. What is the difference between @ContextConfiguration and @SpringApplicationConfiguration in Spring Boot Testing?
21. Where does Spring Boot look for application.properties file by default?
22. How do you define profile specific property files?

**Spring Boot Auto Configuration **
1. What is Spring Boot auto-configuration?
2. How does auto-configuration work? How does it know what to configure?
3. What are some common Spring Boot annotations?
4. What does @EnableAutoConfiguration annotation do?
5. How does Spring Boot auto-configuration works?
6. What does @SpringBootApplication do?
7. Does Spring Boot do component scanning? Where does it look by default?
8. How are DataSource and JdbcTemplate auto-configured?
9. What is the purpose of spring.factories?
10. How do you customize Spring Boot auto configuration?
11. How to create your own auto-configuration in Spring Boot?
12. What are the examples of @Conditional annotations? How are they used?

**Spring Boot Starter **
1. What is starter dependency in Spring Boot? What is the advantage of it?
2. How do you define properties in Spring Boot? Where?
3. What does @SpringBootApplication annotation do?
4. What things affect what Spring Boot sets up?
5. What does spring boot starter web include?
6. Can you make your own custom starter dependency?
7. What are some common Spring Boot Starter dependencies? Can you name a few?
8. How do you add a Spring boot starter in your project?
9. Which Spring Boot starter will you add to enable Spring boot testing and relevant libraries?
10. What is Spring Boot Starter Parent? 

**Spring Boot Actuator **
1. What is the Spring Boot Actuator?
2. What are the different ways Actuator provides to gain insight into a Spring Boot application?
3. Why do you need to secure Spring Boot Actuator’s endpoints?
4. How do you secure the Spring Boot Actuator’s endpoint to restrict access?
5. What value does Spring Boot Actuator provide?
6. What are the two protocols you can use to access actuator endpoints?
7. What are the actuator endpoints that are provided out of the box?
8. What is the info endpoint for? How do you supply data?
9. How do you change the logging level of a package using the logger’s endpoint?
10. How do you access an endpoint using a tag? 
11. What are metrics for?
12. How do you create a custom metric?
13. What is a Health Indicator in Spring Boot? 
14. What are the Health Indicators that are provided out of the box?
15. What is the Health Indicator status?
16. What are the Health Indicator statuses that are provided out of the box?
17. How do you change the Health Indicator status severity order?

**Spring Boot CLI**
1. What is Spring Boot CLI?
2. Can you write a Spring application with Groovy?
3. What are the main advantages of the Spring Boot command-line interface (CLI)?
4. What does @Grab annotation do? When to use this?
5. What is Spring Initializer?
6. How does Spring Boot CLI resolve dependencies?

**Spring Testing**
1. How to define a testing class in Spring?
2. Which starter package do you need to test the spring boot application?
3. What type of tests typically use Spring?
4. What are the three common Spring boot test annotations?
5. How can you create a shared application context in a JUnit integration test?
6. When and where do you use @Transactional in testing?
7. How are mock frameworks such as Mockito or EasyMock used in Spring Boot?
8. How is @ContextConfiguration used in Spring Boot?
9. How does Spring Boot simplify writing tests?
10. What does @SpringBootTest do? How does it interact with @SpringBootApplication and @SpringBootConfiguration?
11. When do you want to use @SpringBootTest annotation?
12. What does @SpringBootTest auto-configure?
13. What dependencies does the spring-boot-starter-test bring to the classpath?
14. How do you perform integration testing with @SpringBootTest for a web application?
15. When do you want to use @WebMvcTest? What does it auto-configure?
16. What are the differences between @MockBean and @Mock annotations?
17. When do you want @DataJpaTest for? What does it auto-configure?
18. What is the use of @DirtiesContext annotation while Testing Spring Boot application?
19. What is the difference between @ContextConfiguration and @SpringApplicatoinConfiguration in Spring Boot testing?
20. What is the difference between @ContextConfiguration and @SpringBootTest?

**Data Management And JDBC**
1. What is the difference between checked and unchecked exceptions?
2. Why does Spring prefer unchecked exceptions?
3. What is the Spring data access exception hierarchy?
4. How do you configure a DataSource in Spring?
5. What is the Template design pattern and what is the JDBC template?
6. What is a callback?
7. What are the JdbcTemplate callback interfaces that can be used with queries?
8. What is each used for? (You would not have to remember the interface names in the exam, but you should know what they do if you see them in a code sample).
9. Can you execute a plain SQL statement with the JDBC template?
10. When does the JDBC template acquire (and release) a connection, for every method called or once per template? Why?
11. How do the JdbcTemplate support queries?
12. How does it return objects and lists/maps of objects?
13. What is a transaction? What is the difference between a local and a global transaction?
14. Is a transaction a cross-cutting concern? How is it implemented by Spring?
15. How are you going to define a transaction in Spring?
16. What does @Transactional do?
17. What is the PlatformTransactionManager?
18. Is the JDBC template able to participate in an existing transaction?
19. What is @EnableTransactionManagement for?
20. How does transaction propagation work? 
21. What happens if one @Transactional annotated method is calling another @Transactional annotated method inside the same object instance?
22. Where can the @Transactional annotation be used?
23. What is a typical usage if you put it at the class level?
24. What does declarative transaction management mean?• What is the default rollback policy? How can you override it?
25. What is the default rollback policy in a JUnit test, when you use the @RunWith(SpringJUnit4ClassRunner.class) in JUnit 4 or @ExtendWith(SpringExtension.class) in JUnit 5, and annotate your @Test annotated method with @Transactional?

**Spring Data JPA**
1. What is JPA? 
2. What are some advantages of using JPA? 
3. What is the Spring data repository? 
4. What is the naming convention for finder methods in the Spring data repository interface? 
5. Why is an interface not a class? 
6. Can we perform actual tasks like access, persist, and manage data with JPA? 
7. How can we create a custom repository in Spring data JPA? 
8. What is PagingAndSortingRepository? 
9. What is @Query used for? 
10. Give an example of using @Query annotation with JPQL. 
11. Can you name the different types of entity mapping. 
12. Define entity and name the different properties of an entity. 
13. What is PlatformTransactionManager? 
14. How can we enable Spring Data JPA features? 
15. Differentiate between findById() and getOne(). 
16. Are you able to participate in a given transaction in Spring while working with JPA?
17. Which PlatformTransactionManager(s) can you use with JPA?
18. What do you have to configure to use JPA with Spring? How does Spring Boot make this easier?
19. How are Spring Data JPA Repositories implemented by Spring at runtime?
20. What type of transaction Management Spring support?
21. How do you call a stored procedure by using the Spring framework?
22. What do the JdbcTemplate and JmsTemplate class offer in Spring? 

**Spring Cloud **
1. Explain Spring cloud? or, What is Spring Cloud? 
2. What are the common features of Spring cloud? 
3. Explain load balancing? or What is load balancing? 
4. How load balancing is implemented in Spring cloud? 
5. What is the meaning of Service registration and discovery? 
6. What is Hystrix? 
7. Explain Netflix feign? Or What is Netflix feign?
8. Why do we use Netflix feign?
9. What is the use of the Spring cloud bus?
10. What are the advantages of Spring cloud?
11. What is PCF? 
12. What is the purpose of the Hystrix circuit breaker?
13. Name the services that provide service registration and discovery.
14. Give the benefits of Eureka and Zookeeper?
15. What is the major difference between Spring Cloud and Spring boot?
16. What are some common Spring cloud annotations?

**Spring Security**
1. Spring Security Basics Interview questions 
1. What is Spring Security? 
2. What is the delegating filter proxy in Spring Security? 
3. What are some restrictions on using delegating filter proxy in Spring security?
4. Do Filter’s life-cycle methods like init() and destroy() will be a delegate to the target bean by DelegatingFilterProxy?
5. Who manages the life-cycle of filter beans in Spring? 
6. What is the security filter chain in Spring Security? 
7. What are some predefined filters used by Spring Security? What are their functions and in which order they occurred? 
8. Can you add custom filters in Spring security’s filter chain? 
9. How to implement a custom filter in Spring Security? 
10. How to add a custom filter into the Spring Security filter chain? 
11. Is security a cross-cutting concern? How is it implemented internally? 
12. What does @ and # is used for in Spring Expression Language (EL)? 
13. Which security annotations are allowed to use SpEL? 
14. What is a security context in Spring? 
2. Spring Security Authentication and Authorization Interview Questions 
15. What are authentication and authorization? Which must come first? 
16. What is a Principal in Spring Security? 
17. Why do you need the intercept-url? 
19. Is it enough to hide sections of my output (e.g. JSP-Page)? 
20. What type of object is typically secured at the method level (think of its purpose, not its Java type). 
21. In which order do you have to write multiple intercept-urls? 
22. What do @Secured and @RolesAllowed do? What is the difference between them? 
3. Spring Security Password Encoding questions
23. Does Spring Security support password hashing? What is salting?
24. What is PasswordEncoder?
25. What are some implementations of PasswordEncoder in Spring Security?
26. How do you control concurrent Sessions on Java web applications using Spring Security?
27. How do you set up LDAP Authentication using Spring Security?
28. How to implement Role-Based Access Control (RBAC) using Spring Security? 
