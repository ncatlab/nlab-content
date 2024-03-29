
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

Let $\mathcal{A}$ be an [[abelian category]] [[category with translation|with translation]]. 

An [[object]] $I$ in the [[category of chain complexes]] modulo [[chain homotopy]], $K(\mathcal{A})$,  is **homotopically injective** if for every $X \in K(\mathcal{A})$ that is
[[quasi-isomorphism|quasi-isomorphic]] to $0$
we have
$$
  Hom_{K(\mathcal{A})}(X,I) \simeq 0
  \,.
$$

Let 

$$
  QuasiIsoMono = \{f \in Mor(A_c) | f mono and quasiio\}
$$ 

be the set of morphisms in the [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ which are both [[quasi-isomorphism]]s as well as [[monomorphism]]s. 

Then

A [[complex]] $I$ is an [[injective object]] with respect to monomorphic quasi-isomorphisms precisely if

* it is homotopically injective in the sense of complexes in $\mathcal{A}$; and

* it is injective as an object of $\mathcal{A}$ (with respect to morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is exact).



## Properties

### In complexes in a Grothendieck category 

**Proposition** 
For $\mathcal{A}$ a [[Grothendieck category]] [[category with translation|with translation]] $T : \mathcal{A}  \to \mathcal{A}$, every [[complex]] $X$ in $Ch_\bullet(\mathcal{A})$ is quasi-isomorphic to a complex $I$ which is injective and homotopically injective (i.e. QuasiIsoMono-injective).


### Relation to derived categories 

For $\mathcal{A}$ an [[abelian category|abelian]] [[Grothendieck category|Grothendieck category]] [[category with translation|with translation]] the [[full subcategory]] $K_{hi}(\mathcal{A}) \subset K(\mathcal{A})$ of _homotopically injective_ complexes realizes the [[derived category]] $D(\mathcal{A})$ of $\mathcal{A}$:

$$
  Q|_{K_{hi}(A)} : K_{hi}(A) \stackrel{\simeq}{\to} D(A)
  \,,
$$

where $Q : K(A) \to D(A)$ and $Q|_{K_{hi}(A)}$ has a [[adjoint functor|right adjoint]].

It follows that for $D$ any other [[triangulated category]], every [[triangulated functor]] $F : K(\mathcal{A}) \to D$ has a right [[derived functor]] $R F : D(\mathcal{A}) \to D$ which is computed by evaluating $F$ on _injective replacements_: for 
$R : D(\mathcal{A}) \stackrel{\simeq}{\to} K_{hi}(\mathcal{A})$ a weak inverse to $Q$, we have

$$
  R F \simeq D(A) \stackrel{R}{\to} K_{hi}(A) \hookrightarrow K(A) \stackrel{F}{\to} D
  \,.
$$

## References#

Much of this discussion can be found in 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

The general notion of [[injective objects]] is in section 9.5, the case of injective complexes in section 14.1.

[[!redirects homotopically injective objects]]
