+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

### The class

In the [[string theory]] and [[M-theory]] literature, $I_8$ denotes the degree-eight [[rational cohomology|rational]] [[characteristic class]]

\[
  \label{TheTerm}
  I_8(E)
  \;\coloneqq\;
  \frac{1}{48}\left(
    p_2(E)
    -
    \frac{1}{4}p_1(E)^2
  \right)
  \;\in\; H^8(X;\mathbb{Q})
\]

of a [[real vector bundle]] $E\to X$, usually the [[tangent bundle]] $E \coloneq T X^{1,10}$ of an 11-dimensional [[spacetime]] $X^{1,10}$. Here $p_i$ denote the [[Pontryagin classes]] and multiplication denotes their [[cup product]]. For $E$ [[spin structure|spin structured]], $\lambda(E) \coloneqq \tfrac{1}{2} p_1(E)$ is the [[first fractional Pontryagin class]], so that $I_8=\tfrac{1}{48}(p_2-\lambda^2)$. Although $\lambda$ is integral on spin bundles, $I_8$ need not be integral.

When $E$ is equipped with a [[connection on a vector bundle|connection]] $\nabla$ with [[curvature]] $R = R(\nabla)$ the same notation is used for the corresponding [[curvature characteristic form]], the [[closed differential form|closed]] [[differential 8-form]] $I_8(R) \in \Omega^8_{dR}(X)$. 

Sometimes $\pm I_8$ is denoted "$X_8$" and generally sign and normalization conventions vary. With the usual real-vector trace convention, we have

\[
  \label{TheChernWeilForm}
  I_8(R)
  =
  -\frac{1}{192}\,\frac{1}{(2\pi)^4}
  \left(
    \operatorname{tr}(R^4)
    -
    \frac{1}{4}
   \big(\operatorname{tr}(R^2)\big)^2
  \right)
  \mathrlap{\,,}
\]
where multiplication now denotes [[wedge product]] of [[differential forms]].

By [[Chern-Weil theory]], the de Rham class of this form is the image of $I_8(E)$ under [[extension of scalars]] from $\mathbb{Q}$ to $\mathbb{R}$:

\[
  \begin{array}{ccccccc}
    \Omega^8_{\mathrm{cl}}(X)
    &\longrightarrow& H^8_{dR}(X)
    &\simeq& H^8(X;\mathbb{R})
    &\longleftarrow& H^8(X;\mathbb{Q})
    \\
    I_8(R)&\longmapsto&[I_8(R)]_{dR}
    &\longleftrightarrow& I_8(E)\otimes 1
    &\longleftarrow& I_8(E)
    \mathrlap{\,.}
  \end{array}
\]

Here $\Omega^8_{\mathrm{cl}}(X)$ denotes the closed 8-forms on the base $X$. Changing the connection changes the representative by an exact form, not the characteristic class.

### As a gravitational coupling

In [[string theory]]/[[M-theory]], $I_8$ appears in a leading [[higher curvature correction]] coupling the [[higher gauge fields]] to [[gravity]]:

