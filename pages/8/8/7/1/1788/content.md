
> under construction



\linebreak

> this entry is one chapter of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- fundamental super p-branes|fundamental super p-branes]]_

\linebreak

\linebreak


#Contents#
* table of contents
{:toc}


> **Abstract**

> [[flux|Flux]]- & [[charge]][[flux quantization|-quantization]] laws for [[higher gauge theories]] of [[Maxwell theory|Maxwell]]-type --- e.g. the common [[electromagnetic field]] but also the [[B-field|B-]], [[RR-field|RR-]], and [[supergravity|C-fields]] considered in [[string theory|string]]/[[M-theory]] --- specify [[non-perturbative quantum field theory|non-perturbative completions]] of these [[higher gauge fields]] by encoding their [[soliton|solitonic]] behaviour and hence the quantized [[charges]] carried by the [[branes]] that source these fluxes.
>
> This pages surveys the general ([[rational homotopy theory|rational]]-)[[homotopy theory|homotopy theoretic]] understanding of flux- & charge-quantization via the [[Chern-Dold character map]] generalized to the non-linear [[Bianchi identities]] appearing in higher-dimensional [[supergravity]] theories, notably for the [[supergravity C-field|C-field in 11d]]. 
>
> While flux quantization applies already to [[classical field theory|classical]] gauge fields and might seem to be better called *flux discretization*, for disambiguation, the choice involved in flux quantization induces the actual [[nLab:strict deformation quantization]] of [[observables]] on fluxes and hence may be understood as part of actual [[quantization]] in the sense of *[[quantum field theory]]*, [[non-perturbative quantum field theory|non-perturbatively]].
>
> With higher flux quantization thus being a key aspect of the general formulation of [[non-perturbative quantum field theory]], which as a whole remains a major open problem of [[mathematical physics|mathematical]] [[theoretical physics]], it is instructive to understand it as a stage in the historical development towards this goal:
>
> * In 1852 [[Michael Faraday|Faraday]] observes [[magnetic field]] [[flux lines]] emanating from magnetic poles &lbrack;[Faraday 1852](#Faraday1852)&rbrack;. 
>   
> * In 1931 [[P. A. M. Dirac|Dirac]] invokes [[quantum mechanics]] to argue that, if there were unpaired such (mono-)poles, then the total flux emanating from them --- and thus the magnetic charge carried by them --- had to come in [[integer]] multiples of a unit quantum &lbrack;[Dirac 1931](#Dirac31)&rbrack;. 
>
> * In the 1950s, while magnetic monopoles remain unobserved, [[Alexei Abrikosov|Abrikosov]] observes that the same electromagnetic flux- & charge-quantization mechanism makes [[Abrikosov vortex|vortex strings]] in [[type II superconductors]] carry units of localized magnetic flux.  &lbrack;[Abrikosov 1957](#Abrikosov57a)&rbrack;
>   
> * In 1985 [[Orlando Alvarez|Alvarez]] understands such *[[soliton|solitonic]]* [[magnetic fields]] as [[cocycles]] in ([[differential ordinary cohomology|differential]]) [[ordinary cohomology]]. &lbrack;[Alvarez 1985](#Alvarez85a)&rbrack;
>
> * In the 1990s [[string theory|string theorists]] argue that the combined flux of [[B-field|B-]] & [[RR-fields]] and hence the charge of [[D-branes]] is analogously quantized in the generalized cohomology theory called "[[twisted K-theory|twisted topological K-theory]]" &lbrack;[Minasian & Moore 1997](#MinasianMoore97); [Witten 1998](#Witten98)&rbrack;; 
>
>   and that the flux of the [[supergravity C-field|C-field]] and hence the charge of [[M-branes]] is quantized in a "[[shifted C-field flux quantization|shifted half-integral]]" cohomology theory &lbrack;[Witten 1996](#Witten96a)&rbrack; which long remains mysterious. 
>
> * In recent years [FSS 2020](#FSS20) have developed a systematic understanding of flux quantization of any higher gauge theory of Maxwell-type in generalized [[non-abelian cohomology]] theory, using [[fundamental theorem of dg-algebraic rational homotopy theory|tools from dg-algebraic]] [[rational homotopy theory]] related to the [[D'Auria-Fre formulation of supergravity|"FDA-method" in the supergravity literature]]. 
>
>   This provides a transparent re-derivation of known flux quantization laws and it allows to finally discuss C-field flux/M-brane charge quantization.

\linebreak

**Overview.** In [[higher gauge theories]] (review in [Alfonsi 2024, §2](#Alfonsi24); [BFJ${}^+$ 2024](#BFJKNRSW24); and our [§1](#FluxDensitiesAndBraneSources) below), 

* *[[flux]]* of *[[field (physics)|fields]]* is sourced by *[[charge|charged]] [[branes]]* ([§1](#FluxDensitiesAndBraneSources)), 

* *[[flux quantization]]* forces total fluxes/charges to form a [[discrete space]], reflecting individual [[soliton|solitonic]] brane sources ([§2](#FluxQuantizationLaws)).

A *choice* of flux quantization is 

* a hypothesis about or

* a specification of 

the [[non-perturbative quantum field theory|non-perturbative completion]] of the given [[higher gauge theory]].

Traditionally, flux quantization laws have been postulated in an ad-hoc fashion in order to patch up "anomalous" theories: 
Since the ancient past, it is common to define any [[theory (physics)|physical theory]] by a [[stationary action principle]] embodied by a [[Lagrangian density]], from which a perturbative [[BRST complex]] is extracted, whose [[quantization]] (e.g. [Henneaux & Teitelboim 1992](#HenneauxTeitelboim92)) is generally afflicted with problems ("[[quantum anomalies|anomalies]]") some of which are dealt with by ad-hoc flux quantization: For example the original [[Dirac charge quantization]] was postulated to cure an anomaly in the quantum theory of an [[electron]] propagating in the background field of a [[magnetic monopole]] (a "0-brane"), while the enigmatic [[shifted C-field flux quantization]] similarly serves to cure an anomaly in the quantum theory of the [[M2-brane]] propagating in the background field of an [[M5-brane]] ([Witten 1996a, §2.2](#Witten96a)).

In contrast, in the modernized picture reviewed here, the available choices of flux-quantization laws $\mathcal{A}$ are [[algebraic topology|algebro-topologically]] determined by the form of the higher [[Gauss law]] on any [[Cauchy surface]], and any such choice given by a compatible [[non-abelian cohomology]]-theory, determines the [[non-perturbative quantum field theory|non-perturbative]] [[phase space]] [[smooth infinity-stack|stack]] of flux-quantized gauge fields. This process makes no reference to [[variational calculus]] on a [[Lagrangian density]] and applies seamlessly to field theories that do not even have a natural Lagrangian description, such as [[self-dual higher gauge theories]].

Typically there is an evident choice of flux quantization which is the choice made in the literature, where considered, but it is important to notice that there are other admissible choices, embodying hypotheses about or definitions of non-evident nonperturbative completions of the given higher gauge theory.

The following table shows in outline the logic of algebra-topological flux quantization, on the left in generality and on the right for our three running examples:

1. Traditional [[Dirac charge quantization]] of the [[electromagnetic field]] (experimentall well-supported)

1. traditional [[D-brane charge quantization in topological K-theory|D-brane charge quantization]] in [[twisted K-theory|twisted]] [[topological K-theory]] ("Hypothesis K", still facing various challenges)

1. more recent [[M-brane]]$\;$[[shifted C-field flux quantization|charge quantization]] in unstable [[twisted Cohomotopy|twisted]] [[Cohomotopy]] ("[[schreiber:Hypothesis H]]").


\begin{imagefromfile}
    "file_name": "GeomPhys-FluxQuantizationSurvey.jpg",
    "width": 850,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


As the above table indicates, the [[algebraic topology|algebro-topological]] nature of flux/charge quantization is [[higher Lie theory|higher Lie theoretic]] (explained in [§2](#FluxQuantizationLaws)), by matching two [[L-infinity algebras|$L_\infty$-algebras]] associated with a given [[higher gauge theory]] of Maxwell type ([§1](#FluxDensitiesAndBraneSources)):

1. The higher [[Gauss law]] of a [[higher gauge theory]] of Maxwell-type is equivalent to the condition that the [[flux densities]] jointly constitute a [[flat L-infinity algebra valued differential form|closed $L_\infty$-algebra valued differential form]] for a characteristic [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$;

1. The [[classifying space]] $\mathcal{A}$ of the topological flux/charge sector is [[rational homotopy type|rationally]] characterized by its [[rational numbers|rational]] [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]]  $\mathfrak{l}\mathcal{A}$ (essentially the "Quillen model" of $\mathcal{A}$: that $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{l}\mathcal{A})$ is the [[Sullivan model]] of $\mathcal{A}$).
 
That these two $L_\infty$-algebras coincide is the condition on the choice of the flux quantization law embodied by $\mathcal{A}$, because it implies that the non-abelian [[Chern-Dold character map]] from the [[non-abelian cohomology]]-theory classified by $\mathcal{A}$ takes values in the [[non-abelian de Rham cohomology]] with coefficients in $\mathfrak{l}\mathcal{A}$, which under $\mathfrak{l}\mathcal{A} \simeq \mathscr{a}$ identifies with the deformation classes of [[flux densities]] satisfying their higher [[Gauss law]].

In comparison to more traditional discussions, beware that the (possibly non-abelian) $L_\infty$-algebra $\mathfrak{a}$ here controls the (possibly non-linear) [[Bianchi identities]]/[[Gauss law]] satisfied by the [[curvature forms]]/[[flux densities]] but is not the higher Lie algebra in which the [[gauge potentials]] take values, if any. 
This is tacitly familiar in the case of RR-flux/D-brane charge: Here the characteristic $L_\infty$-algebra $[b_2, \, v_{2\bullet-1}] = v_{2\bullet + 1}$ bears no resemblance to the [[Lie algebra]] [[special unitary Lie algebra|$\mathfrak{su}(n)$]], and yet after choosing [[D-brane charge quantization in topological K-theory]] it follows that gauge potentials with coefficients in $\mathfrak{su}(n)$ (namely [[connection on a bundle|connections]] on Hermitean [[vector bundles]]) provide [[cocycles]] for the resulting [[differential K-theory]]. It is in this way (flux quantization $\rightsquigarrow$ K-theory $\rightsquigarrow$ gauge bundles as cocycles) that non-abelian [[gauge fields]] appear on [[D-branes]].


## Flux densities and Brane sources
 {#FluxDensitiesAndBraneSources}

(...)

## Flux/Charge quantization laws
 {#FluxQuantizationLaws}

(...)

## Examples in String/M-Theory

(...)

## References


* {#Abrikosov57a} [[Alexei Abrikosov]], *On the Magnetic properties of superconductors of the second group*, Sov. Phys. JETP **5** (1957) 1174-1182; Zh. Eksp. Teor. Fiz. **32** (1957) 1442-1452 &lbrack;[spire:9138](https://inspirehep.net/literature/9138), [[Abrikosov-MagneticPropertiesOfSuperconductors.pdf:file]]&rbrack;

* {#Alfonsi24} [[Luigi Alfonsi]], *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;

* {#Alvarez85a} [[Orlando Alvarez]], *Cohomology and Field Theory*, talk at: *Symposium on Anomalies, Geometry, Topology*, Argonne IL (28-30 March 1985) &lbrack;[inspire:965785](https://inspirehep.net/conferences/965785), [pdf](https://lib-extopc.kek.jp/preprints/PDF/1985/8507/8507262.pdf), [[Alvarez-CohomologyAndFieldTheory.pdf:file]]&rbrack;

* {#BFJKNRSW24} [[Leron Borsten]], [[Mehran Jalali Farahani]], [[Branislav Jurčo]], [[Hyungrok Kim]], [[Jiří Nárožný]], [[Dominik Rist]], [[Christian Saemann]], [[Martin Wolf]], *Higher Gauge Theory*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2401.05275](https://arxiv.org/abs/2401.05275)&rbrack;

* {#Dirac31} [[P.A.M. Dirac]], _Quantized Singularities in the Electromagnetic Field_,  Proceedings of the Royal Society A **133** (1931) 60-72 &lbrack;[doi:10.1098/rspa.1931.0130](http://rspa.royalsocietypublishing.org/content/133/821/60.short)&rbrack;

* {#Faraday1852} [[Michael Faraday]], *Delienation of Lines of Magnetic Force by iron filings*, §37 in: *Experimental Researches in Electricity.--Twenty-Ninth Series*, Philosophical Transactions of the Royal Society of London **142** (1852) 137-159 &lbrack;[doi:10.1098/rstl.1852.0012](https://doi.org/10.1098/rstl.1852.0012), [jstor:108540](https://www.jstor.org/stable/108540)&rbrack;

  > (the notion of "lines of force" is introduced on pp. 154)


* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;


* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], *[[Quantization of Gauge Systems]]*, Princeton University Press (1992) &lbrack;[doi:10.2307/j.ctv10crg0r](https://doi.org/10.2307/j.ctv10crg0r)&rbrack;

* {#MinasianMoore97} [[Ruben Minasian]], [[Gregory Moore]], *K-theory and Ramond-Ramond charge*, JHEP 9711:002 (1997) $[$[arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230), [doi:10.1088/1126-6708/1997/11/002](https://doi.org/10.1088/1126-6708/1997/11/002)$]$


* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. **22** 1   (1997) 1-13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), <a href="https://doi.org/10.1016/S0393-0440(96)00042-3">doi:10.1016/S0393-0440(96)00042-3</a>&rbrack;

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019 (1998) \[<a href="http://arxiv.org/abs/hep-th/9810188">arXiv:hep-th/9810188</a>, [doi:10.1088/1126-6708/1998/12/019](https://doi.org/10.1088/1126-6708/1998/12/019)\]


