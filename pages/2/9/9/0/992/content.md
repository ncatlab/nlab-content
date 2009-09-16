<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Idea#

A stable [[(infinity,1)-category]], is an $(\infty,1)$-category all whose objects are stable in the sense of [[stable homotopy theory]]: they behave as if they were [[spectrum|spectra]].

The [[homotopy category]] of a stable $\infty$-category is a [[triangulated category]].  This could be considered remarkable, because the definition of triangulated categories is involved and their behaviour is bad, whereas the definition of stable $\infty$-category is very simple.  So the complexity and bad behavior of triangulated categories comes from trying to capture at the level of a homotopy category a type of structure that properly belongs to an $(\infty,1)$-category.

The relation between triangulated categories and stable $\infty$-categories has apparently been clear to some experts, but a comprehensive discussion appeared only more recently in the first part of Jacob Lurie's PhD thesis

* Jacob Lurie, _Stable $\infty$-Categories_ ([pdf](http://math.mit.edu/~lurie/topoibook/DAGI.pdf))

building on the general theory of [[(infinity,1)-category|(infinity,1)-categories]] as developed in his book

* Jacob Lurie, [[Higher Topos Theory]].

#Definition#

(...the following should eventually bit split into separate entries for each keyword...)

As with ordinary categories, an  object in a [[(infinity,1)-category]] is a [[zero object]] if it is both [[initial object]] and a [[terminal object]]. An $(\infty,1)$-category with a zero object is a **pointed** $(\infty,1)$-category.

Here and in the following, all notions such as [[initial object]], [[terminal object]], [[diagram]], [[pullback]], [[pushout]] etc. are to be interpreted in the sense of $(\infty,1)$-categories. See [[Higher Topos Theory]].

In a pointed $(\infty,1)$-category $C$ with zero object $0$, the **kernel** of a morphism $g : X \to Y$ is the [[pullback]]

$$
  \array{
     ker(g) &\to& X
     \\
     \downarrow && \downarrow^g
     \\
     0 &\to& Y
  }
$$

(so that $ker(g) \to X \stackrel{g}{\to} Y$ is a [[fibration sequence]])

and the **cokernel** of $g$ is the [[pushout]]

$$
  \array{
     X &\stackrel{g}{\to}& Y
     \\
     \downarrow && \downarrow
     \\
     0 &\to& coker(g)
  }
  \,.
$$

An arbitrary commuting square in $C$ of the form

$$
  \array{
     A &\to& B
     \\
     \downarrow && \downarrow
     \\
     0 &\to& C
  }
$$

is a **triangle** in $C$. A pullback triangle is called an **exact triangle** and a pushout triangle a **coexact triangle**.

A **stable $(\infty,1)$-category** is a pointed $(\infty,1)$-category such that

* for every morphism in $C$ kernel and cokernel exist;

* every exact triangle is coexact and vice versa, i.e. every morphism is the cokernel of its kernel and the kernel of its cokernel. 

#Constructions in stable $\infty$-categories#

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

but also that, conversely, every object $X$ has a suspension
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

For every pointed $(\infty,1)$-category which is not yet stable there is something like its free stabilization, a stable $(\infty,1)$-category $Sp(C)$ that can be defined as the [[homotopy limit]]

$$
  Sp(C) := holim(   \cdots \to C \stackrel{\Omega}{\to} C \stackrel{\Omega}{\to} C )
  \,.
$$

For $C =$ [[Top]] the $(\infty,1)$-category of topological spaces, $Sp(Top)$ is the familiar [[stable (infinity,1)-category of spectra]] used in stable homotopy theory (which gives stable $(\infty,1)$-categories their name).

Moreover, every [[derived category]] of an [[abelian category]] is the triangulated homotopy category of a stable $(\infty,1)$-category. 

Hence stable homotopy theory and homological algebra are both special cases of the theory of stable $(\infty,1)$-categories.

# Alternative models # 

Stable $(\infty,1)$-categories are equivalent to

* $\Leftrightarrow$ [[stable model category]]

* $\Leftrightarrow$ [[pre-triangulated spectral category]]

The following three concepts are equivalent to each other and special cases of the above models, or equivalent in characteristic 0.

* [[pretriangulated dg-category]]

* [[Frobenius category]]

A [[triangulated category]] linear over a field $k$ can canonically be refined to 

* an [[enhanced triangulated category]]:

  * a [[pretriangulated dg-category|pretriangulated]] [[dg-category]];

* an [[A-infinity-category]];

* a stable $(\infinity,1)$-category.

If $k$ has characteristic 0, then all these three concepts become equivalent.


# Warning on terminology #

A stable $\infty$-category should not be confused with a [[k-tuply monoidal n-category|stably monoidal]] $\infty$-category.  A connection between the terms is that the $(\infty,1)$-category of [[spectrum|spectra]] is the prototypical stable $\infty$-category, while _connective_ spectra (not all spectra) can be identified with [[k-tuply groupal n-groupoid|stably groupal]] $\infty$-groupoids, aka _infinite loop spaces_ or $E_\infty$-[[E-infinity-space|spaces]].


#References#

The canonical reference is of course

* [[Jacob Lurie]], [[Stable Infinity-Categories]]

This claims that

>most of the results presented here are well-known to experts

but is certainly the only comprehensive source for these results.

A diagram of the interrelation of all the models for stable $(\infty,1)$-categories with a useful list of literature for each are these seminar notes:

* S. Schwede, _Enhancements of triangulated categories_ ([pdf](http://www.math.uni-bonn.de/people/schwede/EnhancedSeminar.pdf))

[[!redirects stable (infinity,1)-categories]]
[[!redirects stable (∞,1)-category]]
[[!redirects stable (∞,1)-categories]]