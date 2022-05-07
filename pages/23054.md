##Idea

Coming originally from the theory of  [[poset|(partially) ordered sets]], the notion of residuated morphism or residuated mapping is, from a categorical viewpoint, just the condition that a map of posets when considered as a functor between the corresponding categories, has a left adjoint.

The notion is used in the theory of [[idempotent semirings]] to give a form of `pseudo-solution' to equations which fail to have actual solutions.

## Definition
 {#Definition}


Given [[posets]] $(E,\le)$ and $(F,\le)$, a monotone map, $f:E\to F$ is said to be _residuated_ if, and only if, for each $y\in F$, the set $\{x\in E\mid f(x)\le y\}$ has a maximal element, which we denote $f^\#(y)$.

##Translation into categorical terms

Each poset gives a small category, and each monotone map gives a functor.  From the categorical viewpoint, the condition that $f$ be residuated interprets as saying it has a left adjoint.

More exactly, the assignment $y\mapsto f^#(y)$ defines a monotone mapping $f^\#:F\to E$ called the _residual mapping_.  We have 

$$f\circ f^\# \le id_F$$

and 

$$f^\#\circ f \ge id_F.$$

##Standard example

The [[ceiling]] function $\lceil{-}\rceil:\mathbb{R}\to \mathbb{Z}$ is residuated. (The details are given in the discussion at [[floor]].)

##Related entries

* [[residuated lattice]]

* [[residuated idempotent semiring]]

* [[Galois connection]]




##References.

One of the standard references for the poset viewpoint is

* T. S. Blyth and M. F. Janowitz, _Residuation Theory_, Pergamon Press, 1972.

The Wikipedia entry is

* [residuated mapping](https://en.wikipedia.org/wiki/Residuated_mapping)

[[!redirects residuated mapping]]