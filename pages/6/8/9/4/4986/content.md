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

## Definition

A [[geometric morphism]] $f\colon E\to S$ is **totally connected** if

1. It is [[locally connected geometric morphism|locally connected]], i.e. its [[inverse image functor]] $f^*$ has a left adjoint $f_!$ which is $S$-[[indexed functor|indexed]], and

1. The functor $f_!$ is [[left exact functor|left exact]], i.e. preserves [[finite limits]].

When thinking of $E$ as a topos over $S$ via $f$, we say that it is a **totally connected $S$-topos**.  In particular, when $S=Set$ and $f = (L Const, \Gamma)$ is the unique [[global sections]] geometric morphism, we call $E$ a **totally connected topos**.

## Properties

Of course, any totally connected geometric morphism is [[connected geometric morphism|connected]], since the [[terminal object]] is a particular finite limit.  It is also [[strongly connected geometric morphism|strongly connected]], since finite products are also finite limits.

## Examples

*  A topos $Sh(X)$ of sheaves on a [[topological space]] is totally connected iff $X$ has a [[dense subset|dense]] point (a single point whose closure is all of $X$).

*  A presheaf topos $Psh(C)$ is totally connected iff $C$ is [[cofiltered category|cofiltered]].

## Totally connected sites

A small [[site]] $C$ is called **totally connected** if

1. $C$ is [[cofiltered category|cofiltered]], and

1. Every [[cover|covering]] [[sieve]] in $C$ is [[connected category|connected]], when regarded as a subcategory of a [[slice category]].

The second condition implies that all constant presheaves are sheaves, and hence that the left adjoint $Colim\colon Psh(C) \to Set$ of $Const\colon Set\to Psh(C)$ restricts to $Sh(C)$ to give a left adjoint of $L Const$.  Cofilteredness of $C$ is exactly what is needed for left exactness of $Colim\colon Psh(C) \to Set$, essentially by definition.  Hence the topos of sheaves on any totally connected site is totally connected.

Conversely, one can show that any totally connected topos can be (but need not be) presented by some totally connected site.

## References

Chapter C3.6 in the [[Elephant]].

[[!redirects totally connected]]
[[!redirects totally connected geometric morphisms]]
[[!redirects totally connected topos]]
[[!redirects totally connected toposes]]
[[!redirects totally connected topoi]]
[[!redirects totally connected site]]
[[!redirects totally connected sites]]
