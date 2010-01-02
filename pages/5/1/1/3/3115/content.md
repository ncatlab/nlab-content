# Definition

Let $A$ be an [[abelian category]] [[category with translation|with translation]]. 

An object in the category of [[complex]]es modulo chain homotopy, $K(A)$, 
of an [[abelian category]] $C$ is **homotopically injective** if for every $X \in K(C)$ that is
[[quasi-isomorphism|quasi-isomorphic]] to $0$
we have
$$
  Hom_{K(C)}(X,I) \simeq 0
  \,.
$$

Let $QuasiIsoMono = \{f \in Mor(A_c) | f mono and quasiio\}$ be the set of morphisms in the category of [[complex]]es $A_c$ which are both [[quasi-isomorphism]]s as well as [[monomorphism]]s. 

Then

A [[complex]] $I$ is an [[injective object]] with respect to monomorphic quasi-isomorphisms precisely if

* it is homotopically injective in the sense of complexes in $A$;

* it is injective as an object of $A$ (with respect to morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is exact).


# In complexes in a Grothendieck category #

**Proposition** 
For $A$ a [[Grothendieck category]] [[category with translation|with translation]] $T : C  \to C$, every [[complex]] $X$ in $A_c$ is quasi-isomorphic to a complex $I$ which is injective and homotopically injective (i.e. QuasiIsoMono-injective).

# Relation to derived categories #

For $A$ an [[abelian category|abelian]] [[Grothendieck category|Grothendieck category]] [[category with translation|with translation]] the full [[subcategory]] $K_{hi}(A) \subset K(A)$ of _homotopically injective_ complexes realizes the [[derived category]] $D(A)$ of $A$:

$$
  Q|_{K_{hi}(A)} : K_{hi}(A) \stackrel{\simeq}{\to} D(A)
  \,,
$$

where $Q : K(A) \to D(A)$ and $Q|_{K_{hi}(A)}$ has a [[adjoint functor|right adjoint]].

It follows that for $D$ any other [[triangulated category]], every triangulated functor $F : K(A) \to D$ has a right [[derived functor]] $R F : D(A) \to D$ which is computed by evaluating $F$ on _injective replacements_: for 
$R : D(A) \stackrel{\simeq}{\to} K_{hi}(A)$ a weak inverse to $Q$, we have

$$
  R F \simeq D(A) \stackrel{R}{\to} K_{hi}(A) \hookrightarrow K(A) \stackrel{F}{\to} D
  \,.
$$

#References#

Much of this discussion can be found in 

* Kashiwara--Schapira, [[Categories and Sheaves]]

The general notion of injective objects is in section 9.5, the case of injective complexes in section 14.1.
