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


{#q-F-7}
#### Question F-7: Can we use arc42 with the [Atlassian Confluence](https://www.atlassian.com/software/confluence) wiki?

[^confluence]: The name and logo of Confluence is copyrighted by Atlassian Software. arc42 is neither affiliated with or in any way sponsored by Atlassian Corporation.

Yes - it's a (near-perfect) combination: Confluence[^confluence] is a powerful, yet easy-to-use
collaboration platform, a "wiki-on-steroids".

You can easyli map the arc42 structure on Confluence pages, and even use
predefined templates to setup the complete arc42 structure in a breath
(see [question F-8 (Confuence tools)](#q-F-8) for details on available tooling).

T>I (Gernot) used Confluence to generate various stakeholder-specific output from a single Confluence "arc42 repository", which saved a lot of documentation effort, as the development team needed only to maintain this single source-of-truth.

In Confluence, you can _tag_ (label, mark) pages, so it becomes very simple to add
arbitrary meta-information to certain parts of your documentation. Use this e.g. to
add version/release-specific information, or to distinguish between "already-implemented"
and "planned-for-the-future" information.

Confluence does not (!) provide out-of-the-box diagramming features, but numerous
tools are available to the rescue, see [question F-9 (Confluence Diagramming tools)](#f-F-9) for details).

{#q-F-8}
#### Question F-8: What tools can I use to setup arc42 in Confluence?

There a a few options to simplify the setup of the arc42 structure within your Confluence:

* The [Networked-Assets ATC macro](https://marketplace.atlassian.com/plugins/com.networkedassets.plugins.space-blueprint/server/overview) to insert the arc42 template into any Confluence space.
* The [smartics Blueprints for arc42](https://marketplace.atlassian.com/plugins/de.smartics.atlassian.confluence.smartics-projectdoc-confluence-arc42/server/overview)
* (Within the near future...) You can get a Confluence space generated out of the arc42 _Golden Master_ from the arc42-template github repository. We're currently working hard on making this available for download. Please [contact us](mailto:gs@gernotstarke.de) for a pre-release version if you're interested.  

See [question F-9 (Diagrams in Confluence)](#q-F-9) for an overview of diagramming tools available for Confluence.

{#q-F-9}
#### Question F-9: How can I create diagrams in Confluence?

* You can create and maintain your diagrams with any modeling tool and export your diagrams in jpg or png. Concluence can import these files, and will even keep a history of updates, if you ever upload newer versions. Beware: This requires maximal manual effort...
* You can create and maintain diagrams with a Confluence graphics plugin. I (Gernot) have positive experience with the following:
  * [Gliffy](https://www.gliffy.com/products/confluence-plugin/), a well-known plugin for creating arbitrary diagrams within Confluence pages. The editor is complety integrated into the web browser. Supports different versions of diagrams, stable and robust, requires a commercial license.
  * [Draw.io](https://support.draw.io/display/DFCS), a powerful browser-based graphics editor, also available as Confluence plugin. I (Gernot) have used the plain-browser version of draw.io - which can be used completely offline and export diagrams to various formats.


  A>#### Your question has not been answered?
  A>Tell us:
  A>
  A>* via [email](mailto:info@arc42.de) to info@arc42.de or
  A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
  A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
