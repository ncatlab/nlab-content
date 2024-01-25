
> under construction (using material from part I of *[[schreiber:Introduction to Hypothesis H]]*)

> this entry is one section of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- fundamental super p-branes|fundamental super p-branes]]_

\linebreak

\linebreak

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



> **Abstract.**

> For [[higher gauge fields]] [of Maxwell type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) --- e.g. the common [[electromagnetic field]] but also the [[B-field|B-]], [[RR-field|RR-]], and [[supergravity|C-fields]] considered in [[string theory|string]]/[[M-theory]] --- [[flux]]-&[[charge]][[flux quantization|-quantization]] laws specify [[non-perturbative quantum field theory|non-perturbative completions]] of these [[field (physics)|fields]] by encoding their [[soliton|solitonic]] behaviour and hence by specifying the quantized [[charges]] carried by the individual [[branes]] that source these fluxes (higher-dimensional [[monopoles]] or [[solitons]]).
>
> This page surveys the general ([[rational homotopy theory|rational]]-)[[homotopy theory|homotopy theoretic]] understanding of flux- & charge-quantization via the [[Chern-Dold character map]] generalized to the non-linear [[Bianchi identities]] appearing in higher-dimensional [[supergravity]] theories, notably for [[B-field|B-]]&[[RR-fields]] in [[D=10 supergravity|10d]] and for the [[supergravity C-field|C-field]] in [[D=11 supergravity|11d]]. 
>
> While flux quantization applies already to [[classical field theory|classical]] gauge fields and might seem to be better called *flux discretization*, for disambiguation, the choice involved in flux quantization induces the actual [[nLab:strict deformation quantization]] of [[observables]] on fluxes and hence may be understood as part of actual [[quantization]] in the sense of *[[quantum field theory]]*, [[non-perturbative quantum field theory|non-perturbatively]].
>
> With higher flux quantization thus being a key aspect of the general formulation of [[non-perturbative quantum field theory]] --- which as a whole remains a major open problem of [[mathematical physics|mathematical]] [[theoretical physics]] --- it may be understood as one step in the historical development towards this goal:
>
> * In 1852 [[Michael Faraday|Faraday]] observes [[magnetic field]] [[flux lines]] emanating from magnetic poles &lbrack;[Faraday 1852](#Faraday1852)&rbrack;. 
>   
> * In 1931 [[P. A. M. Dirac|Dirac]] invokes [[quantum mechanics]] to argue that, if there were unpaired such (mono-)poles, then the total flux emanating from them --- and thus the magnetic charge carried by them --- had to come in [[integer]] multiples of a unit quantum &lbrack;[Dirac 1931](#Dirac31)&rbrack;. 
>
> * In 1957 --- while magnetic monopoles remain unobserved --- [[Alexei Abrikosov|Abrikosov]] notices that the same electromagnetic flux-&charge-quantization mechanism makes [[Abrikosov vortex|vortex strings]] in [[type II superconductors]] carry units of localized magnetic flux.  &lbrack;[Abrikosov 1957](#Abrikosov57a)&rbrack;
>   
> * In 1985 [[Orlando Alvarez|Alvarez]] understands such *[[soliton|solitonic]]* [[magnetic fields]] as [[cocycles]] in ([[differential ordinary cohomology|differential]]) [[ordinary cohomology]]. &lbrack;[Alvarez 1985](#Alvarez85a)&rbrack;
>
> * In the 1990s [[string theory|string theorists]] conjectured that the combined flux of [[B-field|B-]]&[[RR-fields]] and hence the charge of [[D-branes]] is analogously quantized in a [[Whitehead-generalized cohomology|generalized]] cohomology theory called "[[twisted K-theory|twisted topological K-theory]]" &lbrack;[Minasian & Moore 1997](#MinasianMoore97); [Witten 1998](#Witten98)&rbrack;; 
>
>   and that the flux of the [[supergravity C-field|C-field]] and hence the charge of [[M-branes]] is quantized in a "[[shifted C-field flux quantization|shifted half-integral]]" cohomology theory &lbrack;[Witten 1996](#Witten96a)&rbrack; which long remains mysterious. 
>
> * In recent years [FSS 2020](#FSS20) have developed a systematic understanding of flux quantization of any [higher gauge theory of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) in generalized [[non-abelian cohomology]] theory, using [[fundamental theorem of dg-algebraic rational homotopy theory|tools from dg-algebraic]] [[rational homotopy theory]] related to the [[D'Auria-Fre formulation of supergravity|"FDA-method" in the supergravity literature]]. 
>
>   This provides a transparent re-derivation of known flux quantization laws and it allows to finally discuss [[supergravity C-field|C-field]] flux/[[M-brane]] charge quantization.

\linebreak

#Contents#
* table of contents
{:toc}


\linebreak

## Outline
 {#Outline}


([§2](#FluxDensitiesAndBraneSources)) A *[[higher gauge theory]]* (review in [Alfonsi 2024, §2](#Alfonsi24); [BFJ${}^+$ 2024](#BFJKNRSW24)) [of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) is a ([[quantum field theory|quantum]]) [[field theory]] analogous to [[vacuum]]-[[electromagnetism]] ([[AQFT on curved spacetimes|on curved spacetimes]]), but with the analog of the electromagnetic [[flux density]] $F_2$ ([which ordinarily is](electromagnetic+field#FieldStrengthAsClosed2Form) a [[differential 2-form]] on 3+1 [[dimension of a manifold|dimensional]] [[spacetime]] $X^4$)  allowed to be a system of [[differential forms]] $\vec F \,\equiv\, \big\{F^{(i)}\big\}_{i \in I}$ of any degree $deg_i \geq 1$ on a [[dimension of a manifold|$D$-dimensional]] [[spacetime]] $X^D$ of any dimension $D = d+1 \geq 2$, and with the analog of the [[Maxwell equations]] being any system of polynomial $\vec P(-)$ first order [[exterior derivative|exterior]]-[[differential equations]] $\mathrm{d} \vec F \,=\, \vec P\big(\vec F\big)$ (the higher [[Bianchi identities]], crucially admitting polynomial "self-sourcing" of fluxes) subject to a linear $\vec \mu(-)$ [[Hodge star operator|Hodge]]-[[duality-symmetric higher gauge theory|self-duality]] relation $\star \vec F \,=\, \vec \mu\big(\vec F\big)$ (the "[[constitutive equation]]").

Such [[higher gauge theories]] famously appear as the [[higher gauge field|gauge field]]-sector in higher-dimensional [[supergravity]] and hence in [[superstring|super]]-[[string theory|string]]/[[M-theory]], which is where they draw most of their motivation from. 

In analogy to how for ordinary [[Maxwell theory]] one may think of [[singularities]] or stable bumps in the [[flux density]] $F_2$ as being sourced by [[charges]] carried by (hypothetical) [[Dirac monopoles]] or by (observed) [[Abrikosov vortex strings]], respectively, so one may think of [[singularities]] or stable bumps in these higher flux densities as sourced by [[singular branes]] or [[solitonic branes]], respectively, for suitably higher dimensional ([[membrane|mem-]])[[branes]] carrying suitable higher charges.

But for [[singular brane|singular]]/[[solitonic branes]] to be "[[elementary particle|elementary]]" objects of individually discernible nature, their charges, and hence the total fluxes which they source, should have discrete ("quantized") values (as indeed observed for [[Abrikosov vortex strings]]). This is the topic of *[[flux quantization]]*:

\linebreak

([§3](#FluxQuantizationLaws)) Just as for [[electromagnetism]], these higher [[flux densities]] themselves do not yet constitute the full [[field (physics)|field]]-content of the given higher gauge theory. 

Traditionally one declares the full [[higher gauge field|higher]] [[gauge field]] to be given by [[gauge potentials]] $\vec A$ whose differential *locally* contributes to the given flux density, $\vec F \,=\, \mathrm{d} \vec A + \cdots$ and which is *globally* subjected to a topological condition which implies *[[flux quantization|flux and charge quantization]]* of the total fluxes and (brane-)charges, making them form a [[discrete space]] reflecting the nature of *individual* ("[[elementary particle|elementary]]") branes carrying/sourcing discrete units of charges/fluxes (as famously observed for [[Abrikosov vortex strings]]). 
But from this point of view it is far from transparent how to identify the structure of gauge potentials for general higher gauge theories.

More systematically, we may understand [[flux quantization]] as the specification of the [[non-perturbative quantum field theory|non-perturbative]] charge/flux sectors in ([[nonabelian cohomology|non-abelian]]) [[generalized cohomology]] of which the [[flux densities]] are but differential-geometric [[Chern-Dold character|characters]], and observe that the corresponding higher [[gauge potentials]] and hence the full field content of the higher gauge theory arise automatically as the [[homotopy theory|homotopy]]/[[higher gauge theory|gauge theoretic]] witnesses of the resulting [[flux quantization]], making the full higher gauge fields be [[cocycles]] in a corresponding ([[nonabelian differential cohomology|nonabelian]]) [[differential cohomology]] theory.

\linebreak

([§4](#Examples)) Examples of [[flux quantization]] beyond [[Dirac charge quantization]] in [[electromagnetism]] play a key role in [[string theory|string]]/[[M-theory]]: 

  * the seminal "Hypothesis K" postulating [[D-brane charge quantization in K-theory]],

  * the more recent "[[schreiber:Hypothesis H]]" postulating [[M-brane]] charge quantization in unstable [[twisted Cohomotopy|twisted]] [[Cohomotopy]].

These hypotheses are not unrelated: Under "[[double dimensional reduction|double dimensional]] [[Kaluza-Klein reduction]]" along a [[circle]] [[fiber]] the [[supergravity C-field|C-field]] fluxes on $X^{10+1}$ are to give rise to *most* of the [[B-field|$B$-]]/[[RR-field]]-fluxes in $X^{9+1}$ (as part of the [[duality between M-theory and type IIA string theory]], which is either conjectural or defining, depending on attitude towards the definition of the elusive [[M-theory]]). Therefore [[schreiber:Hypothesis H]] may be understood as providing an [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *lift* of [[D-brane charge quantization in K-theory|Hypothesis K]] to the extent that it reduces to the latter under [[double dimensional reduction]], and as an [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *correction* to the extent that it does not quite reduce to Hypothesis K.

While the discussion of the fine-grained predictions and mutual (in)compatibilities of these flux-quantization laws is beyond the scope of this review, these examples serve to highlight nature of the space of choices of flux quantization laws and with them the general mechanism of flux quantization --- which previous more *ad hoc*-discussions have barely brought out.

Notice therefore that a *choice* of flux quantization is (depending on perspective of how that higher gauge theory is ultimately defined):

* a hypothesis about 

or else

* a specification of 

the [[non-perturbative quantum field theory|non-perturbative completion]] of the given [[higher gauge theory]], which is generally an issue that deserves (more) attention.

Traditionally, flux quantization laws have been postulated sporadically and in ad-hoc fashion, in order to patch up "anomalous" theories: 
Since the ancient past it is common to define any [[theory (physics)|physical theory]] by a [[stationary action principle]] embodied by a [[Lagrangian density]], from which a perturbative [[BRST complex]] is extracted, whose [[quantization]] (e.g. [Henneaux & Teitelboim 1992](#HenneauxTeitelboim92)) is generally afflicted with problems ("[[quantum anomalies|anomalies]]") some of which are dealt with by ad-hoc flux quantization: For example the original [[Dirac charge quantization]] was postulated to cure an anomaly in the quantum theory of an [[electron]] propagating in the background field of a [[magnetic monopole]] (a "0-brane"), while the enigmatic [[shifted C-field flux quantization]] similarly serves to cure an anomaly in the quantum theory of the [[M2-brane]] propagating in the background field of an [[M5-brane]] ([Witten 1996a, §2.2](#Witten96a)).

In contrast, in the modernized picture reviewed here, the available choices of flux-quantization laws $\mathcal{A}$ are [[algebraic topology|algebro-topologically]] determined by the form of the higher [[Gauss law]] on any [[Cauchy surface]], and any such choice, given by a compatible [[non-abelian cohomology]]-theory, determines the [[non-perturbative quantum field theory|non-perturbative]] [[phase space]] [[smooth infinity-stack|stack]] of flux-quantized gauge fields. This process makes no reference to [[Lagrangian densities]] and applies seamlessly to field theories that do not even have a natural Lagrangian description, such as [[self-dual higher gauge theories]].

Typically there is an "evident" choice of flux quantization and this is the choice tacitly made in the literature, where considered at all. But it is important to notice that there are other admissible choices, embodying hypotheses about (or definitions of) non-evident nonperturbative completions of the given higher gauge theory. 

The following table shows in outline the logic of algebra-topological flux quantization; on the left in generality and on the right for our three running examples:

1. traditional [[Dirac charge quantization]] of the [[electromagnetic field]] (experimentally well-supported);

1. traditional [[D-brane charge quantization in topological K-theory|D-brane charge quantization]] in [[twisted K-theory|twisted]] [[topological K-theory]] ("Hypothesis K", still facing various challenges);

1. more recent [[M-brane]]$\;$[[shifted C-field flux quantization|charge quantization]] in unstable [[twisted Cohomotopy|twisted]] [[Cohomotopy]] ("[[schreiber:Hypothesis H]]").


\begin{imagefromfile}
    "file_name": "GeomPhys-FluxQuantizationSurvey-240123.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


As this table indicates, the [[algebraic topology|algebro-topological]] nature of flux/charge quantization is [[higher Lie theory|higher Lie theoretic]] (explained in [§3](#FluxQuantizationLaws)), by matching two [[L-infinity algebras|$L_\infty$-algebras]] associated with a given [[higher gauge theory]] [of Maxwell type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) ([§2](#FluxDensitiesAndBraneSources)):

**(i)** The higher [[Gauss law]] of a [[higher gauge theory]] [of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) is equivalent to the condition that the [[flux densities]] jointly constitute a [[flat L-infinity algebra valued differential form|closed $L_\infty$-algebra valued differential form]] with values in a characteristic [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$;

\begin{imagefromfile}
    "file_name": "GeomPhys-GaussLawAsFlatnessCondition-240123.jpg",
    "width": 740,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

**(ii)** The [[classifying space]] $\mathcal{A}$ of the topological flux/charge sector is [[rational homotopy type|rationally]] characterized by its [[rational numbers|rational]] [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]]  $\mathfrak{l}\mathcal{A}$ (essentially the "Quillen model" of $\mathcal{A}$: that $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{l}\mathcal{A})$ is the [[Sullivan model]] of $\mathcal{A}$) and the nonabelian [[Chern-Dold character]] map extracts from $\mathcal{A}$-cohomology its image in $\mathfrak{l}\mathcal{A}$-valued [[nonabelian de Rham cohomology]]:

\begin{imagefromfile}
    "file_name": "NonabCharacter-240123.jpg",
    "width": 840,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}
 
\begin{imagefromfile}
    "file_name": "GeomPhys-FirstIdeaFluxQuantization-240123.jpg",
    "float": "right",
    "width": 580,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


That these two $L_\infty$-algebras coincide is the condition on the choice of the flux quantization law embodied by $\mathcal{A}$; and it implies that the non-abelian [[Chern-Dold character map]] $ch_{\mathcal{A}}$ from the [[non-abelian cohomology]]-theory classified by $\mathcal{A}$ takes values in the [[non-abelian de Rham cohomology]] with coefficients in $\mathfrak{l}\mathcal{A}$, which under $\mathfrak{l}\mathcal{A} \simeq \mathscr{a}$ identifies with the deformation classes of [[flux densities]] satisfying their higher [[Gauss law]].

Finally, given such a choice of flux quantization law $\mathcal{A}$, the [[gauge potentials]] and hence the full [[moduli stack]] of [[higher gauge fields]] appears by forming the above matching not just as an identification in [[non-abelian de Rham cohomology]] but as a [[homotopy fiber product]] of the corresponding [[moduli stacks]]: This makes the full flux-quantized [[higher gauge fields]] be [[cocycles]] in [[nonabelian differential cohomology]] with coefficients in $\mathcal{A}$.

\begin{remark}
**(the role of [[L-infinity algebra|$L_\infty$-algebras]]: curvature-coefficients instead of gauge potiential-coefficients)**
\linebreak
In comparison to more traditional discussions, beware that the (possibly non-abelian) [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ here controls the (possibly non-linear) [[Bianchi identities]]/[[Gauss law]] satisfied by the [[curvature forms]]/[[flux densities]] --- and thus is *not* the (higher) Lie algebra in which the [[gauge potentials]] take values, if any. (Even in the abelian case, where both types of coefficient $L_\infty$-algebras make sense, they differ by a degree-shift.)

This is an underappreciated use of [$L_\infty$-algebras in physics](L-infinity-algebra#ReferencesInPhysics), but it is known from the ["FDA"-method in supergravity](D'Auria-Fre+formulation+of+supergravity) and is tacitly familiar in traditional discussion of RR-flux/D-brane charge: 

Here the characteristic $L_\infty$-algebra $[b_2, \, v_{2\bullet-1}] = v_{2\bullet + 1}$ bears no resemblance to the [[Lie algebra]] [[special unitary Lie algebra|$\mathfrak{su}(n)$]], and yet after choosing [[D-brane charge quantization in topological K-theory]] it follows (an algebro-topological form of "[[gauge enhancement]]") that gauge potentials with coefficients in $\mathfrak{su}(n)$ (namely [[connection on a bundle|connections]] on Hermitean [[vector bundles]]) provide [[cocycles]] for the resulting [[differential K-theory]]. It is in this way (RR-flux quantization $\rightsquigarrow$ K-theory $\rightsquigarrow$ gauge bundles as cocycles) that non-abelian [[gauge fields]] appear on [[D-branes]].

In fact, flux quantization as discussed here does not apply to [[su(n)|$\mathfrak{su}(n)$]]-[[Yang-Mills theory]] directly:

Generally, not all [[L-infinity algebras|$L_\infty$-algebras]] appear as rational [[Whitehead L-infinity algebras|Whitehead $L_\infty$-algebras]] of (the [[homotopy type]] of) a space $\mathcal{A}$ that is amenable to [[rationalization]]; those that do are "[[nilpotent L-infinity algebra|nilpotent]]". 
Specifically, [[su(n)|$\mathfrak{su}(n)$]] ($n \geq 2$) is not a [[nilpotent Lie algebra]], which relates to the fact that flux quantization as discussed here --- while it does apply to non-linear/non-abelian higher Bianchi identities such as for the [[supergravity C-field|C-field]] --- does not apply directly to [[Yang-Mills theory]] with gauge Lie algebra [[su(n)|$\mathfrak{su}(n)$]] (or other [[classical Lie algebras]]).
\end{remark}

\linebreak

In the following we discuss all this in more detail.

\linebreak

## Flux densities and Brane sources
 {#FluxDensitiesAndBraneSources}


### Ordinary electromagnetic flux and its "branes"
 {#OrdinaryElectromagneticFluxAndItsBranes}

Faraday observed "lines of force" -- now called *flux of the magnetic field* -- concentrating towards the *poles* of rod magnets:

\begin{imagefromfile}
    "file_name": "GeomPhys-FaradayIronFilings-240124.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    },
    "caption": "From Faraday’s diary of experimental investigation, vol VI, entry from 11th Dec. 1851, as reproduced in [Martin 2009, p. 311](#Martin09); the colored arc is our addition, for ease of comparison with the next graphics"
\end{imagefromfile}

In modern [[differential geometry|differential-geometric]] formulation, the [[flux density|density of these flux lines]] through any given [[surface]]-element is encoded in a [[differential 2-form]] $F_2$:

\begin{imagefromfile}
    "file_name": "GeomPhys-FluxDensityAs2Form-240124.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    },
    "caption": "adapted from [Hyperphysics](#Hyperphysics)"
\end{imagefromfile}

\begin{imagefromfile}
    "file_name": "GeomPhys-EMFluxDensity-240124.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -35,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


More in detail, with respect to any [[foliation]] of [[spacetime]] $X^4$ by [[spacelike]] [[Cauchy surfaces]] $X^4 \simeq \mathbb{R}^1 \times X^d$ (assuming [[globally hyperbolic spacetime|global hyperbolicity]]), the spatial component of $F_2$ is the *magentic flux density* $B$, while the [[Hodge duality|Hodge dual]]  (with respect to $X^4$) of the temporal component is the *electric flux density* $E$.

Imagining, as Dirac did, that Faraday's rod magnet could be made *infinitely* long and thin, any one of its poles would look like an isolated [[monopole|mono-pole]] with flux concentrating towards it from all directions:

\begin{imagefromfile}
    "file_name": "MagneticMonopole-240124.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

At the point of the idealized monopole itself, the flux density $B$ per unit volume would diverge -- a "singularity" much in the sense of [[black holes]], which therefore we do not regard to be part of spacetime(time): The spacetime domain on which to discuss the fluxes sourced by a magnetic monopole is not [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ itself, but its  [[complement]] around the [[worldline]] $\mathbb{R}^{0,1}$ of the would-be monopole:

$$
  \mathbb{R}^{3,1} 
    \setminus
  \mathbb{R}^{0,1}
  \;
  \underset{\mathrm{homeo}}{\simeq}
  \;
  \mathbb{R}^{0,1}
  \times
  \big(
    \mathbb{R}^3 \setminus \{0\}
  \big)
  \;
  \underset{\mathrm{homeo}}{\simeq}
  \;
  \mathbb{R}^{0,1} 
  \times 
  R^1_{\gt 0}
  \times S^2
  \;
  \underset{\mathrm{hmtp}}{\simeq}
  \;
  S^2
  \,.
$$

As such, magnetic monopoles are the *[[singular brane|singular]] 0-[[branes]]* of electromagnetism --- in theory: Whether magnetic monopoles exist in nature remains open; they have not been seen in [[experiment]], but there are decent theoretical arguments that they should exist in [[grand unified theories]].

On the other hand, the "[[solitonic branes]] of electromagnetism" are experimentally well-established (and have famously been regarded as actual 1-[[branes]] ([[strings]]) approximated by a [[Nambu-Goto action]]: [Nielsen & Olesen 1973](vortex+string#NielsenOlesen73); [Polyakov 2008, p. 1](vortex+string#Polyakov08); [Beekman & Zaanen 2011](vortex+string#BeekmanZaanen11)): These are the [[Abrikosov vortices]] formed in [[type II superconductors]] with in a transverse magnetic field:

\begin{imagefromfile}
    "file_name": "SuperconductorVortexStructure-230304.jpg",
    "width": 720,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "adapted from [Loudon and Midgley 2009](superconductivity#LoudonMidgley09)"
\end{imagefromfile}

In this case the "sphere" through which the total magnetic flux density is measured is nominally the [[plane]] filled by the superconducting material, but since far away from any vortex the magentic flux has to vanish, this plane appears to the fluxes via its [[one-point compactification]] with the "point at infinity" adjoined.

These vortext strings are *[[solitons]]* in that the flux density is everywhere finite, and yet the "bumps" in the flux density are topologically stable. Much like a bump in a rug cannot be flattened as long as the boundary of the rug is fixed in place, so the requirement that flux densities "[[vanishing at infinity|vanish at infinity]]" keeps the vortex strings in place --- or at least this is the case once we take account of [[Dirac flux quantization]] below.

In summary:

\begin{imagefromfile}
    "file_name": "GeomPhys-MonopolesAndVortices-240124.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


The fact that there are, generally, these two kinds of "branes imprinted on flux" is "well-known" and yet underappreciated:

\linebreak

### The distinction between singular and solitonic branes
 {#TheDistinctionBetweenSingularAndSolitonicBranes}

Imprinted on [[flux densities]] may be *two kinds* of [[branes]], here to be called:

1.  **[[singular branes]]** ([[black branes]]) reflected in **diverging flux density** at **singular loci** to be removed from spacetime,

1. **[[solitonic branes]]** reflected in *localized* but
**finite flux density**, namely **[[vanishing at infinity]]**, transversally.

>   Beware that, while the terminology "[[solitonic brane]]" is wide-spread, its exact meaning differs between authors (as does the term "[[soliton]]" that it is derived from): It was introduced in [Duff, Khuri & Lu 1992](#DuffKhuriLu92), [1994](#DuffKhuriLu94) and [Duff & Lu 1993](#DuffLu93), [1994](#DuffLu94) to mean stable but *non-singular* brane-like solutions to (supergravity/flux) equations of motion, which is how we use it here. But already [Stelle 1998](solitonic+brane#Stelle98) uses "solitonic" to instead mean the  "[[electric-magnetic duality|electromagnetic-dual]] [[singular brane]]", e.g. calling the singular [[NS5-brane|$\mathrm{NS}_5$-brane]] the soliton of the [[F1-brane|fundamental string]]. Somewhat in this vein, many later authors (e.g.  [Smith (2002), p. 5](solitonic+brane#Smith02)) use "solitonic" for any singular or non-singular brane-like supergravity solution,  thus regarding it as the antonym to the [[fundamental particle|fundamental]] [[sigma-model]] branes.

In other words, the choice of spacetime [[domain]] encodes where the fluxes sourced by singular or solitonic branes are not necessarily defined or constrained to vanish, respectively &lbrack;[SS23-MF, §2.1](#SS23-MF)&rbrack;:

\begin{imagefromfile}
    "file_name": "GeomPhys-SingularAndSolitonicBranes.240124.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

For example, in the case of *flat branes*, both these spacetime domains are [[homotopy equivalence|homotopy equivalence]] to [[spheres]], but of differen dimensions:

(1.) Spacetime domain for flat singular branes:

\begin{imagefromfile}
    "file_name": "GeomPhys-FlatSingularBranes-240124.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


(2.) Spacetime domain for flat solitonic branes:

\begin{imagefromfile}
    "file_name": "GeomPhys-FlatSolitonicBranes-240124.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


\linebreak

### Solution space of higher Maxwell equations

(...)

\begin{imagefromfile}
    "file_name": "GeomPhys-HigherMaxwellEquations.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


\begin{proposition}
**([SS23-FQ](#SS23-FQ))**
  On a [[globally hyperbolic spacetime]] $X^D \,\simeq\, \mathbb{R}^{0,1} \times X^d$, the solution space to [higher Maxwell-equations](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) of motion brought into the [[duality-symmetric higher gauge theory|duality-symmetric form]] is [[isomorphism|isomorphic]] to the solution of the [[Bianchi identities]] on any [[Cauchy surface]] $\iota \,:\, X^d \hookrightarrow X^D$, then to be called the higher *[[Gauss law]]*
\end{proposition}

\begin{imagefromfile}
    "file_name": "GeomPhys-HigherMaxwellSolutionSpace.jpg",
    "width": 850,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


(...)

\begin{imagefromfile}
    "file_name": "CanonicalAndCovariantPhaseSpace-240124.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


(...)





(...)







## Flux/Charge quantization laws
 {#FluxQuantizationLaws}

(...)

## Examples in String/M-Theory
 {#Examples}

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

* {#Hyperphysics} Hyperphysics, *Magnetic Flux* &lbrack;[hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html](http://hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html)&rbrack;

* {#LoudonMidgley09} J. C. Loudon, P. A. Midgley, *Imaging Flux Vortices in Type II Superconductors with a Commercial Transmission Electron Microscope*, Ultramicroscopy **109** 6 (2009) 700-729 &lbrack;[arXiv:0807.2401](https://arxiv.org/abs/0807.2401), [doi:10.1016/j.ultramic.2009.01.008](https://doi.org/10.1016/j.ultramic.2009.01.008)&rbrack;


* {#Martin09} Thomas Martin (ed.), *Faraday's diaray of experimental investigation* 1820-1862, HR Direct (2009)  &lbrack;[webpage](http://faradaysdiary.com/), preview:[pdf](http://faradaysdiary.com/ws3/faraday.pdf)&rbrack;

* {#MinasianMoore97} [[Ruben Minasian]], [[Gregory Moore]], *K-theory and Ramond-Ramond charge*, JHEP 9711:002 (1997) &lbrack;[arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230), [doi:10.1088/1126-6708/1997/11/002](https://doi.org/10.1088/1126-6708/1997/11/002)&rbrack;

* {#SS23-MF} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:M/F-Theory as Mf-Theory|M/F-Theory as $M f$-Theory]]*, Rev. Math. Phys. **35** 10 (2023) &lbrack;[doi:10.1142/S0129055X23500289](https://doi.org/10.1142/S0129055X23500289), [arXiv:2103.01877](https://arxiv.org/abs/2103.01877)&rbrack;

* {#SS23-FQ} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;


* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. **22** 1   (1997) 1-13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), <a href="https://doi.org/10.1016/S0393-0440(96)00042-3">doi:10.1016/S0393-0440(96)00042-3</a>&rbrack;

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019 (1998) \[<a href="http://arxiv.org/abs/hep-th/9810188">arXiv:hep-th/9810188</a>, [doi:10.1088/1126-6708/1998/12/019](https://doi.org/10.1088/1126-6708/1998/12/019)\]

(...)

\linebreak

\linebreak