1. The [[one-loop]] [[effective action functional]] of [[type IIA string theory]] contains, in addition to that of plain [[type IIA supergravity]], a term proportional to 

   \[
     \label{TheOneLoopActionTerm}
     \int_{X^{1,9}} B_2 \wedge I_8(R)
   \]

   for $B_2$ the [[differential 2-form|2-form]] [[gauge potential]] of the [[B-field]].

   For this reason $I_8$ is widely known also as the *one-loop term*, following [Vafa & Witten 1995](#VafaWitten95), [Duff, Liu, Minasian 1995](#DuffLiuMinasian95).

1. The leading eight-derivative correction to the [[action functional]] of [[11D supergravity]] contains a term proportional to

   \[
     \label{TheHigherCurvatureActionTerm}
     \int_{X^{1,10}} C_3 \wedge I_8(R)
     \mathrlap{\,,}
   \]

   where $C_3$ is the [[differential 3-form|3-form]] [[gauge potential]] of the [[supergravity C-field]]. This is one term in a supersymmetric interaction, not the entire correction.

These two terms (eq:TheOneLoopActionTerm) and (eq:TheHigherCurvatureActionTerm) are related under [[duality between M-theory and type IIA string theory]].

(Here in both cases $R = R(\nabla)$ is the [[Riemann curvature]] of the respective [[Levi-Civita connection|Levi-Civita]] [[spin connection]] [[first order formulation of gravity|reflecting]] the [[field (physics)|field]] of [[gravity]].)

Under passage to [[Euler-Lagrange equations of motion]], the term (eq:TheHigherCurvatureActionTerm) modifies the [[equation of motion]] of the [[supergravity C-field]]. Written as a [[Bianchi identity]] for the dual flux density $G_7$ (which equals $\star G_4$ to leading order), the modified equation reads
\[
  \label{TheI8CorrectedCFieldEquationOfMotion}
  \mathrm{d} G_7
  =
  -\tfrac{1}{2}
  G_4 \wedge G_4
  + 
  \beta I_8(R)
\]
for some [[real number|real]] [[coefficient]] $\beta$, carrying [[physical unit]] $\ell_P^6$, for $\ell_P$ the [[Planck length]] in 11D (sign conventions as [below](#TheOrdinarySpacetimeForm)). Thereby $I_8$ appears then also in the [[C-field tadpole cancellation]] for [[KK-compactifications]] on [[8-manifolds]]. 

### Original discussions
 {#OriginalDiscussions}

Historically, the type IIA one-loop coupling was studied by [Vafa & Witten 1995](#VafaWitten95), and its eleven-dimensional interpretation by [Duff, Liu & Minasian 1995](#DuffLiuMinasian95). [Becker & Becker 1996](#BeckerBecker96) used the correction in compactifications on eight-manifolds. [Witten 1996](#Witten96) subsequently analyzed both [shifted C-field flux quantization](#WittenFluxQuantization96) and the [[M5-brane|five-brane]] [[effective action]]. [Freed, Harvey, Minasian & Moore 1998](#FreedHarveyMinasianMoore98) established the role of the [[bulk]] [[higher Chern-Simons theory|Chern-Simons]] [[interaction]] in cancellation of the remaining normal-bundle anomaly. Later developments include the formulation of [[C-field flux quantization]] by [Diaconescu, Freed & Moore 2003](#DiaconescuFreedMoore03), and [[anomaly inflow]] computations for [[wrapped brane|wrapped]] [[M5-branes]] by [BBMN 2019](#BBMN19).


### Superspace refinement

The characteristic-class and anomaly arguments [above](#OriginalDiscussions) identify the ordinary curvature coupling. They do not by themselves determine

1. how the curvature coupling extends to a [[local supersymmetry|locally]] [[supersymmetry|supersymmetric]] interaction, including [[flux]] and [[fermion]] ([[gravitino]]) terms,

1. how implementation of the modified [[equation of motion]] (eq:TheI8CorrectedCFieldEquationOfMotion) on [[super-spacetime]] ("[[superspace]]") affects the [[torsion constraints of supergravity|torsion constraints]] of [[11D supergravity]].

The [[superspace]] approach of [Howe & Tsimpis 2003](#HoweTsimpis03) and [Souères & Tsimpis 2017](#SoueresTsimpis17) uses a [[differential form on supermanifold|superform]] enhancement of $I_8(R)$ (eq:TheChernWeilForm), denoted $\mathcal{I}_8(\mathcal{R})$ [below](#TheSuperspace8Form), built from the superspace Lorentz curvature $\mathcal{R}$, as a source in the Bianchi identity of the super flux 7-form.

In ordinary 11D supergravity the flux superforms have at most two spinorial indices. The curvature superform $\mathcal{I}_8$, however, generally has components with as many as eight. Thus the sourced Bianchi identity cannot in general be satisfied while retaining the classical flux ansatz. In the deformation framework of [Howe & Tsimpis 2003](#HoweTsimpis03), a nontrivial first-order change of the local supergravity equations is encoded by the previously vanishing component $G_{\alpha\beta\gamma\delta}$ of the 4-form, modulo field redefinitions; the 4-form Bianchi identities then relate this component to a change of the dimension-zero torsion.

Three questions must be distinguished: constructing a first-order supersymmetric action term; determining the corresponding deformation of the constrained superspace geometry; and extending that deformation consistently to higher orders. The cited superspace literature gives a cohomological framework for these questions and substantial partial results. In particular, [Souères & Tsimpis 2017](#SoueresTsimpis17) identify a sufficient condition for the first-order anomaly superinvariant and verify part of it. Their remaining check, and the further questions concerning the full deformation, are described [below](#WhatIsKnownAndWhatIsOpen).

\linebreak


## Properties


### As a higher curvature correction to 11-dimensional supergravity
  {#AsHigherCurvatureCorrectionTo11dSugra}

#### The ordinary spacetime form and corrected flux equation
 {#TheOrdinarySpacetimeForm}

The [[interaction|coupling]] [[Lagrangian density]] $C_3\wedge I_8(R)$ (eq:TheHigherCurvatureActionTerm) belongs to the eight-[[derivative]] sector of the [[M-theory]] [[effective action]], at order $\ell_p^6$ (with $\ell_p$ the 11D [[Planck length]]) relative to the two-derivative action of [[D=11 supergravity]]. Its gravitational [[supersymmetry]] partners include terms schematically of the form $R^4$; a full completion also involves the [[supergravity C-field]] [[flux density]] $G_4$ and the [[gravitino]]. For the different approaches to these corrections, see at *[[11D supergravity]]* the section *[References -- Higher Curvature Corrections](D%3D11+N%3D1+supergravity#ReferencesOnHigherCurvatureCorrectionsIn11dSupergravity)*.

On ordinary eleven-dimensional spacetime, away from magnetic sources, the bosonic anomaly-corrected flux equations are conventionally organized as

\[
  \label{11dSugraBIAtOrder6}
  \begin{aligned}
    \mathrm{d}G_4 
    &=0
    \,,
    \\
    \mathrm{d}G_7 
      &=
    -\frac{1}{2} G_4\wedge G_4
     \,+\,
    \beta \, I_8(R)
    \mathrlap{\,,}
\end{aligned}
\]

through the order under consideration, where the [[real number|real]] parameter $\beta$ is proportional to $\ell_p^6$. Its numerical factor and sign depend on conventions for the fluxes and action; the normalization of $I_8$ here remains that of (eq:TheTerm). Reversing the convention for $G_7$ reverses both terms on the right. For example:

* [Souères & Tsimpis 2017, (4.2)--(4.3)](#SoueresTsimpis17) write $\mathrm{d}G_7 + \tfrac{1}{2}G_4\wedge G_4 = \ell^6 X_8$ with $X_8 \coloneqq \operatorname{tr}R^4 - \tfrac{1}{4}(\operatorname{tr}R^2)^2$ and a numerical factor absorbed into $\ell$. Since $X_8 = -192 (2\pi)^4 I_8$ (by eq:TheChernWeilForm), this is (eq:11dSugraBIAtOrder6) with $\beta = -192(2\pi)^4\ell^6$ in their units.

* [Howe & Tsimpis 2003, (56)](#HoweTsimpis03) write $\mathrm{d}G_7 = +\tfrac{1}{2}G_4\wedge G_4 + \beta X_8$, with the opposite sign convention for $G_7$; their parameter $\beta$ must also be translated when comparing the source coefficients.

On ordinary [[spacetime]] the second equation in (eq:11dSugraBIAtOrder6) packages the corrected C-field [[equation of motion]]. To leading order $G_7=\star G_4$, but this relation itself receives corrections at order $\beta$. Concretely ([Souères & Tsimpis 2017, (4.10)--(4.11)](#SoueresTsimpis17)): if the bosonic corrected action is $\int \big(R\star 1 - \tfrac{1}{2}G_4\wedge\star G_4 - \tfrac{1}{6}C_3\wedge G_4\wedge G_4 + \ell^6 X_8\wedge C_3 + \Delta L\star 1\big)$ with $\Delta L$ gauge invariant, then the variation of $\Delta L$ with respect to $C_3$ is exact, and is absorbed into a corrected duality relation $G_7 = \star G_4 + \mathcal{O}(\ell^6)$.

This bosonic flux equation displays only part of the correction. The curvature coupling and its supersymmetry partners also modify the gravitational and fermionic equations. On superspace these changes must be compatible with all components of the flux and geometric Bianchi identities, as discussed [below](#EffectOfTheSourceOnSuperspaceGeometry).


#### Undeformed supergravity on superspace
 {#UndeformedSugraOnSuperspace}

Let $\mathcal{M}^{11|32}$ be the 11-dimensional [[super spacetime]], with super-coframe $(E^a, E^\alpha)$ ($a = 0, \cdots, 10$ a vector index, $\alpha = 1, \cdots, 32$ a Majorana spinor index), equipped with a [[Lorentz group|Lorentz]]-valued [[spin connection]] with [[torsion]] $T^A$ and [[curvature]] $\mathcal{R}$. Superforms decompose by the number $p$ of even and $q$ of odd form indices: $\Omega^n = \bigoplus_{p+q = n}\Omega^{p,q}$. Assigning engineering dimension $-1$ to $E^a$ and $-1/2$ to $E^\alpha$, the components of a given superform have dimension increasing by $1/2$ with each odd index traded for an even one.

**The torsion constraint.** The superspace formulation of ordinary [[11D supergravity]] goes back to [Cremmer & Ferrara 1980](#CremmerFerrara80) and [Brink & Howe 1980](#BrinkHowe80). Central to it is the constraint on the dimension-zero torsion

\[
  \label{UndeformedDimZeroTorsion}
  T_{\alpha\beta}{}^c
  \;=\;
  - \mathrm{i}\, (\gamma^c)_{\alpha\beta}
  \,.
\]

Sign and normalization vary between references, e.g. [Souères & Tsimpis 2017, (2.4)](#SoueresTsimpis17), [CGNT 2004, (2.9)](#CGNT04). The dimension-zero equation should be distinguished from a full set of conventional torsion constraints, which also specifies components with vector indices.

**The geometric formulation.** [Howe 1997](#Howe97) derives the on-shell theory from the standard dimension-zero torsion using Weyl superspace, with structure group $\mathrm{Spin}(1,10)\times\mathbb{R}^{+}$. The scale curvature vanishes, so the scale connection can be removed locally. Passing to the usual formulation globally requires attention to its holonomy; simple connectivity is a sufficient hypothesis used in [CGNT 2004, §3](#CGNT04). It is not a prerequisite for the local argument. See also [Howe & Tsimpis 2003, §2](#HoweTsimpis03) and [CGNT 2004, §2.5--2.6](#CGNT04).

**The duality-symmetric flux formulation.** In [Giotopoulos, Sati & Schreiber 2024, Def. 2.74](#GSS24), the super-coframe $(e^a,\psi^\alpha)$ and spin connection $\omega$ obey the full bosonic super-torsion constraint $T^a=\mathrm{d}e^a+\omega^a{}_b\wedge e^b-\overline{\psi}\Gamma^a\psi=0$. This includes the dimension-zero constraint in their conventions, together with vanishing vector-valued torsion components of higher dimension.

A detailed equivalence theorem, with computer algebra checks, is [Giotopoulos, Sati & Schreiber 2024, Thm. 3.1](#GSS24). Consider an $(11\vert 32)$-dimensional super-spacetime satisfying the above bosonic torsion constraint, with no constraint imposed on the gravitino field strength. It carries super flux densities of the form ([GSS24, (8)--(9)](#GSS24))

\[
  \label{DualitySymmetricSuperFlux}
  \begin{aligned}
    G^s_4
    &=
    \tfrac{1}{4!}(G_4)_{a_1 \cdots a_4}\, e^{a_1}\cdots e^{a_4}
    +
    \tfrac{1}{2}\big(\overline{\psi}\,\Gamma_{a_1 a_2}\psi\big)\, e^{a_1} e^{a_2}
    \,,
    \\
    G^s_7
    &=
    \tfrac{1}{7!}(G_7)_{a_1 \cdots a_7}\, e^{a_1}\cdots e^{a_7}
    +
    \tfrac{1}{5!}\big(\overline{\psi}\,\Gamma_{a_1 \cdots a_5}\psi\big)\, e^{a_1} \cdots e^{a_5}
    \,,
  \end{aligned}
  \qquad
  \begin{aligned}
    \mathrm{d}G^s_4 &= 0
    \,,
    \\
    \mathrm{d}G^s_7 &= \tfrac{1}{2} G^s_4 \wedge G^s_4
    \,,
  \end{aligned}
\]

*if and only if* the underlying fields solve the equations of motion of 11D supergravity (the C-field, Rarita-Schwinger and Einstein equations, with $G_7 = \star G_4$ implied), and the superfields are the unique rheonomic extension of their restriction to the bosonic body. (The sign convention for $G_7$ here is opposite to that of (eq:11dSugraBIAtOrder6).) In this formulation:

* The vanishing of the $(\overline{\psi}\kappa\psi)$-component of the gravitino field strength *follows* from imposing *both* flux Bianchi identities, instead of being obtained through a scaling condition. These supply the needed 2-index and 5-index constraints ([GSS24, Rem. 3.10](#GSS24)).

* Both directions of the equivalence are proven. The converse direction, that the Bianchi identities imply no constraints beyond the equations of motion, makes up the bulk of the work ([GSS24, footnote 13 and Conclusion](#GSS24)).

These are different choices of hypotheses and variables for the undeformed theory. The duality-symmetric theorem does not by itself settle the analogous equivalence for a deformed theory. Earlier indications of this formulation are in [Castellani, D'Auria & Fré 1991, §III.8.5](#CDF91) and [Candiello & Lechner 1994, §6](#CandielloLechner94); cf. [Howe & Tsimpis 2003, §5](#HoweTsimpis03).

**The flux superforms.** On the undeformed on-shell superspace, the purely spinorial component of the curvature is linear in the flux superfield $G_{abcd}$. In the conventions of [Souères & Tsimpis 2017, (E.1)](#SoueresTsimpis17),

\[
  \label{SpinorialCurvatureComponent}
  \mathcal{R}_{\alpha\beta\,ab}
  \;=\;
  \frac{\mathrm{i}}{6}\left(
  (\gamma^{cd})_{\alpha\beta}\, G_{abcd}
  +
  \frac{1}{24}(\gamma_{ab}{}^{cdef})_{\alpha\beta}\, G_{cdef}
  \right)
  \mathrlap{\,.}
\]

The super 4-form $\mathcal{G}_4$ has only the non-vanishing components

$$
  (\mathcal{G}_4)_{4,0} : \;\; G_{abcd}
  \,,
  \qquad
  (\mathcal{G}_4)_{2,2} : \;\; G_{ab\,\alpha\beta} = -\mathrm{i}(\gamma_{ab})_{\alpha\beta}
  \,,
$$

the latter being the term $\tfrac{1}{2}(\overline{\psi}\,\Gamma_{a_1a_2}\psi)e^{a_1}e^{a_2}$ in (eq:DualitySymmetricSuperFlux). The super 7-form $\mathcal{G}_7$ has only the non-vanishing components $(\mathcal{G}_7)_{7,0} = \star G_4$ and $(\mathcal{G}_7)_{5,2} \propto (\gamma_{a_1 \cdots a_5})_{\alpha\beta}$, and in the sign convention of (eq:11dSugraBIAtOrder6) they satisfy $\mathrm{d}\mathcal{G}_4 = 0$ and $\mathrm{d}\mathcal{G}_7 = -\tfrac{1}{2}\mathcal{G}_4 \wedge \mathcal{G}_4$ ([Howe & Tsimpis 2003, (10), (54)--(55)](#HoweTsimpis03), [Souères & Tsimpis 2017, (2.5)--(2.6)](#SoueresTsimpis17)). The components $(\mathcal{G}_4)_{p,4-p}$ have dimension $-1 + p/2$. The lowest one, the purely spinorial component $G_{\alpha\beta\gamma\delta} = (\mathcal{G}_4)_{0,4}$ of dimension $-1$, vanishes, as does $(\mathcal{G}_4)_{1,3}$. Similarly, all components of $\mathcal{G}_7$ with more than two spinorial indices vanish.

In the 4-form formulation, [Howe & Tsimpis 2003, §4](#HoweTsimpis03) show that the non-conventional constraint $G_{0,4}=0$, together with $\mathrm{d}\mathcal{G}_4=0$ and the conventional geometric constraints, leads back to ordinary supergravity. This uses the relation to the dimension-zero torsion and the geometric formulation just discussed. Consequently a nontrivial deformation of the local equations in this framework requires a nontrivial $G_{0,4}$, modulo the allowed field redefinitions. This statement is about constrained supergravity, not an arbitrary closed 4-form on a supermanifold.

**$\tau$-cohomology and spinorial cohomology.** With respect to the bigrading, the super exterior derivative decomposes as $\mathrm{d} = \mathrm{d}_b + \mathrm{d}_f + \tau + t$ of bidegrees $(1,0)$, $(0,1)$, $(-1,2)$ and $(2,-1)$, where $\tau$ is the purely algebraic operator given by contraction with the dimension-zero torsion,

$$
  (\tau\omega)_{a_1 \cdots a_{p-1}\,\beta_1 \cdots \beta_{q+2}}
  \;\propto\;
  T_{(\beta_1\beta_2}{}^c\, \omega_{c\, a_1 \cdots a_{p-1}\, \beta_3 \cdots \beta_{q+2})}
  \,,
$$

and $t$ is algebraic in the dimension-$3/2$ torsion ([Howe & Tsimpis 2003, (13)--(17)](#HoweTsimpis03), [Souères & Tsimpis 2017, (2.10)--(2.11)](#SoueresTsimpis17)). Since $\tau^2 = 0$, this defines the *$\tau$-cohomology* $H^{p,q}_\tau$. On it, $\mathrm{d}_f$ induces a nilpotent differential $\mathrm{d}_s[\omega] \coloneqq [\mathrm{d}_f \omega]$, whose cohomology is the *[[spinorial cohomology]]* $H^{p,q}_s$ (denoted $H^{p,q}_F$ in [Howe & Tsimpis 2003](#HoweTsimpis03), [Tsimpis 2004](#Tsimpis04)); one writes $H^{p,q}_s(\mathrm{phys})$ when the coefficients are required to be local tensorial functions of the physical fields. For the constraint (eq:UndeformedDimZeroTorsion), the groups $H^{0,q}_s$ are isomorphic to the [[pure spinor]] cohomology of [Berkovits 2002](#Berkovits02) ([Howe & Tsimpis 2003, §3 & App. D](#HoweTsimpis03), [Souères & Tsimpis 2017, §2.4](#SoueresTsimpis17)).

For the constraint (eq:UndeformedDimZeroTorsion), non-trivial $\tau$-cohomology arises only by means of the "M2-brane identity" $(\gamma^a)_{(\alpha\beta}(\gamma_{ab})_{\gamma\delta)} = 0$, and

$$
  H^{p,q}_\tau \;=\; 0
  \quad
  \text{for}\;\; p \geq 3
  \,.
$$

This was conjectured in [Howe & Tsimpis 2003, §5](#HoweTsimpis03) and subsequently proven ([Movshev, Schwarz & Xu 2011](#MovshevSchwarzXu11), [Brandt 2010-2013](#Brandt10)), as noted in [Souères & Tsimpis 2017, §2.2](#SoueresTsimpis17).


#### The superspace eight-form
 {#TheSuperspace8Form}

Applying the same [[invariant polynomial]] as in (eq:TheTerm) to the superspace curvature $\mathcal{R}$ defines the closed eight-[[differential form on a supermanifold|superform]]

\[
  \label{TheSuperspaceI8}
  \mathcal{I}_8(\mathcal{R})
  \;\coloneqq\;
  \frac{1}{48}
  \Big(
    p_2(\mathcal{R})
     -
   \tfrac{1}{4} 
   p_1(\mathcal{R}) \wedge p_1(\mathcal{R})
  \Big)
  \mathrlap{\,.}
\]

Here the $p_i(\mathcal{R})$ denote [[Chern-Weil theory|Chern-Weil]] superforms. The unnormalized $X_8$ of [Howe & Tsimpis 2003, (56)](#HoweTsimpis03) and [Souères & Tsimpis 2017, (4.2)](#SoueresTsimpis17) is the superform $\operatorname{tr}\mathcal{R}^4-\tfrac{1}{4}(\operatorname{tr}\mathcal{R}^2)^2=-192(2\pi)^4\mathcal{I}_8$ in the trace convention (eq:TheChernWeilForm) above. This construction is distinct from specifying the ordinary class $I_8(T X)$ or ordinary form $I_8(R)$.

**Pullback to the bosonic body.** For an inclusion $i \colon X \hookrightarrow \mathcal{M}$ of the bosonic body, naturality gives

\[
  i^*\mathcal{I}_8(\mathcal{R})
   \;=\;
  I_8(i^*\mathcal{R})
  \mathrlap{\,,}
\]

where $i^*\mathcal{R}$ is the curvature of the pulled-back spin connection, which depends also on the [[gravitino]]. In components: with $e^a \coloneqq E^a\vert$ and $\psi^\alpha \coloneqq E^\alpha\vert$ the vielbein and gravitino (evaluation at $\theta = 0$), the pullback of a superform receives contributions from *all* its components $(\mathcal{I}_8)_{p,q}$, each contracted with $p$ factors of $e$ and $q$ factors of $\psi$ ([Souères & Tsimpis 2017, (3.3)](#SoueresTsimpis17)). Only after setting the gravitino to zero does the pullback reduce to $(\mathcal{I}_8)_{8,0}\vert$, which on the undeformed bosonic background is $I_8(R)$ of the ordinary Riemann curvature. The subscript $q$ counts spinorial indices, not the degree of an ordinary differential form on $X$.

**The components.** The non-vanishing components $\mathcal{R}_{ab\,cd}$, $\mathcal{R}_{a\alpha\, cd}$, $\mathcal{R}_{\alpha\beta\, cd}$ of the curvature have dimensions $2$, $3/2$, $1$, respectively, so that the component $(\mathcal{I}_8)_{p,8-p}$ has dimension $4 + p/2$. The purely spinorial component $(\mathcal{I}_8)_{0,8}$ involves only $\mathcal{R}_{\alpha\beta\,cd}$, and hence by (eq:SpinorialCurvatureComponent) it is a homogeneous *quartic polynomial in the flux superfield* $G_{abcd}$, contracted with products of four $\gamma$-matrices ([Souères & Tsimpis 2017, §4.2 & (C.2)](#SoueresTsimpis17)). No gravitino field strength appears explicitly in this polynomial; this does not mean that the superfield has no fermionic components in its $\theta$-expansion. These component formulas use the undeformed constraints, as appropriate for the first-order source. This is the component through which the source term first enters the superspace Bianchi identities ([below](#EffectOfTheSourceOnSuperspaceGeometry)).

**The sourced Bianchi identities.** Writing the flux superforms as $\mathcal{G}_4$ and $\mathcal{G}_7$, the proposed superspace extension of (eq:11dSugraBIAtOrder6) is

\[
  \label{SuperspaceG7Bianchi}
  \begin{aligned}
  \mathrm{d}\mathcal{G}_4 
  &= 0
  \mathrlap{\,,}
  \\
  \mathrm{d}\mathcal{G}_7
  &=
  -\frac{1}{2}\mathcal{G}_4\wedge\mathcal{G}_4
    \,+\,
  \beta\, \mathcal{I}_8(\mathcal{R})
  \mathrlap{\,.}
  \end{aligned}
\]

The deformation problem is to solve these equations with local tensorial corrections built from the supergravity fields, retaining the same physical multiplet, modulo conventional choices and field redefinitions. They must hold in every $(p,q)$-component, compatibly with the geometric [[Bianchi identities]] and [[torsion constraints in supergravity|torsion constraints]]. The existence of the curvature superform $\mathcal{I}_8$ is not itself the open problem: the issue is finding the constrained supergravity deformation with this source.

Treating $\beta$ as a formal deformation parameter and writing

\[
 \begin{aligned}
   \mathcal{G}_4
   &=
   \mathcal{G}_4^{(0)}+\beta \mathcal{G}_4^{(1)}+\cdots,
   \\
   \mathcal{G}_7
   &=\mathcal{G}_7^{(0)}
    + \beta \mathcal{G}_7^{(1)}+\cdots
  \end{aligned}
\]

(and similarly for torsion and curvature), the first-order equations, written as expansions of differential forms on a fixed underlying supermanifold, read ([Souères & Tsimpis 2017, (4.5)](#SoueresTsimpis17))

\[
  \label{FirstOrderSourcedBianchi}
  \begin{aligned}
  \mathrm{d}\mathcal{G}_4^{(1)}
    &= 0
  \\
  \mathrm{d}\mathcal{G}_7^{(1)}
    & = 
  -\mathcal{G}_4^{(0)} \wedge \mathcal{G}_4^{(1)}
    +
  \mathcal{I}_8(\mathcal{R}^{(0)})
  \mathrlap{\,.}
  \end{aligned}
\]

Here $\mathcal{R}^{(0)}$ is the curvature of the undeformed supergravity superspace: since $\mathcal{I}_8$ already comes multiplied by $\beta$, the first-order correction to the curvature does not enter at this order. Closure of the right-hand side follows from $\mathrm{d}\mathcal{G}_4^{(0)} = \mathrm{d}\mathcal{G}_4^{(1)}  = \mathrm{d}\mathcal{I}_8 = 0$. 

However, $\mathcal{G}_4^{(1)}$ and $\mathcal{G}_7^{(1)}$ are not arbitrary forms: they belong to a deformation of the whole constrained superspace geometry. Closedness of a source is necessary, but does not guarantee a primitive in the required class of local tensorial expressions.

There is also a distinction between expanding differential forms and expanding their components in a moving super-coframe. If $E^A=E^{(0)A}+\beta E^{(1)A}+\cdots$, the latter expansion includes coframe corrections, and the component expressions for the exterior derivative change with the geometry. [Souères & Tsimpis 2017, (4.26)--(4.28)](#SoueresTsimpis17) discuss this distinction and their identification of the component fields on the body. The displayed form equations use the fixed exterior derivative $\mathrm{d}$; when converting them into frame components the coframe terms must be included.

#### Effect of the source term on the superspace geometry
 {#EffectOfTheSourceOnSuperspaceGeometry}

For flux superforms of the undeformed form (eq:DualitySymmetricSuperFlux), with components of at most two spinorial indices, the combination $\mathrm{d}\mathcal{G}_7 + \tfrac{1}{2}\mathcal{G}_4\wedge\mathcal{G}_4$ has components only with at most four spinorial indices. This holds whatever the torsion, since $\tau$ raises the number of spinorial indices by two. On-shell, all of these components vanish ([above](#UndeformedSugraOnSuperspace)).

The source can have components with five or more spinorial indices, including the generically nonzero $(\mathcal{I}_8)_{0,8}$. Thus the classical flux ansatz cannot solve the sourced identity for general fields. This is a statement about a universal deformation of the theory; some source components may vanish on special backgrounds, for example $(\mathcal{I}_8)_{0,8}$ when $G_{abcd}=0$.

The lowest sourced equation requires new components of $\mathcal{G}_7$. Identifying a nontrivial change of $\mathcal{G}_4$ and torsion requires the subsequent equations and the deformation cohomology; it does not follow from counting spinorial indices alone. The expectation that the full $I_8$ correction changes the torsion constraint is recorded in [Giotopoulos, Sati & Schreiber 2024, §2.1.7](#GSS24), following [CGNT 2004](#CGNT04). The two main parametrizations of such a deformation are as follows.

**1. In the geometric formulation**, by the dimension-zero torsion. Up to conventional constraints (field redefinitions of the supervielbein and connection), its most general form is ([Howe & Tsimpis 2003, (6)](#HoweTsimpis03), [CGNT 2004, (2.9)](#CGNT04))

\[
  \label{DeformedDimensionZeroTorsion}
  T_{\alpha\beta}{}^{c}
  \;=\;
  -\mathrm{i}(\gamma^c)_{\alpha\beta}
  +
  (\gamma^{d_1 d_2})_{\alpha\beta}\, X_{d_1 d_2}{}^c
  +
  (\gamma^{d_1\cdots d_5})_{\alpha\beta}\, Y_{d_1 \cdots d_5}{}^c
  \mathrlap{\,,}
\]

where $X$ and $Y$ are traceless with vanishing totally antisymmetric parts, hence in the $\mathrm{Spin}(1,10)$ representations $(11000)$ and $(10002)$, respectively, and of order $\beta$. Non-trivial first-order deformations correspond to a vector-valued spinorial cohomology with physical coefficients ([Howe & Tsimpis 2003, §3](#HoweTsimpis03)). [CGNT 2004, §3 & App. B](#CGNT04) analyze the torsion [[Bianchi identities]] to first order in general $X$, $Y$:

* At dimension $1/2$ the identities impose two constraints on $X, Y$ ([CGNT 2004, (3.1)](#CGNT04)); at dimension $1$ no further constraints arise ([CGNT 2004, (3.4)--(3.5)](#CGNT04)).

* All other components of the dimension-$1/2$ torsion are expressed through spinor derivatives of $X$, $Y$, except for a Weyl spinor which becomes of order $\beta$ (on simply connected spacetimes) and whose derivative is again fixed by $X$, $Y$; the Weyl curvature need not remain flat in the deformed theory ([CGNT 2004, (3.3)](#CGNT04)).

* Their Appendix B also treats equations at dimensions $3/2$ and $2$, and explains how to extract the corrected equations of motion once $X$, $Y$ are specified as functions of the physical fields. The required functions for the $I_8$ correction are not determined there.

**2. In the 4-form formulation**, by the purely spinorial component $G_{\alpha\beta\gamma\delta} = (\mathcal{G}_4)_{0,4}$ of the flux 4-form. In the presence of the 7-form identity, "the central role played by the dimension zero torsion is taken over by" this component ([CGNT 2004, §4](#CGNT04)):

* In the 4-form framework, the first-order class $[G^{(1)}_{0,4}]\in H^{0,4}_s(\mathrm{phys})$ encodes the deformation modulo the allowed redefinitions. Vanishing of the class gives a trivial deformation in this sense ([Howe & Tsimpis 2003, §4](#HoweTsimpis03)). The coefficient restriction $\mathrm{phys}$ is essential: these are local functions of the supergravity field strengths and their derivatives, not unrestricted superfields.

* Explicitly ([Howe & Tsimpis 2003, (69)--(70)](#HoweTsimpis03), [Tsimpis 2004, (4.2)--(4.4)](#Tsimpis04)), to first order, up to [[gauge transformations]] and field redefinitions,

  \[
    \label{G04Expansion}
    \begin{aligned}
    G_{\alpha\beta\gamma\delta}
    & =
    \tfrac{1}{8}
    (\gamma^{a_1 a_2})_{(\alpha\beta}(\gamma^{b_1 b_2})_{\gamma\delta)}\, A_{a_1 a_2;b_1 b_2}
    \\
    & \;\;
    +
    \tfrac{1}{240}
    (\gamma^{a_1 \cdots a_5})_{(\alpha\beta}(\gamma^{b_1 b_2})_{\gamma\delta)}\, B_{a_1 \cdots a_5;b_1 b_2}
    \\
    & \;\;
    +
    \tfrac{1}{28800}
    (\gamma^{a_1 \cdots a_5})_{(\alpha\beta}(\gamma^{b_1 \cdots b_5})_{\gamma\delta)}\, C_{a_1 \cdots a_5;b_1 \cdots b_5}
    \mathrlap{\,,}
    \end{aligned}
  \]

  with irreducible [[tensors]] $A$, $B$, $C$ in $(02000)$, $(01002)$, $(00004)$, subject to three differential constraints ([Howe & Tsimpis 2003, (83)](#HoweTsimpis03)).

  *Perturbative meaning.* At first order in the source parameter,

  \[
    \label{ExpansionOfG04ComponentsInBeta}
    A=\beta A^{(1)}+\mathcal{O}(\beta^2),
    \qquad B=\beta B^{(1)}+\mathcal{O}(\beta^2),
    \qquad C=\beta C^{(1)}+\mathcal{O}(\beta^2).
  \]

  This isolates the order-$\ell_p^6$ correction; the possible lower-order deformation is discussed [below](#TheOrderEll3Deformation). The coefficients are local tensorial functions of $G_{abcd}$, $T_{ab}{}^\alpha$, $R_{abcd}$ and their covariant derivatives, with the indicated representation projections. The three field strengths have mass dimensions $1$, $3/2$, $2$. Since $G_{0,4}$ has dimension $-1$ and $\beta$ has dimension $-6$, the first-order coefficients have dimension $5$ ([Tsimpis 2004, §4](#Tsimpis04)). They are evaluated using the undeformed superspace relations at this order.

  The three constraints of [Howe & Tsimpis 2003, (83)](#HoweTsimpis03) are first-order equations. At higher orders, derivatives, torsion, gauge identifications and lower-order corrections also contribute. The resulting equations are generally inhomogeneous; one cannot impose the same homogeneous constraints independently on every coefficient and thereby infer an extension. This concerns the deformation of the theory as local field equations, which is distinct from expanding a particular solution of those equations in $\beta$.

* Given an admissible $G^{(1)}_{0,4}$, the first-order 4-form [[Bianchi identities]] determine:

  1. $(\mathcal{G}_4)_{1,3}$ ([Howe & Tsimpis 2003, (82)](#HoweTsimpis03)), 

  1. the deformation tensors $X$ and $Y$ in (eq:DeformedDimensionZeroTorsion) as explicit linear combinations of derivatives of $A$, $B$, $C$ ([Howe & Tsimpis 2003, (87)--(88)](#HoweTsimpis03)), 

  1. the dimension-$1/2$ torsion and Weyl spinor, 

  1. and then systematically the remaining components of $\mathcal{G}_4$, of torsion and of curvature.

[Howe & Tsimpis 2003, §4 & §6](#HoweTsimpis03) give the low-dimensional reconstruction and describe the systematic continuation. This relates the 4-form and geometric approaches, but does not identify an arbitrary geometric deformation with a 4-form deformation: [CGNT 2004, §2.7 & §4](#CGNT04) explicitly leave open the existence of a suitable closed 4-form in the general deformed geometry and discuss differences between the two cohomological descriptions.

**3. The source.** In terms of the first-order equations (eq:FirstOrderSourcedBianchi), the components of lowest dimension of the sourced 7-form identity read, using $\mathcal{G}^{(0)}_{0,4} = \mathcal{G}^{(0)}_{1,3} = 0$:

\[
  \label{LowestComponentsOfSourcedBianchi}
  \begin{aligned}
    (0,8)\colon\;\;\;&
    \mathrm{d}_f \mathcal{G}^{(1)}_{0,7}
    +
    \tau \mathcal{G}^{(1)}_{1,6}
    \;=\;
    (\mathcal{I}_8)_{0,8}
    \,,
    \\
    (1,7)\colon\;\;\;&
    \mathrm{d}_b \mathcal{G}^{(1)}_{0,7}
    +
    \mathrm{d}_f \mathcal{G}^{(1)}_{1,6}
    +
    \tau \mathcal{G}^{(1)}_{2,5}
    \;=\;
    (\mathcal{I}_8)_{1,7}
    \,,
    \\
    (2,6)\colon\;\;\;&
    \mathrm{d}_b \mathcal{G}^{(1)}_{1,6}
    +
    \mathrm{d}_f \mathcal{G}^{(1)}_{2,5}
    +
    \tau \mathcal{G}^{(1)}_{3,4}
    +
    t\, \mathcal{G}^{(1)}_{0,7}
    \;=\;
    -\mathcal{G}^{(0)}_{2,2}\wedge \mathcal{G}^{(1)}_{0,4}
    +
    (\mathcal{I}_8)_{2,6}
    \,,
  \end{aligned}
\]

Here $\mathcal{G}^{(1)}_{p,q}$ on the left denotes the first-order frame component of the seven-form, while the $\mathcal{G}^{(1)}_{0,4}$ on the right belongs to the four-form. The operators $\mathrm{d}_b, \mathrm{d}_f, \tau, t$ are those of the undeformed geometry (variations of the component differential acting on the classical seven-form contribute only at higher vector degree, since its lowest nonzero component is $(5,2)$). The source is evaluated on the undeformed geometry. (The homogeneous version of the $(2,6)$-component is [Howe & Tsimpis 2003, (57)--(58)](#HoweTsimpis03).) From this:

* **The first condition is $\tau$-exactness.** Under the quarticity hypothesis used in [Howe & Tsimpis 2003](#HoweTsimpis03) and [Souères & Tsimpis 2017](#SoueresTsimpis17), the first-order seven-form is at least quartic in the physical field strengths. Then $\mathcal{G}^{(1)}_{0,7} = 0$ for dimensional reasons, and the $(0,8)$-component says that $(\mathcal{I}_8)_{0,8}$, a quartic polynomial in $G_{abcd}$ by the [above](#TheSuperspace8Form), must be $\tau$-exact, with $\mathcal{G}^{(1)}_{1,6}$ its primitive ([Howe & Tsimpis 2003, §5](#HoweTsimpis03), [Souères & Tsimpis 2017, (4.18)](#SoueresTsimpis17)).

* **Determining $G^{(1)}_{0,4}$.** This component first enters the displayed hierarchy at $(2,6)$, multiplied by the classical $(2,2)$ component of $\mathcal{G}_4$. Solving the sourced hierarchy is the proposed way to determine its spinorial cohomology class ([Howe & Tsimpis 2003, §5](#HoweTsimpis03)). A nontrivial deformation of the local field equations must give a nontrivial class in the 4-form framework. This is a conditional implication, not a computation of that class or a proof of solvability.

* **Uniqueness.** The possible ambiguities in solving (eq:SuperspaceG7Bianchi) at order $\beta$ lie in $H^{0,7}_s(\mathrm{phys})$, $H^{1,6}_s(\mathrm{phys})$ and $H^{2,5}_s(\mathrm{phys})$. [Howe & Tsimpis 2003, §5](#HoweTsimpis03) argue that these vanish at this order for deformations at least quartic in the fields, so that the solution, if it exists, is unique up to field redefinitions.

* **Duality is deformed.** $(\mathcal{G}_7)_{7,0}$ is no longer the Hodge dual of $(\mathcal{G}_4)_{4,0}$, and $\mathcal{G}_7$ is not the superspace dual of $\mathcal{G}_4$ ([Howe & Tsimpis 2003, §5](#HoweTsimpis03)).

The resulting research problem is to find a local solution of the coupled sourced identities and geometric constraints, and to extract the corrected fluxes, torsion and field equations. In particular, determining $G^{(1)}_{0,4}$ as a function of the physical fields would give the input for the 4-form reconstruction. Solving just the purely spinorial seven-form equation does not complete this task.

#### The superinvariant via the action principle
 {#ViaTheActionPrinciple}

[Souères & Tsimpis 2017](#SoueresTsimpis17) (see also [Howe & Tsimpis 2003, §5](#HoweTsimpis03), [Souères 2018](#Soueres18)) approach the corresponding first-order superinvariant through the superspace *action principle* ("ectoplasm"): a closed 11-superform $L_{11}$ gives an invariant by integration over the bosonic body. When the form is constructed using the classical on-shell constraints, invariance is understood modulo the classical equations of motion. This is the setting for a first-order action correction, not an off-shell or all-order construction. For a [[Chern-Simons form|Chern-Simons]] term $Z_{11}$ with closed 12-superform $W_{12} = \mathrm{d}Z_{11}$, this applies if $W_{12}$ is *Weil-trivial*: if it also has a [[gauge invariance|gauge-invariant]] primitive $K_{11}$ built locally and tensorially from the constrained on-shell superfields. Then $L_{11} \coloneqq Z_{11} - K_{11}$ is closed. Weil-triviality does not follow from the triviality of the de Rham cohomology of superspace, since it refers to the constrained (on-shell) superfields ([Souères & Tsimpis 2017, §2.1](#SoueresTsimpis17)).

* For undeformed supergravity, $W_{12} = -\tfrac{1}{6}G_4\wedge G_4\wedge G_4$ has $K_{11} = \tfrac{1}{3}G_4\wedge G_7$, giving an on-shell superform representative of the standard action ([Souères & Tsimpis 2017, (3.5)--(3.7) & App. A](#SoueresTsimpis17)).

* For the anomaly term, in the normalization of [Souères & Tsimpis 2017](#SoueresTsimpis17) (expansion in $\ell^6$, source $\ell^6 X_8$; see [above](#TheOrdinarySpacetimeForm)), $W^{(1)}_{12} = X_8 \wedge \mathcal{G}^{(0)}_4$ with $Z_{11} = X_8\wedge C_3^{(0)}$. *If* the first-order Bianchi identities (eq:FirstOrderSourcedBianchi) are solved, then $K_{11} = \mathcal{G}^{(1)}_7\wedge\mathcal{G}^{(0)}_4 - 2\,\mathcal{G}^{(0)}_7\wedge \mathcal{G}^{(1)}_4$, giving the superinvariant ([Souères & Tsimpis 2017, (4.6)--(4.8)](#SoueresTsimpis17))

  $$
    \Delta S
    \;=\;
    \ell^6
    \int
    \Big(
      X_8 \wedge C^{(0)}_3
      -
      G^{(1)}_7 \wedge G^{(0)}_4
      +
      2\, G^{(0)}_7 \wedge G^{(1)}_4
    \Big)
    \,.
  $$

The logical relations established in [Souères & Tsimpis 2017, §4.2](#SoueresTsimpis17) are:

1. If the sourced Bianchi identities have a solution which is at least quartic in the fields, then $X_{0,8} \propto (\mathcal{I}_8)_{0,8}$ is $\tau$-exact (as [above](#EffectOfTheSourceOnSuperspaceGeometry)).

1. Conversely, if $X_{0,8}$ is $\tau$-exact, then $W^{(1)}_{12}$ is Weil-trivial, hence the first-order superinvariant exists. The component $K_{3,8}$ is constructed from a $\tau$-primitive of $X_{0,8}$, of the type denoted $\mathcal{G}^{(1)}_{1,6}$ above ([Souères & Tsimpis 2017, (4.21)](#SoueresTsimpis17)), and all higher components exist by induction using $H^{p,q}_\tau = 0$ for $p \geq 3$.

1. Item 2 does not by itself show that the full sourced Bianchi system (eq:SuperspaceG7Bianchi) admits a solution; the explicit formula for $\Delta S$ above presupposes one.

**Status of $\tau$-exactness.** After Fierz rearrangement, $X_{0,8}$ can be organized by $\gamma$-matrix structures ([Souères & Tsimpis 2017, (4.24)](#SoueresTsimpis17)). All of them are $\tau$-exact except possibly those in the $\mathrm{Spin}(1,10)$ representations $(04000)$, $(03002)$ and $(02004)$. The authors show that the contributions in $(04000)$ and $(02004)$ cancel ([Souères & Tsimpis 2017, (4.25)](#SoueresTsimpis17)), and that these cancellations depend on the relative coefficient $-\tfrac{1}{4}$ in the trace polynomial $X_8=\operatorname{tr}\mathcal{R}^4-\tfrac{1}{4}(\operatorname{tr}\mathcal{R}^2)^2$: the purely spinorial components of $\operatorname{tr}\mathcal{R}^4$ and $(\operatorname{tr}\mathcal{R}^2)^2$ are not separately $\tau$-exact. The absence of $(03002)$ is left unchecked in that paper ([Souères & Tsimpis 2017, §5](#SoueresTsimpis17)). This is the outstanding step in that explicit sufficient-condition argument. Further computational work on the action-principle construction is described in [Souères 2018](#Soueres18).

**Counting superinvariants.** Provided the sourced Bianchi identities are solvable at order $\ell^6$, there are at least two independent superinvariants at eight derivatives: $\Delta S$ above, and one from $W'_{12} = \tfrac{1}{6}G_4\wedge G_4 \wedge G_4$ ([Souères & Tsimpis 2017, (4.12)--(4.15)](#SoueresTsimpis17)). The latter lacks the Chern-Simons term required for anomaly cancellation. If the 12-forms $G_4\wedge\operatorname{tr}R^4$ and $G_4 \wedge (\operatorname{tr}R^2)^2$ are separately Weil-trivial, the authors obtain at least three; any such separate supersymmetrizations must contain terms cubic or lower in the fields ([Souères & Tsimpis 2017, §4.1--4.2](#SoueresTsimpis17)).

**Uniqueness.** [Howe & Tsimpis 2003, §5](#HoweTsimpis03) argue for uniqueness of the anomaly superinvariant within the class that is at least quartic in the fields; [Souères & Tsimpis 2017](#SoueresTsimpis17) retain this qualification. The later proof of $H^{p,q}_\tau=0$ for $p\geq3$ supplies an algebraic ingredient of the argument. This should not be read as an unrestricted classification of all eight-derivative invariants, or as a proof that a particular sourced solution exists. Likewise, the ambiguity groups in the seven-form construction above are spinorial cohomology with physical coefficients; their analysis is not replaced simply by the vanishing of $H_\tau$ at high vector degree.

**Higher orders.** First-order supersymmetry does not ensure integrability at the next order ([Souères & Tsimpis 2017, §4.3](#SoueresTsimpis17)). In the 4-form deformation framework, [Howe & Tsimpis 2003, §7](#HoweTsimpis03) identify $H^{0,5}_s(\mathrm{phys})$ as the relevant obstruction group. Its role is different from that of the algebraic $\tau$-cohomology used to construct $K_{11}$.

For example, simply expanding (eq:SuperspaceG7Bianchi) one order further, with fixed exterior derivative as in (eq:FirstOrderSourcedBianchi), gives

\[
  \label{SecondOrderSourcedBianchi}
  \begin{aligned}
    \mathrm{d}\mathcal{G}^{(2)}_4 &=0,\\
    \mathrm{d}\mathcal{G}^{(2)}_7
    &=-\mathcal{G}^{(0)}_4\wedge\mathcal{G}^{(2)}_4
      -\tfrac{1}{2}\mathcal{G}^{(1)}_4\wedge\mathcal{G}^{(1)}_4
      +\mathcal{I}^{(1)}_8,
  \end{aligned}
\]

where $\mathcal{I}^{(1)}_8$ is the coefficient of $\beta$ in $\mathcal{I}_8(\mathcal{R}^{(0)}+\beta\mathcal{R}^{(1)}+\cdots)$. This displays why the problem depends on the first-order flux and geometry, not just on the undeformed polynomial $\mathcal{I}_8(\mathcal{R}^{(0)})$. Closedness of the second-order source does not establish its solvability with the required local superspace constraints.

If the sourced Bianchi identities are solvable to all orders, then
$\ell^6 X_8\wedge G_4-\tfrac{1}{2}G_4\wedge G_4\wedge G_4=\mathrm{d}(G_7\wedge G_4)$
is Weil-trivial to all orders. This is a conditional construction; the resulting invariant already differs from $\Delta S$ at order $\ell^6$ ([Souères & Tsimpis 2017, (4.31)--(4.32)](#SoueresTsimpis17)). An induction through the components of a fixed first-order superform, as above, is therefore distinct from an induction in the deformation parameter.

Moreover, a formal extension in powers of the coefficient $\beta$ tests the integrability of this particular deformation. It should not be identified with the entire M-theory derivative expansion, which may contain independent higher-derivative interactions.

#### What is known and what is open
 {#WhatIsKnownAndWhatIsOpen}

The status of the *local constrained superspace construction in the cited literature* can be summarized as follows.

* **The undeformed theory.** Its geometric and superform formulations are established, with their respective conventional constraints and local/global qualifications ([Howe 1997](#Howe97), [Giotopoulos, Sati & Schreiber 2024](#GSS24)). The latter gives a detailed equivalence theorem for the duality-symmetric flux formulation.

* **The deformation framework.** The first-order 4-form deformation is encoded by $[G^{(1)}_{0,4}]\in H^{0,4}_s(\mathrm{phys})$, with an explicit low-dimensional reconstruction ([Howe & Tsimpis 2003](#HoweTsimpis03)). The geometric approach determines torsion in terms of the deformation tensors $X,Y$ and explains how to obtain corrected dynamics from them ([CGNT 2004](#CGNT04)). Neither parametrization alone supplies the required local expressions for the $I_8$ source.

* **A sufficient condition for the first-order invariant.** $\tau$-exactness of $X_{0,8}$ implies Weil-triviality of $G^{(0)}_4\wedge X_8$, hence an on-shell first-order superinvariant. The high-vector-degree $\tau$-cohomology vanishing used in this construction has been proved. [Souères & Tsimpis 2017](#SoueresTsimpis17) verify the $(04000)$ and $(02004)$ cancellations, and explicitly leave the $(03002)$ calculation unresolved.

The remaining tasks in this programme are consequently distinct:

1. Complete the cited $\tau$-exactness calculation (or give another proof of the required Weil-triviality). The unperformed $(03002)$ check is a gap in that particular construction; it is not evidence that the anomaly interaction fails to have a supersymmetric completion.

1. Construct the $I_8$-sourced deformation as a local solution of the coupled flux and geometric Bianchi identities, including an explicit representative for $G^{(1)}_{0,4}$ and the resulting torsion and field equations. The action-principle argument for an invariant and the reconstruction of this full constrained geometry must not be conflated. The general comparison of geometric and 4-form/7-form descriptions also requires the qualifications discussed in [CGNT 2004, §2.7](#CGNT04).

1. Establish higher-order integrability, beginning with the inhomogeneous second-order problem (eq:SecondOrderSourcedBianchi). Neither the first-order reconstruction nor the high-vector-degree $\tau$-cohomology vanishing alone proves this. Uniqueness claims must retain the restrictions on field content, order and allowed redefinitions under which they were made.

The strong existence statement in the abstract of [Howe & Tsimpis 2003](#HoweTsimpis03) should be read together with the consistency premise and indirect argument in its §5, and the more explicit sufficient-condition analysis of [Souères & Tsimpis 2017, §4.2 & §5](#SoueresTsimpis17). The statements above describe what those constructions supply and leave to be supplied, rather than asserting the absence of every possible alternative existence argument.

There is also substantial progress in component sectors and amplitudes. For example, [Peeters, Vanhove & Westerberg 2000](#PVW00) analyze the anomaly-related $R^4$ sector before including gauge-field terms, while [Hyakutake 2025](#Hyakutake25) studies $(DF)^4$ terms and associated fermion bilinears. Such results constrain the completion, but their stated scope is narrower than a solution of all the sourced superspace identities. See also [[higher curvature corrections to D=11 supergravity -- references]].

Finally, local superspace consistency and global [[C-field flux quantization]] are different questions. A local solution must still be related to globally defined, quantized fields; ordinary characteristic-class and anomaly arguments do not by themselves solve the local superspace deformation problem, and local Bianchi calculations do not by themselves settle its global refinement.

#### The possible order-$\ell_p^3$ deformation
 {#TheOrderEll3Deformation}

[Tsimpis 2004](#Tsimpis04) computes $H^{0,4}_s(\mathrm{phys})$ up to order $\ell^3$:

* At orders $\ell$ and $\ell^2$ it vanishes, so there are no deformations at these orders within this local field-strength framework.

* At order $\ell^3$ it is one-dimensional, generated by a combination of the two $G^2$-terms in the $A$- and $B$-components of (eq:G04Expansion) ([Tsimpis 2004, (4.8)--(4.10)](#Tsimpis04)).

The generator is absorbed by the shift of the super 4-form $\mathcal{G}_4 \mapsto \mathcal{G}_4 - \tfrac{\beta' \ell^3}{4\pi}\operatorname{tr}\mathcal{R}^2$, which is locally a shift of the super 3-form potential by a Chern-Simons form ([Tsimpis 2004, (4.11)--(4.15)](#Tsimpis04)). Here $\beta'$ is an arbitrary real parameter, unrelated to $\beta$ above. The potential redefinition uses the connection through a Lorentz Chern-Simons form; it is not a redefinition by a gauge-invariant tensorial 3-form. Its local availability therefore does not contradict the nontriviality of the class with physical tensorial coefficients.

In the action principle, the corresponding superinvariant is $\int\big(C_3\wedge G_4 \wedge \operatorname{tr}R^2 + 2\,G_7\wedge \operatorname{tr}R^2\big)$, from $W_{12} = G_4\wedge G_4\wedge \operatorname{tr}R^2$ with $K_{11} = -2 G_7 \wedge \operatorname{tr}R^2$ ([Souères & Tsimpis 2017, §3.2 & App. B](#SoueresTsimpis17)). [Howe & Tsimpis 2003, §7](#HoweTsimpis03) note that an order-$\ell^3$ term $G_4\wedge\operatorname{tr}R^2$ on the right-hand side of the $G_7$ Bianchi identity is incompatible with five-brane anomaly cancellation.

The relation to shifting $G_4$ by a multiple of $\ell_p^3p_1(R)$ makes the global interpretation of this deformation sensitive to [[C-field flux quantization]]. In the local classical description it can be removed by a C-field redefinition involving a Lorentz Chern-Simons form; the global removal is discussed by Tsimpis for trivial first Pontryagin class. In the nontrivial case, removing it changes the flux quantization condition: $[G_{\beta'}/2\pi\ell^3] = [G/2\pi\ell^3] + \beta' p_1$ ([Tsimpis 2004, (4.17)--(4.18)](#Tsimpis04)). Tsimpis also notes the issue with the conventional parity transformation. The existence of this possible deformation does not fix a mandatory nonzero coefficient in the quantum M-theory action.

In particular, one cannot obtain a general corrected equation merely by appending a mixed $\ell_p^3G_4\wedge\lambda(R)$ term to (eq:11dSugraBIAtOrder6). Algebraically, a change of variables $\widetilde G_4=G_4+a\ell_p^3\lambda(R)$ gives

\[
  -\frac{1}{2}G_4\wedge G_4
  \;=\;
  -\frac{1}{2}\widetilde G_4\wedge\widetilde G_4
  +
  a\ell_p^3\widetilde G_4\wedge\lambda(R)
  -
  \frac{a^2\ell_p^6}{2}\lambda(R)\wedge\lambda(R)
  \mathrlap{\,.}
\]

Thus even this change of flux variable produces an additional order-$\ell_p^6$ curvature term. The coefficient, global flux convention and any further corrections have to be specified together.


### Inflow to M5-brane anomalies
  {#InflowToM5BraneAnomaly}

Consider an 11-dimensional [[spin structure|spin]]-[[manifold]] $X^{11}$ and a 2-parameter family of 6-dimensional [[submanifolds]] $Q_{M5}\hookrightarrow X^{11}$. When regarded as a family of [[worldvolumes]] of an [[M5-brane]], the family of [[normal bundles]] $N_X Q_{M5}$ of this inclusion carries a [[characteristic class]]

\[
  \label{IM5}
  I^{M5}
  \;\coloneqq\;
  I^{M5}_{\psi} + I_C
  \;\in\;
  H^8(F\times Q_{M5},\mathbb{Z})
  \mathrlap{\,,}
\]

where

1. the first summand is the class of the [[chiral anomaly]] of [[chiral fermions]] on $Q_{M5}$ ([Witten 96, (5.1)](#Witten96)),

2. the second term is the class of the [[quantum anomaly]] of a [[self-dual higher gauge field]] ([Witten 96, (5.4)](#Witten96)).

Moreover, there is the restriction of the $I_8$-term (eq:TheTerm) to $Q_{M5}$, hence to the [[tangent bundle]] of $X^{11}$ restricted to $Q_{M5}$ (the "anomaly inflow" from the [[bulk spacetime]] to the M5-brane)

\[
\label{I8AnomalyInflow}
I_8\vert_{M5}
\;\coloneqq\;
I_8\big(T_{Q_{M5}}X\big)
\;\in\;
H^8(F\times Q_{M5},\mathbb{Z}).
\]

The sum of these cohomology classes, evaluated on the [[fundamental class]] of $Q_{M5}$, is proportional to the [[second Pontryagin class]] of the [[normal bundle]]

\[
\label{SumOfM5AndInflowAnomalyIsp2}
I^{M5}+I_8\vert_{M5}
=\frac{1}{24}p_2(N_{Q_{M5}})
\]

([Witten 96, (5.7)](#Witten96)).

This result used to be "somewhat puzzling" ([Witten 96, p. 35](#Witten96)) since consistency of the [[M5-brane]] in [[M-theory]] should require its total [[quantum anomaly]] to vanish. But $p_2(N_{Q_{M5}})$ does not in general vanish, and the right conditions to require under which it does vanish were "not clear" ([Witten 96, p. 37](#Witten96)).

(For more details on the computations involved in this and the following arguments, see also [Bilal--Metzger 03](#BilalMetzger03).)

A resolution was proposed in [Freed--Harvey--Minasian--Moore 98](#FreedHarveyMinasianMoore98), see also [Bah--Bonetti--Minasian--Nardoni 18, (5)](#BahBonettiMinasianNardoni18), [BBMN 19, (2.9) and Appendices A.4, A.5](#BBMN19). By this proposal, the anomaly inflow from the bulk would not be just $I_8$, as in (eq:I8AnomalyInflow), but would be all of the following [[fiber integration]]

\[
\label{FiberIntegration}
\pi_*\left(-\frac{1}{6}G_4\wedge G_4\wedge G_4+G_4\wedge I_8\right)
=
-\frac{1}{24}p_2+\frac{1}{2}(G^{M5}_4)^2+I_8.
\]

Here we used [this Prop.](Spin5#FiberIntegrationOfCupPowersOfChiOver4Sphere) to find that

\[
\pi_*(\chi^3)=2p_2
\]

which would cancel against the first term $\tfrac{1}{24}p_2$ in (eq:FiberIntegration). Hence with this proposal, the remaining M5-brane anomaly (eq:SumOfM5AndInflowAnomalyIsp2) would be canceled -- except for a remaining term $\tfrac{1}{2}(G^{M5}_4)^2$ which is ignored by fiat.


### For $Spin(7)$- or $Sp(1)\cdot Sp(2)$-structure

If $X^8$ has

* [[Spin(7)-structure]] (hence in particular if it is a [[Calabi-Yau manifold]] of complex dimension four, which has $SU(4)=$ [[Spin(6)]]-structure)

or

* [[Sp(2).Sp(1)-structure]]

then

\[
\frac{1}{2}\left(p_2-\frac{1}{4}p_1^2\right)=\chi_8
\]

is the [[Euler class]] (see [this Prop.](Spin7-manifold#CharacteristicClassesForSpinStructure) and [this Prop.](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure), respectively), hence then

\[
  I_8=\frac{1}{24}\chi_8.
\]
\linebreak

## Related concepts

* [[Pontryagin classes]], [[Stiefel-Whitney classes]], [[Wu classes]], [[Euler class]]

* [[C-field tadpole cancellation]]

* [[spinorial cohomology]], [[pure spinor]], [[torsion constraints in supergravity]]

## References

### Ordinary characteristic class and spacetime coupling

The original one-loop coupling, flux quantization and eight-manifold compactifications:

* {#VafaWitten95} [[Cumrun Vafa]], [[Edward Witten]]: *A One-Loop Test of String Duality*, Nuclear Physics B **447** (1995) 261--270 &lbrack;[arXiv:hep-th/9505053](https://arxiv.org/abs/hep-th/9505053), [doi:10.1016/0550-3213(95)00280-6](https://doi.org/10.1016/0550-3213%2895%2900280-6)&rbrack;

* {#DuffLiuMinasian95} [[Mike Duff]], [[James Liu]], [[Ruben Minasian]], *Eleven Dimensional Origin of String/String Duality: A One Loop Test*, Nuclear Physics B **452** (1995) 261--282 &lbrack;[arXiv:hep-th/9506126](https://arxiv.org/abs/hep-th/9506126), [doi:10.1016/0550-3213(95)00368-3](https://doi.org/10.1016/0550-3213%2895%2900368-3)&rbrack;

* {#BeckerBecker96} [[Katrin Becker]], [[Melanie Becker]], *M-Theory on Eight-Manifolds*, Nuclear Physics B **477** (1996) 155--167 &lbrack;[arXiv:hep-th/9605053](https://arxiv.org/abs/hep-th/9605053), [doi:10.1016/0550-3213(96)00367-7](https://doi.org/10.1016/0550-3213%2896%2900367-7)&rbrack;

* {#WittenFluxQuantization96} [[Edward Witten]], *On Flux Quantization in M-Theory and the Effective Action*, Journal of Geometry and Physics **22** (1997) 1--13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), [doi:10.1016/S0393-0440(96)00042-3](https://doi.org/10.1016/S0393-0440%2896%2900042-3)&rbrack;

### Superspace extension and higher-curvature corrections

These papers analyze superforms, superspace constraints or the cohomology controlling their deformations. The superspace use of $I_8$ or $X_8$ is additional to the ordinary characteristic-class construction.

For the broader literature, see [[higher curvature corrections to D=11 supergravity -- references]].

The superspace formulation of undeformed 11D supergravity:

* {#CremmerFerrara80} [[Eugène Cremmer]], [[Sergio Ferrara]], *Formulation of Eleven-Dimensional Supergravity in Superspace*, Physics Letters B **91** 1 (1980) 61--66

* {#BrinkHowe80} [[Lars Brink]], [[Paul Howe]], *Eleven-Dimensional Supergravity on the Mass-Shell in Superspace*, Physics Letters B **91** 3--4 (1980) 384--386

* {#Howe97} [[Paul Howe]], *Weyl Superspace*, Physics Letters B **415** (1997) 149--155 &lbrack;[arXiv:hep-th/9707184](https://arxiv.org/abs/hep-th/9707184)&rbrack;
  > Derives the on-shell theory from the standard dimension-zero torsion in Weyl superspace; the flat scale connection is removable locally, with a separate global qualification.

* {#CDF91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], *Supergravity and Superstrings -- A Geometric Perspective*, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224)&rbrack;
  > §III.8: 11D supergravity in superspace (rheonomy), including the duality-symmetric 4-form/7-form formulation (§III.8.5).

* {#CandielloLechner94} Antonio Candiello, [[Kurt Lechner]]: *Duality in supergravity theories*, Nuclear Physics B **412** (1994) 479--501 &lbrack;[arXiv:hep-th/9309143](https://arxiv.org/abs/hep-th/9309143), [doi:10.1016/0550-3213(94)90389-1](https://doi.org/10.1016/0550-3213%2894%2990389-1)&rbrack;

* {#GSS24} [[Grigorios Giotopoulos]], [[Hisham Sati]], [[Urs Schreiber]], *Flux Quantization on 11-dimensional Superspace*, JHEP **07** (2024) 082 &lbrack;[arXiv:2403.16456](https://arxiv.org/abs/2403.16456), [doi:10.1007/JHEP07(2024)082](https://doi.org/10.1007/JHEP07%282024%29082)&rbrack;
  > Thm. 3.1: on a super-spacetime satisfying the bosonic torsion constraint, the duality-symmetric super-flux Bianchi identities for $(G^s_4, G^s_7)$ are equivalent to the equations of motion of 11D supergravity, proven in detail with computer algebra checks; §2.1.7 on the $I_8$-correction as expected to require relaxing the torsion constraint.

Spinorial and pure spinor cohomology:

* {#CNT02} [[Martin Cederwall]], [[Bengt Nilsson]], [[Dimitrios Tsimpis]], *Spinorial cohomology and maximally supersymmetric theories*, JHEP **02** (2002) 009 &lbrack;[arXiv:hep-th/0110069](https://arxiv.org/abs/hep-th/0110069), [doi:10.1088/1126-6708/2002/02/009](https://doi.org/10.1088/1126-6708/2002/02/009)&rbrack;
  > Linearized cohomology tables for 11D supergravity with respect to the super-vielbein and to the super 3-form; observes that deformations force the super 4-form to have non-vanishing components of negative dimension.

* {#Berkovits02} [[Nathan Berkovits]]: *Towards covariant quantization of the supermembrane*, JHEP **09** (2002) 051 &lbrack;[arXiv:hep-th/0201151](https://arxiv.org/abs/hep-th/0201151)&rbrack;

The vanishing of $\tau$-cohomology $H^{p,q}_\tau$ for $p \geq 3$, conjectured in [Howe & Tsimpis 2003](#HoweTsimpis03):

* {#MovshevSchwarzXu11} [[Michael Movshev]], [[Albert Schwarz]], [[Renjun Xu]]: *Homology of Lie algebra of supersymmetries and of super Poincaré Lie algebra*, Nuclear Physics B **854** (2012) 483--503 &lbrack;[arXiv:1106.0335](https://arxiv.org/abs/1106.0335), [doi:10.1016/j.nuclphysb.2011.08.023](https://doi.org/10.1016/j.nuclphysb.2011.08.023)&rbrack;

* {#Brandt10} [[Friedemann Brandt]], *Supersymmetry algebra cohomology* I--IV, Journal of Mathematical Physics **51** (2010) 122302 &lbrack;[arXiv:0911.2118](https://arxiv.org/abs/0911.2118)&rbrack;, **51** (2010) 112303 &lbrack;[arXiv:1004.2978](https://arxiv.org/abs/1004.2978)&rbrack;, **52** (2011) 052301 &lbrack;[arXiv:1005.2102](https://arxiv.org/abs/1005.2102)&rbrack;, **54** (2013) 052302 &lbrack;[arXiv:1303.6211](https://arxiv.org/abs/1303.6211)&rbrack;

The deformation theory:

* {#HoweTsimpis03} [[Paul Howe]], [[Dimitrios Tsimpis]], *On higher-order corrections in M theory*, JHEP **09** (2003) 038 &lbrack;[arXiv:hep-th/0305129](https://arxiv.org/abs/hep-th/0305129), [doi:10.1088/1126-6708/2003/09/038](https://doi.org/10.1088/1126-6708/2003/09/038)&rbrack;
  > §3: spinorial cohomology; §4: deformations of the 4-form theory are parametrized by $G_{\alpha\beta\gamma\delta}$; §5: the $X_8$-sourced seven-form Bianchi identity, the action principle and the (conditional) uniqueness argument; §6: explicit dimension $-1/2$ and dimension-zero solution, expressing the torsion deformation through $G_{\alpha\beta\gamma\delta}$.

* {#Tsimpis04} [[Dimitrios Tsimpis]], *11D supergravity at $\mathcal{O}(\ell^3)$*, JHEP **10** (2004) 046 &lbrack;[arXiv:hep-th/0407271](https://arxiv.org/abs/hep-th/0407271), [doi:10.1088/1126-6708/2004/10/046](https://doi.org/10.1088/1126-6708/2004/10/046)&rbrack;
  > $H^{0,4}_s(\mathrm{phys})$ vanishes at orders $\ell$, $\ell^2$, and is one-dimensional at order $\ell^3$, where it is generated by a shift of $G_4$ by $\operatorname{tr}R^2$.

* {#CGNT04} [[Martin Cederwall]], [[Ulf Gran]], [[Bengt Nilsson]], [[Dimitrios Tsimpis]], *Supersymmetric Corrections to Eleven-Dimensional Supergravity*, JHEP **05** (2005) 052 &lbrack;[arXiv:hep-th/0409107](https://arxiv.org/abs/hep-th/0409107), [doi:10.1088/1126-6708/2005/05/052](https://doi.org/10.1088/1126-6708/2005/05/052)&rbrack;
  > First-order analysis of a general dimension-zero torsion deformation, with the dimension-1/2 and dimension-1 constraints and a route to the corrected equations; comparison of geometric and 4-form formulations (§2.7).

* {#SoueresTsimpis17} [[Bertrand Souères]], [[Dimitrios Tsimpis]], *The action principle and the supersymmetrisation of Chern-Simons terms in eleven-dimensional supergravity*, Physical Review D **95** 2 (2017) 026013 &lbrack;[arXiv:1612.02021](https://arxiv.org/abs/1612.02021), [doi:10.1103/PhysRevD.95.026013](https://doi.org/10.1103/PhysRevD.95.026013)&rbrack;
  > Sections 4--5 and Appendix C: the anomaly superinvariant, reduction of its existence to $\tau$-exactness of $X_{0,8}$, the verified $(04000)$ and $(02004)$ cancellations and the remaining $(03002)$ check, and conditional integrability results.

* {#Soueres18} [[Bertrand Souères]], *Supergravities in Superspace*, doctoral thesis, Lyon (2018) &lbrack;[tel:01998725](https://theses.hal.science/tel-01998725), [pdf](https://theses.hal.science/tel-01998725/document)&rbrack;
  > Further development of the superspace action-principle approach and its computational tools.

Examples of complementary component calculations:

* {#PVW00} [[Kasper Peeters]], [[Pierre Vanhove]], Anders Westerberg: *Supersymmetric $R^4$ actions and quantum corrections to superspace torsion constraints* (2000) &lbrack;[arXiv:hep-th/0010182](https://arxiv.org/abs/hep-th/0010182)&rbrack;
  > Summarizes results for the gravitational sector before inclusion of gauge-field terms.

* {#Hyakutake25} [[Yoshifumi Hyakutake]], *Effective Action in M-Theory: $(DF)^4$ Superinvariants* (2025) &lbrack;[arXiv:2507.14984](https://arxiv.org/abs/2507.14984)&rbrack;
  > Local supersymmetry analysis of the $(DF)^4$ sector and associated fermion bilinears.


An [LLM generated](machine+learning#CouplingProofAssistantsWithMachineLearningReferences) [[proof]] of existence of [[higher curvature corrections|higher curvature corrected]] [[superspace]] [[11D supergravity]], so far to second order in the [[I8|$I_8$]]-deformation of the [[supergravity C-field|$G_7$]]-[[Bianchi identity]]:

* {#ExistenceOfCurvatureCorrected11DSuGra} [[nLab materials]]: *Existence Proof of Curvature Corrected 11D Superspace Supergravity* (2026-11-07) \[<a href="https://www.dropbox.com/scl/fo/weluevnfxeyn4fhl0ou8n/ADq5grV2u3xYry6Z_2Nlt6g?rlkey=z75tlj3hejfu5yzmnu1qec6ss&dl=0">db</a>\]


### Ordinary anomaly polynomials and M5-brane inflow

These references concern worldvolume anomalies and bulk inflow, including their global refinements, rather than a solution of the eleven-dimensional superspace deformation problem.

* {#Witten96} [[Edward Witten]], *Five-Brane Effective Action in M-Theory*, Journal of Geometry and Physics **22** 2 (1997) 103--133 &lbrack;[arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234), [doi:10.1016/S0393-0440(97)80160-X](https://doi.org/10.1016/S0393-0440%2897%2980160-X)&rbrack;

* {#FreedHarveyMinasianMoore98} [[Daniel Freed]], [[Jeffrey Harvey]], [[Ruben Minasian]], [[Gregory Moore]], *Gravitational Anomaly Cancellation for M-Theory Fivebranes*, Advances in Theoretical and Mathematical Physics **2** 3 (1998) 601--618 &lbrack;[arXiv:hep-th/9803205](https://arxiv.org/abs/hep-th/9803205), [doi:10.4310/ATMP.1998.v2.n3.a8](https://doi.org/10.4310/ATMP.1998.v2.n3.a8)&rbrack;

* {#HarveyMinasianMoore98b} [[Jeffrey Harvey]], [[Ruben Minasian]], [[Gregory Moore]], *Non-abelian Tensor-multiplet Anomalies*, JHEP **09** (1998) 004 &lbrack;[arXiv:hep-th/9808060](https://arxiv.org/abs/hep-th/9808060), [doi:10.1088/1126-6708/1998/09/004](https://doi.org/10.1088/1126-6708/1998/09/004)&rbrack;

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger: *Anomaly cancellation in M-theory: a critical review*, Nuclear Physics B **675** (2003) 416--446 &lbrack;[arXiv:hep-th/0307152](https://arxiv.org/abs/hep-th/0307152), [doi:10.1016/j.nuclphysb.2003.10.002](https://doi.org/10.1016/j.nuclphysb.2003.10.002)&rbrack;

* {#BahBonettiMinasianNardoni18} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], [[Emily Nardoni]], *Class $\mathcal{S}$ Anomalies from M-theory Inflow*, Physical Review D **99** 8 (2019) 086020 &lbrack;[arXiv:1812.04016](https://arxiv.org/abs/1812.04016), [doi:10.1103/PhysRevD.99.086020](https://doi.org/10.1103/PhysRevD.99.086020)&rbrack;

{#BBMN19}

* {#BahBonettiMinasianNardoni19} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], [[Emily Nardoni]], *Anomaly Inflow for M5-branes on Punctured Riemann Surfaces*, JHEP **06** (2019) 123 &lbrack;[arXiv:1904.07250](https://arxiv.org/abs/1904.07250), [doi:10.1007/JHEP06(2019)123](https://doi.org/10.1007/JHEP06%282019%29123)&rbrack;

### Global and topological formulations

On characteristic classes, quantized charges and their refinements:

* {#DiaconescuFreedMoore03} [[Duiliu-Emanuel Diaconescu]], [[Daniel Freed]], [[Gregory Moore]]: *The M-theory 3-form and $E_8$ gauge theory*, in *Elliptic Cohomology: Geometry, Applications, and Higher Chromatic Analogues*, Cambridge University Press (2007) 44--88 &lbrack;[arXiv:hep-th/0312069](https://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489.005](https://doi.org/10.1017/CBO9780511721489.005)&rbrack;

* {#Sati10} [[Hisham Sati]], *Geometric and topological structures related to M-branes*, Proceedings of Symposia in Pure Mathematics **81** (2010) 181--236 &lbrack;[arXiv:1001.5020](https://arxiv.org/abs/1001.5020)&rbrack;

* {#Sati11a} [[Hisham Sati]], *Geometric and topological structures related to M-branes II: Twisted String and String$^c$ structures*, Journal of the Australian Mathematical Society **90** 1 (2011) 93--108 &lbrack;[arXiv:1007.5419](https://arxiv.org/abs/1007.5419), [doi:10.1017/S1446788711001261](https://doi.org/10.1017/S1446788711001261)&rbrack;

* {#Sati11b} [[Hisham Sati]], *Twisted topological structures related to M-branes*, International Journal of Geometric Methods in Modern Physics **8** 5 (2011) 1097--1116 &lbrack;[arXiv:1008.1755](https://arxiv.org/abs/1008.1755), [doi:10.1142/S0219887811005567](https://doi.org/10.1142/S0219887811005567)&rbrack;

[[!redirects one-loop anomaly polynomial I8]]
