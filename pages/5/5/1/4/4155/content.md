
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

## nPOV definition

The modern approach to defining the modular automorphism group
is through the theory of noncommutative [[L_p-spaces]].
This was pioneered by [Haagerup in 1979](#Haagerup) and [Yamagami in 1992](#Yamagami).

In this approach,
given a [[von Neumann algebra]] $M$, a faithful semifinite normal [[weight]] $\mu$ on $M$, and an [[imaginary number]] $t$,
the modular automorphism associated to $M$, $\mu$, and $t$ is
$$\sigma_\mu^t\colon M\to M,\qquad m\mapsto \mu^t m \mu^{-t}.$$

This approach makes it easy to deduce various properties of the modular automorphism group.

For more details, see a [MathOverflow answer](https://mathoverflow.net/questions/386464/making-sense-of-every-non-commutative-algebra-has-its-own-internal-time-evoluti/386481#386481).


## Traditional definition ##
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

* {#Haagerup} [[Uffe Haagerup]], [$L^p$-spaces associated with an arbitrary von Neumann algebra](https://dmitripavlov.org/haagerup.pdf).  Algèbres d'opérateurs et leurs applications en physique mathématique.  Colloques Internationaux du Centre National de la Recherche Scientifique 274, 175–184.

* {#Yamagami} [[Shigeru Yamagami]], _Algebraic aspects in modular theory_, Publications of the Research Institute for Mathematical Sciences 28:6 (1992), 1075-1106.  [doi](http://dx.doi.org/10.2977/prims/1195167738).

* [[Shigeru Yamagami]], _Modular theory for bimodules_, Journal of Functional Analysis 125:2 (1994), 327-357.  [doi](http://dx.doi.org/10.1006/jfan.1994.1127).

### General

Introduction:

* Stephen J. Summers: "Tomita-Takesaki Modular Theory" ([arXiv:math-ph/0511034](https://arxiv.org/abs/math-ph/0511034))

Role in [[algebraic quantum field theory]]:

* [[Hans-Jürgen Borchers]], *On Revolutionizing of Quantum Field Theory with Tomita's Modular Theory*, ESI Preprint 773 (1999) &lbrack;[pdf](https://www.mat.univie.ac.at/~esiprpr/esi773.pdf)&rbrack; 



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

Videos of lecture series on modular theory by [[Masamichi Takesaki]] and Serban Stratila:

* {#TTLectures} [Master Class in Modular Theory](https://www.youtube.com/playlist?list=PLhkiT_RYTEU1OTAqcn3FOQHnHbREAiZdz)

### Noncommutative Integration

A very detailed overview of modular flow, non-commutative $L_p$-spaces, etc. which includes many further references:

* {#Kostecki13} Ryszard Paweł Kostecki _$W^{*}$-algebras and noncommutative integration_ [arXiv:1307.4818](https://arxiv.org/abs/1307.4818)



[[!redirects modular conjugation]]
[[!redirects modular conjugations]]
[[!redirects modular flow]]
[[!redirects modular flows]]
[[!redirects modular automorphism]]
[[!redirects modular automorphisms]]
[[!redirects modular automorphism group]]
[[!redirects modular automorphism groups]]

[[!redirects Tomita theory]]
[[!redirects Tomita modular theory]]
[[!redirects Tomita modular flow]]

[[!redirects Tomita-Takesaki theory]]
[[!redirects Tomita-Takesaki modular theory]]
[[!redirects Tomita-Takesaki modular flow]]

[[!redirects Tomita–Takesaki theory]]
[[!redirects Tomita–Takesaki modular theory]]
[[!redirects Tomita–Takesaki modular flow]]
