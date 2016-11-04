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

<t-b-d>

{#q-C-6-5}
#### Question C-6-5: Which scenarios shall I describe or document?

<t-b-d>
