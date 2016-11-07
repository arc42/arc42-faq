{pagebreak}

### 6. Runtime view

{#q-C-6-1}
#### Question C-6-1: What is a runtime scenario?

The runtime view describes the behavior and interaction of the system’s
building blocks with one or more _scenarios_.

A runtime scenario shows specific interactions or behaviors of building blocks or building block instances, either with each other or external elements.

It shows _how_ the system fulfills certain tasks.

{#q-C-6-2}
#### Question C-6-2: What do I document in the runtime view?

How the system executes, the dynamics of the system, its behavior in terms of its building blocks.

The following types of scenarios might be relevant for you:

* The most important use cases, features or functions
*	System startup
*	The systems´ behavior on its most important external interfaces
* The systems´ behavior in important error or failure situations

A>It's important that the runtime view shows which building block is responsible for what activities or functions within the system. Therefore the mapping of (static) blocks to activities, process steps, functions or other dynamic elements is important.

{#q-C-6-3}
#### Question C-6-3: How can I describe scenarios or execution flows?

You have several options (many more than for the static building block view..).
The following list is ordered by increasing documentation and maintenance effort. Options further down that list are more fine-grained and usually contain more
details.

1. Document scenarios in plain text by enumerations or numbered lists. Include precise hints which building block executes which step(s) of use cases, processes or functions.
2. Use activity diagrams or flowcharts with swimlanes.
3. Use UML sequence diagrams. They are time-consuming to create and maintain with most interactive tools, but are an excellent means to show the mapping between building blocks and their actions. See [question F-10 (tools for sequence diagrams)](#q-F-10) for some tips on tools.

UML has some additional options (e.g. state transition or object diagrams) to describe behavioral aspects of systems or building blocks. Those can be sometimes be useful, but are less often used that activity- or sequence diagrams.

{#q-C-6-4}
#### Question C-6-4: What are partial scenarios?

Partial scenarios describe parts or extracts of complete scenarios or processes. They show only interesting, difficult, risky or important aspects of some _greater_ process.

Concentrating on these _essentials_ brings several benefits:

* You avoid trivial parts of scenarios
* You work more economically by leaving out unneccessary, non-important or low-priority aspects. That saves time/effort in creating and maintaining documentation!
* Smaller scenarios might be easier to understand (if (!) you make very clear which parts of the overall scenario you left out!)

A risk of partial scenarios might be consumers that don't understand the prerequisites or preconditions of a partial scenario. Use annotations within your diagrams to explicitly clarify such required knowledge or facts.

In the figure shown below, you find a complete scenario first, and a nice partial scenario as an extract afterwards.

{width=50%}
![Long and mostly boring scenario](images/faq/C-Sections/long-and-mostly-boring.png)

As you see, the first interactions seem quite trivial. Therefore, we can simple leave them out in a partial scenario:


{width=30%}
![Corresponding partial scenario](images/faq/C-Sections/short-and-interesting.png)|


{#q-C-6-5}
#### Question C-6-5: Which scenarios shall I describe or document?

The following types of scenarios are candidates for runtime scenarios:

* The general case (aka the _rule_) of the most important use cases, features or functions.
* Important interactions with external systems, neighbours or user categories.
* Dynamic behavior of important external interfaces.
* Interactions that affect important quality goals or requirements.
* Error or failure conditions that might influence overall system behavior.
* Bootstrap-, startup or shutdown procedures, especially in distributed systems.
* Interactions that somehow deviate from _normal_ stakeholder expectation, especially deviate from developer expectation.
* Interactions that work in non-standard ways.
* Scenarios or processes that are subject to timing constraints
