
This page contains the resources used in the paper "Guidelines for Extracting Microservices from Monolithics", available at [doi:10..xxx/yyyyy]().

## Summary

1. [AirBnb](#airbnb-ab)
2. [Atlassian](#atlassian-at)
3. [Danske Bank](#danske-bank-db)
4. [Karma](#karma-km)
5. [Medium](#medium-md)
6. [Netflix](#netflix-nf)
7. [SoundCloud](#soundcloud-sc)
8. [Thoughworks](#thoughworks-th)
9. [TransferWise](#transferwise-tw)
10. [Uber](#uber-ub)
11. [WIX](#wix-wx)

<hr>

## AirBnb (AB)

## Atlassian (AT)

- Video: [From Monolith to Microservices](https://www.youtube.com/watch?v=1jvgxdzxJGQ) - AtlasCamp 2016

	- [4:13](https://youtu.be/1jvgxdzxJGQ?t=256) - Monoliths takes long periods of time to test, deploy and validate.
	- [4:40](https://youtu.be/1jvgxdzxJGQ?t=286) - Use containers
	- [7:57](https://youtu.be/1jvgxdzxJGQ?t=477) - Use Orchestration
	- [10:36](https://youtu.be/1jvgxdzxJGQ?t=636) - Use continuous integration

- Article: [Building microservices in 2019 and beyond](https://atlassian.com/continuous-delivery/microservices/building-microservices) - Atlassian blog

	> "The guiding principle of microservices is to build an application by splitting its business components in small services that can be deployed and operated independently from each other."
	
	> "You can also start by separating the logic from your web UI and make sure that it interacts with your backend via a RESTful API over HTTP"
	
	> "You'll need to split a codebase in multiple services, implement the right patterns to fail gracefully and recover from network issues, deal with data consistency, monitor service load, etc."
	
	> "identified the boundaries of your services and when you've figured out how you can change your teams to be more vertical in terms of competencies you can start splitting your monolith to build microservices."
	
	> "...communication protocol between your services should be as simple as possible."
	
	> "In some cases you might find yourself using an event-driven architecture with asynchronous message-based communications"
	
	> "...you should look into basic message queue services like RabbitMQ and avoid adding complexity to the messages transmitted over the network."
	
	> "This means that each service might end up having its own datastore to persist the data that it needs."
	
	> "...event-driven architecture allows the account service logic to be kept simple"
	
	> "...your system should be resilient to partial failure"
	
	> "as part of your transition to microservices it is critical that you embrace continuous delivery to reduce the risks of release failure, as well as making sure that your team is focused on building and running the application, rather than being stuck deploying it."
	
	> "An iterative strategy to sequentially migrate smaller components to microservices is a safer bet. Identify the most well defined service boundaries within an established monolith application and iteratively work to decouple them into their own microservice"

- Article: [Microservices and Microservices Architecture](https://www.atlassian.com/continuous-delivery/microservices) - Atlassian Blog

	> "Microservices is a modern term used to describe a traditional "separation of concerns" pattern within a distributed, network project"
	
	> "A Microservice is a web service that is responsible for one piece of domain logic." 
	
	> "Microservices interact with each other via simple network protocols like REST."
	
	> "The guiding principle of microservices is to build an application by splitting its business components into small services that can be deployed and operated independently from each other"
	
	> "This separation of concerns and decoupled independent function, enables streamlined agile software development practices like continuous delivery and integration."
	
	> "Monolith it may start to become cumbersome to have many developers working on singular codebase. Code conflicts become more frequent and the risk of updates to one feature introducing bugs in an unrelated feature increases."
	
	> "Horizontal scaling. Microservices are distributed by design and can be deployed in clusters. This enables dynamic horizontal scaling across the service boundaries."
	
	> "Microservice ownership teams can operate independently of other feature teams in the organization"
"The separation of business concerns into independent microservices ensures that the service team owning that service is focused on the complete quality deliverable"
	
	> "Exponential Infrastructure Costs. Each new microservice an organization adds to its production deployment comes with its own cost of test suite, deployment playbooks, hosting, infrastructure, monitoring tools and more."
	
	> "Added Organizational Overhead. An added level of communication and collaboration is needed to coordinate updates and interfaces between microservices architecture teams"
	
	> "Containerization and the deployment of containers, is a new pattern of distributed infrastructure"
	
	> "Start small to understand the technical requirements of a distributed system, how to fail gracefully and scale individual components."

## Danske Bank (DB)

## Karma (KM)

## Medium (MD)

## Netflix (NF)

- Video: [Microservices at Netflix Scale: Principles, Tradeoffs & Lessons Learned](https://www.youtube.com/watch?v=57UK46qfBLY) - GOTO Conference 2016

	- [05:31](https://youtu.be/57UK46qfBLY?t=331) - One database is a single point of failure
	- [07:50](https://youtu.be/57UK46qfBLY?t=470) - Microservices should be stateless
	- [08:30](https://youtu.be/57UK46qfBLY?t=510) - Vertical limits and scalability
	- [09:11](https://youtu.be/57UK46qfBLY?t=547) - Isolation, redundancy and isolation of microservices to avoid a single point of failure
	- [09:55](https://youtu.be/57UK46qfBLY?t=593) - Chaos Monkey - Netflix test approach
	- [17:28](https://youtu.be/57UK46qfBLY?t=1048) - Lack of agility in development process and evolving
	- [17:50](https://youtu.be/57UK46qfBLY?t=1069) - Loose coupling for teams isolation / Independent life cycles
	- [19:12](https://youtu.be/57UK46qfBLY?t=1152) - Benefit on separation of concerns
	- [20:00](https://youtu.be/57UK46qfBLY?t=1201) - Problems in organizational change
	- [21:55](https://youtu.be/57UK46qfBLY?t=1315) - Centralized infrastructure and high cost
	- [22:10](https://youtu.be/57UK46qfBLY?t=1331) - Migration / hybrid ecosystem
	- [23:13](https://youtu.be/57UK46qfBLY?t=1394) - Uses IPC or RPC communication
	- [26:20](https://youtu.be/57UK46qfBLY?t=1579) - Use telemetry / metrics to monitor services
	- [36:40](https://youtu.be/57UK46qfBLY?t=2201) - Use containers
	- [47:57](https://youtu.be/57UK46qfBLY?t=2876) - Use CI/CD to automate releases


- Video: [Mastering Chaos - A Netflix Guide to Microservices](https://www.youtube.com/watch?v=CZ3wIuvmHeM) - QCon 2016

	- [6:43](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Difficult do debug and diagnose issues
	- [09:00](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Separation of concerns and isolation
	- [09:12](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Scalability and workload partitioning
	- [28:10](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Avoid to store data and state within one application
	- [35:51](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Continuous learning and automate failure resolutions
	- [40:37](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=) - Use containers


- Article [Adopting Microservices at Netflix: Lessons for Architectural Design](https://www.nginx.com/blog/microservices-at-netflix-architectural-best-practices/) - Nginx Blog

	> "Defines a microservices architecture as a service‐oriented architecture composed of loosely coupled elements that have bounded contexts"

	> "Loosely coupled means that you can update the services independently"

	> "Do not use the same backend data store across microservices"

	>  "You need to add a tool that performs master data management (MDM)"

	> "Do a separate build for each microservice"

	> "Deploying microservices in containers is important, because it means you just need just one tool to deploy everything"

	> "Treat Servers as Stateless"

	> "...microservices and its peers interact strictly through APIs and so don’t share data structures, database schemata, or other internal representations of objects"


## SoundCloud (SC)

## Thoughworks (TH)

## TransferWise (TW)

## Uber (UB)

## WIX (WX)