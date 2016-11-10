{pagebreak}

### 9. Architectural decisions

In software engineering literature you find both "architecture decision" and "architectural decision".

{#q-C-9-1}
#### Question C-9-1: What kind of decisions shall I describe or document?

Describe or document the following kind of decisions:

* risky
* with expensive consequences
* with long-lasting effects
* affecting either
  * a large number of stakeholders
  * very special or important stakeholders
* that took a long time or much effort to decide
* astonishing

>(document) architecturally significant" decisions: those that affect the structure, non-functional characteristics, dependencies, interfaces, or construction techniques.
>
>Quoted from [Michael Nygard](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)

{#q-C-9-2}
#### Question C-9-2: How can I document an architectural decision?

* Write a blog for your decisions, every decisions becomes a blog post.
* Use a text format similar to an (Alexandrian) pattern, like explained in [question C-9-3 (Architecture Decision Record)](#q-C-9-3).
* For important decisions, the following topics might be interesting:
  * subject of the decision
  * affected stakeholders
  * decision criteria (with priorities)
  * alternatives
  * evaluation of alternatives for the various criteria
  * who took the decision?
  * reason for chosing _this_ alternative in favor of others

{#q-C-9-3}
#### Question C-9-3: What's an _Architecture Decision Record_ (ADR)?

In [2011 Michael Nygard proposed](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) to document important architecture decisions in the following pattern-like format:

* Title: A short phrase with an ID, e.g. "ADR 9: LDAP for Multitenant Integration"
* Context: Forces at play, including technological, political, social, and project organizational. Forces might be conflicting.
* Decision: How do we deal with these forces, what do we do.
* Status: A decision may be "proposed" (if stakeholders haven't yet agreed), or "accepted" (once it is agreed). Later it might be marked "deprecated" or "superseded" (you might include a reference to its replacement).
* Consequences: What happens after the decision has been applied. All consequences should be listed here, not just the "positive" ones. A particular decision may have positive, negative, and neutral consequences.

The ADR format lacks decision criteria, which I (Gernot) sometimes regard as really important... but maybe I'm prejudiced.

{#q-C-9-4}
#### Question C-9-4: How can we handle a _large number_ of architecture decisions?

Create a blog (RSS-feed) and write a brief entry for your important decisions. Tag those with labels (e.g.: frontend, backend, SAP-interface or similar), so stakeholders can _filter_ them.

Such a blog shows the history of your system quite well. You can combine
the blog with the idea of _architecture decision records_ (see [question C-9-3](#q-C-9-3)).

{pagebreak}

### 10. Quality scenarios

{#q-C-10-1}
#### Question C-10-1: What is _Software Quality_?

(from IEEE Standard 1061): Software quality is the degree to which software possesses a desired combination of attributes. This desired combination of attributes need to be clearly defined; otherwise, assessment of quality is left to intuition.

{#q-C-10-2}
#### Question C-10-2: What is a _quality scenario_?

Quality scenarios document required quality attributes.
They help to describe required or desired qualities of a system, in pragmatic and
informal manner, yet making the abstract notion of “quality” concrete and tangible.

  {width=50%}
  ![Generic form of (Quality) scenario](images/faq/schematic-Q-scenario.png)

  * Event/stimulus: Any condition or event arriving at the system
  * System (or part of the system) is stimulated by the event.
  * Response: The activity undertaken after the arrival of the stimulus.
  * Metric (response measure): The response should be measurable in some fashion.

  There are different kinds of scenarios:

  1. Usage scenarios: The system is used (any use case or system function is executed).
    Such scenarios describe how the system _behaves_ in these cases, e.g. in terms of
    runtime performance, memory consumption, throughput or similar.
  2. Change (or modification) scenarios: Any component within the system, its environment
    or its operational infrastructure changes or is being changed.
  3. Failure scenarios: Some part of the system, its infrastructure or neighbors fail.


{#q-C-10-3}
#### Question C-10-3: What is a _quality tree_?

(syn: quality attribute utility tree). A hierarchical model to describe
product quality: The root "quality" is hierarchically refined in _areas_ or
topics, which itself are refined again. Quality scenarios form the leaves of
these tree.

  * Standards for product quality, like ->ISO 25010, propose _generic_
  quality trees. You find this _generic_ quality tree in
  [question C-1-2 (quality goals)](#q-C-1-2).
  * The quality of a specific system can be described by a _specific_
  quality tree (see the example below).

  {width=60%}  
  ![Sample Quality Tree](images/faq/QualityTree.png)


{#q-C-10-4}
#### Question C-10-4: Are there examples for quality scenarios?


* A new price calculation rule can be added to the pricing engine within 4 hours.
* The daily sales report for a single product category is generated within 10 seconds.
* When storage devices fail, the system gracefully shuts down (instead of crashing uncontrollably).
* The web client requires <5MB per browser session.
* Should the system run out of memory while processing the xyz algorithm, it will not crash, but will report the situation to an administrative user, stop the xyz process and return control to the interactive user within 30 seconds.
 

### 11. Risks and technical debt

{#q-C-11-1}
#### Question C-11-1: What are _risks_ and _technical debt_?

**Short answer**: The currently known problems.

**Longer answer**

: The known risks (things that might become problems) and problems in the system, its related organizational, operational and development processes. They can refer to source code, structures, concepts,
decisions and all other aspects of the system.


T>It's useful for development teams to have an overview of currently known risks and problems, so it can actively _manage_ the development and evolution of the system.


### 12. Glossary

You should ensure that all participating people have a _common_ understanding of the important business (and technical) terminology which they use in context with the system.

The glossary is one manifestation of the general rule of "better explicit than implicit".




A>#### Your question has not been answered?
A>Tell us:
A>
A>* via [email](mailto:info@arc42.de) to info@arc42.de or
A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
