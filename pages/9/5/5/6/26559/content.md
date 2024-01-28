
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

> For [[higher gauge fields]] [of Maxwell type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) --- e.g. the common [[electromagnetic field]] (the "A-field") but also the [[B-field|B-]], [[RR-field|RR-]], and [[supergravity|C-fields]] considered in [[string theory|string]]/[[M-theory]] --- [[flux]]&[[charge]][[flux quantization|-quantization]] laws specify [[non-perturbative quantum field theory|non-perturbative completions]] of these [[field (physics)|fields]] by encoding their [[soliton|solitonic]] behaviour and hence by specifying the quantized [[charges]] carried by the individual [[branes]] that source these fluxes (higher-dimensional [[monopoles]] or [[solitons]]).
>
> This page surveys the general ([[rational homotopy theory|rational]]-)[[homotopy theory|homotopy theoretic]] understanding &lbrack;[FSS23-Char](#FSS23)&rbrack;  of flux- & charge-quantization via the [[Chern-Dold character map]] generalized to the *non-linear* (self-sourcing) [[Bianchi identities]] that appear in higher-dimensional [[supergravity]] theories, notably for [[B-field|B-]]&[[RR-fields]] in [[D=10 supergravity]] and for the [[supergravity C-field|C-field]] in [[D=11 supergravity]]. 
>
> While flux quantization applies already to [[classical field theory|classical]] gauge fields and might seem to be better called *flux discretization*, for disambiguation, the choice involved in flux quantization induces the actual [[strict deformation quantization]] of [[observables]] on fluxes &lbrack;[SS23-Obs](#SS23-Obs)&rbrack; and hence may be understood as part of actual [[quantization]] in the sense of *[[quantum field theory]]*, [[non-perturbative quantum field theory|non-perturbatively]].
>
> With higher flux quantization thus being a key aspect of the general formulation of [[non-perturbative quantum field theory]] --- which as a whole remains a major open problem of [[mathematical physics|mathematical]] [[theoretical physics]] --- it may usefully be understood as one step in the historical development towards this goal:
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
> * In recent years we have developed &lbrack;[FSS23-Char](#FSS23)&rbrack; a systematic understanding of flux quantization of any [higher gauge theory of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) in generalized [[non-abelian cohomology]] theory, using [[fundamental theorem of dg-algebraic rational homotopy theory|tools from dg-algebraic]] [[rational homotopy theory]] related to the [[D'Auria-Fre formulation of supergravity|"FDA-method" in the supergravity literature]]. 
>
>   This provides a transparent re-derivation of known flux quantization laws and it allows to finally discuss [[supergravity C-field|C-field]] flux- and [[M-brane]] charge-quantization.

\linebreak

#Contents#
* table of contents
{:toc}


\linebreak

## Outline
 {#Outline}


([§2](#FluxDensitiesAndBraneSources)) A *[[higher gauge theory]]* (review in [Alfonsi 2024, §2](#Alfonsi24); [BFJ${}^+$ 2024](#BFJKNRSW24)) [of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) is a ([[quantum field theory|quantum]]) [[field theory]] analogous to [[vacuum]]-[[electromagnetism]] ([[AQFT on curved spacetimes|on curved spacetimes]]), but with the analog of the electromagnetic [[flux density]] $F_2$ ([which ordinarily is](electromagnetic+field#FieldStrengthAsClosed2Form) a [[differential 2-form]] on 3+1 [[dimension of a manifold|dimensional]] [[spacetime]] $X^4$)  allowed to be a system of [[differential forms]] $\vec F \,\equiv\, \big\{F^{(i)}\big\}_{i \in I}$ of any degree $deg_i \geq 1$ on a [[dimension of a manifold|$D$-dimensional]] [[spacetime]] $X^D$ of any dimension $D = d+1 \geq 2$, and satisfying a higher (see Def. \ref{HigherMaxwellEquations} below) analog of [[Maxwell's equations]].

Such [[higher gauge theories]] famously appear as the [[higher gauge field|gauge field]]-sector in higher-dimensional [[supergravity]] and hence in [[superstring|super]]-[[string theory|string]]/[[M-theory]], which is where they draw most of their motivation from. 

In analogy to how for ordinary [[Maxwell theory]] one may think of [[singularities]] or stable bumps in the [[flux density]] $F_2$ as being sourced by [[charges]] carried by (hypothetical) [[Dirac monopoles]] or by (observed) [[Abrikosov vortex strings]], respectively, so one may think of [[singularities]] or stable bumps in these higher flux densities as sourced by [[singular branes]] or [[solitonic branes]], respectively, for suitably higher dimensional ([[membrane|mem-]])[[branes]] carrying suitable higher charges.

But for [[singular brane|singular]]/[[solitonic branes]] to be "[[elementary particle|elementary]]" objects of individually discernible nature, their charges, and hence the total fluxes which they source, should have discrete ("quantized") values (as indeed observed for [[Abrikosov vortex strings]]). This is the topic of *[[flux quantization]]*:

\linebreak

([§3](#FluxQuantizationLaws)) Just as for [[electromagnetism]], these higher [[flux densities]] themselves do not yet constitute the full [[field (physics)|field]]-content of the given higher gauge theory. 

Traditionally one declares the full [[higher gauge field|higher]] [[gauge field]] to be given by [[gauge potentials]] $\vec A$ whose differential *locally* contributes to the given flux density, $\vec F \,=\, \mathrm{d} \vec A + \cdots$ and which is *globally* subjected to a topological condition that implies *[[flux quantization|flux and charge quantization]]* of the total fluxes and (brane-)charges, making them form a [[discrete space]] reflecting the nature of *individual* ("[[elementary particle|elementary]]") branes carrying/sourcing discrete units of charges/fluxes (as famously observed for [[Abrikosov vortex strings]]). 
But from this point of view it is far from transparent how to identify the structure of gauge potentials for general higher gauge theories.

More systematically, we may understand [[flux quantization]] as the specification of the [[non-perturbative quantum field theory|non-perturbative]] charge/flux sectors in ([[nonabelian cohomology|non-abelian]]) [[generalized cohomology]] of which the [[flux densities]] are but differential-geometric [[Chern-Dold character|characters]], and observe that the corresponding higher [[gauge potentials]] and hence the full field content of the higher gauge theory arise automatically as the [[homotopy theory|homotopy]]/[[higher gauge theory|gauge theoretic]] witnesses of the resulting [[flux quantization]], making the full higher gauge fields be [[cocycles]] in a corresponding ([[nonabelian differential cohomology|nonabelian]]) [[differential cohomology]] theory.

\linebreak

([§4](#Examples)) Examples of [[flux quantization]] beyond [[Dirac charge quantization]] in [[electromagnetism]] play a key role in [[string theory|string]]/[[M-theory]]: 

  * the seminal "Hypothesis K" postulating [[D-brane charge quantization in K-theory]],

  * the more recent "[[schreiber:Hypothesis H]]" postulating [[M-brane]] charge quantization in unstable [[twisted Cohomotopy|twisted]] [[Cohomotopy]].

These hypotheses are not unrelated: Under "[[double dimensional reduction|double dimensional]] [[Kaluza-Klein reduction]]" along a [[circle]] [[fiber]] the [[supergravity C-field|C-field]] fluxes on $X^{10+1}$ are to give rise to *most* of the [[B-field|$B$-]]/[[RR-field]]-fluxes in $X^{9+1}$ (as part of the [[duality between M-theory and type IIA string theory]], which is either conjectural or defining, depending on attitude towards the definition of the elusive [[M-theory]]). Therefore [[schreiber:Hypothesis H]] may be understood as providing an [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *lift* of [[D-brane charge quantization in K-theory|Hypothesis K]] to the extent that it reduces to the latter under [[double dimensional reduction]], and as a [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *correction* to the extent that it does not quite reduce to Hypothesis K.

While the discussion of the fine-grained predictions and mutual (in)compatibilities of these flux-quantization laws is beyond the scope of this review, these examples serve to highlight the nature of the space of choices of flux quantization laws and with them the general mechanism of flux quantization --- which previous more *ad hoc*-discussions have barely brought out.

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


That these two $L_\infty$-algebras coincide is the condition on the choice of the flux quantization law embodied by $\mathcal{A}$; and it implies that the non-abelian [[Chern-Dold character map]] $ch_{\mathcal{A}}$ from the [[non-abelian cohomology]]-theory classified by $\mathcal{A}$ takes values in the [[non-abelian de Rham cohomology]] with coefficients in $\mathfrak{l}\mathcal{A}$, which under $\mathfrak{l}\mathcal{A} \simeq \mathfrak{a}$ identifies with the deformation classes of [[flux densities]] satisfying their higher [[Gauss law]].

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


## Flux densities and Brane charges
 {#FluxDensitiesAndBraneSources}


### Electromagnetic flux and its "branes"
 {#OrdinaryElectromagneticFluxAndItsBranes}

[[Michael Faraday|Faraday]] observed "lines of force" -- now called *flux of the magnetic field* -- concentrating towards the *poles* of rod magnets:

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
    "caption": "From Faraday’s diary of experimental investigation, vol VI, entry from 11th Dec. 1851, as reproduced in [Martin 2009, p. 311](#Martin09) -- the colored arc is our addition, for ease of comparison with the next graphics."
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

At the point of the idealized monopole itself, the flux density $B$ per unit volume would diverge -- a "singularity" much in the sense of [[black holes]], which therefore we do not regard to be part of space(-time): The spacetime domain on which to discuss the fluxes sourced by a magnetic monopole is (more on this [below](#TheDistinctionBetweenSingularAndSolitonicBranes)) not [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ itself, but its  [[complement]] around the [[worldline]] $\mathbb{R}^{0,1}$ of the would-be monopole:

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

On the other hand, the "[[solitonic branes]] of electromagnetism" are experimentally well-established (and have famously been regarded as actual 1-[[branes]] ([[strings]]) approximated by a [[Nambu-Goto action]] &lbrack;[Nielsen & Olesen 1973](vortex+string#NielsenOlesen73); [Polyakov 2008, p. 1](vortex+string#Polyakov08); [Beekman & Zaanen 2011](vortex+string#BeekmanZaanen11)&rbrack;): These are the [[Abrikosov vortices]] formed in [[type II superconductors]] within a transverse magnetic field:

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

These vortex strings are *[[solitons]]* in that the flux density is everywhere finite, and yet the "bumps" in the flux density are topologically stable. Much like a bump in a rug cannot be flattened as long as the boundary of the rug is fixed in place, so the requirement that flux densities "[[vanishing at infinity|vanish at infinity]]" keeps the vortex strings in place --- or at least this is the case once we take account of [[Dirac flux quantization]] below.

In summary:

\begin{imagefromfile}
    "file_name": "GeomPhys-MonopolesAndVortices-240124.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

The spacetime domains on which to exhibit fluxes of singular EM-branes (monopoles) and of  solitonic EM-branes (vortices) are as shown on the left of the following graphics, respectively, whose right hand side already shows the [[classifying maps]] of their quantized charges, further discussed [below](#FluxQuantizationLaws):

\begin{imagefromfile}
    "file_name": "GeomPhys-ChargeOfMonopolesAndVortices.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


The fact that there are, generally, these two kinds of "branes imprinted on flux" is "well-known" and yet underappreciated:

\linebreak


### Singular versus solitonic branes
 {#TheDistinctionBetweenSingularAndSolitonicBranes}

Generally, imprinted on [[flux densities]] may be *two kinds* of [[branes]], here to be called:

1.  **[[singular branes]]** ([[black branes]]) reflected in **diverging flux density** at **singular loci** that are to be removed from spacetime,

    > Beware that in [[supergravity]] these are also called "elementary branes" &lbrack;[Duff & Lu 1994](#DuffLu94)&rbrack;, in reference to how [[black holes]] carry the same quantum numbers as [[elementary particles]] -- but here we rather not conflate these two aspects.

1. **[[solitonic branes]]** reflected in **finite flux density** which is localized in that it **[[vanishing at infinity|vanishes at infinity]]**, transversally.

   >  The terminology "[[solitonic brane]]" was introduced in [Duff, Khuri & Lu 1992](solitonic+brane#DuffKhuriLu92), [1994](solitonic+brane#DuffKhuriLu94) and [Duff & Lu 1993](solitonic+brane#DuffLu93), [1994](#DuffLu94) to mean stable but non-singular brane-like solutions to (supergravity/flux) equations of motion ("[[solitons]]"). 

This general distinction between [[singular branes]] and [[solitonic branes]] is important for the correct identification of the implications of choices of [[flux quantization]]-laws on the corresponding brane charges.

\linebreak

**Spacetime domains for brane fluxes.**
More formally, one may encode these two cases by  slightly adjusting the nature of the **spacetime domain** on which fluxes are actually defined &lbrack;cf. [SS23-MF, §2.1](#SS23-MF)&rbrack;:

1. fluxes sourced by [[singular branes]] of [[dimension]] $p+1$ inside [[spacetime]] $X^{d+1}$ are actually defined on the [[complement]] $X^{d+1} \setminus Q^{p+1}$ of their singular [[worldvolume]],

1. fluxes sourced by [[solitonic branes]] 
of [[codimension]] $d-p$ are actually defined on their transverse space $T^{d-p}$ equipped with a "[[point at infinity]]" on which they are required to vanish.

\begin{imagefromfile}
    "file_name": "GeomPhys-DomainsForSingAndSolFluxes.240125.jpg",
    "width": 620,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

The condition of flux densities [[vanishing at infinity]] on some space is naturally formalized by considering the larger [[category]] of [[pointed topological spaces]] $(X, x \in X)$ (we discuss further below how to properly speak of differential geometric smoothness in this context) and regarding their given "[[base point]]" as being the "point at infinity", whence we shall write $(X, \infty_X)$ for the generic pointed space. Then a function "[[vanishing at infinity]]" on $(X,\infty_X)$ is a function on $X$ that literally vanishes at $\infty_X$.

For example:

1. The result of *adjoining* to $\mathbb{R}^n$ its "point at infinity" (this is called its *[[one-point compactification]]*, here to be denoted $\mathbb{R}^n_{\cup \{\infty\}}$) is [[homeomorphism|homeomorphic]] to the [[n-sphere|$n$-sphere]] with any basepoint: 

   $$
     \mathbb{R}^n_{\cup \{\infty\}} 
       \,\underset{homeo}{\simeq}\, 
     S^n
     \,.
   $$

1. On the other hand, to consider unconstrained functions on some $X$ in this context, we may regard all the points of $X$ as being at finite distance by declaring that the "point at infinity" is disjoint from $X$, hence by considering the [[disjoint union]] (denoted "$\sqcup$" as opposed to "$\cup$"):
 
   $$
     X_{\sqcup \{\infty\}}
     \;\coloneqq\;
     X \sqcup \{ \infty \}
     \,.
   $$

Given two such pointed spaces, their *[[smash product]]* "$\wedge$" is their [[Cartesian product]] with all points that are at infinity in either factor identified with a single new point at infinity:

$$
  \big(
    X,\, \infty_X
  \big)
  \wedge
  \big(
    Y,\, \infty_Y
  \big)
  \;\;
  \coloneqq
  \;\;
  \frac{
    X \times Y
  }{
    X \times \{\infty_Y\}
    \,\cup\,
    \{\infty_X\} \times Y
  }
$$

\linebreak

\begin{example}\label{FlatBranes}
**(The case of flat branes.)**
\linebreak
In the case of *flat branes* --- i.e. with [[Cartesian space|Cartesian]] [[worldvolumes]] inside [[Minkowski spacetime]]  --- both these spacetime domains are [[homotopy equivalence|homotopy equivalent]] to [[spheres]], but of different dimensions:

(1.) The spacetime domain for flat *singular* branes is homotopy-equivalent to the [[unit sphere]] in the transverse space, hence the sphere *around* the singular brane locus:

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


(2.) The spacetime domain for flat solitonic branes is homotopy equivalent to the sphere which is the [[one-point compactification]] of the transverse space (its [[stereographic projection]]):

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

\end{example}

\begin{example}\label{FlatBranesOfElectromagnetism}
**(the flat branes of electromagnetism)**
\linebreak
Specifying Ex. \ref{FlatBranes}  to the case of ordinary electromagnetic flux ([above](#OrdinaryElectromagneticFluxAndItsBranes)) it follows from this general reasoning that a flux density 2-form $F_2$ in $D=3+1$ may reflect the presence of 

1. singular 0-branes with spacetime domain 

   $$
     \mathbb{R}^{3,1} \setminus \mathbb{R}^{0,1} 
       \,\underset{\mathrm{homeo}}{\simeq}\, 
     \mathbb{R}^{0,1} \times \mathbb{R}_{\gt 0} \times S^2  
       \,\underset{\mathrm{hmtp}}{\simeq}\, 
     S^2
   $$

1. solitonic 1-branes with spacetime domain

   $$
     \mathbb{R}^{1,1}_+ 
       \wedge 
     \mathbb{R}^{2}_{\cup \{\infty\}}
     \;\underset{homeo}{\simeq}\;
     \mathbb{R}^{1,1}_+ 
       \wedge 
     S^2
     \;\underset{hmtp}{\simeq}\;
     S^2
   $$

which are exactly the familiar cases of [[magnetic monopoles]] (hypothetical) and [[Abrikosov vortex strings]] (observed), discussed [above](#OrdinaryElectromagneticFluxAndItsBranes).
\end{example}

\begin{example}\label{NearHorizonGeometriesOfSingularBranes}
**(near-horizon geometries of singular branes**)
\linebreak
The idea of regarding singular branes from the [[complement]]  of their singular locus in spacetime is familiar from the [[AdS/CFT correspondence]]:

The [[near horizon geometry]] of any $\gt 1/4$ [[BPS state|BPS]] [[black brane]] (for references see ) are all [[product topological spaces|product spaces]] of an [[anti de Sitter spacetime]] with a ([free discrete quotient](group+actions+on+spheres#FreeActionsByFiniteGroupsAndSphericalSpaceForms) of) a [[sphere]] (a [[spherical space form]]) around the singularity &lbrack;[Acharya, Figueroa-O'Farrill, Hull & Spence 1999](near-horizon+geometry#AFFHS98)&rbrack;. On a causal chart of AdS spacetime, this is homeomorphic to the flat brane complements form Ex. \ref{FlatBranes}:

\begin{imagefromfile}
    "file_name": "GeomPhys-NearHorizonGeometries.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\end{example}

In general, the spacetime domain on which to measure flux densities may be a mix of these purely singular and purely solitonic situations, in which case the notions of singular and of solitonic branes blend into each other:

\begin{example}\label{SolitonicBranesInKKCompactifications}
**(solitonic branes in KK-compactifications)**

In mild generalization of Ex. \ref{FlatBranes}, consider the case that spacetime is a trivial [[circle]]-[[fiber bundle]] over a [[Minkowski spacetime]]

$$
  X^D 
    \,\equiv\,
  \mathbb{R}^{1,d-1} \times S^1
  \,.
$$

In this case the flux sourced by solitonic branes of [[codimension]] $n$ as seen on the base spacetime $\mathbb{R}^{1,d-1}$ is measured on the [[smash product]] space
$$
  \big(
    S^1 \times \mathbb{R}^n
  \big)_{\cup \{\infty\}}
  \;\underset{homeo}{\simeq}\;
  S^1_{\sqcup \{\infty\}}
  \wedge
  \mathbb{R}^n_{\cup \{\infty\}}
  \;\underset{homeo}{\simeq}\;
  S^1_{\sqcup \{\infty\}}
  \wedge
  S^n  
  \,.
$$

This was maybe first understood by [Bergman, Gimon & Hořava 1999, §2.2 & §2.3](#BergmanGimonHořava99) (there in slightly different language).
\end{example}


\linebreak


### Higher fluxes and their brane sources
 {#HigherFluxAndItsBranes}

On this backdrop of ordinary electromagnetic flux ([above](#OrdinaryElectromagneticFluxAndItsBranes)) and of the general rule for measuring flux sourced by [[singular branes]] or [[solitonic branes]] ([above](#TheDistinctionBetweenSingularAndSolitonicBranes)) it clearly makes sense to consider [[theory (physics)|physical theories]] of [[higher gauge fields]] whose precise nature remains to be discussed, but whose flux densities are reflected in higher-degree differential forms $F^{(i)}_{deg_i}(X^D)$, these possibly being of different field species to be labeled by a [[finite set|finite]] [[index set]] $I \in Set$ and jointly to be denoted as follows:

\[
  \label{TheHigherFluxDensities}
  \vec F
  \;\equiv\;
  \Big\{
    F^{(i)}_{\mathrm{deg}_i}
    \,\in\,
    \Omega_{dR}^{deg_i}\big(
      X^D
    \big)
  \Big\}
  \,.
\]

\[\label{FluxesAndTheirSingularSources}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-FluxesAndTheirSingularBranes-240125.jpg",
    "float": "right",
    "width": 460,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Remarkably, such higher flux densities "automatically" appear in higher dimensional [[supergravity]], namely as "[[superpartners]]" of the [[gravitino]]-field that cannot be accounted for by the [[graviton]] itself. In particular in [[D=10 supergravity]] and [[D=11 supergravity]] these higher flux densities are known under the (now) fairly standard symbols shown on the right, along with the standard name of the correspoding [[singular branes]] (the "higher-dimensional monopoles").

* [[D=10 supergravity]]: [[B-field]]$\leftrightarrow$[[NS5-brane]]/[[F1-brane]] and [[RR-field]]$\leftrightarrow$[[D-branes]]

* [[D=11 supergravity]]: [[C-field]]$\leftrightarrow$[[M5-brane]]/[[M2-brane]].

(cf. [Blumenhagen, Lüst & Theisen 2013, §18.5, Table 18.3](#BlumenhagenLüstTheisen13))

\begin{remark}
**(singular vs. solitonic D-branes)**
\linebreak
Historically, the [[D-branes]] in [[D=10 supergravity]] were first identified as such &lbrack;[Polchinski 1995, cf. (14)](#Polchinski95)&rbrack; in their [[singular brane]] incarnation &lbrack;[Duff & Lu 1994](#DuffLu94)&rbrack;, while their incarnation as solitonic branes (in the [above sense](#TheDistinctionBetweenSingularAndSolitonicBranes)) was considered only later in the context of the hypothesis of [[D-brane charge quantization in K-theory]] &lbrack;[Bergman, Gimon & Hořava 1999, §2.2 & §2.3](#BergmanGimonHořava99), building on earlier discussion by [Witten 1998, §4.1](#Witten98)&rbrack; to be discussed further [below](#Examples).

But beware that the distinction between these two aspects of D-branes, while "well-known", is not commonly highlighted in the literature (not even in these original articles).
\end{remark}

The above flux densities in 11d and 10d are closely related:

Consider the case of C-field flux densities $G_4$ and $G_7$ an an 11-dimensional spacetime $X^{11}$ which is the total space of a [[circle group|circle]]-[[principal bundle]] over a 10-dimensional base manifold $X^{10}$, and denote by

* $\theta \,\in\, \Omega^1_{dR}(X^{11})$ any fiberwise [[Maurer-Cartan form]] along the fibers (i.e. an [[Ehresmann connection]] form),

* $F_2 \,\in\, \Omega^2_{dR}(X^{10})$ the corresponding ([[first Chern class|first]]) [[Chern class]]-[[characteristic form]], i.e. the [[curvature]] form whose [[pullback of differential forms|pullback]] to $X^{11}$ is

  $$
    \mathrm{d} \theta
    \;=\;
    p^\ast F_2
    \,.
  $$

Assuming that all flux densities are $S^1$-inavariant (hence focusing on their 0th [[Kaluza-Klein reduction|KK-modes]]) they decompose into a [[basic differential form|basic]] component (a differential form on $X^{10}$, [[pullback of differential forms|pulled back]] along the projection $p$) and the [[wedge product]] of a [[basic differential form]] with the [[Maurer-Cartan form]] $\theta$ on the $S^1$-fibers:

\[\label{KKComponentsOfCFieldFlux}\]

\begin{imagefromfile}
    "file_name": "GeomPhys-DDReductionOfCFieldFlux.jpg",
    "width": 330,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This is the process of "[[double dimensional reduction]]" -- called this way since both spacetime dimension is reduced by [[Kaluza-Klein reduction]] on a fiber space, but also the degrees of densities of fluxes "through the fiber space" are decreased -- known as part of the [[duality between M-theory and type IIA string theory]]: The new component flux densities $H_3$ and $H_7$ are interpreted as those of the [[B-field]] and the component flux densitirs $F_4$ and $F_6$ (and $F_2$) as those of the [[RR-field]] in [[type IIA supergravity]].

Here the flux density $F_2$, which in 10d is understood as witnessing singular [[D6-brane|$D_6$-brane]] sources, is a $\color{orange}\text{gravitational}$ flux from the 11d point of view: If $X^{10} \,=\, \mathbb{R}^{6,1} \times \mathbb{R}_{\gt 0} \times S^1$ is the spacetime domain around a flat singular [[D6-brane]], then the total space of the circle-principal bundle $X^{11}$ (a multiple of the [[complex Hopf fibration]]) is known as the corresponding "[[KK-monopole]]" spacetime.

This transmutation, under [[Kaluza-Klein compactification]], of parts of the gravitational field in higher dimensions into [[gauge fields]] in lower dimensions is a major subtlety in choosing [[flux quantization]] laws: Since these laws apply to higher gauge fields but not directly to the field of gravity, there may appear new possibilities for flux quantization after [[KK-reduction]] to lower dimensions which do not come from flux quantization in higher dimensions. 


\linebreak


### Equations of motion of higher flux
 {#EquationsOfMotionOfFlux}

As we now turn to the [[equations of motion]] for [[flux densities]] (the analogs of [[Maxwell's equations]] for [[electromagnetic field|electromagnetic]] flux), the key move towards identifying possible [[flux quantization laws]] ([below](#FluxQuantizationLaws)) is to arrange these equations, equivalently, as:

1. a purely *[[cochain cohomology|cohomological]]* system of [[differential equations]] known as higher *[[Bianchi identities]]*;

1. a purely *[[geometry|geometric]]* system of [[linear equations]] expressing a *[[Hodge duality|Hodge self-duality]]*,

the point being that the first item is entirely "[[algebraic topology|algebro-topological]]" ([[homotopy theory|homotopy-theoretic]]),  while dependency on geometry,  namely on the [[spacetime]] [[pseudo-Riemannian metric|metric]]  (the [[field (physics)|field]] of [[gravity]]) is all isolated in the second item.

It turns out &lbrack;[SS23-FQ](#SS23-FQ)&rbrack; that from such *duality-symmetric laws of flux*, the [[canonical phase space]] of the [[higher gauge theory]], including the [[flux quantization|flux-quantization structure]] may be obtained straightforwardly, *without* going through the traditional and thorny route of [[BRST complex|BRST-]][[BV formalism|BV analysis]] based on an [[stationary action principle]] given by a [[Lagrangian density]]. 

\begin{imagefromfile}
    "file_name": "GeomPhys-PhaseSpaceFromEOMsSchematics-240125.jpg",
    "width": 860,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


This move of isolating "pre-metric flux equations" supplemented by a "constitutive" duality constraint has a curious status in the  literature. On the one hand, it is elementary and immediate as an equivalent re-formulation of the usual form of (higher) Maxwell-type equations of motion,
and as such has been highlighted a century ago  &lbrack;[Kottler (1922a)](pre-metric+electromagnetism#Kottler22a), [(1922b)](pre-metric+electromagnetism#Kottler22b), [Cartan (1924) §80](pre-metric+electromagnetism#Cartan24), [Dantzig (1934)](pre-metric+electromagnetism#Dantzig34)&rbrack; and again more recently &lbrack;[Hehl & Obukhov (2003)](pre-metric+electromagnetism#HehlObukhov03), [Delphenich (2005a)](pre-metric+electromagnetism#Delphenich05a), [(2005b)](pre-metric+electromagnetism#Delphenich05a)&rbrack; (see the surveys [Hehl, Itin & Obukhov 2016](pre-metric+electromagnetism#HehlItinObukhov16) and [Delphenich (202x)](pre-metric+electromagnetism#DelphenichBook)). 

While the broader community does not seem to have taken much note of "premetric electromagnetism" as such, we notice that just the same perspective is evidently what string theorists call "duality-symmetric" &lbrack;[Bandos, Berkovits & Sorokin 1998](#BandosBerkovitsSorokin98)&rbrack; or "democratic" &lbrack;[Mkrtchyan & Valach 2023](#MkrtchyanValach23)&rbrack; formulations of fluxes in supergravity  (see Examples \ref{MotionOfSupergravityCField} and \ref{MotionOfCoupledBRRFields} below).



\begin{definition}\label{HigherMaxwellEquations}
**Higher Maxwell-type equations** (in vacuum)
on a [[tuple]] (eq:TheHigherFluxDensities) of [[flux]] [[differential forms]] $\vec F \,\equiv\, \big\{F^{(i)}\big\}_{i \in I}$ of any degree $deg_i \geq 1$ on a [[dimension of a manifold|$D$-dimensional]] [[spacetime]] $X^D$ (a [[pseudo-Riemannian manifold]]) of any dimension $D = d+1 \geq 2$ , is:

1. any system of [[polynomial]] $\vec P(-)$ first order [[exterior derivative|exterior]]-[[differential equations]] $\mathrm{d} \vec F \,=\, \vec P\big(\vec F\big)$ (the higher [[Bianchi identities]], crucially admitting polynomial "self-sourcing" of fluxes);

1. subject to a [[linear map|linear]] $\vec \mu(-)$ [[Hodge star operator|Hodge]]-[[duality-symmetric higher gauge theory|self-duality]] relation $\star \vec F \,=\, \vec \mu\big(\vec F\big)$ (the "[[constitutive equation]]"):

\[\label{EqHigherMaxwellEquations}\]
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

Concretely:

* $\vec P$ is an $I$-tuple of graded-symmetric [[polynomials]] with [[rational numbers|rational]] [[coefficients]] in $I$ [[variables]] of degrees $\vec deg$,

* $\vec \mu$ is a [[linear map|linear]] [[endomorphism]] on the [[vector space]] [[linear span|spanned]] by these variables.

\end{definition}

\begin{remark}
The equations in Def. \ref{HigherMaxwellEquations} imply that $\vec P$ and $\vec \mu$ respect degrees in a certain evident way. Moreover, the following property of the [[Hodge star operator]] on [[Lorentzian manifolds]] (see [there](Hodge+star+operator#eq:HodgeSquareOnRiemannian)) implies further constraints on the available higher Maxwell-type equations:
\[
  \label{HodgeSquareOnLorentzianSpacetime}
  \star 
  \,
  \star
  \,
  F_{deg}
  \;\;
  =
  \;\;
  -(-1)^{deg(D-deg)}
  \,
  F_{deg}
  \,,
  \;\;\;\;\;\;\;\;
  \text{for}
  \;
  F_{deg}
  \,\in\,
  \Omega^{deg}_{dR}(X^D)
  \,.
\]
This controls notably the existence of genuinely [[self-dual higher gauge theories]], see Ex. \ref{MotionOfSelfDualHigherGaugeFluxes} below.

\end{remark}


\begin{remark}
Not all higher gauge theories are of the higher Maxwell-form (Def. \ref{HigherMaxwellEquations}): For instance [higher Chern-Simons type theories](higher+gauge+field#OfChernSimonsType) are different.
\end{remark}


\begin{example}\label{MotionOfElectromagneticField}
**(Motion of the ordinary electromagnetic fluxes)**

The classical [[Maxwell equations]] expressed in terms of differential forms (see basic references [here](Maxwell's+equations#ReferencesForMaxwellEquationsViaDifferentialForms)) are as shown on the left, with their [[premetric electromagnetism|premetric]] form shown on the right (see the references [there](pre-metric+electromagnetism#ReferencesPremetricElectromagnetism)):

\begin{imagefromfile}
    "file_name": "GeomPhys-MotionOfElectromagnetism.jpg",
    "width": 430,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Here the [[differential 3-form]] $J_3$ embodies the density of an [[electric current]] carrying an [[electric field]] and inducing a [[magnetic field]]. This kind of *[[background field|background]]* source term, where the source is not given by (a polynomial in) the flux densities themselves, does not fit into the Definition \ref{HigherMaxwellEquations} and shall be disregarded for the purpose of the present discussion, meaning that we focus on the special case of Maxwell's equations "in vacuum":

\begin{imagefromfile}
    "file_name": "GeomPhys-MotionOfVacuumElectromagnetism.jpg",
    "width": 430,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{example}

It is clear that, mathematically at least, Ex. \ref{MotionOfElectromagneticField}, makes sense more generally for flux densities of any degree. In particular:


\begin{example}\label{MotionOfUnboundedRRFields}
**(Motion of unbounded [[RR-field]] fluxes)**

The [[equations of motion]] of the [[RR-field]] fluxes in [[D=10 supergravity]] in the case of vanishing [[B-field]]-fluxes are often taken to be as follows (e.g. [Mkrtchyan & Valach 2023](#MkrtchyanValach23)):

\[\label{PureUnboundedRREquations}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-MotionOfPureRRFluxes.jpg",
    "width": 780,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

> (While we may think of $\bullet$ as ranging over all [[natural numbers]] -- which is suggestive in view of [[D-brane charge quantization in topological K-theory|Hypothesis K]] discussed below -- of course on the given spacetime manifold of dimension $D=10$ all differential forms of degree $\gt 10$ vanish identically.)

and, more generally, those with non-vanishing [[B-field]] as follows:

\[\label{TwistedUnboundedRREquations}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-UnboundedBRRFluxMotion.jpg",
    "width": 780,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Beware, while these equations are now often stated in this form, and while this is the form that motivates the traditional [[D-brane charge quantization in topological K-theory|Hypothesis K]], it is at least subtle to see them in entirety as actually arising from ordinary [[D=10 supergravity]] (namely from [[KK-compactification]] of [[D=11 supergravity]]), since in that context: 

1. The fluxes $F_0$ and $F_{10}$ are not actually present (they arise only in [[massive type IIA supergravity]], which has its own subtleties).

1. The flux $H_7$ has a non-linear [[Bianchi identity]] ($\mathrm{d} H_7 \,=\, -F_4 \wedge F_4 + F_2 \wedge F_6$) which does not fit the suggestive pattern.

For more on this see Ex. \ref{MotionOfCoupledBRRFields} below.
\end{example}

Notice that in type IIB, (eq:PureUnboundedRREquations) describes a flux density ($F_5$) which is Hodge dual (not just to any other flux in the tuple but) to itself, $F_5 \,=\, \star\, F_5$. Generally we have:



\begin{example}\label{MotionOfSelfDualHigherGaugeFluxes}
**(Motion of [[self-dual higher gauge field]] fluxes)**

Since Def. \ref{HigherMaxwellEquations} regards *every* higher gauge theory as being "self-dual" in a sense, the [[equations of motion]] of [[flux densities]] of actual [[self-dual higher gauge fields]] -- in the strict sense that one and the same flux density form is required to be Hodge dual to itself -- are readily an example of Def. \ref{HigherMaxwellEquations}:

\[\label{SelfDualHigherFluxEquationsOfMotion}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-MotionOfSelfDualFlux.jpg",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Due to the properties of the square of the Hodge operator (eq:HodgeSquareOnLorentzianSpacetime),
this has non-trivial solutions iff the degree of the flux is odd, $deg = 2k+1$, and hence iff spacetime dimension is $D = 4k + 2$, $k \in \mathbb{N}$.
\end{example}

What is much more clear-cut than the example of fluxes in [[D=10 supergravity]] (Ex. \ref{MotionOfUnboundedRRFields}) is the following example of fluxes in [[D=11 supergravity]], where at least on flat spacetimes there is no ambiguity in the literature:


\begin{example}\label{MotionOfSupergravityCField}
**(Motion of [[supergravity C-field|C-field]] fluxes)**

The equations of motion of the [[supergravity C-field|C-field]] in [[D=11 supergravity]] (originally the "3-index A-field" due to [Cremmer, Julia & Scherk 1978](D=11+supergravity#CremmerJuliaScherk78), see also [D'Auria & Fré 1982, p. 131](D=11+supergravity#DAuriaFré82); [Castellani, D'Auria & Fré 1991, §III.8](D=11+supergravity#CastellaniDAuriaFré91); [Miemiec & Schnakenburg 2006, p. 32](D=11+supergravity#MiemiecSchnakenburg06)) are traditionally as shown on the left here, with their equivalent "duality-symmetric" reformulation shown on the right (see the references [there](duality-symmetric+higher+gauge+theory#PremetricCFieldReferences)):

\[\label{CFieldEquationsOfMotion}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-MotionOfCField.jpg",
    "width": 580,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{MotionOfCoupledBRRFields}
**(Motion of type IIA B&RR-field fluxes)**

Under [[double dimensional reduction]] of the C-field flux from Ex. \ref{MotionOfSupergravityCField} along a [[circle]]-[[bundle]] as in (eq:KKComponentsOfCFieldFlux), the equations of motion (eq:CFieldEquationsOfMotion) of the C-field from are equivalently expressed in terms of its [[B-field|B]]&[[RR-field]]-components as follows &lbrack;[Mathai & Sati 2004, §4](duality+between+M-theory+and+type+IIA+string+theory#MathaiSati04); [FSS17-Sph, §3](#FSS17SphereCocycles); see also [Figueroa-O'Farrill & Simón 2003, §1.2](#Figueroa-O'FarrillSimón03)&rbrack;:

\[\label{BRRFieldEquationsOfMotion}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-DoubleDimReductionOfCField-240127.jpg",
    "width": 810,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

These are the equations of motion of the flux densities of [[type IIA supergravity]] in their duality-symmetric formulation &lbrack;[Cremmer, Julia, Lu & Pope 1998, §3](#CremmerJuliaLuPope98)&rbrack;. 

Several terms in (eq:BRRFieldEquationsOfMotion) deserve special attention, either for how they appear or for how they do *not* appear:

1. The Hodge dual $F_8 \,\coloneqq\, \star \, F_2$ is *not* part of the C-field in 11d, but is part of the gravitational field (the Hodge star encodes the 10d metric and $F_2$ is an aspect of the 11d fiber geometry). The expression for $\mathrm{d} H_8$ arises as part of the gravitational field equations &lbrack;[Cremmer, Julia, Lu & Pope 1998 (3.4)](#CremmerJuliaLuPope98)&rbrack;.

1. The presence in [[type IIA supergravity]] of the non-linear Bianchi identity for $H_7$, albeit readily verified and "well-known" at least since [CJCP98 (3.4)](#CremmerJuliaLuPope98), is not as widely appreciated as the pattern (eq:TwistedUnboundedRREquations) from Ex. \ref{MotionOfUnboundedRRFields} -- which it *breaks*.

1. No flux densities $F_0$ nor $F_{10}$ appear in 10d from [[KK-reduction]] on a circle, nor are they part of [[type IIA supergravity]]. These fluxes are instead part of [[massive type IIA supergravity]] whose relation to [[D=11 supergravity]]/[[M-theory]] remains less understood, see the references [here](massive+type+IIA+string+theory#ReferencesLiftToMTheory).

\end{example} 




\linebreak


### Solution space of the flux equations
 {#SolutionSpaceOfHigherMaxwellEquations}

**The phase space.** Abstractly, the *phase space* of a any [[field theory]] is nothing but the space of all those [[field histories]] that satisfy the given [[equations of motion]] (the "[[on-shell]]" field histories). Phrased this way, this is sometimes called the 
*[[covariant phase space]]*, to emphasize that no choice of [[foliation]] of spacetime by [[Cauchy surfaces]] has been or needs to be made.

\begin{imagefromfile}
    "file_name": "CanonicalAndCovariantPhaseSpace-240124.jpg",
    "float": "right",
    "width": 610,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 10,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The more traditionally familiar
**[[canonical phase space]]** (common physics jargon, somewhat incompatible with the mathematician's "canonical") is instead a parameterization of the covariant phase space by [[initial value data]] on a choice of [[Cauchy surface]]. 
This choice breaks the "manifest covariance" of the covariant phase space. Nevertheless, if a Cauchy surface exists at all (hence on [[globally hyperbolic spacetimes]]), then both these phase spaces are equivalent, by definition, the equivalence being the map that generates from [[initial value data]] the essentially unique [[on-shell]] [[field history]] that evolves from it (possibly up to [[gauge transformation]]).

**Solution space of on-shell flux densities.** At this point in our discussion, we do not yet know what the full field content of our field theories really is -- this will be implied by a choice of flux quantization [below](#FluxQuantizationLaws) -- we only know the corresponding [[flux densities]]. To remember this, we shall call the space of flux densities solving their equations of motion (Def. \ref{HigherMaxwellEquations}) the *solution space*, and we are after its incarnation as a *canonical solution space* of initial value data on a Cauchy surface. But this goes a long way, since the higher Maxwell-type equations of motion constrain exclusively the flux densities: Once the flux-quantization the canonical phase will simply consist of all flux-quantized [[gauge potentials]] compatible with the flux densities in the canonical solution space.

\begin{proposition}\label{SolutionSpaceViaGaussLaw}
**([SS23-FQ](#SS23-FQ))**
  On a [[globally hyperbolic spacetime]] $X^D \,\simeq\, \mathbb{R}^{0,1} \times X^d$, the solution space to [higher Maxwell-equations](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) of motion (Def. \ref{HigherMaxwellEquations}) is [[isomorphism|isomorphic]] to the solution of the [[Bianchi identities]] restricted to any [[Cauchy surface]] $\iota \,:\, X^d \hookrightarrow X^D$, there to be called the higher *[[Gauß law]]*:

\[\label{GaussLawFromBianchiIdentities}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-HigherMaxwellSolutionSpace.jpg",
    "width": 850,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 5,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{proposition}

\begin{example}
**(the phase space of electromagnetism)**
\linebreak
In the case of ordinary vacuum [[electromagnetism]], Prop. \ref{SolutionSpaceViaGaussLaw} applied to the ordinary Maxwell equations from Ex. \ref{MotionOfElectromagneticField} says that the initial value data on a Cauchy surface $X^3$ is given by *independently* specifying magnetic and electric flux densities 

$$
  B,\, E \,\in\, \Omega^2_{dR}(X^3)
$$ 

subject only to the [ordinary Gauß laws](Gauss+law#InElectromagnetism):

$$
  \mathrm{d} B \,=\, 0
  \,,\;\;\;
  \mathrm{d} E \,=\, 0
  \,.
$$

Indeed, the actual [[phase space]] of electromagnetism, after [[Dirac charge quantization]], is well-known (see [there](electromagnetism#ReferencesPhaseSpaceAndPoissonBrackets)) to have as

* [[canonical coordinate]] the [[gauge potential]] $A$,

* [[canonical momentum]] the electric flux density $E$.

Thereby $B \,\equiv\, \mathrm{d}A$ is indeed independent from $E$ (and satisfies its Gauß law definitionally, while the Gauß law on $E$ is a phase space [[constrained mechanics|constraint]]).

Notice how, thereby, this traditional split of [[initial value data]] into [[canonical coordinates]] and [[canonical momenta]] (whose definition requires assumption and [[variational calculus|variation]] of a [[Lagrangian density]]) is preempted here, under Prop. \ref{SolutionSpaceViaGaussLaw}, already by the pregeometric/duality-symmetric formulation of Maxwell's equations (in Ex. \ref{MotionOfElectromagneticField}), in the sense that the spacetime archetypes of the canonical coordinates and momenta   on a Cauchy surface (the former seen under the differential) are just the ordinary flux density $F_2$ and its "duality partner" $G_2$.
\end{example}


\begin{remark}\label{GravityDecouplesOnCanonicalPhaseSpace}
**(Gravity "decouples" on canonical phase space)**
\linebreak
The inverse isomorphism (eq:GaussLawFromBianchiIdentities) is given by time evolution of initial value data. Notice that the [[pseudo-Riemannian metric]] on $X^D$ -- the [[background field]] of [[gravity]] -- enters *only* in determining the nature of this isomorphism $\iota^\ast$ (the time evolution away from the Cauchy surface), but does not affect the nature of the initial value data (of the canonical phase space) as such.
\end{remark}

It is this "decoupling" *on the canonical phase space* of the gravity/metric effects from the phase space [[Gauß law]] constraint which allows to gain plenty of insight into brane configurations from purely cohomological analysis of fluxes on Cauchy surfaces, disregarding the full solution of the coupled (super-)gravity equations of motion:


### Qualitative solutions: Brane intersections
 {#BraneIntersectionsImprintedOnFlux}

Prop. \ref{SolutionSpaceViaGaussLaw} implies that on [[globally hyperbolic spacetimes]] the structure of [[on-shell]] flux densities in [[supergravity]] may be analyzed already by solving the (non-linear) [[Gauss law]] (eq:GaussLawFromBianchiIdentities) on any [[Cauchy surface]] and ignoring the coupling to [[gravity]] there (assuming only that there exists at least one gravitational field configuration which solves its [[Einstein equations]] with source terms of this form). Since the same Gauss law also governs the admissible flux quantization laws [below](#FluxQuantizationLaws) we showcase a couple of qualitative solutions to highlight just how much non-trivial (brane-)physics is encoded in these equations.

\begin{example}\label{D6CreationAndHananyWittenEffect}
**([[D6-D8 brane bound state|D6/D8-intersections]] and the [[Hanany-Witten effect]])**
A popular conjecture by [Hanany & Witten 1997](#Hanany-Witten+effect#HananyWitten97) states that the expected $\mathrm{D}_{\!p}$-branes stretching between $\mathrm{NS}_5$ and  $\mathrm{D}_{p+2}$ (cf. [above](#HigherFluxAndItsBranes)) are "created" as the $\mathrm{D}_{\!p+2}$-branes are "dragged over" the $\mathrm{NS}_5$, intuitively like a pole will cause a spike in a rubber sheet that is pulled over its tip. It was suggested by [Marolf 2001 (§2)](Hanany-Witten+effect#Marolf01) that this *[[Hanany-Witten effect]]* should be understandable entirely from analysis of the flux Bianchi identities (eq:GaussLawFromBianchiIdentities). 

For the case of [[D6-D8 brane bound states|NS5/D6/D8-brane intersections]] &lbrack;[Hanany & Zaffaroni 1998 (§2.4)](Hanany-Witten+effect#HananyZaffaroni98); [Bergshoeff, Lozano & Ortin 1998 (p. 60)](Hanany-Witten+effect#BergshoeffLozanoOrtin98) this may be seen as follows (the other cases work analogously):

Here, by the flux equation (eq:TwistedUnboundedRREquations) 
\[
  \label{EquationsForHananyWittenEffectForD6D8}
  \begin{array}{l}
  \mathrm{d} F_0 \;=\; 0
  \,,
  \\
  \mathrm{d}
  \,
  F_2
  \;=\;
  H_3 \wedge F_0
  \,,
  \end{array}
\]
the flux density $F_0$ of $\mathrm{D}_8$-branes (the "Romans mass") is a [[locally constant function]] that vanishes in the vacuum and jumps by $N$ units across the singular locus of $N$ [[D8-branes|$\mathrm{D}_8$-branes]] (cf. e.g. [Fazzi 2017 (p. 40)](NS5-brane#Fazzi17)).
But this means that:

\begin{imagefromfile}
    "file_name": "FluxesOfD6BetweenNS5AndD8-230618b.jpg",
    "float": "right",
    "width": 580,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": -40, 
        "left": 10
    }
\end{imagefromfile}


(1.) When the [[NS5-brane|$\mathrm{NS}_5$-brane]] is located in the vacuum where $F_0 = 0$, then its sourcing of $F_{2}$-flux is "switched off" by the vanishing $F_0$-factor 
in (eq:EquationsForHananyWittenEffectForD6D8), hence if $F_2$ vanishes at infinity then the [[PDE]] demands it vanishes everywhere,  reflecting the absence of [[D6-branes|$\mathrm{D}_6$-branes]].

(2.) When the [[NS5-brane|$\mathrm{NS}_5$-brane]] is located on the other side of the [[D8-brane|$\mathrm{D}_8$-branes]], where $F_0 = N$, then the equation (eq:EquationsForHananyWittenEffectForD6D8) shows that $F_2$-flux/[[D6-brane|$\mathrm{D}_6$]]-number density which vanishes far away will increase along the coordinate axis $x^9$ orthogonal to the [[D8-branes|$\mathrm{D}_8$-branes]] in proportionality to the $\mathrm{d}x^9$-component of the flux $H_3$, and hence pronouncedly so as one crosses the [[NS5-brane|$\mathrm{NS}_5$-brane]] locus.

\end{example}

\begin{example}
**([[M2/M5-brane bound state|M2$\perp$M5-brane intersections]] on [[M-strings]])**
\linebreak
Consider the singular loci of two parallel flat [[M5-branes]] at a distance $2d \gt 0$

\begin{tikzcd}[sep=0pt]
    \mathbb{R}^{1,5}_{{}_{(i)}}
    \ar[rr, hook]
    &&
    \mathbb{R}^{1,D}
    \\
    (t,\vec x) 
      &\mapsto& 
    \big(t,\vec x, (-1)^i d, \vec 0\big)
\end{tikzcd}

each reflected by unit 4-flux through their sourrounding [[4-spheres]]:

$$
    G_4^{{}^{(i)}}
    \;\coloneqq\;
    \mathrm{dvol}_{S^4}
    \,\in\,
    \Omega^4_{\mathrm{dR}}(S^4)
    \xhookrightarrow{ \quad \mathrm{pr}_{S^4}^\ast \quad}
    \Omega^4_{\mathrm{dR}}\Big(
      \mathbb{R}^{1,5}_{{}_{(i)}}
      \times
      \mathbb{R}_{\plus}
      \times
      S^4
    \Big)
    \;\simeq\;
    \Omega^4_{\mathrm{dR}}\Big(
      \mathbb{R}^{1,10}
      \setminus
      \mathbb{R}^{1,5}_{{}_{(i)}}
    \Big)
  \,.
$$

With the total 4-flux thus
$
  G_4 
  \;\coloneqq\;
  G_4^{(1)}
  +
  G_4^{(2)}
  \,,
$
the [[supergravity C-field|C-field]] Bianchi identity (Ex. \ref{MotionOfSupergravityCField}) says that the flux $G_7$ sourced by [[M2-branes]] obeys the equation

\[
  \label{M2FluxSourcedSourceByTwoM5Branes}
  \begin{array}{rcl}
    \mathrm{d}
    G_7
    &=&
    -
    \tfrac{1}{2} G_4 \wedge G_4
    \\
    &=&
    - G_4^{(1)} \wedge G_4^{(2)}
  \end{array}
\]

where the wedge product of the two translated $S^4$-volume forms acts as an effective "[[electric current|electric potential]]" source term.

For illustration purposes we consider a qualitative sketch of  the 2-dimensional analog of this situation, where the 4-forms are replaced by 2-forms:

\begin{imagefromfile}
    "file_name": "GeomPhys-FluxOfM2M5Intersection.jpg",
    "float": "right",
    "width": 380,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}

**Effective dipole of quadratic brane flux.**
The figure means to indicate the nature of the differential 2-form which is the wedge product of two copies of the pullback of $\mathrm{dvol}_{S^1}$ to around either of the punctures (the brane loci) in the 2-punctured plane. Here:

* the strength of the circular lines indicates the absolute value of the flux density sourced by the respective 5-brane,

* the arrows indicate the orientation of the flux density of either 5-brane,

* the parallelograms indicate the orientation of their wedge product.

Evidently, the absolute value of the wedge product is concentrated near the 5-branes and particularly between them...


\begin{imagefromfile}
    "file_name": "GeomPhys-SourcingM2FluxFromM5Fluxes.jpg",
    "float": "right",
    "width": 670,
    "unit": "px",
    "margin": {
        "top": -35,
        "bottom": 0,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}


...but the orientation of the wedge product changes sign across the axis connecting the branes, as shown. This means that the flux *sourced* by this wedge product, according to (eq:M2FluxSourcedSourceByTwoM5Branes), is, if vanishing at infinity, concentrated between the branes.

This sourced flux concentration (indicated in red) witnesses an [[M2-brane]] stretching between the two [[M5-branes]]. The [[brane intersection|intersection]] is known as the *[[M-string]]*.

\end{example}

Notice how in these examples we *chose* integral values for the total source brane fluxes. Next we discuss how such *flux quantization* is systematically added to the higher gauge theory.



## Flux/Charge quantization laws
 {#FluxQuantizationLaws}

With the solution space (Prop. \ref{SolutionSpaceViaGaussLaw}) of higher Maxwell-type equations of motion (Def. \ref{HigherMaxwellEquations}) in hand, the question of flux quantization is to further constrain the [[flux densities]] such that the total fluxes through closed hypersurfaces (notably through [[n-spheres]]) only take certain discrete values.

The technical issue to be resolved here is that:

* this is a *global condition* on the flux densities: The local flux densities may take any value (compatible with the equations of motion) and yet the accumulation of all these local contributions over a hypersurface needs to be constrained;

* the evident idea of constraining the ordinary [[integration of differential forms|integrals]] of the [[flux densities]] (their "[[periods]]") makes sense only for [[closed differential forms]] and hence does not work for non-linear Bianchi identities (such as those of the [[supergravity C-field|C-field]], Ex. \ref{MotionOfSupergravityCField}, and the B&RR-field, Ex. \ref{MotionOfCoupledBRRFields}).

To solve this, one may first observe that:

\begin{imagefromfile}
    "file_name": "GeomPhys-IntegralFlux2.jpg",
    "float": "right",
    "width": 380,
    "unit": "px",
    "margin": {
        "top": 0,
        "bottom": 0,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}


* the [[integration of differential forms|integrals]]/[[periods]] of ordinary [[closed differential form|closed]] differential $n$-forms $F_n$ over $n$-manifolds are in [[natural bijection|natural correspondence]] with their [[de Rham cohomology|de Rham]]-[[cohomology class|classes]],  $[F_n] \in H^n_{dR}(-)$, which in turn are equivalently their "deformation classes", namely their *[[concordance]] [[equivalence class|classes]]*: $H^n_{dR}(-) \,\simeq\, \Omega^n_{dR}(-)_{clsd}\big/_{cncrdnc}$,

* so that integrality of closed flux density $F_n$ is witnessed by an integral cohomology class $[\chi] \in H^n(X;\mathbb{Z})$ whose "[[de Rham theorem|de Rham character]]" image $ch[\chi] \in H^n_{dR}(X)$ coincides with the deformation class $[F_n]$


and then that this perspective generalizes &lbrack;[FSS23-Char](#FSS23), [SS23-FQ](#SS23-FQ)&rbrack;:

\begin{imagefromfile}
    "file_name": "GeomPhys-StepsInFluxQuantization.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -35,
        "bottom": 20,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}

(1) Higher Maxwell-type equations (eq:EqHigherMaxwellEquations) have a **characteristic [[L-infinity algebra|$L_\infty$-algebra]]** $\mathfrak{a}$:
The flux densities are equivalently [[L-infinity algebra valued differential forms|$\mathfrak{a}$-valued differential forms]], and the [[Gauss law]] (eq:GaussLawFromBianchiIdentities) is equivalently the condition that these be *closed* (i.e.: [[flat L-infinity-algebra valued differential form|flat]], aka a "[[Maurer-Cartan element]]"; in [[D'Auria-Fre formulation of supergravity|Italian SuGra literature]]: "satisfying an FDA").
<br/>
(2.)  Also [[homotopy type|topological spaces]] $\mathcal{A}$ (under mild conditions) have a characteristic $L_\infty$-algebra: Their $\mathbb{R}$-rational  **[[Whitehead L-infinity algebra|Whitehead bracket $L_\infty$-algebra]]**.
<br/>
(3.) The **nonabelian** [[Chern-Dold character map]] turns $\mathcal{A}$-valued maps into [[flat L-infinity algebra valued differential forms|closed $\mathfrak{l}\mathcal{A}$-valued differential forms]], generalizing the [[Chern character]] for $\mathcal{A} =$ [[KU|$\mathrm{KU}_0$]].
<br/>
(4.) The **possible flux quantization laws** for a higher gauge field are those spaces $\mathcal{A}$ whose Whitehead $L_\infty$-algebra is the characteristic one.
<br/>
(5.) Given a flux quantization law $\mathcal{A}$, the corresponding **[[gauge potentials]]** are deformations of the flux densities into characters of a $\mathcal{A}$-valued map, witnessing the flux densities as reflecting discrete charges quantized in $\mathcal{A}$-cohomology.
<br/>
(It is not obvious that this reduces to the usual notion of gauge potentials, but it does.)
<br/>
(6.) These non-perturbatively completed higher gauge fields form a *[[smooth infinity-groupoid|smooth higher groupoid]]*: the "canonical **[[nonabelian differential cohomology|differential $\mathcal{A}$-cohomology]]** [[moduli stack]]". Since these are now the flux-quantized [[on-shell]] [[field (physics)|fields]], this is the *[[phase space]]* of the flux-quantized higher gauge theory.


\begin{imagefromfile}
    "file_name": "GeomPhys-CanonNonabDiffCohomAsPhaseSpace2.jpg",
    "width": 870,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

This flux-quantized phase space hence subsumes the "solitonic" fields with non-trivial charge sectors $\chi$, and as such is a non-perturbative completion of the traditional phase spaces (which correspond to a fixed charge sector only, typically to $\chi = 0$).

Incidentally, it follows (as discussed below) that the choice of flux quantization law $\mathcal{A}$ not only defines the solitonic content of the theory but completely characterizes it:

\begin{imagefromfile}
    "file_name": "GeomPhys-TopologicalPhaseSpace.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -35,
        "bottom": 20,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}

The [[shape modality|shape]] (topological realization) of this phase space stack is the **space of topological fields**,

which implies that the [[ordinary homology]] of the phase space stack constitutes the **topological quantum observables** on the higher gauge theory.

Hence if one focuses only on the solitonic or *topological field*-content of the phase space, then we see plain [[nonabelian cohomology|$\mathcal{A}$-cohomology]] moduli of the Cauchy surface, with the full phase space stack serving to justify this object.

\linebreak

We now explain all this in more detail:

\linebreak


### Gauss laws as closure of $L_\infty$-valued forms

(...)

\linebreak


### Flux quantization laws as Nonabelian cohomology

(...)

\linebreak


### Phase spaces as Differential nonabelian cohomology

(...)

\linebreak


### Background fluxes as Twisting of cohomology

(...)


\linebreak

## Examples in String/M-Theory
 {#Examples}

(...)

\linebreak

### C-Field flux quantization in 11d

(...)

\linebreak

### B-&RR-Field flux quantization in 10d

(...)


\linebreak

## References


* {#Abrikosov57a} [[Alexei Abrikosov]], *On the Magnetic properties of superconductors of the second group*, Sov. Phys. JETP **5** (1957) 1174-1182; Zh. Eksp. Teor. Fiz. **32** (1957) 1442-1452 &lbrack;[spire:9138](https://inspirehep.net/literature/9138), [[Abrikosov-MagneticPropertiesOfSuperconductors.pdf:file]]&rbrack;

* {#Alfonsi24} [[Luigi Alfonsi]], *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;

* {#Alvarez85a} [[Orlando Alvarez]], *Cohomology and Field Theory*, talk at: *Symposium on Anomalies, Geometry, Topology*, Argonne IL (28-30 March 1985) &lbrack;[inspire:965785](https://inspirehep.net/conferences/965785), [pdf](https://lib-extopc.kek.jp/preprints/PDF/1985/8507/8507262.pdf), [[Alvarez-CohomologyAndFieldTheory.pdf:file]]&rbrack;

* {#BandosBerkovitsSorokin98} [[Igor Bandos]], [[Nathan Berkovits]], [[Dmitri Sorokin]], *Duality-Symmetric Eleven-Dimensional Supergravity and its Coupling to M-Branes*, Nucl. Phys. B **522** (1998) 214-233 \[<a href="https://doi.org/10.1016/S0550-3213(98)00102-3">doi:10.1016/S0550-3213(98)00102-3</a>, [arXiv:hep-th/9711055](https://arxiv.org/abs/hep-th/9711055)\]


* {#BergmanGimonHořava99} [[Oren Bergman]], [[Eric G. Gimon]], [[Petr Hořava]], *Brane Transfer Operations and T-Duality of Non-BPS States*, JHEP 9904 (1999) 010 &lbrack;[arXiv:hep-th/9902160](https://arxiv.org/abs/hep-th/9902160), [doi:10.1088/1126-6708/1999/04/010](https://doi.org/10.1088/1126-6708/1999/04/010)&rbrack;

* {#BlumenhagenLüstTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], _Brane solutions in supergravity_, chapter 18.5 in: _Basic Concepts of String Theory_, Springer (2013) &lbrack;[doi:10.1007/978-3-642-29497-6](https://doi.org/10.1007/978-3-642-29497-6)&rbrack;


* {#BFJKNRSW24} [[Leron Borsten]], [[Mehran Jalali Farahani]], [[Branislav Jurčo]], [[Hyungrok Kim]], [[Jiří Nárožný]], [[Dominik Rist]], [[Christian Saemann]], [[Martin Wolf]], *Higher Gauge Theory*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2401.05275](https://arxiv.org/abs/2401.05275)&rbrack;

* {#CremmerJuliaLuPope98} [[Eugene Cremmer]], [[Bernard Julia]], H. Lu, [[Christopher Pope]], Section 3 of: *Dualisation of Dualities, II: Twisted self-duality of doubled fields and superdualities*, Nucl. Phys. B **535**(1998) 242-292 $[$[arXiv:hep-th/9806106](https://arxiv.org/abs/hep-th/9806106), <a href="https://doi.org/10.1016/S0550-3213(98)00552-5">doi:10.1016/S0550-3213(98)00552-5</a>$]$


* {#Dirac31} [[P.A.M. Dirac]], _Quantized Singularities in the Electromagnetic Field_,  Proceedings of the Royal Society A **133** (1931) 60-72 &lbrack;[doi:10.1098/rspa.1931.0130](http://rspa.royalsocietypublishing.org/content/133/821/60.short)&rbrack;

* {#DuffLu94} [[Michael Duff]], [[Jian Xin Lu]], *Black and super $p$-branes in diverse dimensions*, Nucl. Phys. B **416** (1994) 301-334 &lbrack;[arXiv:hep-th/9306052](http://arxiv.org/abs/hep-th/9306052), <a href="https://doi.org/10.1016/0550-3213(94)90586-X">doi:10.1016/0550-3213(94)90586-X</a>&rbrack;


* {#Faraday1852} [[Michael Faraday]], *Delienation of Lines of Magnetic Force by iron filings*, §37 in: *Experimental Researches in Electricity.--Twenty-Ninth Series*, Philosophical Transactions of the Royal Society of London **142** (1852) 137-159 &lbrack;[doi:10.1098/rstl.1852.0012](https://doi.org/10.1098/rstl.1852.0012), [jstor:108540](https://www.jstor.org/stable/108540)&rbrack;

  > (the notion of "lines of force" is introduced on pp. 154)


* {#Figueroa-O'FarrillSimón03} [[José Figueroa-O'Farrill]], [[Joan Simón]], *Supersymmetric Kaluza-Klein reductions of M2 and M5-branes*, Adv. Theor. Math. Phys. **6** (2003) 703-793 &lbrack;[arXiv:hep-th/0208107](https://arxiv.org/abs/hep-th/0208107), [doi:10.4310/ATMP.2002.v6.n4.a4](https://doi.org/10.4310/ATMP.2002.v6.n4.a4)&rbrack;

* {#FSS17SphereCocycles} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Rational sphere valued supercocycles in M-theory|Rational sphere valued supercocycles in M-theory and type IIA string theory]]*, J. Geometry and Physics, **114** (2017) 91-108 &lbrack;[arXiv:1606.03206](https://arxiv.org/abs/1606.03206), [doi:10.1016/j.geomphys.2016.11.024](http://dx.doi.org/10.1016/j.geomphys.2016.11.024)&rbrack;



* {#FSS23} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;


* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], *[[Quantization of Gauge Systems]]*, Princeton University Press (1992) &lbrack;[doi:10.2307/j.ctv10crg0r](https://doi.org/10.2307/j.ctv10crg0r)&rbrack;

* {#Hyperphysics} Hyperphysics, *Magnetic Flux* &lbrack;[hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html](http://hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html)&rbrack;

* {#LoudonMidgley09} J. C. Loudon, P. A. Midgley, *Imaging Flux Vortices in Type II Superconductors with a Commercial Transmission Electron Microscope*, Ultramicroscopy **109** 6 (2009) 700-729 &lbrack;[arXiv:0807.2401](https://arxiv.org/abs/0807.2401), [doi:10.1016/j.ultramic.2009.01.008](https://doi.org/10.1016/j.ultramic.2009.01.008)&rbrack;


* {#Martin09} Thomas Martin (ed.), *Faraday's diaray of experimental investigation* 1820-1862, HR Direct (2009)  &lbrack;[webpage](http://faradaysdiary.com/), preview:[pdf](http://faradaysdiary.com/ws3/faraday.pdf)&rbrack;

* {#MkrtchyanValach23} [[Karapet Mkrtchyan]], [[Fridrich Valach]], *Democratic actions for type II supergravities*, Phys. Rev. D **107** 6 (2023) 066027 \[<a href="https://doi.org/10.1103/PhysRevD.107.066027">doi:10.1103/PhysRevD.107.066027</a>[arXiv:2207.00626](https://arxiv.org/abs/2207.00626)\]


* {#Polchinski95} [[Joseph Polchinski]], _Dirichlet-Branes and Ramond-Ramond Charges_, Phys. Rev. Lett. **75** (1995) 4724-4727 &lbrack;[arXiv:hep-th/9510017](https://arxiv.org/abs/hep-th/9510017), [doi:10.1103/PhysRevLett.75.4724](https://doi.org/10.1103/PhysRevLett.75.4724)&rbrack;


* {#MinasianMoore97} [[Ruben Minasian]], [[Gregory Moore]], *K-theory and Ramond-Ramond charge*, JHEP 9711:002 (1997) &lbrack;[arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230), [doi:10.1088/1126-6708/1997/11/002](https://doi.org/10.1088/1126-6708/1997/11/002)&rbrack;

* {#SS23-MF} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:M/F-Theory as Mf-Theory|M/F-Theory as $M f$-Theory]]*, Rev. Math. Phys. **35** 10 (2023) &lbrack;[doi:10.1142/S0129055X23500289](https://doi.org/10.1142/S0129055X23500289), [arXiv:2103.01877](https://arxiv.org/abs/2103.01877)&rbrack;

* {#SS23-FQ} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;

* {#SS23-Obs} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Quantum Observables of Quantized Fluxes]]* &lbrack;[arXiv:2312.13037](https://arxiv.org/abs/2312.13037)&rbrack;

* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. **22** 1   (1997) 1-13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), <a href="https://doi.org/10.1016/S0393-0440(96)00042-3">doi:10.1016/S0393-0440(96)00042-3</a>&rbrack;

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019 (1998) \[<a href="http://arxiv.org/abs/hep-th/9810188">arXiv:hep-th/9810188</a>, [doi:10.1088/1126-6708/1998/12/019](https://doi.org/10.1088/1126-6708/1998/12/019)\]

(...)

\linebreak

\linebreak

