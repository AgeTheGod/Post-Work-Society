---
title: What Is Society 
layout: default
parent: Definition Of Terms
nav_order: 1
---
#   What Is Society?

A Society is a group of individual persons that have grouped together for mutual benefit; to achieve common goals and to support each other in achieving those goals.

```mermaid
classDiagram
    class Society
    class Person
    class BeneficialService["Beneficial Service"]
    class GoverningBody["Governing Body"]
    class Constitution
    class RegulatorySystem["Regulatory System"]
    class SocialRole["Social Role"]
    class Market

    Person <|-- Visitor
    Person <|-- Member

    Society <-- Member : is a member of
    Society *-- GoverningBody : managed by
    Society *-- BeneficialService : provides
    Society *-- Constitution : has
    Society *-- Market : provides
    Society *-- RegulatorySystem

    Person <-- SocialRole : filled by
    SocialRole --> Society
    Citizen --> GoverningBody : serves on

    OnDemandService <|-- BeneficialService
    UniversalService <|-- BeneficialService
    
    Market --|> InternalMarket
    OnDemandService --> InternalMarket
```

##  Person

A person is any individual

##  Beneficial Service

##  Regulatory Body

##  Constitution
