
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#

* automatic TOC goes here
{:toc}


## Idea

A stable [[(∞,1)-category]] $C$, is an $(\infty,1)$-category with finite [[limit]]s which is _stable_ under forming [[loop space object]]s: 

$C$ has a [[zero object]] and the corresponding loop [[(∞,1)-functor]]

$$
  \Omega : C \to C
$$

an an _equivalence_ with inverse the [[suspension object]] functor

$$
  C \leftarrow C : \Sigma
  \,.
$$


This means that the objects of a stable $(\infty,1)$-category are stable in the sense of [[stable homotopy theory]]: they behave as if they were [[spectrum|spectra]].

Indeed, every $(\infty,1)$-category with finite [[limit]]s has a free [[stabilization]] to a stable $(\infty,1)$-category $Stab(C)$, and the objects of $Stab(C)$ are the [[spectrum object]]s of $C$.

The [[homotopy category of an (∞,1)-category]] of a stable $\infty$-category is a [[triangulated category]].  

Notice that the definition of triangulated categories is involved and their behaviour is bad, whereas the definition of stable $\infty$-category is simple and natural.  The complexity and bad behavior of triangulated categories comes from them being the [[decategorification]] of a structure that is natural in [[higher category theory]].

## Definition

As with ordinary categories, an  object in a [[(infinity,1)-category]] is a [[zero object]] if it is both [[initial object]] and a [[terminal object]]. An $(\infty,1)$-category with a zero object is a **pointed** $(\infty,1)$-category.

Here and in the following, all notions such as [[initial object]], [[terminal object]], [[diagram]], [[pullback]], [[pushout]] etc. are to be interpreted in the sense of $(\infty,1)$-categories. See [[Higher Topos Theory]].

In a pointed $(\infty,1)$-category $C$ with zero object $0$, the **kernel** of a morphism $g : Y \to Z$ is the [[pullback]]

$$
  \array{
     ker(g) &\to& Y
     \\
     \downarrow && \downarrow^g
     \\
     0 &\to& Z
  }
$$

(so that $ker(g) \to Y \stackrel{g}{\to} Z$ is a [[fibration sequence]])

and the **cokernel** of $f:X\to Y$ is the [[pushout]]

$$
  \array{
     X &\stackrel{f}{\to}& Y
     \\
     \downarrow && \downarrow
     \\
     0 &\to& coker(f)
  }
  \,.
$$

An arbitrary commuting square in $C$ of the form

$$
  \array{
     X &\stackrel{f}{\to}& Y
     \\
     \downarrow && \downarrow^g
     \\
     0 &\to& Z
  }
$$

is a **triangle** in $C$. A pullback triangle is called an **exact triangle** and a pushout triangle a **coexact triangle**. By the universal property of pullback and pushout, to any triangle are associated canonical morphisms $X\to\ker(g)$ and $coker(f)\to Z$. In particular, for every exact triangle there is a canonical morphism $coker(ker(g)\to Y)\to Z$ and for every coexact triangle there is a canonical morphism $X\to ker(Y\to coker(f))$. 

A **stable $(\infty,1)$-category** is a pointed $(\infty,1)$-category such that

* for every morphism in $C$ kernel and cokernel exist;

* every exact triangle is coexact and vice versa, i.e. every morphism is the cokernel of its kernel and the kernel of its cokernel. 

## Constructions in stable $\infty$-categories

### Looping and delooping

The relevance of the axioms of a stable $(\infty,1)$-category is that they imply that not only does every object $X$ have a [[loop space object]] $\Omega X$ defined by the exact triangle

$$
  \array{
    \Omega X &\to& 0
    \\
    \downarrow && \downarrow
    \\
    0 &\to& X
  }
$$

but also that, conversely, every object $X$ has a [[suspension object]]
$\Sigma X$ defined by the coexact triangle

$$
  \array{
    X &\to& 0
    \\
    \downarrow && \downarrow
    \\
    0 &\to& \Sigma X
  }
  \,.
$$

These arrange into $(\infty,1)$-endofunctors

$$
  \Omega : C \to C
$$
$$
  \Sigma : C \to C
$$
which are autoequivalences of $C$ that are inverses of each other.


### Stabilization

For every pointed $(\infty,1)$-category with finite [[limit]]s which is not yet stable there is its free [[stabilization]] (see there for more details): 

a stable $(\infty,1)$-category $Sp(C)$ that can be defined as the [[limit in a quasi-category|limit]] in the [[(∞,1)-category of (∞,1)-categories]]

$$
  Sp(C) := holim(   \cdots \to C \stackrel{\Omega}{\to} C \stackrel{\Omega}{\to} C )
  \,.
$$

For $C =$ [[Top]] the $(\infty,1)$-category of topological spaces, $Sp(Top)$ is the familiar [[stable (infinity,1)-category of spectra]] used in stable homotopy theory (which gives stable $(\infty,1)$-categories their name).

Moreover, every [[derived category]] of an [[abelian category]] is the triangulated homotopy category of a stable $(\infty,1)$-category. 

Hence stable homotopy theory and homological algebra are both special cases of the theory of stable $(\infty,1)$-categories.


