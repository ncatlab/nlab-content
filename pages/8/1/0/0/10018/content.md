
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the [[path integral quantization]] formulation of [[quantum field theory]] the [[correlation functions]] ([[expectation values]]) are schematically [[path integrals]] of the form

$$
  \langle \phi(x_1) \cdots \phi(x_n)\rangle
  \coloneqq
  \frac{
    \int [D\phi] \,\phi(x_1) \cdots \phi(x_n) \, \exp\left(i S\left(\phi\right)\right)
  }{
    \int [D\phi]\,\exp\left(i S\left(\phi\right)\right)
  }
  \,.
$$

Therefore, as for ordinary [[moments]] (and explicitly so under [[Wick rotation]], if possible), there is [[generating functional]] for the correlators of the schematic form

$$
  \Psi(J)
  =
  \int [D \phi] \, \exp\left(i S\left(\phi\right) + i \int_X J \phi d\mu\right)
  \,.
$$

Here in the exponent one may regard 

$$
  S'(\phi,J) = S(\phi) + \int_X J \phi d\mu
$$

as a new [[action functional]] defined on a larger space of [[field (physics)|fields]] that also contains the parameters $J$ as fields. In this context one calls $J$ a **source field**.

This is in the corresponding [[equations of motion]] of $S'$ $J$ will act like a source term. The [[Euler-Lagrange equations]] for the modified action are:

$$
  EL(S') = EL(S) + J = 0
  \,.
$$

Notably if $EL(S)$ is a homogeneous [[wave equation]] (as for a [[free field theory]]) then $J$ is the inhomogeneous term in such a wave equation which describes indeed a "source" of wave excitations. 

## Related concepts

[[!include holographic principle -- table]]
[[!redirects source fields]]