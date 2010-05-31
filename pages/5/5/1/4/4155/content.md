
<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
This page is about the modular theory introduced by Tomita for [[von Neumann-algebra]]s. It is important both for the structure theory of von Neumann-algebras and in the [[Haag-Kastler approach]] to [[AQFT]], one important example is the [[Bisognano-Wichmann theorem]]. It is often called Tomita-Takesaki theory, because the first presentation beyond a preprint is due to Takesaki. 

## Definition ##
Let $\mathcal{H}$ be a [[Hilbert space]], $\mathcal{M}$ a [[von Neumann-algebra]] with commutant $\mathcal{M}'$ and a separating and cyclic vector $\Omega$. Then there is a **modular operator** $\Delta$ and a **modular conjugation** $J$ such that:

1. $\Delta$ is self-adjoint, positive and invertible (but not bounded).

2. $\Delta\Omega = \Omega$ and $ J\Omega = \Omega$

3. $J$ is antilinear, $J^* = J, J^2 = \mathbb{1}$, $J$ commutes with $\Delta^{it}$. This implies
$$
Ad(J) \Delta = \Delta^{-1}
$$

4. For every $A \in \mathcal{M}$ the vector $A\Omega$ is in the domain of $\Delta^{\frac{1}{2}}$ and
$$
J \Delta^{\frac{1}{2}} A \Omega = A^* \Omega =: SA \Omega
$$

5. The unitary group $\Delta^{it}$ defines a group automorphism of $\mathcal{M}$:
$$
Ad(\Delta^{it}) \mathcal{M} = \mathcal{M} \; \; \text{for all} \; t \in \mathbb{R} 
$$

6. $J$ maps $\mathcal{M}$ to $\mathcal{M}'$.

## References ##

Many textbooks on operator algebras contain a chapter about modular theory.

[[!redirects modular group]]
[[!redirects modular groups]]
[[!redirects modular conjugation]]
[[!redirects modular conjugations]]
[[!redirects Tomita theory]]
[[!redirects Tomita-Takesaki theory]]