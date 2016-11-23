{pagebreak}

{#section-vii-G}
## G Questions on arc42 and versions / variants


{#q-G-1}
#### Question G-1: Shall I _version control_ our architecture documentation?

Yes, of course!. At best with the same strategy, processes and tools you use for your source code.

(Gernot's opinion): If it's not under version control, it does not exist (with the sole exception of well-managed wiki systems, that easily allow you to read older versions of documents.)

If you cannot use your version control system for your
(architecture) documentation, see [Question G-2](#q-G-2).

{#q-G-2}
#### Question G-2: We cannot use version control for documents. What to do?

**Really** (really!) make sure you find a (mostly automated)
way to get your documentation under version control.

One way which helped me several times is the following:

* When you release your software (in continous deployment
  scenarios, you might stick to major releases...),
  create a pdf file from your documentation.
* Put this pdf under version control, in the same branch,
tag/label or release info as your code-to-be-released.


{#q-G-3}
#### Question G-3: How does versioning work with graphical models?

Although some tool vendors argue differently, recognizing the meaning
of differences in diagrams imho requires human intelligence:
I (Gernot) have not yet found any automatism supporting meaningful _diff_
of diagrams or images. In my opinion somebody needs to care for
new versions of diagrams.

It's often a good idea to (automatically) include the modification date
in a diagram (some modeling tools support this feature).



{#q-G-4}
#### Question G-4: How can I describe several _variants_ of a system?

<t.b.d.>


A>#### Your question has not been answered?
A>Tell us:
A>
A>* via [email](mailto:info@arc42.de) to info@arc42.de or
A>* on our [github issue tracker](https://github.com/arc42/arc42-template/issues) at https://github.com/arc42/arc42-template/issues.
A>* or on [Twitter (@arc42Tipps)](https://twitter.com/arc42Tipps).
