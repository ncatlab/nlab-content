
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

An _orientifold_ ([Dai-Lin-Polchinski 89, p. 12](#DaiLinPolchinski89)) is a [[target space|target]] [[spacetime]] for [[string theory|string]] [[sigma-models]] that combines aspects of $\mathbb{Z}_2$-[[orbifold]]s with _[[orientation]] reversal_ on the worldsheet, whence the name.

In [[type II string theory]] orientifold backgrounds (inducing [[type I string theory]]) with $\mathbb{Z}_2$-[[fixed points]] -- called _[[O-planes]]_ (see there for more) --  are required for [[RR-field tadpole cancellation]]. This is a key consistency condition in particular for [[intersecting D-brane models]] used in [[string phenomenology]].

Where generally ([[higher gauge field|higher gauge]]) [[field (physics)|fields]] in [[physics]]/[[string theory]] are [[cocycles]] in ([[differential cohomology theory|differential]]) [[cohomology theory]] and typically in [[complex oriented cohomology theory]], fields on orientifolds are cocycles in genuinely $\mathbb{Z}_2$-[[equivariant cohomology]] and typically in [[real-oriented cohomology theory]]. For instance, the [[B-field]], which otherwise is a (twisted) cocycle in ([[ordinary differential cohomology|ordinary]]) [[differential cohomology]], over an orientifold is a cocycle in (twisted) [[HZR-theory]], and the [[RR-fields]], which usually are cocycles in ([[twisted cohomology|twisted]] [[differential K-theory|differential]]) [[K-theory]], over an orientifold are cocycles in [[KR-theory]] ([Witten 98](#Witten98)).

An explicit model for [[B-fields]] for the [[bosonic string]]  on orientifolds (differential [[HZR-theory]]) is given in ([Schreiber-Schweigert-Waldorf 05](#Jandl)) and examples are analyzed in this context in ([Gawedzki-Suszek-Waldorf 08](#GawedzkiSuszekWaldorf08)). See also ([HMSV 16](#HMSV16), [HMSV 19](#HMSV19)).

The claim that for the [[superstring]] the B-field is more generally a cocycle with coefficients in the [[Picard infinity-group]] of [[complex K-theory]] ([[super line 2-bundles]]) and a detailed discussion of the orientifold version of this can be found in ([Distler-Freed-Moore 09](#Precis), [Distler-Freed-Moore 10](#DistlerFreedMooreII)) with details in ([Freed 12](#Freed)).

The quadratic pairing entering the [[11d Chern-Simons theory]] that governs the [[RR-field]] here as a [[self-dual higher gauge field]] is given in ([DFM 10, def. 6](#Precis)).

## Properties

### Orientifold backreaction?
 {#OrientifoldBackreactionOrNot}

Essentially all existing results on orientifolds (such as [[O-plane]]-charges and [[RR-field tadpole cancellation]]) are derived for string [[sigma-models]] on [[flat orbifold]] ([[toroidal orbifold]]) or orientifolded [[Calabi-Yau manifold]] [[target spacetimes]], or for orientifoldings of algebraically defined [[rational CFT]] [[string vacua]] ([[Gepner models]], [[non-geometric vacua]]).

#### No string-theory results on back-reacted orientifolds
 {#NoResultOnBackreactedOrientifolds}
 
There are to date no results in actual [[string theory]] for what one might expect to be the curved back-reacted geometry of [[orientifolds]], analogous to the curved [[near horizon geometry]] that is well-known for the case of [[black brane|black]] [[D-branes]].

From [Banks-van den Broeck 06](#BanksBroeck06):

> The discussion of these $[$orientifold$]$ compactifications is generally carried out in low energy [[effective field theory]] $[$[3a](https://arxiv.org/abs/hep-th/0412277), [3b](https://arxiv.org/abs/hep-th/0506066) $]$ $[$[4](https://arxiv.org/abs/hep-th/0412129)$]$, despite the fact that they all contain [[orientifold]] [[singularities]]. Further, there is no [[perturbative string theory|perturbative world sheet treatment]] of these backgrounds.

> $[...]$

> The inevitable orientifold of [[flux compactifications]] is one potential barrier to an [[effective field theory]] treatment $[$footnote 1 : [[Greg Moore|G. Moore]] and S. Ramanujam have emphasized to us the problems with the back reaction of the orientifold $[...$] $]$


From [Cordova-de Luca-Tomasiello 19](#CordovaLucaTomasiello19) (p. 2 and p. 30):

> To assess the validity  of these $[$assumed effective orientifold$]$ solutions in [[string theory]], one should  ideally use the full string theory action, or  switch to a [[duality in string theory|dual]] description. Unfortunately neither of  these options is available

> $[...]$

> the presence of [[O-planes]] is inferred by comparison with their flat-space behavior. Since the $[$spacetimes with orientifolds considered$]$ have strong curvature and coupling, [[higher curvature corrections|stringy corrections]] come into play, and it is impossible to decide with [[supergravity]] alone whether the solutions are valid.  

> It is important to stress that this will be so for any solution with [[O-planes]]. It would be important, then,to develop techniques to decide  whether a solution with O-planes will survive in full string theory.  In other words, it would be important to understand what conditions one needs  to impose near the [[O-plane]] [[singularities]].

> $[...]$

>  We clearly need alternative procedures that are better justified physically.


#### A popular assumption in effective field theory
 {#AnAssumptionInEffectiveFieldTheory}

Nevertheless, motivated from the fact that the computations for [[flat orbifolds]] show that the [[O-planes]] there are similar to (while clearly different from!) [[D-branes]] (*not* in their back-reacted form as [[black branes]], though!) with [[negative number|negative]] tension (i.e. negative [[energy]] density) it may seem plausible that the low energy [[effective field theory]] of [[perturbative string theory vacua]] including [[O-planes]] is a modification of [[supergravity]] where negative-energy source-terms are added to the [[equations of motion]] much like one might add [[black brane|black]] [[D-brane]]-contributions, but simply equipped with a negative sign prefactor.

This _ad hoc_ effective field theory picture of orientifold backgrounds has been advocated, seminally, in [Giddings-Kachru-Polchinski 01](#GiddingsKachruPolchinski01), in a one-sentence argument (below (2.19)):

> String theory does have such $[$negative tension$]$ objects, and so evades the no-go theorem $[$which rules out certain warped solutions of supergravity$]$.

There this is followed by reference to a presumed example considered earlier in [Verlinde 00](#Verlinde00), where the statement is introduced in a similar manner (above (9)):

> In a more complete treatment, we must also include the backreaction of the 64 orientifold planes. These have a negative tension equal to −1/4 times the D3-brane tension, which need to be taken into account. We can write an explicit form for the background metric $[$just as for D-branes but with a minus sign included$]$.

One may feel this is plausible -- and it might even be right, sometimes -- but there does not exist a derivation of this statement from actual [[perturbative string theory]] (see [above](#NoResultOnBackreactedOrientifolds)), beyond the hand-waving leap of faith extrapolating from perturbative string theory on flat orientifolds to curved backreacted orientifold throat geometries (if such indeed exist).

#### Its use in the landscape/swampland literature
 {#UseInLandscapeSwamplandLiterature}

Nevertheless, in the wake of the discussion of the [[landscape of string theory vacua|landscape]] (or not) of [[de Sitter spacetime|de Sitter]] [[string theory vacua]] and of the "[[swampland conjectures]]" it became popular to rely on the handwaving argument of [Giddings-Kachru-Polchinski 01](#GiddingsKachruPolchinski01) and behave as if it is established that questions about [[effective field theory|low energy effective]] [[orientifold]] [[string theory vacua]] may be answered using a modification of [[supergravity]] where the [[equations of motion]] are changed -- by hand -- simply by including negative-tension source terms of some form. 

This step happens for instance around (2.2) in [Junghans 20](#Junghans20) where it is justified, without references, by the words "as is standard in the literature" (footnote 5 in [Junghans 20](#Junghans20)).


\linebreak

### Lifts to M-theory F-theory

Lifts of orientifold background from [[type II string theory]] to [[F-theory]] go back to ([Sen 96](#Sen96), [Sen 97a](#Sen97a)). 

Lifts of [[type IIA string theory]] orientifolds of [[D6-branes]] to [[ADE singularities|D-type ADE singularities]] in [[M-theory]] (through the [[duality between M-theory and type IIA string theory]]) goes back to ([Sen 97b](#Sen97b)). See at _[[heterotic M-theory on ADE-orbifolds]]_.

A more general scan of possible lifts of type IIA orientifolds to M-theory is indicated in ([Hanany-Kol 00, around (3.2)](#HananyKol00)), see ([Huerta-Sati-Schreiber 18, Prop. 4.7](#HuertaSatiSchreiber18)) for details.

For instance the [[O4-plane]] lifts to the [[MO5-plane]].

(...)

## Related concepts

* [[fractional D-brane]]
 
  [[permutation D-brane]]

* [[O-plane]], 

  [[O-plane charge]], 

  [[RR-field tadpole cancellation]]

* [[worldsheet parity operator]]

* [[type I string theory]]

* [[real-oriented cohomology theory]]

* [[higher orientifold]]



## References
 {#References}


### General

The concept originates around


* {#DaiLinPolchinski89} Jin Dai, [[Robert Leigh]], [[Joseph Polchinski]], p. 12 of _New Connections Between String Theories_, Mod. Phys. Lett. A4 (1989) 2073-2083 ([spire:25758](http://inspirehep.net/record/25758), [pdf scan](https://lib-extopc.kek.jp/preprints/PDF/1989/8905/8905564.pdf))



Early accounts include

* {#Mukhi97} [[Sunil Mukhi]], _Orientifolds: The Unique Personality Of Each Spacetime Dimension_, [Workshop on Frontiers of Field Theory, Quantum Gravity and String Theory, Puri, India, 12 - 21 Dec 1996](http://cds.cern.ch/record/323857) ([arXiv:hep-th/9710004](https://arxiv.org/abs/hep-th/9710004), [cern:335233](http://cds.cern.ch/record/335233))

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], section 3 of _Triples, Fluxes, and Strings_, Adv. Theor. Math. Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))


Traditional lecture notes include

* [[Atish Dabholkar]], _Lectures on Orientifolds and Duality_, In *Trieste 1997, High energy physics and cosmology* 128-191 ([arXiv:hep-th/9804208](https://arxiv.org/abs/hep-th/9804208), [spire:454332](https://inspirehep.net/literature/454332))

* Carlo Angelantonj, [[Augusto Sagnotti]], _Open Strings_, Phys. Rept. 371:1-150,2002; Erratum ibid.376:339-405, 2003 ([arXiv:hep-th/0204089](https://arxiv.org/abs/hep-th/0204089))

Textbook discussion is in

* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Section 15.3 of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics, Springer 2013

and specifically in the context of [[intersecting D-brane models]] with an eye towards [[string phenomenology]] in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], sections 5.3.4 and 10.1.3 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

Exposition:

* Marcus Berg, _Introduction to Orientifolds_ ([pdf](https://tp.hotell.kau.se/marcus/physics/talks/orienti_short.pdf), [[BergOrientifolds.pdf:file]])

The original observation that [[D-brane charge]] for orientifolds should be in [[KR-theory]] is due to

* {#Witten98} [[Edward Witten]], section 5 of _D-branes and K-theory_, J. High Energy Phys., 1998(12):019, 1998 ([arXiv:hep-th/9810188](http://arxiv.org/abs/hep-th/9810188)) 

and was re-amplified in

* {#Gukov00} [[Sergei Gukov]], _K-Theory, Reality, and Orientifolds_, Commun.Math.Phys. 210 (2000) 621-639 ([arXiv:hep-th/9901042](http://arxiv.org/abs/hep-th/9901042))

### In terms of KO-theory

Discussion of orbi-orienti-folds in terms of [[equivariant K-theory|equivariant]] [[KO-theory]] is in

* N. Quiroz, [[Bogdan Stefanski]], _Dirichlet Branes on Orientifolds_, Phys.Rev. D66 (2002) 026002 ([arXiv:hep-th/0110041](https://arxiv.org/abs/hep-th/0110041))

* [[Volker Braun]], [[Bogdan Stefanski]], _Orientifolds and K-theory_, Braun, Volker. "Orientifolds and K-theory." Progress in String, Field and Particle Theory. Springer, Dordrecht, 2003. 369-372 ([arXiv:hep-th/0206158](https://arxiv.org/abs/hep-th/0206158))

* H. Garcia-Compean, W. Herrera-Suarez, B. A. Itza-Ortiz, O. Loaiza-Brito, _D-Branes in Orientifolds and Orbifolds and Kasparov KK-Theory_, JHEP 0812:007, 2008 ([arXiv:0809.4238](https://arxiv.org/abs/0809.4238))

A definition and study of orientifold [[bundle gerbes]], modeling the [[B-field]] [[background gauge field|background]] for the [[bosonic string]] (differential [[HZR-theory]]), is in

* {#Jandl} [[Urs Schreiber]], [[Christoph Schweigert]], [[Konrad Waldorf]], _Unoriented WZW models and Holonomy of Bundle Gerbes_, Communications in Mathematical Physics August 2007, Volume 274, Issue 1, pp 31-64 ([arXiv:hep-th/0512283](http://arxiv.org/abs/hep-th/0512283))


* {#GawedzkiSuszekWaldorf08} [[Krzysztof Gawedzki]], Rafal R. Suszek,  [[Konrad Waldorf]], _Bundle Gerbes for Orientifold Sigma Models_ Adv. Theor. Math. Phys. 15(3), 621-688 (2011) ([arXiv:0809.5125](http://arxiv.org/abs/0809.5125))

see also

* {#HMSV16} [[Pedram Hekmati]], [[Michael Murray]], [[Richard Szabo]], [[Raymond Vozzo]], _Real bundle gerbes, orientifolds and twisted KR-homology_ ([arXiv:1608.06466](http://arxiv.org/abs/1608.06466))

* {#HMSV19} [[Pedram Hekmati]], [[Michael Murray]], [[Richard Szabo]], [[Raymond Vozzo]], _Sign choices for orientifolds_, Commun. Math. Phys. 378, 1843–1873 (2020) ([arXiv:1905.06041](https://arxiv.org/abs/1905.06041))

An elaborate formalization in terms of [[differential cohomology]] in general and [[twisted K-theory|twisted]] [[differential K-theory]] in particular that also takes the spinorial degrees of freedom into account is briefly sketched out in

* {#Precis} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 
based on stuff like

* {#BergmanGimonSugimoto01} [[Oren Bergman]], [[Eric Gimon]], [[Shigeki Sugimoto]], _Orientifolds, RR Torsion, and K-theory_, JHEP 0105:047, 2001 ([arXiv:hep-th/0103183](https://arxiv.org/abs/hep-th/0103183))

Details on the computation of [[string scattering amplitudes]] in such a background:

* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_, Surveys in Differential Geometry, Volume 15 (2010) ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581), [doi:10.4310/SDG.2010.v15.n1.a4](http://dx.doi.org/10.4310/SDG.2010.v15.n1.a4))
 
Related lecture notes / slides include

* [[Daniel Freed]], _Dirac charge quantization, K-theory, and orientifolds_, talk at a workshop _Mathematical methods in general relativity and quantum field theories_, Paris, November 2009 ([pdf](http://www.ma.utexas.edu/users/dafr/paris_nt.pdf), [[FreedK09.pdf:file]])

* {#Moore10} [[Greg Moore]], _The RR-charge of an orientifold_, Oberwolfach talk 2010 ([pdf](https://www.physics.rutgers.edu/~gmoore/Oberwolfach_June2010_FINAL.pdf), [[MooreOrientifold2010.pdf:file]], [ppt](http://www.physics.rutgers.edu/~gmoore/AnnArbor_Feb2010_FINAL.ppt))

* {#Freed} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lecures at _[K-Theory and Quantum Fields](http://www.esi.ac.at/activities/events/2012/k-theory-and-quantum-fields)_, ESI 2012 ([[FreedESI2012.pdf:file]])
 

A detailed list of examples of [[KR-theory]] of orientifolds and their [[T-duality]] is in 

* {#DMR13} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _T-duality For Orientifolds and Twisted KR-theory_ ([arXiv:1306.1779](http://arxiv.org/abs/1306.1779))

* {#DMR14} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _String theory on elliptic curve orientifolds and KR-theory_ ([arXiv:1402.4885](http://arxiv.org/abs/1402.4885))


A formulation of some of the relevant aspects of (bosonic) orientifolds in terms of the  [[schreiber:differential cohomology in an (∞,1)-topos -- survey|differential nonabelian cohomology]] with coefficients in the [[2-group]] $AUT(U(1))$ coming from the [[crossed module]] $[U(1) \to \mathbb{Z}_2]$ is indicated in 

* [[Urs Schreiber]],  talk [[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]] at [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]] 

More on this in section 3.3.10 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


### Examples and Models
 {#ReferencesExamplesAndModels}


Specifically [[K3]] [[orientifolds]] ($\mathbb{T}^4/G_{ADE}$) in [[type IIB string theory]], hence for [[D9-branes]] and [[D5-branes]]:

* [[Eric Gimon]], [[Joseph Polchinski]], Section 3.2 of: _Consistency Conditions for Orientifolds and D-Manifolds_, Phys. Rev. D54: 1667-1676, 1996 ([arXiv:hep-th/9601038](https://arxiv.org/abs/hep-th/9601038))

* {#GimonJohnson96} [[Eric Gimon]], [[Clifford Johnson]], _K3 Orientifolds_, Nucl. Phys. B477: 715-745, 1996 ([arXiv:hep-th/9604129](https://arxiv.org/abs/hep-th/9604129))

* {#BuchelShiuTye99} Alex Buchel, [[Gary Shiu]], S.-H. Henry Tye, _Anomaly Cancelations in Orientifolds with Quantized B Flux_, Nucl.Phys. B569 (2000) 329-361 ([arXiv:hep-th/9907203](https://arxiv.org/abs/hep-th/9907203))

* P. Anastasopoulos, A. B. Hammou, _A Classification of Toroidal Orientifold Models_, Nucl. Phys. B729:49-78, 2005 ([arXiv:hep-th/0503044](https://arxiv.org/abs/hep-th/0503044))

Specifically [[K3]] [[orientifolds]] ($\mathbb{T}^4/G_{ADE}$) in [[type IIA string theory]], hence for [[D8-branes]] and [[D4-branes]]:

* {#ParkUranga98} [[Jaemo Park]], [[Angel Uranga]], _A Note on Superconformal $\mathcal{N}=2$ theories and Orientifolds_, Nucl. Phys. B542:139-156, 1999 ([arXiv:hep-th/9808161](https://arxiv.org/abs/hep-th/9808161))


* {#AFIRU00a} G. Aldazabal, S. Franco, [[Luis Ibanez]], R. Rabadan, [[Angel Uranga]], _D=4 Chiral String Compactifications from Intersecting Branes_, J. Math. Phys. 42:3103-3126, 2001 ([arXiv:hep-th/0011073](https://arxiv.org/abs/hep-th/0011073))

* {#AFIRU00b} G. Aldazabal, S. Franco, [[Luis Ibanez]], R. Rabadan, [[Angel Uranga]], _Intersecting Brane Worlds_, JHEP 0102:047, 2001 ([arXiv:hep-ph/0011132](https://arxiv.org/abs/hep-ph/0011132))

* {#KataokaShimojo01} H. Kataoka, M. Shimojo, _$SU(3) \times SU(2) \times U(1)$ Chiral Models from Intersecting D4-/D5-branes_, Progress of Theoretical Physics, Volume 107, Issue 6, June 2002, Pages 1291–1296 ([arXiv:hep-th/0112247](https://arxiv.org/abs/hep-th/0112247), [doi:10.1143/PTP.107.1291](https://doi.org/10.1143/PTP.107.1291))

> The $\mathbb{Z}_N$ action with even $N$ contains an order 2 element $[ ...]$  Then there will be D8-branes in the type IIA D4-brane theory. Since the concept of intersecting D-branesinvolves use of the same dimensional D-branes, we restrict ourselves to the case that the order $N$ of $\mathbb{Z}_N$ is odd. ([p. 4](https://arxiv.org/pdf/hep-th/0112247.pdf#page=4))

* {#Honecker01} [[Gabriele Honecker]], _Non-supersymmetric Orientifolds with D-branes at Angles_, Fortsch.Phys. 50 (2002) 896-902 ([arXiv:hep-th/0112174](https://arxiv.org/abs/hep-th/0112174))

* {#Honecker02a} [[Gabriele Honecker]], _Intersecting brane world models from D8-branes on $(T^2 \times T^4/\mathbb{Z}_3)/\Omega\mathcal{R}_1$ type IIA orientifolds_, JHEP 0201 (2002) 025 ([arXiv:hep-th/0201037](https://arxiv.org/abs/hep-th/0201037))

* {#Honecker02b} [[Gabriele Honecker]], _Non-supersymmetric orientifolds and chiral fermions from intersecting D6- and D8-branes_, thesis 2002 ([[HoneckerIntersectingDBraneModels02.pdf:file]])

The [[Witten-Sakai-Sugimoto model]] on [[D4-D8-brane bound states]] for [[QCD]] with [[orthogonal group|orthogonal]] [[gauge groups]] on O-planes:

* {#ImotoSakaiSugimoto09} Toshiya Imoto, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _$O(N)$ and $USp(N)$ QCD from String Theory_, Prog.Theor.Phys.122:1433-1453, 2010 ([arXiv:0907.2968](https://arxiv.org/abs/0907.2968))

* Hee-Cheol Kim, Sung-Soo Kim, Kimyeong Lee, _5-dim Superconformal Index with Enhanced $E_n$ Global Symmetry_, JHEP 1210 (2012) 142 ([arXiv:1206.6781](https://arxiv.org/abs/1206.6781))




Specifically D5 brane models [[T-duality|T-dual]] to D6/D8 models:

* [[Angel Uranga]], _A New Orientifold of $\mathbb{C}^2/\mathbb{Z}_N$ and Six-dimensional RG Fixed Points_, Nucl. Phys. B577:73-87, 2000 ([arXiv:hep-th/9910155](https://arxiv.org/abs/hep-th/9910155))

* {#FengHeKarchUranga01} Bo Feng, [[Yang-Hui He]], [[Andreas Karch]], [[Angel Uranga]], _Orientifold dual for stuck NS5 branes_, JHEP 0106:065, 2001 ([arXiv:hep-th/0103177](https://arxiv.org/abs/hep-th/0103177))


Specifically for [[D6-branes]]:

* {#IshiharaKataokaSato99} S. Ishihara, H. Kataoka, Hikaru Sato, _$D=4$, $N=1$, Type IIA Orientifolds_, Phys. Rev. D60 (1999) 126005 ([arXiv:hep-th/9908017](https://arxiv.org/abs/hep-th/9908017))

* [[Mirjam Cvetic]], Paul Langacker, Tianjun Li, Tao Liu, _D6-brane Splitting on Type IIA Orientifolds_, Nucl. Phys. B709:241-266, 2005 ([arXiv:hep-th/0407178](https://arxiv.org/abs/hep-th/0407178))

Specifically for [[D3-branes]]/[[D7-branes]]:

* [Feng-He-Karch-Uranga 01](#FengHeKarchUranga01)

Specifically 2d [[toroidal orbifold|toroidal]] orientifolds:

2d toroidal [[orientifolds]]:

* Dongfeng Gao, [[Kentaro Hori]], Section 7.3 of: _On The Structure Of The Chan-Paton Factors For D-Branes In Type II Orientifolds_ ([arXiv:1004.3972](https://arxiv.org/abs/1004.3972))

* {#DMR14} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _String theory on elliptic curve orientifolds and KR-theory_ ([arXiv:1402.4885](http://arxiv.org/abs/1402.4885))

Various:

* [[Dieter Lüst]], S. Reffert, E. Scheidegger, S. Stieberger, _Resolved Toroidal Orbifolds and their Orientifolds_, Adv.Theor.Math.Phys.12:67-183, 2008 ([arXiv:hep-th/0609014](https://arxiv.org/abs/hep-th/0609014))


### Orientifold Gepner models

Orientifolds of [[Gepner models]]

* Brandon Bates, [[Charles Doran]], Koenraad Schalm, _Crosscaps in Gepner Models and the Moduli space of $T^2$ Orientifolds_, Advances in Theoretical and Mathematical Physics, Volume 11, Number 5, 839-912, 2007 ([arXiv:hep-th/0612228](https://arxiv.org/abs/hep-th/0612228))


Specifically [[string phenomenology]] and the [[landscape of string theory vacua]] of Gepner model [[orientifold]] compactifications:

* {#DijkstraHuiszoonSchellekens04a} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Chiral Supersymmetric Standard Model Spectra from Orientifolds of Gepner Models_, Phys.Lett. B609 (2005) 408-417 ([arXiv:hep-th/0403196](https://arxiv.org/abs/hep-th/0403196))

* {#DijkstraHuiszoonSchellekens04b} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl.Phys.B710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))


### Lift to M-theory
 {#ReferencesInMTheory}


Lifts of orientifolds to [[M-theory]] ([[MO5]], [[MO9]]) and [[F-theory]] are discussed in

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_ ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))

* {#Sen97a} [[Ashoke Sen]], _Orientifold Limit of F-theory Vacua_ ([arXiv:hep-th/9702165](http://arxiv.org/abs/hep-th/9702165))

* {#Sen97b} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))




* {#Hori98} [[Kentaro Hori]], _Consistency Conditions for Fivebrane in M Theory on $\mathbb{R}^5/\mathbb{Z}_2$ Orbifold_, Nucl. Phys. B539:35-78, 1999 ([arXiv:hep-th/9805141](https://arxiv.org/abs/hep-th/9805141))


* {#Gimon98} [[Eric Gimon]], _On the M-theory Interpretation of Orientifold Planes_ ([arXiv:hep-th/9806226](https://arxiv.org/abs/hep-th/9806226), [spire:472499](http://inspirehep.net/record/472499))

* {#AKY98} Changhyun Ahn, Hoil Kim, Hyun Seok Yang, _$SO(2N)$ $(0,2)$ SCFT and M Theory on $AdS_7 \times \mathbb{R}P^4$_, Phys.Rev. D59 (1999) 106002 ([arXiv:hep-th/9808182](https://arxiv.org/abs/hep-th/9808182))


* {#HananyKol00} [[Amihay Hanany]], [[Barak Kol]], section 4 of _On Orientifolds, Discrete Torsion, Branes and M Theory_, JHEP 0006 (2000) 013 ([arXiv:hep-th/0003025](https://arxiv.org/abs/hep-th/0003025))

* {#ArgyresMaimonPelland02} [[Philip Argyres]], [[Ron Maimon]], Sophie Pelland, _The M theory lift of two O6 planes and four D6 branes_, JHEP 0205 (2002) 008 ([arXiv:hep-th/0204127](https://arxiv.org/abs/hep-th/0204127))

  following

* [[Edward Witten]], _Solutions Of Four-Dimensional Field Theories Via M Theory_, ([arXiv:hep-th/9703166](https://arxiv.org/abs/hep-th/9703166))

The [[MO5]] is originally discussed in 

* Keshav Dasgupta, [[Sunil Mukhi]], _Orbifolds of M-theory_, Nucl. Phys. B465 (1996) 399-412 ([arXiv:hep-th/9512196](https://arxiv.org/abs/hep-th/9512196))

* {#Witten95} [[Edward Witten]], _Five-branes And M-Theory On An Orbifold_, Nucl. Phys. B463:383-397, 1996 ([arXiv:hep-th/9512219](https://arxiv.org/abs/hep-th/9512219))

See also:

* [[Andreas Braun]], _M-Theory and Orientifolds_ ([arXiv1912.06072](https://arxiv.org/abs/1912.06072))



The classification in [Hanany-Kol 00 (3.2)](#HananyKol00) also appears, with more details, in Prop. 4.7 of

* {#HuertaSatiSchreiber18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))


The "higher orientifold" appearing in [[Horava-Witten theory]] with circle 2-bundles replaced by the [[circle n-bundle with connection|circle 3-bundles]] of the [[supergravity C-field]] is discussed towards the end of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field|The E8 moduli 3-stack of the C-field in M-theory]]_ ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455))

### Orientifold backreaction

* {#Verlinde00} [[Herman Verlinde]], _Holography and Compactification_, Nucl. Phys. B580 (2000) 264-274 ([arXiv:hep-th/9906182](https://arxiv.org/abs/hep-th/9906182))

* {#GiddingsKachruPolchinski01} [[Steven Giddings]], [[Shamit Kachru]], [[Joseph Polchinski]], _Hierarchies from Fluxes in String Compactifications_, Phys. Rev. D66:106006, 2002 ([arXiv:hep-th/0105097](https://arxiv.org/abs/hep-th/0105097))

* {#BanksBroeck06} [[Tom Banks]], K. van den Broek, _Massive IIA flux compactifications and U-dualities_, JHEP 0703:068, 2007 ([arXiv:hep-th/0611185](https://arxiv.org/abs/hep-th/0611185))

* {#CordovaLucaTomasiello19} [[Clay Cordova]], G. Bruno De Luca, [[Alessandro Tomasiello]], _New de Sitter Solutions in Ten Dimensions and Orientifold Singularities_ ([arXiv:1911.04498](https://arxiv.org/abs/1911.04498))

* {#Junghans20} Daniel Junghans, _O-plane Backreaction and Scale Separation in Type IIA Flux Vacua_ ([arXiv:2003.06274](https://arxiv.org/abs/2003.06274))



[[!redirects orientifolds]]
