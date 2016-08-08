
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

The _covering lifting property_ on a [[functor]] between [[sites]] is a sufficient condition for it to induce a [[geometric morphism]] between the corresponding [[sheaf toposes]] _covariantly_, i.e. with [[direct image]] going in the same direction. Sometimes, one calls such a functor _cocontinuous_, _cover-reflecting_ (e.g., the [[Elephant]]) or a _comorphism of sites_.

(As opposed to a [[morphism of sites]], also known as a _continuous_ functor, which induces a geometric morphism contravariantly, going the other way around.)

## Definition

Let $C$ and $D$ be [[sites]].

+-- {: .num_defn #clp}
###### Definition

A [[functor]] $f \colon C \to D$ is said to have the _covering lifting property_ ([MacLane-Moerdijk, p. 410](#MacLaneMoerdijk)) if for every object $U \in C$ and every [[cover]] $\{q_i : V_i \to f(U)\}$ of $f(U) \in D$, there is a cover $\{p_j : U_j \to U\}$ of $U \in C$ such that $\{f(p_j) : f(U_j) \to f(U)\}$ refines $\{q_i : V_i \to f(U)\}$ (i.e., if every cover of the image of any $U$ under $f$ is refined by the image of a cover of $U$).

=--

## Properties

A functor between sites with covering lifting property induces a [[geometric morphisms]] between the corresponding [[sheaf toposes]] covariantly, with [[inverse image]] given by pre-composition with $F$ followed by [[sheafification]]. ([MacLane-Moerdijk, Theorem VII.10.5](#MacLaneMoerdijk))

See also: [The Elephant, Proposition C2.3.18](#Elephant).

## References

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

* {#Elephant} [[Peter Johnstone]], [[Elephant|Sketches of an elephant: a topos theory compendium]]

[[!redirects cover-reflecting]]
[[!redirects comorphism of sites]]