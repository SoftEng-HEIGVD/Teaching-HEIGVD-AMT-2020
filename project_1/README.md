# A simple version of Stack Overflow

The goal of this project is to build a basic version of the famous website, which allows a community of users to ask questions, provide answers and build up a reputation over time. Obviously, we do not have the time to implement every feature provided on the site, but we should at least:

* **Allow anonymous users to browse the list of questions and answers**. Because we hope to be successful, we have to make sure that our UI can cope with large amounts of data (hence we have to use pagination).
* **Allow anonymous users to register with our service, and later on to login**. One thing we will pay attention to is where we should define the rules that define what a "strong" password is.
* Allow connected users to ask **questions**.
* Allow connected users to provide **answers** to questions.
* Allow connected users to add **comments** to both questions and answers.
* Allow connected users to **vote** both for questions and comments. One could think about **different rules** here (can people vote several times for the same question? can people vote for their own questions? can votes go below zero?). Here, we will ask you to define your rules and document them in automated tests (so that they are not only documented, but also enforced). Something that we will also pay attention to is that the application **behaves correctly under load** (e.g. what happens if the same user find a votes at the same time?).
* Allow connected users to update their personal information on a **profile page**.
* Give some **statistics** (number of registered users, number of questions, etc.) to the users.
* Ideally, there should be a mechanism for efficiently **navigating the large amount of information**. Is it a search function? Is it a tagging mechanism? We are not going to give precise guidelines, it is up to you to put paillettes in our lives.

## Constraints

* We want to implement this application by applying the **MVC pattern on the server side**. In other words, we do not want to build a single-page app, even if it tempting to use Vue.js or React.
* We want to implement the application by **using some of the Java EE APIs directly** (Servlets, JSPs, JSTL, JDBC). In other words, we do not want to use higher-level frameworks, even if it is tempting to use Spring Boot and Hibernate.
* We want to **pay special attention to the structure of the code base**. We want to ensure that the **tiers are well separated**. We also want to ensure that the **code is easy to navigate and to read** (always keep in mind that you are writing code that other people will need to maintain! In this case, keep in mind that you will need to come back to the codebase at the end of the semester). 
* It is not easy to get the "right" structure at the start of the project. It is normal to constantly refactor the code to improve its structure and quality. Having **automated tests** to protect us during **refactoring** phases is also something we want to practice in this project.

## Tools

* **The first week**, we will use a traditional, **full-fledged Jakarta EE application server** (you can work with **Payara**, **Wildfly** or **Tomee**). The goal is for you to realize that with this type of platforms, there are "containers" in which we deploy applications. When we work with full-fledged application servers, this is obvious. We see an admin console. We have an explicit deployment operation (as shown in the Bootcamp webcasts). 
* In **the second week**, we will **transition to a more modern developer toolset and workflow** (which is geared to towards the use of containers). We will use **Open Liberty**, which provides a Jakarta EE implementation, but in an "embedded" mode. The application server will disappear behind the scenes. We will not have an admin console anymore. The deployment process will be "hidden" between 1-2 lines in your pom.xml and Dockerfile. The point is for you to always remember that the components that you develop (servlets, business services, etc.) are still executed in a "managed environment" where "something" augments your code, intercepts method calls, etc. These are all notions that we will see in the course, but that you will benefit from when writing the code.
* We will use a number of different test tools, for different purposes. Of course, we will use **JUnit**, but also **Mockito**, **JMeter**, **CodeceptJS** and **ArchUnit**.

## What will happen at the end of the semester?

When we have completed this project, and the second one (the gamification engine), we will come back to this project. Whenever the user performs a meaningful task (ask a question, provide an answer, add a comment, vote, etc.), we will **notify the gamification engine**. The rules configured in the gamification engine will update the reputation data of the impacted users (think badges, points, etc.). This project will then also **query the gamification engine** to retrieve reputation information (hall of fame, evolution of points over time, badges, etc.) and present it in existing/new pages.