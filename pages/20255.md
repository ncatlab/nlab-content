
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

#Contents#
* table of contents
{:toc}

## Idea

In the [[string theory]]-literature "$I_8$" is the standard notation for a certain [[characteristic class]] of [[manifolds]] (of their [[tangent bundles]]): It is a [[rational numbers|rational]] linear combination of the [[cup product|cup square]] of the [[first fractional Pontryagin class]]  with itself, and the [[second Pontryagin class]]:

\[
  \label{TheTerm}
  I_8
  \;\coloneqq\;
  \tfrac{1}{48}
  \Big(
    p_2 \;-\; \big( \tfrac{1}{2} p_1\big)^2
  \Big)
  \;\; 
  \in
  H^8\big( -, \mathbb{Q}\big)
  \,.
\]

In general this is a [[cohomology class]] in [[ordinary cohomology]] with [[rational number|rational]] [[coefficients]], though in applications it appears in further rational combination with other classes that in total yield a class in [[integral cohomology]].

The expression (eq:TheTerm) controls certain [[quantum anomaly cancellation]] in [[M-theory]] and [[type IIA string theory]] ([Vafa-Witten 95](#VafaWitten95), [Duff-Liu-Minasian 95 (3.10) with (3.14)](#DuffLiuMinasian95)). Since it was first obtain as a [[1-loop]]-contribution in [[perturbative quantum gravity|perturbative quantum]] [[supergravity]], it is often known as _the one-loop anomaly term_ or the _one-loop anomaly polynomial_ in [[M-theory]]/[[type IIA string theory]].


\linebreak

## Properties

### As a higher curvature correction to 11d Supergravity
 {#AsHigherCurvatureCorrectionTo11dSugra}

A systematic analysis of the possible [[supersymmetry|supersymmetric]] [[higher curvature corrections]] of [[D=11 supergravity]] makes the $I_8$ appear as the higher curvature correction at order $\ell^6$, where $\ell$ is the [[Planck length]] in 11d ([Souères-Tsimpis 17, Section 4](#SoueresTsimpis17)).

At this order, the [[equation of motion]] for the [[supergravity C-field]] [[flux]] $G_4$ and its dual $G_7$ is ([Souères-Tsimpis 17, (4.3)](#SoueresTsimpis17))

$$
  d G_7(\ell)
  \;=\;
  -\tfrac{1}{2}
  G_4(\ell) \wedge G_4(\ell)
  + 
  \ell^6 I_8(R)
  \,,
$$

where the flux forms themselves appear in their higher order corrected form as [[power series]] in the [[Planck length]]

$$
  G_4(\ell)
  \;=\;
  G_4 + \ell^6 G_4^{(1)} + \cdots
$$

$$
  G_7(\ell)
  \;=\;
  G_7 + \ell^6 G_7^{(1)} + \cdots
$$

([Souères-Tsimpis 17, (4.4)](#SoueresTsimpis17))

Beware that this is not the lowest order [[higher curvature correction]]: there is already one at $\mathcal{O}(\ell^3)$, given by $\ell^3 G_4 \wedge \tfrac{1}{2}p_1(R)$ ([Souères-Tsimpis 17, Section 3.2](#SoueresTsimpis17)). Hence the full correction at $\mathcal{O}(\ell^6)$ should be the further modification of (eq:11dSugraBIAtOrder6) to

\[
  \label{11dSugraBIAtOrder6}
  d G_7(\ell)
  \;=\;
  -\tfrac{1}{2}
  G_4(\ell) \wedge 
  \big( 
    G_4(\ell)
    -
    2\ell^3 \tfrac{1}{2} p_1(R)
  \big)
  + 
  \ell^6 I_8(R)
  \,,
\]



### Inflow to M5-brane anomalies
 {#InflowToM5BraneAnomaly}

Consider an 11-dimensional [[spin structure|spin]]-[[manifold]] $X^{(11)}$ and a 2-parameter family of 6-dimensional [[submanifolds]] $Q_{M5} \hookrightarrow X^{(11)}$. When regarded as a family of [[worldvolumes]] of an [[M5-brane]], the family of [[normal bundles]] $N_X Q_{M5}$ of this inclusion carries a [[characteristic class]]

\[
  \label{IM5}
  I^{M5}
  \;\coloneqq\;
  I^{M5}_{\psi} 
  + 
  I_{C}
  \;\in\;
  H^8(F \times Q_{M5},\mathbb{Z})
\]

where

1. the first summand is the class of the [[chiral anomaly]] of [[chiral fermions]] on $Q_{M5}$ ([Witten 96, (5.1)](#Witten96)), 

1. the second term the class of the [[quantum anomaly]] of a [[self-dual higher gauge field]] ([Witten 96, (5.4)](#Witten96))

Moreover, there is the restriction of the $I_8$-term (eq:TheTerm) to $Q_{M5}$, hence to the [[tangent bundle]] of $X^{11}$ to $Q_{M5}$ (the "anomaly inflow" from the [[bulk spacetime]] to the M5-brane)

\[
  \label{I8AnomalyInflow}
  I_8\vert_{M5}
  \;\coloneqq\;
   I_8
   \big(
     T_{Q_{M5}} X
   \big)
  \;\in\;
  H^8(F \times Q_{M5},\mathbb{Z})
  \,.
\]

The sum of these cohomology classes, evaluated on the [[fundamental class]] of $Q_{M5}$ is proportional to the [[second Pontryagin class]] of the [[normal bundle]]

\[
  \label{SumOfM5AndInflowAnomalyIsp2}
  I^{M5}
  \;+\;
  I_8\vert_{M5}
  \;=\;
  \tfrac{1}{24} p_2(N_{Q_{M5}})
\]

([Witten 96 (5.7)](#Witten96))

This result used to be "somewhat puzzling" ([Witten 96, p. 35](#Witten96)) since consisteny of the [[M5-brane]] in [[M-theory]] should require its total [[quantum anomaly]] to vanish. But $p_2(N_{Q_{M5}})$ does not in general vanish, and the right conditions to require under which it does vanish were "not clear" ([Witten 96, p. 37](#Witten96)).

(For more details on computations involved this and the following arguments, see also [Bilal-Metzger 03](#BilalMetzger03)).


A resolution was proposed in ([Freed-Harvey-Minasian-Moore 98](#FreedHarveyMinasianMoore98)), further clarified in ([Monnier 13](#Monnier13)), see also ([Bah-Bonetti-Minasian-Nardoni 18](#BahBonettiMinasianNardoni18)). There it is asserted that 

1. the correct bulk anomaly inflow is not just that from $I_8$ itself, but includes also a contribution from the class $G_4$ of the [[supergravity C-field]], as per (eq:FiberIntegration) below ([Monnier 13, around (3.11)](#Monnier13));

1. for $G^{M5}_4$ the "restriction" of the class of the [[supergravity C-field]] to $Q_{M5}$, the term $I^{M5}_{C}$ in (eq:IM5) should have a further summand $-\tfrac{1}{2}\big( G_4^{M5} \big)^2$ ([Monnier 13, around (3.7)](#Monnier13), using [Monnier 14b, (2.13)](#Monnier14b))

1. for 11d spacetime a [[4-sphere]]-[[fiber bundle]], 

   $$
     \array{
        S^4 &\longrightarrow& X^{(11)} 
        \\
        && \big\downarrow^{\mathrlap{\pi}}
        \\
        && X^{(6)}
     }
   $$ 
  
   as befits the [[near horizon geometry]] of a [[black brane|black]] [[M5-brane]], the [[supergravity C-field]] should be taken to be of the form ([Monnier 13, (3.12)](#Monnier13))

   $$
     G_4 =\coloneqq \tfrac{1}{2}\chi + \pi^\ast(G^{M5}_4)
   $$ 
   
   with $\tfrac{1}{2}\chi$ the degree-4 [[Euler class]], whose integral over the 4-sphere fiber is unity ([this Prop.](Sullivan+model+of+a+spherical+fibration#SullivanModelForSphericalFibration)), reflecting the presence of a single M5.

By this proposal (also [Bah-Bonetti-Minasian-Nardoni 18 (5)](#BahBonettiMinasianNardoni18), [BBMN 19 (2.9) and appendix A.4, A.5](#BBMN19)), the anomaly inflow from the bulk would not be just $I_8$, as in (eq:I8AnomalyInflow) but would be all of the following [[fiber integration]] 

\[
  \label{FiberIntegration}
  \array{
    \pi_\ast
    \Big(
      -
      \tfrac{1}{6}
      G_4  G_4  G_4
      +
      G_4  I_8
    \Big)
    & =
    - \tfrac{1}{24} p_2 + \tfrac{1}{2}(G^{M5}_4)^2 + I_8
  }
\]

Here  we used [this Prop](Spin5#FiberIntegrationOfCupPowersOfChiOver4Sphere) to find that 

$$
  \pi_\ast\big(
    \chi^3
  \big)
  \;=\;
  2 p_2
$$

which would cancel against the first term $\tfrac{1}{24} p_2$ in (eq:FiberIntegration). Hence with this proposal, the remaining M5-brane anomaly (eq:SumOfM5AndInflowAnomalyIsp2) would be canceled.



\linebreak

## Related concepts

* [[Pontryagin classes]], [[Stiefel-Whitney classes]], [[Wu classes]], [[Euler class]]

* [[C-field tadpole cancellation]]


## References

### General

The term showed  in [[string theory]]/[[M-theory]] [[anomaly cancellation]] in 

* {#VafaWitten95} [[Cumrun Vafa]], [[Edward Witten]], _A One-Loop Test Of String Duality_, Nucl.Phys.B447:261-270, 1995 ([arXiv:hep-th/9505053](https://arxiv.org/abs/hep-th/9505053))

* {#DuffLiuMinasian95} [[Mike Duff]], [[James Liu]], [[Ruben Minasian]], _Eleven Dimensional Origin of String/String Duality: A One Loop Test_, Nucl.Phys. B452 (1995) 261-282 ([arXiv:hep-th/9506126](https://arxiv.org/abs/hep-th/9506126))

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J.Geom.Phys.22:103-133, 1997 ([arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234))


For further discussion see

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ , 
  
  part I, Proc. Symp. Pure Math. 81 (2010), 181-236 ([arXiv:1001.5020](http://arXiv.org/abs/1001.5020)), 

  part _II: Twisted $String$ and $String^c$ structures_, J. Australian Math. Soc. 90 (2011), 93-108 ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419)); 

  part _III: Twisted higher structures_, Int. J. Geom. Meth. Mod. Phys. 8 (2011), 1097-1116 ([arXiv:1008.1755](http://arxiv.org/abs/1008.1755))

### From higher curvature corrections to 11d Supergravity

Derivation from classification of [[higher curvature corrections]] to [[D=11 supergravity]]:

* {#SoueresTsimpis17} Bertrand Souères, [[Dimitrios Tsimpis]], Section 4 of: _The action principle and the supersymmetrisation of Chern-Simons terms in eleven-dimensional supergravity_, Phys. Rev. D 95, 026013 (2017) ([arXiv:1612.02021](https://arxiv.org/abs/1612.02021))


### In relation to the quantum anomaly of the M5-brane

In relation to the [[quantum anomaly]] of the [[M5-brane]]:

The original computation of the total M5-brane anomaly due to 

* [Witten 96](#Witten96)

left a remnant term of $\tfrac{1}{24} p_2$. It was argued in

* {#FreedHarveyMinasianMoore98} [[Dan Freed]], [[Jeff Harvey]], [[Ruben Minasian]], [[Greg Moore]], _Gravitational Anomaly Cancellation for M-Theory Fivebranes_, Adv.Theor.Math.Phys.2:601-618, 1998 ([arXiv:hep-th/9803205](https://arxiv.org/abs/hep-th/9803205))

* {#HarveyMinasianMoore98b} [[Jeff Harvey]], [[Ruben Minasian]], [[Greg Moore]], _Non-abelian Tensor-multiplet Anomalies_, JHEP9809:004, 1998 ([arXiv:hep-th/9808060](https://arxiv.org/abs/hep-th/9808060))

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger, _Anomaly cancellation in M-theory: a critical review_, Nucl.Phys. B675 (2003) 416-446 ([arXiv:hep-th/0307152](https://arxiv.org/abs/hep-th/0307152))

that this term disappears (cancels) when properly taking into account the singularity of the [[supergravity C-field]] at the locus of the [[black brane|black]] [[M5-brane]].

A more transparent version of this argument was offered in

* {#Monnier13} Samuel Monnier, _Global gravitational anomaly cancellation for five-branes_, Advances in Theoretical and Mathematical Physics, Volume 19 (2015) 3 ([arXiv:1310.2250](https://arxiv.org/abs/1310.2250)) 

based on a refined discussion of the quantum anomaly of the [[self-dual higher gauge field]] on the M5-brane in 


* {#Monnier14a} Samuel Monnier, _The anomaly line bundle of the self-dual field theory_, Comm. Math. Phys. 325 (2014) 41-72 ([arXiv:1109.2904](http://arxiv.org/abs/1109.2904))

* {#Monnier14b} Samuel Monnier, _The global gravitational anomaly of the self-dual field theory_, Comm. Math. Phys. 325 (2014) 73-104 ([arXiv:1110.4639](http://arxiv.org/abs/1110.4639), [pdf slides](http://www.physics.rutgers.edu/het/video/monnier11b.pdf))

This formulation via an anomaly 12-form is (re-)derived also in

* {#BahBonettiMinasianNardoni18} Ibrahima Bah, Federico Bonetti, [[Ruben Minasian]], Emily Nardoni, _Class $\mathcal{S}$ Anomalies from M-theory Inflow_, Phys. Rev. D 99, 086020 (2019) ([arXiv:1812.04016](https://arxiv.org/abs/1812.04016))

* {#BBMN19} Ibrahima Bah, Federico Bonetti, [[Ruben Minasian]], Emily Nardoni, _Anomaly Inflow for M5-branes on Punctured Riemann Surfaces_ ([arXiv:1904.07250](https://arxiv.org/abs/1904.07250))


[[!redirects one-loop anomaly polynomial I8]]
