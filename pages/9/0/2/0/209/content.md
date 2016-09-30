
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _faithful_ if for each pair of objects $x, y \in C$, the function

$$F : C(x,y) \to D(F(x), F(y))$$

between [[hom sets]] is [[injection|injective]].  

More abstractly, we may say a functor is faithful if it is $2$-[[k-surjective functor|surjective]] &#8211; or loosely speaking, 'surjective on equations between given morphisms'.

See also [[faithful morphism]] for a generalization to an arbitrary [[2-category]].

## Properties

+-- {: .num_prop }
###### Proposition

A faithful functor [[reflected limit|reflects]] [[epimorphisms]] and [[monomorphisms]].

=--

(The simple proof is spelled out for instance at _[[epimorphism]]_.)


## Related concepts

* [[essentially surjective functor]]

* [[full functor]]

* [[full and faithful functor]]

* [[equivalence of categories]]

[[!redirects faithful]]
[[!redirects faithful functors]]
