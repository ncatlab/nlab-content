

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[quantum electrodynamics]] the [[interaction]] between the [[Dirac field]] $\Psi$, whose [[quanta]] are [[electrons]], and the [[electromagnetic field]] $A$, whose [[quanta]] are [[photons]], is encoded by the [[interaction]] [[Lagrangian density]]

$$
  \mathbf{L}_{int}
  \;=\;
  i (\Gamma^\mu)^\alpha{}_\beta
  \overline{\psi}_\alpha \psi^\beta a^\mu
  \,
  dvol_\Sigma
$$

(with notation as as used at _[[A first idea of quantum field theory]]_).


For $g_{sw} \in C^\infty_{cp}(\Sigma)$ a [[bump function]] on [[spacetime]] thought of as an [[adiabatic switching|adiabatically switched]] [[coupling constant]], the corresponding [[interaction]] [[action functional]] is the [[local observable]]

$$
  \begin{aligned}
    S_{int}
    & \coloneqq
    i
    \underset{\Sigma}{\int}
      g_{sw}(x)
      \,
      (\Gamma^\mu)^\alpha{}_\beta
      \,
      \overline{\mathbf{\Psi}}_\alpha(x)
      \cdot
      \mathbf{\Psi}^\beta(x)
      \cdot
      \mathbf{A}_\mu(x)
      \,
     dvol_\Sigma(x)
     \\
     & =
    i
    \underset{\Sigma}{\int}
      g_{sw}(x)
      \,
      (\Gamma^\mu)^\alpha{}_\beta
      \,
      :
      \overline{\mathbf{\Psi}}_\alpha(x)
      \mathbf{\Psi}^\beta(x)
      \mathbf{A}_\mu(x)
      :
      \,
     dvol_\Sigma(x)
  \end{aligned}
  \,,
$$


where in the first line we have the [[integral]] over a pointwise product ([this def.](A+first+idea+of+quantum+field+theory#Observable)) of three [[field observables]] ([this def.](A+first+idea+of+quantum+field+theory#PointEvaluationObservables)), which in the second line we write equivalently as a [[normal ordered product]], by the discusssion at _[[Wick algebra]]_ ([this def.](Wick+algebra#NormalOrderedProductNotation)).


(e.g. [Scharf 95, (3.3.1)](#Scharf95))

The corresponding [[Feynman diagram]] is

<img src="https://ncatlab.org/nlab/files/InteractionVertexOfQED.jpg" width="200">

The square of the [[coupling constant]]

$$
  \alpha \coloneqq \tfrac{1}{4 \pi} g^2
$$

is called the _[[fine structure constant]]_.



## Related concepts

* [[Lamb shift]]

* [[phi^n interaction]]

## References

Discussion in the context of [[causal perturbation theory]] is in 

* {#Scharf95} [[Günter Scharf]], section 3.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition


[[!redirects electron-photon interactions]]

[[!redirects electron-photon vertex]]
[[!redirects electron-photon vertices]]
