
### 4. Solution strategy

{#q-C-4-1}
#### Question C-4-1: What is the "solution strategy"?

A short summary and explanation of the fundamental solution ideas and strategies.

An architecture is often based upon some key solution ideas or strategies. These ideas should be familiar to everyone involved in architecture work.



{#q-C-4-2}
#### Question C-4-2: How to document the "solution strategy"?

**Short answer**

: As brief as possible. As many different stakeholders will read the "solution strategy", its explanation shouldn't be overly technical.

**Longer answer**

: State these decisions which gravely influence(d) your architecture. Refrain from overly detailed explanation, don't describe possible alternatives or even implementation guidelines.

  You can (or should) dive into such technical detail in arc42 section 8 (crosscutting concepts), where you can elaborate on the _how_ and _why_
  of your approaches. If only single building blocks are concerned,
  even the building block view (arc42 section 5) might be the appropriate
  location for this information.

  Provide hyperlinks or at least references to sections or documents
  giving additional information or detail.

T> It's often a great idea to refer to specific quality requirements or goals when explaining solution approaches - see the examples
in [question C-4-3 (examples for _solution strategy_)](#q-C-4-3).


{#q-C-4-3}
#### Question C-4-3: Can you provide examples for the _solution strategy_?

Yes - of course :-)

The following examples are taken from the [arc42 by Example]()
Leanpub book.

###### From the Html-Sanity-Checker example architecture

1. Implement HtmlSC mostly in the Groovy programming language and partially in Java
with minimal external dependencies.
2. Wrap this implementation into a Gradle plugin, so it can be used
within automated builds. Details are given in the
[Gradle userguide](https://docs.gradle.org/current/userguide/userguide.html).
3. Apply the [_template-method-pattern_](http://sourcemaking.com/design_patterns/template_method/)
to enable:
  * multiple checking algorithms. See the [concept for checking algorithms](#section-ii-8-checking-algorithm),
  * both HTML (file) and text (console) output. See the [reporting-concept](#section-ii-8-reporting).

(Remark: Some hyperlinks in the paragraph above might not work,
  as they were only meant to be examples.)


###### From a Mass-Market CRM system


{width=95%}
|Goal/Requirement    |Architectural Approach                  |Details        |
|--------------------|----------------------------------------|---------------|
|Flexible Data Structure |Database structure + persistence code is completely (100%) generated from UML-model |Persistence concept, section 8.1 |
|--------------------|----------------------------------------|---------------|
|Flexibility in Transmission Formats (CSV and fix-record-formats |Create domain-specific languages for CSV and fix-format import/export configurations. Build an ANTLR based parser for these languages plus the corresponding interpreters. |Custom Eclipse Editor, Section 8.2 |
|--------------------|----------------------------------------|---------------|
|Flexibility (Configurable CSV/fix formats) |Implement customized editor for CSV/fix DSL as Eclipse plugin |Custom Eclipse Editor, Section 8.2  |
|--------------------|----------------------------------------|---------------|



(Remark: Again - no links to details are given in last column of
  the table - in any real architecture documentation you should prefer hyperlinks to just naming the sections. )
