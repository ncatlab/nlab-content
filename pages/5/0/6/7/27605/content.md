
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **Priestley space** is a [[compact topological space]] with a [[partial order]] $\leq$ which satisfies the *Priestley separation axiom*:

* If $x \nleq y$, then there exists a [[clopen]] [[upper set]] $U$ of $X$ such that $x \in U$ and $y \notin U$. 

## Properties

Every Priestley space is a [[sober topological space]]. Furthermore, every Priestley space is a [[Hausdorff space]] and a [[Stone space]]. 

## Examples

* Every [[finite set|finite]] [[poset]] is a Priestley space. 

## Category of Priestley spaces

The category of Priestley spaces is the category whose objects are Priestley spaces and whose morphisms are [[monotonic]] [[continuous functions]] between Priestley spaces. 

The category of Priestley spaces is the [[opposite category]] of [[DistLat]], the category of [[distributive lattices]]. This phenomenon is called **Priestley [[duality]]**, and is a [[Stone duality|Stone-type duality]] akin to the one between [[Stone spaces]] and [[Boolean algebras]] or [[locales]] and [[frames]]. The category of Priestley spaces is thus equivalent to the category of [[coherent locales]]. 

## In constructive mathematics

In [[constructive mathematics]], it is no longer provable that Priestley spaces coincide with objects of $\mathrm{DistLat}^\op$. 

Better behaved in constructive mathematics are [[coherent locales]] and [[coherent maps]], which are provably still the objects and morphisms of $\mathrm{DistLat}^\op$ even in the absence of [[excluded middle]] or [[axiom of choice|choice axioms]]. 

## Related concepts

* [[distributive lattice]]

* [[coherent locale]]

## References

* Wikipedia, [Priestley space](https://en.wikipedia.org/wiki/Priestley_space)

[[!redirects Priestley space]]
[[!redirects Priestley spaces]]

[[!redirects Priestley topological space]]
[[!redirects Priestley topological spaces]]

[[!redirects category of Priestley spaces]]