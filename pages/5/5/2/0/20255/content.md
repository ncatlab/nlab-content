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

In the [[string theory]] and [[M-theory]] literature, $I_8$ denotes the degree-eight [[rational cohomology|rational]] [[characteristic class]]

\[
  \label{TheTerm}
  I_8(E)
  \;\coloneqq\;
  \frac{1}{48}\left(p_2(E)-\frac{1}{4}p_1(E)^2\right)
  \;\in\; H^8(X;\mathbb{Q})
\]

of a real [[vector bundle]] $E\to X$, usually the [[tangent bundle]] of spacetime. Here $p_i$ are the [[Pontryagin classes]] and multiplication denotes the [[cup product]]. For a [[spin structure|spin]] bundle, $\lambda(E)\coloneqq\tfrac{1}{2} p_1(E)$ is the [[first fractional Pontryagin class]], so that $I_8=\tfrac{1}{48}(p_2-\lambda^2)$. Although $\lambda$ is integral on spin bundles, $I_8$ need not be integral.

The same notation denotes the ordinary closed differential eight-form $I_8(R)\in\Omega^8(X)$ obtained by [[Chern-Weil theory]] from a [[affine connection|connection]] with [[curvature]] $R$. These are two related objects on ordinary spacetime: a rational characteristic class and its differential-form representative. The characteristic class describes topological constraints, whereas the ordinary form enters local [[effective actions]] and [[equations of motion]]. The notation $X_8$ is also common, but its sign and normalization vary. With the usual real-vector trace convention,

\[
  I_8(R)
  =
  -\frac{1}{192}(2\pi)^4
  \left(
    \operatorname{tr}(R^4)
    -
    \frac{1}{4}
   \big(\operatorname{tr}(R^2)\big)^2
  \right).
\]

Thus a frequently used convention for $X_8$ gives $X_8=-I_8$; other authors omit the overall numerical factor. Wedge products are implicit in this curvature formula.

Physically, this polynomial governs the gravitational coupling $B_2\wedge I_8$ in [[type IIA string theory]] and its eleven-dimensional counterpart $C_3\wedge I_8$, where $C_3$ is the [[supergravity C-field]]. It contributes to [[M5-brane]] [[anomaly inflow]], to the corrected equation for the dual seven-form flux, and to [[C-field tadpole cancellation]] in compactifications on eight-manifolds. It is often called the *one-loop anomaly term*. It should not be identified with the entire M5-brane anomaly polynomial, which also depends on the [[normal bundle]].

