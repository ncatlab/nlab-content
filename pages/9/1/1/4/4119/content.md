
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _basis for a topology_ is a collection of morphisms in a [[category]] $C$ that induce the structure of a [[site]] on $C$. In particular, they _generate_ a [[Grothendieck topology]] on $C$.

A similar notion is that of [[coverage]].

## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[category]] with [[pullback]]s. A **basis (for a [[Grothendieck topology]])** on $C$ is an assignment to each [[object]] $U$ of $C$ of a collection of families $\{U_i \to U\}$ of morphisms, called **[[covering]] families]]** such that

1. _isomorphisms cover_ -- every family consistsing of a single [[isomorphism]] $\{V \stackrel{\cong}{\to}U\}$ is a covering family;

1. _stability axiom_ -- the collection of covering families is stable under [[pullback]]: if $\{U_i \to U\}$ is a covering family and $f : V \to U$ is any morphism in $C$, then $\{f^* U_i \to V\}$ is a covering family;

1. _transitivity axiom_ -- if $\{U_i \to U\}_{i \in I}$ is a covering family and for each $i$ also $\{U_{i,j} \to U_i\}_{j \in J_i}$ is a covering family, then also the family of composites $\{U_{i,j} \to U_i \to U\}_{i\in I, j \in J_i}$ is a covering family.

=--

+-- {: .un_defn}
###### Definition


The [[Grothendieck topology]] on $C$ _generated_ from a basis of covering families is that for which a [[sieve]] $\{S_i \to U\}$ is covering precisely if it contains a covering family of morphisms.

=--


## Properties

Given any [[Grothendieck topology]] on $C$, there is a **maximal basis** which generates it: this has as covering families precisely thoses families of morphisms that generate a covering sieve under completion under precomposition.




## References

This appears for instance as definition 2 on page 111 of

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ 



[[!redirects basis for a Grothendieck topology]]

[[!redirects bases for a topology]]
[[!redirects bases for a Grothendieck topology]] .