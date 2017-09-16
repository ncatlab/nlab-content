> [[Urs Schreiber|Urs]]: after writing this I remembered that there is already [[indiscrete category]]. Will merge both entries...

#Idea#

The _codiscrete groupoid_ on a [[set]] is the [[groupoid]] whose [[object]]s are the elements of the [[set]] and which has a _unique morphism_ for every ordered pair of objects.

#Definition#

For $X$ set, the **codiscrete groupoid** of $X$ is the groupoid $Codisc(X)$ with

* $Obj(X) = X$;

* $Mor(X) = X \times X$.

This definition makes sense also [[internal category|internally]], for $X$ an object in any category with finite [[limit]]s.

+--{.query}

[[Eric Forgy|Eric]]: If true, is it worth pointing out that the underlying [[directed graph]] is complete?

=--

#Remarks#

* Every codiscrete groupoid is [[equivalence of caategories|equivalent]] to the [[point]].

* The codiscrete groupoid is also sometimes called the _chaotic groupoid_ on $X$. The intuition is probably that "everything being connected with everything else sound pretty chaotic", but one can argue that the term "chaotic groupoid" exactly misses the true intrinsic nature of codiscrete groupoids: since these are all just "puffed up versions of the point" they are "maximally homogenous" things. Which space would be less chaotic than the point?

* For $X$ a finite set of cardinality $n$, the [[category algebra]] of $Codisc(X)$ is the algebra of $n\times n$-matrices. The contractibility of $Codisc(X)$ is reflected in the fact that this algebra is [[Morita equivalence|Morita equivalent]] to the ground field algebra, which is the [[category algebra]] of the [[point]].

  This maybe serves to illustrate: even though codiscrete groupoids are pretty trivial, they are not too trivial to be entirely without interest. Often it is useful to have big puffed-up versions of the point available.