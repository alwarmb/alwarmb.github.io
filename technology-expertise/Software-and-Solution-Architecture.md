# arc42 - Software Architecture Methodology

arc42 - the template for effective, practical and pragmatic software architecture documentation and communication. arc42 has a clear, simple and effective structure to document and communicate your software system. It is optimized for understandability and adequacy. arc42 naturally guides you to explain any kind of architecture information or decision in an understandable way, easy to maintain.

arc42 answers the following two questions in a pragmatic way and can be tailored to your specific needs:

- What should you document/communicate about your architecture?
- How should you document/communicate?


![arc42-overview-V8.png](./images/arc42/arc42-overview-V8.png)

## 1. Introduction and Goals

<img src="./images/arc42/01-intro-and-goals.png" width="500">

Short description of the requirements, driving forces, extract (or abstract) of requirements. Top three (max five) quality goals for the architecture which have highest priority for the major stakeholders. A table of important stakeholders with their expectation regarding architecture.

## 2. Constraints

<img src="./images/arc42/02-constraints-overview.png" width="500">

Anything that constrains teams in design and implementation decisions or decision about related processes. Can sometimes go beyond individual systems and are valid for whole organizations and companies.

## 3. Context and Scope

<img src="./images/arc42/03-context-overview.png" width="500">

Delimits your system from its (external) communication partners (neighboring systems and users). Specifies the external interfaces. Shown from a business/domain perspective (always) or a technical perspective (optional)

## 4. Solution Strategy

<img src="./images/arc42/04-solution-strategy-overview.svg" width="300">

Summary of the fundamental decisions and solution strategies that shape the architecture. Can include technology, top-level decomposition, approaches to achieve top quality goals and relevant organizational decisions.

## 5. Building Block View

<img src="./images/arc42/05-building-block-overview.png" width="300">

Static decomposition of the system, abstractions of source-code, shown as hierarchy of white boxes (containing black boxes), up to the appropriate level of detail.

## 6. Runtime View

<img src="./images/arc42/06-runtime-overview.png" width="400">

Behavior of building blocks as scenarios, covering important use cases or features, interactions at critical external interfaces, operation and administration plus error and exception behavior.

## 7. Deployment View

<img src="./images/arc42/07-deployment-overview.png" width="200">

Technical infrastructure with environments, computers, processors, topologies. Mapping of (software) building blocks to infrastructure elements.

## 8. Crosscutting Concepts

<img src="./images/arc42/08-concepts-overview.png" width="300">

Overall, principal regulations and solution approaches relevant in multiple parts (→ cross-cutting) of the system. Concepts are often related to multiple building blocks. Include different topics like domain models, architecture patterns and -styles, rules for using specific technology and implementation rules.

## 9. Architectural Decisions

<img src="./images/arc42/09-decision-overview.png" width="350">

Important, expensive, critical, large scale or risky architecture decisions including rationales.

## 10. Quality Requirements

<img src="./images/arc42/10-q-scenario-overview.png" width="500">

Quality requirements as scenarios, with quality tree to provide high-level overview. The most important quality goals should have been described in section 1.2. (quality goals).

## 11. Risks and Technical Debt

<img src="./images/arc42/11-risk-overview.png" width="300">

Known technical risks or technical debt. What potential problems exist within or around the system? What does the development team feel miserable about?

## 12. Glossary

<img src="./images/arc42/12-glossary-overview.png" width="400">

Important domain and technical terms that stakeholders use when discussing the system. Also: translation reference if you work in a multi-language environment.

# Software Architecture Design Patterns

## Ambassador Pattern

Create helper services that send network requests on behalf of a consumer service or application. An ambassador service can be thought of as an out-of-process proxy that is co-located with the client.

This pattern can be useful for offloading common client connectivity tasks such as monitoring, logging, routing, security (such as TLS), and resiliency patterns in a language agnostic way. It is often used with legacy applications, or other applications that are difficult to modify, in order to extend their networking capabilities. It can also enable a specialized team to implement those features.

![ambassador-pattern](./images/arc-snippets/ambassador-pattern.drawio.png)

## Backend for Frontends Pattern

Create separate backend services to be consumed by specific frontend applications or interfaces. This pattern is useful when you want to avoid customizing a single backend for multiple interfaces. This pattern was first described by Sam Newman.

