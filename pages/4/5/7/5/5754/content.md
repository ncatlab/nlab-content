
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _Peierls bracket_ ([Peierls 52](#Peierls52)) is equivalently the canonical [[symplectic manifold|symplectic]] [[Poisson bracket]] on the [[covariant phase space]] of [[field theories]] such as of the [[scalar field]] ([D&#252;tsch-Fredenhagen 01](#DutschFredenhagen01), [Khavkine 14](#Khavkine14), [Collini 16, prop. 31 and below](#Collini16)). Its construction requires the linearized [[field (physics)|field]] [[equations of motion]] satisfied by the [[gauge invariance|gauge invariant]] fields to have unique  [[retarded and advanced Green functions]]. Moreover, it extends "off shell" from the [[phase space]] to the space of all field configurations ([Marolf 94](#Marolf94), [D&#252;tsch-Fredenhagen 03, section 2.1](#DuetschFredenhagen03), [Fredenhagen-Rejzner 12, section 5](#FredenhagenRejzner12)), where however it is only [[Poisson bracket]], no longer [[symplectic manifold|symplectic]]. For more on this aspect see at _[[off-shell Poisson bracket]]_.

The [[Peierls bracket]] of two suitably [[smooth function|smooth]] [[functions]] $A$ and $B$ on [[field (physics)|field]] configuration space is the antisymmetrized influence on $B$ of an [[infinitesimal object|infinitesimal]] perturbation of a [[gauge fixing|gauge-fixed]] [[action]] by a function that restricts to $A$ on the embedding of the space of solutions in the field configuration space. It is the construction of the influence of $A$ on $B$ that requires the existence of unique retarded and advanced [[Green's functions]] of the linearized field equations. One can avoid [[gauge fixing]] the action, as long as $A$ and $B$ are [[gauge invariance|gauge invariant]] [[observables]]. In that case, unique retarded and advanced Green's functions may not exist, but due to the gauge invariance of $A$ and $B$ any representative of the gauge equivalence class of Green's functions with appropriate causal [[support]]. Since gauge invariant observables can be expressed in terms of gauge invariant fields (at least at the linearized level, which is all that matters in the construction) the existence and uniqueness of such equivalence classes of Green's functions is equivalent to the existence and uniqueness of retarded and advanced Green's functions for the linearized field equations satisfied by gauge invariant field combinations. 

For example, in [[electrodynamics]], advanced and retarded Green's functions exist on [[globally hyperbolic spacetimes]] for [[Maxwell equations]] in terms of the [[field strength]] $F=\mathbf{d}A$ and correspond to unique gauge equivalence classes of Green's functions for Maxwell equations in terms of the [[vector potential]] $A$.

The [[algebra of functions]] on the space of field configurations becomes a [[Poisson algebra]] in the following way. Pick a set of functions on the space of field configurations that restrict to a non-degeneratce [[coordinate system]] on the embedded [[covariant phase space]]. These functions, together with the [[equations of motion]] and [[gauge fixing]] conditions define a [[Poisson bivector]] by being declared canonical, such that the [[kernel]] of the bivector coincides with the ideal generated by the [[equations of motion]] and the [[gauge fixing]] conditions. Obviously the Poisson structure thus constructed on the algebra of functions on field configurations is not unique and depends on the above choice of coordinates; the same non-uniqueness may be parametrized instead by a choice of a [[connection on a bundle|connection]] on the space of field configurations. The embedded [[covariant phase space]] becomes a [[symplectic leaf]] of the symplectic [[foliation]] of the space of field configurations.


## Definition

### The Peirls bracket

> under construction

+-- {: .num_defn #PeirlsFormula}
###### Definition
(...)

...suitable PDE with advanced/retarded [[Green's function]] $\Delta_S^{A/R}$, then the _causal Gree's function_ is their difference

$$
  \Delta_S \coloneqq \Delta_S^{R} - \Delta_S^A
$$

(...)

=--

([#Khavkine 14, def. 3.9](#Khavkine14))

### The off-shell Peierls bracket

The idea of ([Marolf 93](#Marolf93), section II) is this: 

If $\{q(0), p(0)\}$ is the given (symplectic) Poisson bracket
on the space of solutions, identified with the space of 
initial data, then requiring that everything Poisson-commutes
with $EL(S)$, the 
[[Euler-Lagrange equation|Euler-Lagrange functional]] of the action, 
uniquely extends this to a bracket $\{q(t_1), p(t_2)\}$
on all hisories, because commutation with $EL(S)$
involves generation of time translation. 
Here $EL(S)$ generates a Poisson ideal and dividing that
out reproduces the original symplectic bracket.

Now observe (Khavkine 1) that $EL(S)$ provides
a foliation of history space by [[symplectic leaves]].
Because under the replacement $EL(S) \mapsto EL(S) - const$
the above still goes through. Observe also (Khavkine 2)
that $EL(S) - const = 0$ is the equations of motion 
for the origial action with a [[source]] term $J q$ added.
Hence the off-shell Peierls Poisson structure has 
[[symplectic leaves]] parameterized by the [[source]] $J$.

Observe finally (Khavkine 3) that with ([Marolf 93, section III B](#Marolf93)) it follows that the Peierls bracket on the shifted leaves
agrees with the original one. (...)


## Properties

+-- {: .num_prop #PeierlsPoissonBracket}
###### Proposition
**(Peierls bracket is the canonical Poisson bracket in field theory)

Given a [[local Lagrangian field theory]], assume that its [[gauge symmetries]] are globally recognizable ([Khavkine 14, section 3.2.2](#Khavkine14)). Then the Peierls bracket (def. \ref{PeirlsFormula}) is the [[Poisson bracket]] corresponding to the [[symplectic form]] on the [[reduced phase space|reduced]] [[covariant phase space]].

=--

([Khavkine 14, theorem 3.2](#Khavkine14))


## References

The definition of what now is called the Peierls bracket originates in

* {#Peierls52} R. Peierls, _The commutation laws of relativistic field theory_ (1952) ([jstor](http://www.jstor.org/pss/99080))
 
In this article the Peierls bracket on the [[covariant phase space]] of a [[gauge theory|non-gauge]] system is defined and the equivalence with the Hamiltonian phase space [[symplectic structure]] is (incompletely) demonstrated. Peierls also discusses how the definition extends to gauge theories and to fermionic theories.

An early review is in

* [[Bryce DeWitt]], _The Spacetime Approach to Quantum Field Theory_, in [[Bryce DeWitt]], [[Raymond Stora]] (eds.), _Les Houches Session XL, Relativity, Groups and Topology II_ (North-Holland, 1983), pp. 382&#8211;738.

which is also the first to explicitly check the [[Jacobi identity]] for the Peirls bracket.

A streamlined general account is in

* {#Khavkine14} [[Igor Khavkine]], _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv.1402.1282](https://arxiv.org/abs/1402.1282))

A traditional physics textbook account amplifying the Peierls bracket is

* {#DeWitt03} [[Bryce DeWitt]], _The global approach to Quantum Field Theory_ (2 volumes), Oxford 2003


The fact that the Peirls bracket for the [[scalar field]] gives the [[Poisson bracket]] in its [[covariant phase space]] is discussed in

* {#DutschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001
([arXiv:hep-th/0101079](https://arxiv.org/abs/hep-th/0101079))

* {#Collini16} [[Giovanni Collini]], prop. 31 and below in _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))


The off-shell generalization to a [[Poisson bracket]] on configuration space (history space) was first given in 

* {#Marolf93} [[Don Marolf]],  _Poisson Brackets on the Space of Histories_ Annals of Physics Volume 236, Issue 2, December 1994, Pages 374-391 ([arXiv:hep-th/9308141](http://arxiv.org/abs/hep-th/9308141))
  

* {#Marolf94} [[Don Marolf]], _The Generalized Peierls Bracket_. Ann. Phys. (N.Y.) 236 (1994) 392&#8211;412 ([arXiv:hep-th/9308150](http://arxiv.org/abs/hep-th/9308150))
  

See also exercise 17.12 in 

* [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_


A mathematically clean account of the (on- and off-shell) Peierls bracket (for [[scalar fields]]) is in section 2.1 of 

* {#DuetschFredenhagen03} [[Michael Dütsch]], [[Klaus Fredenhagen]], _The Master Ward Identity and Generalized Schwinger-Dyson Equation in Classical Field Theory_,  	Commun.Math.Phys. 243 (2003) 275-314 ([arXiv:hep-th/0211242](http://arxiv.org/abs/hep-th/0211242))
  

and in section 2 of

* Ferdinand Brennecke, [[Michael Dütsch]], _Removal of violations of the Master Ward Identity in perturbative QFT_, Rev.Math.Phys.20:119-172,2008 ([arXiv:0705.3160](http://arxiv-web3.library.cornell.edu/abs/0705.3160))

there with an eye towards the [[renormalization]] program of [[perturbative quantum field theory|perturbative Algebraic Quantum Field Theory]] (pAQFT) on flat and [[AQFT on curved spacetimes|on curved spacetimes]].

* {#DuetschFredenhagen04} [[Michael Dütsch]] and [[Klaus Fredenhagen]], _Causal perturbation theory in terms of retarded products, and a proof of the action Ward identity_, Rev. Math. Phys. 16 (2004) 1291-1348 ([arXiv:hep-th/0403213](http://arxiv.org/abs/hep-th/0403213))
  







Further references to its use in the renormalization program of pAQFT can be found in:

* {#FredenhagenRejzener12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_. Commun.Math.Phys. 314 (2012) 93-127 ([arXiv:1101.5112](http://arxiv.org/abs/1101.5112))
  

Functional analytic aspects of the definition and existence of the Peierls bracket (including its off-shell extension) are discussed in section 3.2 of

* {#BrunettiFredenhagenRibeiro12} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Pedro Ribeiro]], _Algebraic Structure of Classical Field Theory I: Kinematics and Linearized Dynamics for Real Scalar Fields_ ([arXiv:1209.2148](http://arxiv.org/abs/1209.2148))
  

The equivalence between the Peierls bracket and the [[symplectic manifold|symplectic]] [[Poisson bracket]] on the [[covariant phase space]] of classical field theory (by showing the equivalence of both to the canonical Poisson bracket in Hamiltonian formalism) was demonstrated in

* {#BarnichHenneauxSchomblond91} [[Glenn Barnich]], [[Marc Henneaux]], C. Schomblond, _Covariant description of the canonical formalism_. Phys.Rev. D44 (1991) R939-R941 ([doi](http://dx.doi.org/10.1103/physrevd.44.r939))

Further discussion of the manifestly covariant equivalence between the Peierls bracket and the [[symplectic manifold|symplectic]] [[Poisson bracket]] on the [[covariant phase space]] of classical field theory (avoiding traditional proof via the canonical Hamiltonian formalism) can be found in

* [[Michael Forger]], Sandro Romero, _Covariant Poisson Brackets in Geometric Field Theory_, Commun.Math.Phys. 256 (2005) 375-410 ([arXiv:math-ph/0408008](http://arxiv.org/abs/math-ph/0408008))

* [[Igor Khavkine]], _Characteristics, Conal Geometry and Causality in Locally Covariant Field Theory_, section 5, ([arXiv:1211.1914](http://arxiv.org/abs/1211.1914))

[[!redirects Peierls brackets]]

[[!redirects Peierls-Poisson bracket]]
[[!redirects Peierls-Poisson brackets]]

[[!redirects Poisson-Peierls bracket]]
[[!redirects Poisson-Peierls brackets]]

