
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

What is called _locally covariant perturbative algebraic quantum field theory_ ([Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Brunetti-Fredenhagen-Verch 03](#BrunettiFredenhagenVerch03)) is a formulation of [[local quantum field theory|local]] [[perturbative quantum field theory|perturbative]] [[quantum field theory]] [[AQFT on curved spacetimes|on general spacetimes]] (hence on general [[classical field theory|classical]] [[background field]] configurations of the field theory of [[gravity]]) which is both mathematically rigorous as well as closely connected to the traditional non-rigorous discussions, hence to [[phenomenology]] and [[experiment]].

The approach uses the [[Haag-Kastler axioms]] for [[algebraic quantum field theory]] in a variant that 

1. demands only [[formal power series]] [[star-algebras]] [[algebra of observables|of observables]] instead of [[C*-algebras]] 

   (this reflects the [[perturbation theory]] in [[Planck's constant]] and the [[coupling constant]]);

1. evaluates [[local nets of observables]] not just on causal subspaces of [[Minkowski spacetime]] but on more general [[globally hyperbolic Lorentzian manifolds]] 

  (this reflects the extension to general curved spacetime backgrounds). 

What connects this to the traditional discussion of QFT is the observation (in essence already due to [Il'in-Slavnov 78](#IlinSlavnov78) but then ignored) that standard [[renormalization]] theory (removal of [[ultraviolet divergences]]) in the guise of [[causal perturbation theory]] ([Epstein-Glaser 73](#EpsteinGlaser73)) automatically produces [[causally local nets]] of [[algebras of observables]] (due to "[[adiabatic switching]]" and [[causal locality]] of the [[S-matrix]], see [there](S-matrix#CausalLocality)), in fact that considering these local nets instead of their would-be colimiting global algebra serves to define the perturbation theory even in the presence of [[infrared divergences]]. (Specifically: This takes care of the "[[algebraic adiabatic limit]]", which defines the [[quantum observables]]. It does not yet in itself define the "[[weak adiabatic limit]]" for the would-be [[vacuum]] [[quantum state]].)



To put this into perspective, notice that formulation of [[quantum field theory]] has many aspects and perspectives. Two almost complementary threads are the following:

**1) [[perturbative QFT|perturbation theory]] by means of [[formal geometry|formal]] [[Feynman diagram]] expansions of ([[Wick rotation|Wick rotated]]) [[path integrals]]**

   This is the approach predominant in [[phenomenology]]. 

   It produces the [[observable]] [[numbers]] which are checked to great precision in [[experiments]] starting from the early development of [[quantum electrodynamics]], fully established with the success of [[quantum chromodynamics]] and recently culminating in the [[Higgs field]] physics seen at the [[LHC]] experiment, confirming the [[standard model of particle physics]].

   While many of the mathematical intricacies of this approach have found solutions over the decades, most of these rely on global properties of [[Minkowski spacetime]] such as translation invariance and existence of an invariant [[vacuum]] [[quantum state]], hence on a consistent concept of [[particles]]. None of this generalizes robustly to [[quantum field theory on curved spacetimes]] of relevance in [[cosmology]], [[black hole radiation]] or the [[instanton in QCD|instanton vacuum of QCD]].


**2) [[algebraic quantum field theory]] by means of [[local nets]] of [[C*-algebras]] of [[observables]]**

   This is the approach predominant in [[mathematical physics]]. 

   It produces the structural [[theorems]] of quantum field theory, such as the [[PCT theorem]] and the [[spin-statistics theorem]] and it seamlessly generalizes to [[QFT on curved spacetimes]].

   In its insistence on [[C*-algebras]] its ambition is to describe the full [[non-perturbative quantum field theory|non-perturbative]] quantum field theory. But as a matter of fact not a single relevant example ([[interaction|interacting]] QFT in spacetime dimensions 4 or greater) is known. Indeed, the construction of the motivating example, [[quantization of Yang-Mills theory]], is one of the open "millenium problems".

$\,$

Locally covariant perturbative quantum field theory provides a synthesis of these two opposites.

$\,$


Quantum field theory is not only extremely rich in its [[phenomenology]] but also its formulation involves a plethora of mathematical tools, such as [[Lorentzian geometry]], [[spin geometry]], [[analysis]] (especially [[Fréchet manifold]] theory for [[jet bundles]] and [[spaces of sections]]) [[variational calculus]], [[symplectic geometry]], [[quantization]] (specifically [[formal  deformation quantization]] for [[perturbative quantum field theory]]) [[functional analysis]] (specifically [[microlocal analysis]] for [[causal perturbation theory]]) and [[operator algebra]]. While lcpAQFT is mathematically rigorous, hence unambiguous and precise, it remains a long story from its first principles to the computation of [[scattering amplitudes]]. To ease the overview, we now indicate the global structure of the topic first.

The input datum is a [[local field theory|local]] [[Lagrangian field theory|Lagrangian]] [[classical field theory]] on [[gravity]] [[background fields|backgrounds]], hence a [[natural transformation]] 
from ([[globally hyperbolic spacetimes|globally hyperbolic]]) [[Lorentzian manifolds]] to [[field bundles]] over these spacetimes equipped with a [[local Lagrangian density]] on their [[jet bundle]].

This induces for each Lorentzian spacetime the corresponding [[covariant phase space]], a [[presymplectic structure|presymplectic]] [[smooth space]]. 

Passage to the corresponding [[perturbative quantum field theory]] means to  choose a [[formal deformation quantization]] of a subalgebra of the [[algebra of functions|algebra of]] [[smooth functions]] on the covariant phase space (the "[[observables]]"). This formal deformation is a [[formal power series]] [[star-algebra]] whose formal parameter is identified with [[Planck's constant]] and it is this [[formal power series]] nature which makes this just a _perturbative_ quantization (while a [[non-perturbative field theory|non-perturbative]] quantization would be required to yield a [[C*-algebra]] of [[quantum observables]], or something similar).

Finally what makes this _locally covariant_ is that the resulting assignment of formal power series algebras of observables to spacetimes is required to still be a [[functor]] satisfying [[causal locality]] (a [[local net]]). It is in this sense that the output of the procedure is an [[algebraic quantum field theory]] in the sense of the [[Haag-Kastler axioms]], only that instead of [[C*-algebras]] it assigns [[formal power series]] [[star-algebras]].

In summary, constructing a locally covariant perturbative quantum field theory means to 

* prescribe a [[classical field theory]] encoded by a functor

  $L \;\colon\;\left\{ \text{spacetimes} \right\} 
     \longrightarrow \left\{ \array{ \text{field bundles equipped with} \\ \text{local Lagrangian densities} }\right\}$ 

  and consider the induced [[covariant phase space]]

   $ \omega \;\colon\; \left\{ \text{spacetimes} \right\} \longrightarrow \{ \text{pre-symplectic smooth spaces} \}$

* choose a [[formal deformation quantization]] of a subalgebra of the smooth functions on the covariant phase space

  $ A_{obs} \;\colon\; \left\{ \text{spacetimes} \right\} \longrightarrow \left\{ \text{formal power series star algebra} \right\} $ 

  such that this satisfies [[causal locality]].


While this is straightforward as a prescription, finding any formal deformation quantization on infinite-dimensional phase spaces is highly non-trivial. (Notice that essentially all the existing literature on formal deformation quantization considers it on finite-dimensional manifolds.) But there is an [[algorithm]] that yields an effective solution together with a parameterization of the available choices, called _[[causal perturbation theory]]_. This algorithm proceeds as follows:

1. Choose a decomposition of the [[Lagrangian density]] $L$ into a [[kinetic action|kinetic term]] $L_{kin}$ and an [[interaction]] term $L_{int} \coloneqq L - L_{kin}$, where $L_{kin}$ is such that its [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] is a [[linear operator|linear]] [[hyperbolic differential operator]] (the "[[wave operator]]" for the [[free field]]);

1. construct its [[Wick algebra]] which is the vector space of [[microcausal functionals]] on phase space equipped with the [[Moyal quantization|Moyal star product]] induced by the [[causal Green function]] of that hyperbolic differential operator;

1. for the remaining [[interaction]] $L_{int}$ regarded as an element of the Wick algebra, [[induction|inductively]] construct its [[S-matrix]] as a [[distribution]] with values in the Wick algebra by demanding it to be [[causal additivity|causally additive]] (this is the step of [[causal perturbation theory]] proper).  The theorem of ([Epstein-Glaser 73](#EpsteinGlaser73)) states that this has a solution, and that the ambiguity in the solution is at each step of the induction parametrized by a finite set of [[real numbers]] (given, at stage $n$, by extending the [[n-point function]] [[distributions]] to the [[diagonal]]).

1. Finally the desired algebra of observables on some spacetime $X$  is the Wick algebra on microcausal functions on any slightly larger spacetime $\tilde X$ deformed by conjugation with the S-matrix evaluated (being a distribution) on any bump function on $\tilde X$ that is unity on $X \subset \tilde X$.

For [[Minkowski spacetime]] this algorithm is due to [Epstein-Glaser 73](#EpsteinGlaser73) building on ideas of St&#252;ckelberg and Bogoliubov, while the generalization to [[globally hyperbolic spacetimes]] is due to [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00) (at least for [[scalar field theory]]). That this does in fact yield a [[local net]] ([[causal locality]]) was first observed in ([Il'in-Slavnov 78](#IlinSlavnov78)), but ignored or forgotten, and then rediscovered and popularized in ([Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)).

When comparing with the bulk of the literature, the reader should beware that most texts do not discuss this algorithm as a means for [[formal deformation quantization]]. Instead, this algorithm of [[causal perturbation theory]] was extracted from experience and justified itself by coinciding with other established recipes of quantum field theory to the extent that these are well-defined, and hence ultimately by producing [[scattering amplitudes]] in [[QED]], [[QCD]] and the [[standard model of particle physics]] which, when truncated to low order in the formal deformation parameter $\hbar$, turn out to coincide to high precision with [[experiment]].

That this algorithm in fact constructs the [[formal deformation quantization]] of the covariant phase space of the given local Lagrangian density $L$ was understood only very recently in ([Collini 16](#Collini16)) (for [[phi^4 theory]] of the [[scalar field]]) and in ([Hawkins-Rejzner 16](#HawkinsRejzner16)) (for the [[scalar field]] with regular non-local interaction terms).

There are choices to be made in finding this deformation quantization. In ([Collini 16](#Collini16)) these are parameterized as the choices of initial conditions in the [[induction|inductive]] construction of [[Fedosov's deformation quantization]] and shown to be equivalent to the choices of causal splitting of distributions in the above algorithm of [[causal perturbation theory]] due to [Epstein-Glaser 73](#EpsteinGlaser73), which in turn equivalently are the choices known as _[[renormalization]]_ coefficients in traditional perspectives to perturbative quantum field theory (which in a mathematically rigorous approach might better be called "normalization" coefficients as in [Scharf 95, section 4.3](#Scharf95)).
The [[main theorem of perturbative renormalization]] states that the space of these choices is a [[torsor]] over a [[group]], called the [[Stückelberg-Petermann renormalization group]].

Finally notice that there is also a choice involved in restricting attention to the [[microcausal functionals]] inside the algebra of all smooth functions on phase space. For deformation quantization on finite-dimensional manifolds it is understood that the full algebra of smooth functions is to be quantized, but for the infinite-dimensional phase space of field theory the full algebra of functions does not even support the [[Poisson bracket]] which is to be deformed. The subalgebra of microcausal functionals just happens to be technically under control, closed under the Poisson bracket, and large enough to contain the point-interaction terms that are relevant in quantum field theories observed in nature ([[QED]], [[QCD]], [[perturbative quantum gravity]]). It seems to be unclear and in fact un-studied what a lift of the whole program to larger subalgebras would mean or entail.

One way to understand why it is not the full space of smooth functions on phase space that should be quantized is the sibling of algebraic deformation quantization known as [[geometric quantization]]. This demands that only the [[Hamiltonian vector field|Hamiltonian observables]] be considered, which are those smooth functions $h$ on phase space such that there exists a smooth vector field $v$ with $d h = \omega(v,-)$ (where $\omega$ is the [[pre-symplectic form]]). On these at the very least the [[Poisson bracket]] is guaranteed to close (for discussion of this in the context of local field theory see [Benini-Schenkel 16](Poisson+manifold#BeniniSchenkel16)), in fact geometric pre-quantization is the [[Lie integration]] of the resulting Poisson-bracket [[Lie algebra]] to the [[quantomorphism group]]. Hence the restriction to Hamiltonian observables may be regarded as part of [[non-perturbative field theory]] and hence highlights the intrinsic incompleteness of perturbative quantization methods. 

At the moment, however, non-perturbative quantization of field theories remains completely non-understood (apart from toy cases such as [[2d conformal field theories]] and certain [[topological field theories]]). For the class of [[Yang-Mills theories]] it is one of in the list of open "Millenium Problems" of the Clay Mathematics Institute ([Jaffe-Witten](quantization+of+Yang-Mills+theory#JaffeWitten), [Douglas 04](quantization+of+Yang-Mills+theory#Douglas04)).

For more detailed discussion of all of this see at _[[geometry of physics -- A first idea of quantum field theory]]_.

Besides lcpQFT being just perturbative (in [[Planck's constant]]), there remains just one problem: 

When applied to [[gauge theory]] on [[quantum field theory on curved spacetime|on curved spacetime]] the usual axioms on a [[local net]] break: either they enforce all [[characteristic classes]] of the [[gauge field]] ("[[instanton sectors]]") to be trivial, or else the axioms encoding locality are broken (see [Schenkel 14](#Schenkel14), [Schreiber 14](https://ncatlab.org/schreiber/show/Higher+field+bundles+for+gauge+fields)).

This remaining problem is meant to be solved by passing from plain [[algebras of observables]] to [[homotopical algebra|homotopical algebras]] ([[higher algebra|higher algebras]]), and hence to a formulation of **[[homotopical algebraic quantum field theory]]** (see [Schenkel 17](#Schenkel17)). This is still in the making.



## References

### Review

Survey and exposition of locally covariant algebraic quantum field theory beyond [[causal perturbation theory]] in [[Minkowski spacetime]] (for which see [there](causal+perturbation+theory#References)) includes the following:

* [Hollands 07, section 3](#Hollands07)

* [[Robert Wald]], _The Formulation of Quantum Field Theory in Curved Spacetime_ ([arXiv:0907.0416](https://arxiv.org/abs/0907.0416))

* [[Robert  Wald]], _The History and Present Status of Quantum Field Theory in Curved Spacetime_ ([arXiv:gr-qc/0608018](https://arxiv.org/abs/gr-qc/0608018))

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#FredenhagenRejzner15} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

* [[Klaus Fredenhagen]], _Quantum field theory and gravitation_, talk at closing colloquium of trimester "Le Monde Quantique", IHES April 2015 ([pdf](https://indico.math.cnrs.fr/event/782/material/slides/1.pdf))

* {#Rejzner16} [[Katarzyna Rejzner]], _[[Perturbative Algebraic Quantum Field Theory]]_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

* [[Urs Schreiber]], _[[geometry of physics -- perturbative quantum field theory]]_, 2017

* {#Duetsch18} [[Michael Dütsch]], _[[From classical field theory to perturbative quantum field theory]]_, 2018

* {#BrunettiFredenhagenTejzner23} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Kasia Rejzner]], *Locally covariant approach to effective quantum gravity*, in *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2212.07800](https://arxiv.org/abs/2212.07800)&rbrack;


### Original articles

The method of [[causal perturbation theory]] goes back to ideas of St&#252;ckelberg and Bogoliubov. The proof that the causal [[S-matrix]] required by this method may always be constructed by an inductive process with a finite-dimensional space of choices ("[[renormalization]]") at each stage is due to 

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

A detailed exposition of this method applied to [[QED]], [[QCD]], [[Yang-Mills theory]] and [[perturbative quantum gravity]] on [[Minkowski spacetime]] is in the textbooks

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001


The axioms for the locally covariant formulation of [[AQFT on curved spacetimes]] is due to

* {#BrunettiFredenhagenVerch03} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Rainer Verch]], _The generally covariant locality principle -- A new paradigm for local quantum physics_, Commun.Math.Phys.237:31-68, 2003 ([arXiv:math-ph/0112041](https://arxiv.org/abs/math-ph/0112041))

The construction of [[Wick algebras]] of [[quantum observables]] of [[free fields]] on curved [[spacetimes]] via [[Hadamard distributions]] relies on the results of

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

The observation that the [[causal perturbation theory]] of [Epstein-Glaser 73](#EpsteinGlaser73) lends itself to a construction of locally covariant perturvative AQFT is due to

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32. ([spire](http://inspirehep.net/record/135575), [doi](http://dx.doi.org/10.1007/BF01035870))

* [Brunetti-Fredenhagen 00, last section](#BrunettiFredenhagen00)

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

Extension of [[causal perturbation theory]] to [[AQFT on curved spacetimes|curved spacetimes]] is due to

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

  following

  * {#Stora93} [[Raymond Stora]], _Differential algebras in Lagrangean field theory_, ETH Lectures, January-February 1993. Manuscript


* {#DuetschFredenhagen00} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#HollandsWald01} [[Stefan Hollands]], [[Robert Wald]], _Local Wick Polynomials and Time Ordered Products of Quantum Fields in Curved Spacetime_, Commun. Math. Phys. 223:289-326,2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))

* [[Stefan Hollands]], [[Robert Wald]], _On the Renormalization Group in Curved Spacetime_, Commun. Math. Phys. 237 (2003) 123-160 ([arXiv:gr-qc/0209029](https://arxiv.org/abs/gr-qc/0209029))

* [[Stefan Hollands]], [[Robert Wald]], _Conservation of the stress tensor in perturbative interacting quantum field theory in curved spacetimes_, Rev.Math.Phys. 17 (2005) 227-312 ([arXiv:gr-qc/0404074](https://arxiv.org/abs/gr-qc/0404074))

Specifically construction of [[renormalization|renormalized]] [[Yang-Mills theory]] on curved spacetimes is due to

* {#Hollands07} [[Stefan Hollands]], _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys.20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

The observation that this construction produces [[formal deformation quantization]] of the classical field theory was made for the [[free field]] and its quantization by [[Wick algebras]] is

* J. Dito, _Star-product approach to quantum field theory: The free scalar field_. Letters in Mathematical Physics, 20(2):125&#8211;134, 1990 ([spire](https://inspirehep.net/record/303898/))

which was amplified in 

* {#DuetschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001
([arXiv:hep-th/0101079](https://arxiv.org/abs/hep-th/0101079))

and generalized to [[quantum field theory on curved spacetimes]] in [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00) and

* {#BrunettiFredenhagen95} [[Romeo Brunetti]], [[Klaus Fredenhagen]], M. K&#246;hler, _The microlocal spectrum condition and Wick polynomials on curved spacetimes_, Commun. Math. Phys. 180, 633-652, 1996 ([arXiv:gr-qc/9510056](https://arxiv.org/abs/gr-qc/9510056))

* {#HollandsWald01} [[Stefan Hollands]], [[Robert Wald]], _Local Wick Polynomials and Time Ordered Products of Quantum Fields in Curved Spacetime_, Commun. Math. Phys. 223:289-326, 2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))


That more generally the deformation quantization of interacting fields yields the traditional prescription of [[causal perturbation theory]] was shown for the  [[scalar field]] [[phi^4 theory]] in

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

and for the interacting scalar field in the toy example of regular non-local interactions in 

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))

The [[perturbative quantum field theory|perturbative quantization]] of [[gauge theories]] ([[Yang-Mills theory]]) in [[causal perturbation theory]]/[[perturbative AQFT]] is discussed (for trivial [[principal bundles]] and restricted to [[gauge invariant observables]]) via [[BRST-complex]]/[[BV-formalism]] in

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

and surveyed in

* [Rejzner 16, chapter 7](#Rejzner16)


A survey of the required generalization for [[gauge theory]] with non-trivial [[instanton sectors]] via [[homotopical algebraic quantum field theory]] is in 

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories
in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[SchenkelTrento2014.pdf:file]]) (with further emphasis on this point in the companion talk [Schreiber 14](field+bundle#Schreiber14)) 

* {#Schenkel17} [[Alexander Schenkel]], _Towards Homotopical Algebraic Quantum Field Theory_, talk at _[Foundational and Structural Aspects of Gauge Theories](https://indico.mitp.uni-mainz.de/event/76/overview)_,
Mainz Institute for Theoretical Physics, 29 May &#8211; 2 June 2017. ([pdf](http://aschenkel.eu/Mainz17.pdf))

[[!redirects perturbative AQFT]]
[[!redirects pAQFT]]

[[!redirects locally covariant perturbative quantum field theory]]
[[!redirects locally covariant perturbative quantum field theories]]

[[!redirects locally covariant perturbative algebraic quantum field theory]]
[[!redirects locally covariant perturbative algebraic quantum field theories]]


[[!redirects locally covariant perturbative QFT]]
[[!redirects locally covariant perturbative QFTs]]

[[!redirects locally covariant perturbative AQFT]]

[[!redirects locally covariant pAQFT]]
