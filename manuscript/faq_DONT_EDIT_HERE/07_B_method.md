{pagebreak}

{#section-vii-B}
## B Questions on methodology


{#q-B-1}
#### Question B-1: Which parts of arc42 are "essential", which are "optional"?

**Short answer**

: Please don't _fill in everything_. Document **only what your stakeholders need** (you should ask them, one-by-one).

**Longer answer**

: Everything you document will potentially require maintenance
effort in the future. With every piece of documentation, you're
effectively piling up maintenance debt - and in parallel creating some information value...

  Please only document things, facts and reasons that you
  or your stakeholders consider _important_ enough to justify
  written documentation.


{#q-B-2}
#### Question B-2: Does arc42 prescribe or enforce specific notations?

No, arc42 works completely (!!) independent of notation or syntax.

{#q-B-3}
#### Question B-3: Shall I use UML for arc42 documentation?

You don't need to - but:

UML notation is well-supported by various (free and commercial) tools,
has a clear semantic and is pretty much standardized - therefore we
(Peter + Gernot) like it.

On the other hand, UML does not guarantee any positive effects for your
architecture or your team. Other notations might work as good (or bad) as UML.

You need to ensure that all stakeholders have a mutual understanding of
your notation. That can become really difficult, if you draw only boxes
and lines - as those have no semantic at all (at least without further explanation)

People tend to interpret such symbols in a way they like - most likely
different than the original author intented...

See [question D-4](#q-D-4).

{#q-B-4}
#### Question B-4: What is the minimal amount of an arc42 documentation?

**Short answer**

: There is no general rule - as the minimal amount depends on the system, its stakeholders, criticality, complexity, size and/or risks.

**Longer answer**

: We suggest to always explain, document or specify the following aspects:

  * 3-5 central quality requirements, expressed in
  scenarios.
  * Context view and external interfaces
  * Brief explanation of your solution strategy, the most important decisions influencing the implementation or operation of the system.
  * Building block view, level 1.
  * Most important crosscutting concepts.


{#q-B-5}
#### Question B-5: Where to document external interfaces?

**Short answer**

: Both scope/context (arc42 section 3) and
building block view (arc42 section 5) provide adequate room
for external interfaces.

**Longer answer**

: How and where you describe external interfaces depends
on several factors:

  * If your system provides external interfaces to external
  consumers **and** you and your team can decide about
  any details of these interfaces - then you have to
  care for their documentation.
  * Do you need to provide external systems with information
  on _how to use_ your interfaces? You could provide
  example code and other interface documentation, but need
  to make sure this information is easily accessible to
  the external stakeholders.
  * Do you just provide _data_ at your external interfaces,
  and no services? Then you might stick to just a documentation of data formats (and maybe semantics).
  * In case you use interfaces provided by external systems,
  make sure their documentation is easily accessible by your
  development and maintenance teams. Include references in the arc42 context or building block view.

See also [question B-6 (how to document interfaces)](#q-B-6)

{#q-B-6}
#### Question B-6: How to document external interfaces?

**Short answer**

: Document / specify interfaces by providing unit-tests. We hope that you would create such unit tests anyway, so you can re-use them as part of your interface documentation.

**Longer answer**

: Describe syntax, semantic, protocoll/interaction of your interfaces, show sample interactions, provide sample data.
Add some unit tests and/or other example code.

{#q-B-7}
#### Question B-7: Where to put links to external systems ("neighbors") documentation?

Use the context view to reference external systems' documentation or to provide references to the parts of your
arc42 documentation containing appropriate information.

If an external system/interface is especially important or risky
for your architecture, it's sometimes adequate to _copy_
parts of this interface document into your own arc42...

T>##### War Story (from Gernot)
T>In one customer project we had to poll an external system
T>for user-credentials: No user could work with our system when
T>this special interface was _down_. One day the incredible happened - we had a fatal production bugs caused by exactly this interface. Too bad the documentation of that (external) system was located on a network share... that was accidently _down_ at the same time - so no developer could access the documentation that was essential to tackle the production bug...

{#q-B-8}
#### Question B-8: What is a blackbox / the blackbox template?  

A blackbox is a building block or component of the system which can be explained or defined in terms of its inputs and outputs, without knowledge of its internal workings.

You can easily document or specify a blackbox with a simple template. We propose a table for it, in the following form
(required information in **bold**, the rest is optional):

|part     |explanation |
|--------------|-----------------------------|
|**Name**      |name or id of this blackbox. The name should be the title of the blackbox template.|
|--------------|-----------------------------|
|**Responsibility** |What does this blackbox do, what task or function does it fulfill? What use-cases, use-case-clusters does it handle? |
|--------------|-----------------------------|
|**Interface** |What is the interface (input, output) of this blackbox, what is its API, what does it require as input and what does it provide as output. |
|--------------|-----------------------------|
|Source code   |Where to find the source code of this blackbox. That might be the most important entry point, a number of files, directories or packages. Anything that might help a developer to find details.
|--------------|-----------------------------|
|Qualities     |What quality requirements does this blackbox satisfy? How fast/secure/robust is it? Does it offer any guarantees or service-level-agreements?
|--------------|-----------------------------|
|Open issues   |Are there known issues, problems or risks associated with this blackbox?
|--------------|-----------------------------|
|Requirements  |What are the requirements satisfied by this blackbox? Such information is important if you need traceability. See [section H (Traceability)](#section-vii-H)
|--------------|-----------------------------|



{#q-B-9}
#### Question B-9: What is a whitebox?

A whitebox contains multiple building blocks (blackboxes) with their relationships. It is a more detailed view of a blackbox
of a higher abstraction level. You find an example in the diagram below:

![Example whitebox diagram](images/faq/B-Method/whitebox-sample.png)

This whitebox contains three blackboxes (A,B,C) and some relationships - a few of which are labelled.

{#q-B-10}
#### Question B-10: What is the _building block hierarchy_?

The building block view explains your source code in a hierarchical way:

The topmost level (level 1) represents the white box description of the overall
system, made up of black box descriptions of the system’s top level building blocks.

Level 2 zooms into the building blocks of Level 1 and is thus made up of the white box descriptions of all building blocks of Level 1 together with the black box descriptions of the building blocks of Level 2.

The following diagram shows a (rather generic) example - starting the hierarchical
decomposition from the context view (called level-0 in arc42 terms)

![Example building block hierarchy](images/faq/B-Method/arc42-building-block-hierarchy.png)


{#q-B-11}
#### Question B-11: How to document a whitebox with the _whitebox template_

The whitebox _template_ is a structured means of specifying or describing whiteboxes. It contains the following elements (required information in **bold**, the rest is optional):

{width=90%}
|part          |explanation |
|--------------|-----------------------------|
|**Diagram**   |Shows the contained blackboxes plus their relationships |
|--------------|-----------------------------|
|**Rationale** |The reason why this whitebox is structured like it is.
|--------------|-----------------------------|
|Contained blackboxes |Names and responsibilities of contained blackboxes, plus references to their detailed description.
|--------------|-----------------------------|
|Internal relationships (interfaces)|Brief description of the relationships between internal blackboxes, plus references to their detailed description.
|--------------|-----------------------------|
|Risks and issues |Know issues or risks with this whitebox, information about eventual technical debt or ideas for improvement |
|--------------|-----------------------------|


{#q-B-12}
#### Question B-12: Where shall I describe important (blackbox) components?

The building block view should be a hierarchical explanation of your source code, of the static (code) structure of your system.
It contains blackboxes of various level-of-detail.

It can be very understandable to make your _important_ blackboxes part of your topmost refinement level, which we call level-1 in arc42.

If your important blackbox is something quite small which
you don't want to explicitly contain in level-1, then you could
contain it in any refinement level - and mark it in its
containing whitebox in color or by other visual means:
Draw it larger than others, attach a graphical label/icon to it,
give it a colored border - anything to let it stand out.
Be pragmatic!

See also the questions in [section C-5 (Building block view)](#faq-sect-C-5).


{#q-B-13}
#### Question B-13: Can I use arc42 in agile projects, e.g. with Scrum?

Yes, of course. See also:

* [section E (Agile)](#section-vii-E),
especially [question E-1 (arc42 and agile methods)](#q-E-1).
* [Question B-16 (economical documentation)](#q-B-16)


{#q-B-14}
#### Question B-14: Can I update documentation incrementally? Or shall I document after the implementation is finished?

**Short answer**

: Create and update documentation continuously - in sync with your sprints
or iterations.

**Longer answer**

: If you defer documentation to "later", I am reasonably sure it might never
be done. Don't procrastinate - but make (brief, short, compact, economical)
documentation a habit, like checking-in source code in version control
or writing automated tests (you test, don't you?).

  In my opinion it's way better to have short up-to-date and current
  documentation of only some aspects of the system, than to just have a plan
  to sometimes document the whole system...

  Reserve a brief period of time every day (or at least every week)
  to catch up with your documentation tasks. Close your door, your
  email reader and your messenger apps, flip your phone to silent mode... and
  jot down some important, interesting, risky or otherwise valuable information
  about your current topics.


{#q-B-15}
#### Question B-15: What kind of information shall I provide for which stakeholder?

See also [question A-5 (target audience of architecture documentation)](#q-A-5).

**Short answer**

: You need to inquire with your specific stakeholders, we can only
give you rough approximations from our experience... that will
most likely miss the goals of people involved in or with your system.

  Show them examples what you _could_ deliver with low effort. Incorporate
  their feedback. See [#tip-iii-3 (appropriateness)](#tip-iii-3).

**Longer answer**

: Read the short answer above! Ask your specific stakeholders, what artifacts
or information they expect or require from the architecture documentation
(or more general, the technical documentation).

  Don't ask what they require from the system (hopefully you already know that...)

  Typical answers we received are summarized in the following table:

{width=95%}
|Stakeholder |Required information/artifacts   |
|------------|---------------------------------|
|Project management |Quality goals, (business) context with external interfaces, solution strategy (most important architectural decisions), building block view level-1, overview of important concepts. Sometimes an overview of infrastructure and deployment. |
|------------|---------------------------------|
|Top- or upper management |Top-3 quality goals, major business requirements, business context with neighbor systems, compliance to IT strategy, compliance to security (and maybe other) standards, operation/deployment concepts, cost-relevant architectural decisions. |
|------------|---------------------------------|
|Product owner |Quality goals, building block view with interfaces, overview of important architectural decisions, overview of crosscutting concepts, known issues and risks |
|------------|---------------------------------|
|Software developers |Quality goals with detailed scenarios, solution strategy with links to detailed concept descriptions and/or example solutions, building block view with interface descriptions, important runtime scenarios, domain model, crosscutting concepts, deployment view with possible variants, glossary. |
|------------|---------------------------------|
|Operators, administrators |Infrastructure and deployment, external interfaces with technical and organizational details, logging and monitoring concepts. |
|Tester, QS-team |Detailed business and quality requirements, solution strategy, building blocks with interfaces, crosscutting concepts influencing testing or testability. |
|------------|---------------------------------|
|Developers of neighbor systems |Business and/or technical context, details description of external interfaces, end-to-end interaction/runtime scenarios at these interfaces. |
|------------|---------------------------------|

{#q-B-16}
#### Question B-16: What does _economical_ documentation mean?

Some tips for appropriate (_economical_ or _thrifty_) documentation:

* Less (shorter) documentation can be often read and digested in shorter time
(but beware of _overly cryptic_ brevity, so no Perl, APG or regular expressions).
* Less documentation implies fewer future changes or modifications.
* Explicitly decide what kind and amount of documentation is appropriate, and
with what level of detail.
* Differentiate between short-lived, volatile documentation (i.e. flipcharts for
  your project work) and long-lived _system_ documentation. See [tip V-6]{#tip-v-6}
* Dare to leave gaps: Deliberately leave certain parts of your (arc42) documentation empty.
Especially within arc42-section 8 (crosscutting concepts) you can often remove numerous subsections
that might not be relevant for your specific system.

See [question B-4 (Minimal amount of documentation)](#q-B-4)


A>#### Your question has not been answered?
A>Tell us:
A>
A>* via [email](mailto:info@arc42.de) to info@arc42.de or
A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
