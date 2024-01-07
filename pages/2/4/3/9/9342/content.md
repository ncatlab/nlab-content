
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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
 {#Idea}

The description of [[quantum field theory]] is traditionally mostly considered only in the [[infinitesimal neighbourhood]] of the underlying [[classical field theory|classical]] and [[free field theory]] As such these descriptions are referred to as _[[perturbative quantum field theory]]_ (pQFT) since they describe only small (in fact: infinitesimal) "[[perturbations]]" of a (hypothetical) free and classical field, instead of the fully interacting quantum fields.

Since this very coarse (but remarkably successful) perturbative concept of quantum field theory has come to often be considered by default, one speaks of _non-perturbative quantum field theory_ in order to amplify that the full theory is meant to be considered, not just the perturbative approximation.

\begin{imagefromfile}
    "file_name": "NonPerturbativeParameterSpace-230613.jpg",
    "float": "right",
    "width": 360,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [SS24, p. 3](#SS24IHH))"
\end{imagefromfile}

{#BeyondInfinitesimalNeighbourhood} **Beyond the infinitesimal neighbourhood of perturbation theory.** More concretely, if we think of generic ([[Lagrangian field theory|Lagrangian]]) [[quantum field theories]] as parameterized by 

1. [[Planck's constant]]$\;\hbar$, 

   expressing the "strength of [[quantum physics|quantum effects]]",

1. [[coupling constants]]$\;g$, 

   expressing the strength of [[interactions]] of [[field (physics)|fields]],

then [[perturbative QFT]] is concerned (just) with computing the [[Feynman perturbation series]] for [[scattering amplitudes]] as (just) a [[formal power series]] in these [[variables]], and since this typically has a *vanishing* [[radius of convergence]] (see [there](perturbative+quantum+field+theory#ReferencesNonConvergenceOfThePerturbationSeries)) it concerns just the [[infinitesimal neighbourhood]] of the origin in this parameter space (the infinitesimal [[halo]] of a single point) -- all the rest of the parameter space is the region of non-perturbative quantum field theory.

**As perturbation with non-perturbative effects.**
Passage from the perturbative to the non-perturbative description of QFT involves taking account of *[[non-perturbative effects]]* invisible to perturbation theory. 

These arise notably from the presence of [[soliton|solitonic]] field configurations ([[instanton|instantonic]], after [[Wick rotation]]): Such solitonic fields are invisible to perturbation theory because  they are not continuously [[connected topological space|connected]] to the [[vacuum]] field configuration, since they are constituted by topologically non-trivial structures, e.g. [[gauge potentials]] which are [[connection on a bundle|connections]] on a topologically non-trivial [[principal bundle]] on [[spacetime]] (such as [[Dirac monopoles]] or [[Yang-Mills instantons]], see at *[[fiber bundles in physics]]*). 

In lack of a general prescription for non-perturbative [[quantization]], authors try to make educated guesses about the would-be non-perturbative effects from inspection of the behaviour of the formal [[Feynman perturbation series]]: popular methods here go by the name *[[Borel resummation]]* and *[[resurgence theory]]*.


**Theory and reality.** Beware the usual habit in theoretical physics jargon of conflating the map with the territory (the field *theory* with the actual fields "in nature" that the theory means to describe): Real quantum fields in nature are always non-perturbative (the value of $\hbar$ and $g$ is not contained in the infinitesimal neightbourhood of the origin -- this is a purely theoretical/computational concept) so that their description by [[perturbative QFT]] is, by design, just an approximation of their complete nature. 


**As non-analyticity.** This is just as with [[smooth functions]] and their description by their [[Taylor series]] of their [[derivatives]] at a given origin: The Taylor series is a "perturbative description" of the full smooth function, which in contrast is the full non-perturbative object. Indeed the [[Feynman perturbation series]] in [[pQFT]] are imagined to be just such Taylor series of actual smooth functions (e.g. [[scattering amplitudes]]) in $\hbar$ and $g$, and the goal of non-perturbative QFT is to provide more information on "[[non-perturbative effects]]", hence on the actual functions (scattering amplitudes) at all or at least some positive values of $\hbar$ and/or $g$.

Of course, special among all smooth functions are the [[analytic functions]], whose Taylor series does already capture the full function, at least in some [[open neighbourhood]].
Accordingly, among QFTs that one can write to paper (but which are unlikely to describe anything in the real world) there are interacting examples (cite...) whose perturbative description already exhausts their full non-perturbative content, in that their [[Feynman perturbation series]] actually [[convergence|converges]], or at least has a [[positive number|positive]] [[radius of convergence]].

**Axiomatization and construction.** Among *axiomatizations* of non-perturbative field theory is 

1. *[[algebraic quantum field theory]]* (AQFT) in terms of [[local nets of observables]] with values in [[C-star algebra|$C^\ast$-algebras]] (axiomatizing the [[Heisenberg picture]] of [[quantum physics]]),

1. *[[functorial quantum field theory]]* in terms of [[cobordism category]] [[linear representation|representations]] (axiomatizing the [[Schrödinger picture]] of [[quantum physics]]).

Among *construction* methods of AQFT has been "[[constructive field theory]]", which aims to make rigorous [[analysis|analytic]] sense of [[path integrals]] in simple cases. This has worked for [[scalar field theory]] such as [[phi^4 theory|$\phi^4$-theory]]  in spacetime dimension 2 and 3, but (so far) not in dimension 4.

There are also some partial tools available from [[quantum mechanics]] such as [[strict deformation quantization]] ([Rieffel 1989](C-star+algebraic+deformation+quantization#Rieffel89)). Here it may be noteworthy that the established construction of [[perturbative quantum field theory]] has been understood to be an example of the systematic process of [[quantization]] called *[[formal deformation quantization]]*, specifically as an example of [[Fedosov deformation quantization]] ([Collini 16](perturbative+algebraic+quantum+field+theory#Collini16)). Since the non-perturbative version of [[formal deformation quantization]] is _[[strict C*-algebraic deformation quantization]]_ the latter might be a useful perspective on the problem of non-perturbative QFT (cf. e.g. [SS23](#SS23QOQF)).


{#ExamplesInIdeaSection} **Examples of nonperturbative QFT.** Presently, non-perturbative quantum field theories have been constructed only for simple toy examples, notably:

* for [[free field theories]] (no interaction),

* in low [[spacetime]] [[dimension]] (e.g. [[2d CFTs]], see e.g. at *[[conformal net]]*),

* for [[topological quantum field theories]] (see e.g. at *[[quantization of 3d Chern-Simons theory]]*),

* for pure [[scalar field theory]] (most famously [[phi^n-theory|$\phi^4$-theory]], cf. [Serone 2018](#Serone18)) 

  > (Examples of non-perturbative [[interacting quantum field theory|interacting]] [[scalar field theory]] in _any_ [[spacetime]] [[dimension]] are claimed in [Buchholtz & Fredenhagen 2020](AQFT#BuchholtzFredenhagen20), at least in the guise of [[local nets of observables|local nets]] of [[quantum observables]], pending the construction (or existence) of compatible [[vacuum states]]). 

**Key application: Confinement/Mass-gap in QCD/Yang-Mills.** A [[non-perturbative effect]] of paramount importance in [[experiment|experimentally]] observed [[quantum physics]] (and invisible to [[perturbative QFT|perturbative]] [[QCD]]) is the [[confinement]] and the [[mass gap]] of [[quantum chromodynamics]] ([[Yang-Mills theory]] with [[simple Lie group|simple]] [[gauge group]]).

That this experimentally observed confinement mechanism is indeed somehow encoded in the [[Lagrangian density]] for the [[gluons]] and [[quarks]] of [[QCD]] is plausibly verfied currently (only) by computer simulation ([[lattice QCD]]), but an analytic construction of a corresponding non-perturbative [[quantization of Yang-Mills theory]] has remained elusive enough to be pronounced one of the open "Millennium Problems" by the Clay Mathematics Institute (see [there](mass+gap#ReferencesMassGapProblem)).

However, qualitative understanding of [[confinement]] is given by an argument that separated [[quarks]] become connected by [[flux tubes]] of the [[strong nuclear force]] [[field (physics)|field]], which behave like [[strings]] whose [[string tension|string]]-[[tension]] exerts an attractive [[force]] on any pair of quarks, keeping them together and hence "[[confinement|confined]]" inside a [[hadron]] [[bound state]].

The attempt to understand non-perturbative confined QCD and hence [[quantum hadrodynamics]] as a theory of such [[flux tube]] [[strings]] has been both the origin of [[string theory]] as well as, after some detour through [[GUT]] [[quantum gravity]], its current understanding via the [[holographic principle]]: See at *[[Polyakov gauge-string duality]]*, at *[[AdS/QCD correspondence]]* and at *[confinement via AdS/QCD](confinement#ViaSkyrmions)*.

However, ironically also [[string theory]] has been mostly understood only in [[perturbation theory]], which currently causes the approach of [[holographic QCD]] to require the assumption of a large (in fact: humongous) and hence unrealistic number of [[quark]] [[color charge|colors]] (namely of [[color branes]]). 

But for this string theory, at least, there are hints as to its non-perturbative completion, enough so that it has a working title ("[[M-theory]]") albeit remaining elusive. See at *[AdS-CFT correspondence -- small-$N$ corrections](AdS-CFT+correspondence#SmallNCorrections)* for more on this.



## Related concepts

* [[non-perturbative effect]]

* [[Borel resummation]], [[resurgence theory]]

* [[strict deformation quantization]]

* [[conformal bootstrap]]

* [[instanton]]

* [[superselection sector]]

* [[non-perturbative string theory]]


## References

> (See also references at *[[non-perturbative effect]]*, *[[soliton]]* and *[[instanton]]*, particularly at *[[Yang-Mills instanton]]*.)

General introduction:

* Alexander P. Bakulev, [[Dmitry Shirkov]], *Inevitability and Importance of Non-Perturbative Elements in Quantum Field Theory*, Proceedings of the 6th Mathematical Physics Meeting, Sept. 14--23 (2010) Belgrade, Serbia  27--54 &lbrack;[arXiv:1102.2380](https://arxiv.org/abs/1102.2380), ISBN:978-86-82441-30-4&rbrack; 

Monographs:

* {#Froehlich92} [[Jürg Fröhlich]], _Non-perturbative quantum field theory -- Mathematical Aspects and Applications_, Advanced Series in Mathematical Physics, World Scientific (1992) &lbrack;[doi:10.1142/1245](https://doi.org/10.1142/1245)&rbrack;

* [[Yitzhak Frishman]], [[Jacob Sonnenschein]], *Non-Perturbative Field Theory -- From Two Dimensional Conformal Field Theory to QCD in Four Dimensions*, Cambridge University Press (2010) &lbrack;[doi:10.1017/CBO9780511770838](https://doi.org/10.1017/CBO9780511770838), summary: [arXiv:1004.4859](https://arxiv.org/abs/1004.4859)&rbrack;.
open access (2023) &lbrack;[doi:10.1017/9781009401654](https://doi.org/10.1017/9781009401654)&rbrack;

* [[Franco Strocchi]], *An Introduction to Non-Perturbative Foundations of Quantum Field Theory*, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;

  > ([[AQFT]] perspective)


Outlook from the point of view of [[causal perturbation theory]]/[[locally covariant perturbative quantum field theory]] is in

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], section 4.1 of _Quantum fields in curved spacetime_, Physics Reports Volume 574, 16 April 2015, Pages 1-35 ([arXiv:1401.2026](https://arxiv.org/abs/1401.2026))

The case of [[scalar field theory]] (such as [[phi^n-theory|$\phi^n$-theory]]):

* {#Serone18} Marco Serone, from 2:46 on in _A look at $\phi^4_2$ using perturbation theory_ (January 2018) &lbrack;[recording](https://www.youtube.com/watch?v=J4nxvY1rOhI)&

* {#BuchholtzFredenhagen20} [[Detlev Buchholz]], [[Klaus Fredenhagen]], _A $C^\ast$-algebraic approach to interacting quantum field theories_,  Commun. Math. Phys. **377** (2020) 947–969  &lbrack;[arXiv:1902.06062](https://arxiv.org/abs/1902.06062), [doi:10.1007/s00220-020-03700-9](https://doi.org/10.1007/s00220-020-03700-9)&rbrack;


Lectures notes for non-perturbative [[supersymmetry|supersymmetric]] QFT (such as in [[AdS-CFT]]) includes

* John Terning, _TASI-2002 Lectures: Non-perturbative Supersymmetry_ ([arXiv:hep-th/0306119](http://arxiv.org/abs/hep-th/0306119))

On non-perturbative [[BV-BRST formalism]]:

* [[Luigi Alfonsi]], *Derived $n$-plectic geometry: towards non-perturbative BV-BFV quantisation and M-theory*, talk at *[M-Theory and Mathematics 2023](/nlab/show/M-Theory+and+Mathematics#2023)*, NYU Abu Dhabi (2023) &lbrack;[web](/nlab/show/M-Theory+and+Mathematics#Alfonsi2023)&rbrack;

On non-perturbative quantization of topological [[flux]] observables in pure [[higher gauge theory]]:

* {#SS23QOQF} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Quantum Observables of Quantized Fluxes]]* &lbrack;[arXiv:2312.13037](https://arxiv.org/abs/2312.13037)&rbrack;

* {#SS24IHH} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Introduction to Hypothesis H]]*

[[!redirects non-perturbative QFT]]

[[!redirects non-perturbative quantum field theories]]

[[!redirects non-perturbative field theory]]
[[!redirects non-perturbative field theories]]


[[!redirects nonperturbative quantum field theory]]
[[!redirects nonperturbative quantum field theories]]

[[!redirects nonperturbative QFT]]
[[!redirects nonperturbative QFTs]]

[[!redirects non-perturbative physics]]


