
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

In [[homotopy type theory]], given a [[universe in type theory|universe]], $\mathcal{U}$, we may define a type of [[mere propositions]] within that universe, $\sum_{A: \mathcal{U}} isProp(A)$. For universes, $\mathcal{U}_i$ and $\mathcal{U}_{i+1}$, we have that $A: \mathcal{U}_i$ entails $A:\mathcal{U}_{i+1}$. We thus have a natural map

$$
Prop_{\mathcal{U}_i} \to Prop_{\mathcal{U}_{i+1}}.
$$

The axiom of **proposition resizing** states that this map is an [[equivalence]]. Any mere proposition in the larger universe may be *resized* to an equivalent mere proposition in the smaller universe.

The axiom is a form of [[impredicativity]] for mere propositions, and by avoiding its use, the type theory is said to remain predicative.

## See also

* [[essentially small type]]

## References

* Section 3.5 of [[The HoTT Book]]