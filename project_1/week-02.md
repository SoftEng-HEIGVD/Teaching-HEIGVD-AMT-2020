# Week 2

> You have replaced the full Jakarta EE server with an embedded container (OpenLiberty), which you will use for the rest of project 1. You have an efficient development environment workflow, with IDE, Debugger and build pipeline (producing Docker images of your application). After registration and login, the user can ask questions. These features are protected with end-user acceptance tests.*

Suggested planning, assuming a group of 4 students:

**Time Box 1: 45 minutes**

* Everybody in the group should watch the [webcast](https://www.youtube.com/watch?v=fJI_9VArhtY&list=PLfKkysTy70Qagym3yvAgf-vvsTnOQjgZz&index=14) introducing Open Liberty () and do a setup. Everybody must have a working environment running locally.

**Time Box 2: 90 minutes**

* Everybody should at least watch this [webcast](https://www.youtube.com/watch?v=Yr7OeHtefvQ&list=PLfKkysTy70Qagym3yvAgf-vvsTnOQjgZz&index=16) and this [webcast](https://www.youtube.com/watch?v=SW9YFmC_va0&list=PLfKkysTy70Qagym3yvAgf-vvsTnOQjgZz&index=17) describing the overall application structure. Not everybody needs to write the code, but there are a lot of explanations that are important (also from a conceptual point of view, that you need to understand and know).

**Next Steps (after the lab session)**

At this point, you should have a first skeleton for your project and everybody in the team should understand how the whole thing works (at least to some level). Now, we need to build on this, but we should be able to split the work:

* **Someone needs to take the lead on setting up the application structure (4 hours)**
  * Start by creating the package structure, adapting the "Joke" use case to your project (you work with Questions, not Jokes).
  * You can basically redo what is done in the two webcasts that describe the structure.
  * As soon as the package structure is in place, commit and make this available to others. This needs to be done before the person doing the registration / login use case can work! You can use placeholder text files in the folders to be able to commit them.
* **Someone needs to take the lead on pipeline setup with GitHub Actions (4 hours)**
  * Follow the instructions in this webcast and create a pipeline for your project.
  * Make sure that at the end, it is possible for some external to the project (e.g. the assistants) to do a docker run with your image. Write down in your README.md how to do that (i.e. what is the name of your image).
* **Someone needs to bring the registration / login logic in the new structure (4 hours)**
  * Watch this [webcast](https://www.youtube.com/watch?v=k5bxeWyv3iQ) for guidelines (ask your team mates to also watch it, even if they don't do the operations or take the time to show them the code)
* **Someone needs to take the lead on the views and the  e2e testing (4 hours)**
  * As you have new pages, you will need to update your presentation layer.
  * Update your end-to-end tests and take the time to read the CodeceptJS documentation to learn about Page Objects, Actors and other patterns that will allow you to grow your test suite gracefully.



