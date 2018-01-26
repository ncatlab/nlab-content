

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

In the construction of [[interacting field theory|interacting]] [[perturbative quantum field theory]] the specification of 

1. the [[gauge fixing|gauge-fixed]] [[free field theory|free field]] [[vacuum]] $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ that the [[perturbation theory|perturbation]] is about ([this def.](S-matrix#VacuumFree));

1. the [[local observable|local]] [[interaction]] [[action functional]] $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g\rangle $ which prescribes the nature of the perturbation ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering))

still leaves, in general, a [[countable set]] of [[finite dimensional vector space|finite dimensional]] [[affine spaces]] of choices $\{c^\alpha_k \in \mathbb{C}\}_{k \in \mathbb{n}}$ to fully specify the corresponding [[interacting field theory|interacting]] [[perturbative QFT]] ([this prop.](renormalization#RenormalizationChoices)). This is called the choice of _[[renormalization|("re"-)normalization]]_ constants of the [[perturbative QFT]].

One says that the interaction $g S_{int}$ is _renormalizable_ if this potentially countably infinite dimensional space of choices happens to be a finite dimensional space, hence if there is $n \in \mathbb{N}$ such that the only available choice is $c^\alpha_k = 0$ for all $k \geq n$. Otherwise one says that $g S_{int}$ is _non-renromalizable_.

(If only a [[finite set]] of [[Feynman diagrams]] contributes to the ("re"-)normalization choices to be made for a renormaliable interaction, then it is called _super-renormalizable_).

## Interpretation

Beware that this terminology has its pitfalls: The [[main theorem of perturbative renormalization]] says, among other things, that for _all_ (translation invariant) perturbative QFTs there do exist constructions of [[time-ordered products]] on the diagonal, hence of [[renormalization|("re"-)normalizations]], hence of choices of these $c_k^\alpha$; even if there are (countably) infinitely many. 

Therefore the issue expressed with the term "non-renormalizable" at this point is not a mathematical [[obstruction]], but a philosophical sentiment: The need to specify an infinite set of further physical constants to specify a [[theory (physics)|physical theory]] is (or has been) felt to defeat the purpose or meaning of having specified a [[theory (physics)|physical theory]]. 

But in practice this is less of a problem than it might seem: By the [[Gell-Mann-Low renormalization cocycle]] the higher the order of the renormalization constants, the higher the [[energy]]/the smaller the [[wavelength]] at which their effect is visible in [[experiment]]. Hence in _practice_ only a finite number of renormalization constants is observable anyway. As the energy/resolution of an experiment is increased by a finite amount, a finite number of further renormalization constants may become visible.

For famous "non-renormalizable" theories such as [[perturbative quantum gravity]] the first such corrections would become visible to [[experiment]] only at energies way beyond current reach, so that for all practical purpose the construction of "non-renormalizable" [[perturbative QFTs]] such as [[perturbative quantum gravity]] via [[renormalization|("re"-)normalization]] does exist ([Scharf 01, chapter 5](#Scharf01)). (A wide-open problem is, instead, the construction of [[interacting field theory|interacting]] [[non-perturbative quantum field theories]] for [[spacetime]] [[dimension]] $\geq 3+1$.)

It has become popular to think of such "non-renormalizable" [[perturbative QFTs]] as "[[effective field theories]]". See there for more.

## Examples

* [[Yang-Mills theory]] (...condition on gauge group...) hence [[QCD]] is renormalizable (t'Hooft, ...)

* [[Einstein gravity]] is non-renormalizable ([Goroff-Sagnotti 85](quantum+gravity#GoroffSagnotti85), [van de Ven 92](#vandeVen92))


## References

Discussion in the rigorous context of [[causal perturbation theory]]/[[pAQFT]] is in 

* {#Scharf95} [[Günter Scharf]], p. 271 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001


See also 

* Wikipedia, _[Renormalizability](https://en.wikipedia.org/wiki/Renormalization#Renormalizability)_

[[!redirects renormalizable interactions]]

[[!redirects renormalizable perturbative QFT]]
[[!redirects renormalizable perturbative QFTs]]

[[!redirects renormalizable QFT]]
[[!redirects renormalizable QFTs]]

[[!redirects non-renormalizable pertrubative QFT]]
[[!redirects non-renormalizable perturbative QFTs]]

[[!redirects non-renormalizable QFT]]
[[!redirects non-renormalizable QFTs]]
