
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[Reedy category]]_, though useful, is in some contexts inconveniently restrictive, since no Reedy category can contain any nonidentity [[isomorphisms]].  This is problematic for many "[[geometric shape for higher structures|shape]] categories" such as Connes' [[category of cycles]] $\Lambda$, [[Segal's category Gamma|Segal's category]] $\Gamma$, the [[tree category]] $\Omega$, and so on.  The notion of *generalized Reedy category* lifts this restriction, while maintaining the truth of the main theorem about Reedy categories: the existence of the [[Reedy model structure]].

In fact, there are two notions of generalized Reedy category in the literature. Cisinski's "cat&#233;gories squelletiques" (Ch. 8 in  [_PCMH_](#Cisinski)) provide a natural generalization of the [[simplex category]], so that diagrams based on them behave much like [[simplicial objects]]. They were introduced primarily for the purposes of modeling [[homotopy types]]. The "generalized Reedy categories" of [Berger & Moerdijk 2011](#BergerMoerdijk11) are a strictly broader generalization suitable e.g. for describing [[dendroidal sets]]. They were introduced for the purposes of modelling more general classes of structure, particularly [[operads]].


## Definitions

### Generalized Reedy categories

+-- {: .num_defn #BMGeneralizedReedyCategory}
###### Definition

A **Berger-Moerdijk generalized Reedy category** is a [[category]] $R$ together with two [[wide subcategories]] $R_+$ and $R_-$, and a [[function]] $d\colon ob(R)\to \alpha$ called *degree*, for some [[ordinal]] $\alpha$, such that

1. every non-isomorphism in $R_+$ raises degree,

1. every non-isomorphism in $R_-$ lowers degree,

1. every isomorphism in $R$ preserves degree,

1. $R_+\cap R_-$ is the [[core]] of $R$ (equivalently, every isomorphism is in both $R_+$ and $R_-$, i.e. they are not just wide but [[pseudomonic functor|pseudomonic]] subcategories),

1. every morphism $f$ factors as a map in $R_-$ followed by a map in $R_+$, uniquely up to isomorphism, 

1. if $f\in R_-$ and $\theta$ is an isomorphism such that $\theta f = f$, then $\theta = 1$ (isomorphisms see the maps in $R_-$ as [[epimorphism|epis]]).

The last condition implies that the isomorphism in the penultimate condition must be unique.  It is not self-dual, but has an obvious dual version.  A BM generalized Reedy category is said to be **dualizable** if it satisfies both this condition and its dual.


=--

+-- {: .num_defn }
###### Definition

A [[morphism]] of generalized Reedy category $S \to R$ is a [[functor]] whish takes $S_+$ to $R_+$, takes $S_-$ to $R_-$ and preserves the degree.

=--

This appears as ([Berger & Moerdijk 2011, def. 1.1](#BergerMoerdijk11)).

+-- {: .num_remark}
###### Remark

Generalized Reedy category structures (as opposed to ordinary structures!) can always be transported along [[equivalence of categories]].

=--


+-- {: .num_defn}
###### Definition

For a **Cisinski generalized Reedy category**, the final condition in 
def. \ref{BMGeneralizedReedyCategory} is replaced by

* every morphism in $R_-$ admits a [[section]], and two parallel morphisms in $R_-$ are equal precisely when they have the same sections.

=--

For clarity, in the context of generalized Reedy categories, an ordinary [[Reedy category]] may be called a *strict Reedy category*.

### Prima Facie comparison between Cisinski and Berger-Moerdijk.

The only difference between the Cisinski notion and the Berger-Moerdijk notion is in the final condition -- let's say, between the _Cisinski condition_ and the _Berger-Moerdijk condition_.

It's easy to see that the Cisinski condition is **strictly stronger** than the Berger-Moerdijk condition.  The Berger-Moerdijk condition asks that $R_-$ arrows be something less than epimorphic in $R$. By comparison, the Cisinski condition asks that $R_-$ arrows be _actually_ epimorphic in $R$, in fact that they be _split_ epimorphic, and more.


### Presheaves on Reedy categories. 

For $R$ a generalized Reedy category, and $X$ a [[presheaf]] on $R$, there are the evident analogue notions of $n$-cells in $X$, degenerate $n$-cells, faces, boundaries, horns, etc.

(..)

## Properties

### Normal monomorphisms (Cisinski)
 {#NormalMorphisms}


Let $A$ be a Cisinski generalized Reedy category. 

+-- {: .num_defn}
###### Definition

An object $a \in A$ is called _degenerate_ precisely if there is a non-isomorphism out of $a$ in $A_-$. 

=--

See ([Cisinski, prop. 8.1.9](#Cisinski)).


+-- {: .num_prop}
###### Proposition

For every object $a \in A$ there exists a morphism $\pi : a \to b$ in $A_-$
with $b$ non-degenerate.

=--

This is ([Cisinski, prop. 8.1.13](#Cisisnki)).

Let $X$ be a [[presheaf]] over $A$. 

+-- {: .num_defn}
###### Definition

For $a \in A$,  a cell $v \in X(a)$ is called **degenerate** precisely if
there is a morphism $\alpha : a \to a'$ in $A_-$ and a cell $u \in X(a')$

$$
  X(\alpha) : u \mapsto v
$$

=--

See ([Cisinski, cor. 8.1.10](#Cisinski)).


Write $A/X$ for the [[category of elements]]
of $X$.



+-- {: .num_defn}
###### Definition

For $a \in A$ an $a$-cell $v \in X(a)$ is called **dominant** if $(a,v) \in A/X$ has trivial [[automorphism group]].

An $a$-cell $u \in X(a)$ is called **normal** if there is a morphism $\alpha : a \to b$ in $A_-$ with $b$ non-degenerate, and a dominant $b$-cell $v \in X(b)$, such that 
$$
  X(\alpha) : v \mapsto u
  \,.
$$

The presheaf $X$ is called **normal** if all its cells are normal.

=--

See ([Cisinski, 8.1.23](#Cisinski)).

+-- {: .num_remark}
###### Remark

A non-degenerate cell is normal precisely if it is dominant.

=--

+-- {: .num_prop}
###### Proposition

$X$ is normal precisely if all its non-degenerate cells are dominant.

=--

This is ([Cisinski, cor. 8.1.25](#Cisinski)).

Let $f : X \to Y$ be a morphism of [[presheaves]] over $A$.

+-- {: .num_defn}
###### Definition

The morphism $f : X \to Y$ is called **normal** if every cell of $Y$ not in the [[image]] of $f$ is normal.

=--

This is ([Cisinski, 8.1.30](#Cisinski)).

+-- {: .num_example}
###### Example

Every [[monomorphism]] between normal presheaves is normal.

=--


+-- {: .num_prop}
###### Proposition

The class of normal monomorphisms in $PSh(A)$ is closed under

* [[pushouts]];

* [[transfinite composition]];

* [[retracts]].

In fact, the class of normal monomorphisms is that generated under these operations from the boundary inclusions $I := \{\partial a \hookrightarrow a\}$.

=--

This is ([Cisinski, prop. 8.1.31, 8.1.35](#Cisinski)).


### Model category structure on presheaves

(...) [[generalized Reedy model structure]]

## Examples

### Berger-Moerdijk type

#### Specific examples

* Any [[Reedy category]] is a generalized Reedy category, in particular the [[simplex category]].

* Any (finite) [[groupoid]] $G$ is also a generalized Reedy category, with $G_+ = G_- = G$.

* Connes' [[category of cycles]] $\Lambda$.

* [[Segal's category Gamma|Segal's category]] $\Gamma$.

* The Moerdijk-Weiss [[tree category]] $\Omega$ is generalized Reedy. The degree is given by the number of vertices in a tree. 

  See also the discussion at _[[dendroidal set]]_ and _[[model structure on dendroidal sets]]_.

* Any generalized [[direct category]] or generalized [[inverse category]] is also a generalized Reedy category, in which either $R_-$ or $R_+$ consists only of the isomorphisms.

#### The class of crossed group sites

+-- {: .num_defn }
###### Definition

For $S$ a [[small category]], a **[[crossed group|crossed $S$-group]]** is a [[presheaf]] $G : S^{op} \to Set$ equipped with

1. for each object $s \in S$ a group structure on $G_s$;

1. for all $s, r\in S$ a left $G_r$-[[action]] on the [[hom-set]] $S(s,r)$ ;

such that for all morphisms $\alpha : s \to r$ and $\beta : t \to s$ in $S$ and $g,h \in G_r$ we have

1. $g_*( \alpha \circ \beta)  = g_*(\alpha) \circ \alpha^*(g)_* \beta$;

1. $g_* (id_r) = id_r$;

1. $\alpha^* (g \cdot h) = h_*(\alpha)^*(g)\cdot \alpha^*(h)$;

1. $\alpha^*(e_r) = e_s$;

where $g_*$, $h_*$ denotes the group action and $\alpha^* : G_r \to G_s$ the presheaf map. 

The **total category** $S G$ of an [[crossed group|crossed $S$-group]] $G$ is the category with the same objects as $S$, and with morphisms $r \to s$ being pairs $(\alpha, g) \in S(s,r)\times G_r$ and with composition defined by

$$
  (\alpha, g) \circ (\beta, h)
  = 
  (\alpha \cdot g_*(\beta), \beta^*(g) \cdot h)
  \,.
$$ 

=--

([BM11, def. 2.1](#BergerMoerdijk11)).

+-- {: .num_defn }
###### Definition

If $S$ is equipped with a generalized Reedy structure, then an [[crossed group|crossed $S$-group]] $G$ is called **compatible** with that generalized Reedy structure if 

1. the $G$-action respects $S^+$ and $S^-$;

1. if $\alpha : r \to s$ is in $S^-$ and $g \in G_s$ such that $\alpha^* (g) = e_r$ and $g_*(\alpha) = \alpha$, then $g = e_s$.

=--

+-- {: .num_example }
###### Example

The category $\Omega_{pl}$ of planar finite rooted [[trees]] is a strict [[Reedy category]]. The category $\Omega$ of non-planar finite rooted [[trees]] is the total category of an $\Omega_{pl}$-[[crossed group]] which to a planar tree $T$ assigns its group of non-planar automorphisms.

=--

+-- {: .num_prop }
###### Proposition

Let $S$ be a strict [[Reedy category]] and let $G$ be a compatible [[crossed group|crossed $S$-group]]. Then there exists a unique dualizabe generalized Reedy structure on $S G$ for which the embedding $S \hookrightarrow S G$ is a morphism of generalized Reedy categories.

=--

([BM11, prop. 2.10](#BergerMoerdijk11)).

## Related concepts

* A "more generalized" notion is a [[c-Reedy category]].
* A more specialized notion is an [[Eilenberg-Zilber category]].

## References


Cisinski's notion of generalized Reedy category appears as def 8.1.1 in

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie|Les préfaisceaux comme modèles des types d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski}


The Berger-Moerdijk definition of generalized Reedy category appears in 

* {#BergerMoerdijk11} [[Clemens Berger]], [[Ieke Moerdijk]], *On an extension of the notion of Reedy category*, Mathematische Zeitschrift **269** (2011) 977–1004 &lbrack;[arXiv:0809.3341](http://arxiv.org/abs/0809.3341), [doi:10.1007/s00209-010-0770-x](https://doi.org/10.1007/s00209-010-0770-x)&rbrack;
 


[[!redirects generalized Reedy categories]]
[[!redirects Berger-Moerdijk generalized Reedy category]]
[[!redirects Berger-Moerdijk generalized Reedy categories]]
[[!redirects Cisinski generalized Reedy category]]
[[!redirects Cisinski generalized Reedy categories]]
