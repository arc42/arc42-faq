{pagebreak}

### 3. Context

{#q-C-3-1}
#### Question C-3-1: What is the context (scope)?

>"The context defines the relationships, dependencies, and interactions between the system and its environment: People, systems, and external entities with which it interacts."
>
>Quoted from [Rozanski-Woods](http://www.viewpoints-and-perspectives.info/home/viewpoints/context/)

The context shows the complete system as one **within its environment**, either from
a business perspective (_business context_) or from a technical or deployment
perspective (_technical context_). The context view (or context diagram) shows
the boundary between a system  and its environment, showing the entities in
its environment (its neighbors) with which it interacts.

It thereby identifies the system’s relevant **external interfaces**.
Make sure that the interfaces are specified with all their relevant aspects (what is communicated, in which format is it communicated, what is the transport medium, …).

T> The interfaces to neighboring systems belong to the most critical and risky aspects of any system development. Ensure early on that you have understood them in their entirety.


{#q-C-3-2}
#### Question C-3-2: How shall I document the context (scope)?

**Short answer**

: Combine a component diagram with a table. In that diagram, your system shall be
a black box. All external interfaces (neighbor systems, user roles, participating actors
  and sensors) shall be visible.

**Longer answer**

: Read the short answer above.

  In case you have many neighbor systems (or external interfaces), you may _categorize_
  them by finding proper abstractions or generalizations. For example, for an e-commerce
  system your system will likely have external interfaces to numerous
  payment providers (credit card companies, banks etc). In the context diagram,
  you can combine all those into a single `payment provider`external interface,
  and defer the details to either a detailed building block level or even a
  _payment privider concept_.

  Accompany your context diagram by a brief table, explaining the names/identifiers from
  the diagram. Refrain from too many details here, but refer or hyperlink to corresponding
  parts of your arc42 documentation.

See [question C-3-7 (simplify documentation of business context)](#q-C-3-7) for
some options of working more efficiently with the business context.

{#q-C-3-3}
#### Question C-3-3: What is the "business context"?

All neighboring systems and _business_ data that is exchanged with the system.

The business context should **avoid** overly technical information (like detailed protocol
   or data type information, communication channels or hardware information).

You find an example on the left side of the diagram below. Contrast it with the _technical context_ of the right side of this image (described in [question C-3-4 (technical context)](#q-C-3-4)).

{#image-bus-tec-concept-infosys}
![Business and technical context (of a simple web shop)](images/faq/C-Sections/Business-vs-technical-context-infosys.png)

{#q-C-3-4}
#### Question C-3-4: What is the "technical context"?

Specification of the technical communication channels or protocols
linking your system to neighboring systems and the environment.

You will find technology and physical infrastructure information
in a technical context.

See also:

* the right part of the [diagram above](#image-bus-tec-concept-infosys),
in contrast to the business context on the left side of that diagram.
* [question C-3-3 (business context)](#q-C-3-3)
* [question C-3-6 (when to document technical context)](#q-C-3-6)


{#q-C-3-5}
#### Question C-3-5: In which cases shall I document the "business context"?

Always (as in "in every single system you ever work on").


There are, though, several options for you to save effort in
documenting the business context - see [question C-3-7 (simplify documentation of business context)](#q-C-3-7).


{#q-C-3-6}
#### Question C-3-6: In which cases shall I document the "technical context"?

When hardware, protocols or deployment is of utmost importance for
many stakeholders, then you can use the technical context to convey
such information.

In most business systems you can ignore the technical context and document or specify _that_ information in the deployment view in arc42-section 7.

I> I (Gernot) have not used a technical context in years, most of my clients in real-world projects were perfectly happy with the combination of business context and deployment view.

{#q-C-3-7}
#### Question C-3-7: How can I simplify documentation of the "business context"?

Some ideas:

* Reduce precision or the amount of detail you show in the business context. Show abstractions, aggregate neighbors or even interfaces.
* Show categories of neighbors, not every single neighbor system.
* Use UML port symbols on a component diagram to avoid drawing too many boxes and lines
* Combine multiple types of users or user-roles into appropriate
abstractions or more generic roles (e.g. combine private and corporate users simply into "users").


{#q-C-3-8}
#### Question C-3-8: Shall I document risks or problems in the context?

External interfaces are especially sensitive to problems or risks,
often functionality or availability of your system depends on
some of these external interfaces.

Problems or risks associated with external interfaces therefore need
special attention or countermeasures - so it's a great idea
to explicitly show those risks or problems in the context view.

Below you find some examples of risks or problems that might occur
at external interfaces:


* Availability risk: if external systems are down: an external system heavily influences the availability of your system.
* Cost risk: the usage of an external system is expensive, individual calls or other types of use cost money. Examples are credit card checks or payment/booking services.
* Security risks: you receive/send sensible data from/to external systems. That could make these interfaces particularly interesting for a potential attacker.
* Volatility (high probability of change) of external systems: Interfaces of external systems are changed often (they are "work in progress"). The syntax and semantics of the transmitted data could be changed on short notice, which means that you either have effort adapting to these changes or you need to develop a flexible consumer for these interfaces.
* Complexity risks: using this interface is exceptionally complex or difficult, because it might have complex data structures, uses esoteric frameworks, complicated handshakes or an arbitrary mixture of those.

T> It can be useful to use either color or iconic symbols to indicate risks. Always explain these risks in the table accompanying the context diagram.
