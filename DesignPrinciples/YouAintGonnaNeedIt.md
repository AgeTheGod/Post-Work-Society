---
title: You Aint Gonna Need It
layout: default
parent: Design Principles
nav_order: 11
---
#   You Aint Gonna Need It (YAGNI)

"You Aint Gonna Need It" (YAGNI) is a core software development principle from Extreme Programming (XP) that states a Application Developer should never implement functionality or features based on assumed future needs, but only when the need is explicitly required.

When Software Engineers try to predict the future, they often over-engineer the software. This creates several unnecessary problems:
- Wasted Time: Coding and testing features that users might never actually want or use.
- Increased Complexity: Extra code makes the overall project harder to read, debug, and maintain.
- Technical Debt: Unused code still requires continuous updates and modifications during future refactoring.
- Delayed Releases: Spending time on "future-proofing" slows down the launch of essential, current requirements.

In Business Analysis (BA) and Requirements Definition, YAGNI means analysing and documenting _only the requirements for the stated needs of the business_. 
This prevents "Analysis Paralysis" (see [Iterate Don't Procrastinate](IterateDontProcrastinate.md)) and keeps the focus strictly on the [Minimum Viable Product (MVP)](MinimumViableProduct.md).

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Nice to Have                 | Stakeholders often request "nice-to-have" features during brainstorming sessions out of fear they won't get them later. |
| Designing "Edge Cases" First | Spending hours documenting a complex workflow for a scenario that only happens to 0.1% of users.                        |
 
In all cases the constantly asked question should be "Do we need this now or can it wait?"  

## YAGNI vs. Design For Change

Of course this doesn't mean that we should not be thinking ahead and planning for future changes i.e. Design for Change. 
However, any future-proofing should be based on _known_ requirements, not speculative ones and backed up with evidence.

For example, let's say we're building an e-commerce site for a local business i.e. a business that only accepts payments in a single currency. 
However client mentions that they might expand internationally next year.
At this point one of three things might happen...
1. You take the client's comment as a requirement and start building a Payments component to include a Currency Converter now
2. You build the checkout system purely in the local currency, but you also create a clear boundary in your code so that adding a currency converter later will be easy and won't require a complete rewrite
3. You ignore the comment and build the payment system based purely in the local currency (maybe even ignoring currency entirely because Money without Currency is just a Number).

Option 1 is a violation of YAGNI because the feature is speculative and not required for the immediate business needs and, most importantly, the client hasn't provided concrete evidence for this requirement or what it would be required to do.

However, and this might not bed immediately obvious, option 3 is also a violation of YAGNI because it ignores the client's comment and does not provide a clear path for future changes. 
"Expanding internationally" may not be an immediate requirement today, but it is a known _potential requirement_ for the future and should be considered in the design of the system.

## Related Principles

YAGNI is frequently paired with two other foundational software guidelines:
- [Keep It Simple](KeepItSimple.md)focuses on simplicity of design.
- [Design For Change](DesignForChange.md) encourages creating systems that can easily adapt to future requirements without major rewrites.

