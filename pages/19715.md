
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[homotopy type theory]], the type of [[h-propositions]] of a [[Tarski universe]] (or [[Russell universe]]) $U$ is not in general $U$-small. Propositional resizing is then the statement that the type of h-propositions is $U$-small. Propositional resizing is a form of [[impredicativity]] for h-propositions, and by avoiding its use, the universe is said to remain predicative.

There is a separate axiom for a hierarchy of universes, which states that all universes in the hierarchy satisfy propositional resizing. 

## Definition

### For individual universes

Let $(U, T)$ be a [[weakly Tarski universe]] and let
$$\sum_{A:U} \mathrm{isProp}(T(A))$$ 
be the type of all propositions in $U$. The weakly Tarski universe $(U, T)$ is **impredicative** or satisfies **propositional resizing** if it has a term $\Omega_U:U$ and an equivalence 
$$\mathrm{propresize}:T(\Omega_U) \simeq \sum_{A:U} \mathrm{isProp}(T(A))$$

A weakly Tarski universe is **strictly impredicative** or satisfies **strict propositional resizing** if the above equivalence becomes a [[definitional equality]]:

$$T(\Omega_U) \equiv \sum_{A:U} \mathrm{isProp}(T(A))$$

In particular, every impredicative [[strictly Tarski universe]] is strictly impredicative. 

### For a universe hierarchy
 
For universes, $\mathcal{U}_i$ and $\mathcal{U}_{i+1}$, we have that $A: \mathcal{U}_i$ entails $A:\mathcal{U}_{i+1}$. We thus have a natural map

$$
Prop_{\mathcal{U}_i} \to Prop_{\mathcal{U}_{i+1}}.
$$

The axiom of **proposition resizing** states that this map is an [[equivalence]]. Any mere proposition in the larger universe may be *resized* to an equivalent mere proposition in the smaller universe.

## See also

* [[essentially small type]]

## References

* Section 3.5 of [[The HoTT Book]]

[[!redirects propositional resizing]]
[[!redirects weak propositional resizing]]
[[!redirects strict propositional resizing]]

[[!redirects impredicative universe]]
[[!redirects impredicative universes]]
[[!redirects impredicative Tarski universe]]
[[!redirects impredicative Tarski universes]]

[[!redirects weakly impredicative universe]]
[[!redirects weakly impredicative universes]]
[[!redirects weakly impredicative Tarski universe]]
[[!redirects weakly impredicative Tarski universes]]

[[!redirects strictly impredicative universe]]
[[!redirects strictly impredicative universes]]
[[!redirects strictly impredicative Tarski universe]]
[[!redirects strictly impredicative Tarski universes]]

[[!redirects axiom of propositional resizing]]