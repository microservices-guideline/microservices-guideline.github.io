
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

- Article: [Building microservices in 2019 and beyond](https://atlassian.com/continuous-delivery/microservices/building-microservices) - Atlassian blog

- Article: [Microservices and Microservices Architecture](https://www.atlassian.com/continuous-delivery/microservices) - Atlassian Blog

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