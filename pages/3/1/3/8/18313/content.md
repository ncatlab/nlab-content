
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given two [[vector bundles]] $E_1 \to X_1$ and $E_2 \to X_2$, then their _external tensor product_ $E_1 \boxtimes E_2 \to X_1 \times X_2$ is the [[tensor product of vector bundles]] on the [[product]] [[space]] $X_1 \times X_2$ of the two [[pullback bundles]] to this space, along the canonical [[projection]] maps $pr_i \colon X_1 \times X_2 \to X_i $.

More abstracty, this is the [[external tensor product]] in the [[indexed monoidal category]] of [[vector bundles]] indexed over suitable [[spaces]].

## Definition

Let $X_1$ and $X_2$ be [[topological spaces]] and let $E_1 \to X_1$ and $E_2 \to X_2$ be [[topological vector bundles]]. 

The [[product topological space]] $X_1 \times X_2$ comes with two [[continuous function|continuous]] [[projection]] functions

$$
  X_1 \overset{pr_1}{\longleftarrow} X_1 \times X_2 \overset{pr_2}{\longrightarrow} X_2
  \,.
$$


This gives rise to the [[pullback bundles]] $pr_1^\ast E_1 \to X_1 \times X_2$ and $pr_2^\ast E_2 \to X_1 \times X_2$. 

The _external tensor product_ $E_1 \boxtimes E_2$ is the [[tensor product of vector bundles]] of these pullback bundles:

$$
  E_1 \boxtimes E_2 \coloneqq (pr_1^\ast E_1) \otimes_{X_1 \times X_2} (pr_2^\ast E_2)
$$

which is again naturally a vector bundle over th product space

$$
  E_1 \boxtimes E_2 \longrightarrow X_1 \times X_2
  \,.
$$

## Properties

+-- {: .num_prop #ExternalProductTheoremIntopologicalKTheory}
###### Proposition
**([[external product theorem]] in [[topological K-theory]])**

For $X$ a [[compact Hausdorff space]] then the external tensor product of vector bundles over $X$ and over the [[2-sphere]] $S^2$ is an [[isomorphism]] of [[topological K-theory]] rings:

$$
  K(X) \otimes K(S^2) \overset{\simeq}{\longrightarrow} K(X \times S^2)
  \,.
$$

=--



## Related entries

* [[direct sum of vector bundles]], [[inner product on vector bundles]]

* [[fundamental product theorem in topological K-theory]]

[[!redirects external tensor products of vector bundles]]
