
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Algebraic QFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functorial QFT
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

1. [[Planck's constant]]$\phantom{-}\hbar$, 

   expressing the "strength of [[quantum physics|quantum effects]]",

1. [[coupling constants]]$\phantom{-}g$, 

   expressing the strength of [[interactions]] of [[field (physics)|fields]],

then [[perturbative QFT]] is concerned (just) with computing the [[Feynman perturbation series]] for [[scattering amplitudes]] as (just) a [[formal power series]] in these [[variables]], and since this typically has a *vanishing* [[radius of convergence]] (see [there](perturbative+quantum+field+theory#ReferencesNonConvergenceOfThePerturbationSeries)) it concerns just the [[infinitesimal neighbourhood]] of the origin in this parameter space (the infinitesimal [[halo]] of a single point) -- all the rest of the parameter space is the region of non-perturbative quantum field theory.

**As perturbation with non-perturbative effects.**
Passage from the perturbative to the non-perturbative description of QFT involves taking account of *[[non-perturbative effects]]* invisible to perturbation theory. 

These arise notably from the presence of [[soliton|solitonic]] field configurations ([[instanton|instantonic]], after [[Wick rotation]]): Such solitonic fields are invisible to perturbation theory because  they are not continuously [[connected topological space|connected]] to the [[vacuum]] field configuration, since they are constituted by topologically non-trivial structures, e.g. [[gauge potentials]] which are [[connection on a bundle|connections]] on a topologically non-trivial [[principal bundle]] on [[spacetime]] (such as [[Dirac monopoles]] or [[Yang-Mills instantons]], see at *[[fiber bundles in physics]]*). 

Beware that this is relevant even on [[Minkowski spacetime]] $\mathbb{R}^{1,d}$, and prominently so: While these [[spacetimes]] are [[contractible topological space|contractible]] in themselves, [[solitons]] ([[instantons]]) are [[field configurations]] whose [[field strength]] is constrained to "[[vanish at infinity]]", which means that they are [[cocycles]] in ([[differential cohomology|differential]]) [[compactly supported cohomology]], hence defined on the [[one-point compactification]] $(-)_{\cup \{\infty\}}$ of space. For instance [[instantons]] on $\mathbb{R}^4$ are effectively bundles [on $\mathbb{R}^4_{\cup \{\infty\}} \simeq S^4$](one-point+compactification#ExamplesSpheres) (see [there](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)).

In lack of a general prescription for non-perturbative [[quantization]], authors try to make educated guesses about the would-be non-perturbative effects from inspection of the behaviour of the formal [[Feynman perturbation series]]: popular methods here go by the name *[[Borel resummation]]* and *[[resurgence theory]]*.


**Theory and reality.** Beware the usual habit in theoretical physics jargon of conflating the map with the territory (the field *theory* with the actual fields "in nature" that the theory means to describe): Real quantum fields in nature are always non-perturbative (the experimentally observed values of [[Planck's constant|$\hbar$]] and [[coupling constant|$g$]] are not contained in the [[infinitesimal neighbourhood]] of the [[zero]] -- this is a purely theoretical/computational concept) so that their description by [[perturbative QFT]] is, by design, just an approximation of their complete nature. 


**As non-analyticity.** The distinction between nonperturbative and perturbative is much that between [[smooth functions]] and the [[Taylor series]] of their [[derivatives]] at a given origin: The Taylor series is a "perturbative description" of the full smooth function, which in contrast is the full non-perturbative object. Indeed the [[Feynman perturbation series]] in [[perturbative QFT]] are imagined to be just such Taylor series of actual smooth functions (e.g. [[scattering amplitudes]]) in $\hbar$ and $g$, and the goal of non-perturbative QFT is to provide more information on "[[non-perturbative effects]]", hence on the actual functions (scattering amplitudes) at all or at least some positive values of $\hbar$ and/or $g$.

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

* [[strongly correlated system]]

* [[non-perturbative effect]]

* [[Borel resummation]], [[resurgence theory]]

* [[strict deformation quantization]]

* [[conformal bootstrap]]

* [[instanton]]

* [[superselection sector]]

* [[non-perturbative string theory]]


## References
 {#References}

> (See also references at *[[non-perturbative effect]]*, *[[soliton]]* and *[[instanton]]*, particularly at *[[Yang-Mills instanton]]*.)

Motivation via the generic [failure of convergence](perturbative+quantum+field+theory#ReferencesNonConvergenceOfThePerturbationSeries) of [[perturbative quantum field theory]]:

* Alexander P. Bakulev, [[Dmitry Shirkov]], *Inevitability and Importance of Non-Perturbative Elements in Quantum Field Theory*, Proceedings of the 6th Mathematical Physics Meeting, Sept. 14--23 (2010) Belgrade, Serbia  27--54 &lbrack;[arXiv:1102.2380](https://arxiv.org/abs/1102.2380), ISBN:978-86-82441-30-4&rbrack; 

Monographs:

* [[Yitzhak Frishman]], [[Jacob Sonnenschein]]: *Non-Perturbative Field Theory -- From Two Dimensional Conformal Field Theory to QCD in Four Dimensions*, Cambridge University Press (2010) &lbrack;[doi:10.1017/CBO9780511770838](https://doi.org/10.1017/CBO9780511770838), summary: [arXiv:1004.4859](https://arxiv.org/abs/1004.4859)&rbrack;.
open access (2023) &lbrack;[doi:10.1017/9781009401654](https://doi.org/10.1017/9781009401654)&rbrack;
  > "Relativistic Quantum Field Theory has been very successful in describing strong, electro-magnetic and weak interactions, in the region of small couplings by using [[perturbative quantum field theory|perturbation theory]], within the framework of the Standard Model. 
  > However, the region of strong coupling, like the hadronic spectrum and various scattering phenomena of hadrons within QCD, is still largely unsolved.
  > A large variety of methods have been used to address this question, including QCD sum rules, lattice gauge simulations, light cone quantization, low energy effective Lagrangians like the Skyrme model and chiral Lagrangians, large $N$ approximation, techniques of conformal invariance, integrable model approach, supersymmetric models, string theory approach etc. In spite of this major effort the gap between the phenomenology and the basic theory has been only partially bridged, and the problem is still open.
  > The goals of this book are to provide a detailed description of the tool box of nonperturbative techniques, to apply them on simplified systems, mainly of gauge dynamics
in two dimensions, and to examine the lessons one can learn from those systems about four dimensional QCD and hadron physics."

and via [[Wightman axioms]]:

* [[Franco Strocchi]], *An Introduction to Non-Perturbative Foundations of Quantum Field Theory*, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;
  > "The perturbative series is [known to diverge](perturbative+quantum+field+theory#ReferencesNonConvergenceOfThePerturbationSeries), and actually, for the prototypic model of self-interacting scalar field ([[phi^4 theory|$\phi^4$-theory]]), on which most of the textbooks are based, the perturbative expansion is misleading, since the theory has been proved to be trivial in $s+1$ dimensions (with $s \geq 3$). Clearly, this makes it difficult to define a QFT through
its perturbative expansion and raises conceptual problems such as the mathematical consistency of such an expansion.
  > As a matter of fact, after more than fifty years of QFT we are still in the embarrassing situation of not knowing a single non-trivial (even non-realistic) model of QFT in 3+1 dimensions, allowing a non-perturbative control."

with focus on [[topological physics -- contents|topological physics]] ([[solitons]], [[Skyrmions]], [[instantons]], [[monopoles]], [[gauge anomalies]], ...):

* [[Roberto Percacci]]: *Non-Perturbative Quantum Field Theory -- An Introduction to Topological and Semiclassical Methods*, SISSA & ICTP (2024) &lbrack;[doi:10.22323/9788898587056](https://doi.org/10.22323/9788898587056), [pdf](https://library.oapen.org/bitstream/handle/20.500.12657/96025/9788898587056.pdf)&rbrack;


Further collections:

* [[Gerard ’t Hooft]], [[Arthur Jaffe]], [[Gerhard Mack]], [[P. K. Mitter]], [[Raymond Stora]] (eds.) *Nonperturbative Quantum Field Theory*,  NATO Science Series B **185** (1988) &lbrack;[doi:10.1007/978-1-4613-0729-7](https://doi.org/10.1007/978-1-4613-0729-7)&rbrack;

* {#Froehlich92} [[Jürg Fröhlich]], _Non-perturbative quantum field theory -- Mathematical Aspects and Applications_, Advanced Series in Mathematical Physics, World Scientific (1992) &lbrack;[doi:10.1142/1245](https://doi.org/10.1142/1245)&rbrack;


Outlook from the point of view of [[causal perturbation theory]]/[[locally covariant perturbative quantum field theory]]:

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], section 4.1 of: _Quantum fields in curved spacetime_, Physics Reports **574** (2015) 1-35 &lbrack;[arXiv:1401.2026](https://arxiv.org/abs/1401.2026), [doi:10.1016/j.physrep.2015.02.001](https://doi.org/10.1016/j.physrep.2015.02.001)&rbrack;


The case of [[scalar field theory]] (such as [[phi^n-theory|$\phi^n$-theory]]):

* {#Serone18} Marco Serone, from 2:46 on in _A look at $\phi^4_2$ using perturbation theory_ (January 2018) &lbrack;[recording](https://www.youtube.com/watch?v=J4nxvY1rOhI)&

* {#BuchholtzFredenhagen20} [[Detlev Buchholz]], [[Klaus Fredenhagen]], _A $C^\ast$-algebraic approach to interacting quantum field theories_,  Commun. Math. Phys. **377** (2020) 947–969  &lbrack;[arXiv:1902.06062](https://arxiv.org/abs/1902.06062), [doi:10.1007/s00220-020-03700-9](https://doi.org/10.1007/s00220-020-03700-9)&rbrack;

See also:

* M. Rovira, A. Parreño, R. J. Perry: *A Variational Approach to Quantum Field Theory* &lbrack;[arXiv:2409.17887](https://arxiv.org/abs/2409.17887)&rbrack;


Relevance of non-perturbative methods in [[condensed matter theory]] ([[quantum materials]]) and [[quantum information theory]] ([[topological quantum computation]]):

*  Alvaro Ferraz, [[Kumar S. Gupta]], [[Gordon W. Semenoff]], Pasquale Sodano (eds): *Strongly Coupled Field Theories for Condensed Matter and Quantum Information Theory*, Springer Proceedings in Physics **239**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-35473-2](https://doi.org/10.1007/978-3-030-35473-2), [pdf](https://link.springer.com/content/pdf/10.1007/978-3-030-35473-2.pdf)&rbrack;

* [[Peter Fulde]], *Correlated Electrons in Quantum Matter*, World Scientific (2012) &lbrack;[doi:10.1142/8419](https://doi.org/10.1142/8419), [pdf](https://www.pks.mpg.de/fileadmin/user_upload/MPIPKS/group_pages/Electronic_Correlations/BOOK_Aktualisierung_Oct19.pdf)&rbrack;

* Andreas Schadschneider, Götz S. Uhrig: *Strongly Correlated Systems in Solid State Physics*, lecture notes (2004) &lbrack;[pdf](https://www.thp.uni-koeln.de/~as/Mypage/PSfiles/Korrel/korrel.pdf), [[SchadschneiderUhrig-StronglyCorrelated.pdf:file]]&rbrack;
  > (focus on [[spin chain]]-models)

Lectures notes for non-perturbative [[supersymmetry|supersymmetric]] QFT (such as in [[AdS-CFT]]) includes

* John Terning, _TASI-2002 Lectures: Non-perturbative Supersymmetry_ ([arXiv:hep-th/0306119](http://arxiv.org/abs/hep-th/0306119))

On non-perturbative [[BV-BRST formalism]]:

* [[Luigi Alfonsi]], *Derived $n$-plectic geometry: towards non-perturbative BV-BFV quantisation and M-theory*, talk at *[M-Theory and Mathematics 2023](/nlab/show/M-Theory+and+Mathematics#2023)*, NYU Abu Dhabi (2023) &lbrack;[web](/nlab/show/M-Theory+and+Mathematics#Alfonsi2023)&rbrack;

On non-perturbative quantization of topological [[flux]] [[observables]] in pure [[higher gauge theory]] (cf. *[[geometry of physics -- flux quantization]]*):

* {#SS23QOQF} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Quantum Observables of Quantized Fluxes]]*, Annales Henri Poincaré (2024) &lbrack;[arXiv:2312.13037](https://arxiv.org/abs/2312.13037), [doi:10.1007/s00023-024-01517-z](https://doi.org/10.1007/s00023-024-01517-z)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Flux Quantization]]*, [[Encyclopedia of Mathematical Physics 2nd ed]] **4** (2025) 281-324 &lbrack;[arXiv:2402.18473](https://arxiv.org/abs/2402.18473), [doi:10.1016/B978-0-323-95703-8.00078-1](https://doi.org/10.1016/B978-0-323-95703-8.00078-1)&rbrack;

* {#SS24IHH} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Introduction to Hypothesis H]]*, lecture notes (2024-)

[[!redirects non-perturbative QFT]]

[[!redirects non-perturbative quantum field theories]]

[[!redirects non-perturbative field theory]]
[[!redirects non-perturbative field theories]]


[[!redirects nonperturbative quantum field theory]]
[[!redirects nonperturbative quantum field theories]]

[[!redirects nonperturbative QFT]]
[[!redirects nonperturbative QFTs]]

[[!redirects non-perturbative physics]]
