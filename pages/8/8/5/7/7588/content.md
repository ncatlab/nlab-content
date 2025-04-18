
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

## Examples and Definitions

### Locale theory

In [[locale theory]], one studies the set of [[open subspaces]] (with the extra structure of a [[frame]]) as the fundamental notion. If $A$ is the frame, then the [[geometric theory]] is that of completely prime filters of $A$. It has a propositional symbol $\phi_a$ for each element of $A$, and axioms -

  - $\phi_a \vdash \phi_b$ (if $a \leq b$)

  - $\top \vdash \phi_1$

  - $\phi_a \wedge \phi_b \vdash \phi_{a\wedge b}$

  - $\phi_{\bigvee_i a_i} \vdash \bigvee_i \phi_{a_i}$

This simply makes a direct correspondence between the algebra of $A$ and the geometric logic. Of course it also corresponds to the finite intersections and arbitrary unions of open sets, which shows how geometric logic is matched to topology.

The classifying topos is the topos of sheaves over $A$.

The frame is a presentation-independent representation of the theory. It can be recovered from the theory as the Lindenbaum algebra of formulae modulo equivalence.

### Propositional geometric theories

A presentation of a frame by generators and relations corresponds more directly to a general propositional [[geometric theory]]. The generators are the signature (propositional symbols) and the relations can be straightforwardly converted to axioms.

### Formal topology

In [[formal topology]], one studies a set $B$ of *[[base for a topology|basic]]* open subspaces, with a _cover relation_ $a\triangleleft U$ between elements and subsets of $B$, to show when one basic open is covered by a family of others. There are various flavours of this. $\triangleleft$ may be the full cover relation or a generating part, and there may sometime be included the extra structure of a [[positivity predicate|positivity]]. In each case the formal topology has the structure of a [[posite]] and so gives rise to a geometric theory of flat continuous functors. Its propositional  symbols are $\phi_a$ for each $a\in B$. The axioms are -

  - $\top \vdash \bigvee_{a\in B} \phi_a$

  - $\phi_a \wedge \phi_b \vdash \bigvee\{\phi_c\mid c\triangleleft\{a\} \wedge c\triangleleft\{b\}\}$

  - $\phi_a \vdash \bigvee_{b\in U}\phi_{b}$ (if $a\triangleleft U$)

The models are known as _formal points_.

### General definition

It is probably impossible to give a real definition of "a notion of point-free topology".  However, one way to capture the notion of "point-free-ness" is by a version of [[well-pointed category|well-pointedness]].

Specifically, suppose that one defines a [[category]] (or $(\infty,1)$-[[(infinity,1)-category|category]]) $S$, whose [[objects]] one thinks of as [[spaces]], and that one intends $Hom(X,Y)$ to be the [[set]] (or $\infty$-[[infinity-groupoid|groupoid]]) of *all* continuous maps from $X$ to $Y$ (whereas $Ob(S)$ need not be the class of all spaces).  Also suppose that $S$ has a [[terminal object]] $pt$, which one interprets as the [[point]].  Then we may call this a __pointwise__ formulation of topology if $pt$ is a [[generator]] in $S$, and __pointless__ if this is not provable (or, for a stronger variation, provably false).

## Pointwise reasoning

The traditional way of doing topology using points may be called __pointwise topology__. Obviously that is natural in point-set topology, but for point-free there is an apparent problem: there may not be enough points to support, semantically, all the syntactic distinctions between formulae in the geometric logic. In other words, geometric logic is not necessarily complete.

It is possible to circumvent this by reasoning in an entirely _pointless_ style, without reference to the points.
For instance with locales, the maps are defined to be the frame homomorphisms, backwards.

Surprisingly, however, it is also possible to reason pointwise: a map from $X$ to $Y$ can be defined by saying how points of $X$ transform to points of $Y$. What makes this work is that there are enough points (models of the geometric theory) if you allow for those that live outside your favourite category of sets. In essence, if the construction is defined for the generic point of $X$ in the topos of sheaves over $X$, then the universal property of classifying toposes gives a point-free map (geometric morphism). The catch is that, to allow the construction to be transported from one topos to another, it has to be _geometric_ - preserved by inverse image functors. Thus continuity becomes a logical issue, of geometricity.

