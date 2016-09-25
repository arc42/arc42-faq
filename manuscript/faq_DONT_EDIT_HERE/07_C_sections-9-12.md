
### 9. Architecture decisions

{#q-C-9-1}
#### Question C-9-1: What kind of decisions shall I describe or document?

<t-b-d>

{#q-C-9-2}
#### Question C-9-2: How can I document an architectural decision?

<t-b-d>

{#q-C-9-3}
#### Question C-9-3: What's an _Architecture Decision Record_ (ADR)?

<t-b-d>

{#q-C-9-4}
#### Question C-9-4: How can we handle a _large number_ of architecture decisions?

Create a blog (RSS-feed) and write a brief entry for your important decisions.
Tag those with labels (e.g.: frontend, backend, SAP-interface or similar),
so stakeholders can _filter_ them.

Such a blog shows the history of your system quite well. You can combine
the blog with the idea of _architecture decision records_ (see [question C-9-3](#q-C-9-3)).


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
  quality trees.
  * The quality of a specific system can be described by a _specific_
  quality tree (see the example below).

  {width=60%}  
  ![Sample Quality Tree](images/faq/QualityTree.png)


{#q-C-10-4}
#### Question C-10-4: Are there samples for quality scenarios?

<t-b-d>


### 11. Risks and technical debt

{#q-C-11-1}
#### Question C-11-1: What are _risks_ and _technical debt_?

<t.b.d.>


### 12. Glossary
<t.b.d.>