Historically, the type IIA one-loop coupling was studied by [Vafa--Witten](#VafaWitten95), and its eleven-dimensional interpretation by [Duff--Liu--Minasian](#DuffLiuMinasian95). [Becker--Becker](#BeckerBecker96) used the correction in compactifications on eight-manifolds. Witten subsequently analyzed both [shifted C-field flux quantization](#WittenFluxQuantization96) and the [five-brane effective action](#Witten96). [Freed--Harvey--Minasian--Moore](#FreedHarveyMinasianMoore98) established the role of the bulk Chern-Simons interaction in cancellation of the remaining normal-bundle anomaly. Later developments include the [integral electric C-field charge](#DiaconescuFreedMoore03), [global five-brane anomalies](#Monnier15), and [inflow computations for wrapped M5-branes](#BBMN19).

The original one-loop, flux-quantization and anomaly-inflow articles cited above concern this ordinary (bosonic) form or characteristic class; they do not thereby construct its superspace completion. A separate question is how the curvature coupling extends to a locally [[supersymmetry|supersymmetric]] interaction, including flux and fermion terms. The [[superspace]] approach of [Howe--Tsimpis](#HoweTsimpis03) and [Souères--Tsimpis](#SoueresTsimpis17) instead uses an eight-superform, written $\mathcal{I}_8(\mathcal{R})$ below, built from the superspace Lorentz curvature $\mathcal{R}$. Its components with odd tangent indices enter a deformation problem not present in the ordinary bosonic equation. Its conditional existence results and remaining cohomological checks are discussed [below](#AsHigherCurvatureCorrectionTo11dSugra).

\linebreak

## Properties


### As a higher curvature correction to 11-dimensional supergravity
  {#AsHigherCurvatureCorrectionTo11dSugra}

#### The ordinary spacetime form and corrected flux equation

The coupling $C_3\wedge I_8(R)$ belongs to the eight-derivative sector of the [[M-theory]] effective action, at order $\ell_p^6$ relative to the two-derivative action of [[D=11 supergravity]]. Its gravitational supersymmetry partners include terms schematically of the form $R^4$; a full completion also involves the four-form flux and fermions. For the different approaches to these corrections, see [[higher curvature corrections to D=11 supergravity -- references]].

On ordinary eleven-dimensional spacetime, away from magnetic sources, the bosonic anomaly-corrected flux equations are conventionally organized as

\[
\label{11dSugraBIAtOrder6}
\begin{aligned}
dG_4 &=0,\\
dG_7 &=-\frac{1}{2}G_4\wedge G_4+\beta I_8(R),
\end{aligned}
\]

through the order under consideration, where $\beta$ is proportional to $\ell_p^6$. Its numerical factor and sign depend on conventions for the fluxes and action; the normalization of $I_8$ here remains that of (eq:TheTerm). Reversing the convention for $G_7$ reverses both terms on the right. The corresponding superspace equation is discussed separately below.

On ordinary spacetime the second equation packages the corrected C-field equation of motion. The relation between $G_7$ and $\star G_4$ itself receives corrections, so imposing $G_7=\star G_4$ without qualification would omit part of the dynamics.

#### The superspace eight-form and Bianchi identities

Let $\mathcal{M}^{11|32}$ be the supergravity [[superspace]], with Lorentz superconnection and curvature $\mathcal{R}$. Applying the same invariant polynomial defines the closed eight-superform

\[
\mathcal{I}_8(\mathcal{R})
\;\coloneqq\;
\frac{1}{48}\left(p_2(\mathcal{R})-\frac{1}{4} p_1(\mathcal{R})\wedge p_1(\mathcal{R})\right).
\]

Here the $p_i(\mathcal{R})$ denote Chern-Weil superforms. The unnormalized $X_8$ of [Souères--Tsimpis, (4.1)--(4.3)](#SoueresTsimpis17) is the superform $\operatorname{tr}\mathcal{R}^4-\tfrac{1}{4}(\operatorname{tr}\mathcal{R}^2)^2=-192(2\pi)^4\mathcal{I}_8$ in the trace convention above. This construction is distinct from specifying the ordinary class $I_8(TX)$ or ordinary form $I_8(R)$. For an inclusion $i:X\hookrightarrow\mathcal{M}$ of the bosonic body, naturality gives

\[
i^*\mathcal{I}_8(\mathcal{R})=I_8(i^*\mathcal{R}).
\]

In the bosonic truncation this recovers the ordinary spacetime curvature expression. But the pullback does not retain all components of the superform: its decomposition $\mathcal{I}_8=\sum_{p+q=8}(\mathcal{I}_8)_{p,q}$ also includes components with $q$ odd tangent indices. The subscript $q$ counts spinorial indices, not the degree of an ordinary differential form on $X$.

Writing the flux superforms as $\mathcal{G}_4$ and $\mathcal{G}_7$, the proposed superspace extension is

\[
d\mathcal{G}_4=0,
\qquad
d\mathcal{G}_7=-\frac{1}{2}\mathcal{G}_4\wedge\mathcal{G}_4+\beta\mathcal{I}_8(\mathcal{R}).
\]

These equations must hold in every even/odd component, compatibly with the geometric [[Bianchi identities]] and [[torsion constraints in supergravity|torsion constraints]]. The existence of the curvature superform $\mathcal{I}_8$ is not itself the open problem: the issue is finding the constrained supergravity deformation with this source.

For example, treating $\beta$ as the deformation parameter and writing

\[
\mathcal{G}_4=\mathcal{G}_4^{(0)}+\beta \mathcal{G}_4^{(1)}+\cdots,
\qquad
\mathcal{G}_7=\mathcal{G}_7^{(0)}+\beta \mathcal{G}_7^{(1)}+\cdots,
\]

the first-order equations read

\[
d\mathcal{G}_4^{(1)}=0,
\qquad
d\mathcal{G}_7^{(1)}=-\mathcal{G}_4^{(0)}\wedge \mathcal{G}_4^{(1)}+\mathcal{I}_8(\mathcal{R}^{(0)}).
\]

Closure of the right-hand side follows from $d\mathcal{G}_4^{(0)}=d\mathcal{G}_4^{(1)}=d\mathcal{I}_8=0$. This necessary consistency check does not establish a solution by covariant local superfields satisfying the superspace constraints. An unrestricted local primitive supplied by the Poincaré lemma is insufficient for that purpose.

#### Superspace deformation theory and the action principle

[Howe--Tsimpis](#HoweTsimpis03) describe deformations using spinorial cohomology, in particular the four-form component with four spinorial indices. They analyze the anomaly-modified seven-form identity and reconstruct low-dimensional superspace data. The geometric analysis of [Cederwall--Gran--Nilsson--Tsimpis](#CGNT04) solves the torsion Bianchi identities to first order in a general dimension-zero torsion deformation; specifying the deformation sourced by $\mathcal{I}_8$ remains an additional task.

[Souères--Tsimpis, Sections 4--5 and Appendix C](#SoueresTsimpis17) develop the superform action principle. A closed twelve-superform $W_{12}$ admits an action construction when it is *Weil-trivial*: besides a Chern-Simons primitive $Z_{11}$, it has a gauge-invariant primitive $K_{11}$, giving the closed Lagrangian superform $K_{11}-Z_{11}$.

For the anomaly correction, a sufficient cohomological condition for the first-order construction is $\tau$-exactness of $X_{0,8}$. This is the purely spinorial component of the curvature eight-superform denoted $X_8$ in that paper, proportional to $(\mathcal{I}_8)_{0,8}$ in the notation here; it is not a component of the ordinary bosonic form $I_8(R)$. Here $\tau$ is the algebraic differential induced by the leading dimension-zero torsion. The authors reduce the possible obstruction to the $\mathrm{Spin}(1,10)$ representations $(04000)$, $(03002)$ and $(02004)$, and verify cancellation of the first and third. The $(03002)$ cancellation is left unchecked. The verified cancellations depend on the relative coefficient $-\tfrac{1}{4}$ in this curvature superform.

Their classification assumes perturbative solvability of the superspace Bianchi identities; their uniqueness statement assumes an invariant starting at fourth order in fields. Integrability to higher orders has further conditions. Consequently these results do not constitute an unconditional existence proof for the complete anomaly-deformed superspace system.

The distinction is between a first-order action invariant, a solution of all constrained superspace Bianchi identities, and extension to higher perturbative orders. The cited superspace work supports the expected completion but does not settle all three questions. Results in selected component sectors or scattering amplitudes do not by themselves fill this gap; see the [[higher curvature corrections to D=11 supergravity -- references#I8SuperspaceDeformation|references on the superspace deformation problem]] and the surrounding bibliography.

#### The possible order-$\ell_p^3$ deformation

The order-$\ell_p^3$ class studied by [Tsimpis](#Tsimpis04) requires a separate qualification. Its relation to shifting $G_4$ by a multiple of $\ell_p^3p_1(R)$ makes its global interpretation sensitive to [[C-field flux quantization]]. On backgrounds with trivial first Pontryagin class it can be removed by a C-field redefinition; in the nontrivial case removing it changes the flux quantization condition. Its existence as a possible supersymmetric deformation does not fix a mandatory nonzero coefficient in the quantum M-theory action.

In particular, one cannot obtain a general corrected equation merely by appending a mixed $\ell_p^3G_4\wedge\lambda(R)$ term to (eq:11dSugraBIAtOrder6). Algebraically, a change of variables $\widetilde G_4=G_4+a\ell_p^3\lambda(R)$ gives

\[
-\frac{1}{2}G_4\wedge G_4
=
-\frac{1}{2}\widetilde G_4\wedge\widetilde G_4
+a\ell_p^3\widetilde G_4\wedge\lambda(R)
-\frac{a^2\ell_p^6}{2}\lambda(R)\wedge\lambda(R).
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

## References

### Ordinary characteristic class and spacetime coupling

The original one-loop coupling, flux quantization and eight-manifold compactifications:

* {#VafaWitten95} [[Cumrun Vafa]], [[Edward Witten]], *A One-Loop Test of String Duality*, Nuclear Physics B **447** (1995) 261--270 &lbrack;[arXiv:hep-th/9505053](https://arxiv.org/abs/hep-th/9505053), [doi:10.1016/0550-3213(95)00280-6](https://doi.org/10.1016/0550-3213%2895%2900280-6)&rbrack;

* {#DuffLiuMinasian95} [[Mike Duff]], [[James Liu]], [[Ruben Minasian]], *Eleven Dimensional Origin of String/String Duality: A One Loop Test*, Nuclear Physics B **452** (1995) 261--282 &lbrack;[arXiv:hep-th/9506126](https://arxiv.org/abs/hep-th/9506126), [doi:10.1016/0550-3213(95)00368-3](https://doi.org/10.1016/0550-3213%2895%2900368-3)&rbrack;

* {#BeckerBecker96} [[Katrin Becker]], [[Melanie Becker]], *M-Theory on Eight-Manifolds*, Nuclear Physics B **477** (1996) 155--167 &lbrack;[arXiv:hep-th/9605053](https://arxiv.org/abs/hep-th/9605053), [doi:10.1016/0550-3213(96)00367-7](https://doi.org/10.1016/0550-3213%2896%2900367-7)&rbrack;

* {#WittenFluxQuantization96} [[Edward Witten]], *On Flux Quantization in M-Theory and the Effective Action*, Journal of Geometry and Physics **22** (1997) 1--13 &lbrack;[arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122), [doi:10.1016/S0393-0440(96)00042-3](https://doi.org/10.1016/S0393-0440%2896%2900042-3)&rbrack;

### Superspace extension and higher-curvature corrections

These papers analyze superforms, superspace constraints or the cohomology controlling their deformations. The superspace use of $I_8$ or $X_8$ is additional to the ordinary characteristic-class construction.

For the broader literature, see [[higher curvature corrections to D=11 supergravity -- references]].

* {#CNT02} [[Martin Cederwall]], [[Bengt Nilsson]], [[Dimitrios Tsimpis]], *Spinorial cohomology and maximally supersymmetric theories*, JHEP **02** (2002) 009 &lbrack;[arXiv:hep-th/0110069](https://arxiv.org/abs/hep-th/0110069), [doi:10.1088/1126-6708/2002/02/009](https://doi.org/10.1088/1126-6708/2002/02/009)&rbrack;

* {#HoweTsimpis03} [[Paul Howe]], [[Dimitrios Tsimpis]], *On higher-order corrections in M theory*, JHEP **09** (2003) 038 &lbrack;[arXiv:hep-th/0305129](https://arxiv.org/abs/hep-th/0305129), [doi:10.1088/1126-6708/2003/09/038](https://doi.org/10.1088/1126-6708/2003/09/038)&rbrack;
  > Sections 4--6: spinorial cohomology and the anomaly-corrected seven-form Bianchi identity.

* {#Tsimpis04} [[Dimitrios Tsimpis]], *11D supergravity at $\mathcal{O}(\ell^3)$*, JHEP **10** (2004) 046 &lbrack;[arXiv:hep-th/0407271](https://arxiv.org/abs/hep-th/0407271), [doi:10.1088/1126-6708/2004/10/046](https://doi.org/10.1088/1126-6708/2004/10/046)&rbrack;

* {#CGNT04} [[Martin Cederwall]], [[Ulf Gran]], [[Bengt Nilsson]], [[Dimitrios Tsimpis]], *Supersymmetric Corrections to Eleven-Dimensional Supergravity*, JHEP **05** (2005) 052 &lbrack;[arXiv:hep-th/0409107](https://arxiv.org/abs/hep-th/0409107), [doi:10.1088/1126-6708/2005/05/052](https://doi.org/10.1088/1126-6708/2005/05/052)&rbrack;

* {#SoueresTsimpis17} [[Bertrand Souères]], [[Dimitrios Tsimpis]], *Action principle and the supersymmetrization of Chern-Simons terms in eleven-dimensional supergravity*, Physical Review D **95** 2 (2017) 026013 &lbrack;[arXiv:1612.02021](https://arxiv.org/abs/1612.02021), [doi:10.1103/PhysRevD.95.026013](https://doi.org/10.1103/PhysRevD.95.026013)&rbrack;
  > Sections 4--5 and Appendix C: the anomaly superinvariant, the remaining $\tau$-exactness check, and conditional integrability results.

* {#Soueres18} [[Bertrand Souères]], *Supergravities in Superspace*, doctoral thesis, Lyon (2018) &lbrack;[tel:01998725](https://theses.hal.science/tel-01998725), [pdf](https://theses.hal.science/tel-01998725/document)&rbrack;

### Ordinary anomaly polynomials and M5-brane inflow

These references concern worldvolume anomalies and bulk inflow, including their global refinements, rather than a solution of the eleven-dimensional superspace deformation problem.

* {#Witten96} [[Edward Witten]], *Five-Brane Effective Action in M-Theory*, Journal of Geometry and Physics **22** 2 (1997) 103--133 &lbrack;[arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234), [doi:10.1016/S0393-0440(97)80160-X](https://doi.org/10.1016/S0393-0440%2897%2980160-X)&rbrack;

* {#FreedHarveyMinasianMoore98} [[Daniel Freed]], [[Jeffrey Harvey]], [[Ruben Minasian]], [[Gregory Moore]], *Gravitational Anomaly Cancellation for M-Theory Fivebranes*, Advances in Theoretical and Mathematical Physics **2** 3 (1998) 601--618 &lbrack;[arXiv:hep-th/9803205](https://arxiv.org/abs/hep-th/9803205), [doi:10.4310/ATMP.1998.v2.n3.a8](https://doi.org/10.4310/ATMP.1998.v2.n3.a8)&rbrack;

* {#HarveyMinasianMoore98b} [[Jeffrey Harvey]], [[Ruben Minasian]], [[Gregory Moore]], *Non-abelian Tensor-multiplet Anomalies*, JHEP **09** (1998) 004 &lbrack;[arXiv:hep-th/9808060](https://arxiv.org/abs/hep-th/9808060), [doi:10.1088/1126-6708/1998/09/004](https://doi.org/10.1088/1126-6708/1998/09/004)&rbrack;

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger: *Anomaly cancellation in M-theory: a critical review*, Nuclear Physics B **675** (2003) 416--446 &lbrack;[arXiv:hep-th/0307152](https://arxiv.org/abs/hep-th/0307152), [doi:10.1016/j.nuclphysb.2003.10.002](https://doi.org/10.1016/j.nuclphysb.2003.10.002)&rbrack;

* {#Monnier15} [[Samuel Monnier]], *Global gravitational anomaly cancellation for five-branes*, Advances in Theoretical and Mathematical Physics **19** 3 (2015) 701--724 &lbrack;[arXiv:1310.2250](https://arxiv.org/abs/1310.2250), [doi:10.4310/ATMP.2015.v19.n3.a5](https://doi.org/10.4310/ATMP.2015.v19.n3.a5)&rbrack;

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
