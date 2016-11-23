{pagebreak}


{#section-vii-J}
## J Questions on managing documentation

{#q-J-1}
#### Question J-1: How to document (very) large systems with arc42

Modularize extensive documentation:

Factor out (extract) documentation commonalities from different parts of the system and create separate documentation for relevant subsystems.

Link up these different parts of the documentation by hyperlinks,
so that consumers can navigate freely between special and common parts.

A toolchain supporting modularization is an important prerequisite:
it's a nuisance with typical office products, but works quite
smoothly with wikis or markup-languages.  

For a schematic example of modularized documentation see
[figure arc42-modularized](#figure-faq-arc42-modularized): The overall systems is made up from three subsystems. The _common_ architecture documentation contains the introduction and goals, strategic decisions, building blocks level 1 plus crosscutting concepts. All these informations are valid and useful for the other three (smaller) documents.

Each subsystems' documentation contains only parts of the arc42 template, and each subsystem focusses on different aspects.

{#figure-faq-arc42-modularized}
![arc42 modularized](images/faq/J-Management/arc42-modularized.png)

The common part of your architecture documentation will most often contain
the global system goals and the overall business context. Eventually
it will also contain the solution strategy plus some crosscutting concepts.

{#q-J-2}
#### Question J-2: Does a _documentation governance_ make sense for architecture documentation?

It depends: On one hand, homogeneity, consistency and standardization can be really useful and efficient for documentation, on the other hand can cost and effort for such standardized documentation become very high.   

Answer the following questions for your situation. The more "yes" answers the more useful a _regulated_ documentation might be:

* Do you have many (i.e. more than 15) IT-systems you develop or maintain?
* Do many of these systems have technical _similarities_ (use common frameworks, implementation approaches, technical concepts)?
* Do you work with different implementation or maintenance teams?
* Do you have a lot of change within your development team?
* Do different organizations work on your systems (i.e. external service providers)?
* Do you work in regulated domains (i.e. medicine, aerospace, pharmaceutics etc.)?
* Will the documentation of your systems be audited, validated or otherwise (formally) checked?
* Are some of your systems _highly critical_ for success or survival of your organization?
* Are your systems maintained by a large development team (>100 people)?

{#q-J-3}
#### Question J-3: Is there a checklist for arc42 documentation?

See [question J-4](#q-J-4).


{#q-J-4}
#### Question J-4: Is there a general checklist for architecture documentation?

Counterquestion: What do you want to achieve with such a checklist?

* Improve the content of the documentation: You won't get that by a checklist, but only by good examples, coaching and feedback.
* Checking formal criteria: Can you improve by checklists - but there's no general consensus on formal criteria. We suggest you refrain from overly formal criteria - as documentation won't get much more useful when it's formal.
* You want to remind your team of some important parts of the documentation: Determine the subset of arc42 that your stakeholders really need - and then include those in your _definition-of-done_
(see also [question E-2 ](#q-E-2))


{#q-J-5}
#### Question J-5: How can I create delta-documentation with arc42?

In other words: How can I document the changes (deltas) between two consecutive versions of a system?

<t.b.d.>


{#q-J-6}
#### Question J-6: What level of access permissions shall stakeholders have on the architecture documentation?

**Short answer**

: Keep the administrative effort as low as possible: If you
accord details access permissions, you create administrative overhead.

**Longer answer**

: Usually, all stakeholders can read and write the documentation. Some cases justify exceptions from this rule:

  * For large teams, you should modularize your documentation
  and restrict write-access to certain parts, to avoid
  _accidental_ changes.
  * You might differentiate (short-term) _project_
  and (long-term) _system_ documentation. Everybody can
  write in project documentation, only few people might modify
  system documentation.
  * In case of regulated documentation, you might need
  detailed permissions (and access logs) to avoid manipulation.


  A>#### Your question has not been answered?
  A>Tell us:
  A>
  A>* via [email](mailto:info@arc42.de) to info@arc42.de or
  A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
  A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
