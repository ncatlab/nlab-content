
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


For $X$ a [[smooth manifold]] and $T^* X \to X$ its [[cotangent bundle]], there is a unique [[differential 1-form]] on $T^* X$ itself, 

$$
  \theta
   \in
  \Omega^1(T^* X)
$$

with the property that under the [[isomorphism]]

$$
  j \;\colon\; \Gamma(T^* X) \stackrel{\simeq}{\to} \Omega^1(X)
$$

between [[differential 1-forms]] and smooth [[sections]] of the [[cotangent bundle]] we have for every smooth section $\sigma \in \Gamma(T^* X)$ the identification

$$
  \sigma^* \theta = j(\sigma)
$$

between the [[pullback of a differential form|pullback]] of $\theta$ along $\sigma$ and the 1-form corresponding to $\sigma$ under $j$.

This unique differential 1-form $\theta \in \Omega^1(T^* X)$ is called the **Liouville form** or **Poincar&#233; 1-form** or **canonical form** or **tautological form** on the cotangent bundle.

The [[de Rham differential]] $\omega \coloneqq d \theta$ is a [[symplectic form]]. Hence every [[cotangent bundle]] is canonically a [[symplectic manifold]].

On a [[coordinate chart]] $\mathbb{R}^n$ of $X$ with canonical [[coordinate functions]] denoted $(x^i)$, the cotangent bundle over the chart is $T^\ast \mathbb{R}^n \simeq \mathbb{R}^n \times \mathbb{R}^n$ with canonical coordinates $((x^i), (p_j))$. In these coordinates the canonical 1-form is (using [[Einstein summation convention]])

$$
  \theta = p_i d x^i
$$

and hence the [[symplectic form]] is 

$$
  \omega = d p_i \wedge d q^i
  \,.
$$


 

## Related concepts

* [[Maurer-Cartan form]]

* [[Euler vector field]]

[[!redirects Liouville 1-form]]
[[!redirects Poincaré 1-form]]
[[!redirects Poincare 1-form]]

[[!redirects Poincaré form]]
[[!redirects Poincare form]]


[[!redirects Liouville-Poincare 1-form]]

