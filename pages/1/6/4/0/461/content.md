
#Contents#
* table of contents
{:toc}

## Definition

The **empty set** $\emptyset$ is the [[set]] with no [[element]]s.

The empty set is unique in most membership-based [[foundations]], but in any case we can say 'the' empty set, since any two empty sets are isomorphic by a unique isomorphism (the [[generalized the]]). 

Indeed, in any foundations (whether membership-based or structural), the empty set is characterized by a [[universal property]]: it is the [[initial object]] in the  [[category]] [[Set]] of all sets: for every set $S$, there is a unique [[function]]

$$
  \emptyset \stackrel{\exists !}{\to} S
  \,.
$$



## Aspects of the empty set

The empty set can be confusing, because it is a degenerate case. Indeed, it is defined as an exception: every set is [[inhabited set|inhabited]], except the empty set. Nothing belongs to the empty set, but the empty set itself is something. Mathematics students are confused that there is a function from the empty set to itself, and even grown mathematicians will misstate definitions because they forget about the empty set.

In terms of the empty set one can give sense to the [[natural number object|natural number]] expression $0^0$, the [[exponentiation]] of [[zero]] with itself, by defining the [[cartesian closed category|exponential]] $m^n$ to be the [[cardinality]] of the [[hom-set]] $\hom_{Set}([m], [n])$ where $[m]$ is an $m$-element set. Then $0^0 = 1$ because $\emptyset$ is an [[initial object]]. 

* Remark: Endless debates (as seen for example at sci.math) about the meaning of $0^0$ are most easily resolved by paying attention to how exponentiation (in a [[ring]] or [[rig]] that admits [[exponentiation]]) is defined. We have just observed how $0^0 = 1$ makes good sense in the rig of natural numbers. But exponentiation for the [[real number]] field ($x^y$ for $x \gt 0$) is standardly defined by continuity considerations, and cannot be continuously extended to cover $0^0$. Of course, that has nothing to do with the empty set! 
