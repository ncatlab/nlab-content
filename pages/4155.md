
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### AQFT and operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##

This page is about the modular theory introduced by Tomita for [[von Neumann-algebras]]. It is important both for the structure theory of von Neumann-algebras and in the [[Haag-Kastler approach]] to [[AQFT]], one important example is the [[Bisognano-Wichmann theorem]]. It is often called Tomita-Takesaki theory, because the first presentation beyond a preprint is due to [[Masamichi Takesaki]]. 

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

## References

### General

An introduction into Tomita-Takesaki modular theory is here:

* Stephen J. Summers: "Tomita-Takesaki Modular Theory" ([arXiv] (http://xxx.uni-augsburg.de/abs/math-ph/0511034))

...while a paper that puts it to serious work is this:

* H.J. Borchers: "On Revolutionizing of Quantum Field Theory
with Tomita's Modular Theory", ([ESI preprint page] (http://www.esi.ac.at/preprints/ESI-Preprints.html))


Many textbooks on operator algebras contain a chapter about modular theory.

MathOverflow question [tomita-takesaki-versus-frobenius-where-is-the-similarity](http://mathoverflow.net/questions/68270/tomita-takesaki-versus-frobenuis-where-is-the-similarity)

* [[Alain Connes]], [[Carlo Rovelli]], _Von Neumann algebra automorphisms and time-thermodynamics relation in general covariant quantum theories_, [arXiv:gr-qc/9406019](http://arxiv.org/abs/gr-qc/9406019), [pdf](http://www.alainconnes.org/docs/carlotime.pdf)

Discussion in terms of [[topos theory]] is in 

* {#Henry14} [[Simon Henry]], _From toposes to non-commutative geometry through the study of internal Hilbert spaces_, 2014  ([pdf](http://www.math.jussieu.fr/~henrys/Thesis.pdf))


See also

* Wikipedia, _[Tomita–Takesaki theory](https://en.wikipedia.org/wiki/Tomita%E2%80%93Takesaki_theory)_


### Modular flow

On [[Tomita-Takesaki modular flow]] as emergent [[time]] evolution in [[quantum physics]] ([[AQFT]]):

* {#Longo19} [[Roberto Longo]], _The emergence of time_ ([arxiv:1910.13926](https://arxiv.org/abs/1910.13926))


[[!redirects modular conjugation]]
[[!redirects modular conjugations]]
[[!redirects modular flow]]

[[!redirects Tomita theory]]
[[!redirects Tomita modular theory]]
[[!redirects Tomita modular flow]]

[[!redirects Tomita-Takesaki theory]]
[[!redirects Tomita-Takesaki modular theory]]
[[!redirects Tomita-Takesaki modular flow]]

[[!redirects Tomita–Takesaki theory]]
[[!redirects Tomita–Takesaki modular theory]]
[[!redirects Tomita–Takesaki modular flow]]
