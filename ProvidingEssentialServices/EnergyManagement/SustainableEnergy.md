---
title: Sustainable Energy
layout: default
parent: Providing Essential Services
nav_order: 1
---
#   Sustainable Energy Management

**Sustainable Energy Management** is (or should be) pretty much the top priority in any modern society (some would say the single most important requirement) and when we talk about Energy Generation we're really talking about "Electricity" because that's what powers pretty much everything that most of us care about.

Fortunately, because of the current focus on "Renewable Energy" and "Sustainable Energy", this is an area that has been exploding with new technologies in recent years to the extent that 100% renewable and sustainable electricity generation is pretty much a reality.
Some Countries are already there (e.g. Costa Rica, Iceland, Norway) and many more, including the UK, are on the way and not far short of being completely self-sustainable.
The cost of renewable energy is now cheaper than fossil fuels in many parts of the world.

>    Note: I'm deliberately not addressing the Climate Change issue in this section.
>    Not saying that it's unimportant (it's actually a critical problem to solve) but it's something that gets resolved as a side-effect of solving the more general Energy Management problem.

So, in this context, Sustainable Energy is essentially the generation of Electricity from resources that do not need continuous replenishment over time.

In addition, when we talk about Resources we are not just talking about the raw energy sources, such as Coal and Oil and Sunshine, but also the materials used to construct whatever mechanism (the technology) is used to convert the raw materials into energy.

In an ideal (and currently non-existent) world this would mean technology that is maintenance free and does not degrade over time but we're not there yet.
Hence, how maintainable a technology is becomes a significant criteria when discussing Sustainable Energy because a solution that needs rebuilding every 5 years is far less sustainable than a solution that lasts for 50 years before it needs replacing. 

This is the difference between Capital Costs and Operating Costs.
The Capital Cost is the cost of initially building the things we need, and once built the Operating Costs are the on-going costs required to keep a solution running once it starts producing

As outlined in [Delivering Energy Generation](./DeliveringEnergyGenerationCapacity) the maintenance of Sustainable Energy generation is decreasing significantly due to the durability of modern materials, such as ceramics, compared to historically significant  materials. 

For the purpose of documenting the enabling technologies for Sustainable Energy Management I've split this into a three part problem...
1. How to generate Electricity from sustainable sources?
2. How to store Electricity until it is required?
3. How to distribute Electricity to where it is needed?

```mermaid
architecture-beta
service generation(server)[National Energy Generation]
service distribution(cloud)[National Grid]
service storage(database)[National Storage]

group consumption(server)[Consumers]
service domestic(server)[Residential] in consumption
service commercial(server)[Commercial] in consumption
service government(server)[Government] in consumption
service essential(server)[Essential Services] in consumption
align row domestic commercial government essential
align row generation distribution storage

generation:R --> L:distribution
distribution:R <--> L:storage

distribution:B --> T:domestic
distribution:B --> T:commercial
distribution:B --> T:government
distribution:B --> T:essential

service local(server)[Local Solar]
local:T --> B:domestic
```
The main reason for separating these three concerns is that [Energy Generation](./EnergyGeneration) is not a single solution and there are many, many deployable technologies for generating energy.
On the other hand, both [Energy Storage](./EnergyStorage) but [Energy Distribution](./EnergyDistribution) are much more limited in their potential solutions.
In addition [Energy Distribution](./EnergyDistribution) is, or should be, a natural monopoly from the viewpoint of the consumer.

Hopefully, the significance of this split will become very apparent when discussing [Delivering Energy](./DeliveringEnergyGenerationCapacity) and [Funding Energy Management](./FundingEnergyManagement).

