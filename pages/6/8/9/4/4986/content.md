+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Totally connected geometric morphism
* table of contents
{: toc}

## Idea

**Totally connectedness** is a stronger form of _local connectedness_ that arose in the work of [[Marta Bunge|M. Bunge]] and [[Jonathon Funk|J. Funk]] on _topos distributions_.

The properties of totally connected geometric morphisms are largely dual to those of [[local geometric morphisms]].

## Definition

A [[geometric morphism]] $f\colon E\to S$ is **totally connected** if

1. It is [[locally connected geometric morphism|locally connected]], i.e. its [[inverse image functor]] $f^*$ has a left adjoint $f_!$ which is $S$-[[indexed functor|indexed]], and

1. The functor $f_!$ is [[left exact functor|left exact]], i.e. preserves [[finite limits]].

When thinking of $E$ as a topos over $S$ via $f$, we say that it is a **totally connected $S$-topos**.  In particular, when $S=Set$ and $f = (L Const, \Gamma)$ is the unique [[global sections]] geometric morphism, we call $E$ a **totally connected topos**.

## Properties

* Of course, any totally connected geometric morphism is [[connected geometric morphism|connected]], since the [[terminal object]] is a particular finite limit.  It is also [[strongly connected geometric morphism|strongly connected]], since finite products are also finite limits.

* Totally connected geometric morphisms are closed under composition and stable under pullback.

* $f$ is totally connected iff $f$ is connected and has a right adjoint in $\mathfrak{Top}$, the [[topos|2-category of toposes]] and geometric morphisms.

* Totally connected geometric morphisms are orthogonal to [[grouplike geometric morphism|grouplike geometric morphisms]] (cf. Johnstone (2002)).

* A connected, locally connected $p:\mathcal{E}\to\mathcal{S}$ that satisfies the [[Nullstellensatz|Lawvere Nullstellensatz]] (i.e. the canonical $\theta:p_*\to p_!$ is epic) is totally connected precisely iff it is a [[quality type]] over $\mathcal{S}$ (i.e. $\theta$ is iso; cf. Johnstone (2011)).

## Examples

*  A topos $Sh(X)$ of sheaves on a [[topological space]] is totally connected iff $X$ has a [[dense subset|dense]] point (a single point whose closure is all of $X$).

*  A presheaf topos $Psh(C)$ is totally connected iff $C$ is [[cofiltered category|cofiltered]].

## Totally connected sites

A small [[site]] $C$ is called **totally connected** if

1. $C$ is [[cofiltered category|cofiltered]], and

1. Every [[cover|covering]] [[sieve]] in $C$ is [[connected category|connected]], when regarded as a subcategory of a [[slice category]].

The second condition implies that all constant presheaves are sheaves, and hence that the left adjoint $Colim\colon Psh(C) \to Set$ of $Const\colon Set\to Psh(C)$ restricts to $Sh(C)$ to give a left adjoint of $L Const$.  Cofilteredness of $C$ is exactly what is needed for left exactness of $Colim\colon Psh(C) \to Set$, essentially by definition.  Hence the topos of sheaves on any totally connected site is totally connected.

Conversely, one can show that any totally connected topos can be (but need not be) presented by some totally connected site.

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

  * **totally connected site** / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]] /  [[∞-cohesive site]]

## References

* [[Marta Bunge]], [[Jonathon Funk]], _Spreads and the Symmetric Topos_ , JPAA **113** (1996) pp.1-38.

* [[Marta Bunge]], [[Jonathon Funk]], _Spreads and the Symmetric Topos II_ , JPAA **130** (1998) pp.49-84.


* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ , Oxford UP 2002. (vol. 2, Section C.3.6, pp.707-710)

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))


[[!redirects totally connected]]
[[!redirects totally connected geometric morphisms]]
[[!redirects totally connected topos]]
[[!redirects totally connected toposes]]
[[!redirects totally connected topoi]]
[[!redirects totally connected site]]
[[!redirects totally connected sites]]


