{pagebreak}

{#section-vii-D}
## D Questions on modeling

Here we collect questions regarding UML and other modeling notations, plus general
questions regarding understandability and consistency of models.

{#q-D-0}
#### Question D-0: Why do I need a _model_? I have source code.

For cute, neat, small and mignion systems, you won't need any model.

For larger, distributed, risky or otherwise complicated systems, architectural
information in addition to source code can support both development and
evolution of systems.

_Models_ in our sense are arbitrary abstractions of architecture or
architecture decisions, relating to either structure or (crosscutting) concepts.

Examples of such _models_ we found useful:

* Context of the system, showing external neighbours and interfaces.
* Building blocks (e.g. subsystems, modules or such), representing potentially
large chunks of source code.
* Other views, e.g. runtime or deployment
* A domain model, representing the core of your domain.

Models can be expressed using diagrams plus explanations, but might also
be textual or tabular...


{#q-D-1}
#### Question D-1: What alternatives to UML exist for architecture models?

Several alternatives compete with UML, the list below gives an overview
(just an arbitrary selection, not exhaustive):

* informal box- and line diagrams. They can be helpful and are often ok, but
please explain your notation, otherwise your diagrams are open for
(mis-)interpretation.
* Fundamental-Modeling-Notation (FMC), an (academic) approach to communicate
dynamic systems with block-diagrams, petri-nets and entity-relationship diagrams.
See the [FMC notation reference](http://www.fmc-modeling.org/notation_reference)
for details. FMC is rarely used in business or industrial systems, although
it's quite promising.
* [SysML](http://sysml.org/) is an UML dialect, created to support systems engineering.
Supported by numerous modeling tools, but in my opinion not practically relevant.
* Simon Browns pragmatic [C4](http://static.codingthearchitecture.com/c4.pdf) model of
software architecture description.

{#q-D-2}
#### Question D-2: How to arc42 and UML relate to each other?

They don't really need each other. You can very well use arc42
with and without UML.

Graphical modelling with UML does by no means make you a better architect,
nor does it (automatically) improve your systems.

You might use UML to describe or specify the following aspects of your
architecture:

* static structure (building block view)
* runtime behavior or runtime scenarios (runtime view)
* deployment or infrastructure

See also [question B-3](#q-B-3).


{#q-D-3}
#### Question D-3: How can I use UML to communicate a hierarchy of building blocks?

Component- and package diagrams can communicate hierarchies, as both UML components
and packages can be _nested_.

<t.b.d: example>

{#q-D-4}
#### Question D-4: How can I describe interfaces with UML?

The trivial option (usually not recommended):
Just draw a line between two boxes to indicate that in interface between those two exist.

If you need more _serious_ options, you have at least the following
options (orderd by required effort for creating and maintaining such descriptions):

1. Give the line a label (to make it referencable) and explain its meaning
in a table below the diagram. This should be sufficient for many non-safety-critical systems.
2. Use the _provided/required_ notation (aka "ball/socket"), explicitely
denoting which services/data/events the providing building block offers. There's a nice
explanation by [Martin Fowler](http://martinfowler.com/bliki/BallAndSocket.html) on this option.
3. Use distinct interface building blocks.
4. Use ball-and-socket notation in combination with port symbols.

The following figure shows options 1-4.

{width="70%"}
![Various options for interfaces in UML](images/faq/interface-options.png)


{#q-D-5}
#### Question D-5: What can I use UML ports for?

Ports, these little rectancular boxes attached to components, packages or even nodes,
represent an (optionally named) collection of interfaces. They come in handy for
several reasons:

* Ports can support the detailed mapping of internal resp. external view of white-
and blackboxes: Use ports to describe which _internal_ building block of any
whitebox communicates with an interface of the corresponding blackbox. In the following
diagram, Foo communicates with Bar over a port. In the refining whitebox,
the component BarA handles that interaction.

{width="50%"}
![Ports to show mapping between blackbox and its refinement](images/faq/ports-for-mapping.png)

* I (Gernot) often used ports to denote the transmission protocoll for a particular
interface: For an interface (e.g. _inFoo_) I can show that its available over http,
https and ftp by attaching the same interface ball/socket to several ports,
each port representing a distinct "access option" (ftp, http, https)...

  Note: This is _not_ what the original inventors of UML intented...

{width="50%"}
![Ports to show access channels or protocols](images/faq/ports-and-channels.png)

* In hardware- and deployment diagrams, ports can represent input/output channels,
network adapters, virtual networks, IP-addresses or similar .

{#q-D-6}
#### Question D-6: How can I improve the _understandability_ of my diagrams/models?

Understandable diagrams contain 5-15 elements with their relationships - _normal_
people simply cannot grasp more than that number.

If you have overloaded or large diagrams, reduce the number of elements
by _abstraction_:

* Aggregate several elements into a named blackbox. These elements should be
cohesive, they should somehow _belong together_. The criteria should be
an explicit decision.
* Refrain from showing loads of details, e.g. attributes or methods of single classes.
Those details can often be left to source code.
* Especially in runtime scenarios, don't always start with the beginning of a scenario,
but _dive-right-into_ the interesting parts.


A>#### Your question has not been answered?
A>Tell us:
A>
A>* via [email](mailto:info@arc42.de) to info@arc42.de or
A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
