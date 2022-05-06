
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Chern-Weil theory
+-- {: .hide}
[[!include infinity-Chern-Weil theory - contents]]
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

By the [[Nahm transform]], the [[moduli space]] of time-translation invariant [[self-dual Yang-Mills theory]] [[solitons]] on 4d [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ is equivalently the space of solutions to the [[Bogomolny equations]] on 3d [[Euclidean space]], which in turn may be thought of as [[magnetic monopoles]] in 3d [[Euclidean field theory|Euclidean]] [[Yang-Mills theory]] coupled to a charged [[scalar field]] (a "[[Higgs field]]"). Therefore this moduli space is traditionally referred to simply as the _moduli space of magnetic monopoles_ (e.g. [Atiyah-Hitchin 88](#AtiyahHitchin88)) or just the _moduli space of monopoles_.

## Definition

The moduli space 

\[
  \label{ModuliSpaceOfkInstantons}
  \mathcal{M}_k
  \;\coloneqq\;
  \cdots
\]

of $k$ monopoles is ... ([Atiyah-Hitchin 88, p. 15-16](#AtiyahHitchin88)).

## Properties

### Scattering amplitudes of monopoles
 {#ScatteringAmplitudesofMonopoles}

Write

\[
  \label{SpaceOfRationalFunctionsOfDegreek}
  R_k
  \;\subset\;
  RationalFunctions\big( \mathbb{C}P^1, \mathbb{C}P^1 \big)
  \;\subset\;
  Maps^{\ast/}\big( S^2, S^2 \big)
\]

for the [[space of maps|space of]] [[pointed topological space|pointed]] [[rational functions]] from the [[Riemann sphere]] to itself, of [[degree of a continuous function|degree]] $k \in \mathbb{N}$, inside the full [[Cohomotopy]] [[cocycle space]]. The [[homotopy type]] of $R_k$ is discussed in [Segal 79](#Segal79).

To each configuration $ c \in \mathcal{M}_k$ of $k \in \mathbb{N}$ magnetic monopoles is associated a [[scattering amplitude]] 

$$
  S(c) \in R_k
$$

([Atiyah-Hitchin 88 (2.8)](#AtiyahHitchin88))

This assignment is in fact a [[diffeomorphism]]

$$
  \mathcal{M}_k
  \overset{ S }{\longrightarrow}
  R_k
$$

from the moduli space (eq:ModuliSpaceOfkInstantons) of $k$ magnetic monopoles to the space (eq:SpaceOfRationalFunctionsOfDegreek) of rational functions of degree $k$.

([Atiyah-Hitchin 88, Theorem 2.10](#AtiyahHitchin88))

## Related concepts

* [[Nahm transform]], [[Bogomolny equation]]

[[!include moduli spaces -- contents]]


## References

### General

* {#AtiyahHitchin88} [[Michael Atiyah]], [[Nigel Hitchin]], _The geometry and dynamics of magnetic monopoles_  M. B. Porter Lectures. Princeton University Press, Princeton, NJ, 1988 ([jstor:j.ctt7zv206](https://www.jstor.org/stable/j.ctt7zv206))

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))

### In string theory

The moduli space of monopoles appears in the [[KK-compactification]] of the [[M5-brane]] on a complex surface ([[AGT-correspondence]]):

* Benjamin Assel, Sakura Schafer-Nameki, Jin-Mann Wong, _M5-branes on $S^2 \times M_4$: Nahm's Equations and 4d Topological Sigma-models_, J. High Energ. Phys. (2016) 2016: 120 ([arxiv:1604.03606](https://arxiv.org/abs/1604.03606))

[[!redirects moduli spaces of monopoles]]