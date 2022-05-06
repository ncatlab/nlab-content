
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

Let $X$ be a [[paracompact space|paracompact]] [[Hausdorff space]]. A [[sheaf]] $F$ of [[groups]] over $X$ is __fine__ if for every two disjoint closed subsets $A,B\subset X$, $A\cap B = \emptyset$, there is an [[endomorphism]] of the sheaf of groups $F\to F$ which restricts to the identity in a neighborhood of $A$ and to the $0$ endomorphism in a neighborhood of $B$. Every fine sheaf is [[soft sheaf|soft]].

A slightly different definition is given in Voisin, in _Hodge Theory and Complex Algebraic Geometry I_ (Definition 4.35):

A __fine sheaf__ $\mathcal{F}$ over $X$ is a sheaf of $\mathcal{A}$-modules, where $\mathcal{A}$ is a sheaf of rings such that, for every open cover $U_i$ of $X$, there is a partition of unity $1 = \sum f_i$ (where the sum is locally finite) subordinate to this covering.

Another definition is given by Godement
in _Topologie algébrique et théorie des faisceaux_
(the paragraph after Theorem II.3.7.2):
a sheaf $F$ is __fine__ if the internal hom $Hom(F,F)$ is a [[soft sheaf]].

## Related concepts

* [[sheaf]]

* [[abelian sheaf cohomology]]

  * [[soft sheaf]]

  * [[flabby sheaf]]

category: sheaf theory