Further details and references are in Vickers [2007](#Vickers07) and [2014](#Vickers14).


## Bundles

A decisive advantage of point-free topology is that it gives a fibrewise topology of **bundles**, understood broadly as maps into a base space. (Note - for generalized spaces, i.e. toposes, bundles must be understood as _bounded_ geometric morphisms.)

It is shown in [Joyal, Tierney](#JoyalTierney84) that, for any elementary topos $\mathcal{E}$, there is an equivalence between localic bundles over $\mathcal{E}$ (i.e. localic geometric morphisms into it) and internal _point-free spaces_ in $\mathcal{E}$. The result does not work point-set.

Joyal and Tierney proved their result for internal frames. However, in some ways it works better for presentations of frames by generators and relations, if there is some geometric theory $\mathbb{T}_0$ of which the systems of generators and relations are models. This is not the case for frames - the frame structure is not geometric.  [Vickers 2007](#Vickers07) works it out for the general case of "GRD-systems", systems of generators, relations and "disjuncts".
Each model $P$ of the geometric theory $\mathbb{T}_0$ itself presents another geometric theory (for its point-free space), and this can be used to make a theory $\mathbb{T}_1$, extending $\mathbb{T}_0$, that classifies "pointed" presentations.
There is a forgetful map (forget the point) $p\colon \mathcal{S}[\mathbb{T}_1] \to \mathcal{S}[\mathbb{T}_0]$ between the classifying toposes.
Then a presentation in $\mathcal{E}$ is a map $P\colon\mathcal{E}\to\mathcal{S}[\mathbb{T}_0]$, and the localic bundle constructed by Joyal and Tierney is a bipullback of $p$ along $P$.

What this account reveals is that the bundle is - using $P$ - a continuous space-valued map on $\mathcal{E}$. For each point $x$ of $\mathcal{E}$, the fibre is $P(x)$ - because fibres are just pullbacks.

## Set of points

Depending on the foundational setting, a point-free space may or may not have a set of points, a discrete coreflection. This can be done in topos theory, but relies on an impredicative use of power_sets_. (Formal topology arose out of a desire to work predicatively.)

However, even when it exists, the set of points does not generally represent the space well.

This is best understood in terms of bundles over $X$. The "set of points" of a bundle $p\colon Y\to X$ is a sheaf over $X$, hence a local homeomorphism $q\colon Z\to X$. As a discrete coreflection it must also have a bundle map $f$ from $q$ to $p$. However, local homeomorphisms have an _opfibrational_ property that limits their ability to approximate general bundles. Suppose $x \sqsubseteq x'$ are two points of $X$ that are related by the specialization order. Then there is a corresponding fibre map $q^{-1}(x) \to q^{-1}(x')$.

As an example, take $X$ to be the Sierpinski space $\mathbb{S}$. Its points are subsets of a singleton $\{\ast\}$ and include $\bot=\emptyset\sqsubseteq\top=\{\ast\}$.
Its sheaves are functions - the fibre maps $Z_{\bot}\to Z_{\top}$.

Now consider the bundle $p\colon 1\to\mathbb{S}$ that picks out the closed point $\bot$. Its fibres over $\bot$ and $\top$ are singleton and empty. Let $q\colon Z \to \mathbb{S}$ be its discrete coreflection. Because there is a bundle map from $q$ to $p$, the fibre $Z_\top$ must be empty. But then because $q$ is a local homeomorphism, $Z_\bot$ must also be empty. $Z$, the "set of points" of $p$, is the empty space over $\mathbb{S}$.

We see that a non-trivial space can have have an empty set of points for purely topological reasons, nothing to do with logic or a pathological nature of point-free spaces.


## Applications

* [[Banach-Tarski paradox]]

## Related concepts

* [[localic homotopy theory]]


## References

An introduction:

* {#Johnstone83} [[Peter Johnstone]]: _The point of pointless topology_; Bull. Amer. Math. Soc. (N.S.) **8** 1 (1983) 41-53 &lbrack;[ams:1983-08-01/S0273-0979-1983-15080-2](http://www.ams.org/bull/1983-08-01/S0273-0979-1983-15080-2/home.html)[euclid:bams/1183550014](http://projecteuclid.org/euclid.bams/1183550014)&rbrack;
  > (advertised as the "trailer" for [Johnstone 1982](#Johnstone82))

Monographs:

* {#Johnstone82} [[Peter Johnstone]]: _[[Stone Spaces]]_, Cambridge Studies in Advanced Mathematics __3__, Cambridge University Press (1982, 1986) &lbrack;[ISBN:9780521337793](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/stone-spaces?format=PB&isbn=9780521337793)&rbrack;

* {#PicadoPultr12} [[Jorge Picado]], [[Aleš Pultr]]: _[[Frames and Locales]]_, Frontiers in Mathematics, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-0154-6](https://doi.org/10.1007/978-3-0348-0154-6)&rbrack;


A [[constructive mathematics|constructive]] treatment:

* {#JoyalTierney84}[[Andre Joyal|Andr&eacute; Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_, Memoirs of the American Mathematical Society **51** (1984), no. 309

For [[formal topology]], see

*  [[Giovanni Sambin]] (2001); _Some points in formal topology_; [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf).

* {#Palmgren05} [[Erik Palmgren]], _From Intuitionistic to Point-Free Topology: On the Foundation of Homotopy Theory_, Logicism, Intuitionism, and Formalism Volume 341 of the series Synthese Library pp 237-253, 2005 ([pdf](http://www2.math.uu.se/~palmgren/homotopy_rev2.pdf))

The pointwise reasoning is explained in the next references (though it was surely understood before them):

* {#Vickers04} [[Steve Vickers]], _The double powerlocale and exponentiation: a case study in geometric logic_, Theory and Applications of Categories **12** (2004) pp. 372-422 ([pdf](http://www.tac.mta.ca/tac/volumes/12/13/12-13.pdf))

* {#Vickers07} [[Steve Vickers]], _Locales and toposes as spaces_, Chapter 8 in _Handbook of Spatial Logics_ (ed. Aiello, Pratt-Hartman, van Bentham), Springer, 2007, pp. 429-496. 

* {#Vickers14} [[Steve Vickers]], _Continuity and geometric logic_, Journal of Applied Logic **12 (1)** (2014), pages 14-27 ([pdf](http://www.cs.bham.ac.uk/~sjv/GeoAspects.pdf))

* [[Steven Vickers]], *Generalized point-free spaces, pointwise* &lbrack;[arXiv:2206.01113](https://arxiv.org/abs/2206.01113)&rbrack;

[[!redirects pointless topology]]

[[!redirects pointwise topology]]
[[!redirects point-wise topology]]

[[!redirects pointfree topology]]
[[!redirects point-free topology]]