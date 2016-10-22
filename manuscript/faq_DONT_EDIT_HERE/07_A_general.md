{pagebreak}

{#section-vii-A}
## A General questions

{#q-A-1}
#### Question A-1: What does the _42_ mean?
"42" is a quotation from the science-fiction novel
[_Hitchhikers Guide to the Galaxy_](https://en.wikipedia.org/wiki/Phrases_from_The_Hitchhiker's_Guide_to_the_Galaxy)
by the famous [Douglas Adams](http://www.theguardian.com/books/2011/feb/03/douglas-adams-42-hitchhiker).

In his book the number _42_ is the "answer to the meaning of life, the universe, and everything" - calculated by a _very_ big computer over a _very very_ long time:

{icon=heart-o}
G>"All right," said Deep Thought. "The Answer to the Great Question..."
G>
G>"Yes..!"
G>
G>"Of Life, the Universe and Everything..." said Deep Thought.
G>
G>"Yes...!"
G>
G>"Is..." said Deep Thought, and paused.
G>
G>"Yes...!"
G>
G>"Is..."
G>
G>"Yes...!!!...?"
G>
G>"Forty-two," said Deep Thought, with infinite majesty and calm.”
G>
G> **― Douglas Adams, The Hitchhiker's Guide to the Galaxy**
G>
G> quoted from [GoodReads](http://www.goodreads.com/quotes/tag/42)

Software developers like to use 42 as _magic_ number, that's a number
without any real significance, which you could replace by any other number.
Of course the name _arc42_ wouldn't sound half as cool if we had choosen
another number.

{#q-A-2}
#### Question A-2: What's the license?

[Creative-Commons Sharealike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

Under this license, you're free to:

* Share: copy and redistribute the material in any medium or format
* Adapt: remix, transform, and build upon the material for any purpose, even commercially.

We, the licensors, (Gernot Starke and Peter Hruschka, the creators of arc42)
cannot (and surely will not) revoke these freedoms as long as you follow the license terms.

You must give appropriate credit, provide a link to the license, and indicate if changes to arc42 were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

If you remix, transform, or build upon material from arc42, you must distribute your contributions under the same license as the original.


{#q-A-3}
#### Question A-3: What's the pricing model of arc42?

arc42 is completely free to use (and will remain so!), for
arbitrary kinds of system, even in commercial context.

{#q-A-4}
#### Question A-4: How widely is arc42 used?
In the D.A.CH. region (Germany, Austria, Switzerland), arc42 is used
by many organizations and corporations in various industries. We don't
know any statistically relevant numbers, though...

In these countries, alternatives like Simon Browns'
[SA4D/C4](http://simonbrown.je/#softwarearchitecture) model
are not well-established.

In the international scene, we guess that arc42 is way behind SA4D/C4.

The template is available in English, German and Spanish. Further translations
are most welcome (but will not be provided by the current maintainers of arc42).


{#q-A-5}
#### Question A-5: What's the target audience of architecture documentation?

**Short answer**

: (Potentially) all stakeholders of a system, that require information
about the architecture, e.g. the internal structure, crosscutting concepts
or fundamental decisions.

**Longer answer**

: Which persons or roles are interested in what parts of the architecture
depends on the specific context. Some typical targets for such documentation:

* Software developers who actually implement within the system.
* Software developers of neighbour systems, who need to know about
external interfaces and/or their technical details.
* Software architects who need to prepare, shepard or implement architectural decisions.
* Operators or administrators of software systems, who either need to configure
the system for specific infrastructure needs, optimize it or perform administrative
tasks requiring architectural understanding. This often includes security relevant
tasks, like firewall or database settings.
* Technical managers who organize maintenance or evolution of the system.
* Auditors or reviewers, who valid, current and accurate architectural information
to assess or evaluate the system.
* Testers and QA-engineers who need to plan, impelement or perform
whitebox-, performance- or security testing.
* Consumers of services offered by the system, in case they need to understand
additional details apart from the interface (blackbox) specification.

In our opinion, software architects should maintain an overview of current
stakeholders together with their specific needs for architectural information.

{#q-A-6}
#### Question A-6: What are possible alternatives to arc42?

* Simon Brown's [SA4D/C4](http://simonbrown.je/#softwarearchitecture) model.
You find a brief introduction in one of his [blog posts](https://www.voxxed.com/blog/2014/10/simple-sketches-for-diagramming-your-software-architecture/)
* [The View-Model](https://www.amazon.de/dp/B0046XS3RO/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1)
of Paul Clements et. al from the Software Engineering Institute.
From our point of view, their approach is _very_ heavyweight and can become quite
formal when applied to real-world projects.
* In case your organization has created its own "Software Architecture Documentation Template": It should contain quality requirements, a scope/context section and
information about building blocks and crosscutting concepts. If it does, you're pretty
close to arc42 anyway...

{#q-A-7}
#### Question A-7: For what kinds of systems is arc42 applicable?
**Short answer**

: Due to its flexibility concerning tools, processes and extend, arc42
  is well-suited for all kinds of IT-systems (small to large, simple to complex,
  all kinds of implementation technologies).

**Longer answer**

: For highly-critical systems, (e.g. safety-critical systems, where health
or life are at stake), you need to seriously consider documentation requirements. In such cases, arc42 might not be the adequate approach (see [question A-8](#q-A-8)).

We recommend to a-priori evaluate arc42, and enhance it according to your
specific needs in such cases.
Let domain experts or appropriate auditors review the resulting documentation
structure.

  For all other _normal_ systems you can apply arc42: Depending on risk,
  complexity, scope or size you should assess both the arc42 structure
  and your toolchain for fitness regarding your specific purpose.

  We successfully worked with dozens of clients in small, medium and
  large organizations on many different systems with arc42 - and it never
  let us down :-)

{#q-A-8}
#### Question A-8: In which cases shall we NOT use arc42?

If you're creating safety-critical systems, e.g. medical
or avionics systems, where health or life are at stake,
you will most likely encounter comprehensive
and formal specification and documentation requirements,
that arc42 will most likely not fulfill.

Many of the hints and tips we give for economical documentation
might not be valid in such cases.


{#q-A-9}
#### Question A-9: How can I contribute or report bugs in arc42?

* We maintain the template itself at [Github](https://github.com/arc42). You can fork the repository and send us pull requests...
* You can open issues in this repo
* You can [email us](mailto:info@arc42.de), or contact us over [Twitter](https://twitter.com/arc42Tipps).



A>#### Your question has not been answered?
A>Tell us:
A>
A>* via [email](mailto:info@arc42.de) to info@arc42.de or
A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
