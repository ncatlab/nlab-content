
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

__Point-free topology__ refers to various formulations of [[topology]] that are not based on the notion of [[topological space]] as a [[set]] of [[points]] equipped with [[extra structure]].  What they generally have in common is that instead the points are described as models of a [[geometric theory]]. This change has some important consequences.

First, it conveniently describes the points not only in one's favourite category of sets, but also in arbitrary [[Grothendieck topos|Grothendieck toposes]].

Second, it opens up the possibility of using predicate geometric theories, to obtain generalized spaces (the classifying toposes) in the sense of Grothendieck.
This article will mostly concern itself with the ungeneralized point-free spaces, corresponding to propositional geometric theories.

The phrase "point-free topology" is often taken as synonymous with _pointless topology_ [Johnstone 83](#Johnstone83). However, let us reserve "pointless" for approaches that avoid mentioning points and refer directly to the geometric theory presentation and structures deriving from it.

## Examples

* In [[locale theory]], one studies the set of [[open subspaces]] (with the extra structure of a [[frame]]) as the fundamental notion. If $A$ is the frame, then the geometric theory is that of completely prime filters of $A$. It has a propositional symbol $\phi_a$ for each element of $A$, and axioms -

  - $\phi_a \vdash \phi_b$ (if $a \leq b$)

  - $\top \vdash \phi_1$

  - $\phi_a \wedge \phi_b \vdash \phi_{a\wedge b}$

  - $\phi_{\bigvee_i a_i} \vdash \bigvee_i \phi_{a_i}$

This simply makes a direct correspondence between the algebra of $A$ and the geometric logic. Of course it also corresponds to the finite intersections and arbitrary unions of open sets, which shows how geometric logic is matched to topology.

The classifying topos is the topos of sheaves over $A$.

The frame is a presentation-independent representation of the theory. It can be recovered from the theory as the Lindenbaum algebra of formulae modulo equivalence.

* A presentation of a frame by generators and relations corresponds more directly to a general propositional geometric theory. The generators are the signature (propositional symbols) and the relations can be straightforwardly converted to axioms.

* In [[formal topology]], one studies a set $B$ of *[[base for a topology|basic]]* open subspaces, with a _cover relation_ $a\triangleleft U$ between elements and subsets of $B$, to show when one basic open is covered by a family of others. There are various flavours of this. $\triangleleft$ may be the full cover relation or a generating part, and there may sometime be included the extra structure of a [[positivity predicate|positivity]]. In each case the formal topology has the structure of a [[posite]] and so gives rise to a geometric theory of flat continuous functors. Its propositional  symbols are $\phi_a$ for each $a\in B$. The axioms are -

(To be continued)


In contrast, the traditional way of doing topology using points may be called __pointwise topology__.


## Definition

In the interest of considering whether a formulation of topology is pointless or not, I offer the following sociomathematical suggestion at a definition:

Working in a given [[logic|logical]] context $\mathcal{L}$, suppose that one defines a [[category]] (or $(\infty,1)$-[[(infinity,1)-category|category]]) $S$, whose [[objects]] one thinks of as [[spaces]] and whose [[morphisms]] one thinks of as [[continuous maps]].  Suppose further that one intends $Hom(X,Y)$ to be the [[set]] (or $\infty$-[[infinity-groupoid|groupoid]]) of *all* continuous maps from $X$ to $Y$ (whereas $Ob(S)$ need not be the class of all spaces).  Also suppose that $S$ has a [[terminal object]] $pt$, which one interprets as the [[point]].

+-- {: .num_defn}
###### Definition

The above is a __pointwise__ formulation of topology if it is [[proof|provable]] (in $\mathcal{L}$) that $pt$ is a [[generator]] in $S$ but __pointless__ if this is not provable.  (One could have stronger notions of pointlessness by asking that this be refutable; if using [[intuitionistic logic]], this could be further strengthened.)
=--

## Applications

* [[Banach-Tarski paradox]]

## Related concepts

* [[localic homotopy theory]]

## References

An introduction to [[locale theory]] is

* {#Johnstone83} [[Peter Johnstone]] (1983); _The point of pointless topology_; Bull. Amer. Math. Soc. (N.S.) Volume 8, Number 1, 41--53; [Euclid](http://projecteuclid.org/euclid.bams/1183550014).

This is, in its own words, to be read as the trailer for Johnstone's book _[[Stone Spaces]]_, which see.

For [[formal topology]], see

*  [[Giovanni Sambin]] (2001); _Some points in formal topology_; [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf).

* {#Palmgren05} [[Erik Palmgren]], _From Intuitionistic to Point-Free Topology: On the Foundation of Homotopy Theory_, Logicism, Intuitionism, and Formalism Volume 341 of the series Synthese Library pp 237-253, 2005 ([pdf](http://www2.math.uu.se/~palmgren/homotopy_rev2.pdf))

[[!redirects pointless topology]]

[[!redirects pointwise topology]]
[[!redirects point-wise topology]]


[[!redirects pointfree topology]]
[[!redirects point-free topology]]

[[!redirects pointless topology]]