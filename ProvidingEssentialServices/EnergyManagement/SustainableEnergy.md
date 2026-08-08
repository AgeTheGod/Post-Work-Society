---
title: Sustainable Energy
layout: default
parent: Providing Essential Services
nav_order: 1
---
#   Sustainable Energy Management

**Sustainable Energy Management** is (or should be) pretty much the top priority in any modern society (some would say the single most important requirement) and when we talk about Energy Generation we're really talking about "Electricity" because that's what powers pretty much everything that most of us care about.

Fortunately, because of the current focus on "Renewable Energy" and "Sustainable Energy", this is an area that has been exploding wioth new technologies in recent years to the externt that 100% renewable and sustainable electricity generation is pretty much a reality.
Some Countries are already there (e.g. Costa Rica, Iceland, Norway) and many more, including the UK, are on the way andf not far short of being completely self-sustainable.
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

The main reason for separating these three concerns is that [Energy Generation](./EnergyGeneration) is not a single solution and whilst there are many, many deployable technologies for generating energy. 
On the other hand, both [Energy Storage](./EnergyStorage) but [Energy Distribution](./EnergyDistribution) is much more limited.
In addition [Energy Distribution](./EnergyDistribution) is, or should be, a natural monopoly from the viewpoint of the consumer. 

Hopefully, the significance of this split will become very apparent when discussing [Delivering Energy](./DeliveringEnergyGenerationCapacity) and [Funding Energy Management](./FundingEnergyManagement).

```mermaid
architecture-beta
group generation(cloud)[API]
service Solar(server) in generation
service Wind(server) in generation
service Nuclear(server) in generation
service Fossile(server) in generation
align column Solar Wind Nuclear Fossile

service Grid(cloud)[National Grid]
%%  server{group}:B --> T:subnet{group}
Solar:R --> L:Grid
Wind:R --> L:Grid
Nuclear:R --> L:Grid
Fossile:R --> L:Grid

group consumer(cloud)[API]
service Residential(server)[DB2] in consumer
service Commercial(server)[DB3] in consumer
service Government(server)[MCP] in consumer
service Essential(server)[MCP] in consumer

service Storage(storage)

Grid:R --> L:Residential
Grid:R --> L:Commercial
Grid:R --> L:Governent
Grid:R --> L:Essential
```


```mermaid
C4Dynamic
title Energy Generation Topology

    ContainerDb(c4, "Generation", "", "")
    Container(c1, "Distribution", "", "")
    Container_Boundary(b, "") {
      Component(Solar, "Solar", "", "")
      Component(Wind, "Wind", "", "")
    }
    Rel(c1, c2, "")
    Rel(c2, c3, "")
    Rel(c3, c4, "")

    UpdateRelStyle(c1, c2, $textColor="red", $offsetY="-40")
    UpdateRelStyle(c2, c3, $textColor="red", $offsetX="-40", $offsetY="60")
    UpdateRelStyle(c3, c4, $textColor="red", $offsetY="-40", $offsetX="10")


```

```mermaid
    C4Deployment
    title Energy System Deployment 

    Deployment_Node(mob, "Customer's mobile device", "Apple IOS or Android"){
        Container(mobile, "Mobile App", "Xamarin", "Provides a limited subset of the Internet Banking functionality to customers via their mobile device.")
    }

    Deployment_Node(comp, "Customer's computer", "Microsoft Windows or Apple macOS"){
        Deployment_Node(browser, "Web Browser", "Google Chrome, Mozilla Firefox,<br/> Apple Safari or Microsoft Edge"){
            Container(spa, "Single Page Application", "JavaScript and Angular", "Provides all of the Internet Banking functionality to customers via their web browser.")
        }
    }

    Deployment_Node(plc, "Big Bank plc", "Big Bank plc data center"){
        Deployment_Node(dn, "bigbank-api*** x8", "Ubuntu 16.04 LTS"){
            Deployment_Node(apache, "Apache Tomcat", "Apache Tomcat 8.x"){
                Container(api, "API Application", "Java and Spring MVC", "Provides Internet Banking functionality via a JSON/HTTPS API.")
            }
        }
        Deployment_Node(bb2, "bigbank-web*** x4", "Ubuntu 16.04 LTS"){
            Deployment_Node(apache2, "Apache Tomcat", "Apache Tomcat 8.x"){
                Container(web, "Web Application", "Java and Spring MVC", "Delivers the static content and the Internet Banking single page application.")
            }
        }
        Deployment_Node(bigbankdb01, "bigbank-db01", "Ubuntu 16.04 LTS"){
            Deployment_Node(oracle, "Oracle - Primary", "Oracle 12c"){
                ContainerDb(db, "Database", "Relational Database Schema", "Stores user registration information, hashed authentication credentials, access logs, etc.")
            }
        }
        Deployment_Node(bigbankdb02, "bigbank-db02", "Ubuntu 16.04 LTS") {
            Deployment_Node(oracle2, "Oracle - Secondary", "Oracle 12c") {
                ContainerDb(db2, "Database", "Relational Database Schema", "Stores user registration information, hashed authentication credentials, access logs, etc.")
            }
        }
    }

    Rel(mobile, api, "Makes API calls to", "json/HTTPS")
    Rel(spa, api, "Makes API calls to", "json/HTTPS")
    Rel_U(web, spa, "Delivers to the customer's web browser")
    Rel(api, db, "Reads from and writes to", "JDBC")
    Rel(api, db2, "Reads from and writes to", "JDBC")
    Rel_R(db, db2, "Replicates data to")

    UpdateRelStyle(spa, api, $offsetY="-40")
    UpdateRelStyle(web, spa, $offsetY="-40")
    UpdateRelStyle(api, db, $offsetY="-20", $offsetX="5")
    UpdateRelStyle(api, db2, $offsetX="-40", $offsetY="-20")
    UpdateRelStyle(db, db2, $offsetY="-10")


```