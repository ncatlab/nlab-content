
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _codiscrete groupoid_ on a [[set]] is the [[groupoid]] whose [[object]]s are the elements of the [[set]] and which has a _unique [[morphism]]_ for every ordered pair of objects.

This is also called the **pair groupoid** of $X$ and sometimes the _chaotic groupoid_ on $X$.

## Definition

For $X$ set, the **codiscrete groupoid** of $X$ is the groupoid $Codisc(X)$ with

* $Obj(X) = X$;

* $Mor(X) = X \times X$.

This definition makes sense also [[internal category|internally]], for $X$ an object in any category with finite [[limit]]s. (In fact, this is one of those cases where the category can easily be defined with some limits lacking; we need only finite [[product]]s of $X$.)


## Remarks

* Every codiscrete groupoid on an [[inhabited set]] is [[contractible space|contractible]]: [[equivalence of categories|equivalent]] to the [[point]]. More generally, any codiscrete groupoid is equivalent to a [[truth value]].

* The codiscrete groupoid on $X$ is also sometimes called the _chaotic groupoid_ on $X$. The intuition is probably that "everything being connected with everything else sounds pretty chaotic", but one can argue that the term "chaotic groupoid" exactly misses the true intrinsic nature of codiscrete groupoids: since these are all just "puffed up versions of the point" they are "maximally homogenous" things. Which space would be less chaotic than the point?

* For $X$ a [[finite set]] of cardinality $n \gt 0$, the [[category algebra]] of $Codisc(X)$ is the algebra of $n\times n$ matrices. The contractibility of $Codisc(X)$ is reflected in the fact that this algebra is [[Morita equivalence|Morita equivalent]] to the [[ground ring]], which is the category algebra of the [[point]].

  This maybe serves to illustrate: even though codiscrete groupoids are pretty trivial, they are not too trivial to be entirely without interest. Often it is useful to have big puffed-up versions of the point available.

## Discussion

+--{.query}

[[Eric Forgy|Eric]]: If true, is it worth pointing out that the underlying [[directed graph]] is complete? 

[[Todd Trimble|Todd]]: I know what you're saying, and it's the correct picture, but 'complete' here refers to a definition of directed graph which is not the one used [[directed graph|here]], where there can be multiple edges from a given source to given target. Graph theorists who speak of 'complete' intend digraph to mean at most one edge from given source to given target. In different language, given by an incidence matrix with 0's and 1's. Equivalently, given by a binary relation on the set of nodes. 

_Toby_:  Being a complete directed graph (in the graph theorists\' usual sense) is still a reasonable property of a directed pseudomultigraph (our kind).  And since there\'s no way that a multigraph can be complete in the sense of having as many edges as possible, I would still use the term 'complete' here.  It\'s a sort of existence *and uniqueness* condition, like a universal property.

=--


[[!redirects codiscrete category]]


[[!redirects codiscrete groupoids]]

[[!redirects pair groupoid]]
[[!redirects pair groupoids]]

[[!redirects chaotic groupoid]]
[[!redirects chaotic groupoids]]