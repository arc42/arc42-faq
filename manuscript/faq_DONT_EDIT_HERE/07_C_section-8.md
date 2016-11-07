{pagebreak}

### 8. Crosscutting concepts

{#q-C-8-1}
#### Question C-8-1: What is a crosscutting concept?

We use the term "concept" for rules, principles or other
decisions, guidelines, processes that influence one or more
elements of the architecture.

* Decisions, or concepts that cannot adequatly be assigned to a single building block
* Decisions or rules that influence several
  * building blocks
  * parts of the implementation
  * runtime scenarios
  * interfaces
  * several developers


{#q-C-8-2}
#### Question C-8-2: Our arc42 section 8 (on concepts) is a melting pot of information we couldn't put elsewhere? How can we keep an overview?

The variety of topics in section 8 might seem chaotic, but all topics contained have something in common: They are all _crosscutting_ (for an explanation, see [question C-8-1 (what is crosscutting)](#q-C-8-1)).

You shall remove (!) all concepts not relevant for your system (see [question C-8-3 (deal with many concepts)](#q-C-8-3)).

Then you can group/order the remaining topics, either to system-specific criteria or after the following proposal (based upon ideas by Stefan Zörner):

* **Business or domain aspects**: domain, entity or data models, the ubiquitous language from domain-driven design 
* **Architectural patterns**: What (recurring) patterns have been applied, and how?
* **Development**: Build and build management, code generation, configuration, (automated) testing, migration
* **Under the hood**: persistence, distribution, transactions, session-handling, caching, threading, exception and error handling, security
* **Interactions with users or external systems**: user interface aspects, i18n, validation, accessibility, communication, integration
* **Operations**: deployment, installation, monitoring


{#q-C-8-3}
#### Question C-8-3: How shall I deal with the multitude of potentially crosscutting topics?

At first, treat arc42 section 8 as a checklist and work iteratively:

1. Remove every topic that is not relevant for your system.
2. Prioritize the remaining subsections, criteria should be importance and risk.
3. Work on the highest priorities and briefly (!) document the corresponding decisions.

Many crosscutting concepts will be highly technical, therefore you document or specify those for developers. Source code with brief explanations can sometimes be sufficient - and can save you from writing awkward documents!

{#q-C-8-4}
#### Question C-8-4: How shall I describe my business-/domain model?

You have several options, shown in order of increasing effort and degree-of-detail

1. Create an (tabular) glossary of relevant business terms.
2. Create an informal outline, where you show data types and their relationships. Define the terms in a glossary.
3. Create a data or entity model (either as UML class diagram or Entity-Relationship diagram), where you show business entities with their attributes and relationsships. Define the terms in a glossary.
4. Define a _rich object model_, where you add methods, functions or services to the entity model.
5. Work according to the _Domain Driven Design_ (see [Evans-2004]): Create a ubiquitous domain language with several bounded contexts, model business entities and aggregates, use value objects, services, repositories and factories to enable communication within and about the domain. (Obviously this FAQ does not strive to provide detailed introduction to the fascinating topic of DDD, you have to look elsewhere[^domaindriven].)  

T>You should always define the meaning of the most important business terms in a glossary. Hopefully other stakeholders have already done that. Business terms are so easy to mis-interpret. You should make sure that does not happen within your system!

[^domaindriven]: Eric Evans: Domain-Driven Design (Addision Wesley, 2004): The original source, 700+ pages of dense content. Vaugn Vernon, another veteran of DDD, has written "Domain-Driven Design Distilled" (Addision Wesley 2016), with only 170 pages - brief intro.

{#q-C-8-5}
#### Question C-8-5: Are there any general rules how to describe a _concept_?

Often developers (or other technical people) have to _adhere_ or comply to concepts, or obey them. Therefore understandability, clarity, and applicability are primary goals, together with a shot of consistency, of course.

Some rules you might apply:

* Be practical and use source code examples to explain and demonstrate. Automated test can accompany the plain code, giving developers a feel _how to do_ things.
* Write your concepts in the form of _developer use cases_": "A developer wants to achieve XYZ" - and explain step by step what people have to do.
* Explain _reasons_ why the concept is like it is. If you deviate from established standards or procedures, explain why and how you came to your solution.
* You can combine text with static and dynamic diagrams to describe your more complicated concepts.
* Describe the applicability: In which or for what cases shall the concept be applied?
* Describe the limits: In what cases, under which circumstances will the concept fail or cease to work?
