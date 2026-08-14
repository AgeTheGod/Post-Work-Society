---
title: Computerized Systems
layout: default
parent: Enabling Technologies
nav_order: 3
---
#   Computerized Systems   

This is really a catch-all bucket of ideas rather than a distinct technology. Computerized Systems covers all kinds of software that executes on a computer to process data to carry out some activity.

##   Predictive Analytics

Predictive Analytics is the practice of using data, statistical algorithms and machine learning techniques to identify the likelihood of future demand based on historical data.
It's basic premise is that historical supply & demand information can be used to make better decisions about future supply & demand requirements and hence produce a more efficient production process with less waste.

This is actually already a well established and very widespread practice in many industries and is used to make informed decisions and improve business outcomes. 
I worked onm my first "predictive analytics" project during a summer break in 1975 whilst studying Statistics at school. 
It was a simple paper-based system that used historical sales data to track stock levels and indicate when new stock needed to be ordered in advance (it was the "dark ages" when re-stocking took weeks not days) to meet projected demand.
In effect it was a very basic "**Just In Time Delivery**" application.

In the intervening 50 years I've worked on multiple predictive analytics projects in various industries and I've seen how the field has evolved and how it has become more sophisticated and more widely used.

Nowadays just about every large organization has some kind of predictive analytics capability and it's used in a wide range of applications such as...
- **Demand Forecasting** : predicting future demand for products and services in order to better plan production and inventory levels.
- **Customer Segmentation** : dividing customers into different groups based on their purchasing preferences to target them with more relevant products and services. Pretty much every retailer does this to one extent or another.
- **Predictive Maintenance** :  predicting when equipment is likely to fail in order to schedule maintenance and to prevent downtime.
- **Supply Chain Optimization** : optimizing the supply chain in order to reduce costs and to improve efficiency.
- **Risk Management** : identifying and mitigate potential risks in order to protect an organization from financial losses and other negative outcomes.
- ...and many more.

Obviously, because it's simply a case of applying algorithms to data then it's also one of those areas that is a candidate for being fully automated.

Unfortunately, any Information Architect worth their salt will tell you that the real problem is not the algorithms but rather the data, and in particular the quality of the data. 
This also just happens to be the same problem we have with Artificial Intelligence i.e. the infamous "Garbage In, Garbage Out" (GIGO) problem.

##  Event-Driven Processing

It might seem odd to include a software design pattern such as Event-Driven Processing in a section about Predictive Analytics but it is actually a key enabler for Predictive Analytics and hence a key enabler for a post-work society.

Event-Driven Processing is a software architecture pattern that is based on the idea of processing events as they occur rather than processing data in batches.
This is particularly important in areas such as manufacturing and distribution where the ability to process data in real-time can lead to more efficient production and distribution processes.

##  Algorithmic Trading

This is a prime example of Predictive Analytics and Event-Driven Processing in action and it is used by many financial institutions to make informed decisions about buying and selling stocks, bonds, commodities, currencies, etc.
The algorithms used in algorithmic trading are designed to analyze large amounts of data in order to identify patterns and trends in prices and then automatically buy or sell financial instrument based on the observed data.
In fact, it is estimated that over 70% of all stock trades in the US are now made by algorithms and this percentage is only expected to increase in the future.

Obviously, this can easily be extended to other areas of the economy such as manufacturing and distribution where the algorithms can be used to make informed decisions about production and distribution based on historical data.

##  Data Centres

Unfortunately, very large scale data processing has two key problems...
1. data storage at scale requires a lot of physical space to hold racks and racks of "always on" disk drives.
2. data processing itself is a very energy intensive process

Consequently, the amount of energy required to store and process data is increasing exponentially as the amount of data being processed increases exponentially.

The current estimates are that worldwide about 150 Zettabytes (this is a very, very large number) of data are generated annually and projected to increase to around 500 Zettabytes by 2030.

    Note: Data storage climbs in intervals of 1,000 (metric) or 1,024 (binary) as follows...
        Gigabyte (GB) = 1,000 MB
        Terabyte (TB) = 1,000 GB
        Petabyte (PB) = 1,000 TB
        Exabyte  (EB) = 1,000 PB
        Zettabyte (ZB) = 1,000 EB
    so 150 Zettabytes is 150,000,000,000,000,000 MB of data and 500 Zettabytes is 500,000,000,000,000,000 MB of data.

In terms of Energy consumption, data centres currently consume around 1.5% of the world's electricity but, with the emergence of Artificial Intelligence, this is expected to increase to around 12% by 2030.

###  Data Centres In Space

Currently most of this data is processed in data centres on Earth but there are many organizations, both Public and Private, that are looking at the possibility of processing data in space in order to take advantage of the cooler temperatures and the abundance of solar energy.

This has become increasingly feasible in recent years due to the decreasing cost of launching payloads into space and the trend towards solid-state drives which are more durable and require less maintenance than traditional hard disk drives (no moving parts means nothing to break).

Note: A side=-effect of "Data Centres In Space" is that moving the energy intensive process of data storage and processing to space would reduce the amount of energy consumed on Earth and hence reduce the carbon footprint of data processing.

##  Data Centres Under Water

Microsoft's "_Project Natick_" originally developed Underwater Data Centres between 2016 and 2020 by submerging a ship-full of data servers in the Atlantic near the UK Orkney Islands. 
That research is primarily being continued by the Chinese (they have more Data Centres than any other country). 

The underlying thinking is that the ocean provides continuous, immense cooling that no land-based system can rival.

Essentially, these are self-contained data servers locked inside a pressurized cylinder that is then sunk onto the ocean floor. 
Beyond a certain depth water temperature is constant (4 Celsius) and the constant flow of the ocean naturally dissipates heat away from the data centre without incurring any energy cost.  

Another, significant side-effect discovered by Microsoft is that replacing the air in the data centre with an inert gas like Nitrogen and stabilising temperature fluctuations significantly extended the "_mean time between failure_" (an important metric for maintaining computer components) by a factor of eight.

When you combine zero cooling costs, lower replacement costs, and the fact that nearly half the global population lives on a coastline (reducing latency), the ocean floor becomes a prime candidate for large scale data storage.
