---
title: Internet Of Things 
layout: default
parent: Enabling Technologies
nav_order: 4
---
#   Internet Of Things

    Note:
        I'm not going to explain the Internet here. 
        It's so ubiquitous that I'm assuming everyuone knows what it is and what it is used for.

The "**Internet Of Things**" sounds like it should be a definition of terms but is actually an enabling technology.

The Internet of Things (IoT) refers to a massive network of everyday physical objects that connect to the internet and exchange data with other systems. 
Basically, it describes a world where ordinary things are identifiable and have digital "brains" that can talk to each other without human interaction.

An IoT system relies on a simple, three-step process to bring everyday items to life:

1. Sensing Data: Physical items are built with small sensors. These sensors act like digital eyes and ears, measuring things like temperature, motion, light, or location.
2. Sending Data: The device uses a network connection (like Wi-Fi, 4G/5G, or Bluetooth) to transmit that information to the cloud.
3. Taking Action: Software analyzes the data and makes an intelligent choice. It might trigger an alert, change a setting automatically, or show the information on a smartphone app.

The bottom line is that the Internet Of Things makes life and many activities much more efficient.
It looks simple (and it is) but has an unending number of potential applications for automating processes that previously required human intetvention.
For example...
- Smart Homes: Thermostats that learn your schedule, lightbulbs you turn off with your phone, and doorbells that stream video to your screen.
- Wearable Tech: Fitness trackers and smartwatches that measure your heart rate and count your daily steps.
- Smart Cities: Traffic lights that adjust their timing based on real-time road congestion to reduce traffic jams.
- Industrial IoT (IIoT): Factory machines that warn workers they are about to break down before they actually stop working.


##  IoT Identifiers

A critical part of the Internet of Things is the IoT Identifier i.e. the unique value assigned to every physical device that is capable of issuing any kind of internet communication so that we can disambiguate any single device from every other device. 

Currently the Internet Of Things uses a 16-byte IPv6 address which is a number so staggeringly big that it's difficult to explain and for all practical purpose they are an infinite resource..

Unfortunately the current IPv6 specification has shortcomings (most significantly the IoT device identifiers for an IoT-enabled device are not immutable and can change over time) and alternative specifications have been proposed to structure an IPv6 address as a hierarchical taxonomy—where specific bytes encode "what it is," "who owns it," and "what it does".

However, because an IPv6 address contains 128 bits, engineers have realized they can treat it as a tiny database row instead of just a randomly generated number. 
As a result several prominent systems and protocol standards have been proposed or deployed that mirror this biological taxonomy approach.
Some of the proposed alternatives are...

| Proposed Protocol                        |                                                                                                                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Object Name Service (ONS)                | The Electronic Product Code (EPC) is the universal standard taxonomy used to classify physical goods (acting like a hyper-advanced barcode). This proposal embeds the EPC code directly into the IPv6 address. |
| Segment Routing v6 (SRv6)                | Developed by the Internet Engineering Task Force (IETF) the SRv6 breaks the 128 bits into strict semantic zones called Locators and Functions.                                                                 |
| EIB/KNX over IPv6                        | In industrial engineering and smart cities, protocols like European Installation Bus (EIB) have been adapted into IPv6 Addressing Proxies to manage massive building components.                               |
| Location-Based Address Autoconfiguration | Developed for massive wireless sensor networks like a planet-wide single integrated network MPIPA (Multi-dimensional Location-Based IPv6 Addressing) and Tree-Based Hierarchical Addressing.                   |

It should be noted that these proposals are not mutually exclusive and it's easily possible that different kinds of devices may use different protocols for defining the device identifier. 
This is known as Semantic Addressing or Context-Aware Addressing (I used a very simple variant of this when I worked on Data Entitlements for Reuters Market Data).

In a unified global network using a taxonomic approach has the advantage that firewalls and routers become incredibly simple.
