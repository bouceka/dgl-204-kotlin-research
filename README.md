# Kotlin overview research (Micronaut) - part 1

## Kotlin Documentation

[Kotlin documentation](https://kotlinlang.org/docs/home.html) is an artifact that describes the programming language in usage. Any user, developer, or architect can read it and implement it in their projects. It also refers to other libraries that can be combined, such as GraphQL, RabbitMQ, ReactJS, etc. It provides a solid explanation of the primary usage of the language. On top of it, Kotlin documentation provides a short education walk through for users without prior knowledge.

### Target Audience

Kotlin documentation is for anyone who wants to learn the Kotlin language or refresh memory. It can happen anytime. Developers use multiple languages, and it's unlikely to remember all the syntax. Documentation is an excellent tool to have open while a developer is writing code.

## Research Overview - Micronaut

For most of my time at NIC, I have been focused on the visual aspects of apps and the Front-end. I want to approach this research from the Back-end perspective and learn more about [microservices architecture](https://microservices.io/).

### What is microservices architecture?

Before we jump on Micronaut, we should refresh what microservices are and the difference between microservices and monoliths.

### Monolith

To understand microservices, we should look at what a monolith is. If we look at ExpressJS server-side app, we would take the whole app, deploy to a NodeJs server, and build it. There we would make the entire app. All the requests would be directed to the same API address. All the features would have access to the same database.

_See in the image_

<p align="center">
<img src="./assets/monolithic.jpg" height="auto" width="700">
<p align="center"><i>Monolithic architecture</i></p>
</p>

| :white_check_mark: Advantage           | :x: Disadvantage                                                                       |
| -------------------------------------- | -------------------------------------------------------------------------------------- |
| Easy to develop (One app at one place) | A simple change can break the app if the developer doesn't understand the app as whole |
| Easy to manage (used one language)     | It is language and framework depended (must be written in one lang)                    |
| Easy to deploy                         | Growth, the bigger the app the worse the deployment is                                 |
|                                        | Traffic, if our app becomes popular. One server wont handle all the traffic.           |
|                                        | It needs to deploy another version of the app                                          |

### Microservices

We split the app into smaller independent services. A single microservice contains all the routing, middlewares, business logic, and database access required to implement **one feature** of our app. That is the biggest difference. One app is created by multiple services that interact with each other. However, all the services must be [loosely coupled](https://chrisrichardson.net/post/microservices/2020/12/14/designing-loosely-coupled-services.html).

<p align="center">
<img src="./assets/microservices.jpg" height="auto" width="700">
<p align="center"><i>Microservices architecture</i></p>
</p>

| :white_check_mark: Advantage                                      | :x: Disadvantage                                                                         |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| All services are self contained                                   | Data management between services (extremely difficult)                                   |
| If one service crashes the portion of our app will work just fine | It is difficult to design                                                                |
| Can be written in multiple languages and frameworks               | Storing data in repository (Monorepo, Polyrepo)                                          |
| Easy to scale if traffic is higher                                | Communicating between services (API Calls, Message Broker, Service Mesh)                 |
| Independently deployable                                          | [Database-per-Service](https://microservices.io/patterns/data/database-per-service.html) |

### Messaging system

For anyone who would wonder how the services communicate with each other, there is a simple diagram that illustrates that. It is a very simplified version of it. The communication works asynchronously between them due to the Event Bus. The Event Bus delegates events (API calls) between the services. In case one crashes, the other dependent service won't crash too.

<p align="center">
<img src="./assets/messaging-request.jpg" height="auto" width="450">
<p align="center"><i>Messaging system architecture (request)</i></p>
</p>
<p align="center">
<img src="./assets/messaging-response.jpg" height="auto" width="450">
<p align="center"><i>Messaging system architecture (response)</i></p>
</p>

## Back to Micronaut

After we recapped what microservices architecture is, we can dive in our concrete Kotlin option.

## Resources

1. [Microservices explained - the What, Why and How?](https://www.youtube.com/watch?v=rv4LlmLmVWk) \[YouTube\]
2. [What is Microservices Architecture?](https://cloud.google.com/learn/what-is-microservices-architecture) \[Website\]
3. [What are Microservices?](https://www.youtube.com/watch?v=CdBtNQZH8a4) \[YouTube\]
4. [Microservices with Node JS and React](https://www.udemy.com/course/microservices-with-node-js-and-react) \[Udemy\]

## \[Related GitHub Repo\]

### \[Title of repo\]

### \[Author of repo\]

### \[Link to repo\]

\[Write a brief description on the purpose of the repo\]

**Note:** All your work should be _in your own words_. If you quote anyone, or if you use any resources other than the Kotlin Overview docs you should say so and provide a link in a **Bibliography**.

## Reflection

\[Use this space to reflect on what you learned. Consult me or the [course site](https://ash-teach.github.io/dgl-204/#/dgl204-2022fa/week-01#assignments) if you need help\]
