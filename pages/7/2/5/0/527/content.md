* tic
{:toc}

This is an experiment in collaboration. I want to write an article about discrete causal spaces. Please help. Coauthors welcome! - [[Eric Forgy|Eric]]

# Goals #

1. Construct a generalization of [[ericforgy:Discrete differential geometry on causal graphs|Discrete differential geometry on causal graphs]] to $n$-dimensional discrete causal spaces that are _locally_ like $n$-diamonds (see the paper for a description of $n$-diamonds until a page is created).

1. The continuum limit of a discrete causal space should be a [[directed space]], or more specifically, a [[smooth Lorentzian space]].

1. Etc

# Abstract #

...

# Introduction #

We need a good category-friendly definition of an $n$-diamond. Here's a first stab that is incomplete, but hopefully gets the ball rolling.

**(Tentative/Incomplete) Definition:** An $n$-diamond is a minimal [[causet]].

**(Tentative/Incomplete) Definition:** An $n$-diamond complex is a [[directed n-graph]] in which each node has exactly $n$ edges directed into it and exactly $n$ nodes directed away from it _and each ??? has fillers_.

**Example:** $\mathbb{Z}^n$ with the its obvious $r$-diamond faces, $0\le r\le n$ is an $n$-diamond complex.

# References #

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))
* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88--100.
* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))
* Fajstrup, Rosicky, _A convenient category for directed homotopy_ ([arXiv](http://arxiv.org/abs/0708.3937))
* Dan Christensen, and Louis Crane, _Causal sites as quantum geometry_ ([arXiv](http://arxiv.org/abs/gr-qc/0410104))
+--{.query}
[[Eric]]: They use the word "diamond". I hope that catches on.
=--
* Louis Crane, _Model categories and quantum gravity_ ([arXiv](http://arxiv.org/abs/0810.4492))
* Bombelli, Henson, Sorkin, _Discreteness without symmetry breaking: a theorem_ ([arXiv](http://arxiv.org/abs/gr-qc/0605006))
* Dagstuhl Seminar Proceedings 04351, _Spatial Representation: Discrete vs. Continuous Computational Models_, ([web](http://drops.dagstuhl.de/portals/index.php?semnr=04351))

See also:

* [[directed homotopy theory]].

***

# Discussion #

_Note.  Topics will be separated by lines and each topic is presented in reverse chronological order._

[[JA]]: Just starting reading this and don't know much about diamonds yet, but I have been working on logic-based approaches to discrete dynamics &#8212; that I sometimes think of as differential geometry over GF(2) &#8212; for quite a while now.  You might take a gander at my [Magnum Opiate](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_and_Dynamic_Systems_2.0) and we could see if it fits in here somewhere.

***

[[Eric]]: Motivated by some emails from [[Tim Porter|Tim]], I think we could use pages on [[causal site]] and [[dg-quiver]]. I am particularly interested in seeing a definition of [[dg-quiver]].

***

[[Eric]]: I wonder if $n$-diamonds should be more closely related to [[n-fold categories]] rather than [[posets]]?

***

(From nCafe: <a href="http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c021347">Authorship</a>)

_[[Urs Schreiber|Urs]] says_: I think Eric wants a [[partial order|poset]] of sorts.

It seems that a good formalization of "[[smooth Lorentzian space|smooth Lorentzian space(time)]]" is something like: a [[partial order|poset]] [[internal category|internal]] to a category of measure spaces.

There are some immediate possibilities about graph versions of this statement that come to mind. For one, a discrete "Lorentzian spacetime" should be a poset such that all causal subsets are finite set.

A [[causet|causal subset]] in a poset $X$ is what John in his latest <a href="http://golem.ph.utexas.edu/category/2009/01/hopf_algebras_from_posets.html">entry</a> calls an "interval", namely for two objects $x,y$ in the poset the [[under category|under-over category]]

$$x\darr X\darr y$$

of all objects in the past of $x$ and in the future of $y$.

_[[Tim Porter|Tim]]_: In a poset one can define a diamond as being an order convex subset possibly with extra properties: U is order convex if $x$, $z$ are in $U$ with $x \lt z$, and $y$ lies between $x$ and $z$ ($x\lt y \lt z$). 

One possible interpretation of what Eric wants is that one specifies a collection of order convex subsets with inclusion on them making a directed set or possibly a lattice. (sort of needing to capture that diamonds should intersect in diamonds  (or not at all). Something like this is used by John Roberts in some of his work I seem to remember. 

 Reminder ('cos I thought this had been mentioned in the caf&#233;) it may also pay to look at gr-qc/0410104 for some ideas but I never convinced myself that that was really what was needed.

category: drafts

[[!redirects Discrete Causal Spaces]]