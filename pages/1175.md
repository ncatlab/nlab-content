
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _von Neumann algebra_ or _$W^*$-algebra_ is an important and special kind of [[operator algebra]], relevant in particular to [[measure theory]] and [[quantum mechanics]]/[[quantum field theory]] in its algebraic formulation as [[AQFT]]. Specifically, (non-commutative) von Neumann algebras can be understood as the [[Isbell duality|formal duals]] of ([[non-commutative geometry|non-commutative]]) [[localizable measurable spaces]] (or [[measurable locales]]); see the section _[Relation to measurable spaces](#RelationToMeasureSpaces)_ below.  


## History and terminology

Since terminology varies in the literature, we will say something about this first.  There are no precise definitions here; see below for those.

(Of course, _$W^*$-algebras_ should not be confused with _[[W-algebras]]_ in (logarithmic) [[conformal field theory]].)

[[John von Neumann]] originally studied certain [[operator algebras]] (back then they were called _[[rings]] of [[linear operator|operators]]_), defined as unital $*$-subalgebras of the algebra $B(H)$ of [[bounded operators]] on some [[Hilbert space]] $H$ that are [[closed subspace|closed]] in any of the several [[operator topology|operator topologies]] on $B(H)$ (except for the norm topology, which
gives $C^*$-[[C-star-algebra|algebras]]); the ultraweak topology is most convenient for our purposes.

One disadvantage of such a definition is that it makes it difficult to separate properties of von Neumann algebras from properties of their [[representations]] on Hilbert spaces.  For example, all faithful representations induce the same ultraweak topology on a von Neumann algebra, but different representations induce different weak topologies.  Furthermore, not all von Neumann algebras come automatically
equipped with a representation on a Hilbert space, such as the [[coproduct]] of two von Neumann algebras (although such a representation can always be constructed).  Finally, this definition unnecessarily confuses two very distinct notions: algebras and [[modules]] (or representations).

Therefore, we may use the modern abstract terminology in which a von Neumann algebra is defined as an [[associative algebra|algebra]] with certain [[extra structure|structures]] and [[extra property|properties]].  It then becomes a theorem that every von Neumann algebra has a free representation on a Hilbert space (such as Haagerup\'s standard form), so we may study von Neumann algebras in the historical concrete sense if we wish; but now we think of these as particular *representations* of algebras.

In the old terminology, morphisms of representations
of von Neumann algebras (von Neumann algebras in the historical concrete sense) are sometimes called _spatial morphisms of von Neumann algebras_ (as opposed to the _abstract morphisms_ that we will define below).  Similarly, the concrete von Neumann algebras themselves are sometimes called _von Neumann algebras_, whereas the abstract von Neumann algebras are called _$W^*$-algebras_.  Compare the historic definitions of $C^*$-algebras, as well as other examples of [[concrete and abstract structures]] such as [[manifolds]].

The [[nPOV]] dictates that a clear distinction between
the categories of algebras and modules must be maintained,
in particular, modules should not be confused with algebras.
Hence we stick to the modern terminology, which also seems
to be preferred in new papers on von Neumann algebras,
see for example [arXiv:1110.5671v1](http://arxiv.org/abs/1110.5671).


## Definitions

For completeness, we give both the modern abstract and historical concrete definitions.


### Abstract von Neumann algebras {#abstractdefn}

We build on the concepts of [[Banach space]] and (abstract) $C^*$-[[C-star-algebra|algebra]].  In this definition, a Banach space is a [[complex number|complex]] Banach space and a [[morphism]] of Banach spaces is a [[short linear map]] (a complex-linear map of norm at most $1$); a $C^*$-algebra is a complex unital $C^*$-algebra, and a morphism of $C^*$-algebras is a unital $*$-homomorphism (which is necessarily also a short linear map).  Note in particular that an [[isomorphism]] of either must be an [[isometry]].

Given a Banach space $A$, a __[[predual]]__ of $A$ is a Banach space $V$ whose [[dual Banach space]] $V^*$ is isomorphic to $A$:
$$ V^* \overset{i}\to A $$
(or more properly, equipped with such an isomorphism $i$).  Similarly, given a morphism $f\colon A \to B$ (properly, with $A$ and $B$ so equipped), a __predual__ of $f$ is a morphism $t\colon W \to V$ whose dual is isomorphic to $f$:
$$ \array {
   V^*                      & \overset{i}\to  & A \\
   \mathllap{t^*}\downarrow &                 & \downarrow\mathrlap{f} \\
   W^*                      & \underset{j}\to & B
} .$$

With these preliminaries, a __$W^*$-algebra__ or ("abstract") *von Neumann algebra* is a $C^*$-algebra that admits a predual (or more properly, equipped with one), and a $W^*$-[[homomorphism]] is a $C^*$-homomorphism that admits a predual.  In this way, the [[category]] of $W^*$-algebras becomes a [[subcategory]] of the category of $C^*$-algebras.

It is a theorem (see [below](#preduals)) that the predual of a $W^*$-algebra or $W^*$-homomorphism is essentially unique; we speak of [[generalized the|the]] predual of $A$, write it $A_*$, and identify $A$ with $(A_*)^*$ (and similarly for morphisms).  (So in fact we don\'t need the word 'equipped'; being a $W^*$-algebra is an [[extra property]], not an [[extra structure]], on a $C^*$-algebra.)

### Concrete von Neumann algebras 

Fix a [[complex number|complex]] [[Hilbert space]] $H$ and consider the [[associative algebra|algebra]] $B(H)$ of [[bounded operators]] on $H$.  A ("concrete") __von Neumann algebra__ on $H$ is a unital $*$-subalgebra of $B(H)$ that is [[closed subspace|closed]] in the [[weak operator topology]], or equivalently in the [[ultraweak topology]] or in the [[strong topology]].  As such is automatically [[closed subspace|closed]] in the [[norm topology]], the von Neumann algebras form a (particularly nice) class of concrete $C^*$-[[C-star-algebra|algebras]] on $H$, where the latter are defined as unital $*$-subalgebras of $B(H)$ closed under the norm topology.

We equip a von Neumann algebra with the topology induced by its inclusion into $B(H)$ equipped with the ultraweak topology.  An __abstract morphism__ of von Neumann algebras can then be defined as a unital $*$-homomorphism that is continous in the ultraweak topology.  Here we are disregarding the data of the inclusion of a von Neumann algebra into $B(H)$ and treating it as an algebra on its own.

Alternatively, we can define a von Neumann algebra $A$
as a unital $*$-algebra that admits an injective morphism into $B(H)$ for some Hilbert space $H$ such that the image of the inclusion is closed in the ultraweak topology on $B(H)$.  One can then prove that the topology induced on $A$ by the ultraweak topology on $B(H)$ does not depend on the choice of $H$ or the particular inclusion of $A$ into $B(H)$.  Hence one can define an abstract morphism of von Neumann algebras as a unital morphism of $*$-algebras that is continuous in the ultraweak topology.

It is a theorem that the category of (concrete) von Neumann algebras and abstract morphisms is [[equivalence of categories|equivalent]] to the category of (abstract) $W^*$-algebras and $W^*$-homomorphisms.  Similarly, we get the category of [[representations]] of $W^*$-algebras on Hilbert spaces using instead the __spatial morphisms__ of concrete von Neumann algebras.


## Sakai's theorem and properties of preduals
   {#preduals}

Sakai's theorem states that preduals considered in the abstract definition
are necessarily unique.
More precisely, given a von Neumann algebra $A$
we consider the category whose objects are pairs $(V,f)$,
where $V$ is a Banach space and $f\colon V^*\to A$ is an isomorphism
of Banach spaces.  A morphism from $(V,f)$ to $(W,g)$
is a morphism $h\colon V\to W$ of Banach spaces
such that $f h^* = g$.

Sakai's theorem then states that in the above category
there is exactly one morphism
between any pair of objects, which is necessarily an isomorphism.
In particular, the category of preduals is canonically isomorphic
to the [[terminal category]].

Sakai's theorem can be extended to morphisms of von Neumann algebras.
Thus preduals of von Neumann algebras and their morphisms
are unique up to a unique isomorphism, in particular we can talk
about [[generalized the|the]] predual of a von Neumann algebra and [[generalized the|the]] predual
of a morphism of von Neumann algebras.

The weak topology induced on a von Neumann algebra by its predual
is called the **ultraweak topology**.
The role of the ultraweak topology for von Neumann algebras
is analogous to the role of the norm topology for C\*-algebras.
In particular, morphisms of von Neumann algebras are precisely
those morphisms of C\*-algebras that are continuous
in the ultraweak topology.

Consider the [[dual vector space|dual space]] $V$ of a von Neumann algebra $A$ equipped
with the ultraweak topology.
The [[topological vector space]] $V$ canonically embeds
into the dual of $A$ as a Banach space, the embedding map being
induced by the canonical continuous map from $A$
equipped with the norm topology to $A$
equipped with the ultraweak topology.
Thus $V$ is also a Banach space.
There is a canonical morphism of Banach spaces from $A$ to $V^*$
given by evaluating an element of $V$ on the given element of $A$.
This morphism is in fact an isomorphism, hence $V$ is the predual of $A$.
In other words, the predual of a von Neumann algebra is canonically
isomorphic to its dual in the ultraweak topology.
Similarly, the predual of a morphism of von Neumann algebras
is canonically isomorphic to its dual in the ultraweak topology.


## Elementary examples

The easiest example of a von Neumann algebra is given by the $C^*$-algebra $B(H)$
of bounded operators on a complex [[Hilbert space]] $H$.
The predual can be canonically identified with the Banach space
of [[trace class operator|trace class operators]].

Any $C^*$-subalgebra of $B(H)$ closed in the ultraweak topology
is again a von Neumann algebra. 

Another example is $L^\infty(X)$ under pointwise almost everywhere multiplication, where $X$ is a σ-finite [[measure space]] or a [[localizable measurable space]]. These are (up to isomorphism) all of the _commutative_ von Neumann algebras, according to a specialized version of the [[Gelfand duality theorem]].

A faithful representation (in fact, the standard from) of $L^\infty(X) \hookrightarrow B(L^2(X))$ is given by considering $L^2(X)$ as an $L^\infty(X)$-module given by pointwise almost everywhere multiplication. 


## Properties of morphisms of von Neumann algebras


## The category of von Neumann algebras

The category of von Neumann algebras is a [[locally presentable category]].

The [[forgetful functor]] from von Neumann algebras
to [[sets]] that sends a von Neumann algebra
to its [[unit ball]] is a [[right adjoint functor]].
In fact, it is a [[monadic functor]] and preserves all [[sifted colimits]].

Thus, [[limits]] and [[sifted colimits]] of von Neumann algebras can be computed
on the level of underlying unit balls.

Small [[coproducts]] of von Neumann algebras exist.
There is also a “reduced” version of small [[coproducts]],
known as [[free products]],
which can be defined in a manner analogous to the [[spatial tensor product]].

## Monoidal structures

There are two different [[tensor products]] one can define on von Neumann algebras.

First, one can use the usual universal property of tensor products
and postulate that morphisms $A\otimes B\to M$
are in a natural bijection with pairs of morphisms
$A\to M$ and $B\to M$ whose images commute in $M$.
This yields a [[symmetric monoidal structure]] on von Neumann algebras.
This monoidal structure is not [[closed]].

Secondly, one can also define a “reduced” version, known as the _spatial tensor product_.
Given two von Neumann algebras $A$ and $B$, their spatial tensor product
is the von Neumann algebra generated by $A\otimes 1$ and $1\otimes B$
in the von Neumann algebra $B(L^2 A\otimes L^2 B)$,
where $L^2 A$ and $L^2 B$ are the Haagerup standard form of $A$ and $B$ respectively.
This also results in a [[symmetric monoidal structure]].
Furthermore, passing to the [[opposite category]]
yields a [[closed monoidal structure]].

## $W^*$-categories


## Modules over von Neumann algebras


## Bimodules over von Neumann algebras and Connes fusion


## Modular algebra and Tomita--Takesaki theory

* [[modular theory]]


## Gelfand duality for commutative von Neumann algebras

See the article [[commutative von Neumann algebra]].

## Relevance

The [[Gelfand duality theorem]] states that there is a contravariant [[equivalence of categories|equivalence]] between the [[category]] of commutative von Neumann algebras and the category of compact strictly localizable enhanced [[measurable space|measurable spaces]]; that is, the [[opposite category]] of one is equivalent to the other. See [Relation to Measurable Spaces](#RelationToMeasureSpaces) below. General von Neumann algebras are seen then as a 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]].

The importance of von Neumann algebras for ([[higher category theory|higher]]) [[category theory]] and topology lays in the evidence that von Neumann algebras are deeply connected with the low dimensional [[quantum field theory]] (2d [[CFT]], [[TQFT]] in low dimensions, inclusions of [[von Neumann algebra factor|factor]]s, [[quantum group]]s and [[knot theory]]; [[elliptic cohomology]]: works of Wenzl, Vaughan Jones, Anthony Wasserman, Kerler, Kawahigashi, Ocneanu, Szlachanyi etc.). 

The highlights of their structure theory include the results on classification of [[von Neumann algebra factor|factors]] ([[Alain Connes]], 1970s) and theory of inclusions of subfactors (V. Jones). (Hilbert) [[bimodule]]s over von Neumann algebras have a remarkable tensor product due Connes ([[Connes fusion]]). Following Segal's manifesto

* Graeme Segal, _Elliptic cohomology (after Landweber-Stong, Ochanine, Witten, and others)_. S&#233;minaire Bourbaki, Vol. 1987/88.  Ast&#233;risque  No. 161-162  (1988), Exp. No. 695, 4, 187--201 (1989).

and its update

* [[Graeme Segal]], _What is an elliptic object?_  Elliptic cohomology,  306--317, London Math. Soc. Lecture Note Ser., 342, Cambridge Univ. Press, Cambridge, 2007. 

on hypothetical connections between [[CFT]] and [[elliptic cohomology]], Stolz and Teichner have made a case for a role von Neumann algebras seem to play in a partial realization of that program:

* [[Stefan Stolz]] and [[Peter Teichner]], _What is an elliptic object?_ ([pdf](http://math.berkeley.edu/~teichner/Papers/Oxford.pdf))

See also the [Wikipedia entry](http://en.wikipedia.org/wiki/Von_Neumann_algebra) entry for more on von Neumann algebras and a list of references and links.


## General

The _[[bicommutant theorem]]_ (as known as the _double commutant theorem_ , or _von Neumann's double commutant theorem_ ) is the following result. 

Let $A \subseteq B(H)$ be a sub-[[star-algebra]] of the [[C-star algebra]] of [[bounded linear operator|bounded linear operators]] on a [[Hilbert space]] $H$. Then $A$ is a [[von Neumann algebra]] on $H$ if and only if $A = A''$, where $A'$ denotes the [[commutant]] of $A$. 

Notice that the condition of $A$ being a von Neumann algebra (being closed in the [[weak operator topology]]; "weak" here can be replaced by "strong", "ultrastrong", or "ultraweak" as described in [[operator topology]]), which is a [[topology|topological]] condition, is by this result equivalent to an algebraic condition (being equal to its bicommutant).  


## Relation to measurable spaces
 {#RelationToMeasureSpaces}

The [[Gelfand-Naimark theorem|Gel'fand–Naimark theorem]] states that the category of [[localizable measurable spaces]] is contravariantly [[equivalence of categories|equivalent]] to (that is equivalent to the [[opposite category|opposite]] of) the category of commutative von Neumann algebras.  As such, arbitrary von Neumann algebras may be interpreted as 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]]. See at _[[noncommutative probability space]]_.


## Topics of interest for the understanding of AQFT

This paragraph will collect some facts of interest for the aspects of [[AQFT]].

In this paragraph $\mathcal{M}$ will always be a von Neumann algebra acting on a [[Hilbert space]] $\mathcal{H}$ with [[commutant]] $\mathcal{M}'$.


### Vectors

+-- {: .un_defn}
###### Definition

A [[vector]] $x \in \mathcal{H}$ is a **[[cyclic vector]]** if $\mathcal{M}x$ is dense in $\mathcal{H}$.

=--

+-- {: .un_defn}
###### Definition

A [[vector]] $x \in \mathcal{H}$ is a **[[separating vector]]** if $M(x) = 0$ implies $M = 0$ for all $M \in \mathcal{M}$.

=--


+-- {: .un_theorem}
###### Theorem

The notions of cyclic and separating are dual with respect to the commutant, that is a vector is cyclic for $\mathcal{M}$ iff it is separating for $\mathcal{M}'$.

=--


### Projections in von Neumann algebras

One crucial feature of von Neumann algebras is that they contain 
"every projection one could wish for": there are three points that make this statement precise:

* the linear combinations of projections are norm dense in a von Neumann algebra

* [[Gleason's theorem]]

* Murray--von Neumann classification of [[von Neumann algebra factor|factors]] 


#### Projections are norm dense

First let us note that every element $A$ of a von Neumann algebra can trivially be written as a linear combination of two selfadjoint elements:
$$
A = \frac{1}{2} (A + A^*) + i\frac{1}{2i} (A - A^*)
$$

Then, by the [[spectral theorem]] every selfadjoint element A is represented by it's spectral measure E via
$$
A = \integral_{-\|A\|}^{\|A\|} \lambda E(d\lambda)
$$
The integral converges in norm to A and all spectral projections are elements of the von Neumann algebra. It immediatly follows that the set of finite sums of multiples of projections is norm dense in every von Neumann algebra. 


#### Gleason's theorem {#GleasonsTheorem}

See [[Gleason's theorem]].


#### Murray--von Neumann classification of factors 
To be done...


### Miscellaneous

* [[split inclusion of von Neumann algebras]]


## Related concepts

* [[enveloping von Neumann algebra]]

* [[von Neumann algebra factor]]


## References
 {#References}

* [[Jacob Lurie]], _von Neumann algebras_, lecture series (2011) ([web](http://www.math.harvard.edu/~lurie/261y.html))
* Abraham Westerbaan, _The Category of von Neumann Algebras_, [1804.02203](https://arxiv.org/abs/1804.02203) 2018



[[!redirects W*-algebra]]
[[!redirects W*-algebras]]
[[!redirects W* algebra]]
[[!redirects W* algebras]]
[[!redirects W-star-algebra]]
[[!redirects W-star-algebras]]
[[!redirects W-star algebra]]
[[!redirects W-star algebras]]
[[!redirects von Neumann algebra]]
[[!redirects von Neumann algebras]]
[[!redirects von Neumann-algebra]]
[[!redirects von Neumann-algebras]]
[[!redirects category of von Neumann algebras]]
[[!redirects categories of von Neumann algebras]]
