

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

*Domain theory* has its origin in

1. topological algebra concerned with Lawson semilattices,

1. [[computer science]], concerned with the problem of finding a viable [[denotational semantics]] for certain theories of [[computability]] (such as the untyped [[lambda calculus]]): this resists straightforward interpretations in terms of plain [[functions]] between sets but does have interpretation in terms of [[monotone functions]] between [[partially ordered sets]] (certain [[lattices]]) &lbrack;[Scott (1970)](#Scott70), [Scott & Strachey (1971)](#ScottStrachey71)&rbrack;. 

The theory has since grown into an area which weaves together diverse strands in [[logic]], [[computability]], [[lattice]] theory, [[general topology]], and [[category theory]]. 

Domain theory can be said to have come into existence with the insight from [Scott (1970)](#Scott70) of interpreting untyped [[lambda calculus]] in terms of [[monotone functions]] between [[continuous lattices]]. In rough terms, the problem can be set out as follows: 

* [[lambda calculus|Lambda calculus]] is a [[syntax]] of [[functions]] and [[functional]] application, whose basic constituents are [[types]], [[terms]] of types, and type and term [[type formation|formation schemes]] with which one can speak of [[product types]] $A \times B$ and [[function types]] $A \Rightarrow B$. 

* One problem is to construct a *meaning* or *[[semantics]]* for such [[syntax]] in terms of "actual" [[sets]] and [[functions]]. The [[categorical semantics]] of [[lambda calculus]] is by [[cartesian closed categories]], in which [[types]] are interpreted as [[objects]] $A$ and [[terms]] are interpreted as ([[generalized element|generalized]]) [[elements]] or "functions" $X \to A$. 

* In so-called untyped lambda calculus (whose [[syntax]] is closely connected with the theory of [[computability]] and [[recursive functions]]), all [[terms]] may be regarded as being of the same [[type]] $D$ (which therefore need not be mentioned, hence "untyped"), so that, intuitively speaking, elements of $D$ and functions on $D$ are treated on one and the same footing. 

* The problem Scott solved is to give faithful [[categorical semantics]] for untyped lambda calculus; where the basic problem is to construct a [[cartesian closed category]] with essentially just one [[object]] $D$ (really two objects: $D$ and a [[terminal object]] $1$), so that $D$ is closed under formation of [[products]] and [[internal homs]]: $D \cong D \times D$ and $D \cong D \Rightarrow D$. Notice that in the [[category of sets]], the only solution is to take $D \cong 1$, so that all terms are then equal ("algorithmic inconsistency"). This is not a faithful modeling of untyped lambda calculus, which has provably unequal terms. 

In 1969, Dana Scott solved this problem topologically: the terms were interpreted as continuous functions on a suitable space $D$ isomorphic to its own function space. This $D$ is called a _domain_. Decades later, we now know many techniques for constructing such domains as suitable objects in cartesian closed categories, but Scott's basic insight, that computability could be interpreted as continuity, 
continues to exert a decisive influence today. 

## Terminology

[[Martín Escardó]] writes on the [nForum](https://nforum.ncatlab.org/discussion/10150/dcpo/?Focus=90736#Comment_90736):

> The usual practice of [[domain theory]] papers and talks is to start by defining “domain” for the purposes of the paper or talk. It is a reusable word. Usually only compound words using the word “domain” have a fixed meaning, such as [[Scott domain]] (bounded complete [[algebraic dcpo]]), [[continuous Scott domain]] (bounded complete [[continuous poset|continuous]] [[dcpo]]), [[FS domain]], [[SFP domain]], [[L-domain]]. I wouldn’t use the plain word “domain” in a paper without first explicitly defining it, as it has been used with so many different meanings in the domain theory literature. Also the terminological conventions vary a bit depending on whether domain theory is used for the purposes of computation (e.g., [[denotational semantics|programming language semantics]], and [[computability|theory of computability]]) or [[topology]] and [[algebra]]. For example, in programming language semantics papers one often encounters [[posets]] that have sups of ascending sequences, rather than [[directed sets]], and a least element, because all the authors are interested in is the existence of (least) fixed point of continuous endo-functions, and these assumptions are enough for this purpose. Such [[posets]] are often called domains in such papers. But for applications of [[domain theory]] to [[topology]], [[dcpo|directed completeness]] is what one needs in general, and often we have more (even all sups — for example, a topological space is [[exponentiable object|exponentiable]] if its [[lattice]] of open sets is a [[continuous poset|continuous]] [[dcpo]] — but this [[dcpo]] has all sups and moreover is a [[distributive lattice]], and the continuous distributive lattices are precisely the topologies of [[exponentiable object|exponentiable spaces]], up to isomorphism). Because these applications and communities are so diverse, it is natural to see a divergence of terminology, even if many of the techniques are the same.

## Related concepts

* [[topological domain theory]]

* [[synthetic domain theory]]

* [[synthetic guarded domain theory]]

* [[denotational semantics]]

## References

### In computation theory

Origin of domain theory in [[denotational semantics]] for [[programming languages]]:

* {#Scott70} [[Dana S. Scott]], *Outline of a mathematical theory of computation*, in: Proceedings of the *Fourth Annual Princeton Conference on Information Sciences and Systems* (1970) 169–176. &lbrack;[pdf](https://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf), [[Scott-TheoryOfComputation.pdf:file]]&rbrack;

* {#ScottStrachey71} [[Dana S. Scott]], [[Christopher Strachey]], *Toward a Mathematical Semantics for Computer Languages*, Oxford University Computing Laboratory, Technical Monograph PRG-6 (1971) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/3228/PRG06.pdf), [[ScottStrachey-MathematicalSemantics.pdf:file]]&rbrack;

* {#Scott76} [[Dana Scott]], *Data types as lattices*. SIAM Journal of Computing **5** 3 (1976) 522--587 &lbrack;[doi:10.1137/0205037](https://doi.org/10.1137/0205037), [pdf](https://www.cs.ox.ac.uk/files/3287/PRG05.pdf)&rbrack;

Discussion [[internalization|internal]] to [[cartesian closed categories]]:

* [[Michael Barr]], *Fixed points in cartesian closed categories*, Theoretical Comp. Sci. **70** (1990) 65–72 &lbrack;<a href="https://doi.org/10.1016/0304-3975(90)90152-8">doi:10.1016/0304-3975(90)90152-8</a>, [pdf](https://www.math.mcgill.ca/barr/papers/dom.pdf), [[Barr-FixedPointsInCCCs.pdf:file]]&rbrack;

Introductions and lecture notes:

* [[Robert D. Tennent]], *The denotational semantics of programming languages*, Communications of the ACM **19** 8 (1976) 437–453 &lbrack;[doi:10.1145/360303.360308](https://doi.org/10.1145/360303.360308), [pdf](https://dl.acm.org/doi/pdf/10.1145/360303.360308)&rbrack;

* [[Andrew M. Pitts]], *Lecture Notes on Denotational Semantics* (2012) &lbrack;[pdf](https://www.cl.cam.ac.uk/teaching/1112/DenotSem/dens-notes-bw.pdf), [[Pitts-DenotationalSemantics.pdf:file]]&rbrack;


Textbook accounts:

* [[Glynn Winskel]], §8 of: *The Formal Semantics of Programming Languages*, MIT Press (1993) &lbrack;[ISBN:9780262731034](https://mitpress.mit.edu/9780262731034/the-formal-semantics-of-programming-languages/), [pdf](https://www.cin.ufpe.br/~if721/intranet/TheFormalSemanticsofProgrammingLanguages.pdf)&rbrack;

* [[David A. Schmidt]], *Denotational Semantics -- A methodology for language development*, Allyn and Bacon (1986)  &lbrack;[pdf](https://people.cs.ksu.edu/~schmidt/text/DenSem-full-book.pdf), [webpage](https://people.cs.ksu.edu/~schmidt/text/densem.html)&rbrack;

* {#GierzHofmannKeimelLawsonLisloveScott03} G. Gierz, [[Karl H. Hofmann]], K. Keimel, J. D. Lawson, M. Mislove, [[Dana S. Scott]], *Continuous Lattices and Domains*, in: *Encyclopedia of Mathematics and its Applications* **93**, Cambridge University Press (2003)  &lbrack;[doi:10.1017/CBO9780511542725](https://doi.org/10.1017/CBO9780511542725)&rbrack;

* [[Thomas Streicher]], *Domain-Theoretic Foundations of Functional Programming*, World Scientific (2006) &lbrack;[pdf](https://doc.lagout.org/programmation/Functional%20Programming/Domain-Theoretic%20Foundations%20of%20Functional%20Programming%20%5BStreicher%202006-12-04%5D.pdf), [doi:10.1142/6284](https://www.worldscientific.com/worldscibooks/10.1142/6284)&rbrack;



See also:

* Wikipedia, *[Domain theory](http://en.wikipedia.org/wiki/Domain_theory)*


Discussion in [[homotopy type theory]]/[[univalent foundations]]:

* {#deJongEscardo21} [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

Review:

* [[Samson Abramsky]], [[Achim Jung]], *Domain Theory*, in: *[[Handbook of Logic in Computer Science]]* **3**, Oxford University Press (1995) &lbrack;[ISBN:9780198537625](https://global.oup.com/academic/product/handbook-of-logic-in-computer-science-9780198537625?cc=de&lang=en&), [pdf](https://www.cs.bham.ac.uk/~axj/pub/papers/handy1.pdf)&rbrack;

* Gordon Plotkin, *Pisa Notes on Domains* &lbrack;[ps](http://homepages.inf.ed.ac.uk/gdp/publications/Domains_a4.ps)&rbrack;

### Relation to causets
 {#ReferencesRelationToCausets}

Possible relation to [[spacetime]] [[causality]] (cf. *[[causets]]*):

* [Domain theory and general relativity](http://www.cs.mcgill.ca/~prakash/Pubs/dom_gr_review.pdf), Keye Martin and [[Prakash Panangaden]]

>**Summary**. We discuss the current state of investigations into the domain theoretic structure of spacetime, including recent developments which explain the connection between measurement, the Newtonian concept of time and the Lorentz distance.

* [A Domain of Spacetime Intervals in General Relativity](http://www.cs.mcgill.ca/~prakash/Pubs/cmp.pdf), Keye Martin and [[Prakash Panangaden]]

> **Abstract**: We prove that a globally hyperbolic [[spacetime]] with its causality relation is a bicontinuous [[poset]] whose interval topology is the manifold topology. From this one can show that from only a countable dense set of events and the causality relation, it is possible to reconstruct a globally hyperbolic spacetime in a purely order theoretic manner. The ultimate reason for this is that globally hyperbolic spacetimes belong to a category that is equivalent to a special category of domains called interval domains. We obtain a mathematical setting in which one can study causality independently of geometry and differentiable structure, and which also suggests that spacetime emerges from something discrete.

### Categorical notions of domain
 {#ReferencesCategoricalNotionsOfDomain}

In [[category theory|category theoretic]] generalizations of  the notion, the informal idea is to replace [[partial orders]] with more general [[categories]], so that there is more space for intensionality. An early reference, which proposes  the notion of *[[Scott-complete categories]]*:

* [[Jiří Adámek]], *A categorical generalization of Scott domains*, Mathematical Structures in Computer Science **7** 5  (1997) 419 - 443 &lbrack;[doi:10.1017/S0960129597002351](https://doi.org/10.1017/S0960129597002351)&rbrack;

The following reference proposes using [[presheaf categories]] as a generalization of prime [[algebraic lattices]]. This also connects to work on [[species#variants|generalized species]]:

* [[Mikkel Nygaard]], [[Glynn Winskel]], *Domain theory for concurrency*, Theoretical Computer Science
**316** 1–3 (2004) 153-190 &lbrack;[doi:10.1016/j.tcs.2004.01.029](https://doi.org/10.1016/j.tcs.2004.01.029), [pdf](https://www.cl.cam.ac.uk/~gw104/DomThy.pdf)&rbrack;



category: computer science