![backend-for-frontend-pattern](./images/arc-snippets//backend-for-frontend-pattern.drawio.png)

## Cache-Aside Pattern

Load data on demand into a cache from a data store. This can improve performance and also helps to maintain consistency between data held in the cache and data in the underlying data store.

![cache-aside-pattern](./images/arc-snippets/cache-aside-pattern.drawio.png)

## Circuit Breaker Pattern

Handle faults that might take a variable amount of time to recover from, when connecting to a remote service or resource. This can improve the stability and resiliency of an application.

![circuit-breaker-pattern](./images/arc-snippets/circuit-breaker-pattern.drawio.png)

## CQRS Pattern

CQRS stands for Command and Query Responsibility Segregation, a pattern that separates read and update operations for a data store. Implementing CQRS in your application can maximize its performance, scalability, and security. The flexibility created by migrating to CQRS allows a system to better evolve over time and prevents update commands from causing merge conflicts at the domain level.

![cqrs-pattern](./images/arc-snippets/cqrs-pattern.drawio.png)

## Federated Identity Pattern

Delegate authentication to an external identity provider. This can simplify development, minimize the requirement for user administration, and improve the user experience of the application.

![federated-identity-pattern](./images/arc-snippets/federated-identity-pattern.drawio.png)

An organization hosts a multi-tenant software as a service (SaaS) application in Microsoft Azure. The application includes a website that tenants can use to manage the application for their own users. The application allows tenants to access the website by using a federated identity that is generated by Active Directory Federation Services (AD FS) when a user is authenticated by that organization's own Active Directory.

![federated-identity-example](./images/arc-snippets/federated-identity-example.drawio.png)

## Gatekeeper Pattern

Protect applications and services by using a dedicated host instance to broker requests between clients and the application or service. The broker validates and sanitizes the requests, and can provide an additional layer of security and limit the system's attack surface.

![gatekeeper-pattern](./images/arc-snippets/gatekeeper-pattern.drawio.png)

## Health Endpoint Monitoring

To verify that applications and services are performing correctly, you can use the Health Endpoint Monitoring pattern. This pattern specifies the use of functional checks in an application. External tools can access these checks at regular intervals through exposed endpoints.

![health-endpoint-monitoring-pattern](./images/arc-snippets/health-endpoint-monitoring-pattern.drawio.png)

## Leader Election Pattern

Coordinate the actions performed by a collection of collaborating instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the others. This can help to ensure that instances don't conflict with each other, cause contention for shared resources, or inadvertently interfere with the work that other instances are performing.

![leader-election-pattern](./images/arc-snippets/leader-election-pattern.drawio.png)

## Materialized View Pattern

Generate prepopulated views over the data in one or more data stores when the data isn't ideally formatted for required query operations. This can help support efficient querying and data extraction, and improve application performance.

![materialized-view-pattern](./images/arc-snippets/materialized-view-pattern.png)

## Publisher / Subscriber Pattern

Enable an application to announce events to multiple interested consumers asynchronously, without coupling the senders to the receivers.

![pub-sub-pattern](./images/arc-snippets/pub-sub-pattern.drawio.png)

## Sharding Pattern

Divide a data store into a set of horizontal partitions or shards. This can improve scalability when storing and accessing large volumes of data.

![sharding-pattern](./images/arc-snippets/sharding-pattern.drawio.png)

## Sidecar Pattern

Deploy components of an application into a separate process or container to provide isolation and encapsulation. This pattern can also enable applications to be composed of heterogeneous components and technologies.

This pattern is named Sidecar because it resembles a sidecar attached to a motorcycle. In the pattern, the sidecar is attached to a parent application and provides supporting features for the application. The sidecar also shares the same lifecycle as the parent application, being created and retired alongside the parent. The sidecar pattern is sometimes referred to as the sidekick pattern and is a decomposition pattern.

![sidecar-pattern](./images/arc-snippets/sidecar-pattern.png)

# Solution Architecture Snippets

## IoT Reference Architecture

![azure-iot-reference-architecture](./images/arc-snippets/azure-iot-reference-architecture.png)

## IoT analytics with Azure Data Explorer

![iot-azure-data-explorer-new](./images/arc-snippets/iot-azure-data-explorer-new.png)

## Machine learning in Azure IoT Edge vision AI

![data-science-cycle](./images/arc-snippets/data-science-cycle.drawio.png)

![vision-edge-flow](./images/arc-snippets/vision-edge-flow.png)

## IoT application-to-device commands

![cloud-to-device-message](./images/arc-snippets/cloud-to-device-message.drawio.png)

## Event Driven Architecture

An event-driven architecture consists of event producers that generate a stream of events, and event consumers that listen for the events.

![event-driven-architecture](./images/arc-snippets/event-driven-architecture.drawio.png)

## Serverless event processing

This reference architecture shows a serverless, event-driven architecture that ingests a stream of data, processes the data, and writes the results to a back-end database.

![serverless-event-processing](./images/arc-snippets/serverless-event-processing.png)

## Azure Kubernetes Service (AKS) microservices architecture

![aks-production-deployment](./images/arc-snippets/aks-production-deployment.png)

## Blue-green deployment of AKS clusters

![blue-green-aks-deployment-diagram-public-architecture](./images/arc-snippets/blue-green-aks-deployment-diagram-public-architecture.png)

# References
- https://www.arc42.org
- https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/iot
- https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/iot-azure-data-explorer
- https://learn.microsoft.com/en-us/azure/architecture/guide/iot-edge-vision/machine-learning
- https://learn.microsoft.com/en-us/azure/architecture/example-scenario/iot/cloud-to-device
- https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/event-driven
- https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/serverless/event-processing
- https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/containers/aks-microservices/aks-microservices-advanced
- https://learn.microsoft.com/en-us/azure/architecture/guide/aks/blue-green-deployment-for-aks