{pagebreak}

### 7. Deployment view

{#q-C-7-1}
#### Question C-7-1: What does the deployment view show?

1. Your hardware structure(s), also called technical infrastructure.
2. The mapping(s), also called deployment, of your software to this hardware.

For part 1, hardware, there might be several variants.
Therefore part 2, deployment, might be different, depending on these hardware structures.

{#q-C-7-2}
#### Question C-7-2: Why do I need a deployment view?

The deployment (mapping of software onto hardware elements) can be rather complicated, see the example in [question C-7-5](#q-C-7-5). See also the second part of question [C-7-1 (deployment)](#q-C-7-1).


{#q-C-7-3}
#### Question C-7-3: Who shall describe/document the deployment view?

The first part of the deployment view, (see question [C-7-1 (deployment)](#q-C-7-1).) will sometimes be created and maintained by stakeholders responsible for technical infrastructure and/or hardware.

The second part, the mapping of software to hardware, will often be documented and maintained by architects and/or the development team.


{#q-C-7-4}
#### Question C-7-4: Shall I use UML deployment diagrams for the deployment view?

The UML provides only this type of diagram for deployment and infrastructure, therefore you have no practical alternative.

On the other hand, you can of course use any free form of diagram to depict your technical infrastructure.

Make sure that stakeholders understand such notations - and that architecture- and infrastructure decisions can be understood based upon these diagrams.

T>As said numerous times in this book: Please add textual explanation (e.g. a table!) to your diagrams, where you briefly explain the elements, their responsibility and any additional information that is required to understand the situation.
T>
T>Often it will be useful to _reason_ about the diagram: Explain _why_ the structure shown is useful and what argumentation lead to the appropriate decisions.

{#q-C-7-5}
#### Question C-7-5: Can there be different deployment scenarios or variants?

Yes, for example when you have different _stages_ from development to your production environment.

See the following example, where the (static) building blocks A, B, C can be deployed in three different alternatives:

{width=70%}
![Deployment variants](images/faq/C-Sections/deployment-variants.png)


{#q-C-7-6}
#### Question C-7-6: What shall I do when my building blocks get dynamically assigned an execution environment (node) - so I cannot statically assign them to infrastructure nodes?

If some part of your system or your infrastructure decides at runtime _where_ a particular instance of a building block gets executed, then the deploment view should at least explain this behavior.

It might be useful to create a "dynamic deployment concept" in arc42 section 8 and refer to this concept from the deployment view.

A>If you doubt such a dynamic mapping: Some modern architecture styles (like microservices, self-contained systems or especially serverless-architectures) already said _bye-bye_ to static mapping of building blocks to specific nodes...
A>For further information, see:
A>
A> * Eberhard Wolff: [Microservices-Book](http://microservices-book.com/)
A> * [Self-contained systems](http://scs-architecture.org/)
A> * Martin Fowler on [serverless architecture](http://martinfowler.com/articles/serverless.html), and an impressive implementation based upon [AWS-Lambda](https://serverless.com/).
