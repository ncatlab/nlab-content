# Bidirectional typechecking

* table of contents
{: toc}

## Idea

*Bidirectional typechecking* is both a style of mathematical presentation of a [[type theory]] and a kind of [[algorithm]] for implementing one.  The idea is that the basic [[judgment]] $t:A$ that a [[term]] $t$ belongs to a [[type]] $A$ is split into two judgments:

* $t \Leftarrow A$: the term $t$ can be *checked* to have the type $A$.
* $t \Rightarrow A$: from the term $t$ we can *infer*, or *synthesize*, the type $A$ that it has.

The difference is that in $t\Leftarrow A$ we regard both $t$ and $A$ as "given" or "inputs", whereas in $t\Rightarrow A$ we regard only $t$ as an "input" and $A$ as an "output" that is "computed" from $t$.  When presented as a pure [[deductive system]], these "input/output modes" do not mean anything, but when implemented as an algorithm they mean that we have two mutually recursive functions:

* $check(t,A)$ which simply succeeds or fails.
* $infer(t)$ which either returns a type $A$ or fails.

See [[logic programming]].

For example, from an un-annotated $\lambda$-abstraction such as the identity function $\lambda x.x$ we cannot infer its type: the variable $x$, and hence the result, could have any type.  But we can *check* that it has any given endomorphism type: $(\lambda x.x) \Leftarrow (A\to A)$ for any type $A$.  On the other hand, if we can infer a type for the function $f$, i.e. $f\Rightarrow (A\to B)$ (for instance, $f$ could be a variable, since variables are declared with their types), and we can check that an argument $a$ has type $A$ (that is, $a\Leftarrow A$), then we can also infer that the application $f(a)$ has type $B$, that is $f(a) \Rightarrow B$.  These observations correspond to bidirectional refinements of the usual typing rules for abstractions and applications:

$$ \frac{\Gamma,x:A \vdash M \Leftarrow B}{\Gamma\vdash (\lambda x.M) \Leftarrow (A\to B)} \qquad \frac{\Gamma\vdash f \Rightarrow (A\to B) \qquad \Gamma\vdash a \Leftarrow A }{\Gamma \vdash f(a) \Rightarrow B}.$$

