---
title: Principles
layout: default
nav_order: 3
---
#   Principles

In normal Application Development the Objectives or Requirements define the capability that we're trying to deliver and the success criteria (and we'll state those when we need to) and are generally quite concrete and measurable.
With Objectives or Requirements we can state what is required in a very specific way e.g. "Implement a new feature that allows users to do X" and we can clearly test whether that has been achieved or not.

There are, however, an additional set of characteristics that we are trying to achieve that are not so easy to define in a concrete way and hence are not so easy to measure.
These are what we would normally refer to as **Non-Functional Requirements** that define the quality of the solution and hence whether it is fit for purpose. 
They are also what I'm referring to as **Principles** because they define general characteristics that we are looking for in any solution.

Back in the days when I did a lot of consultancy one of the up-front questions I asked was "_What does good look like?_" (and, equally, "_What do we think is bad?_") irrespective of what any potential solution might be.
This is quite a fundamental question because there's no point in proposing any solution that is unsustainable over time or is not scalable or that it is not reproducible or that it is not maintainable.
Essentially, finding out that something is not fit for purpose after a lot of time and effort has been expended on a solution is a very expensive way to find out.

Any piece of work should have some up-front Principles that constrain or limit what we are trying to achieve and it's the answer to the question "_What does good look like?_" that produces the set of Principles that we should be considering.

Principles tend to be a bit more abstract that Objectives or Requirements and hence are not so easy to define in a concrete way. 
They tend to include words like "maintainable", "scalable", "reproducible", "sustainable" and testing whether those things have been achieved is not a true or false outcome.

Defining what good looks like also leads into answering the question "_What are we optimizing for?_" because once we have a set of principles we also have a set of things that need to be balanced against each other and potentially resulting in trade-offs.
When that happens we need to be able to make decisions about what is more important and what is less important and hence what we are optimizing for.

We tend not to think about principles in the context of defining a Socio-Economic Framework such as the Post Work Society (or at least nobody has done so in any of the publications I've read on this subject) but I've always found them useful.

Plus, like anything else, any changes in the underlying principles will have a knock-on effect on the rest of the system and hence need to be carefully considered before changing them. 
This can only be done if they are clearly stated and agreed upon up-front.

Written Principles, once established, also create stability by ensuring that we don't keep changing direction when the next big thing comes along or keep searching for perfect solutions that do not exist and hence will never be achievable.

Hence I included this section because I believe that if these are not stated (and agreed upon) up-front then eventually the system being developed will deteriorate into chaos because different parts get built to a different set of underlying principles and eventually inconsistency breaks the system.

##  Core Principles

|                                                    |                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Prioritizing People](PrioritizingPeople.md)       | A Society is composed of People and it's the People that should receive the most benefit from Society | 
| [Sustainable Services](SustainableServices.md)     |                                                                                                       |
| [Scalable Solutions](ScalableSolutions.md)         |                                                                                                       | 
| [Reproducible Solutions](ReproducibleSolutions.md) |                                                                                                       |
| [Minimized Maintenance](MinimizedMaintenance.md)   |                                                                                                       |

##  Design Principles

I'm a big fan of Iterative Development ([Wikipedia](https://en.wikipedia.org/wiki/Iterative_and_incremental_development)) in the belief that long-running projects will be subject to many changes during their lifecycle so not conducive to "**Big Design Up-Front**" ([Wikipedia](https://en.wikipedia.org/wiki/Big_design_up_front)).

However, to make Iterative Development work it's important to establish and follow a number of key principles as part of the development process.
The single most fundamental principle Iterative Development is...

    The only sign of success is a working solution that is being used by real people in the real world.

That's it and if it's not that then all you have is "Slideware" (software that only looks good on paper) and all the other buzzwords that are used to try to make it sound like you are doing something useful when in fact you are just wasting time and resources iterating on something that does not exist.

| Principle                                                 | Summary                                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Evolution Not Revolution](EvolutionNotRevolution.md)      | Don't try to change everything at once, but instead evolve and improve over time. The core (unsaid) principle of iterative development.                                                    |
| [Just Good Enough](JustGoodEnough.md)                      | Solutions do not have to be perfect, they just have to be good enough to meet the needs of the people that are using them.                                                                 |
| [You Ain't Gonna Need It](YouAintGonnaNeedIt.md)           | Don't implement something until you actually need it.                                                                                                                                      |
| [Iterate Don't Procrastinate](IterateDontProcrastinate.md) | Don't wait to implement something until you have a perfect solution, but instead iterate and improve over time.                                                                            |
| [Keep It Simple, Stupid](KeepItSimple.md)                  | is another principle that is often cited in software development but I don't think it is as important as the others because it is more of a design principle than a development principle. |
| [ Minimum Viable Product](MinimumViableProduct.md)         | The minimum viable product is the smallest possible solution that can be implemented to meet the needs of the people that are using it.                                                    |
| [ Design For Change](DesignForChange.md)                   | Design solutions that can be easily changed and adapted over time as the needs of the people that are using them change.                                                                   |
| [Fast, Good, Cheap](FastGoodCheap.md)              |         | 
