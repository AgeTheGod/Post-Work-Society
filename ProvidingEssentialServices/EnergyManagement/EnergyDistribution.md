---
title: Energy Distribution Technologies
layout: default
parent: Sustainable Energy
nav_order: 3
---
#   Energy Distribution Technologies

Energy distribution works on the same basic design principles as Telecommunications with massive "backbones" designed to move high volumes of energy over long distances with lower power direct connections that that deliver electricity directly to homes and businesses.

In most countries Energy Distribution is a well established mature industry - in the UK it was first mandated in 1926 and officially completed in 1938 but many other European countries quickly followed in the 1940's.

These were all "national grids" but following these successes some countries then began plugging them into each other
- 1951 (The UCPTE): France, Germany, Italy, Austria, Belgium, Luxembourg, the Netherlands, and Switzerland officially interconnected their national grids. This created the Union for the Coordination of Production and Transport of Electricity, forming the foundation of today's Continental European Grid—the largest synchronous electrical network in the world.
- 1963 (Nordel): The Scandinavian countries (Norway, Denmark, Finland, and [Sweden](https://www.google.com/search?kgmid=/m/0d0vqn)) successfully linked their national transmission systems to form a unified Nordic power block.

These are the "standard" High Voltage Grids suitable for distributing energy approximately 500km between producer and consumer. 

## Ultra-High Voltage (UHV) Distribution

Electric currents lose power over distance which limits the distance between the electricity producer and the electricity consumer.

This is not particular significant for shorter distances between producer and consumer but is an issue for much larger land masses, such as China, Brazil and India where the distance between producer and consumer can be 1000's of kilometres even High Voltage distribution suffers a significant power loss.
The core principle is the equation...

    Power(P) = Voltage(V) × Current(I)

where...
- To transmit a fixed amount of electrical power (P), increasing the voltage (V) allows the electric current (I) to decrease.
- Line losses (energy wasted as heat) are proportional to the square of the current (I²R).

Ultra-High Voltage (UHV) the power that is transmitted over immense distances with minimal energy loss.
Formally, UHV is defined as systems operating at alternating current (AC) voltages of 1,000 kV (1 million volts) or higher, and direct current (DC) voltages of 800 kV or higher.

This is significant fron the Sustainable Energy perspective because it means that mega-scale renewable energy built far away from populated areas become viable.

## Wireless Power Transmission

Since the first electrical grid was switched on, one physical rule has dictated the design of every city, home, and appliance. 
Electricity needs a wire to connect an electrocal device to a power source. 
That requirement is why billions of tons of copper are buried under our streets and strung between wooden poles and every house is wired up with multiple electric power sockets. 

Wireless Power Transmission (WPT) is a technology that allows electrical energy to be transferred from a power source to an electrical load across an air gap without using physical wires or cables.
The concept relies on a transmitter converting electricity into a time-varying electromagnetic field (or wave), which travels through space to be captured by a receiver and converted back into usable electrical current.

WPT is split into two primary fields based on distance: Near-field (short-range) and Far-field (long-range).

- Near-Field (Magnetic Coupling) sends energy over distances ranging from millimetres to a few centimetres.
  - **Inductive Coupling**: Electricity passes through a transmitter coil, creating a localized magnetic field. When a receiver coil is placed nearby, the magnetic field induces an electric current in it. This is the basis of the Qi standard used globally.
  - **Resonant Inductive Coupling**: Both coils are tuned to the exact same magnetic frequency. This allows energy to transfer more efficiently over slightly larger gaps (up to a couple of meters).
- Far-Field (Power Beaming) beams energy over hundreds of meters or even kilometres, requiring a direct line of sight.
  - **Microwave Power Beaming**: Electricity is converted into high-frequency microwaves, beamed via an antenna, and captured by a specialized receiving antenna called a rectenna. 
  - **Laser Power Beaming**: High-intensity laser beams shoot light energy across vast distances to a photovoltaic receiver (similar to a solar panel), which converts the light back into electricity.

WPT has evolved from low-power consumer tech to heavy industrial and energy grid pilots.

|            |                                  |                                                                                                                                                                                                                                  |
|------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Near-Field | Smartphone & Wearable Users      | Millions use inductive charging pads daily to power Apple, Samsung, and Google devices                                                                                                                                           |
|            | Household Electronics            | Devices like electric toothbrushes and sleek kitchen appliances have used sealed, waterproof inductive charging bases for decades to eliminate electrocution risks in wet environments.                                          |
|            | Implantable Medical Devices      | Advanced pacemakers, insulin pumps, and artificial hearts use WPT to recharge safely through human skin. This completely eliminates the need for wires exiting the body, preventing dangerous surgical infections.               |
| Mid-Range  | Automated Guided Vehicles (AGVs) | Automated warehouse robots and forklifts pull up over wireless floor pads to top up their batteries dynamically. This eliminates wear-and-tear on physical plugs and avoids hazardous sparks.                                    |
|            | Industrial Sensor Networks       | Tech hubs like Finland rely heavily on WPT to continuously power remote sensors in heavy machinery or sealed environments without needing regular battery replacements.                                                          |
|            | Hands-Free EV Charging           | Pioneered by companies like WiTricity and integrated by major auto manufacturers, drivers park directly over a pad embedded in a garage floor or driveway to charge their car automatically.                                     |
| Far-Field  | Terrestrial Grid Support         | National Grid in the UK launched active pilot studies to see if far-field microwave beaming can replace heavy cables to route emergency power during storms or link remote island renewable generators.                          |
|            | Space-Based Solar Power (SBSP)   | Space organizations and companies like Space Solar are actively building systems intended to collect continuous, intense solar energy via satellites in orbit and beam it directly down to Earth grid stations using microwaves. |

