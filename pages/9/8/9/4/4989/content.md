
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Cohesive site
* table of contents
{: toc}

## Idea

A **cohesive site** is a small [[site]] whose [[topos of sheaves]] is a [[cohesive topos]].

## Definition

Let $C$ be a small [[site]], i.e. a [[small category]] equipped with a [[Grothendieck topology]].  We say that $C$ is a **cohesive site** if

1. $C$ has finite [[products]].

1. The coverage on $C$ makes it a [[locally connected site]], i.e. every [[cover|covering]] [[sieve]] on an object $U\in C$ is [[connected category|connected]] as a [[subcategory]] of the [[slice category]] $C/U$.

1. Every object $U\in C$ admits a [[global section]] $*\to U$.

1. (more conditions?)

## Sheaves on cohesive sites

We claim that the topos $Sh(C)$ of sheaves on a cohesive site $C$ is a [[cohesive topos]].  We will write $Disc = L Const$ for the [[inverse image functor]] of the [[global sections]] [[geometric morphism]] $(L Const, \Gamma)\colon Sh(C) \to Set$, since it constructs [[discrete objects]] in the cohesive topos $Sh(C)$.

Firstly, since $C$ is a [[locally connected site]], any constant presheaf is a sheaf.  This implies that the functor $Disc$ has a further left adjoint given by taking colimits over $C^{op}$, which we denote $\Pi_0$.  Hence $Sh(C)$ is a [[locally connected topos]].

Moreover, since $C$ has finite products, it is in particular [[cosifted category|cosifted]], and therefore $\Pi_0$ preserves finite products.  In particular, $Sh(C)$ is [[connected topos|connected]] and even *strongly connected*.

Next, we claim that $C$ is a [[local site]].  This means that its [[terminal object]] $*$ is *cover-irreducible*, i.e. any covering [[sieve]] of $*$ must contain its identity map.  But since $C$ is a locally connected site, every covering family is inhabited, and since every object has a global section, every covering sieve must include a global section.  In the case of $*$, the only global section is an identity map; hence $C$ is a local site, and so $Sh(C)$ is a [[local topos]].  The right adjoint $Codisc$ of $\Gamma$ is defined by
$$ Codisc(A)(U) = A^{C(*,U)} = A^{\Gamma(U)}.$$

We now claim that the transformation $Disc(A) \to Codisc(A)$ is [[monic]].  Since sheaves are closed under limits in presheaves, this condition can be checked pointwise at each object $U\in C$.  But since constant presheaves are sheaves, the map $Disc(A)(U) \to Codisc(A)(U)$ is just the [[diagonal morphism|diagonal]]
$$ A \to A^{C(*,U)} $$
which is monic since $C(*,U)$ is always inhabited (by assumption on $C$).

Thus, it remains to show "continuity" of $\Pi_0$. ...

## Related concepts

An [[(n,1)-cohesive site]] is a site whose [[(n,1)-topos]] of $n$-sheaves is [[cohesive (n,1)-topos|cohesive]], and an [[(∞,1)-cohesive site]] is a site whose [[(∞,1)-topos]] of sheaves is [[cohesive (∞,1)-topos|cohesive]].


* [[locally connected site]] / [[locally ∞-connected site]]

* **cohesive site** / [[(∞,1)-cohesive site]]


[[!redirects cohesive sites]]
[[!redirects site of cohesion]]
[[!redirects sites of cohesion]]
