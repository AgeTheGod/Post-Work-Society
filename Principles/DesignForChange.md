---
title: Design For Change
layout: default
parent: Design Principles
nav_order: 6
---
#   Design For Change

Design for Change (also known as Evolutionary Design) is a software engineering and system design principle that states software should be built to accommodate future, unpredictable changes with minimal effort and disruption.

Since business requirements, technologies, and user needs constantly evolve, a good design assumes that change is inevitable and structures code so it can adapt easily without requiring a complete rewrite.

To successfully design for change, a system must isolate its different parts so that altering one piece does not break another. This is achieved through two main concepts:
- Low Coupling: Independent components. Changing the code inside your payment system should not break the code in your user profile system. [7]
- High Cohesion: Focused components. Each module or class should do exactly one job and do it well, making it easy to locate where a change needs to happen.


Design For Change, especially in Application Development, is based on the SOLID Principles of Object-Oriented Design. 
These are five foundational rules specifically engineered to combat "spaghetti code" and make software flexible, understandable, and highly adaptable to future business requirements.

|   |                                       |                                                                                                             | |
|---|---------------------------------------|-------------------------------------------------------------------------------------------------------------|-|
| S | Single Responsibility Principle (SRP) | A class or module should have one, and only one, reason to change.                                          |
| O | Open/Closed Principle (OCP)           | Software entities should be open for extension, but closed for modification.                                |
| L | Liskov Substitution Principle (LSP)   | Subtypes must be substitutable for their base types without breaking the application.                       |
| I | Interface Segregation Principle (ISP) | Clients should not be forced to depend on interfaces or methods they do not use.                            |
| D | Dependency Inversion Principle (DIP)  | High-level modules should not depend on low-level modules; both should depend on abstractions (interfaces). |

By strictly adhering to these five rules, any application naturally becomes modular. 
Consequently, when a new business requirement demands a change we only have to modify one isolated part of the overall application and completely protecting the rest of your application from any accidental regression bugs.

The larger and more complex the application is then the more desirable it is to Design For Change because the cost of a complete rewrite becomes prohibitive and the risk of introducing bugs into existing functionality becomes unacceptable. Obviously with something a large and complex as the Post Work Society we cannot afford to have a complete rebuild of Society every time a new requirement is introduced.

## Related Principles

- [Minimum Viable Product](MinimumViableProduct.md) An MVP must evolve into a mature product so if you do not design for change from day one, your MVP will become unmaintainable forcing a costly, risky "revolutionary" redesign later.
- [YAGNI](YouAintGonnaNeedIt.md) says "Don't build features for tomorrow." Design for Change says "But build today's features so they are easy to change tomorrow."
- [Evolution Not Revolution](EvolutionNotRevolution.md) ensures that as you grow, you build on top of that foundation incrementally rather than panic-building massive new systems.

