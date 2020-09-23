# Welcome to AMT 2020



## This Week

* **Objectives**

  * Be able to explain what it means for a component to be "managed" and by "what" components are managed.
  * Be able to explain what dependency injection means in object-oriented programming.
  * Be able to explain how dependency injection can be implemented "from scratch". See https://github.com/SoftEng-HEIGVD/Teaching-HEIGVD-AMT-Dependency-Injection
  * Be able to explain how dependency injection is implemented in the Java EE / Jakarta EE platform.
  * Be able to explain what Aspect Oriented Programming (AOP) is.
  * Be able to explain the relationship between AOP, managed components and dependency injection.

* **Project**

  * Replace Payara / Wildfly with Open Liberty, a modern implementation of Jakarta EE (see [this webcast](https://www.youtube.com/watch?v=fJI_9VArhtY&list=PLfKkysTy70QZe0fhUhZmR64ZPUIFpN4MJ&index=1&t=733s))
  * Study the reference architecture described in [this](https://www.youtube.com/watch?v=Yr7OeHtefvQ&list=PLfKkysTy70QZe0fhUhZmR64ZPUIFpN4MJ&index=3) and [this](https://www.youtube.com/watch?v=SW9YFmC_va0&list=PLfKkysTy70QZe0fhUhZmR64ZPUIFpN4MJ&index=4) webcast, which provides the overall structure for your application across all tiers.
  * Reuse the code you wrote during the first week.
  * Make sure that your CodeceptJS tests still work and extend them.
  * Implement a new feature (users can ask questions)
  * Implement a first continuous integration pipeline with GitHub Actions (build and publish a Docker image as described in [this webcast](https://www.youtube.com/watch?v=jrTIZBMmqhI&list=PLfKkysTy70QZe0fhUhZmR64ZPUIFpN4MJ&index=2&t=8s)).

* **The Question of the Week**: 

  * *Expliquez comment les Enterprise Java Beans (EJBs) permettent d'appliquer les principes de la programmation orientée aspects (AOP). Appuyez-vous sur un exemple de code et expliquez en détails ce qui se passe "derrière les décors" (i.e. expliquez ce que le serveur d'application fait).*

* **Repos**

  * Here is the repo for the first Java EE demo: https://github.com/SoftEng-HEIGVD/Teaching-HEIGVD-AMT-Discovery

* **Notes about the YouTube Playlist:**

  * I have added 4 videos (see the links in the Project paragraph just above).

  

## Semester Planning

#### Week 1 (14.09.2020)

* Introduction to multi-tiered architectures
* Introduction to the Java EE / Jakarta EE platform and its evolution of the last 20 years
* The MVC design pattern
* Here is the repo for the first Java EE / Jakarta EE demo: https://github.com/SoftEng-HEIGVD/Teaching-HEIGVD-AMT-Discovery
* Here is the repo for the second demo (MVC): https://github.com/SoftEng-HEIGVD/Teaching-HEIGVD-AMT-MVC-simple-example. The README.md provides instructions for configuring IntelliJ and a local app server.
* *Project: you have a first basic prototype of an application, which you can deploy in a Jakarta EE application server (e.g. Payara). The application allows the user to navigate between the (empty) pages of your future application. There is a working registration / login page, which is backed by in-memory datastore. You have learned how to do end-user acceptance testing with CodeceptJS.*

#### Week 2 (21.09.2020)

* The notion of managed component
* Dependency injection
* Aspect Oriented Programming (AOP)
* *Project: you have replaced the full Jakarta EE server with an embedded container (OpenLiberty), which you will use for the rest of project 1. You have an efficient development environment workflow, with IDE, Debugger and build pipeline (producing Docker images of your application). After registration and login, the user can ask questions. These features are protected with end-user acceptance tests.*

#### Week 3 (28.09.2020)

* Addressing the "It works on my machine" syndrome with load testing
* Persistence with JDBC
* *Project: you have moved from in-memory data stores to a RDMBs. You have performance / load tests for several use cases of your application. You have a Docker Compose topology for your application, with (at least) a database container.*

#### Week 4 (05.10.2020)

* Reflection
* Persistence with JPA
* *Project: users can add comments on questions and answers. You have unit / integration tests that validate the rules that govern these features (e.g. who has the right to add / edit / remove a comment?)*

#### Week 5 (12.10.2020)

* Both sessions reserved for project work
* *Project: users can vote for questions and answers. You have unit / integration tests that validate the rules that govern these features (e.g. who has the right to vote on what? how many times?). You have end-user acceptance tests for all uses cases. You have load tests to validate the behavior of your application under concurrency. In particular, you have validated that it is not possible to loose votes under load.*



### AUTUMN BREAK 



#### Week 6 (26.10.2020)

* **Monday: code freeze for project 1**
* **Wednesday: written test 1**
* **Friday: demonstration of project 1**

#### Week 7 (02.11.2020)

* The design of REST APIs
* Document REST APIs with Swagger / Open APIs
* Introduction to Spring Boot
* *Project: you have a first skeleton of the gamification engine, based on Spring Boot. You have specified the /events endpoint, used to report user activity with POST requests. You do have to persist the events yet. You have JMeter scripts to exercise load on the endpoint. You have Cucumber BDD tests to specify and validate the behaviour of the endpoint.*

#### Week 8 (09.11.2020)

* Introduction to Spring Boot
* Introduction to Spring Data
* *Project: you have introduced the notion of "application" (your gamification engine is used to gamify several applications, so you need to process API calls in the context of a specific application). You have introduced the notion of "end-user". It is possible to register an application, get an API key. It is possible to send a stream of end-user events to the engine and thanks to the API key to make the correct associations. It is possible to get information about end-user via the REST API.*

#### Week 9 (16.11.2020)

* Monoliths and micro services
* *Project: you have introduced a simple rule system. The user of your gamification engine (i.e. the developer of the gamified application) can specify how reputation points are awarded for different end-user events. You have implemented a number of queries to benefit from this information and made them available via the REST API (e.g. it is possible to get the reputation of one end-user, to get the top-10 end-users, to get the evolution of the reputation for one end-user over time).*

#### Week 10 (23.11.2020)

* CQRS & event sourcing
* *Project: you have extended the rule system. The user of your gamification engine can specify how badges are awarded for different end-user events. You have extended your set of queries to make this information available via the REST API.*

#### Week 11 (30.11.2020)

* Both sessions reserved for project work
* *Project: you have a complete system. You have automated tests to validate end-to-end scenarios: several app developers can register their app with the gamification engine. They can create rules to setup their reputation system. The activity of end-users within the different applications is streamed to the gamification engine, which applies the configured rules. Application developers have access to the reputation of their users. You have load tests to validate that the system works correctly under concurrency.*

#### Week 12 (07.12.2020)

* **Monday: code freeze for project 2**
* **Wednesday: written test 2**
* **Friday: demonstration of project 2**

#### Week 13 (14.12.2020)

* Recap and guidelines for the end of the semester



### CHRISTMAS BREAK 



#### Week 14 (04.01.2020)

* Putting names to what we have put in practice: hexagonal architecture, clean architecture, onion architecture, domain driven design, the test pyramid
* Review of key concepts: separation of concerns, Aspect Oriented Programming, dependency injection, inversion of control, etc.
* *Project: you have created a complete system, where your first project uses the your second project to gamify the experience of people who ask questions and provide answers. The application that you developed at the beginning of the semester makes calls to the REST API that you have developed in the second part of the semester.*

#### Week 15 (11.01.2020)

* **Wednesday: written test 3**
* *Project: your gamified application makes calls to your gamification engine to retrieve reputation information and present it in its user interface (e.g. the hall of fame is displayed on the home page, statistics are displayed on the profile page).*

#### Week 16 (18.01.2020)

* **Wednesday: demonstration of project 3**

* **Friday: demonstration of project 3**

#### 

## Resources

* The [**companion book**](https://github.com/SoftEng-HEIGVD/Teaching-HEIGVD-AMT-Book) (work in progress, you will have content for the first part of the semester).
* The [AMT 2020 YouTube Playlist](https://www.youtube.com/playlist?list=PLfKkysTy70Qagym3yvAgf-vvsTnOQjgZz)
* Frameworks and tools:
  * Jakarta ee specs and application servers
    * https://jakarta.ee
    * https://microprofile.io
    * https://openliberty.io
    * https://www.payara.fish
    * https://www.wildfly.org
    * https://tomee.apache.org
  * Spring ecosystem
    * https://spring.io/projects/spring-boot
    * https://spring.io/projects/spring-data
    * https://spring.io/projects/spring-data-jpa
  * API design and documentation
    * https://swagger.io/specification
  * Testing
    * https://codecept.io
    * https://cucumber.io
    * https://jmeter.apache.org



