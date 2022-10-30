
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A basic characteristic of [[physics]] in the context of [[special relativity]] and [[general relativity]] is that causal influences on a [[Lorentzian manifold]] [[spacetime]] propagate in [[timelike]] or [[lightlike]] directions but not [[spacelike]].

The fact that any two spacelike-separated regions of spacetime thus behave like [independent subsystems](http://ncatlab.org/nlab/show/quantum+mechanics#Subsystems) is called **causal locality** or, with a slightly stronger technical definition, **Einstein causality**.

(One sometimes sees a further criterion to causality, that the causal influences in timelike and lightlike directions only propagate into the [[future]], but this is not so simply dealt with; it probably only makes sense as a statement about coarse-grained [[entropy]] in [[statistical physics]].)

For a formalization of this idea see for instance

* [[local quantum field theory]]

* [[local prequantum field theory]]

* [[local net of observables]]

Under [[Wick rotation]], causal locality becomes "[[statistical locality]]"  (see _[[Osterwalder-Schrader theorem]]_).

## Microcausality
 {#Microcausality}

From ([Grigor'ev 197x](#Grigoriev)):

> Microcausality condition

> a requirement that the causality condition (which states that cause must precede effect) be satisfied down to an arbitrarily small distance and time interval. The microcausality condition usually refers to distances &#8818; $10^{-16}$ [[meter|cm]] and to times &#8818; $10^{-24}$ [[second|sec]].

> It is shown in the theory of [[special relativity|relativity]] that the assumption of the existence of physical signals that propagate with a velocity greater than the velocity of [[light]] leads to violation of the causality requirement. Thus, the microcausality condition prohibits the propagation of signals at a velocity greater than the velocity of [[light]] "in the small".

> In [[quantum physics|quantum theory]], where [[quantum operator|operators]] correspond to physical quantities, the microcausality condition requires the interchangeability of any operators that pertain to two points of [[space-time]] if these points cannot be linked by a light signal. This interchangeability means that the physical quantities to which these operators correspond can be precisely determined independently and simultaneously. The microcausality condition is important in [[quantum field theory]], especially in the dispersion and [[AQFT|axiomatic approaches]]; these approaches are not based on specific [[model (physics)|model]] concepts of interaction and therefore can be used for direct verification of the microcausality condition. In the most highly developed branch of [[quantum field theory]] &#8212; [[quantum electrodynamics]] &#8212; the microcausality condition has been experimentally verified for distances &#8818; $10^{-15}$ cm (and, correspondingly, for times &#8818; $10^{-25}$ sec).

> The violation of the microcausality condition would make it necessary to radically alter the method of describing physical processes and to reject the dynamic description used in modern theories, in which the state of a physical system at a given moment of time (the effect) is determined by the states of the system at preceding times (the cause).

Notice that $10^{-15}$[[cm]] $ = 10^{-17}m  = 10^{-2}$[[fm]] and that the (charge) [[radius]] of the [[proton]] is about 0.8 [[fm]]. So the bound cited by ([Grigor'ev 197x](#Grigoriev)) in the above quote is about 1/100 the diameter of a proton.

It seems that [Grigor'ev 197x](#Grigoriev) just cited the length scale resolution of particle accelerators at that time. More recently, the [[LHC]] (see there) probes scales $\simeq 10^{-20}m$.

## In S-matrix theories and string theory

In [[S-matrix]] theories causality is meant to be incarnated in terms of [[analytic function|analyticity]] properties of the [[scattering amplitudes]] (for this reason one often speaks of "the analytic S-matrix").

One S-matrix theory is [[perturbative string theory]]. Discussion of causality in string theory includes [Martinec 95](#Martinec95) and ([Erler-Gross 04](#ErlerGross04)). The latter write in their introduction:

> Perhaps then it comes as a surprise that critical string theory produces an analytic [[S-matrix]] consistent with macroscopic causality. In absence of any other known theoretical mechanism which might explain this, despite appearances one is lead to believe that string interactions must be, in some sense, local.

and

> We find that string theory avoids problems with nonlocality in a surprising way. In particular, we find that the Witten vertex is "local enough" to allow for a nonsingular description of the theory which is completely local along a single null direction.

and

> unlike lightcone string field theory, it is clear that cubic string field theory at least has a local limit where all spacetime coordinates are taken to the midpoint. We investigate this limit with a careful choice of regulator and show that at any stage the theory is nonsingular but arbitrarily close to being local and manifestly causal. We believe that the existence of this limit, though singular, must account for the macroscopic causality of the string S-matrix. Thus, string theory is local enough to avoid the inconsistencies of a theory which is acausal and nonlocal in time, but is nonlocal enough to make string theory different from quantum field theory

Then they comment on Martinec's account above, and other's, by saying:

> To motivate our particular perspective, it seems appropriate to discuss earlier attempts to understand the role of locality, causality and time in string theory, and explain why we feel these approaches do not adequately address the problems just raised.

## Related concepts

* [[local prequantum field theory]]

* [[local quantum field theory]]

* [[causal structure]]

* in [[FQFT]]: 

  [[extended field theory]]

* in [[AQFT]]: 

  [[local net of observables]], [[Haag-Kastler axioms]]

## References

* V. I. Grigor'ev, _Microcausality condition_, The Great Soviet Encyclopedia, 3rd Edition (1970-1979) ([web](http://encyclopedia2.thefreedictionary.com/Microcausality+Condition))
 {#Grigoriev}

* Jessey Wright, _Quantum field theory: Motivating  the Axiom of Micorcausality_, PhD thesis 2012 ([pdf](http://uwspace.uwaterloo.ca/bitstream/10012/6998/1/Wright_Jessey.pdf))

* Anthony Duncan, _The Conceptual Framework of Quantum Field Theory -- Dynamics IV: Aspects of locality: clustering, microcausality, and analyticity_, Oxford Scholarship Online ([web](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199573264.001.0001/acprof-9780199573264-chapter-6))

* [[John Bell]], _The theory of local beables_ (1975) ([pdf](http://cds.cern.ch/record/980036/files/197508125.pdf))
 {#Bell75}


* [pdf](http://ptp.oxfordjournals.org/content/52/1/335.full.pdf)

Discussion in theories with [[higher curvature corrections]] of the gravitational background and in [[string theory]] includes

* Xian O. Camanho, Jose D. Edelstein, [[Juan Maldacena]], Alexander Zhiboedov, _Causality Constraints on Corrections to the Graviton Three-Point Coupling_ ([arXiv:](http://arxiv.org/abs/1407.5597))

* Giuseppe D'Appollonio, [[Paolo Di Vecchia]], [[Rodolfo Russo]], [[Gabriele Veneziano]], _Regge behavior saves String Theory from causality violations_ ([arXiv:1502.01254](http://arxiv.org/abs/1502.01254))

Discussion of causality in [[string theory]] includes

* {#Martinec95} [[Emil Martinec]], _Strings and Causality_ ([pdf](cds.cern.ch/record/569030/files/9311129.pdf)) in L. Baulieu, V.  Dotsenko, V. Kazakov, P. Windey (eds.) Quantum Field Theory and String Theory , NATO ASI Series B: Physics Vol. 328 (1995)

which is a short commented analysis of the string 2-point function as compared to the particle 2-point function and in view of how causality is read off. In the course martinec referes to string fiels, somewhat colloquially.

* {#ErlerGross04} [[Theodore Erler]], [[David Gross]], _Locality, Causality, and an Initial Value Formulation for Open String Field Theory_ ([arXiv:hep-th/0406199](https://arxiv.org/abs/hep-th/0406199))


[[!redirects causal locality]]

[[!redirects Einstein causality]]
[[!redirects Einstein-causality]]

[[!redirects Einstein locality]]
[[!redirects Einstein-locality]]

[[!redirects microlocality]]
[[!redirects microcausality]]

[[!redirects locality]]

[[!redirects causality]]
