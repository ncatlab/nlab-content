
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let throughout $\mathcal{C}$ be a [[stable (∞,1)-category]], $\mathcal{A}$ an [[abelian category]], 

A _homological functor_ 

$$
   \pi \;\colon\; \mathcal{C}\longrightarrow \mathcal{A}
$$ 

is an [[(∞,1)-functor]] that transforms every [[homotopy cofiber sequence]]

$$ X\to Y\to Z\to \Sigma X $$

in $\mathcal{C}$ into a [[long exact sequence]]

$$ \dots \to \pi(X)\to \pi(Y)\to \pi(Z)\to \pi(\Sigma X) \to \dots $$

in $\mathcal{A}$. One writes 

$$
  \pi_n \coloneqq \pi\circ \Sigma^{-n}
$$

for $n \in \mathbb{N}$ and for $\Sigma$ the [[suspension]] functor.

## Examples

+-- {: .num_example}
###### Example


* $\mathcal{C}$ is arbitrary, $\mathcal{A}$ is the category of [[abelian groups]] and $\pi$ is $\pi_0 \mathcal{C}(S,-)$ for some object $S\in\mathcal{C}$

* $\mathcal{C}$ is equipped with a [[t-structure]], $\mathcal{A}$ is the [[heart of a stable (∞,1)-category|heart]] of the t-structure, and $\pi$ is the canonical functor.

* $\mathcal{C} = D(\mathcal{A})$ is the [[derived category]] of the abelian category $\mathcal{A}$ and $\pi=H_0$.

* Any of the above with $\mathcal{C}$ and $\mathcal{A}$ replaced by their [[opposite categories]].

* Any reduced [[generalized homology theory]].

=--

## Related concepts

* [[homotopical functor]]

* [[Adams spectral sequence]]

* [[Lurie spectral sequence]]

[[!redirects homological functors]]
[[!redirects homological (∞,1)-functor]]
[[!redirects homological (∞,1)-functors]]
