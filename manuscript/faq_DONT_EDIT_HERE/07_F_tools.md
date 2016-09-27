{pagebreak}

{#section-vii-F}
## F Questions on tools for arc42

A>We do not endorse or advertise specific tools here.
A>We have **no** relations whatsoever to a tool vendor.
A>All tool and product names mentioned here are trademarked and/or copyrighted by the corresponding tool creators or vendors.

As authors, we reserve the right to explain our personal experience and opinion. You should
not base your tool selection solely on the information given here! There might be awesome tools
available which we failed to mention...

{#q-F-1}
#### Question F-1: What tools are well-suited for arc42?

This is a classical _it depends_ type of question. Ask three different people,
get at least five different (and most likely conflicting) answers...

* As arc42 documentation should always be a combination of text, tables and diagrams,
a combination of different tools will often be a better choice than trying to get everything
from a single tool (although tool vendors will tell you a different story)
* Often, (UML) modeling tools come with an abundance of functions and _very_ limited usability.
Their learning curve is high and might frustrate many.
* Still - I usually prefer a _real_ modeling tool over a pure graphics editor, for their
better model consistency.


{#q-F-2}
#### Question F-2: What are useful criteria for selecting a toolset for arc42?

Some other criteria to watch out for:

* Teamwork: several people should be able to work in parallel
* Versioning: documentation artifacts need to be version-controlled. That's quite easy
for single files, but some modeling tools make versioning harder than it should be.
* Artifact generation: Sometimes you need _beautiful_ or stakeholder-specific output (e.g. pdf, html).
Some tools excel in this, others fail miserably.
* Robustness: You don't want to re-create diagrams or documentation because your boss made
you use that (supposedly) cheap free-and-open-source documentation tool... I had especially
bad experiences with immature graphic/UML editors.)
* Availability of know-how: For several of the more common tools it's quite easy to find people with corresponding experience. Some tool vendors provide excellent support,
also in methodical questions.

{#q-F-3}
#### Question F-3: Can I automatically include important code artifacts in arc42 documentation?

At best, integrated with out automatic build system?

<t.b.d.>


{#q-F-4}
#### Question F-4: How do I use arc42 with modeling tools?

Most modeling tools lack _out-of-the-box_ arc42 support,
you have to create your desired arc42 (sub-)structures
by yourself.

arc42 does provide an empty arc42-structured model
for Sparx Enterprise Architect(R), although not very
elaborated.

We advice to restrict the use of modeling tools to the
pure graphical part of architecture documentation,
leave text and tables to other tools that are more
suited for these kinds of information.
In this case, create the following arc42-sections in
your modeling tool:

* Context view
* Building block view
* Runtime view
* Deployment view
* Crosscutting concepts


{#q-F-5}
#### Question F-5: How can I use arc42 together with [Sparx Enterprise Architect(r)](http://www.sparxsystems.com/)

<t.b.d.>


{#q-F-6}
#### Question F-6: Are there (free or open-source) modeling tools available?

**Short answer**

: In principal, yes. For example:
  * [UMLet](http://www.umlet.com/)
  * [Modelio](https://www.modelio.org/)
  * [Violet](http://alexdp.free.fr/violetumleditor/page.php)

**Longer answer**

: We have, at least until October 2016, not gotten to know
any free modeling tool that can really compete with commercial
tools with respect to robustness, useability, feature completeness and availability-of-know-how.
Before you go for any free modeling tool,
please make reasonably sure that your candidate fulfills
the basic requirements we explained in [Question F-2](#q-F-2),
concerning teamwork, robustness, versioning and artifact generation.

  Actually, compliance to any specific UML standard is very
  often overrated.
