
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[tensor product of representations|tensor product]] $\rho_{j_1} \otimes \rho_{j_2}$ of two [[representations]] of some [[Lie group]] $G$ (by default often the [[special orthogonal group]] $SO(3)$) and given its decomposition into a [[direct sum]] of [[irreducible representations]] $\{\rho_{t_{tot}}\}$ by an [[isomorphism]]

$$
  \rho_{j_1} \otimes \rho_{j_2} \stackrel{\simeq}{\longrightarrow} \underset{j_{tot}}{\oplus} C_{j_1 j_2}{}^{j_{tot}} \rho_{j_{tot}}
$$

then the [[matrix]] elements of this [[linear map]] in some standard [[basis]] are called -- in the [[physics]] literature -- the _Clebsch-Gordan coefficients_ or equivalently (up to a constant) the _Wigner 3j symbols_ .

Specifically for $G = SO(3)$ the [[rotation group]] in 3-dimensional [[Cartesian space]], then the standard [[basis]] elements of the [[representation]] $\rho_{j}$ of total [[angular momentum]] $j \in \mathbb{N}$ are traditionally denoted

$$
  |j,m\rangle \in \rho_{j}
  \;\;\,,\;\;
  -j \leq m \leq j
$$

and their [[inner product]] is traditionally denoted by

$$
  \langle j_1, m_1 | j_2, m_2\rangle
  \in
  \mathbb{C}
  \,.
$$

In these basis elements that above [[matrix]] then has components given by

$$
  \langle (j_1, m_1)\otimes(j_2,m_2) | j_{tot}, m_{tot}\rangle
  \in
  \mathbb{C}
  \,.
$$

These expressions are specifically the _Clebsch-Gordan coefficients_ as they appear in the physics literature.

## Related concepts

* [[Wigner 6-j symbol]]

* [[Wigner 9-j symbol]]

* [[Fierz identity]]

* [[fusion ring]]

## References

Lecture notes include for instance

* M. Tuckerman, _Quantum mechanics and dynamics -- Addition of angular momenta -- [The general problem](http://www.nyu.edu/classes/tuckerman/quant.mech/lectures/lecture_8/node2.html))_

[[!redirects Clebsch-Gordan coefficients]]

[[!redirects 3j symbol]]
[[!redirects 3j symbols]]
[[!redirects 3-j symbol]]
[[!redirects 3-j symbols]]

[[!redirects Wigner 3j symbol]]
[[!redirects Wigner 3j symbols]]
[[!redirects Wigner 3-j symbol]]
[[!redirects Wigner 3-j symbols]]
