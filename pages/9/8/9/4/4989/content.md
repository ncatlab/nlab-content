
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Cohesive site
* table of contents
{: toc}

## Idea

A **cohesive site** is a small [[site]] whose [[topos of sheaves]] is a [[cohesive topos]].

## Definition
 {#Definition}


+-- {: .num_defn}
###### Definition

Let $C$ be a [[small site|small]] [[site]], i.e. a [[small category]] equipped with a [[coverage]]/[[Grothendieck topology]].  We say that $C$ is a **cohesive site** if

1. $C$ has a [[terminal object]].

1. The coverage on $C$ makes it a [[locally connected site]], i.e. every [[cover|covering]] [[sieve]] on an object $U\in C$ is [[connected category|connected]] as a [[subcategory]] of the [[slice category]] $C/U$.

1. Every object $U\in C$ admits a [[global section]] $*\to U$.

1. $C$ is a [[cosifted category]] 

   (for instance in that it has all [[finite products]], see at _[[categories with finite products are cosifted]]_).

=--


## Properties

### Sheaves on a cohesive site are cohesive
 {#SheavesOnACohesiveSiteAreCohesive}

+-- {: .num_prop}
###### Proposition

For $C$ a cohesive site, the [[category of sheaves]] $Sh(C)$ on $C$ is a [[cohesive topos]] over [[Set]] for which _[[pieces have points]]_ .

=--

+-- {: .proof}
###### Proof

Following the notation at [[cohesive topos]], we write 

$$
  (Disc \dashv \Gamma) 
    \coloneqq 
  (L Const \dashv \Gamma) 
  \;\colon\; 
  Sh(C) \to Set
$$

for the [[global section]] [[geometric morphism]], where the [[inverse image]] $Disc$ constructs [[discrete object]]s. We need to exhibit two more adjoints

$$
  (\Pi_0 \dashv Disc \dashv \Gamma \dashv CoDisc) 
  \;\colon\; 
  Sh(C) \to Set
$$

and show that $\Pi_0$ preserves [[finite products]]. Finally we need to show that $\Gamma X \to \Pi_0 X$ is an [[epimorphism]] for all $X$.

Firstly, since $C$ is a [[locally connected site]], any constant presheaf is a sheaf.  This implies that the functor $Disc$ has a further [[left adjoint]] given by taking [[colimits]] over $C^{op}$, which we denote $\Pi_0$.  Hence $Sh(C)$ is a [[locally connected topos]].

Moreover, since $C$ is [[cosifted category|cosifted]], $\Pi_0$ preserves finite products.  In particular, $Sh(C)$ is [[connected topos|connected]] and even *strongly connected*.

Next, we claim that $C$ is a [[local site]].  This means that its [[terminal object]] $*$ is *cover-irreducible*, i.e. any covering [[sieve]] of $*$ must contain its identity map.  But since $C$ is a locally connected site, every covering family is inhabited, and since every object has a global section, every covering sieve must include a global section.  In the case of $*$, the only global section is an identity map; hence $C$ is a local site, and so $Sh(C)$ is a [[local topos]].  The [[right adjoint]] $Codisc$ of $\Gamma$ is defined by

$$ 
  CoDisc(A)(U) = A^{C(*,U)} = A^{\Gamma(U)}
  \,.
$$

We now claim that the transformation $Disc(A) \to Codisc(A)$ is [[monic]].  Since sheaves are closed under limits in presheaves, this condition can be checked pointwise at each object $U\in C$.  But since constant presheaves are sheaves, the map $Disc(A)(U) \to Codisc(A)(U)$ is just the [[diagonal morphism|diagonal]]

$$ 
  A \to A^{C(*,U)} 
$$

which is monic since $C(*,U)$ is always inhabited (by assumption on $C$).

=--

### Aufhebung

A [[cohesive topos]] over a cohesive site satisfies [[Aufhebung]] of the [[unity of opposites|moments]] of [[becoming]]. See at _[[Aufhebung]]_ the section _[Aufhebung of becoming -- Over cohesive sites](http://ncatlab.org/nlab/show/Aufhebung#ExamplesBecomingFormalization)_


## Examples

### Cohesive presheaf sites

Consider a category $C$ equipped with the trivial coverage/topology. Then the [[category of sheaves]] on $C$ is the [[category of presheaves]] on $C$

$$
  Sh(C) \simeq PSh(C)
$$

and trivially every constant presheaf is a sheaf. So we always have an [[adjoint triple]] of  functors

$$
  (\Pi_0 \dashv Disc \dashv \Gamma) : Sh(C) \to Set
  \,,
$$

where

* $\Pi_0$ is the functor that takes [[colimit]]s of functors $X : C^{op} \to Set$ 

  $$
    \Pi_0 X = {\lim_\to} X
  $$

* $\Gamma$ is the functor that takes [[limit]]s;

  $$
    \Gamma X = {\lim_\leftarrow} X    
    \,.
  $$

The condition that $\Pi_0$ preserves finite products is precisely the condition that $C$ be a [[cosifted category]].

In conclusion we have

+-- {: .num_prop}
###### Proposition

A small category equipped with the trivial coverage/topology is a cohesive site if

* it is [[cosifted category|cosifted]];

* has a [[terminal object]] $*$.

* every object $U$ has a [[global element]] $* \to U$.

The first two conditions ensure that $Sh(C) = PSh(C)$ is a [[cohesive topos]]. The last condition implies that _cohesive pieces have points_ in $PSh(C)$.

=--

### Sites of open balls

Any full small subcategory of [[Top]] on [[connected]] topological spaces with the canonical induced [[open cover]] [[coverage]] is a cohesive site. If a subcategory on [[contractible]] spaces, then this is also an [[(∞,1)-cohesive site]]. 

Specifically we have:

+-- {: .num_prop}
###### Proposition

The categories [[CartSp]] and [[ThCartSp]] equipped with the standard [[open cover]] [[coverage]] are cohesive sites.

=--

The axioms are readily checked.

Notice that the cohesive topos over $ThCartSp$ is the [[Cahiers topos]].

+-- {: .num_prop}
###### Proposition

The cohesive concrete objects of the cohesive topos $Sh(CartSp)$ are precisely the [[diffeological space]]s.

=-- 

See [[cohesive topos]] for more on this.


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* **cohesive site** / [[∞-cohesive site]]


## References

* [[Urs Schreiber]]: §3.4.2.1 in: *[[schreiber:dcct|Differential cohomology in a cohesive $\infty$-topos]]* &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;



[[!redirects cohesive sites]]
[[!redirects site of cohesion]]
[[!redirects sites of cohesion]]
