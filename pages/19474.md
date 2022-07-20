
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea

**Guarded recursion** is a form of [[recursion]] that ensures that solutions of self-referential descriptions exist. This is achieved by "guarding" the recursive occurrence of the object under consideration using a unary [[modality]] $\blacktriangleright$ and pronounced "later". 

The *later modality* was first considered by Nakano ([Nakano 2000](#Nakano00)) and used to  ensure *productivity* of [[coinduction|coinductively]] defined [[programs]]. 

For example, for an object $A$, the [[type]] of *guarded streams* is the unique solution to the equation
\[
\text{Str}_g A \cong A \times \blacktriangleright \text{Str}_g A
\]

The intended meaning is that the head of the stream is available now while the tail is only available after one step of computation. 

(There are other forms of guarded recursion which act through syntactic restriction.)


## Related concepts

* [[synthetic guarded domain theory]]

## References

* Robert Atkey, Conor McBride, _Productive Coprogramming with Guarded Recursion_, ([Productive Coprogramming with Guarded Recursion](https://bentnib.org/productive.pdf))

* Aleš Bizjak, _On Semantics and Applications of Guarded Recursion_, ([PhD thesis](https://abizjak.github.io/documents/thesis/semantics-applications-gr.pdf))

* Ranald Clouston, Aleš Bizjak, Hans Bugge Grathwohl, Lars Birkedal, _The Guarded Lambda-Calculus: Programming and Reasoning with Guarded Recursion for Coinductive Types_, ([arXiv:1606.09455](https://arxiv.org/abs/1606.09455))

* {#Nakano00} Nakano Hiroshi, 2000, _A Modality for Recursion_. In Logic in Computer Science (LICS’00). ([pdf](https://pdfs.semanticscholar.org/a177/47f98e5b821f03ec8be858794f2f83a683b7.pdf))

* [[Lars Birkedal]], Ales Bizjak, Ranald Clouston, Hans Bugge Grathwohl, [[Bas Spitters]], Andrea Vezzosi, _Guarded cubical type theory_ [arxiv](https://arxiv.org/abs/1611.09263)

* [[Jon Sterling]], [[Robert Harper]], *Guarded Computational Type Theory*, LICS '18 (2018) 879–888 &lbrack;[arxiv:1804.09098](https://arxiv.org/abs/1804.09098), [doi:10.1145/3209108.3209153](https://doi.org/10.1145/3209108.3209153)&rbrack;

A general calculus for dependent modal type theories.

*  Ranald Clouston, Bassel Mannaa, Rasmus Ejlers Møgelberg, Andrew M. Pitts, [[Bas Spitters]], _Modal Dependent Type Theory and Dependent Right Adjoints_ [arxiv](https://arxiv.org/abs/1804.05236)