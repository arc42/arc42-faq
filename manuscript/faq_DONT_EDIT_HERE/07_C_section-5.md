
{#faq-sect-C-5}
### 5. Building block view

{#q-C-5-1}
#### Question C-5-1: What is a "building block"?

**Short answer**

: Any piece of source code of your system.

**Longer answer**

: Any _programming_ or source code construct (e.g. module, component, subsystem, class, interface, package, library, framework, layer, partition, tier, function, macro, operation, data structure, …) that you implemented to make your system work.

  Further examples of building blocks which _might_ be relevant for your system:

  * _configuration_ files or items
  * UI specific files, styles or definitions,
  like css-files in web development.
  * Any kind of templates used to generate other artifacts at
  compile-, build- or runtime
  * Build- or makefiles
  * Deployment- or installation-related artifacts (e.g. deployment-
    or container descriptors)

{#q-C-5-2}
#### Question C-5-2: Do third-party libraries, frameworks or tools count among building blocks?

**Short answer**

: Limit building blocks to _things_ you implement or maintain yourself.

**Longer answer**

: Some external software (like middleware, database, UI-toolkit or similar)
might be essential to understanding the structure of your system. You can
include those in the building block view.

  You definitely should show those elements in the deployment view
  (arc42-section 7)!.

{#q-C-5-3}
#### Question C-5-3: How does source code relate to building blocks?

**Short answer**

: Building blocks represent your source code. Your building blocks
should be an abstraction of your source code.

  The problem: There can be several possibilities how you can
  aggregate source code constructs to building blocks. I'm afraid you
  have to read the longer answer below...

**Longer Answer**

: Mapping code to building blocks is a challenge, which we like to demonstrate by a small example, see the following figure. In its center
you see a directory listing of (Python) source code files making up the system.
Both on the left and the right side of the images you find different, but perfectly valid building block structures for these files.

![Different mappings of code to building blocks](images/faq/C-Sections/mapping-code-to-blocks.png)

Both versions were created with different abstraction criteria, both
are possible.

In reality, you should organize your source code along your
abstraction criteria. Some technologies or frameworks impose
certain directory structures that can suggest completely
different building block structures than those intended by the architects.

Especially layer structures (view, application, infrastructure)
found in some technologies can obfuscate any business- or domain structures that could be useful in understanding the overall
organization of the system.

T> Keep the mapping of source code to building blocks close to either the:  
T>
T> * directory structure of your source code files
T> * modularization constructs of your programming language. In Java, for example, this would be packages.

Every single piece of source code should be contained in one of your level-1 building blocks.


{#q-C-5-4}
#### Question C-5-4: How detailed shall we document the building block view?

**Short answer**

: Show at least level-1, the top-level structure of the implementation.

**Longer answer**

: As detailed as your stakeholders need it. In many cases, refining just a few of the top-level building blocks will be sufficient - with safety-critical system (as always) being an exception!


T> When development teams have a clear understanding of important **crosscutting concepts** (arc42 section 8), they sometimes don't need a detailed building block view.

{#q-C-5-5}
#### Question C-5-5: Can I refine a group of building blocks together?

Yes, sometimes it can be helpful (although it somewhat destroys the symmetrical
  structure of the building block hierarchy).

You find an example below:

![Refine two blackboxes togegher](images/faq/C-Sections/refine-several-blackboxes-together.png)

{#q-C-5-6}
#### Question C-5-6: How can I document or specify building blocks?

It depends on wether you need an overview (black box) or details (white box):

For the overview (**black box**), you should document or specify building blocks by giving the following information:

* **Responsibility**: What does this blackbox do, what task or function does it fulfill? What use-cases, use-case-clusters does it handle?
* **Interface**: What is the interface (input, output) of this blackbox, what is its API, what does it require as input and what does it provide as output.
* Source code: Where to find the source code of this blackbox. That might be the most important entry point, a number of files, directories or packages. Anything that might help a developer to find details.

We call this the **black box template**, see also [question B-8 (black box template)](#q-B-8).

For details (**white box**), you should use a diagram with some explanation
(aka white box template, see [question B-9 (white box template)](#q-B-9).

{#q-C-5-7}
#### Question C-5-7: How shall I document building blocks for non-object-oriented systems?

Wether object-oriented, procedural, functional or any other
programming paradigm: Building blocks are an abstraction of your
source code. You shall primarily describe or specify their
respective _responsibilities_ (and a few other details).

arc42 does **not** depend on a particular development approach or
programming paradigm...

For other hints to describe or specify building block structures, see [question C-5-6 (document building blocks)](#q-C-5-6).

{#q-C-5-8}
#### Question C-5-8: How do I describe internal interfaces?

By _internal interface_ we mean the interface between building blocks within
a system, in contrast to _external interfaces_ that connects our system to the external world.

You have a number of options, shown below with increasing degree of detail and effort:

1. Show the interface by any connection (line) within a whitebox diagram.
2. Give the interface a (hopefully self-describing) name (aka _aptonym_).
3. Describe the name informally (e.g. within a table below the respective whitebox diagram) with one or two sentences.
4. Document the interface and its usage by one or more unit-tests. The idea behind those tests should be "test-as-documentation". On one hand these tests are precise, on the other hand they shouldn't add much overhead to your work, as you will write some unit tests anyway (at least we hope so...)
5. Add the programming interface (API): list methods or functions with the required/optional parameters.
6. Add further UML details to your whitebox diagram, e.g. ball-socket, ports, and describe those within your modelling tool.
7. Add quality attributes of this interface to the API description, e.g. performance or throughput guarantees. Some people call those the "service level agreements" of the interface.

I like to emphasize the usefulness of _test-as-documentation_: It's a developer-friendly and pragmatic way of documenting potentially critical elements of your architecture. Those tests will (hopefully) be automatically included into your documentation - so the documentation is always correct.


{#q-C-5-9}
#### Question C-5-9: How do I describe external interfaces?

Basically similar to internal interfaces (see [question C-5-8 (internal interfaces)](#q-C-5-8)).

The major distinction might be the fact that _external_ people (beyond the scope and influence of your systems' stakeholders) can be involved, both as consumers and as providers of interfaces (or data or events at these interfaces).

As these _external_ people will likely not have access to your internal arc42 documentation, you might be required to provide distinct documents for your external interfaces.

T>Changing external interfaces will usually be much harder than modifications at internal interfaces - simply because external stakeholders will be involved (whom you cannot control or influence).
T>Therefore external interfaces contain greater risks than internal interfaces, and they need more attention, care and management. As software architect, these _pesky_ things belong to your responsibility.  

{#q-C-5-10}
#### Question C-5-10: How can I avoid redundancy with interfaces in the building block view?

Especially external interfaces might occur several times within the building block hierarchiy - how can I avoid to document or specify them at several places redundantly?

See the diagram below - the `interface X` (marked with red circles)
occures three times in the hypothetical system shown there.

![](images/faq/C-Sections/avoid-redundancy-in-interfaces.png)

Handle such situations in the following manner:

1. In the context diagram, give the interface an appropriate name and briefly explain its business relevance or significance in just a few words.
2. Describe the interface in detail at the level where it is actually handled (e.g. the service is implemented or data is consumed). In the diagram above, this would be whitebox "B".
3. At all other occurances (especially in the context view), add references to the detailed description. In the scenario above, such references should occur in the context and the level-1 whitebox.


{#q-C-5-11}
#### Question C-5-11: How does the hierarchy of building blocks relate to the arc42 sections (5.1, 5.2 etc.)?

**Short answer**

: Level-n of the building block view shall be documented in section 5-n of the building block view, where level-0 (zero) is the context view and level-1 your topmost system whitebox.

**Longer answer**

: See the following diagram.

![Mapping of building block hierarchy to arc42 sections](images/faq/C-Sections/map-hierarchy-to-sections.png)


{#q-C-5-12}
#### Question C-5-12: What kind of building blocks don't I need to document or specify?

In case you want or need to save documentation effort, you have some good opportunities within the building block view. You can possibly omit the following kinds of building blocks from your documentation:

* Really small blocks that will easily be understood by reading the source code.
* Blocks that serve general purpose and are not specific to your system.
* Blocks that only apply (thoroughly defined) crosscutting concepts and don't do much else.
* Blocks that implement purely _technical_ functions, like persistence, logging, communication, data transformation, data validation or data dispatching.

Tendencially avoid documenting lower-level building blocks.

{#q-C-5-12}
#### Question C-5-12: What kind of building blocks shall I document or specify?

This is the opposite of [question C-5-12 (blocks you don't need to document)](#q-C-5-12).

You should document or specify the following kinds of building blocks:

* The level-1 whitebox (aka the top-level decomposition of your system).
* Blocks adressing specific or important functionality.
* Blocks that adress important quality attributes of the system.
* Blocks that handle complicated or complex functionality.
* Blocks that mitigate or handle risks.
* Blocks that contain surprises or unusual ideas.
* Blocks that somehow deviate from the rest of the system.
* Blocks that deviate from typical developers' expectation.
* Blocks that are required or important for creating business value.

Focus on higher-level building blocks. Level-1 should always be documented.     

Remember to be lazy and document economically: Smaller documentation for fewer building blocks are easier and cheaper to maintain than large documentation for many blocks...
