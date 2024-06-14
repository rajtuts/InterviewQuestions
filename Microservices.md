**1. Core Concepts in Microservices**
1. Cohesion
2. Coupling
3. Immutability in Microservices
4. Open/Close Principle
5. DRY (Don’t Repeat Yourself)
6. SOLID
7. Single Responsibility Principle
8. 8 Fallacies of Distributed Computing
9. Continuous Integration (CI)
10. CAP Theorem
11. 12 Factor App
12. Typical Git workflow for a real project

**2. Introduction to Microservices**
1. Characteristics of a microservices architecture
2. Benefits of using Microservices Architecture
3. Challenges in Microservices
4. Difference between Microservices and SOA

**Microservices**
3. Microservices Interview Questions
1. How will you define Microservices Architecture?
2. What is Domain Driven Design?
3. What is Bounded Context?
4. What is polyglot persistence? Can this idea be used in monolithic applications as well?
5. Why Microservices are better than Monoliths?
6. Isn’t in process communication in monolithic application faster than tons of remote network calls in microservices architecture?
7. How microservices are different than SOA?
8. What is difference between small-services and microservices?
9. What are benefits of using microservices architecture?
10. How to partition a large application into microservices architecture, correctly?
11. How big a single microservice should be?
12. How do microservices communicate with each other?
13. What shall be preferred communication style in microservices: synchronous or asynchronous?
14. What is difference between Orchestration and Choreography in microservices context?
15. How to maintain ACID in microservice architecture?
16. How frequent a microservice be released into production?
17. How to achieve zero-downtime during the deployments?
18. How to achieve zero downtime deployment(blue/green) when there is a database change?
19. How to slowly move users from older version of application to newer version?
20. How will you monitor fleet of microservices in production?
21. How will you troubleshoot a failed API request that is spread across multiple services?
22. What are different layers of a single microservice?
23. How will you develop microservices using Java?
24. Is it a good practice to deploy multiple microservices in a single tomcat container (servlet container)?
25. What are Cloud Native applications?
26. What is Spring Boot?
27. What is Spring Cloud?
28. What is difference between application.yml and bootstrap.yml?
29. How will you implement service discovery in microservices architecture?
30. How does Eureka Server work?
31. How to externalize configuration in a distributed system?
32. How will you use config-server for your development, stage and production environment?
33. What is difference between config first bootstrap and discovery first bootstrap in context of Spring Cloud Config client?
34. How to halt a Spring Boot based microservice at startup if it can not connect to Config Server during bootstrap?
35. How to refresh configuration changes on the fly in Spring Cloud environment?
36. How to achieve client side load balancing in Spring Microservices using Spring Cloud?
37. How to use client side load-balancer Ribbon in your microservices architecture?
38. How to use both LoadBalanced as well as normal RestTemplate object in the single microservice?
39. How will you make use of Eureka for service discovery in Ribbon Load Balancer?
40. Can we use Ribbon without eureka?
41. How will you use ribbon load balancer programmatically?
42. What is difference between @EnableEurekaClient and @EnableDiscoveryClient?
43. How to make microservices zone aware so as to prefer same zone services for interservice communication using Spring Cloud?
44. How to list all instances of a single microservice in Spring Cloud environment?
45. What is API Gateway?
46. How to protect internal endpoints leaking from API Gateway?
47. How to protect Sensitive Security Tokens from leaking into downstream system?
48. How to retry failed requests at some other available instance using Client Side Load Balancer?
49. What is Circuit Breaker Pattern?
50. What are Open, Closed and Half-Open states of Circuit Breaker?
51. What are use-cases for Circuit Breaker Pattern?
52. What are benefits of using Circuit Breaker Pattern?
53. Can circuit breaker be used in asynchronous communication?
54. What is Hystrix?
55. What are main features of Hystrix library?
56. How to use Hystrix for fallback execution?
57. When not to use Hystrix fallback on a particular microservice?
58. How will you ignore certain exceptions in Hystrix fallback execution?
59. What is Strangulation Pattern in microservices architecture?
60. What is Circuit Breaker?
61. What is difference between using a Circuit Breaker and a naive approach where we try/catch a remote method call and protect for failures?
62. What is Request Collapsing feature in Hystrix?
63. What is difference between Circuit Breaker and Hystrix?
64. Where exactly should i use Circuit Breaker Pattern?
65. What is bulkhead design pattern?
66. How does Hystrix implements Bulkhead Design Pattern?
67. What is Hystrix approach to Bulkhead Pattern?
68. In microservices architecture, what are smart endpoints and dumb pipes?
69. What is difference between Semaphore and ThreadPool based configuration in Hystrix?
70. How to handle versioning of microservices?
71. What is difference between partitioning microservices based on technical capabilities vs business capabilities? Which one is better?
72. Running Spring boot app at different port on server startup
73. How will you run certain business logic at the app startup?
74. How to correctly implement a reporting microservice in a distributed system?
75. What is Event Sourcing and CQRS? When should it be used? Should be use it for the entire system?
76. How to send business errors from a RESTful microservice to client application?
77. Is it a good idea to share common database across multiple microservices?
78. How will you make sure that the email is only sent if the database transaction does not 89 fail?
79. How will you atomically update the database and publish an event to message broker from single transaction?
80. How will you propagate security context of user when one microservice calls another microservice on behalf of user?
81. What is Token Relay in Spring Security?
82. How to Enable Token Relay?
83. How to revoke Access and Refresh Tokens on data breach to limit the damage?
84. Shall Authentication and Authorization be one service?
85. What is API Key security?
86. What are best practices for microservices architecture?
87. Shall we share common domain models or DTOs across microservices?
88. How to share common code across multiple microservices?
89. What is continuous delivery?
90. How will you improve the performance of distributed system?
91. How will you implement caching for microservices?
92. Which protocol is generally used for client to service and inter-service communication?
93. What are advantages of using asynchronous messaging within microservices architecture?
94. What is good tool for documenting Microservices?
95. How will you integrate Swagger into your microservices?
96. What are common properties for a Spring Boot project?

**4. Security in Microservices**
1. Why Basic Authentication is not suitable in Microservices Context?
2. Why OAuth2?
3. How OAuth2 Works?
4. What are different OAuth2 Roles?
5. What are different OAuth 2.0 grant types (OAuth flows)?
6. When shall I use resource owner credentials?
7. When shall I use Authorization Code grant?
8. When shall I use client credentials?
9. OAuth2 and Microservices
10. What is JWT?
11. What are usecases for JWT?
12. How does JWT looks like?
13. What is AccessToken and RefreshToken?
14. How to use a RefreshToken to request a new AccessToken?
15. How to call the protected resource using AccessToken?
16. Can a refreshToken be never expiring? How to make refreshToken life long valid?
17. Generate AccessToken for Client Credentials
18. Why there is no RefreshToken support in Oauth2 Client Credentials workflow?
19. How to implement the Logout functionality using JWT?
20. Security in inter-service communication
21. How to setup multiple authentications in Spring Security?
22. What is purpose of @EnableResourceServer?
23. What is purpose of @EnableOAuth2Sso?
24. What is purpose of @EnableOAuth2Client?
25. How can we add custom claims to JWT AccessToken?
26. Security Best Practices
27. How to enable spring security at service layer?
