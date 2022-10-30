

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


Over a [[smooth manifold]] $\Sigma$ of [[dimension]] $p+1$, let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] and $\tilde E^\ast \coloneqq E^\ast \otimes_{\Sigma} \wedge_\Sigma^{p+1} T^\ast \Sigma$ the [[tensor product of vector bundles]] of the [[dual vector bundle]] with the [[differential n-form|differential (p+1)-form bundle]].

+-- {: .num_defn #FormallyAdjointDifferentialOperators}
###### Definition
**(formally adjoint differential operators)**

Two [[differential operators]]

$$
  P, P^\ast
   \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \Gamma_\Sigma(\tilde E^\ast)
$$

are called _formally adjoint_ if there exists a [[bilinear map|bilinear]] [[differential operator]]

$$
  \label{FormallyAdjointDifferentialOperatorWitness}
  K \;\colon\;
  \Gamma_\Sigma(E) \otimes \Gamma_\Sigma(E)
    \longrightarrow
   \Gamma_\Sigma(\wedge^{p} T^\ast \Sigma)
$$

such that for all $\Phi_1, \Phi_2 \in \Gamma_\Sigma(E)$ we have

$$
  P(\Phi_1) \cdot \Phi_2
  -
  \Phi_1 \cdot P^\ast(\Phi_2)
   \;=\;
  d K(\Phi_1, \Phi_2)
$$

=--

([Khavkine 14, def. 2.4](#Khavkine14))

See also ([Vinogradov-Krasilshchik 99, chapter 5, &#167;2.3](#VinogradovKrasilshchik99))

## Examples
 {#Examples}


+-- {: .num_example #FormallySelfAdjointKleinGordonOperator}
###### Example
**([[Klein-Gordon operator]] is formally self-adjoint )**

Let $\Sigma = \mathbb{R}^{p,1}$ be [[Minkowski spacetime]] with [[Minkowski metric]] $\eta$ and let $E \coloneqq \Sigma \times \mathbb{R}$ be the [[trivial line bundle]]. The canonical [[volume form]] $dvol_\Sigma$ induces an [[isomorphism]] $\tilde E^\ast \simeq E$.

Consider then the [[Klein-Gordon operator]]

$$
  (\Box - m^2)
    \;\colon\; 
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
     \longrightarrow
  \Gamma_\Sigma(\Sigma \times \mathbb{R}) \otimes \langle dvol_\Sigma\rangle
  \,.
$$

This is its own formal adjoint (def. \ref{FormallyAdjointDifferentialOperators}) witnessed by the bilinear differential operator (eq:FormallyAdjointDifferentialOperatorWitness) given by

$$
  K(\Phi_1, \Phi_2)
  \;\coloneqq\;
  \left(
    \frac{\partial \Phi_1}{\partial x^\mu} \Phi_2
    -
    \Phi_1 \frac{\partial \Phi_2}{\partial x^\mu}
  \right)
  \eta^{\mu \nu}\iota_{\partial_\nu} dvol_\Sigma
  \,.
$$

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    d K(\Phi_1, \Phi_2)
    & =
    d
    \left(
      \frac{\partial \Phi_1}{\partial x^\mu} \Phi_2
      -
      \Phi_1 \frac{\partial \Phi_2}{\partial x^\mu}
    \right)
    \eta^{\mu \nu}\iota_{\partial_\nu} dvol_\Sigma
    \\
    &=
    \left(
    \left(
      \eta^{\mu \nu}\frac{\partial^2 \Phi_1}{\partial x^\mu \partial x^\nu} \Phi_2
      + 
      \eta^{\mu \nu} \frac{\partial \Phi_1}{\partial x^\mu} \frac{\partial \Phi_2}{\partial x^\nu}
    \right)
    -
    \left(
      \eta^{\mu \nu}
      \frac{\partial \Phi_1}{\partial x^\nu} \frac{\partial \Phi_2}{\partial x^\mu}  
      + 
      \Phi_1 \eta^{\mu \nu} \frac{\partial^2 \Phi_2}{\partial x^\nu \partial x^\mu}
    \right)
    \right)
    dvol_\Sigma
    \\
    & =
    \left(
      \eta^{\mu \nu}\frac{\partial^2 \Phi_1}{\partial x^\mu \partial x^\nu} \Phi_2
      -
      \Phi_1 \eta^{\mu \nu} \frac{\partial^2 \Phi_2}{\partial x^\nu \partial x^\mu}
    \right)
    dvol_\Sigma    
    \\
    & =
    \Box(\Phi_1) \Phi_2 - \Phi_1 \Box (\Phi_2)
  \end{aligned}
$$

=--

## Related concepts

* [[generalized solution of a differential equation]]

* [[Green hyperbolic differential operator]]

## References

* {#VinogradovKrasilshchik99} [[Alexandre Vinogradov]], I. S. Krasilshchik (eds.) _Symmetries and Conservation Laws for Differential Equations of Mathematical Physics_, vol. 182 of Translations of Mathematical Monographs. American Mathematical Society, Providence, RI, 1999. ([pdf](ftp://softbank.iust.ac.ir/MathBooks/V/Vinogradov%20-%20Symmetries%20and%20Conservation%20Laws%20for%20Differential%20equations%20of%20mathematical%20physics.pdf))


* {#Khavkine14} [[Igor Khavkine]], _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv:1402.1282](https://arxiv.org/abs/1402.1282))


[[!redirects formal adjoint differential operators]]

[[!redirects formally adjoint differential operator]]
[[!redirects formally adjoint differential operators]]