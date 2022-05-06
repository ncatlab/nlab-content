
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

__Point-free topology__ refers to various formulations of [[topology]] that are not based on the notion of [[topological space]] as a [[set]] of [[points]] equipped with [[extra structure]].  What they generally have in common is that instead the points are described as [[models]] of a [[geometric theory]]. This change has some important consequences.

First, it conveniently describes the points not only in one's favourite [[category of sets]], but also in arbitrary [[Grothendieck topos|Grothendieck toposes]].

Second, it opens up the possibility of using predicate geometric theories, to obtain generalized spaces (the [[classifying toposes]]) in the sense of Grothendieck.
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

  - $\top \vdash \bigvee_{a\in B} \phi_a$

  - $\phi_a \wedge \phi_b \vdash \bigvee\{\phi_c\mid c\triangleleft\{a\} \wedge c\triangleleft\{b\}\}$

  - $\phi_a \vdash \bigvee_{b\in U}\phi_{b}$ (if $a\triangleleft U$)

The models are known as _formal points_.

## Pointwise reasoning

The traditional way of doing topology using points may be called __pointwise topology__. Obviously that is natural in point-set topology, but for point-free there is an apparent problem: there may not be enough points to support, semantically, all the syntactic distinctions between formulae in the geometric logic. In other words, geometric logic is not necessarily complete.

It is possible to circumvent this by reasoning in an entirely _pointless_ style, without reference to the points.
For instance with locales, the maps are defined to be the frame homomorphisms, backwards.

Surprisingly, however, it is also possible to reason pointwise: a map from $X$ to $Y$ can be defined by saying how points of $X$ transform to points of $Y$. What makes this work is that there are enough points (models of the geometric theory) if you allow for those that live outside your favourite category of sets. In essence, if the construction is defined for the generic point of $X$ in the topos of sheaves over $X$, then the universal property of classifying toposes gives a point-free map (geometric morphism). The catch is that, to allow the construction to be transported from one topos to another, it has to be _geometric_ - preserved by inverse image functors. Thus continuity becomes a logical issue, of geometricity.

Further details and references are in Vickers [2007](#Vickers07) and [2014](#Vickers14).


## Bundles

A decisive advantage of point-free topology is that it gives a fibrewise topology of **bundles**, understood broadly as maps into a base space. (Note - for generalized spaces, i.e. toposes, bundles must be understood as _bounded_ geometric morphisms.)

It is shown in [Joyal, Tierney](#JoyalTierney84) that, for any elementary topos $\mathcal{E}$, there is an equivalence between localic bundles over $\mathcal{E}$ (i.e. localic geometric morphisms into it) and internal _point-free spaces_ in $\mathcal{E}$. The result does not work point-set.


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

For a constructive treatment more appropriate to the ideas on this page see

* {#JoyalTierney84}[[Andre Joyal|Andr&eacute; Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_, Memoirs of the American Mathematical Society **51** (1984), no. 309

For [[formal topology]], see

*  [[Giovanni Sambin]] (2001); _Some points in formal topology_; [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf).

* {#Palmgren05} [[Erik Palmgren]], _From Intuitionistic to Point-Free Topology: On the Foundation of Homotopy Theory_, Logicism, Intuitionism, and Formalism Volume 341 of the series Synthese Library pp 237-253, 2005 ([pdf](http://www2.math.uu.se/~palmgren/homotopy_rev2.pdf))

The pointwise reasoning is explained in the next references, though it was surely understood before them.

* {#Vickers04}[[Steve Vickers]], _The double powerlocale and exponentiation: a case study in geometric logic_, Theory and Applications of Categories **12** (2004) pp. 372-422 ([pdf](http://www.tac.mta.ca/tac/volumes/12/13/12-13.pdf))

* {#Vickers07}[[Steve Vickers]], _Locales and toposes as spaces_, Chapter 8 in _Handbook of Spatial Logics_ (ed. Aiello, Pratt-Hartman, van Bentham), Springer, 2007, pp. 429-496. 

* {#Vickers14}[[Steve Vickers]], _Continuity and geometric logic_, Journal of Applied Logic **12 (1)** (2014), pages 14-27 ([pdf](http://www.cs.bham.ac.uk/~sjv/GeoAspects.pdf))



[[!redirects pointless topology]]

[[!redirects pointwise topology]]
[[!redirects point-wise topology]]


[[!redirects pointfree topology]]
[[!redirects point-free topology]]

[[!redirects pointless topology]]