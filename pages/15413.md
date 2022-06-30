
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


+-- {: .num_defn #clp}
###### Definition
**(covering lifting property)**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[sites]]. A [[functor]] 

$$
  F \;\colon\; \mathcal{C} \to \mathcal{D}
$$ 

is said to have the _covering lifting property_  if for every object $U \in \mathcal{C}$ and every [[cover]] $\{q_i \colon V_i \to F(U)\}$ of $F(U) \in \mathcal{D}$, there is a cover $\{p_j \colon U_j \to U\}$ of $U \in \mathcal{C}$ such that $\{f(U_j) \overset{f(p_j)}{\to} f(U)\}$ refines $\{ V_i \overset{q_i}{\to} f(U)\}$ (i.e., if every cover of the image of any $U$ under $f$ is refined by the image of a cover of $U$).

=--

([MacLane-Moerdijk, p. 410](#MacLaneMoerdijk))

## Properties

+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition


A functor between sites with covering lifting property (Def. \ref{clp}) induces a [[geometric morphisms]] between the corresponding [[sheaf toposes]] covariantly, 

$$
  Sh(\mathcal{C})
    \underoverset
      {\underset{F_{\ast}}{\longrightarrow}}
      {\overset{L \circ F^\ast}{\longleftarrow}}
      {\bot}
  Sh(\mathcal{D})
$$

with [[inverse image]] given by [[composition|pre-composition]] $F^\ast$ with $F$ followed by [[sheafification]] $L \,\colon\, PSh(\mathcal{C}) \longrightarrow Sh(\mathcal{C})$. 

=--

([MacLane-Moerdijk, Theorem VII.10.5](#MacLaneMoerdijk), [The Elephant, Proposition C2.3.18](#Elephant)).

## References

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

* {#Elephant} [[Peter Johnstone]], [[Elephant|Sketches of an elephant: a topos theory compendium]]

[[!redirects cover-reflecting]]
[[!redirects comorphism of sites]]