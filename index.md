
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

- Video: [From Monorail to Monorepo: Airbnb's journey into microservices](https://www.youtube.com/watch?v=47VOcGGm6aU) - GitHub Universe 2018

	- [19:12](https://www.youtube.com/watch?v=47VOcGGm6aU)  - Not allow developers to contribute codes into monorail anymore unless it's like maintenance code you will not be allowed to add new features into monorail and this is really to kind of force people to adopt microservices.

	- [24:11](https://www.youtube.com/watch?v=47VOcGGm6aU) - talk to each other by doing RPC calls over TCP so there's no JSON over HTTP between services (Apache Thrift)

	- [24:44](https://www.youtube.com/watch?v=47VOcGGm6aU) - Communication is asynchronous you don't expect a result back, we use Kafka's or a message queue so you would basically just put in queue a message

	- [30:57](https://www.youtube.com/watch?v=47VOcGGm6aU)  - we're also moving in to deploy pipelines so it used to be where anyone can deploy any piece of code to any environments

	- [32:04](https://www.youtube.com/watch?v=47VOcGGm6aU) - we're actually moving into spinnaker a open source continuous delivery tool built in-house by Netflix

	- [36:31](https://www.youtube.com/watch?v=47VOcGGm6aU) - We have dozens, hundreds, maybe even thousands of services that are communicating with each other and something goes wrong, you don't know where it went wrong so you really need good monitoring tools.

- Article: [The Great Migration: from Monolith to Service-Oriented](https://www.infoq.com/presentations/airbnb-soa-migration)

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

	> "The separation of business concerns into independent microservices ensures that the service team owning that service is focused on the complete quality deliverable"
	
	> "Exponential Infrastructure Costs. Each new microservice an organization adds to its production deployment comes with its own cost of test suite, deployment playbooks, hosting, infrastructure, monitoring tools and more."
	
	> "Added Organizational Overhead. An added level of communication and collaboration is needed to coordinate updates and interfaces between microservices architecture teams"
	
	> "Containerization and the deployment of containers, is a new pattern of distributed infrastructure"
	
	> "Start small to understand the technical requirements of a distributed system, how to fail gracefully and scale individual components."

## Danske Bank (DB)

- Papper [From Monolithic to Microservices: An Experience Report from the Banking Domain](https://ieeexplore.ieee.org/document/8354415)

## Karma (KM)

- [How we build microservices at Karma](https://blog.karmawifi.com/how-we-build-microservices-at-karma-71497a89bfb4)

## Medium (MD)

- Article: [Microservice Architecture at Medium](https://medium.engineering/microservice-architecture-at-medium-9c33805eb74f)

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
	- [31:15](https://youtu.be/57UK46qfBLY?t=1874) - Use circuit breaker to enable fallbacks and recover system failure
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

- Article: [Building Products at SoundCloud — Part I: Dealing with the Monolith](https://developers.soundcloud.com/blog/building-products-at-soundcloud-part-1-dealing-with-the-monolith)

- Article: [Building Products at SoundCloud — Part II: Breaking the Monolith](https://developers.soundcloud.com/blog/building-products-at-soundcloud-part-2-breaking-the-monolith)

- Article: [Building Products at SoundCloud — Part III: Microservices in Scala and Finagle](https://developers.soundcloud.com/blog/building-products-at-soundcloud-part-3-microservices-in-scala-and-finagle)

- Article: [Microservices and the monolith](https://developers.soundcloud.com/blog/microservices-and-the-monolith)

## Thoughworks (TH)

- Article: [How to break a Monolith into Microservices](https://martinfowler.com/articles/break-monolith-into-microservices.html)

## TransferWise (TW)

- Thesis: [Migrating the Monolith to a Microservices Architecture: the Case of TransferWise](https://digi.lib.ttu.ee/i/?3491)


## Uber (UB)

- Article: [Service-Oriented Architecture: Scaling the Uber Engineering Codebase As We Grow](https://eng.uber.com/soa/)

- Article: [Rewriting Uber Engineering: The Opportunities Microservices Provide](https://eng.uber.com/building-tincup/)

## WIX (WX)

- Video: [Journey from Monolith to Microservices and DevOps by WIX](https://www.youtube.com/watch?v=NrFRC7HB3rU) - 
XP Days Ukraine 2017

	- [6:41](https://youtu.be/NrFRC7HB3rU?t=405) - Identify scalability concerns of the system that will help to figure out what parts can be separated
	- [10:26](https://youtu.be/NrFRC7HB3rU?t=624) -  Start separating different system areas that can easily be identified (E.g. Wix site builder system was separated from the viewer part)
	- [27:32](https://youtu.be/NrFRC7HB3rU?t=1651) - Create feature killers to make it possible to turn off services that are down. So the system can work even without a feature
	- [32:21](https://youtu.be/NrFRC7HB3rU?t=1941) - The new microservice should be owned by a team, who will be responsible for deploys, fixes, etc.
	- [33:34](https://youtu.be/NrFRC7HB3rU?t=2014) -  The size of the microservice should be related to the size of the team who is building this microservice
	- [34:41](https://youtu.be/NrFRC7HB3rU?t=2081) - After separating the main parts of the monolith, start to extract other segments of each main part
	- [38:46](https://youtu.be/NrFRC7HB3rU?t=2326) - Default to the technology stack that your team knows how to operate. Leave the technical innovation for the non critical microservices and let the team who owns it to take full responsibility for its operation
	- [42:54](https://youtu.be/NrFRC7HB3rU?t=2574) - It’s all about trade off. Don’t use things that you don’t really need. Check the main concerns of your system and start from them

- Video: [Scaling Engineering by Hacking Conway's Law by Aviran Mordo](https://www.youtube.com/watch?v=eG27-f79YX0) - Devoxx UK 2016

	- [24:00](https://youtu.be/eG27-f79YX0?t=1445) - Limit your code stack so you don’t have to implement same functionality in multiples languages. Thus you can improve code reuse and development velocity.