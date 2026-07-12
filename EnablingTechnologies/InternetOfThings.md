---
title: Internet Of Things 
layout: default
parent: The Internet
nav_order: 4
---
#   Internet Of Things

    Note:
        I'm not going to explain the Internet here. 
        It's so ubiquitous that I'm assuming everyone knows what it is and what it is used for.

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

##  IoT State Machines

    ToDo: State Machines are not simple to explain. Might skip this.

##  How Taxonomic IoT Routing Works

In a standard internet setup, routers have to memorize millions of individual paths to find specific devices. 
This makes routing tables massive, slow, and expensive to run.

However, a global network using the Taxonomic IoT approach can keep their routing tables incredibly small and fast through a process called Prefix Aggregation (or summarization) combined with a technique called Hardware-Level Bit-Shifting.
Essentially, the routers only memorize the fixed structure of the physical architecture itself and never have to memorize the trillions of individual IoT-enabled devices 

The result is a 4-step process 

    ToDo: This is a very technical summary (though nothing like as complicated as the actual technical paper).
        Need to think about how to make this less technical.

### 1. Hierarchical Summarization (The ZIP Code Effect)

The primary way router tables stay small is that local routers do not need to know where individual devices are. 
They only route data based on the Static Half (Bits 0–63) of the address.
Think of it like sorting physical mail. 
A sorting facility in London does not care about your specific kitchen smart bulb; it only looks at the postal code so that a message gets delivered to that address.

- The Global Core Routers: Only look at Bits 0–15 (Region). Their routing tables contain just a few thousand entries (one for each geographic sector).
- The Regional Routers: Only look at Bits 16–39 (Owner/Organization). They forward all data for a specific organization to a single gateway link.
- The Campus/Local Routers: Only look at Bits 40–55 (Subnet).

Because of this strict hierarchy, a local router's table only needs one single entry to cover billions of devices. 
Instead of listing every device, the table simply says:

    "If the first 64 bits match 2001:00A2:001F:004B::/64, send it down Port 3." 

If the message matches that rule then it continues its journey but if it fails then everything else is ignored.

### 2. Line-Rate Filtering via Subnet Masks

When a data packet arrives at a local router, the router uses an electronic trick called AND-masking performed directly on its silicon microchips (using ASICs—Application-Specific Integrated Circuits).
Instead of reading the whole 128-bit text string, the chip overlays a binary mask onto the incoming address.

Incoming Address:  2001:0db8:85a3:0001:0102:8a2e:0370:7334
Router's Mask:     FFFF:FFFF:FFFF:FFFF:0000:0000:0000:0000
Instant Result:    2001:0db8:85a3:0001 (Match Found! Forward immediately)

### 3. Class-Based Traffic Prioritisation (No Database Needed)

Once the packet arrives inside the local network, the router has to decide how fast to process it. 
In a traditional network, a router must check a complex database of rules (Access Control Lists) to see if a device or specific message is high-priority.

With a taxonomic address, the router skips the database entirely by looking at Bits 56–63 (Network Priority & Safety Class):
- The router's hardware is hardwired with a rule: If bits 56–63 equal 0xAA (Critical Safety), put this packet in the front of the queue.
- If those bits equal 0xFF (Low-Priority Consumer Tech), the packet is held back if the network is busy.

Hence, the router can prioritize life-saving machinery or shutdown commands instantly without looking up a single database record.

### 4. Hardware-Level Dynamic Sorting (TCAM)

What happens when the packet finally reaches the geographic location and needs to find the correct device class (like separating drones from climate sensors)?
Local switches use a specialized type of high-speed memory called TCAM (Ternary Content-Addressable Memory). 
TCAM allows the router to search its entire table for the Class ID (Bits 64–71) in a single clock cycle (the faster the CPU the quicker this happens).

A match at this point identifies a specific device to which the message is passed and the specific device then processes whatever instruction it has been given (assuming it is a legal instruction according to the relevant Device State Machine)
