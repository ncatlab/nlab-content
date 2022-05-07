
#Contents#
* table of contents
{:toc}

## Idea

Domain theory has its origin in the problem in finding a viable [[denotational semantics]] for certain theories of [[computability]] (such as the untyped lambda calculus) which resist straightforward interpretations in terms of sets and functions. It has since grown into an area which weaves together diverse strands in [[logic]], computability, lattice theory, general [[topology]], and [[category theory]]. 

Domain theory can be said to have come into existence with [[Dana Scott]]'s solution for interpreting untyped lambda calculus in terms of continuous lattices. In rough terms, the problem can be set out as follows: 

* [[lambda calculus|Lambda calculus]] is a syntax of functions and functional application, whose basic constituents are types, terms of types, and type and term formation schemes with which one can speak of product types $A \times B$ and function space types $A \Rightarrow B$. 

* One problem is to construct a meaning or semantics for this syntax in terms of "actual" elements and functions. In category-theoretic terms, lambda calculus is naturally modeled by cartesian closed categories, in which types are interpreted as objects $A$ and terms are interpreted as (generalized) elements or "functions" $X \to A$. 

* In so-called untyped lambda calculus (whose syntax is closely connected with the theory of computability and recursive functions), all terms may be regarded as being of the same type $D$ (which therefore need not be mentioned, hence "untyped"), so that intuitively speaking, elements of $D$ and functions on $D$ are treated on one and the same footing. 

* The problem Scott solved is to faithfully model untyped lambda calculus; in categorical terms, the basic problem is to construct a cartesian closed category with just one object $D$ (or rather, two objects: $D$ and a terminal object $1$), so that $D$ is closed under formation of products and function spaces: $D \cong D \times D$ and $D \cong D \Rightarrow D$. Notice that in the category of sets, the only solution is to take $D \cong 1$, so that all terms are then equal ("algorithmic inconsistency"). This is not a faithful modeling of untyped lambda calculus, which has provably unequal terms. 

In 1969, Dana Scott solved this problem topologically: the terms were interpreted as continuous functions on a suitable space $D$ isomorphic to its own function space. This $D$ is called a _domain_. Decades later, we now know many techniques for constructing such domains as suitable objects in cartesian closed categories, but Scott's basic insight, that computability could be interpreted as continuity, 
continues to exert a decisive influence today. 

## Terminology

[[Martín Escardó]] writes on the [nForum](https://nforum.ncatlab.org/discussion/10150/dcpo/?Focus=90736#Comment_90736):

> The usual practice of [[domain theory]] papers and talks is to start by defining “domain” for the purposes of the paper or talk. It is a reusable word. Usually only compound words using the word “domain” have a fixed meaning, such as [[Scott domain]] (bounded complete [[algebraic dcpo]]), [[continuous Scott domain]] (bounded complete [[continuous dcpo]]), [[FS domain]], [[SFP domain]], [[L-domain]]. I wouldn’t use the plain word “domain” in a paper without first explicitly defining it, as it has been used with so many different meanings in the domain theory literature. Also the terminological conventions vary a bit depending on whether domain theory is used for the purposes of computation (e.g., [[programming language semantics]], and [[theory of computability]]) or [[topology]] and [[algebra]]. For example, in [[programming language semantics]] papers one often encounters [[posets]] that have sups of ascending sequences, rather than [[directed sets]], and a least element, because all the authors are interested in is the existence of (least) fixed point of continuous endo-functions, and these assumptions are enough for this purpose. Such [[posets]] are often called domains in such papers. But for applications of [[domain theory]] to [[topology]], [[directed completeness]] is what one needs in general, and often we have more (even all sups — for example, a topological space is [[exponentiable]] if its [[lattice]] of open sets is a [[continuous dcpo]] — but this [[dcpo]] has all sups and moreover is a [[distributive lattice]], and the [[continuous distributive lattices]] are precisely the topologies of [[exponentiable spaces]], up to isomorphism). Because these applications and communities are so diverse, it is natural to see a divergence of terminology, even if many of the techniques are the same.

## Related concepts

* [[topological domain theory]]
* [[synthetic domain theory]]

## References

* [Wikipedia](http://en.wikipedia.org/wiki/Domain_theory)(English)


* Notes available online by Abramsky and Jung: [here](http://www.cs.bham.ac.uk/~axj/pub/papers/handy1.pdf)

* Notes by Gordon Plotkin, [here](http://homepages.inf.ed.ac.uk/gdp/publications/Domains_a4.ps)

* [Domain theory and general relativity](http://www.cs.mcgill.ca/~prakash/Pubs/dom_gr_review.pdf), Keye Martin and [[Prakash Panangaden]]

>**Summary**. We discuss the current state of investigations into the domain theoretic structure of spacetime, including recent developments which explain the connection between measurement, the Newtonian concept of time and the Lorentz distance.

* [A Domain of Spacetime Intervals in General Relativity](http://www.cs.mcgill.ca/~prakash/Pubs/cmp.pdf), Keye Martin and [[Prakash Panangaden]]

> **Abstract**: We prove that a globally hyperbolic [[spacetime]] with its causality relation is a bicontinuous [[poset]] whose interval topology is the manifold topology. From this one can show that from only a countable dense set of events and the causality relation, it is possible to reconstruct a globally hyperbolic spacetime in a purely order theoretic manner. The ultimate reason for this is that globally hyperbolic spacetimes belong to a category that is equivalent to a special category of domains called interval domains. We obtain a mathematical setting in which one can study causality independently of geometry and differentiable structure, and which also suggests that spacetime emerges from something discrete.

Discussion in [[homotopy type theory]]/[[univalent foundations]]:

* {#deJongEscardo21} [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))



category: computer science