## The homotopy category of a stable $(\infty,1)$-category: triangulated categories

The [[homotopy category of an (∞,1)-category|homotopy category]] $Ho(C)$ of a stable $(\infty,1)$-category $C$ -- its [[decategorification]] to an ordinary [[category]] -- is less well behaved than the original stable $(\infty,1)$-category, but remembers a shadow of some of its structure: this shadow is the structure of a [[triangulated category]] on $Ho(C)$

* the **translation functor** $T : Ho(C) \to Ho(C)$ comes from the [[suspension object|suspenesion]] functor $\Sigma : C \to C$;

* the **distinguished triangles** in $Ho(C)$ are pieces of the [[fibration sequence]]s in $C$.


For details see [StabCat, section 3](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0608/0608228v5.pdf#page=6).

Alternately, one can first pass to a [[stable derivator]], and thence to a triangulated category.  Any suitably complete and cocomplete $(\infty,1)$-category has an underlying [[derivator]], and the underlying derivator of a stable $(\infty,1)$-category is always stable---while the underlying category of any stable derivator is triangulated.  But the derivator retains more useful information about the original stable $(\infty,1)$-category than does its triangulated homotopy category.


## Models  {#alternativemodels}

In direct analogy to how a general [[(∞,1)-category]] may be [[presentable (∞,1)-category|presented]] by [[model category]], a stable $(\infty,1)$-categories may be presented by a

* [[stable model category]].

Or a

* [[pre-triangulated spectral category]].

There are further variants and special cases of these models.
The following three concepts are equivalent to each other and special cases of the above models, or equivalent in characteristic 0.

* [[pretriangulated dg-category]]

* [[Frobenius category]]

A [[triangulated category]] linear over a field $k$ can canonically be refined to 

* an [[enhanced triangulated category]]:

  * a [[pretriangulated dg-category|pretriangulated]] [[dg-category]];

* an [[A-infinity-category]];

* a stable $(\infinity,1)$-category.

If $k$ has characteristic 0, then all these three concepts become equivalent.




## Stabilization and localization of presheaf $(\infty,1)$-categories {#StabGiraud}

Let $C$ and $D$ be [[(infinity,1)-category|(∞,1)-categories]] and
$Func(C,D)$ the [[(∞,1)-category of (∞,1)-functors]] between them.

Its [[stabilization]] is equivalent to the functor category into the stabilization of $C$:

$$
  Stab(Func(C,D)) \simeq Func(C,Stab(D))
  \,.
$$

In particular, in the case $D = $ [[∞Grpd]] for which 
$Func(C, D) = Func(C, \infty Grpd) =: PSh_{(\infty,1)}(C)$ 
is the [[(∞,1)-category of (∞,1)-presheaves]] we have with
$Stab(\infty Grpd) = Sp$ (the [[stable (∞,1)-category of spectra]]) that

$$
  Stab(PSh_{(\infty,1)}(C)) \simeq Func(C,Sp)
  \,.
$$

This is [StabCat, example 10.13]() .


**Proposition** **("stable Giraud theorem")**
 
Every stable and [[presentable (∞,1)-category]] $C$ is equivalent to an
(accessible) left-exact [[localization of an (∞,1)-category|localization of]] a stabilized $(\infty,1)$presheaf $(\infty,1)$-category: there exists a small $(\infty,1)$-category $E$ and an adjunction

$$
  C \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  Stab(PSh(E)) \simeq Func(E,Sp)
  \,.
$$

This is [StabCat prop 15.9]().

This is the stable analog of the statement that every 
[[(∞,1)-category of (∞,1)-sheaves]] is a left exact localization of
an $(\infty,1)$-category of presheaves.


In terms of ([[stable model category|stable]]) [[model category|model categories]], something like an analog of this statement is theorem 3.3.3 in 

* [[Stefan Schwede]], [[Brooke Shipley]], _Classification of stable model categories_ ([pdf](http://hopf.math.purdue.edu/Schwede-Shipley/class.final.pdf))


## Warning on terminology 

A stable $\infty$-category should not be confused with a [[k-tuply monoidal n-category|stably monoidal]] $\infty$-category.  A connection between the terms is that the $(\infty,1)$-category of [[spectrum|spectra]] is the prototypical stable $\infty$-category, while _connective_ spectra (not all spectra) can be identified with [[k-tuply groupal n-groupoid|stably groupal]] $\infty$-groupoids, aka _infinite loop spaces_ or $E_\infty$-[[E-infinity-space|spaces]].


## References

The canonical reference is of course

* [[Jacob Lurie]], _[[Stable Infinity-Categories]]_

A diagram of the interrelation of all the models for stable $(\infty,1)$-categories with a useful list of literature for each are these seminar notes:

* [[Stefan Schwede]], _Enhancements of triangulated categories_ ([pdf](http://www.math.uni-bonn.de/people/schwede/EnhancedSeminar.pdf))

[[!redirects stable (infinity,1)-categories]]
[[!redirects stable (∞,1)-category]]
[[!redirects stable (∞,1)-categories]]