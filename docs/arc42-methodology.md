# arc42 - Software Architecture Methodology

arc42 - the template for effective, practical and pragmatic software architecture documentation and communication. arc42 has a clear, simple and effective structure to document and communicate your software system. It is optimized for understandability and adequacy. arc42 naturally guides you to explain any kind of architecture information or decision in an understandable way, easy to maintain.

arc42 answers the following two questions in a pragmatic way and can be tailored to your specific needs:

- What should you document/communicate about your architecture?
- How should you document/communicate?


![arc42-overview-V8.png](./_images/arc42/arc42-overview-V8.png)

# 1. Introduction and Goals

<img src="./_images/arc42/01-intro-and-goals.png" width="500">

Short description of the requirements, driving forces, extract (or abstract) of requirements. Top three (max five) quality goals for the architecture which have highest priority for the major stakeholders. A table of important stakeholders with their expectation regarding architecture.

# 2. Constraints

<img src="./_images/arc42/02-constraints-overview.png" width="500">

Anything that constrains teams in design and implementation decisions or decision about related processes. Can sometimes go beyond individual systems and are valid for whole organizations and companies.

# 3. Context and Scope

<img src="./_images/arc42/03-context-overview.png" width="500">

Delimits your system from its (external) communication partners (neighboring systems and users). Specifies the external interfaces. Shown from a business/domain perspective (always) or a technical perspective (optional)

# 4. Solution Strategy

<img src="./_images/arc42/04-solution-strategy-overview.svg" width="300">

Summary of the fundamental decisions and solution strategies that shape the architecture. Can include technology, top-level decomposition, approaches to achieve top quality goals and relevant organizational decisions.

# 5. Building Block View

<img src="./_images/arc42/05-building-block-overview.png" width="300">

Static decomposition of the system, abstractions of source-code, shown as hierarchy of white boxes (containing black boxes), up to the appropriate level of detail.

# 6. Runtime View

<img src="./_images/arc42/06-runtime-overview.png" width="400">

Behavior of building blocks as scenarios, covering important use cases or features, interactions at critical external interfaces, operation and administration plus error and exception behavior.

# 7. Deployment View

<img src="./_images/arc42/07-deployment-overview.png" width="200">

Technical infrastructure with environments, computers, processors, topologies. Mapping of (software) building blocks to infrastructure elements.

# 8. Crosscutting Concepts

<img src="./_images/arc42/08-concepts-overview.png" width="300">

Overall, principal regulations and solution approaches relevant in multiple parts (→ cross-cutting) of the system. Concepts are often related to multiple building blocks. Include different topics like domain models, architecture patterns and -styles, rules for using specific technology and implementation rules.

# 9. Architectural Decisions

<img src="./_images/arc42/09-decision-overview.png" width="350">

Important, expensive, critical, large scale or risky architecture decisions including rationales.

# 10. Quality Requirements

<img src="./_images/arc42/10-q-scenario-overview.png" width="500">

Quality requirements as scenarios, with quality tree to provide high-level overview. The most important quality goals should have been described in section 1.2. (quality goals).

# 11. Risks and Technical Debt

<img src="./_images/arc42/11-risk-overview.png" width="300">

Known technical risks or technical debt. What potential problems exist within or around the system? What does the development team feel miserable about?

# 12. Glossary

<img src="./_images/arc42/12-glossary-overview.png" width="400">

Important domain and technical terms that stakeholders use when discussing the system. Also: translation reference if you work in a multi-language environment.

# References
- https://www.arc42.org