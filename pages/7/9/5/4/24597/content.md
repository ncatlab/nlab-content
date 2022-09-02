+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Split essentially surjective functors
* table of contents
{: toc}

## Idea

In foundations without the [[axiom of choice]], it is not true that every [[equivalence of categories]] is a [[fully faithful functor|fully faithful]] [[essentially surjective functor]], since the mere property of being isomorphic is not enough to get a specific isomorphism between two objects without the axiom of choice. Instead one has to use split essentially surjective functors, where the isomorphisms are structure rather than mere property. 

## Definition

A [[functor]] $F : C \to D$ is **split essentially surjective** if the functor come with the structure of a [[family]] of [[isomorphisms]]  
$$p_y \in \biguplus_{x \in C} F(x) \cong y$$
indexed by objects $y \in D$. 

### In homotopy type theory

In [[homotopy type theory]], a [[functor]] $F : C \to D$ is **split essentially surjective** if the functor comes with the structure of an dependent [[isomorphism]]  
$$p(y):\sum_{x:C} F(x) \cong y$$
for all objects $y:D$. 

## Examples

* Every [[equivalence of categories]] is fully faithful and split essentially surjective. 

* Every essentially surjective functor between [[gaunt categories]] is split essentially surjective. 

## Properties

* Every split essentially surjective functor is [[essentially surjective]]. 

## Related concepts

[[!include properties of functors -- contents]]

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects split essentially surjective functor]]
[[!redirects split essentially surjective functors]]
[[!redirects split essentially surjective on objects functor]]
[[!redirects split essentially surjective on objects functors]]
[[!redirects seso functor]]
[[!redirects seso functors]]
[[!redirects split essentially surjective]]