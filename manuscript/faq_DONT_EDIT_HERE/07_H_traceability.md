{pagebreak}


{#section-vii-H}
## H Questions on arc42 and traceability

{#q-H-1}
#### Question H-1: What does _traceability_ mean (with arc42)?

C>"Traceability (or Requirements Traceability) refers to the ability to link product requirements back to stakeholders' rationales and forward to corresponding design artifacts, code, and test cases." (quoted from [Wikipedia](https://en.wikipedia.org/wiki/Traceability#Software_development))

Full-scale traceability needs every single requirement
to be referenced in any part of the architecture/solution
documentation.

From a more pragmatical architectural (arc42) perspective,
traceabilty can also refer
to the understandability or explanation of important or fundamental architecture or
solution decisions: "We took the decision Dec-X because of
the requirements Req-Y."


{#q-H-2}
#### Question H-2: Shall we strive for traceabilty in our documentation?

**Short answer**

: If you can, you should definitely avoid it: It's horribly expensive, takes an awful lot of time and is really difficult.

**Longer answer**

: In case you're working in safety critical systems, like
medical, pharmaceutical or avionics, you are most likely required to provide traceability.

One nice hook within arc42 are blackboxes within the building block view: Use the blackbox template to document:

* the requirements fulfilled or satisfied by this particular building block,
* the source code needed to implement this building block.

{#q-H-3}
#### Question H-3: How can I keep architecture documentation in sync with source code?

We've several suggestions, but the most important one first:

T> Appoint a person responsible for the appropriate amount and
quality of your technical and/or architecture documentation.

* Document economically, especially be frugal with building block details: Many developers will understand many details of building blocks by digesting source code - so don't create a large number of whitebox diagrams.
* Level-1 of the building block view will be one of your best friends: That top-level structure of your system will most often
remain quite stable over time, and won't need to be updated often. Many source code changes don't affect level-1!
* Defer documentation of volatile parts: In case you can anticipate structural changes or volatility in certain parts of your system, leave the documentation of these parts as abstract and high-level as possible until these parts have reached a stable state.
* Prefer documenting "crosscutting concepts" (arc42 section 8) over detailed building blocks (section 5) or runtime scenarios (section 6).
