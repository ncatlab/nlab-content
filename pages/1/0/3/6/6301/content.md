
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

From ([Grigor'ev 197x](#Grigoriev)):

> Microcausality condition

> a requirement that the causality condition (which states that cause must precede effect) be satisfied down to an arbitrarily small distance and time interval. The microcausality condition usually refers to distances &#8818; $10^{-16}$ [[meter|cm]] and to times &#8818; $10^{-24}$ [[second|sec]].

> It is shown in the theory of [[special relativity|relativity]] that the assumption of the existence of physical signals that propagate with a velocity greater than the velocity of [[light]] leads to violation of the causality requirement. Thus, the microcausality condition prohibits the propagation of signals at a velocity greater than the velocity of [[light]] "in the small".

> In [[quantum physics|quantum theory]], where [[quantum operator|operators]] correspond to physical quantities, the microcausality condition requires the interchangeability of any operators that pertain to two points of [[space-time]] if these points cannot be linked by a light signal. This interchangeability means that the physical quantities to which these operators correspond can be precisely determined independently and simultaneously. The microcausality condition is important in [[quantum field theory]], especially in the dispersion and [[AQFT|axiomatic approaches]]; these approaches are not based on specific [[model (physics)|model]] concepts of interaction and therefore can be used for direct verification of the microcausality condition. In the most highly developed branch of [[quantum field theory]] &#8212; [[quantum electrodynamics]] &#8212; the microcausality condition has been experimentally verified for distances &#8818; $10^{-15}$ cm (and, correspondingly, for times &#8818; $10^{-25}$ sec).

> The violation of the microcausality condition would make it necessary to radically alter the method of describing physical processes and to reject the dynamic description used in modern theories, in which the state of a physical system at a given moment of time (the effect) is determined by the states of the system at preceding times (the cause).

Notice that $10^{-15}$[[cm]] $ = 10^{-17}m  = 10^{-2}$[[fm]] and that the (charge) [[radius]] of the [[proton]] is about 0.8 [[fm]]. So the bound cited by ([Grigor'ev 197x](#Grigoriev)) in the above quote is about 1/100 the diameter of a proton.

It seems that [Grigor'ev 197x](#Grigoriev) just cited the length scale resolution of particle accelerators at that time. More recently, the [[LHC]] (see there) probes scales $\simeq 10^{-20}m$.


## In algebraic quantum field theory
  {#InAlgebraicQuantumFieldTheory}

In [[algebraic quantum field theory]] causal locality is formalized as follows. This is a key statement in the [[Haag-Kastler axioms]] on [[causally local nets of quantum observables]]:

+-- {: .num_defn #CausalLocalityOfAlgebrasOfObservables}
###### Definition
**(causal locality of algebras of observables)**

A [[co-presheaf]] of [[algebras of quantum observables]] $\mathcal{A}$ on some [[spacetime]] is _causally local_ if the algebras  $\mathcal{A}(\mathcal{O})$ localized in [[spacelike]] separated [[spacetime]] regions $\mathcal{O}$ commute with each other (inside any of the algebras of observables localized in the causal closure $\mathcal{O}$ of the union of the two spacetime regions). 

$$
  \left(
    \mathcal{O}_1 
     \;\text{spacelike separated from}
     \;
    \mathcal{O}2
  \right)
  \;\Rightarrow\;
  \left(
    [\mathcal{A}(\mathcal{O}_1), \mathcal{A}(\mathcal{O}_2)]
    \;=\;
    0
    \;\;\;\;
    \in \mathcal{A}( \mathcal{O} )
  \right)
  \,.
$$

=--

Under [[Wick rotation]], this causal locality becomes "statistical locality""  (see at _[[Osterwalder-Schrader theorem]]_).

In [[perturbative algebraic quantum field theory]] this condition follows from the [[causal additivity]] of the [[S-matrix]] (see there the section _[Causal locality and Quantum obsrvables](S-matrix#CausalLocality)_).

There are variants that one may consider:

+-- {: .num_defn #StrongLocality}
###### Definition
**(strong causal locality of algebras of observables)**

A [[local net of quantum observables]] is **strongly causally local** if it is causally local in that algebras $A_1 = A(O_1)$ and $A_2 = A(O_2)$ associated with  spacelike separated regions commute with each other, and in addition for all commutative subalgebras $C_1 \subset A_1$ and $C_2 \subset A_2$ the algebra $C_1 \vee C_2 \subset A(O_1 \vee O_2)$ satisfies

1. $(C_1 \vee C_2) \cap A_1 = C_1$

1. $(C_1 \vee C_2) \cap A_2 = C_2$.

=--

This is ([Nuiten 11, def. 14](#Nuiten11)).


There have been various proposals to understand these conditions from other principles: 

1. In ([Schreiber 09](#Schreiber09)) the condition \ref{CausalLocalityOfAlgebrasOfObservables} is related to [[n-functor|n-functoriality]] of a corresponding ([[Schrödinger picture]]) [[functorial quantum field theory]].

1. In ([Nuiten 11, theorem 4.2](#Nuiten11)) the condition \ref{StrongLocality} us shown to be implied by the associated pre-sheaf of [[Bohr toposes]] satisfying spatial [[descent]] by [[local geometric morphisms]].

1. In ([Brunetti-Fredenhagen-Imani-Rejzner 12](#BrunettiFredenhagenImaniRejzner12)) condition def. \ref{CausalLocalityOfAlgebrasOfObservables} is shown to be equivalent to the [[co-presheaf]] of observables being a [[monoidal functor]] is a suitable way.


## In S-matrix theories and string theory

In [[S-matrix]] theories [[causal additivity]] is meant to also be incarnated in terms of [[analytic function|analyticity]] properties of the [[scattering amplitudes]] (for this reason one often speaks of "the analytic S-matrix").

One S-matrix theory is [[perturbative string theory]]. Discussion of causality in string theory includes [Martinec 95](#Martinec95) and ([Erler-Gross 04](#ErlerGross04)). The latter write in their introduction:

> Perhaps then it comes as a surprise that critical string theory produces an analytic [[S-matrix]] consistent with macroscopic causality. In absence of any other known theoretical mechanism which might explain this, despite appearances one is lead to believe that string interactions must be, in some sense, local.

and

> We find that string theory avoids problems with nonlocality in a surprising way. In particular, we find that the Witten vertex is "local enough" to allow for a nonsingular description of the theory which is completely local along a single null direction.

and

> unlike lightcone string field theory, it is clear that cubic string field theory at least has a local limit where all spacetime coordinates are taken to the midpoint. We investigate this limit with a careful choice of regulator and show that at any stage the theory is nonsingular but arbitrarily close to being local and manifestly causal. We believe that the existence of this limit, though singular, must account for the macroscopic causality of the string S-matrix. Thus, string theory is local enough to avoid the inconsistencies of a theory which is acausal and nonlocal in time, but is nonlocal enough to make string theory different from quantum field theory

Then they comment on Martinec's account above, and other's, by saying:

> To motivate our particular perspective, it seems appropriate to discuss earlier attempts to understand the role of locality, causality and time in string theory, and explain why we feel these approaches do not adequately address the problems just raised.

## Related concepts

* [[causal structure]]

* [[causal additivity]]

* [[causal closure]]

* [[causal perturbation theory]]

* [[local prequantum field theory]]

* [[local quantum field theory]]

* in [[AQFT]]: 

  [[local net of observables]], [[Haag-Kastler axioms]]

* in [[FQFT]]: 

  [[extended field theory]]


## References

### In local quantum field theory

* {#Grigoriev} V. I. Grigor'ev, _Microcausality condition_, The Great Soviet Encyclopedia, 3rd Edition (1970-1979) ([web](http://encyclopedia2.thefreedictionary.com/Microcausality+Condition))
 
* Jessey Wright, _Quantum field theory: Motivating  the Axiom of Micorcausality_, PhD thesis 2012 ([pdf](http://uwspace.uwaterloo.ca/bitstream/10012/6998/1/Wright_Jessey.pdf))

* Anthony Duncan, _The Conceptual Framework of Quantum Field Theory -- Dynamics IV: Aspects of locality: clustering, microcausality, and analyticity_, Oxford Scholarship Online ([web](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199573264.001.0001/acprof-9780199573264-chapter-6))

* {#Bell75} [[John Bell]], _The theory of local beables_ (1975) ([pdf](http://cds.cern.ch/record/980036/files/197508125.pdf))

* [pdf](http://ptp.oxfordjournals.org/content/52/1/335.full.pdf)

### In algebraic quantum field theory

For references on the traditional discussion in [[AQFT]] see at _[[Haag-Kastler axioms]]_ and at _[[causally local net of observables]]_. Proposals to understand the causal locality axiom from other principles include


* {#Schreiber09} [[Urs Schreiber]], _AQFT from $n$-functorial QFT_ , Comm. Math. Phys., Volume 291, Issue 2, pp.357-401 2009 ([pdf](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf))


* {#Nuiten11} [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets]]_, Proceedings of [QPL 2011](http://qpl.science.ru.nl/), [EPTCS 95, 2012](http://rvg.web.cse.unsw.edu.au/eptcs/content.cgi?QPL2011), pp. 211-218
([arXiv:1109.1397](http://arxiv.org/abs/1109.1397))

* {#BrunettiFredenhagenImaniRejzner12} [[Romeo Brunetti]], [[Klaus Fredenhagen]], Paniz Imani, [[Katarzyna Rejzner]], _The Locality Axiom in Quantum Field Theory and Tensor Products of $C^*$-algebras_ ([arXiv:1206.5484](https://arxiv.org/abs/1206.5484))




### In S-matrix theories and string theory

Discussion of causality in [[string theory]] includes the following:

A brief look at the causality property of the string 2-point function is in

* {#Martinec95} [[Emil Martinec]], _Strings and Causality_ ([pdf](cds.cern.ch/record/569030/files/9311129.pdf)) in L. Baulieu, V.  Dotsenko, V. Kazakov, P. Windey (eds.) Quantum Field Theory and String Theory , NATO ASI Series B: Physics Vol. 328 (1995)

An in-depth discussion of causality of the [[string scattering amplitude|string scattering]] [[S-matrix]] via [[open string field theory]] is in

* {#ErlerGross04} [[Theodore Erler]], [[David Gross]], _Locality, Causality, and an Initial Value Formulation for Open String Field Theory_ ([arXiv:hep-th/0406199](https://arxiv.org/abs/hep-th/0406199))

This rediscovered some facts that had earlier been noticed in

* M. Maeno, _Canonical quantization of Witten's string field theory using midpoint light-cone time_, Phys. Rev. D43 no. 12 (1991).

Discussion in theories with [[higher curvature corrections]] of the gravitational background and in [[string theory]] includes

* Xian O. Camanho, Jose D. Edelstein, [[Juan Maldacena]], Alexander Zhiboedov, _Causality Constraints on Corrections to the Graviton Three-Point Coupling_ ([arXiv:](http://arxiv.org/abs/1407.5597))

* Giuseppe D'Appollonio, [[Paolo Di Vecchia]], [[Rodolfo Russo]], [[Gabriele Veneziano]], _Regge behavior saves String Theory from causality violations_ ([arXiv:1502.01254](http://arxiv.org/abs/1502.01254))


[[!redirects causal locality]]

[[!redirects Einstein causality]]
[[!redirects Einstein-causality]]

[[!redirects Einstein locality]]
[[!redirects Einstein-locality]]

[[!redirects microlocality]]
[[!redirects microcausality]]

[[!redirects locality]]

[[!redirects causality]]