Bidirectional typechecking is closely related to "canonical forms only" presentations of type theories (such as [[logical frameworks]]) that involve [[hereditary substitution]].  For instance, because we infer a type for an application $f(a)$ by inferring a type for $f$, but we can only *check* the type of an un-annotated abstraction $\lambda x.M$, an un-augmented bidirectional theory cannot typecheck a $\beta$-redex (see [[beta-reduction]] $(\lambda x.M)(a)$.  Thus it is a natural system in which to describe a type theory in which only canonical forms (no redexes) exist.  But it is also easy to augment a bidirectional system with [[type ascription]], which mediates between the two modes and allows typechecking redexes: if we can check $t\Leftarrow A$, then we can *infer* the same type of the *ascribed* term $(t:A)\Rightarrow A$, allowing a redex to be written as $(\lambda x.M : A\to B)(a)$.

+-- {: .un_remark}
###### Remark
There are many different notations used in the literature for the bidirectional typing judgments.  Sometimes one finds $t\rightrightarrows A$ and $t\leftleftarrows A$ in place of our $t\Rightarrow A$ and $t\Leftarrow A$.  Other times the order of the term and the type is reversed, for instance writing $t\in A$ for inferring and $A\ni t$ for checking.  Sometimes upwards and downwards-pointing arrows are used instead of leftwards and rightwards ones (e.g. $t \uparrow A$ and $t \downarrow A$, or maybe $t :^\uparrow A$ and $t :^\downarrow A$ or a dozen other variants) --- but unfortunately there is no consensus on which judgment points up and which points down!  It seems to be somewhat more common for checking to point up and inference to point down, as this matches the direction that "information flows through the derivation tree", but the opposite convention is found in plenty of papers too.  (It could be that there is a "modern" consensus that only older papers violate.)
=--

## References

### General

* [[Jana Dunfield]], [[Neel Krishnaswami]], *Bidirectional Typing* (Survey), 2019, ([pdf](https://www.cl.cam.ac.uk/~nk480/bidir-survey.pdf))

* Pierce, B. C., Turner, D. N.: _Local Type Inference_, ACM SIGPLAN–SIGACT Symposium on Principles of Programming Languages (POPL), San Diego, California, 1998, Full version in ACM Transactions on Programming Languages and Systems (TOPLAS), 22(1), January 2000, pp. 1–44, ([pdf](http://www.cis.upenn.edu/~bcpierce/papers/lti-toplas.pdf)).  This is usually cited as the "original" paper on bidirectional typechecking.

* [[Frank Pfenning]], *Lecture Notes on Bidirectional Type Checking*, [pdf](https://www.cs.cmu.edu/~fp/courses/15312-f04/handouts/15-bidirectional.pdf)

* [[Conor McBride]], *Basics of bidirectionality*, [blog post](https://pigworker.wordpress.com/2018/08/06/basics-of-bidirectionalism/)

* David Christiansen, *Bidirectional typing rules: a tutorial*, [pdf](http://www.davidchristiansen.dk/tutorials/bidirectional.pdf)

### For dependent types

* [[Thierry Coquand]], *An algorithm for type-checking dependent types*, 1996, [pdf](https://core.ac.uk/download/pdf/82345314.pdf)

* Thierry Coquand and Makoto Takeyama, *An Implementation of Type:Type*, 2002, [springerlink](https://link.springer.com/chapter/10.1007/3-540-45842-5_4)

* Ulf Norell, *Towards a practical programming language based on dependent type theory*. PhD thesis, Chalmers University of Technology and Göteborg University, 2007. [web](http://www.cse.chalmers.se/~ulfn/papers/thesis.html)

* Andreas Abel, Thierry Coquand, Peter Dybjer _Verifying a Semantic $\beta\eta$-Conversion Test for Martin-L&ouml;f Type Theory (extended version)_, 2008 [semantic scholar (includes pdf)](https://www.semanticscholar.org/paper/Verifying-a-Semantic-%CE%B2%CE%B7-Conversion-Test-for-Type-(-Abel-Coquand/ea73f57e4f1111b136cb9f0659c627dba25e53c8)

* Andreas Abel and [[Thorsten Altenkirch]], *A partial type checking algorithm for $Type:Type$*, 2008, [pdf](http://www.cs.nott.ac.uk/~psztxa/publ/msfp08.pdf)

* Andres L&ouml;h, Conor McBride and Wouter Swierstra, *A Tutorial Implementation of a Dependently Typed Lambda Calculus*, 2009, [web](https://www.andres-loeh.de/LambdaPi/) (includes Haskell code)

* Andrea Asperti, Wilmer Ricciotti, Claudio Sacerdoti Coen, and Enrico Tassi. *A bi-directional refinement algorithm for the calculus of (co)inductive constructions*, 2012, [arxiv](https://arxiv.org/abs/1202.4905)

* Kevin Watkins, Iliano Cervesato, Frank Pfenning, and David Walker. *A concurrent logical framework I: Judgments and properties*. Technical Report CMU-CS-02-101, Department of Computer Science, Carnegie Mellon University, 2002. Revised May 2003, [pdf](http://www.cs.cmu.edu/~fp/papers/CMU-CS-02-101.pdf)

### Other type theories

* Rowan Davies and [[Frank Pfenning]]. *Intersection types and computational effects*. In P. Wadler, editor, Proceedings of the Fifth International Conference on Functional Programming (ICFP'00), pages 198-208, Montreal, Canada, September 2000. ACM Press. [pdf](http://www.cs.cmu.edu/~fp/papers/icfp00.pdf)

* [[Jana Dunfield]] and [[Frank Pfenning]]. *Tridirectional typechecking*. In X.Leroy, editor, Conference Record of the 31st Annual Symposium on Principles of Programming Languages (POPL'04), pages 281-292, Venice, Italy, January 2004. ACM Press. Extended version available as Technical Report CMU-CS-04-117, March 2004. [pdf](http://www.cs.cmu.edu/~fp/papers/popl04.pdf)

* [[Jana Dunfield]], Neelakantan R. Krishnaswami, *Complete and Easy Bidirectional Typechecking for Higher-Rank Polymorphism*, 2013, [arxiv](https://arxiv.org/abs/1306.6032)

* Francisco Ferreira and Brigitte Pientka, *Bidirectional Elaboration of Dependently Typed Programs*, 2014, [pdf](https://www.cs.mcgill.ca/~fferre8/papers/BidirectionalElaboration.pdf).  Despite the name, this paper is not about full [[dependent type theory]] but only has one level of dependency.

* [[Jana Dunfield]], Neelakantan R. Krishnaswami, *Sound and Complete Bidirectional Typechecking for Higher-Rank Polymorphism with Existentials and Indexed Types*, 2016, [arxiv](https://arxiv.org/abs/1601.05106)

[[!redirects bidirectional type checking]]
[[!redirects bidirectional type-checking]]
[[!redirects type inference]]
[[!redirects type synthesis]]
