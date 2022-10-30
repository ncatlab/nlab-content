
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

In fact, there are two notions of generalized Reedy category in the literature, one due to Cisinski and one to Berger--Moerdijk.  They share many properties and examples.

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

This appears as ([Berger-Moerdijk, def. 1.1](#BergerMoerdijk)).

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
there is a morphism $\alpha : a \to a'$ in $A_-$ and a cell $u \in $

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

The morphism $f : X \to Y$ is called **normal** if every cell of $Y$ not in the [[image]] of $f$ is dominant.

=--

This is ([Cisinski, 8.1.30](#Cisinski)).

+-- {: .num_example}
###### Example

Every [[monomorphism]] between normal presheaves is normal.

=--


+-- {: .num_prop}
###### Proposition

The class of normal monomorphisms in $PSh(A)$ is closed under

* [[retracts]];

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

(...) ([Berger-Moerdijk, section 2](#BergerMoerdijk))

## References


Cisinski's notion of generalized Reedy category appears as def 8.1.1 in

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie|Les préfaisceaux comme modèles des types d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski}


The Berger-Moerdijk definition of generalized Reedy category appears in 

* [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_ (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 {#BergerMoerdijk}


[[!redirects generalized Reedy categories]]
[[!redirects Berger-Moerdijk generalized Reedy category]]
[[!redirects Berger-Moerdijk generalized Reedy categories]]
[[!redirects Cisinski generalized Reedy category]]
[[!redirects Cisinski generalized Reedy categories]]
