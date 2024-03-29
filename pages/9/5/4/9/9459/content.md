
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $(X, \{-,-\})$ a [[Poisson manifold]], there is a unique [[bivector]] (skew-symmetric rank (2,0)-[[tensor field]]) $\pi \in \wedge^2 \Gamma(T X)$ such that for all functions $f,g \in C^\infty(X)$ the [[Poisson bracket]] is given by the [[Schouten bracket]] $[-,-]$ as 

$$
  \{f,g\} = [[\pi, f],g]
  \,.
$$

This $\pi$ is called the **Poisson tensor** or **Poisson bivector** of $(X, \{-,-\})$.

Every bivector $\pi$ such that $[\pi, \pi] = 0$ in the [[Schouten bracket]] arises this way.

## In terms of Lie algebroids

The Poisson tensor constitutes the [[anchor map]] of the [[Poisson Lie algebroid]] $\mathfrak{P}$ which corresponds to the [[Poisson manifold]].

Regarded as an element in the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P}) \simeq (\wedge^\bullet \Gamma(T X), [\pi,-])$,  the Poisson tensor also constitutes the canonical [[Lie algebroid cocycle]] on $\mathfrak{p}$ which is in [[transgression]] with the canonical [[invariant polynomial]] on $\mathfrak{P}$, the one that exhibits $\mathfrak{P}$ as a [[symplectic Lie n-algebroid|symplectic Lie 1-algebroid]].

## Related concepts

* [[deformation quantization]]

  * [[Moyal quantization]]


[[!redirects Poisson tensors]]
[[!redirects Poisson bivector]]
[[!redirects Poisson bivectors]]


