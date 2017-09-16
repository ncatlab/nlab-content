#Definition#

There is a very general notion of _injective objects_ in a category $C$, and a sequence of refinements as $C$ is equipped with more [[stuff, structure, property|structure and property]], in particular for $C$ an [[abelian category]] [[additive and abelian categories|or a relative]].

## General definition ##

Let $C$ be a [[category]] and $J$ a collection of morphisms in $C$. Frequently $J$ is the class of all [[monomorphism]]s or a related class.  An object $I$ in $C$ is **$J$-injective** if all diagrams

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} 
    \\
    Z
  }
$$

admit an extension

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} & \nearrow_{\exists}
    \\
    Z
  }
  \,.
$$

If $C$ has a [[terminal object]] $*$ this can be thought of as a lift

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} & \nearrow_{\exists}
    &
    \downarrow
    \\
    Z
    &\to&
    *
  }
$$

as for [[weak factorization system|factorization systems]].

If $C$ is a [[small category]] then $I$ is $J$-injective precisely if the [[hom-functor]]

$$
  Hom_C(-,I) : C^{op} \to Set
$$

takes morphisms in $J$ to [[epimorphism]]s in [[Set]].

The dual notion is a [[projective object]].


## In abelian categories ##

More specifically, the term _injective object_ is used in the context that  $C$ is an [[abelian category]] for $J$ the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is [[exact sequence|exact]].  (Then $J$ is simply the class of all [[monomorphism]]s, but abelian category theorists like to think about exact sequences.)

+--{: .query}
[[Mike Shulman|Mike]]: Unless I'm very confused, in an abelian category, that is just the class of all monomorphisms.  But maybe you have some more general context in mind?

_Toby_:  I think that it\'s just a cultural preference, as I wrote above.
=--
 
Then an [[object]] $I$ of $C$ is **injective** if it satisfies the following equivalent conditions:

* the [[hom-functor]] $Hom_C(-, I) : C^{op} \to Set$ is [[exact functor|exact]];

* for all [[morphism]]s $f : X \to Y$ such that $0 \to X \to Y$ is [[exact sequence|exact]] and for all $k : X \to I$, there exists $h : Y \to I$ such that $ h\circ f = k$.

$$
  \array{
    0 &\to& X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^k & \swarrow_{\exists h}
    \\
    &&
    I 
  }
  \,.
$$

## In categories of chain complexes ##

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

A [[complex]] $I$ is injective with respect to monomorphic quasi-isomorphisms precisely if

* it is homotopically injective in the sense of complexes in $A$;

* it is injective as an object of $A$ (with respect to morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is exact).


#Existence of injective objects#


## In complexes in a Grothendieck category ##

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