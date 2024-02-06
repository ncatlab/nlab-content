
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
> * In the 1990s [[string theory|string theorists]] hypothesize that the combined flux of [[B-field|B-]]&[[RR-fields]] and hence the charge of [[D-branes]] is analogously quantized in a [[Whitehead-generalized cohomology|generalized]] cohomology theory called "[[twisted K-theory|twisted topological K-theory]]" &lbrack;[Minasian & Moore 1997](#MinasianMoore97); [Witten 1998](#Witten98)&rbrack;; 
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

## Overview
 {#Outline}


**([§2](#FluxDensitiesAndBraneSources))** A *[[higher gauge theory]]* (review includes [Alfonsi 2024, §2](#Alfonsi24); [BFJ${}^+$ 2024](#BFJKNRSW24)) [of Maxwell-type](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) (Def. \ref{HigherMaxwellEquations} below) is a ([[quantum field theory|quantum]]) [[field theory]] analogous to [[vacuum]]-[[electromagnetism]] ([[AQFT on curved spacetimes|on curved spacetimes]]), but with the analog of the electromagnetic [[flux density]] $F_2$ ([which ordinarily is](electromagnetic+field#FieldStrengthAsClosed2Form) a [[differential 2-form]] on 3+1 [[dimension of a manifold|dimensional]] [[spacetime]] $X^4$)  allowed to be a system of [[differential forms]] $\vec F \,\equiv\, \big\{F^{(i)}\big\}_{i \in I}$ of any degree $deg_i \geq 1$ on a [[dimension of a manifold|$D$-dimensional]] [[spacetime]] $X^D$ of any dimension $D = d+1 \geq 2$, and satisfying a higher analog of [[Maxwell's equations]] (eq:EqHigherMaxwellEquations).

Such [[higher gauge theories]] famously appear as the [[higher gauge field|gauge field]]-sector in higher-dimensional [[supergravity]] and hence in [[superstring|super]]-[[string theory|string]]/[[M-theory]], which is where they draw most of their motivation from. 

In analogy to how for ordinary [[Maxwell theory]] one may think of [[singularities]] or stable bumps in the [[flux density]] $F_2$ as being sourced by [[charges]] carried by (hypothetical) [[Dirac monopoles]] or by (observed) [[Abrikosov vortex strings]], respectively, so one may think of [[singularities]] or stable bumps in these higher flux densities as sourced by [[singular branes]] or [[solitonic branes]], respectively, for suitably higher dimensional ([[membrane|mem-]])[[branes]] carrying suitable higher charges.

\linebreak

**([§3](#FluxQuantizationLaws))** 
But for such [[singular brane|singular]]/[[solitonic branes]] to be "[[elementary particle|elementary]]" objects of individually discernible nature, their charges, and hence the total fluxes which they source, should have discrete ("quantized") values (as indeed observed for [[Abrikosov vortex strings]]). This is what *[[flux quantization]]* is about.

Traditionally one declares the full higher gauge field to be given by gauge potentials $\widehat A$ whose curvature is the flux density $\vec F$ and which is globally subjected to a topological condition that implies the flux and charge quantization. While this is classical for electromagnetism (and Yang-Mills theory), it is far from transparent, from this point of view, how to identify the structure of gauge potentials for general higher gauge theories.

More systematically, one may understand [[flux quantization]] as the specification of a [[generalized cohomology|generalized]] ([[nonabelian cohomology|non-abelian]]) [[cohomology theory]] for which the charges are required to be [[cocycles]], and of which the total fluxes are then the differential-geometric (Chern-Dold-)*[[Chern-Dold character|characters]]*.

From this modern point of view, the higher [[gauge potential]] and hence the full field content of the higher gauge theory, arises as the homotopy/gauge theoretic witness of the matching of total fluxes with the character of the charges, making the full higher gauge fields be cocycles in a corresponding generalized (nonabelian) *[[differential cohomology theory|differential]]* cohomology theory.

\linebreak

**([§4](#Examples))** Examples of [[flux quantization]] beyond [[Dirac charge quantization]] in [[electromagnetism]] play a key role in [[string theory|string]]/[[M-theory]]: 

  * the seminal "Hypothesis K" postulating [[D-brane charge quantization in K-theory]],

  * the more recent "[[schreiber:Hypothesis H]]" postulating [[M-brane]] charge quantization in unstable [[twisted Cohomotopy|twisted]] [[Cohomotopy]].

These hypotheses are not unrelated: Under "[[double dimensional reduction|double dimensional]] [[Kaluza-Klein reduction]]" along a [[circle]] [[fiber]], the [[supergravity C-field|C-field]] fluxes on $X^{10+1}$ are to give rise to *most* of the [[B-field|$B$-]]/[[RR-field]]-fluxes in $X^{9+1}$ (as part of the [[duality between M-theory and type IIA string theory]], which is either conjectural or defining, depending on attitude towards the definition of the elusive [[M-theory]]). Therefore [[schreiber:Hypothesis H]] may be understood as providing an [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *lift* of [[D-brane charge quantization in K-theory|Hypothesis K]] to the extent that it reduces to the latter under [[double dimensional reduction]], and as a [[non-perturbative effect|non-perturbative]]/[[M-theory|M-theoretic]] *correction* to the extent that it does not quite reduce to Hypothesis K.

\linebreak

**Perspective.** This highlights that a *choice* of flux quantization is (depending on perspective of how that higher gauge theory is ultimately defined):

* a hypothesis about 

or else

* a specification of 

the [[non-perturbative quantum field theory|non-perturbative completion]] of the given [[higher gauge theory]], which is generally an issue that deserves (more) attention.

Traditionally, flux quantization laws have been postulated sporadically and in ad-hoc fashion, in order to patch up "anomalous" theories: 
Since the ancient past it has been common to define any [[theory (physics)|physical theory]] by a [[stationary action principle]] embodied by a [[Lagrangian density]], from which a perturbative [[BRST complex]] is extracted, whose [[quantization]] (e.g. [Henneaux & Teitelboim 1992](#HenneauxTeitelboim92)) is generally afflicted with problems ("[[quantum anomalies|anomalies]]") some of which are dealt with by ad-hoc flux quantization: For example the original [[Dirac charge quantization]] was postulated to cure an anomaly in the quantum theory of an [[electron]] propagating in the background field of a [[magnetic monopole]] (a "0-brane"), while the enigmatic [[shifted C-field flux quantization]] similarly serves to cure an anomaly in the quantum theory of the [[M2-brane]] propagating in the background field of an [[M5-brane]] ([Witten 1996a, §2.2](#Witten96a)).

In contrast, in the modernized picture reviewed here, the available choices of flux-quantization laws $\mathcal{A}$ are [[algebraic topology|algebro-topologically]] determined by the form of the higher [[Gauss law]] on any [[Cauchy surface]], and any such choice, given by a compatible [[non-abelian cohomology]]-theory, determines the [[non-perturbative quantum field theory|non-perturbative]] [[phase space]] [[smooth infinity-stack|stack]] of flux-quantized gauge fields. This process makes no reference to [[Lagrangian densities]] and applies seamlessly to field theories that do not even have a natural Lagrangian description, such as [[self-dual higher gauge theories]].

Typically there is an "evident" choice of flux quantization and this is the choice tacitly made in the literature, where considered at all. But it is important to notice that there are other admissible choices, embodying hypotheses about (or definitions of) non-evident nonperturbative completions of the given higher gauge theory. 

\linebreak

**The logic of flux quantization.** The following table shows in outline the logic of algebro-topological flux quantization as reviewed here; on the left in generality and on the right for our running examples:

1. traditional [[Dirac charge quantization]] of the [[electromagnetic field]] (experimentally well-supported);

1. traditional [[D-brane charge quantization in topological K-theory|D-brane charge quantization]] in [[twisted K-theory|twisted]] [[topological K-theory]] ("Hypothesis K");

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

**(i) Bianchi-Gauss $L_\infty$-algebras.** The higher [[Bianchi identities]] of [duality-symmetric higher flux densities](higher+gauge+field#HigherGaugeTheoryOfMaxwellType), and hence their their higher [[Gauss law]] (Prop. \ref{SolutionSpaceViaGaussLaw}) are equivalent to the condition that the [[flux densities]] jointly constitute a [[flat L-infinity algebra valued differential form|closed $L_\infty$-algebra valued differential form]] with [[coefficients]] in a characteristic [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ (Prop. \ref{SolutionsAsFlatForms} below):

\begin{imagefromfile}
    "file_name": "GeomPhys-GaussLawAsFlatnessCondition-240128.jpg",
    "width": 740,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

**(ii) Whitehead $L_\infty$-algebras.** The [[classifying space]] $\mathcal{A}$ of any charge quantization law is [[rational homotopy type|rationally]] characterized by its [[rational numbers|rational]] [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]]  $\mathfrak{l}\mathcal{A}$ (essentially the "Quillen model" of $\mathcal{A}$: that $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{l}\mathcal{A})$ is the [[Sullivan model]] of $\mathcal{A}$) and the nonabelian [[Chern-Dold character]] map extracts from $\mathcal{A}$-cohomology its image in $\mathfrak{l}\mathcal{A}$-valued [[nonabelian de Rham cohomology]] (eq:NonabelianCharacterMap):

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


That these two $L_\infty$-algebras coincide is a consistency condition on the choice of the flux quantization law embodied by $\mathcal{A}$; and it implies that the non-abelian [[Chern-Dold character map]] $ch_{\mathcal{A}}$ from the [[non-abelian cohomology]]-theory classified by $\mathcal{A}$ takes values in the [[non-abelian de Rham cohomology]] with coefficients in $\mathfrak{l}\mathcal{A}$, which under $\mathfrak{l}\mathcal{A} \simeq \mathfrak{a}$ identifies with the total flux of [[flux densities]] satisfying their higher [[Gauss law]].

Finally, given such a choice of flux quantization law $\mathcal{A}$, the [[gauge potentials]] and hence the full [[moduli stack]] of [[higher gauge fields]] appears by forming the above matching not just as an identification in [[non-abelian de Rham cohomology]] but as a [[homotopy fiber product]] of the corresponding [[moduli stacks]]: This makes the full flux-quantized [[higher gauge fields]] be [[cocycles]] in [[nonabelian differential cohomology]] with coefficients in $\mathcal{A}$.

\begin{remark}\label{RoleOfLInfinityAlgebras}
**(the role of [[L-infinity algebra|$L_\infty$-algebras]]: curvature-coefficients instead of gauge potiential-coefficients)**
\linebreak
In comparison to more traditional discussions, beware that the (possibly non-abelian) [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ here controls the (possibly non-linear) [[Bianchi identities]]/[[Gauss law]] satisfied by the [[curvature forms]]/[[flux densities]] --- and thus is *not* the (higher) Lie algebra in which the [[gauge potentials]] take values, if any. (Even in the abelian case, where both types of coefficient $L_\infty$-algebras make sense, they differ by a degree-shift.)

This is an underappreciated use of [$L_\infty$-algebras in physics](L-infinity-algebra#ReferencesInPhysics), but it is known from the ["FDA"-method in supergravity](D'Auria-Fre+formulation+of+supergravity) and is tacitly familiar in traditional discussion of RR-flux/D-brane charge: 

Here the characteristic $L_\infty$-algebra $[b_2, \, v_{2\bullet-1}] = v_{2\bullet + 1}$ bears no resemblance to the [[Lie algebra]] [[special unitary Lie algebra|$\mathfrak{su}(n)$]], and yet after choosing [[D-brane charge quantization in topological K-theory]] it follows (an algebro-topological form of "[[gauge enhancement]]") that gauge potentials with coefficients in $\mathfrak{su}(n)$ (namely [[connection on a bundle|connections]] on Hermitean [[vector bundles]]) provide [[cocycles]] for the resulting [[differential K-theory]]. It is in this way (RR-flux quantization $\rightsquigarrow$ K-theory $\rightsquigarrow$ gauge bundles as cocycles) that non-abelian [[gauge fields]] appear on [[D-branes]].

In fact, flux quantization as discussed here does not apply to [[su(n)|$\mathfrak{su}(n)$]]-[[Yang-Mills theory]] directly:

Generally, not all [[L-infinity algebras|$L_\infty$-algebras]] appear as rational [[Whitehead L-infinity algebras|Whitehead $L_\infty$-algebras]] of (the [[homotopy type]] (eq:HomeoToHomotopyType) of) a topological space $\mathcal{A}$ that is amenable to [[rationalization]]; those that do are "[[nilpotent L-infinity algebra|nilpotent]]". 
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

In modern [[differential geometry|differential-geometric]] formulation, the [[flux density|density of these flux lines]] through any given [[surface]]-element is encoded in a [[differential 2-form]] $F_2$, as indicated in the following schematic graphics:

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


More in detail, with respect to any [[foliation]] $X^4 \simeq \mathbb{R}^1 \times X^3$ of a [[globally hyperbolic spacetime|globally hyperbolic]] [[spacetime]] $X^4$ by [[spacelike]] [[Cauchy surfaces]] $X^3$, the spatial component of $F_2$ is the *magentic flux density* $B$, while the [[Hodge duality|Hodge dual]]  (with respect to $X^4$) of the temporal component is the *electric flux density* $E$.

Imagining, as Dirac did, that Faraday's rod magnet could be made *infinitely* long and thin, any one of its poles would look like an isolated [[monopole|mono-pole]] with flux concentrating towards it from all directions:

\[\label{MagneticMonopoleSchematics}\]
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

As such, magnetic monopoles are the *[[singular brane|singular]] 0-[[branes]]* of electromagnetism (cf. [below](#TheDistinctionBetweenSingularAndSolitonicBranes)) --- in theory: Whether magnetic monopoles exist in nature remains open; they have not been seen in [[experiment]], but there are decent theoretical arguments that they should exist if the [[standard model of particle physics|standard model]] [[gauge group|symmetry]] is a [[broken symmetry]] [[grand unified theories|grand unified symmetry]].

On the other hand, the "[[solitonic branes]]" of electromagnetism (cf. again [below](#TheDistinctionBetweenSingularAndSolitonicBranes)) are experimentally well-established (and have famously been regarded as actual 1-[[branes]] ([[strings]]) approximated by a [[Nambu-Goto action]] &lbrack;[Nielsen & Olesen 1973](vortex+string#NielsenOlesen73); [Polyakov 2008, p. 1](vortex+string#Polyakov08); [Beekman & Zaanen 2011](vortex+string#BeekmanZaanen11)&rbrack;): These are the [[Abrikosov vortices]] formed in [[type II superconductors]] within a transverse magnetic field:

\[\label{AbrikosovVortexSchematics}\]
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

The [[near horizon geometry]] of any $\gt 1/4$ [[BPS state|BPS]] [[black brane]] are all [[product topological spaces|product spaces]] of an [[anti de Sitter spacetime]] with a ([free discrete quotient](group+actions+on+spheres#FreeActionsByFiniteGroupsAndSphericalSpaceForms) of) a [[sphere]] (a [[spherical space form]]) around the singularity &lbrack;[Acharya, Figueroa-O'Farrill, Hull & Spence 1999](near-horizon+geometry#AFFHS98)&rbrack;. On a causal chart of AdS spacetime, this is homeomorphic to the flat brane complements from Ex. \ref{FlatBranes}:

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

On this backdrop of ordinary electromagnetic flux ([above](#OrdinaryElectromagneticFluxAndItsBranes)) and of the general rule for measuring flux sourced by [[singular branes]] or [[solitonic branes]] ([above](#TheDistinctionBetweenSingularAndSolitonicBranes)) it clearly makes sense to consider [[theory (physics)|physical theories]] of [[higher gauge fields]] whose precise nature remains to be discussed, but whose flux densities are reflected in higher-degree differential forms $F^{(i)}(X^D)$, these possibly being of different field species to be labeled by a [[finite set|finite]] [[index set]] $I \in FinSet$ and jointly to be denoted as follows:

\[
  \label{TheHigherFluxDensities}
  \vec F
  \;\equiv\;
  \Big\{
    F^{(i)}
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

\begin{example}
**([[double dimensional reduction]] of fluxes form 11d to 10d)**
\linebreak
Consider the case of C-field flux densities $G_4$ and $G_7$ on an 11-dimensional spacetime $X^{11}$ which is the total space of a [[circle group|circle]]-[[principal bundle]] 

\begin{tikzcd}[sep=15pt]
  S^1 \ar[r, hook] &[-5pt] X^{11}
  \ar[d, "p"]
  \\
  & X^{10}
\end{tikzcd}

and denote by

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

This is the process of "[[double dimensional reduction]]" -- called this way since both spacetime dimension is reduced by [[Kaluza-Klein reduction]] on a fiber space, but also the degrees of densities of fluxes "through the fiber space" are decreased -- known as part of the [[duality between M-theory and type IIA string theory]]: The new component flux densities $H_3$ and $H_7$ are interpreted as those of the [[B-field]] and the component flux densities $F_4$ and $F_6$ (and $F_2$) as those of the [[RR-field]] in [[type IIA supergravity]].

Here the flux density $F_2$, which in 10d is understood as witnessing singular [[D6-brane|$D_6$-brane]] sources, is a $\color{orange}\text{gravitational}$ flux from the 11d point of view: If $X^{10} \,=\, \mathbb{R}^{6,1} \times \mathbb{R}_{\gt 0} \times S^2$ is the spacetime domain around a flat singular [[D6-brane]] (cf. [above](#TheDistinctionBetweenSingularAndSolitonicBranes)), then the total space of the circle-principal bundle $X^{11}$ (a multiple of the [[complex Hopf fibration]]) is known as the corresponding "[[KK-monopole]]" spacetime.
\end{example}

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

While the broader community does not seem to have taken much note of "premetric electromagnetism" as such, we notice that just the same perspective is evidently what in [[supergravity]] and [[string theory]] is called "duality-symmetric" &lbrack;[Bandos, Berkovits & Sorokin 1998](#BandosBerkovitsSorokin98)&rbrack; or "democratic" &lbrack;[Mkrtchyan & Valach 2023](#MkrtchyanValach23)&rbrack; formulations of fluxes in supergravity  (see Examples \ref{MotionOfSupergravityCField} and \ref{MotionOfCoupledBRRFields} below).



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
        "top": -20,
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

Since Def. \ref{HigherMaxwellEquations} regards *every* higher gauge theory (of Maxwell-type) as being "self-dual" in a sense, the [[equations of motion]] of [[flux densities]] of actual [[self-dual higher gauge fields]] -- in the strict sense that one and the same flux density form is required to be Hodge dual to itself -- are readily an example of Def. \ref{HigherMaxwellEquations}:

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
**(Motion of [[type IIA supergravity|type IIA]] [[B-field|B]]&[[RR-field]] fluxes)**

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

1. The presence in [[type IIA supergravity]] of the non-linear Bianchi identity for $H_7$, albeit readily verified and "well-known" at least since [CJLP98 (3.4)](#CremmerJuliaLuPope98), is not as widely appreciated as the pattern (eq:TwistedUnboundedRREquations) from Ex. \ref{MotionOfUnboundedRRFields} -- which it *breaks*.

1. No flux densities $F_0$ nor $F_{10}$ appear in 10d from [[KK-reduction]] on a circle, nor are they part of [[type IIA supergravity]]. These fluxes are instead part of [[massive type IIA supergravity]] whose relation to [[D=11 supergravity]]/[[M-theory]] remains less understood, see the references [here](massive+type+IIA+string+theory#ReferencesLiftToMTheory).

\end{example} 




\linebreak


### Solution space of the flux equations
 {#SolutionSpaceOfHigherMaxwellEquations}

**The phase space.** Abstractly, the *phase space* of a any [[field theory]] is nothing but the space of all those [[field histories]] that satisfy the given [[equations of motion]] (the "[[on-shell]]" field histories). Phrased this way, this is sometimes called the 
*[[covariant phase space]]*, to emphasize that no choice of [[foliation]] of spacetime by [[Cauchy surfaces]] has been or needs to be made.

\[\label{CanonicalAndCovariantPhaseSpace}\]
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

**Solution space of on-shell flux densities.** At this point in the discussion, the full gauge field content is not yet determined -- this will only be implied by a choice of flux quantization [below](#FluxQuantizationLaws) -- so far we are only considering the [[flux densities]] of the would-be gauge fields. To remember this, we shall call the space of flux densities solving their equations of motion (Def. \ref{HigherMaxwellEquations}) the *solution space*; and we are after its incarnation as a *canonical solution space* of initial value data on a Cauchy surface. But this goes a long way, since the higher Maxwell-type equations of motion constrain exclusively the flux densities: Once the flux-quantization the canonical phase will simply consist of all flux-quantized [[gauge potentials]] compatible with the flux densities in the canonical solution space.

\begin{proposition}\label{SolutionSpaceViaGaussLaw}
**([SS23-FQ](#SS23-FQ))**
  On a [[globally hyperbolic spacetime]] $X^D \,\simeq\, \mathbb{R}^{0,1} \times X^d$, the solution space to given [higher Maxwell-equations](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) of motion (Def. \ref{HigherMaxwellEquations}) is [[isomorphism|isomorphic]] to the solution of (just) the duality-symmetric [[Bianchi identities]] (eq:EqHigherMaxwellEquations) restricted ([[pullback of differential forms|pulled back]] to) to any [[Cauchy surface]] $\iota \,:\, X^d \hookrightarrow X^D$, there to be called the higher *[[Gauß law]]*:

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
**(Solution- and phase-space of ordinary electromagnetism)**
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

Indeed, the actual [[phase space]] of electromagnetism, after introducing a [[gauge potential]], is well-known (see [there](electromagnetism#ReferencesPhaseSpaceAndPoissonBrackets)) to have as

* [[canonical coordinate]] the [[gauge potential]] $A$,

* [[canonical momentum]] the electric flux density $E$.

Thereby $B \,\equiv\, curv\big(\widehat{A}\big)$ is indeed independent from $E$ (and satisfies its Gauß law definitionally, while the Gauß law on $E$ is a phase space [[constrained mechanics|constraint]]).

Notice how, thereby, this traditional split of [[initial value data]] into [[canonical coordinates]] and [[canonical momenta]] (whose definition requires assumption and [[variational calculus|variation]] of a [[Lagrangian density]]) is preempted here, under Prop. \ref{SolutionSpaceViaGaussLaw}, already by the pregeometric/duality-symmetric formulation of Maxwell's equations (in Ex. \ref{MotionOfElectromagneticField}), in the sense that the spacetime archetypes of the canonical coordinates and momenta   on a Cauchy surface (the former seen under the differential) are just the ordinary flux density $F_2$ (since $B = \iota^\ast F_2$) and its "duality partner" $G_2$ (since $E = \iota^\ast G_2$).
\end{example}


\begin{remark}\label{GravityDecouplesOnCanonicalPhaseSpace}
**(Gravity "decouples" on canonical phase space)**
\linebreak
The inverse isomorphism (eq:GaussLawFromBianchiIdentities) is given by time evolution of initial value data. Notice that the [[pseudo-Riemannian metric]] on $X^D$ -- the [[background field]] of [[gravity]] -- enters *only* in determining the nature of this isomorphism $\iota^\ast$ (the time evolution away from the Cauchy surface), but does not affect the nature of the initial value data (of the canonical phase space) as such.
\end{remark}

It is this "decoupling" *on the canonical phase space* of the gravity/metric effects from the phase space [[Gauß law]] constraint which allows to gain plenty of insight into brane configurations from purely cohomological analysis of fluxes on Cauchy surfaces, disregarding the full solution of the coupled (super-)gravity equations of motion:


### Qualitative solutions: Brane intersections
 {#BraneIntersectionsImprintedOnFlux}

Prop. \ref{SolutionSpaceViaGaussLaw} implies that on [[globally hyperbolic spacetimes]] the structure of [[on-shell]] flux densities in [[supergravity]] may be analyzed already by solving the (non-linear) [[Gauss law]] (eq:GaussLawFromBianchiIdentities) for duality-symmetric fluxes on any [[Cauchy surface]] and ignoring the coupling to [[gravity]] there (assuming only that there exists at least one gravitational field configuration which solves its [[Einstein equations]] with source terms of this form). Since the same Gauss law also governs the admissible flux quantization laws [below](#FluxQuantizationLaws) we showcase a couple of qualitative solutions to highlight just how much non-trivial (brane-)physics is encoded in these equations.

\begin{example}\label{D6CreationAndHananyWittenEffect}
**([[D6-D8 brane bound state|D6/D8-intersections]] and the [[Hanany-Witten effect]])**
A popular conjecture by [Hanany & Witten 1997](#Hanany-Witten+effect#HananyWitten97) states that the expected $\mathrm{D}_{\!p}$-branes stretching between $\mathrm{NS}_5$ and  $\mathrm{D}_{p+2}$ (cf. [above](#HigherFluxAndItsBranes)) are "created" as the $\mathrm{D}_{\!p+2}$-branes are "dragged over" the $\mathrm{NS}_5$, intuitively like a pole will cause a spike in a rubber sheet that is pulled over its tip. It was suggested by [Marolf 2001 (§2)](Hanany-Witten+effect#Marolf01) that this *[[Hanany-Witten effect]]* should be understandable entirely from analysis of the flux Bianchi identities (eq:GaussLawFromBianchiIdentities). 

For the case of [[D6-D8 brane bound states|NS5/D6/D8-brane intersections]] &lbrack;e.g. [Hanany & Zaffaroni 1998 (§2.4)](Hanany-Witten+effect#HananyZaffaroni98); [Bergshoeff, Lozano & Ortin 1998 (p. 60)](Hanany-Witten+effect#BergshoeffLozanoOrtin98) this may be seen as follows (the other cases work analogously):

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
**([[M2/M5-brane bound state|M2$\perp$M5-brane intersections]] on "[[M-strings]]")**
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

each reflected by unit 4-flux through their surrounding [[4-spheres]]:

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
    \,,
  \end{array}
\]

where the wedge product of the two translated $S^4$-volume forms acts as an effective "[[electric current|electric potential]]" source term.

For the purpose of illustration we consider a qualitative sketch of  the 2-dimensional analog of this situation, where the 4-forms are replaced by 2-forms:

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

Notice how in these examples we *chose* integral values for the total source brane fluxes. Next we discuss how such *flux quantization* is systematically enforced in the higher gauge theory.



## Flux/Charge quantization laws
 {#FluxQuantizationLaws}

With the solution space (Prop. \ref{SolutionSpaceViaGaussLaw}) of higher Maxwell-type equations of motion (Def. \ref{HigherMaxwellEquations}) in hand, the question of flux quantization is to further constrain the [[flux densities]] such that the total fluxes and their total source charges take values in some discrete space.

The technical issue to be resolved here is that:

* this is a *global condition* on the flux densities: The local flux densities may take any value (compatible with the equations of motion) and yet the total accumulation of all these local contributions needs to be constrained;

* the evident idea of constraining the ordinary [[integration of differential forms|integrals]] of the [[flux densities]] (their "[[periods]]") makes sense only for [[closed differential forms]] and hence does not work for non-linear Bianchi identities (such as those of the [[supergravity C-field|C-field]], Ex. \ref{MotionOfSupergravityCField}, and the B&RR-field, Ex. \ref{MotionOfCoupledBRRFields}).

To resolve this, one may first observe that:

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
(2.)  Also ([[homotopy types]] (eq:HomeoToHomotopyType) of) [[topological spaces]] $\mathcal{A}$ (under mild conditions) have a characteristic $L_\infty$-algebra: Their $\mathbb{R}$-rational  **[[Whitehead L-infinity algebra|Whitehead bracket $L_\infty$-algebra]]**.
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


### Total flux as Non-abelian de Rham cohomology
 {#TotalFluxInNonabelianDeRhamCohomology}

We explain how higher [[Bianchi identities]] (eq:EqHigherMaxwellEquations) and their corresponding higher [[Gauss laws]] (eq:GaussLawFromBianchiIdentities) are equivalently the closure ([[flat L-infinity algebra valued differential form|flatness]]) condition on [[L-infinity algebra valued differential form|differential forms valued in]] a characteristic [[L-infinity algebra|$L_\infty$-algebra]] (Prop. \ref{SolutionsAsFlatForms} below), so that *total flux* is a class in $\mathfrak{a}$-valued [[nonabelian de Rham cohomology]] (Def. \ref{NonabelianDeRhamCohomology} below).

\linebreak

The notion of $L_\infty$- or *strong homotopy Lie algebra*  is finally becoming more widely appreciated in physics, where they appear in various guises (see the references [there](L-infinity-algebra#ReferencesInPhysics)).
Here we are concerned with  $L_\infty$-algebras
which are (i) [[nilpotent L-infinity algebra|nilpotent]], (ii) [[connective chain complex|connective]] (iii) of [[finite type]], in their *joint* incarnation as higher [[flux density]] [[coefficients]] *and* as [[Whitehead L-infinity algebra|higher Whitehead brackets]] (all to be explained in a moment), which one might refer to as the 

**Flux Homotopy Lie algebra triality.**

\begin{imagefromfile}
    "file_name": "GeomPhys-FluxHomotopyLieTriality.jpg",
    "float": "right",
    "width": 380,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 10,
        "right": -10, 
        "left": 10
    }
\end{imagefromfile}

$\bullet$ With *[[rational homotopy theory|rational homotopy]]* we are referring here specifically the *[[fundamental theorem of dg-algebraic rational homotopy theory]]*, mainly due to Quillen, Sullivan and Bousfield & Gugenheim, as reviewed in [FSS23-Char, §5](#FSS23), 

$\bullet$ by the *[[D'Auria-Fre formulation of supergravity|FDA method in supregravity]]* we are referring, with some hindsight, to the observations of [van Nieuwenhuizen 1983](D'Auria-Fre+formulation+of+supergravity#Nieuwenhuizen82); [D
Auria & Fré 1982](D'Auria-Fre+formulation+of+supergravity#DAuriaFre82); [Castellani, D'Auria & Fré](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre), as explained in [FSS13](geometry+of+physics+--+fundamental+super+p-branes#FSS13), [FSS18](geometry+of+physics+--+fundamental+super+p-branes#FSS16b),[HSS19](geometry+of+physics+--+fundamental+super+p-branes#HSS19), reviewed in [FSS19-$\mathbb{Q}$Struc](#FSS19HigherStruc).

$\bullet$ The *[[Chern-Dold character|nonabelian character]]* is the generalization of the [[Chern-Dold character]] map from [[topological K-theory]] and [[Whitehead-generalized cohomology]] to generalized [[non-abelian cohomology]], constructed in [FSS23-Char](#FSS23).

In particular, this means that $L_\infty$-algebras as used here are *not* directly to be understood as generalizations of the gauge Lie algebras familiar from Yang-Mills theory, which are coefficients of the gauge potentials, but instead as the coefficients of their flux densities (cf. Rem. \ref{RoleOfLInfinityAlgebras}).

\linebreak

**$L_\infty$-Algebras.** Since we are assuming [[L-infinity algebras|$L_\infty$-algebras]] to be connective and of finite type (meaning that they are degreewise finite-dimensional and concentrated in non-negative degrees) we may *define* them through their Chevalley-Eilenberg (CE) algebras in the following manner, which is not only convenient for dealing with the otherwise intricate sign rules, but also essential to their alternative perspectives in the above triality:

$\;\;$**Chevalley-Eilenberg algebras of Lie algebras.**
Namely, for $\mathfrak{g}$ a finite-dimensional Lie algebra (our ground field is the real numbers, throughout) with Lie bracket a skew-symmetric linear map $[-,-] \,:\, \mathfrak{g} \otimes \mathfrak{g} \to \mathfrak{g}$, its linear dual vector space $\mathfrak{g}^\ast$ is equipped with the dual bracket $[-,-]^\ast \,:\,\mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast$ which extends uniquely to a degree=1 [[derivation]] on the graded [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g} \,:=\, \underset{n \in \mathbb{N}}{\bigoplus}
\,\underbrace{\mathfrak{g}^\ast \wedge \cdots \wedge \mathfrak{g}^\ast}_{n\;factors}$:

\[\label{LieAlgebrasAsDGCAlgebras}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-LieAlgebraUnderCE.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

One readily checks that this derivation squares to zero iff the bracket satisfies its [[Jacobi identity]](!):
$$
  \text{
    Jacobi identity for
  }
  \;
  [-,-]
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  \mathrm{d}_{{}_{[-,-]}}
  \circ 
  \mathrm{d}_{{}_{[-,-]}}
  \;=\;
   0
  \,.
$$
The resulting [[dgc-algebra|differential graded-commutative (dgc) algebra]] $(\wedge^\bullet \mathfrak{g}^\ast, \mathrm{d}_{[-,-]})$  is known as the *[[Chevalley-Eilenberg algebra|Chevalley-Eilenberg complex]]* $\mathrm{CE}(\mathfrak{g})$ whose cochain cohomology computes the [[Lie algebra cohomology]] of $\mathfrak{g}$ (with trivial coefficients) --- but the key point at the moment is that its construction is a *[[fully faithful functor|fully faithful]]* [[full subcategory|embedding]] the [[category]] of [[finite-dimensional vector space|finite-dimensional]] [[Lie algebras]] into the [[opposite category|opposite]] of that of [[dgc-algebras]].


$\;\;$**$L_\infty$-algebras of finite type.**
With ordinary Lie algebras viewed as special dgc-algebras this way, it is *immediate* to generalize them to the case where  $\mathfrak{g}$ may be a [[graded vector space]] of degreewise finite dimension ("of [[finite type]]"): Namely, writing
$$
  (\mathfrak{g}^\vee)_n
  \;\coloneqq\;
  (\mathfrak{g}_n)^\ast,
  \;\;\;\;\;\;\;\;\;\;\;\;
  \wedge^\bullet
  \mathfrak{g}^\vee
  \;\coloneqq\;
  \mathrm{Sym}(\mathfrak{g}^\vee[1])
$$
we can use *verbatim* the same construction:

A degree=1 derivation on $\wedge^\bullet\mathfrak{g}^\vee$ is determined by its restriction to $\wedge^1 \mathfrak{g}^\vee$, where it is a sum of co-[[arity|$n$-ary]] [[linear maps]], whose [[linear dual map|linear duals]] are identified as [[arity|$n$-ary]] degree=(-1) brackets on $\mathfrak{g}[1]$:

\begin{imagefromfile}
    "file_name": "GeomPhys-LInfinityUnderCE.jpg",
    "width": 880,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}
\[\label{FinTypeLInfinityAlgebrasAsDGCAlgebras}\]

Here the simple condition that $\mathrm{d}_{{}_{[\cdots]}}$ be a differential implies a tower of conditions on these brackets, generalizing the Jacobi identity on an ordinary 
Lie algebra and known as the conditions that make $\big( \mathfrak{g}, [-], [-,-], [-,-,-], \cdots \big)$ an [[L-infinity algebra|$L_\infty$-algebra]]:
$$
  \array{
    \text{higher Jacobi identity for}
    \\
    [-], 
    [-,-],
    [-,-,-],
    \cdots
  }
  \;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;
  \mathrm{d}_{{}_{[\cdots]}}
  \circ
  \mathrm{d}_{{}_{[\cdots]}}
  \;=\;
  0
  \,.
$$

In other words, we may identify $L_\infty$-algebras of finite type as the [[formal dual]] to [[dgc-algebras]] whose [[underlying]] [[graded-commutative algebra]] is [[symmetric algebra|free]] on a [[graded vector space]].

Some examples:

\begin{imagefromfile}
    "file_name": "GeomPhys-ExamplesOfFinTypeLInfinity.jpg",
    "width": 850,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


$\;\;$**Flat $L_\infty$-algebra valued differential forms** now  have an immediate definition from
this perspective: They are the [[dg-algebra]] [[homomorphism]] from  their CE-algebras into [[de Rham algebras]] (aka "[[Maurer-Cartan elements]]"):

\[
  \label{FlatLInfinityAlgebraValuedDifferentialForms}
  \left.
  \begin{array}{l}
    \mathfrak{a}
    \in
    L_\infty Alg^{ftp}
    \\
    X \in SmthMfd
  \end{array}
  \right\}
  \;\;\;\;\;\;\; 
  \vdash
  \;\;\;\;\;\;\;
  \Omega^1_{dR}(X;\mathfrak{a})_{clsd}
  \;\coloneqq\;
  Hom_{dgAlg}\big(
    CE(\mathfrak{a})
    ,\,
    \Omega^\bullet_{dR}(X)
  \big)
  \,.
\]

Namely, a graded algebra homomorphism from a [[Chevalley-Eilenberg algebra|CE-algebra]] sends the algebra generators $\vec b$ to differential forms $\vec B$, and its respect for the differentials imposes on these differential forms exactly the closure/flatness condition:

\begin{imagefromfile}
    "file_name": "GeomPhys-MCConditionAsDGAlgHomomorphy.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 10,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Some examples:


\begin{imagefromfile}
    "file_name": "GeomPhys-ExamplesOfFlatLInfinityValuedForms.jpg",
    "width": 820,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

$\;\;$**Flux densities satisfying Bianchi/Gauss laws are flat $L_\infty$-algebra-valued differential forms.**
Remarkably, it follows that polynomials $\vec P$ defining [[Bianchi identities]] (eq:EqHigherMaxwellEquations) and [[Gauss laws]] (eq:GaussLawFromBianchiIdentities) are equivalently structure constants of $L_\infty$-algebras 
$\mathfrak{a}$, such that the Bianchi/Gauss law is the closure/flatness condition on $\mathfrak{a}$-valued forms:

\begin{imagefromfile}
    "file_name": "GeomPhys-CharacteristicLieOfGaussLaw-240129.jpg",
    "width": 930,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

With Prop. \ref{SolutionSpaceViaGaussLaw} this means:

\begin{proposition}\label{SolutionsAsFlatForms}
Given a higher gauge theory of Maxwell-type (Def. \ref{HigherMaxwellEquations}) with [[Bianchi identities]] given by graded-symmetric [[polynomials]] $\vec P$ (eq:EqHigherMaxwellEquations) its space of [[flux densities]] solving the higher Maxwell equations is 
identified with the space of closed differential forms with coefficients in the $L_\infty$-algebra $\mathfrak{a}$ on $I$ $(\vec deg-1)$-graded generators with structure constants $\vec P$:

\begin{imagefromfile}
    "file_name": "GeomPhys-GaussLawAsFlatnessCondition-240129.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{proposition}

\begin{example}\label{SolutionSpaceOfElectromagnetism}
 The characteristic $L_\infty$-algebra of ordinary vacuum electromagnetism is the [[direct sum]] $b \mathfrak{u}(1) \oplus b \mathfrak{u}(1)$ of two copies of the [[line Lie 2-algebra]], which by the previous example and Prop. \ref{SolutionsAsFlatForms} corresponds to:

$$
  SolSpace_{EM}(X^3)
  \;\simeq\;
  \Omega^1_{dR}\big(
    X^3
    ;\,
    b\mathfrak{u}(1)
    \times
    b\mathfrak{u}(1)
  \big)_{clsd}
  \;\simeq\;
  \Omega^2_{dR}(X^3)
  \times
  \Omega^2_{dR}(X^3)
  \,.
$$

An element here is a pair $(B,E)$, where 

1. the magnetic flux density is the curvature $B = \mathrm{curv}\big(\widehat A\big)$ of the gauge potential which plays the role of the "[[canonical coordinate]]" on the field space;

1. the electric flux density $E$ serves as the [[canonical momentum]].
  
\end{example}

$\;\;$**Total flux in non-abelian de Rham cohomology.** While, with Prop. \ref{SolutionsAsFlatForms}, the [[Gauss law]] of the given [[higher gauge theory]] of Maxwell-type constrains the [[flux densities]] on any [[Cauchy surface]] $X^d \hookrightarrow X^D$ to constitute a [[flat L-infinity-algebra valued differential form|flat $L_\infty$-algebra valued differential form]], the actual value of these differential forms depends on the [[Cauchy surface]], which is an arbirary choice. 

We should, therefore, regard as the *total flux* that aspect of the [[flux densities]] which is [[invariant]] under choice of [[Cauchy surfaces]].

But since the [[Gauss law]] is (by Prop. \ref{SolutionSpaceViaGaussLaw}) nothing but the [[pullback of differential forms|restriction]] to the Cauchy surface of the [[Bianchi identities]] (on the duality-symmetric flux densities of Def. \ref{HigherMaxwellEquations}), the argument of Prop. \ref{SolutionsAsFlatForms} shows that this invariant aspect is the [[equivalence classes]] of flux densities under *[[concordance]]*:

\[\label{ConcordanceOfFlatDifferentialForms}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-CauchyEvolutionOfGaussLawData-240204.jpg",
    "width": 760,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\begin{definition}\label{NonabelianDeRhamCohomology}
(**[[non-abelian de Rham cohomology]]** &lbrack;[FSS23-Char, Def. 6.3](#FSS23)&rbrack;)
\linebreak
Given an [[L-infinity algebra|$L_\infty$-algebra $\mathfrak{a}$]] and a [[smooth manifold]] $X^d$, we say that a pair of [[flat L-infinity algebra valued differential forms|closed $\mathfrak{a}$-valued differential forms]] $\vec B_0, \vec B_1 \,\in\, \Omega^1_{dR}\big(X^d;\mathfrak{a}\big)_{clsd}$ (eq:FlatLInfinityAlgebraValuedDifferentialForms) are *cohomologous* iff they are [[concordance|concordant]]: iff there exists a [[flat L-infinity algebra valued differential forms|closed $\mathfrak{a}$-valued differential form]] $\vec F$ on the [[cylinder]] over $X^d$ whose restriction ([[pullback of differential forms|pullback]]) to the $k$th boundary component equals $\vec B_k$:

$$
  \vec B_0
  \;\sim\;
  \vec B_1
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \exists
  \;\;
  \vec F
  \,\in\,
  \Omega^1_{dR}\big(
    X^d \times [0,1]
    ;\,
    \mathfrak{a}
  \big)_{clsd}
  \;\;\;
  \text{with}
  \;\;\;
  \left\{
  \begin{array}{l}
    \vec B_1 \,=\, \iota_1^\ast \vec F
    \\
    \vec B_0 \,=\, \iota_0^\ast \vec F
  \end{array}
  \right.
  \,.
$$

The [[quotient set]] by this [[equivalence relation]] is $\mathfrak{a}$-valued *[[nonabelian de Rham cohomology]]* of $X^d$:
$$
  H^1_{dR}\big(
    X^d;\mathfrak{a}
  \big)
  \;\coloneqq\;
  \Omega^1_{dR}\big(
    X^d
    ;\,
    \mathfrak{a}
  \big)_{clsd}
  \Big/
  \!
  \sim
  \,.
$$
\end{definition}

\begin{remark}
**(flux conservation)**
\linebreak
\begin{imagefromfile}
    "file_name": "GeomPhys-TotalFluxInNonabDeRhamCohom-240129.jpg",
    "float": "right",
    "width": 320,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 20, 
        "left": 20
    }
\end{imagefromfile}

Regarding the image of flux densities in non-abelian de Rham cohomology as expressing their *total flux*
it follows immediately that:

$\;\;\;\;\;$*Total flux is conserved under time evolution.* 

\end{remark}

\linebreak

\begin{remark}
**(nonabelian de Rham cohomology as dg-homotopy classes)**
\linebreak
For comparison to the flux quantization rules discussed [below](#FluxQuantizationLawsAsNonabelianCohomology)
it is useful to understand this equivalently &lbrack;[FSS23-Char, Thm. 6.5](#FSS23)&rbrack; as the set of dg-homotopy classes of the corresponding dgc-homomorphisms:

\begin{imagefromfile}
    "file_name": "GeomPhys-NonabDeRhamAsHomotopyClasses-240129b.jpg",
    "width": 680,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


\end{remark}

\linebreak

\begin{example}
([FSS23-Char, Prop. 6.4](#FSS23))
\linebreak
  In the case of ordinary electromagnetism and abelian higher gauge fields, hence for $\mathfrak{a} = b^n \mathfrak{u}(1)$ the [[line Lie n-algebra|line Lie $(n+1)$-algebra]], Def. \ref{NonabelianDeRhamCohomology} reduces to the ordinary notions:

1. $\Omega^1_{dR}\big(X^d; b^n\mathbb{R}\big)_{clsd} \,\simeq\, \Omega^{n+1}(X^d)_{clsd}$ are ordinary [[closed differential forms]];

1. [[concordance]] between these is the [[coboundary]] relation in the ordinary [[de Rham complex]];

1. $H^1_{dR}\big(X^d;\, b^n \mathbb{R}\big) \,\simeq\, H^{n+1}_{dR}\big(X^d\big)$ is ordinary [[de Rham cohomology]].

and since the latter also gives the [[periods]] of closed differential forms, this recovers indeed the usual notion of total (integrated) flux.

Concretely, with 

$$
  F_2
  \;\coloneqq\;
  q
  \mathrm{dvol}_{S^2}
  \;\in\;
  \Omega^2_{dR}\big(S^2\big)
  \;\overset{p^\ast_{S^2}}{\longrightarrow}\;
  \Omega^2_{dR}\big(\mathbb{R}^3 \setminus \{0\}\big)
  \;\simeq\;
  \Omega^1_{dR}\big(\mathbb{R}^3 \setminus \{0\}  
    ;\,
    b\mathbb{R}
  \big)
$$

the flux density around a [[magnetic monopole]] of charge $q$ (eq:MagneticMonopoleSchematics), the total flux is 

$$
  \array{
    H^2_{dR}\big(
     \mathbb{R}^3 \setminus \{0\}
    \big)
    &\simeq&
    H^2_{dR}\big(
     S^2
    \big)
    &\simeq&
    \mathbb{R}
    \\
    F_2
    &\mapsto&
    \big[ F_2\,  \big]
    &\mapsto&
    \int_{S^2} F_2
    \mathrlap{
      = q
      \,.
    }
  }
$$

\end{example}

\linebreak

With [[on-shell]] flux densities thus understood as cocycles in [[nonabelian de Rham cohomology]], we find their flux quantization laws among the corresponding [[torsion subgroup|torsion]]-ful [[nonabelian cohomology]]-theories:

\linebreak

### Flux quantization laws as Nonabelian cohomology
 {#FluxQuantizationLawsAsNonabelianCohomology}

We explain how the $\mathfrak{a}$-valued [[nonabelian de Rham cohomology]] of the previous subsection receives *character maps* from generalized [[nonabelian cohomology]] theories whose [[classifying spaces]] $\mathcal{A}$ have compatible rational [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] $\mathfrak{l}\mathcal{A} \simeq \mathfrak{a}$ --- whence $\mathcal{A}$ encodes a flux quantization law for Bianchi identities characterized by $\mathfrak{a}$, and lifting through the $\mathcal{A}$-character map corresponds to choices of *charge quanta* which source given total flux.

\linebreak

{#ClassifyingSpacesForGeneralizedCohomology}
**Classifying spaces for generalized cohomology.**
It is a classical fact of [[algebraic topology]] -- which may have remained somewhat underappreciated in [[mathematical physics]] -- that reasonable [[generalized cohomology theory|generalized]] [[cohomology theories]] have *classifying spaces* $\mathcal{A}$, in that the sets of cohomology classes assigned to a given domain space (which we take to be a [[smooth manifold]] $X$) are in [[natural bijection]] with the [[homotopy classes]] $\pi_0 Maps\big(-, \mathcal{A}\big)$ of [[continuous maps]] from $X$ into $\mathcal{A}$ (it is only the [[homotopy type]] (eq:HomeoToHomotopyType) of $\mathcal{A}$ that matters here).


The archetypical examples are *[[Eilenberg-MacLane spaces]]* like $K(\mathbb{Z},n)$ which classify [[ordinary cohomology]] such as [[integral cohomology]], in any degree $n$. 
As $n$ ranges, these EM-spaces happen to be [[loop spaces]] of each other, $K(\mathbb{Z},n) \simeq \Omega K(\mathbb{Z}, n+1)$.

\begin{imagefromfile}
    "file_name": "GeomPhys-ClassifyingSpacesForCohomology.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

{#NonabelianCohomology} Generalizing from this classical example, one considers [[Whitehead-generalized cohomology theories]] which [[Brown representability theorem|are classified by]] any sequences of [[pointed topological spaces]] $\{E_n\}_{n \in \mathbb{N}}$ equipped with [[weak homotopy equivalences]] $E_n \simeq \Omega E_{n+1}$, called a *[[spectrum]] of spaces*. 

This implies that each $E_n$ is an [[infinite-loop space]], which makes them be "[[abelian infinity-group|abelian $\infty$-groups]]" reflecting the fact that the homotopy classes of maps into these spaces indeed have the [[structure]] of *[[abelian groups]]*.

The maybe most familiar example of such *abelian* generalized cohomology is [[topological K-theory]], whose classifying space [[KU|$KU_0$]] may be identified with the space of [[Fredholm operators]] on an infinite-dimensional [[separable]] [[complex vector space|complex]] [[Hilbert space]].

While [[Whitehead-generalized cohomology theory]] has received so much attention that it is now widely understood as the default or even the exclusive meaning of "generalized cohomology", historically long preceding it is the [[nonabelian cohomology]] of [[Chern-Weil theory]], classified by the original [[classifying spaces]] $B G$ of [[compact Lie groups]] $G$. 

Unless $G$ happens to be [[abelian group|abelian]] itself, this [[nonabelian cohomology]] does not assign abelian [[cohomology groups]], nor even any groups at all, but just *[[pointed set|pointed]] cohomology sets*. Nevertheless, as the historical name "nonabelian cohomology" clearly indicates, these systems of cohomology sets may usefully be regarded as constituting a kind of cohomology theory, too.

In this vein one may observe &lbrack;[FSS23-Char, §2](#FSS23)&rbrack; that (the [[homotopy type]] of) *every* connected space $\mathcal{A}$ is equivalently the [[classifying space]] of an [[infinity-group]] $\Omega \mathcal{A}$, namely of its own [[loop space]] regarded as an [[A-infinity space|$A_\infty$-space]] under concatenation of loops), so that homotopy classes of maps into *any* connected space are examples of an evident generalization of Chern-Weil-style [[nonabelian cohomology]].

A fundamental and historical example of such "truly-generalized" [[nonabelian cohomology]] is *[[Cohomotopy|CoHomotopy]]*,
whose classifying spaces are the ([[homotopy type|homotopy types]]) of [[spheres]].

Notice that "generalized nonabelian cohomology" is really "not necessarily abelian": It subsumes all the other cases: For $E_\bullet$ a [[spectrum]] we have

$$
  E^n(X) \,\simeq\, H^1\big(X;\, \Omega E_n\big)
  \,.
$$

\linebreak

**Character maps on generalized cohomology.**
Moreover, it is classical that, over smooth manifolds, reasonable cohomology theories have their non-[[torsion subgroup|torsion]] content reflected in [[de Rham cohomology]] via *character maps*:

* on [[integral cohomology]] this is *[[de Rham theorem]]*, 

* on ordinary [[non-abelian cohomology]] this is the *[[Chern-Weil homomorphism]]*,

* on [[topological K-theory]] this is the *[[Chern character]]*,

* on any [[Whitehead-generalized cohomology]] this is the *[[Chern-Dold character]]*

\[\label{ExamplesOfCharacterMaps}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-CharacterMaps.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The nonabelian character in the generality of generalized non-abelian cohomology, such as [[Cohomotopy|CoHomotopy]], is due to &lbrack;[FSS23-Char, Def. IV.2](#FSS23)&rbrack;, constructed via the [[fundamental theorem of dg-algebraic rational homotopy theory]]. We next survey how this works. 

The key point is that [[rational homotopy theory]] characterizes the non-[[torsion subgroup|torsion]] content of (the [[homotopy type]] of) a (classifying) space by an [[L-infinity algebra|$L_\infty$-algebra]]-approximation $\mathfrak{l}\mathcal{A}$ to its [[loop space]] [[infinity-group|$\infty$-group]] $\Omega \mathcal{A}$.


\begin{proposition}\label{SullivanTheorem}
**(Quillen-Sullivan-Whitehead $L_\infty$-algebra** &lbrack;cf. [FSS23-Char, Prop. 4.23, 5.6 & 5.13](#FSS23)&rbrack;)
\linebreak

For a [[topological space]] $\mathcal{A}$ which is

1. [[simply connected topological space|simply connected]]: $\pi_0(\mathcal{A}) = \ast$ and $\pi_1(\mathcal{A}) = 1$;

1. of [[rational cohomology|rational]] [[finite type]]: $\mathrm{dim}_{\mathbb{Q}}\big(H^n(\mathcal{A}; \mathbb{Q})\big) \lt \infty$;

there is a polynomial dgc-algebra over $\mathbb{R}$, unique up to dga-[[isomorphism]], whose

*  generators are the $\mathbb{R}$-rational homotopy groups of $\mathcal{A}$,

   $$
     \mathrm{CE}(\mathfrak{l}\mathcal{A})
     \;=\;
     \Big(
     \wedge^\bullet
     \big(
       \,{
         \color{darkblue}
         \pi_\bullet
         \big(
           \Omega \mathcal{A}
         \big)
         \!\otimes_{{}_\mathbb{Z}}\!
         \mathbb{R}
       }\,
     \big)^\vee
     ,\,
     \mathrm{d}_{CE(\mathfrak{l}\mathcal{A})}
     \Big)
   $$

* [[cochain cohomology]] is the [[ordinary cohomology|ordinary]] [[real cohomology]] of $\mathcal{A}$.


  $$
    H^\bullet\big(
      \mathrm{CE}(\mathfrak{l}\mathcal{A})
    \big)
    =
    H^\bullet(\mathcal{A};\, \mathbb{R})
    \,.
  $$

\end{proposition}
This [[dgc-algebra]] is known as the [[minimal model|minimal]] **[[Sullivan model]]** of $\mathcal{A}$.
By (eq:FinTypeLInfinityAlgebrasAsDGCAlgebras) it is the [[Chevalley-Eilenberg algebra]] of an [[L-infinity algebra|$L_\infinity$-algebra]] which we denote by $\mathfrak{l}\mathcal{A}$ (essentially the "Quillen model"): The [[Whitehead bracket]] algebra structure on the $\mathbb{R}$-rational [[homotopy groups]] of the [[loop space]]

\[
 \label{WhiteheadLInfinityAlgebra}
  \mathfrak{l}\mathcal{A}
  \;=\;
  \color{darkblue}
  \pi_\bullet\big(
    \Omega \mathcal{A}
  \big) \otimes_{\mathbb{Z}} \mathbb{R}
  \,.
\]

(Think of "$\mathfrak{l}(-)$" as standing for "Lie" or for "loops".)

Some examples for how to use Prop. \ref{SullivanTheorem} to compute [[Sullivan models]] and hence $\mathbb{R}$-[[Whitehead L-infinity algebras|Whitehead $L_\infty$-algebras]] $\mathfrak{l}\mathcal{A}$ of spaces:

\begin{imagefromfile}
    "file_name": "GeomPhys-FirstExamplesOfSullivanModels.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 0,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\begin{imagefromfile}
    "file_name": "GeomPhys-FurtherExamplesOfSullivanModels.jpg",
    "width": 907,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": -3
    }
\end{imagefromfile}

Many of the [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebras]] of familar spaces do not have established names as [[L-infinity algebras|$L_\infty$-algebras]]. An interesting exception is the [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] of the [[4-sphere]], which happens to coincide with what in [[D=11 supergravity]]-theory is known (quite independently) as the  *gauge algebra of the C-field* &lbrack;[Cremmer, Julia, Lu & Pope 1998, (2.6)](#CremmerJuliaLuPope98); [Sati 2010, §4](#Sati10); [Sati & Voronov 2022, (13)](#SatiVoronov22)&rbrack; (see more references [there](D=11+N=1+supergravity#ReferencesCFieldGaugeAlgebra)):

\begin{imagefromfile}
    "file_name": "GeomPhys-CFieldGaugeAlgebraAsWhiteheadBracket.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\begin{remark} 
**(prefactors in Sullivan algebras)**
\linebreak
As stated so far, the ubiquituous prefactor $-\tfrac{1}{2}$ is pure convention, due to the freedom of rescaling generators by rational (or even real) numbers while retaining dga-isomorphy. However, this factor is fixed by requiring certain integrality properties of the generators, see [FSS21-HopfWZ, Prop. 4.6](#FSS21WZ). 

This becomes relevant when regarding the lift back from $\mathfrak{l}S^4$ to $\mathcal{A} \equiv S^4$ as a [[flux quantization]] law, because then it implies that the C-field flux densities $G_4$ and $G_7$ in the image of the normalized generators $\omega_4$ and $\omega_7$ satisfy expected integrality conditions &lbrack;[FSS21-HopfWZ, Thm. 4.8](#FSS21WZ)&rbrack;. We discuss this further [below](#CFieldFluxQuantizationIn10d).
\end{remark}

\linebreak


**Rational homotopy theory: Discrading torsion in nonabelian cohomology.**
From the perspective ([above](#ClassifyingSpacesForGeneralizedCohomology)) that any topological space $\mathcal{A}$ serves as the *classifying space* of a generalized [[nonabelian cohomology theory]],
the idea of [[rational homotopy theory]] (survey in [Hess 2006](rational+homotopy+theory#Hess06); [FSS23-Char, §4](#FSS23)) becomes that of extracting the non-[[torsion subgroup|torsion]] content of such a cohomology theory, which we will see is, over [[smooth manifolds]], that shadow of it that is reflected in the [[non-abelian de Rham cohomology]] (Def. \ref{NonabelianDeRhamCohomology}) of $\mathfrak{l}\mathcal{A}$-valued differential forms.

\begin{imagefromfile}
    "file_name": "GeomPhys-HomotopyToCohomology.jpg",
    "width": 660,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\begin{imagefromfile}
    "file_name": "GeomPhys-RationalizingHomotopyGroups-240204.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Hence to have a classifying space for the non-torsion part of $\mathcal{A}$-cohomology means to ask for:

\[\label{RationalizationOfASpace}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-RationalizationOfASpace.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

For example, the [[rationalization]] of an integral [[Eilenberg-MacLane space]] $B^n \mathbb{Z} \,\equiv\, K(\mathbb{Z},n)$ classifies [[ordinary cohomology|ordinary]] [[rational cohomology]], mapping to ordinary [[de Rham cohomology]]:

\begin{imagefromfile}
    "file_name": "GeomPhys-CharacterInOrdinaryCohomology.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

We may regard this as the archetype of a *character map* and ask for its generalization to any $\mathcal{A}$-cohomology theory.  The pivotal  observation of [FSS23-Char](#FSS23) is that for this purpose one may invoke the *[[fundamental theorem of dg-algebraic rational homotopy theory]]:

\linebreak

**The Fundamental Theorem of dg-Algebraic Rational Homotopy Theory** (review in [FSS23-Char, Prop. 5.6](#FSS23))
says that the [[homotopy theory]] of [[rational spaces]] ([[simply-connected topological space|simply-connected]] with [[finite-dimensional vector space|fin-dim]] [[rational cohomology]]) is all encoded by their  [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebras]] (eq:WhiteheadLInfinityAlgebra) over the [[rational numbers]].

In particular, for $X$ a [[CW-complex]], the [[homotopy classes]] of [[maps]] into the [[rationalization]] $L^{\mathbb{Q}}\mathcal{A}$ (eq:RationalizationOfASpace) of a space $\mathcal{A}$ is identified with dg-homotopy classes of  homomorphisms from the rational [[Sullivan model]] of $\mathcal{A}$ to the "[[PL de Rham complex|piecewise polynomial de Rham complex]]" of the topological space $X$:

\[\label{FundamentalTheoremOfRHT}\]
\begin{tikzcd}
  \mathrm{Map}\big(
    X
    ,\,
    L^{\mathbb{Q}} \mathcal{A}
  \big)_{/ \mathrm{homotopy}}
  \;\;
  \simeq
  \;\;
  \mathrm{Hom}_{\mathrm{dgAlg}}\Big(
    \mathrm{CE}\big(
      \mathfrak{l}^{\mathbb{Q}}
      \mathcal{A}
    \big)
    ,\,
    \Omega^\bullet_{\mathrm{PLdR}}(X)
  \Big)_{
    \!/\mathrm{concordance},
  }
\end{tikzcd}


Observing that the right-hand side looks close to the definition of [[nonabelian de Rham cohomology|$\mathfrak{l}\mathcal{A}$-valued de Rham cohomology]] (Def. \ref{NonabelianDeRhamCohomology}), in order to actually connect to such smooth differential forms one needs to extend the [[ground field]] scalars from the [[rational numbers]] to the [[real numbers]]:

\begin{imagefromfile}
    "file_name": "GeomPhys-RealRationalizationOfASpace.jpg",
    "float": "right",
    "width": 530,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

{#RationalizationOverTheReals} $\;\;$**Rational homotopy theory over the Reals.** &lbrack;[Bousfield & Gugenheim 1976](rational+homotopy+theory#BousfieldGugenheim76); reviewed in [FSS23-Char, Def. 5.7, Rem. 5.2, Prop. 5.8](#FSS23)&rbrack;
The construction (eq:RationalizationOfASpace) also works over $\mathbb{R}$ (but is then not a "[[localization of spaces|localization]]") to give the *$\mathbb{R}$-rationalization*.

With this "[[derived functor|derived]] [[extension of scalars]]" &lbrack;[FSS23-Char, Lem 5.3](#FSS23)&rbrack; and for $X$ a smooth manifold,  the fundamental theorem (eq:FundamentalTheoremOfRHT) does relate to smooth differential forms &lbrack;[FSS23-Char, Lem. 6.4](#FSS23)&rbrack; via a **[[non-abelian de Rham theorem]]** &lbrack;[FSS23-Char, Thm. 6.5](#FSS23)&rbrack;:

\[\label{NonabelianDeRhamTheorem}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-NonabelianDeRhamTheorem.jpg",
    "width": 860,
    "unit": "px",
    "margin": {
        "top": -15,
        "bottom": 5,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


**In abelian (ie. Whitehead-generalized) cohomology** theories both the rationalization step and the subsequent extension of scalars to $\mathbb{R}$  can be more easily described as forming the [[smash product]] of the [[coefficient]] [[spectrum]] with the rational [[Eilenberg-MacLane spectrum]] $H\mathbb{R}$ &lbrack;[FSS23-Char, Ex. 5.7](#FSS23)&rbrack;. 
This is how the *[[Chern-Dold character]]* map over $\mathbb{R}$ is tacitly used  in all the literature on abelian ([[Whitehead-generalized cohomology|Whitehead-generalized]]) [[differential cohomology]] theory (e.g. [Bunke & Nikolaus 2014, Def. 4.2](twisted+differential+cohomology#BunkeNikolaus14)):

\[\label{RealificationOfSpectra}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-RealRationalizationOfSpectra.jpg",
    "width": 530,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

The point of the non-abelian de Rham theorem (eq:NonabelianDeRhamTheorem) is to generalize the realifification  (eq:RealificationOfSpectra) of [[Whitehead-generalized cohomology]] to generalized [[non-abelian cohomology]], such as to [[Cohomotopy]]; and the key result that makes this work is the fundamental 
theorem of dg-algebraic homotopy theory (eq:FundamentalTheoremOfRHT). This, ultimately, is the "reason" why [[L-infinity algebra valued differential forms|$L_\infty$-valued differential 
forms]] relate fluxes to their flux-quantization laws.

\linebreak

**The general non-abelian character map** is now immediate &lbrack;[FSS23-Char, Def. IV.2](#FSS23)&rbrack;:
It is the [[cohomology operation]] induced by $\mathbb{R}$-[[rationalization]] of [[classifying spaces]], seen under the [[non-abelian de Rham theorem]] (eq:NonabelianDeRhamTheorem):

\[\label{NonabelianCharacterMap}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-NonabelianCharacterMap.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

All the classical abelian character maps (eq:ExamplesOfCharacterMaps) are special cases of this generalized nonabelian character &lbrack;[FSS23-Char, §7](#FSS23)&rbrack;, but now examples in generalized [[nonabelian cohomology]] are also included; for instance there is a character map on [[Cohomotopy]]-theory &lbrack;[FSS23-Char, Ex. 6.11](#FSS23)&rbrack;


**Flux quantization in generalized nonabelian cohomology.** With the generalized nonabelian character map (eq:NonabelianCharacterMap) in hand, we may finally state the general concept of flux quantization (to be further refined [below](#PhaseSpacesAsDifferentialNonabelianCohomology)):

Recalling (eq:ConcordanceOfFlatDifferentialForms) that the $\mathfrak{a}$-valued [[nonabelian de Rham cohomology]] of a [[Cauchy surface]] encodes the *total flux* of the [[higher gauge fields]] characterized by the [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$, it follows that for every choice of classifying space $\mathcal{A}$ with $\mathfrak{l}\mathcal{A} \,\simeq\, \mathfrak{a}$ the nonabelian character map (eq:NonabelianCharacterMap) may be understood as assigning to *discrete charges* embodied by $\mathcal{A}$-cohomology-classes the corresponding total flux (thereby losing torsion-information encoded in the charges but not in the fluxes):

\[\label{NonabelianCharacterMapChargesToFluxes}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-CharacterMapChargesToFluxes-240202.jpg",
    "width": 450,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Since the total charges in $H^1\big(X^d; \Omega \mathcal{A})\big)$ on the left form a discrete set, we may think of implementing flux quantization in $\mathcal{A}$-cohomology as *[[lifting]]* of total fluxes through the character map:

\begin{imagefromfile}
    "file_name": "GeomPhys-FirstIdeaOfFluxQuantization.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Notice that such a lift is not *just* a (quantization/discretization-)*condition* on the total fluxes, but also *[[extra structure]]*, namely a choice of [[torsion subgroup|torsion]]-component of the total charge reflected in total fluxes, as see in $\mathcal{A}$-cohomology:

\begin{imagefromfile}
    "file_name": "GeomPhys-CharacterKernelAndCokernel.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

However, in a [[higher gauge theory]] it is unnatural to have [[extra structure]] given by an [[equality]] of gauge equivalence classes, instead one should consider an explicit [[gauge transformation]] between actual fields. Doing so leads to emergence of the [[gauge potentials]] and of the higher [[phase space]] stack of the theory, in the [next subsection](#PhaseSpacesAsDifferentialNonabelianCohomology).

\begin{example}
  **(flux quantization laws for ordinary electromagnetism)**
  \linebreak

  By Ex. \ref{SolutionSpaceOfElectromagnetism} the characteristic $L_\infty$-algebra of vacuum electromagnetism is two copies of the [[line Lie 2-algebra]] $b \mathfrak{u}(1)$. This is the [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] of the [[classifying space]] $B \mathrm{U}(1) \,\simeq\, B^2 \mathbb{Z}$ and hence of its [[rationalization]] $B^2 \mathbb{Q}$.

Therefore -- among many further variants -- there are the following choices of flux quantization laws for electromagnetism:

| EM flux quantization law |  comment |
|--------------------------|----------|
| $\underset{mag}{\underbrace{B^2 \mathbb{Q}}} \,\times\, \underset{el}{\underbrace{B^2 \mathbb{Q}}}$ | this choice imposes *no* flux quantization (it does rule out [[irrational number|irrational]] total fluxes) and as such was the tacit choice since [Maxwell 1865](Maxwell's+equations#Maxwell1865) until [Dirac 1931](#Dirac31) |
| $\underset{mag}{\underbrace{B^2 \mathbb{Z}}} \,\times\, \underset{el}{\underbrace{B^2 \mathbb{Q}}}$ | this choice imposes integrality of magentic charge but no further condition on electric flux -- common choice since [Dirac 1931](#Dirac31), for instance in [Alvarez 1985b, p. 299](#Alvarez85b); [Freed 2000, Ex. 2.1.2](#Freed00) | 
| $\underset{mag}{\underbrace{B^2 \mathbb{Z}}} \,\times\, \underset{el}{\underbrace{B^2 \mathbb{Z}}}$ | this choice imposes integrality of both magentic and electric charges -- considered in [Freed, Moore & Segal 2007a](#FreedMooreSegal07a), [2007b](#FreedMooreSegal07b); [Becker, Benini, Schenkel & Szabo 2015, Rem. 2.3](#BeckerBeniniSchenkelSzabo15); [Lazaroiu & Shahbazi 2022](#LazaroiuShahbazi22); [Lazaroiu & Shahbazi 2023, §2](#LazaroiuShahbazi23) | 
| $\underset{mag}{\underbrace{B^2 \mathbb{Z}}} \,\rtimes\, \underset{el}{\underbrace{B\big( K \ltimes B\mathbb{Z} \big) }}$ | for a [[finite group]] $K \to Aut(\mathbb{Z})$ -- this choice induces non-commutativity between EL/EL- and EL/M-fluxes, an example of a "non-evident" flux quantization condition considered in [SS23-FQ](#SS23-FQ) |



\end{example}

\linebreak


### Phase spaces as Differential nonabelian cohomology
 {#PhaseSpacesAsDifferentialNonabelianCohomology}


With higher Maxwell-type equations of flux given ([above](#EquationsOfMotionOfFlux)) and with a compatible flux/charge quantization law $\mathcal{A}$ chosen ([above](#TotalFluxInNonabelianDeRhamCohomology)), we explain here how the full [[on-shell]] [[field (physics)|field]] content of the [[higher gauge theory]] (including the [[gauge potentials]]) and hence its [[phase space]] (eq:CanonicalAndCovariantPhaseSpace) appears as the corresponding "[[moduli space]]" of [[nonabelian differential cohomology]] $\widehat{A}$ of any [[Cauchy surface]]. 

In fact, such a [[phase space]] is not just a [[smooth manifold]], but is a *[[smooth infinity-groupoid|smooth $\infty$-groupoid]]* (aka *[[smooth infinity-stack|smooth $\infty$-stack]]*, hence a higher *[[moduli stack]]*) whose [[higher morphisms]] represent the [[higher gauge transformations]] between the field configurations; and so we briefly review some required concepts from [[(infinity,1)-topos theory|higher topos theory]]. 

However, the "topological observables" on the higher gauge theory (those that detect topological charge structure but not the local [[differential geometry]] of field configurations) depend only on the "[[shape modality|shape]]" of the phase space stack, which by the properties of "[[cohesive (infinity,1)-topos|cohesive higher topos theory]]" turns out to coincide simply with the actual [[mapping space]] from the Cauchy surface into the classifyong space $\mathcal{A}$. 

Therefore the reader who is not to be bothered with [[(infinity,1)-topos theory|higher topos theory]] and is content with the "topological" implications of flux quantization may safely (dis-)regard this subsection as a black box which guarantees that once a classifying spaces $\mathcal{A}$ is chosen for flux quantization, it controls not only the set $H^1\big(X^d;\, \mathcal{A}\big) \,\equiv\, \pi_0 Map(X^d, \mathcal{A})$ of total charges of the theory, but also the full [[moduli space]] $Map(X^d, \mathcal{A})$ of local charges.

\linebreak

**Smooth sets of moduli of flux densities.**

The idea of *[[moduli stacks]]* is the evident refinement of that of *[[classifying spaces]]*: Given a certain kind of [[mathematical structure|structure]] (in physics typically: a certain kind of fields):

1. a *classifying space* is such that [[homotopy classes]] of ([[continuous map|continuous]]) [[maps]] to it from any $X$ correspond to [[equivalence classes]] of such structures on $X$,

1. a *moduli stack* is such that the individual ([[smooth map|smooth]]) maps to it from any $X$ correspond to the individual such structures on $X$,

   with ([[higher homotopy|higher]]) [[homotopies]] of these maps corresponding to the ([[higher gauge transformation|higher]]) [[gauge transformations]] between these structures.

In order to understand that and how such moduli stacks may exist at all, it is useful to take a perspective where *every* kind of space under consideration (such as spacetime itself) is *defined* (not as an underlying set of points with extra structure but) by the maps it receives from given *probes*.

We refer the reader to the section *[[geometry of physics -- smooth sets]]* or else to &lbrack;[Schreiber 2024](#Schreiber24), [Giotopoulos & Sati 2023](#GiotopoulosSati23)&rbrack; for more exposition and discssion of the following idea:

$\;$**Smooth sets.** For the present purpose of [[higher differential geometry]], the relevant probe spaces are "abstract coordinate charts", namely [[Cartesian spaces]] $\mathbb{R}^n$, and the idea is that any space $X$ which qualifies as a "[[smooth set]]" should be *defined* (not necessarily by an [[underlying]] [[set]] of points equipped with [[smooth structure]] but) by a system of sets of ways 

\[
  \label{PlotsByCartesianSpaces}
  \mathbb{R}^n 
    \;\mapsto\;
  Plots\big(
    \mathbb{R}^n
    ,\,
    X
  \big)
\]

of *plotting out* probe spaces $\mathbb{R}^n$ inside the would-be space $X$. Basic consistency requirements demand that this assignment should make a [[contravariant functor]] to [[Sets]] (a "[[presheaf]]")

$$
  Plots\big(
    -;
    X
  \big)
  \;\colon\;
  CartSp^{op} \longrightarrow Set
$$

from/on the [[category]] [[CartSp]] of [[Cartesian spaces]] $\mathbb{R}^n$ ($n \in \mathbb{R}$) with [[smooth functions]] between them. Similar considerations show that a *smooth map* $f \,\colon\, X \to Y$ between [[smooth sets]] defined this way (only) by their systems of plots should be just a compatible system of transformations of plots-of-$X$ to plots-of-$Y$, hence should be a [[natural transformation]] between such functors.

The further consistency requirement of *locality* of probes demands that such a smooth map $f \,\colon\, X \to Y$ should "count as" an [[invertible morphism|invertible]] [[isomorphism]] ([[diffeomorphism]] of smooth sets) already if it is a *[[local isomorphism]]* in that its transformation $f_\ast$ of plots is a [[bijection]] (not necessarily on all plots but) between *[[germs]]* of plots (around $0 \in \mathbb{R}^n$, say, hence a bijection on "[[stalks]]" at $0$).

This way one find that the [[category]] of [[smooth sets]] should be the "[[localization of a category|localization]]" $L^{iso}$ of the [[category of presheaves]] on [[CartSp]] at the *[[stalk]]-wise [[bijections]]* hence at the "[[local isomorphisms]]" ($liso$), also known as the *[[category of sheaves]]* or the *[[sheaf topos]]* over the *[[site]]* [[CartSp]]:

\[
  \label{SmoothSetsByLocalization}
  SmoothSet
  \;\coloneqq\;
  Sh(CartSp)
  \;\simeq\;
  L^{liso}  PSh(CartSp)
  \,.
\]

For example, if $X$ is an ordinary [[smooth manifold]] then it is regarded as a smooth set by taking its plots to be the actual [[smooth functions]] into it:

$$
  \array{
    SmthMfd &\hookrightarrow& SmoothSet
    \\
    X 
      &\mapsto& 
    \underset{
      Plot(-;X)
    }{\underbrace{C^\infty(-;X)}}
  }
$$

In particular, the probe [[Cartesian spaces]] $\mathbb{R}^n$ are incarnated themselves as smooth sets in this way. This allows to compare the *prescribed* plots $Plot(\mathbb{R}^n,X)$ of any smooth set with the actual smooth maps $Hom\big(\mathbb{R}^n, X \big)$ into it (forming the [[hom-sets]] of [[SmoothSet]]), and remarkably they coincide (this is the *[[Yoneda lemma]]* over [[CartSp]]), thus rendering consistent the above "bootstrap definition" of smooth sets:

$$
  \left.
  \begin{array}{l}
    X \in SmoothSet
    \\
    \mathbb{R}^n \in CartSp
  \end{array}
  \right\}
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  \array{
    Hom\big(\mathbb{R}^n,\, X\big)
    &\overset{\sim}{\longrightarrow}&
    Plot\big(\mathbb{R}^n,\, X\big)
    \\
    f &\mapsto& f_\ast id_{\mathbb{R}^n}
    \,.
  }
$$

But the category [[SmoothSet]] contains now much more than just ordinary [[smooth manifolds]], in particular it contains ([[truncated object in an (infinity,1)-category|0-truncated]]) [[moduli stacks]] of [[differential forms]]:

For $p \in \mathbb{N}$, the smooth [[differential n-forms]] clearly form a [[sheaf]] over [[CartSp]] and hence may be regarded as the plots of a [[smooth set]] $\mathbf{\Omega}^p_{dR} \,\in\, SmoothSet$:

$$
  Plot\big(
    \mathbb{R}^n
    ,\,
    \mathbf{\Omega}^p_{dR}
  \big)
  \;\;
  \coloneqq
  \;\;
  \Omega^p_{dR}(\mathbb{R}^n)
  \,.
$$

One checks that this is a moduli stack for differential forms on [[smooth manifolds]], in that for $X \in SmthMfd \hookrightarrow SmthSet$ we have a [[natural bijection]]

\[
  \label{DifferentialFormsModulatedOnManifolds}
  X \in SmthMfd \hookrightarrow SmthSet
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  Hom\big(
    X
    ,\,
    \mathbf{\Omega}^p_{dR}
  \big)
  \;\simeq\;
  \Omega^p_{dR}(X)
\]

of the smooth maps from $X$ into $\mathbf{\Omega}^p_{dR}$ with the actual smooth differential forms.

Here it is useful to think of $\mathbf{\Omega}^p_{dR}$ as a space which carries a *universal differential $p$-form* $\omega_p^{univ} \,\in\, \Omega^p_{dR}\big(\mathbf{\Omega}^p_{dR}\big)$ (as befits a moduli stack of differential forms) such that every differential form on any $X$ is the [[pullback of differential forms|pullback]] of $\omega_p^{univ}$ along a unique smooth map $X \to \mathbf{\Omega}^p_{dR}$.

In fact, it makes sense to define differential forms on any smooth set by
$$
  X \,\in\, SmthSet
  \;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  \Omega^p_{dR}(X)
  \;\coloneqq\;
  Hom\big(
    X
    ,\,
    \mathbf{\Omega}^p_{dR}
  \big)
$$

and then that universal differential form on $\mathbf{\Omega}^p_{dR}$ actually exists:

$$
  \omega_p^{univ}
  \;\coloneqq\;
  id
  \,\in\,
  Hom\big(
    \mathbf{\Omega}^p_{dR}
    ,\,
    \mathbf{\Omega}^p_{dR}
  \big)  
  \;\equiv\;
  \Omega^p_{dR}\big(
    \mathbf{\Omega}^p_{dR}
  \big)
  \,.
$$

It is in this way that the category [[SmoothSet]] makes (0-truncated) [[moduli stacks]] exist in just the way they ought to (and higher moduli stacks exist similarly in the higher generalization of [[smooth sets]] to [[smooth infinity-groupoids]] that we turn to below).

For the case at hand, it is now straightforward to further specialize this example: The (0-truncated) moduli stack of [[flat L-infinity algebra valued differential forms|flat $\mathfrak{a}$-valued differential forms]] for a given [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ is the [[smooth set]] whose plots are just those differential forms on [[Cartesian spaces]]

\[
  \label{ModuliSheafOfFlatDifferentialForms}
  \Omega^1_{dR}(\text{-};\mathfrak{a})_{clsd}
  \;\in\;
  SmthSet
\]

and in generalization of (eq:DifferentialFormsModulatedOnManifolds), this is again the moduli stack of such differential forms in that:

\[
  \label{FlatDifferentialFormsModulatedOnManifolds}
  X \in SmthMfd \hookrightarrow SmthSet
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  Hom\big(
    X
    ,\,
    \Omega^1_{dR}(\text{-};\mathfrak{a})_{clsd}
  \big)
  \;\simeq\;
  \Omega^p_{dR}(X)
  \,.
\]



\linebreak


**Simplicial sets of moduli of charges.**

\begin{imagefromfile}
    "file_name": "GeomPhys-HigherGaugeTransformationSimplices.jpg",
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

But independently of the differential geometry, the collection of fields in a [[higher gauge theory]] is not really a [[set]] with unambiguously distinct [[elements]]: A pair $\Phi$, $\Phi'$ of [[gauge fields]] may be distinct and yet [[identification type|identified]] by [[gauge transformations]] $\Phi \underoverset{\sim}{g}{\longrightarrow} \Phi'$.  Moreover, for [[higher gauge fields]] there is not really a set of such gauge transformations either, as any pair of them, in turn, may be distinct and yet [[identification type|identified]] by a [[gauge-of-gauge transformation]] $\mu$, etc.

\begin{imagefromfile}
    "file_name": "GeomPhys-GlobularAmongSimplicial.jpg",
    "float": "right",
    "width": 170,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


There are different equivalent ways to record systems of such [[higher gauge transformations]]. A [[globular set|globular]] or [[cubical set|cubical]] arrangement suggests itself but turns out to come with technical subtleties, while the "[[simplicial set|simplicial]]" arrangement indicated above turns out to be remarkably useful and has an [[simplicial homotopy theory|extremely well-developed theory]]: Here the [[gauge-of-gauge transformations]] are always taken to fill a *[[triangle]]* of ordinary [[gauge transformations]], the next [[higher gauge transformations]] are taken to fill a *[[tetrahedron]]* of these, and generally an $n$-gauge transformation is taken to form the $n$-dimensional generalization of tetrahedra, called *[[n-simplex|$n$-simpleces]]*. Notice that this subsumes the intuitively expected "[[globular set|globular]]" situations by taking some faces of the simplices to be labeled by identity-transformations, as indicated on the right.

Hence (still disregarding its [[differential geometry]]) the [[underlying]] set of fields of a [[higher gauge theory]] is, beyond the "0-simplices" of the nominal fields themselves, actually a system of sets of higher simplices of [[higher gauge transformations]] in any dimension, such that with any $n$-simplex also all its face $(n-1)$-simplices and all the correspoinding "thin" ("degenerate") $(n+1)$-simplices are part of this *[[simplicial set]]*:

\begin{imagefromfile}
    "file_name": "GeomPhys-SimplicialSetSchematics.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Hence --- in the spirit (eq:PlotsByCartesianSpaces) of generalized spaces defined by how to plot out probe-spaces inside them  ---, such [[simplicial sets]] are those generalized spaces which are probe-able by the abstract [[cellular simplices]] $\Delta^n$ forming the [[simplex category]] $\Delta$, and hence the category [[SimpSet]] of simplicial sets is that of [[presheaves]] on $\Delta$:

$$
  SimpSet
  \;\coloneqq\;
  PSh(\Delta)
  \,.  
$$

For example, given a [[Lie group]] $G$ with [[Lie algebra]] $\mathfrak{g}$ then the **[[groupoid]] of $G$-[[Yang-Mills theory|Yang-Mills]] [[gauge potentials]]** on $\mathbb{R}^3$ --  to be denoted $\mathbf{Plt}(\mathbb{R}^3,\mathbf{B}G_{conn})$ for reasons discussed below -- is the [[simplicial set]] whose:

\begin{imagefromfile}
    "file_name": "GeomPhys-GroupoidOfYMFieldOnR3.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -35,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

*0-Simplices* are the YM [[gauge potentials]], hence the [[Lie algebra valued differential form|$\mathfrak{g}$-valued 1-forms]] $A \in \Omega^1_{dR}(\mathbb{R}^3; \mathfrak{g})$;

*1-Simplices* are the smooth $G$-valued functions $g \,\colon\, \mathbb{R}^3 \to G$ serving as [[gauge transformations]] between such [[gauge potentials]];

*2-Simplices* are uniquely filled whenever the gauge transformations around their boundary compose;

*$n\geq 3$-Simplices* are uniquely filled whenever their face $(n-1)$-simplices exist. 

\begin{imagefromfile}
    "file_name": "The2Horns.jpg",
    "float": "right",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

That this example is indeed a *[[groupoid]]* in that the gauge transformation 1-simplices have [[inverse morphism|inverses]] and [[composition|composites]] (whenever composable) is witnessed by the fact that whenever one finds in this simplicial set a pair of 1-simplices that share a 0-simplex (jargon: a "[[horn|2-horn]]" $\Lambda^2_i$) then there exists a 2-simplex completing the diagram.

Similarly one defines the higher [[horns]] $\Lambda^n_i \subset \Delta^n$ to be the sub-simplicial sets of a simplex missing the interior and the $ith$ face, and then says that a simplicial set is an *[[infinity-groupoid|$\infty$-groupoid]]* (historical terminology: *[[Kan complex]]*) if all images of $\Lambda^n_i$ inside it may be completed to an images of $\Delta^n$.:

\begin{imagefromfile}
    "file_name": "GeomPhys-KanCondition.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

As an abstract class of examples: For $\mathcal{X},\, \mathcal{Y} \,\in\, SimpSet_{Kan}$, there is the [[infinity-groupoid|$\infty$-groupoid]] [[derived hom-space|of maps]] between them $Map(\mathcal{X},\mathcal{Y})\,\in\, SimpSet_{Kan}$, whose $\Delta^n$-shaped plots are the $\Delta^n$-parameterized systems of simplicial maps

\[
  \label{MappingComplex}
  Plt\big(
    \Delta^n
    ,\,
    Map(\mathcal{X},\mathcal{Y})
  \big)
  \;\coloneqq\;
  Hom\big(
    \Delta^n
    \times
    \mathcal{X}
    ,\,
    \mathcal{Y}
  \big)
  \,,
\]

hence whose 0-simplices are the plain maps $\mathcal{X} \to \mathcal{Y}$ and whose 1-simplices are [[homotopies]] between such maps.

\[\label{HomotopyEquivalenceOfSimplicialSets}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-HomotopyEquivalence.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Hence a  *homotopy equivalence* between [[infinity-groupoids|$\infty$-groupoids]] consiste of maps back and forth which are inverses *up to homotopy* (in that there exist homotopies $g$, $g'$ as shown).

> (Beware that if one works with all simplicial sets instead of just the [[Kan complexes|Kan-simplicial sets]] among them, as often done in the literature, then the relevant notion of equivalence is instead "[[weak homotopy equivalence]]".)

\begin{imagefromfile}
    "file_name": "GeomPhys-TopologicalSimplices.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

As a more concrete class of examples: A [[topological space]] $X$ gives rise to an [[infinity-groupoid|$\infty$-groupoid]] $\esh X \,\in\, SimpSet_{Kan}$: its *[[path infinity-groupoid]]* whose [[n-morphism|$n$-morphisms]] are the [[continuous map|continuous]] images of the *topological* $n$-simplices $\Delta^n_{Top}$ in $X$:

\[
  \label{SimplicialShape}
  \begin{array}{l}
  Plot\big(
    \Delta^n
    ,\,
    \esh 
    X
  \big)
  \\
  \;\coloneqq\;
  Hom_{Top}\Big(
    \underset{
      \Delta^n_{Top}
      \phantom{
        \vert^{\vert^{\vert}}
      }
    }{
    \underbrace{
      \big\{
        \vec x \in (\mathbb{R}_{\geq 0})^{\times^{n+1}}
        \,\big\vert\,
        \textstyle{\sum}_i x^i = 1
      \big\}
    }
    }
    ,\,
    X
  \Big)
  \,.
  \end{array}
\]

\linebreak

\[\label{HomeoToHomotopyType}\]
\begin{imagefromfile}
    "file_name": "GeomPhys-HomotopyType.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 0,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

This [[path infinity-groupoid|path $\infty$-groupoid]]-construction forgets the topology on $X$ (the "[[cohesion]]" of its points as embodied by its system of [[open subsets]]) but retains the *[[shape modality|shape]]* of $X$, namely its *[[homotopy type]]*: The [[equivalence class]] of $\esh X$ under [[homotopy equivalences]] (eq:HomotopyEquivalenceOfSimplicialSets). A [[homotopy hypothesis|classical fact]] of [[homotopy theory]] asserts (in particular) that every [[homotopy type]] in $SimpSet_{Kan}$ is equivalently the [[shape modality|shape]]/[[path infinity-groupoid|path $\infty$-groupoid]] of some topological space, which traditionally leads to some conflation of these different notion of "space".

Here we shall denote actual homotopy types $\mathcal{X} \,\in\, SimpSet_{Kan}$ by calligraphic symbols. In particular, it is homotopy types $\mathcal{A}$ which determine flux quantization laws [above](#FluxQuantizationLawsAsNonabelianCohomology):

The plain (as opposed to [[differential cohomology|differential]]) [[nonabelian cohomology]] ([above](#NonabelianCohomology))
of a topological space $X$ is an invariant of its [[shape]]/[[homotopy type]] $\esh X$ (eq:SimplicialShape) formed by the [[simplicial mapping complex]] (eq:MappingComplex):

\[
  \label{NonabelianCohomologyViaSimplicialMappings}
  \left.
  \begin{array}{l}
    \mathcal{A}
    \,\in\,
    SimpSet_{Kan}
    \\
    X \,\in\, Top
  \end{array}  
  \;
  \right\}
  \;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;
  H^1(X;\, \mathcal{A})
  \;\;
    \simeq
  \;\;
  \pi_0 Map\big(
    \esh X
    ,\,
    \mathcal{A}
  \big)
  \,,
\]

where on the right $\pi_0(-)$ refers to the connected components of an $\infty$-groupoid $\mathcal{X} \,\in\, SimpSet_{Kan}$ being the [[quotient set]] of the 0-simplices by the [[equivalence relation]] embodied by the 1-simplices:
$
  \pi_0
  \mathcal{X}
  \;\coloneqq\;
  \mathcal{X}_0\big/\mathcal{X}_1
$.

While above we saw that any cohomology class $[\chi] \,\in\, H^1\big(X;\, \mathcal{A}\big)$ may be understood as the *total charge* sourcing $\mathfrak{l}\mathcal{A}$-valued flux, next we may use differential homotopy theory in order to regard actual representative maps $\esh X \to \mathcal{A}$ as witnessing the *local charge*, in a sense, which may be regarded as the source not just of a total flux in $H^1\big(X;\, \mathfrak{l}\mathcal{A}\big)$ but an actual locally defined flux density $\vec B$.


\linebreak

**Smooth simplicial sets of deformations of flux densities.**
With the above discussion one has moduli for 

1. [[flux densities]] with their [[differential geometry|differential geometric]] nature, in [[SmoothSet]],

1. local charges with their [[higher gauge theory|higher gauge theoretic]] nature, in [[SimpSet]].

In order to discuss moduli for the full flux-quantized fields,  one need to combine these two aspects into a category of *smooth simplicial sets* (smooth Kan-simplicial sets, to be precise). 

It is clear that these should be presheaves on [[CartSp]] with values in [[Kan complexes|Kan-simplicial sets]], subject to their *combined* notion of equivalence: *local* equivalences as for [[smooth sets]] (eq:SmoothSetsByLocalization) and *homomotopy* equivalences as for [[infinity-groupoid|$\infty$-groupoids]] (eq:HomotopyEquivalenceOfSimplicialSets):

For $\mathcal{X}, \mathcal{Y} \,\in\, PSh\big(CartSp,\, SimpSet_{Kan}\big)$ a morphism $f \,\colon\, \mathcal{X} \to \mathcal{Y}$ is a **local homotopy equivalence** (lheq) if it is a morphism that restricts to a [[homotopy equivalence]] (eq:HomotopyEquivalenceOfSimplicialSets) on all [[germs]] of plots, hence on all simplicial [[stalks]].

To regard these local homotopy equivalences as the actual equivalences of smooth simplicial sets means to pass to the [[simplicial localization]] of the category of smooth simplicial sets at the local homotopy equivalences, to be denoted:

\[
  \label{SmoothInfinityGroupoids}
  SmthGrpd_\infty
  \;\coloneqq\;
  \mathbf{L}^{lheq}
  SmoothSimpSet_{Kan}
  \;\coloneqq\;
  \mathbf{L}^{lheq}
  PSh\big(
    CartSp
    ,\,
    SimpSet_{Kan}
  \big)
\]

and referred to as the *[[(infinity,1)-topos|$\infty$-topos]] of [[smooth infinity-groupoid|smooth $\infty$-groupoids]]*.

It is clear that both [[smooth sets]] as well as plain [[infinity-groupoids|$\infty$-groupoids]] are jointly contained in this larger category, the former as the objects which are constant on [[simplex category|$\Delta$]] (the [[truncated object of an (infinity,1)-category|0-truncated objects]]) and the latter as the objects which are constant on [[CartSp|$CartSp$]] (the geometrically [[discrete object|discrete]] objects):

\begin{imagefromfile}
    "file_name": "GeomPhys-SmoothInfinityGroupoids-240206.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}



\begin{imagefromfile}
    "file_name": "GeomPhys-CechGroupoid.jpg",
    "float": "right",
    "width": 520,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

As an example of a local homotopy equivalence of smooth simplicial sets, consider a [[smooth manifold]] $X^d$  and $\big\{\mathbb{R}^d \simeq U_j \xhookrightarrow{ \iota_j } X \big\}_{j \in J}$ a [[good open cover]]. Then the **[[Čech groupoid]]** $\widehat X{}^d \,\in\, SmoothSimpSet_{Kan}$ has as $\Delta^n$-shaped plots the smooth maps into the $(n+1)$-fold intersections of the open patches:

\[
  \label{CechGroupoid}
  \begin{array}{l}
  Plot\Big(
    \mathbb{R}^n
    \times
    \Delta^n
    ,\,
    \widehat{X}{}^d
  \Big)
  \\
  \;
  \coloneqq
  \;
  C^\infty\big(
    \mathbb{R}^n
    ,\,
    \underset{
      j_\bullet \in J^{n+1}
    }{
      \textstyle{\coprod}
    }
    \,
    U_{j_0} \cap \cdots \cap U_{j_n}
  \big)
  \,.
  \end{array}
\]

Since the patches are subsets of $X^d$, this has an evident map to $X^d$ which is readily seen to be a local homotopy equivalence.

Since this map becomes invertible in (eq:SmoothInfinityGroupoids), maps in $SmoothGrpd_\infty$ out of $X^d$ are the same as maps out of $\widehat X{}^d$. But some further theory shows that $\widehat X{}^d$ is a *good* (namely: [[cofibrant object|cofibrant]]) representative of the local homotopy equivalence class of $X^d$, in that maps out of it may be considered already before localization, in $SmoothSimpSet_{Kan}$.

This is important, because for any [[infinity-groupoid|$\infty$-groupoid]] $\mathcal{A} \,\in\, SimpSet_{Kan} \xhookrightarrow{const} SmoothSimpSet_{Kan}$ regarded as a geometrically discrete [[smooth infinity-groupoid|smooth $\infty$-groupoid]], the [[nonabelian cohomology]] $H^1\big(X;\, \Omega\mathcal{A}\big)$ (eq:NonabelianCohomologyViaSimplicialMappings)
may equivalently be computed as the special case of "differential" cohomology of [[smooth infinity-groupoid|smooth $\infty$-groupoids]] with coefficients that happen to be non-differential (geometrically [[discrete object|discrete]]) 

\[
  \label{NonabelianCohomologyViaSimplicialMappings}
  \left.
  \begin{array}{l}
    \mathcal{A}
    \,\in\,
    SimpSet_{Kan}
    \\
    X^d \,\in\, SmthMfd
  \end{array}  
  \;
  \right\}
  \;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;
  H^1(X;\, \mathcal{A})
  \;\;
    \simeq
  \;\;
  \pi_0 Map\big(
    \,
    \widehat X{}^d
    ,\,
    \mathcal{A}
    \,
  \big)
  \,,
\]

In components this is the **[[Čech cohomology]]**-presentation of generalized [[nonabelian cohomology]].

On the other hand, if $A \,\in\, SmoothSet \hookrightarrow SmoothGrpd_\infty$ is 0-truncated, then smooth simplicial maps out of the [[Čech groupoid]] into $A$ collapse to maps out of just $X$ itself.


\begin{imagefromfile}
    "file_name": "GeomPhys-ModulatingFluxesAndCharges.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": 0, 
        "left": 20
    }
\end{imagefromfile}

In summary so far, this means that flux densities as well as their local charges are now *both* "[[modulating morphism|modulated]]" by maps of [[smooth infinity-groupoids|smooth $\infty$-groupoids]]:

In order to impose flux quantization -- hence the condition that these $\mathfrak{a}$-flux densities are sourced by such $\mathcal{A}$-charges -- it remains to construct moduli stack in which both these components may be universally related:

\linebreak


**Higher deformations of flux densities.**
Recall (eq:ConcordanceOfFlatDifferentialForms) that a [[coboundary]] in $\mathfrak{a}$-valued de Rham cohomology is a "[[concordance]]" of flux densities, to be thought of as a path of smooth variations of the flux densities subject to their [[Bianchi identities]]:

\begin{imagefromfile}
    "file_name": "GeomPhys-DeformationPathOfFluxDensities-240204.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

But in higher gauge theories, there are also non-trivial deformations-of-deformations varying over [[n-simplex|$n$-simplices]]":

\begin{imagefromfile}
    "file_name": "GeomPhys-SimplicialSetOfFluxDeformations.jpg",
    "width": 900,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

Since each component here is a set of plots of a [[smooth set]] of on-shell flux densities (eq:ModuliSheafOfFlatDifferentialForms), we have in total a smooth (Kan-)simplicial set &lbrack;[FSS23-Char, Def. 9.1](#FSS23)&rbrack; which we may think of as the [[shape modality|shape]]/[[shape via cohesive path ∞-groupoid|smooth path $\infty$-groupoid]]

$$
  \esh
  \,
  \Omega^1_{\mathrm{dR}}\big(
    -;
    \mathfrak{a}
  \big)_{clsd}
  \;\in\;
  SmoothSimpSet_{Kan}
  \,.
$$

It is in this object that [[flux densities]] become comparable to their local charges:

First of all, there is evidently the canonical inclusion of the smooth set of flux densities

$$
  \Omega^1_{\mathrm{dR}}\big(
    -;
    \mathfrak{a}
  \big)_{clsd}
  \xrightarrow{
    \;\;
    \eta^{\esh}
    \;\;
  }
  \,
  \Omega^1_{\mathrm{dR}}\big(
    -;
    \mathfrak{a}
  \big)_{clsd}
  \,.
$$

But moreover, 
if here $\mathfrak{a} \,\simeq\, \mathfrak{l}\mathcal{A}$ is a [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] (Prop. \ref{SullivanTheorem}), then the [[fundamental theorem of dg-algebraic rational homotopy theory]] (eq:FundamentalTheoremOfRHT) furthermore says that we have a (homotopy-)equivalence to the $\mathbb{R}$-rationalization $L^{\mathbb{R}} \mathcal{A}$ of $\mathcal{A}$   ([above](#RationalizationOverTheReals)):

$$
  \mathcal{A}
    \xrightarrow{\;\; \eta^{\mathbb{R}} \;\;}
  L^{\mathbb{R}}
  \mathcal{A}
    \xrightarrow{\;\; \sim \;\;}
  \esh
  \,
  \Omega^1_{\mathrm{dR}}\big(
    -;
    \mathfrak{a}
  \big)_{clsd}  
  \,.
$$

This way we may now implement [[flux quantization]] 

* of flux densities $\vec F \,\colon\, X^d \to \Omega^1_{dR}\big(-;\mathfrak{a}\big)$

* by local charges $\xhi \,\colon\, X^d \to \mathcal{A}$



\linebreak

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
 {#CFieldFluxQuantizationIn10d}

(...)

\linebreak

### B-&RR-Field flux quantization in 10d

(...)


\linebreak



## References

* {#Abrikosov57a} [[Alexei Abrikosov]], *On the Magnetic properties of superconductors of the second group*, Sov. Phys. JETP **5** (1957) 1174-1182; Zh. Eksp. Teor. Fiz. **32** (1957) 1442-1452 &lbrack;[spire:9138](https://inspirehep.net/literature/9138), [[Abrikosov-MagneticPropertiesOfSuperconductors.pdf:file]]&rbrack;

* {#Alfonsi24} [[Luigi Alfonsi]], *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;

* {#Alvarez85a} [[Orlando Alvarez]], *Cohomology and Field Theory*, talk at: *Symposium on Anomalies, Geometry, Topology*, Argonne IL (28-30 March 1985) &lbrack;[inspire:965785](https://inspirehep.net/conferences/965785), [pdf](https://lib-extopc.kek.jp/preprints/PDF/1985/8507/8507262.pdf), [[Alvarez-CohomologyAndFieldTheory.pdf:file]]&rbrack;

* {#Alvarez85b} [[Orlando Alvarez]], _Topological quantization and cohomology_, Comm. Math. Phys. **100** 2 (1985) 279-309 &lbrack;[euclid:cmp/1103943448](https://projecteuclid.org/euclid.cmp/1103943448)&rbrack;


* {#BandosBerkovitsSorokin98} [[Igor Bandos]], [[Nathan Berkovits]], [[Dmitri Sorokin]], *Duality-Symmetric Eleven-Dimensional Supergravity and its Coupling to M-Branes*, Nucl. Phys. B **522** (1998) 214-233 \[<a href="https://doi.org/10.1016/S0550-3213(98)00102-3">doi:10.1016/S0550-3213(98)00102-3</a>, [arXiv:hep-th/9711055](https://arxiv.org/abs/hep-th/9711055)\]

* {#BeckerBeniniSchenkelSzabo15} [[Christian Becker]], [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], Rem. 2.3 in: _Abelian duality on globally hyperbolic spacetimes_, Commun. Math. Phys. **349** (2017) 361-392 &lbrack;[arXiv:1511.00316](https://arxiv.org/abs/1511.00316), [doi:10.1007/s00220-016-2669-9](https://doi.org/10.1007/s00220-016-2669-9)&rbrack;


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


* {#FSS19HigherStruc} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The rational higher structure of M-theory]]_  in: _Proceedings of the [LMS-EPSRC Durham Symposium](http://www.maths.dur.ac.uk/lms/)_: _[[Higher Structures in M-Theory 2018]]_, August 2018, Fortschritte der Physik **67** 8-9 (2019) &lbrack;[arXiv:1903.02834](https://arxiv.org/abs/1903.02834), [doi:10.1002/prop.201910017](https://doi.org/10.1002/prop.201910017)&rbrack;

* {#FSS21WZ} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_, Comm. Math. Phys. **384** (2021) 403–432 &lbrack;[arXiv:1906.07417](https://arxiv.org/abs/1906.07417), [doi:10.1007/s00220-021-03951-0](https://doi.org/10.1007/s00220-021-03951-0)&rbrack;


* {#FSS23} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;

* {#Freed00} [[Daniel Freed]], *[[Dirac charge quantization and generalized differential cohomology]]*, Surveys in Differential Geometry **7**, Int. Press (2000) 129-194 &lbrack;[arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220), [doi:10.4310/SDG.2002.v7.n1.a6](https://dx.doi.org/10.4310/SDG.2002.v7.n1.a6), [spire:537392](https://inspirehep.net/literature/537392)&rbrack;


* {#FreedMooreSegal07a} [[Daniel S. Freed]], [[Gregory W. Moore]], [[Graeme Segal]], *The Uncertainty of Fluxes*, Commun. Math. Phys. **271** (2007) 247-274 &lbrack;[arXiv:hep-th/0605198](https://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3)&rbrack;

* {#FreedMooreSegal07b} [[Daniel S. Freed]], [[Gregory W. Moore]], [[Graeme Segal]], *Heisenberg Groups and Noncommutative Fluxes*, Annals Phys. **322** (2007) 236-285 &lbrack;[arXiv:hep-th/0605200](https://arxiv.org/abs/hep-th/0605200), [doi:10.1016/j.aop.2006.07.014](https://doi.org/10.1016/j.aop.2006.07.014)&rbrack;

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]]: *[[schreiber:Smooth Sets of Fields]]* &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301)&rbrack;


* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], *[[Quantization of Gauge Systems]]*, Princeton University Press (1992) &lbrack;[doi:10.2307/j.ctv10crg0r](https://doi.org/10.2307/j.ctv10crg0r)&rbrack;

* {#Hyperphysics} Hyperphysics, *Magnetic Flux* &lbrack;[hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html](http://hyperphysics.phy-astr.gsu.edu/hbase/magnetic/fluxmg.html)&rbrack;

* {#LazaroiuShahbazi22} [[Calin Lazaroiu]], [[Carlos S. Shahbazi]], around Def. 1.16 in: *The duality covariant geometry and DSZ quantization of abelian gauge theory*, Advances in Theoretical and Mathematical Physics **26** (2022) 2213–2312 &lbrack;[arXiv:2101.07236](https://arxiv.org/abs/2101.07236), [doi:10.4310/ATMP.2022.v26.n7.a5](https://dx.doi.org/10.4310/ATMP.2022.v26.n7.a5)&rbrack;

* {#LazaroiuShahbazi23} [[Calin Lazaroiu]], [[Carlos S. Shahbazi]], around (3) in: *The geometry and DSZ quantization of four-dimensional supergravity*, Letters in Mathematical Physics  **113** 4 (2023) &lbrack;[arXiv:2101.07778](https://arxiv.org/abs/2101.07778), [doi:10.1007/s11005-022-01626-y](https://doi.org/10.1007/s11005-022-01626-y)&rbrack;


* {#LoudonMidgley09} J. C. Loudon, P. A. Midgley, *Imaging Flux Vortices in Type II Superconductors with a Commercial Transmission Electron Microscope*, Ultramicroscopy **109** 6 (2009) 700-729 &lbrack;[arXiv:0807.2401](https://arxiv.org/abs/0807.2401), [doi:10.1016/j.ultramic.2009.01.008](https://doi.org/10.1016/j.ultramic.2009.01.008)&rbrack;

* {#Martin09} Thomas Martin (ed.), *Faraday's diary of experimental investigation* 1820-1862, HR Direct (2009)  &lbrack;[webpage](http://faradaysdiary.com/), preview:[pdf](http://faradaysdiary.com/ws3/faraday.pdf)&rbrack;

* {#MkrtchyanValach23} [[Karapet Mkrtchyan]], [[Fridrich Valach]], *Democratic actions for type II supergravities*, Phys. Rev. D **107** 6 (2023) 066027 \[<a href="https://doi.org/10.1103/PhysRevD.107.066027">doi:10.1103/PhysRevD.107.066027</a>[arXiv:2207.00626](https://arxiv.org/abs/2207.00626)\]


* {#Polchinski95} [[Joseph Polchinski]], _Dirichlet-Branes and Ramond-Ramond Charges_, Phys. Rev. Lett. **75** (1995) 4724-4727 &lbrack;[arXiv:hep-th/9510017](https://arxiv.org/abs/hep-th/9510017), [doi:10.1103/PhysRevLett.75.4724](https://doi.org/10.1103/PhysRevLett.75.4724)&rbrack;


* {#MinasianMoore97} [[Ruben Minasian]], [[Gregory Moore]], *K-theory and Ramond-Ramond charge*, JHEP 9711:002 (1997) &lbrack;[arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230), [doi:10.1088/1126-6708/1997/11/002](https://doi.org/10.1088/1126-6708/1997/11/002)&rbrack;

* {#Sati10} [[Hisham Sati]], *Geometric and topological structures related to M-branes*, in *Superstrings, Geometry, Topology, and $C^\ast$-algebras*, Proc. Symp. Pure Math. **81** (2010) 181-236 &lbrack;[arXiv:1001.5020](http://arXiv.org/abs/1001.5020), [ams:pspum/081](http://www.ams.org/books/pspum/081)&rbrack;

* {#SS23-MF} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:M/F-Theory as Mf-Theory|M/F-Theory as $M f$-Theory]]*, Rev. Math. Phys. **35** 10 (2023) &lbrack;[doi:10.1142/S0129055X23500289](https://doi.org/10.1142/S0129055X23500289), [arXiv:2103.01877](https://arxiv.org/abs/2103.01877)&rbrack;

* {#SS23-FQ} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;

* {#SS23-Obs} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Quantum Observables of Quantized Fluxes]]* &lbrack;[arXiv:2312.13037](https://arxiv.org/abs/2312.13037)&rbrack;

* {#SatiVoronov22} [[Hisham Sati]], [[Alexander Voronov]], (13) in: *Mysterious Triality and M-Theory* &lbrack;[arXiv:2212.13968](https://arxiv.org/abs/2212.13968)&rbrack;


* {#Schreiber24} [[Urs Schreiber]], *[[schreiber:Higher Topos Theory in Physics]]*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2311.11026](https://arxiv.org/abs/2311.11026)&rbrack;

* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. **22** 1   (1997) 1-13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), <a href="https://doi.org/10.1016/S0393-0440(96)00042-3">doi:10.1016/S0393-0440(96)00042-3</a>&rbrack;

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019 (1998) \[<a href="http://arxiv.org/abs/hep-th/9810188">arXiv:hep-th/9810188</a>, [doi:10.1088/1126-6708/1998/12/019](https://doi.org/10.1088/1126-6708/1998/12/019)\]

(...)

\linebreak

\linebreak

