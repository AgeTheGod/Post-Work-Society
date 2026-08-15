---
title: What Are Design Principles
layout: default
parent: Design Principles
nav_order: 1
---
#   What Are Design Principles?

I'm a big fan of Iterative Development ([Wikipedia](https://en.wikipedia.org/wiki/Iterative_and_incremental_development)) in the belief that long-running projects will be subject to many changes during their lifecycle so not conducive to "**Big Design Up-Front**" ([Wikipedia](https://en.wikipedia.org/wiki/Big_design_up_front)).

This is the reason why back in the days when I did a lot of consultancy one of the up-front questions I asked was "_What does good look like?_" (and, equally, "_What do we think is bad?_") irrespective of what any potential solution might be.
This is quite a fundamental question because there's no point in proposing any solution that is unsustainable over time or is not scalable or that it is not reproducible or that it is not maintainable.

Essentially, finding out that something is not fit for purpose after a lot of time and effort has been expended on a solution is a very expensive way to find out.

So any piece of work should have some up-front Design Principles that constrain or limit what we are trying to achieve and it's the answer to the question "_What does good look like?_" that produces the set of Principles that we should be considering.

Design Principles also tend to be a bit more abstract that Objectives or Requirements and hence are not so easy to define in a concrete way.
They tend to include words like "maintainable", "scalable", "reproducible", "sustainable" and testing whether those things have been achieved is not a true or false outcome.
They also tend to be difficult to measure

Defining what good looks like also leads into answering the question "_What are we optimizing for?_" because once we have a set of principles we also have a set of things that need to be balanced against each other and potentially resulting in trade-offs.
When that happens we need to be able to make decisions about what is more important and what is less important and hence what we are optimizing for.

We tend not to think about principles in the context of defining a Socio-Economic Framework such as the Post Work Society (or at least nobody has done so in any of the publications I've read on this subject) but I've always found them useful.

Plus, like anything else, any changes in the underlying Design Principles will have a knock-on effect on the rest of the system and hence need to be carefully considered before changing them.
This can only be done if they are clearly stated and agreed upon up-front.

##  Some Examples of Design Principles

### The "Ilities"

The "ilities" (often called "_Quality Attributes_" or "_Non-Functional Requirements_") are a group of words in software engineering and system Design Principles that end in "-ility".

The Core "Ilities" of Modern Systems are...
- Scalability: The ability to handle an increasing workload without breaking or lowering performance.
- Flexibility / Extensibility: The ease with which a system can be modified to add new features or adapt to change.
- Sustainability: The ability of a system to run indefinitely without draining resources, budgets, or energy.
- Reliability: The ability of a system to consistently perform its required functions without failure.
- Availability: The percentage of time a system is up, running, and accessible to users when needed.
- Maintainability: How easy it is to find bugs, fix errors, and update the codebase without breaking things.
- Security: The ability of a system to protect data and resist malicious attacks or unauthorized access.
- Usability: The ease with which a human user can learn, operate, and navigate the system interface.
- Portability: The ease with which software can be moved from one environment or operating system to another. [4, 5]

When designing an application or system you rarely get all the "ilities" in a single solution and System Architects must constantly balance them because optimizing for one often hurts another. 
For example:
- Increasing Security (more encryption, extra logins) often decreases Usability (slower for the user).
- Increasing Flexibility (making code abstract to handle future changes) can decrease Maintainability (making it harder for a new developer to understand).

Given that these are mostly abstract qualities they can be applied to any system, not just software, and hence are a good starting point for defining the Design Principles of the Post Work Society. 
(Not to mention that this is the list that I'm most familiar with from my own experience.)

### Mike Gancarz: The UNIX Philosophy

In 1994, Mike Gancarz published "_The UNIX Philosophy_" based on his own Unix development at DEC in the 1980s.
The book focuses on porting UNIX to different computers during the Unix wars of the 1980s and describes his philosophy that portability should be more important than the efficiency of using non-standard interfaces for hardware and graphics devices.

The nine basic "tenets" he claims to be important are
- Small is beautiful.
- Make each program do one thing well.
- Build a prototype as soon as possible.
- Choose portability over efficiency.
- Store data in flat text files.
- Use software leverage to your advantage.
- Use shell scripts to increase leverage and portability.
- Avoid captive user interfaces.
- Make every program a filter.

Another list that has extensive applicability to many other kinds of application development (not just UNIX) and underpin many of the more modern design approaches such as Domain Driven Design (DDD) and Microservices.

### Dieter Rams: 10 Principles for Good Design

Developed in the late 20th century by industrial designer Dieter Rams, these principles are famously known as the "10 Commandments" of product design.
- Good design is innovative: Technology always evolves, offering new opportunities for design.
- Good design makes a product useful: It emphasizes utility and ignores anything that distracts from it.
- Good design is aesthetic: Objects we use every day affect our well-being.
- Good design makes a product understandable: It makes the product's structure clear or even "talk".
- Good design is unobtrusive: Products are tools, not decorative art objects.
- Good design is honest: It does not make a product look more valuable or powerful than it is.
- Good design is long-lasting: It avoids being fashionable so it never looks outdated.
- Good design is thorough down to the last detail: Care and accuracy show respect toward the user.
- Good design is environmentally friendly: It conserves resources and minimizes physical pollution.
- Good design is as little design as possible: Focuses purely on the essentials—less, but better. 
