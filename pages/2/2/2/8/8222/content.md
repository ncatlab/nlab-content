

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

Let $\mathcal{A}$, $\mathcal{B}$ be two [[abelian categories]]. 

A **homological $\delta$-functor** from $\mathcal{A}$ to $\mathcal{B}$ is for each $n \in \mathbb{N}$ a [[functor]]

$$
  T_n : \mathcal{A} \to \mathcal{B}
$$

equipped for each [[short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with a [[natural transformation]]

$$
  \delta_n : T_n(C) \to T_{n-1}(A)
$$

such that for each such short exact sequence there is, [[natural transformation|naturally]] a [[long exact sequence]]

$$
      \cdots T_{n+1}(C) \stackrel{\delta}{\to} T_n(A) \to T_n(B) \to T_n(C) \stackrel{\delta }{\to} T_{n-1}(A) \to \cdots
 \,.
$$



=--

## Examples

The archetypical example is the [[chain homology]] functor

$$
  H_\bullet(-) : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
$$

from the [[category of chain complexes]] of some [[abelian category]] (for $\mathbb{N}$-graded complexes).

The _universal_ example are (non-total) [[right derived functors]].

## Related concepts

* [[derived functor in homological algebra]]


## References

The notion is due to 

* [[Alexander Grothendieck]], _[[Tohoku|Sur quelques points d'algèbre homologique]]_

A textbook account is for instance section 2.1 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

[[!redirects delta-functors]]
[[!redirects ∞-functor]]
[[!redirects ∞-functors]]

[[!redirects universal delta-functor]]
[[!redirects universal delta-functors]]
[[!redirects universal ∞-functor]]
[[!redirects universal ∞-functors]]

[[!redirects delta functor]]
[[!redirects delta functors]]
[[!redirects δ functor]]
[[!redirects δ functors]]
