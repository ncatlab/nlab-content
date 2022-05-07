

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[11-dimensional supergravity]] the [[brane]] electrically charged under the [[supergravity C-field]] is the [[M2-brane]]/[[membrane]]. The dual under [[electric-magnetic duality]] is the M5-brane.

## Definition

### As a Green-Schwarz type sigma-model

As a [[Green-Schwarz sigma-model]]: [BLNPST 97](#BLNPST97)

### As a black $p$-brane

As a [[black brane]] solution of [[11-dimensional supergravity]] the M5-brane is given ([Gueven 92](#Gueven92)) by the [[spacetime]] $\mathbb{R}^{5,1} \times (\mathbb{R}^5-\{0\})$ with [[pseudo-Riemannian metric]] given by

$$
  g = H^{-1/3} g_{\mathbb{R}^{5,1}} \oplus H^{2/3} g_{\mathbb{R}^5-\{0\}}
$$

for $H = 1 + \frac{1}{r}$ and $r$ the distance in $\mathbb{R}^5$ from the origin, and with [[field strength]] of the [[supergravity C-field]] being

$$
  F = \star_{\mathbb{R}^5} \mathbf{d}H
  \,.
$$

This is a $1/2$-[[BPS state]] of 11-dimensional supergravity.

The [[near horizon geometry]] of this spacetime is [[anti de Sitter spacetime|AdS7]]$\times$[[4-sphere|S4]]. For more on this see at _[[AdS-CFT]]_.


[[!include black branes in supergravity -- table]]


### At an orbifold singularity
 {#AtAnOrbifoldSingularity}

{#NearHorizonOrbifold} More generally for 1/2 BPS black M5-branes, the near horizon geometry is $AdS_7 \times S^4/G$, where $G$ is a [[finite subgroup of SU(2)]] ([[ADE classification|ADE subgroup]]) acting by left multiplication on the [[quaternions]] $\mathbb{H}$ in the canonical way, under the identitfication $S^4 \simeq S(\mathbb{R}^5) \simeq S(\mathbb{R}\oplus \mathbb{H})$ ([MFF 12, section 8.3](#MFF12)).

While this geometric discussion in [MFF 12, section 8.3](#MFF12) works for all the [[finite subgroups of SU(2)]], folklore has it that in [[M-theory]] the M5-branes appear only at A-type singularities, while the more general [[6d (2,0)-superconformal field theories]] for all possible [[ADE-singularities]] appear only after passage to [[F-theory]] ([ZHTV 14, p. 3](#ZHTV14)).

On the other hand, when placing the M5 at an MO5-[[orientifold]] ([Witten 95](#Witten95)) its worldvolume theory breaks from $(2,0)$ to $(1,0)$-supersymmetry and all ADE-singularities should be allowed.

(...)


## Properties

### Worldvolume theory

the [[worldvolume]] theory of the M5-brane is the [[6d (2,0)-superconformal QFT]].

This [[worldvolume]] theory involves [[self-dual higher gauge theory]] of the [[nonabelian cohomology|nonabelian]] kind ([Witten07](#Witten07), [Witten09](#Witten09)): the fields are supposed to be [[connections on a 2-bundle]]($\sim$ [[gerbe]]), presumably with structure [[2-group]] the [[automorphism 2-group]] $AUT(G)$ of some [[Lie group]] $G$. 

For instance in the proposal of ([SSW11](#SSW11)) one sees in equation (2.1) _almost_ the data of an $\mathfrak{aut}(\mathfrak{g})$-[[2-groupoid of Lie 2-algebra valued forms|Lie 2-algebra valued forms]].

### Branes inside the M5

The M5-brane admits two solitonic excitations ($p$-branes within branes)

* $p = 1$: the [[self-dual string]]

* $p = 3$: the [[3-brane in 6d]] (see there for more)

See also 

* [[M2-M5 brane bound state]]

### Dimensional reduction

On [[Kaluza-Klein mechanism|dimensional reduction]] of [[11-dimensional supergravity]] on a circle the M5-brane turns into the [[NS5-brane]] and the [[D-brane|D4-brane]] of [[type II string theory]].

The [[Kaluza-Klein mechanism|compactification]] of the 5-brane on a [[Riemann surface]] yields as [[worldvolume]] [[theory (physics)|theory]] [[N=2 D=4 super Yang-Mills theory]]. See at _[N=2 D=4 SYM -- Construction by compactification of 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)_.

### Holographic dual

The [[AdS/CFT correspondence]] for the 5-brane is $AdS_7/CFT_6$ and relates the [[6d (2,0)-superconformal QFT]] to [[7-dimensional supergravity]] obtained by [[Kaluza-Klein mechanism|reduction]] of [[11-dimensional supergravity]] on a 4-[[sphere]] to an asymptotically 7d [[anti de Sitter spacetime]].

### Conformal blocks and 7d Chern-Simons dual
 {#7dCSDual}

The [[self-dual higher gauge theory|self-dual 2-connection]]-field (see there for more details) on the 6-dimensional [[worldvolume]] M5-brane is supposed to have a [[holographic principle|holographic]] description in terms of a [[higher dimensional Chern-Simons theory|7-dimensional Chern-Simons theory]] ([Witten 1996](#Witten96)). We discuss the relevant "fractional" [[quadratic form]] on [[ordinary differential cohomology]] that defines the correct [[action functional]].

Let $\hat G$ be the [[circle n-bundle with connection|circle 3-bundle with connection]] on a 7-dimensional manifold $X$ with boundary the M5-brane, thought of as the [[Kaluza-Klein mechanism|compactification]] of the [[supergravity C-field]] from [[11-dimensional supergravity]] down to [[7-dimensional supergravity]].

As discussed there, the [[higher dimensional Chern-Simons theory|7-dimensional Chern-Simons theory]] [[action functional]] on these 3-connections is

$$
  \hat G_4 \mapsto
  \exp(i \int_X \hat G_4 \cup \hat G_4)
  \,,
$$

where 

* $\exp(i \int_X (-))$ is the [[higher holonomy]] / [[fiber integration in ordinary differential cohomology]] from $X$ to the point

* of the [[Beilinson-Deligne cup product]] [[circle n-bundle with connection|7-connection]] $\hat G_4 \cup \hat G_4$.

The space of [[states]] of this 7d theory on the M5 worldvolume $\partial X$ would be the space of [[conformal blocks]] of the [[6d (2,0)-supersymmetric QFT]] on the [[worldvolume]].

Except, that it turns out that the [[first Chern class]] of the corresponding [[prequantum line bundle]] is _twice_ that required from [[geometric quantization]].

Therefore the above action functional is not yet the correct one, but only a fractional version of it is. However, the class $G_4 \cup G_4$ in [[integral cohomology]] has in general no reason to be divisible by 2.

This is related to the fact that as a [[quadratic form]] on the [[ordinary differential cohomology]] group $\hat H^4(X)$, the above is not a [[quadratic refinement]] of 

$$
  (\hat G, \hat G') \mapsto \exp(i \int_X \hat G \cup \hat G') 
  \,,
$$

but of twice that. In ([Witten 1996](#Witten96)) it was argued, and later clarified in ([Hopkins-Singer](#HopkinsSinger)), that instead the action functional should be replaced by a proper [[quadratic refinement]].

This is accomplished by shifting the center of the [[quadratic form]]
by a lift $\lambda \in H^4(X, \mathbb{Z})$ of the degree-4 [[Wu class]] $\nu_4 \in H^4(X, \mathbb{Z}/2)$ from 0 to $\frac{1}{2}\lambda$. 

(For that to make sense in [[integral cohomology]], either the [[Wu class]] $\lambda$ happens to be divisible by 2 on $X$, or else one has to regard it itself as a twisted differential character of sorts, as explained in ([Hopkins-Singer](#HopkinsSinger)). For the moment we will assume that $X$ is such that $\lambda$ is divisbible by 2.)

Since $X$, being a [[spacetime]] for [[supergravity]], admits (and is thought to be equipped with) a [[spin structure]], by the discussion at [[Wu class]] it follows that $\lambda$ is the [[first fractional Pontryagin class]] $\frac{1}{2}p_1$

$$
  (\frac{1}{2}p_1 \; mod \; 2) 
   \; 
     =
   \; 
   \nu_4 \in H^4(X, \mathbb{Z}/2)
  \,.
$$

By the very definition of [[Wu class]], it follows that for any $\hat \alpha \in \hat H^4(X)$ the combination

$$
  \hat \alpha \cup \hat \alpha + \hat \alpha \cup \hat \lambda = Sq^4(\hat \alpha) - \hat \alpha \cup \hat \lambda
  \; =\;  0 \;  mod  \; 2
$$

is divisible by 2.

Therefore define then the modified quadratic form

$$
  \exp(i S^\lambda) 
   \; : \; 
  \hat a \mapsto \exp i \int_X 
  \frac{1}{2}
  \left(
    \hat a \cup \hat a
    + 
    \hat a \cup \hat \mathbf{\lambda}
  \right)
$$

(see [[differential string structure]] for the definition of the differential refinement $\hat \mathbf{\lambda} = \frac{1}{2}\hat \mathbf{p}_1$),
where, note, we have included a global factor of 2, which is now possible due to the inclusion of the integral lift of the Wu class.

Notice that where the [[equations of motion]] of the original [[action functional]] are $\hat a = 0$, those of this shifted one are $\hat a = - \frac{1}{2}\hat \mathbf{\lambda}$. One may therefor calls $-\frac{1}{2}\lambda$ here a _background [[charge]]_ for the 7-d Chern-Simons theory.

This is now indeed a [[quadratic refinement]] of the [[intersection pairing]]:

$$
  \exp i \left( 
    S^\lambda\left(\hat a + \hat b \right)
    - 
    S^\lambda\left( \hat a \right)
    - 
    S^\lambda\left( \hat b \right)
    + 
    S^\lambda\left( 0 \right)
  \right)
  = 
  \exp i \int_X ( \hat a \cup \hat b  )
  \,.
$$

To express the correct action functional for the 7d Chern-Simons theory it is useful to define the shifted [[supergravity C-field]]

$$
  \hat a  := \hat G_4 - \frac{1}{2}\hat \mathbf{\lambda}
  \,,
$$

which the object whose [[equations of motion]] with respect to the 7d Chern-Simons theory are still $\hat a = 0$.

Then in terms of the original $\hat G_4$ the action functional for the [[holographic principle|holographic dual]] [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] reads

$$
  \exp(i S(\hat G_4))
  = 
  \exp(i \int_X
    \frac{1}{2}
    (
      \hat G_4 \cup \hat G_4  
      -
      (\frac{1}{2}\hat \mathbf{\lambda})^2
    )
  )
  \,.
$$

This is the action as it appears in ([Witten96, (3.6)](#Witten96)).

In terms of [[twisted differential c-structures]] we may summarize the outcome of this reasoning as follows:

_The divisibility of the action functional requires a $2(G_4 - a)$-[[twisted Wu structure]] in $\mathbb{Z}/2$-cohomology. Its lift to integral cohomology is the $2(G_4 - a)$-[[twisted differential string structure]] known as the "Witten quantization condition" on the [[supergravity C-field]]_.

### Restriction of the supergravity $C$-field
 {#RestrictionOfTheCField}

We discuss the conditions on the 
restriction of the [[supergravity C-field]] on the ambient 
[[11-dimensional supergravity]] [[spacetime]] to the M5-brane.

This is similar to the analogous situation in [[type II string theory]].
The [[Freed-Witten anomaly cancellation]] condition demands that
the restriction of the [[B-field]] $\hat H_3 \hat H^3(X)$ 
on spacetime $X$ to an 
[[orientation|oriented]] [[D-brane]] $Q \hookrightarrow X$ has
to trivialize, up to [[torsion]], relative to the integral 
[[Stiefel-Whitney class]] $W_3 = \beta(w_2)$, where
$\beta$ is the [[Bockstein homomorphism]] induced from the 
[[short exact sequence]] $\mathbb{Z} \stackrel{\cdot 2}{\to}
\mathbb{Z} \to \mathbb{Z}_2$:

$$
  H_3|_Q \simeq W_3
  \,,
$$

thus defining a [[twisted spin^c-structure]] on the [[D-brane]].

The analog of this for the M5-brane is discussed in 
([Witten00, section 5](#Witten2000)). There it is argued that
there is a class 

$$
  \theta \in H^3(Q, U(1))
$$

on the 5-brane such that under the [[Bockstein homomorphism]]
$\beta'$ induced by the [[short exact sequence]]
$\mathbb{Z} \to \mathbb{R} \to U(1)$ we have for the
[[supergravity C-field]] $\hat G \in \hat H^4(X)$ the condition

$$
  G|_Q = \beta'(\theta)
  \,.
$$

By the [above](#7dCSDual) quantization condition, this may also be thought of
as witnessing a [[twisted string structure]] on the 5-brane ([Sati](#Sati10)).

This condition reduces to the above one for the $B$-field under [[double dimensional reduction]] on the circle.

### M5-brane charge

See at _[[M5-brane charge]]_

\linebreak


### Anomaly cancellation
 {#AnomalyCancellation}

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

Moreover, there is the restriction of the [[I8]]-term (see [there](I8#eq:TheTerm)) to $Q_{M5}$, hence to the [[tangent bundle]] of $X^{11}$ to $Q_{M5}$ (the "anomaly inflow" from the [[bulk spacetime]] to the M5-brane)

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

This result used to be "somewhat puzzling" ([Witten 96, p. 35](#Witten96)) since consistency of the [[M5-brane]] in [[M-theory]] should require its total [[quantum anomaly]] to vanish. But $p_2(N_{Q_{M5}})$ does not in general vanish, and the right conditions to require under which it does vanish were "not clear" ([Witten 96, p. 37](#Witten96)).

(For more details on computations involved in this and the following arguments, see also [Bilal-Metzger 03](#BilalMetzger03)).

A resolution was proposed in [Freed-Harvey-Minasian-Moore 98](#FreedHarveyMinasianMoore98), also [Bah-Bonetti-Minasian-Nardoni 18 (5)](#BahBonettiMinasianNardoni18), [BBMN 19 (2.9) and appendix A.4, A.5](#BBMN19). By this proposal, the anomaly inflow from the bulk would not be just $I_8$, as in (eq:I8AnomalyInflow) but would be all of the following [[fiber integration]] 

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
    - \tfrac{1}{24} p_2 + \tfrac{1}{2}([G^{M5}_4])^2 + I_8
  }
\]

Here  we used [this Prop](Spin5#FiberIntegrationOfCupPowersOfChiOver4Sphere)

$$
  \pi_\ast\big(
    \chi^3
  \big)
  \;=\;
  2 p_2
$$

which would cancel against the first term $\tfrac{1}{24} p_2$ in (eq:FiberIntegration). Hence with this proposal, the previously remaining M5-brane anomaly (eq:SumOfM5AndInflowAnomalyIsp2) would be canceled... except for yet one last remaining term (see also [BBMN 19b (5.22)](#BBMN19b))

\[
  \label{RemainingAnomaly}
  [G^{M5}_4]^2 
  \;\in\; 
  H^8(Q_{M5}; \mathbb{Z})
  \,,
\]

where $G_4^{M5}$ denotes the [[basic differential form|basic form]]-component of $G_4$ with respect to the given [[spherical fibration]].

This basuc component has been ignored in [FHMM98](#FreedHarveyMinasianMoore98) and previous references. That this [[basic differential form|basic form]] component $G_4^{M5}$ indeed needs to be considered is highlighted in [BBMN 19b (3.16) & App. C](#BBMN19b) (where it is denoted $\gamma_4$, see also [BBM 20 (2.3)](#BahBonettiMinasian20)).

See also at _[M-theory -- Open problems -- M5-brane anomaly cancellation](M-theory#OpenProblemM5BraneAnomalyCancellation)_.

An argument that the remaing anomaly  (eq:RemainingAnomaly) vanishes by [[schreiber:Hypothesis H]] is in [SS 20a](#SS20a).

\linebreak

[[!include M2-M5 brane bound states in the BMN matrix model -- subsection]]

\linebreak

## Related concepts

* [[Perry-Schwarz action]]

* [[M5-brane instanton]]

* [[small instanton]]

* [[half M5-brane]]

* [[string theory]]

* [[11-dimensional supergravity]], [[M-theory]]

* [[supergravity Lie 6-algebra]], [[M-theory super Lie algebra]]

[[!include gauge theory from AdS-CFT -- table]]

[[!include table of branes]]


## References
 {#References}

### Survey

The history as of the 1990 is reviewed in 

* {#Duff99} [[Mike Duff]], chapter II of _[[The World in Eleven Dimensions]]: Supergravity, Supermembranes and M-theory_, IoP 1999 ([publisher](https://www.crcpress.com/The-World-in-Eleven-Dimensions-Supergravity-supermembranes-and-M-theory/Duff/9780750306720))

Further reviews and general accounts include

* [[Robbert Dijkgraaf]], _The mathematics of fivebranes_ ([pdf](http://arxiv.org/PS_cache/hep-th/pdf/9810/9810157v1.pdf))

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ (2010)

### Black brane description
 {#ReferencesAsBlackBrane}

#### Unwrapped

The M5 was first found as a [[black brane]] of [[11-dimensional supergravity]] (the [[black fivebrane]]) in 

* {#Gueven92} [[Rahmi Gueven]], _Black $p$-brane solutions of $D = 11$ supergravity theory_, Phys. Lett. B276 (1992) 49 (<a href="https://doi.org/10.1016/0370-2693(92)90540-K">doi:10.1016/0370-2693(92)90540-K</a>, [spire:338203](http://inspirehep.net/record/338203))

  also in: [[Mike Duff]] (ed.),  _[[The World in Eleven Dimensions]]_ 135-141

That this metric, as well as that of every black $p$ brane for _odd_ $p$, is completely non-singular was observed in 

* [[Gary Gibbons]], [[Gary Horowitz]], [[Paul Townsend]], p. 15 of _Higher-dimensional resolution of dilatonic black hole singularities_, Class. Quant. Grav. 12:297-318, 1995 ([arXiv:hep-th/9410073](https://arxiv.org/abs/hep-th/9410073))

Classification of more general M5-brane [[ADE-singularities]] is in  

* S. Ferrara, A. Kehagias, H. Partouche, A. Zaffaroni, _Membranes and Fivebranes with Lower Supersymmetry and their AdS Supergravity Duals_, Phys.Lett. B431 (1998) 42-48 ([arxiv:hep-th/9803109](https://arxiv.org/abs/hep-th/9803109))

* {#MFF12} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], Section 8.3 of: _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

also to some extent in


* Changhyun Ahn, Kyungho Oh, Radu Tatar, _Orbifolds $AdS_7 \times S^4$ and Six Dimensional $(0, 1)$ SCFT_, Phys. Lett. B442 (1998) 109-116 ([arXiv:hep-th/9804093](https://arxiv.org/abs/hep-th/9804093))

but see p. 3 of 

* {#ZHTV14} Michele Del Zotto, [[Jonathan Heckman]], [[Alessandro Tomasiello]], [[Cumrun Vafa]], _6d Conformal Matter_, <a href="https://link.springer.com/article/10.1007%2FJHEP02%282015%29054">10.1007/JHEP02(2015)054</a> ([arXiv:1407.6359](https://arxiv.org/abs/1407.6359))


Identification of the $\mathcal{N} = (2,0)$ black M5-brane sitting at the [[ADE singularity|A-type singularity]] of an $MO5$ $\mathbb{Z}/2$-[[orientifold]] locally of the form $\mathbb{R}^{5,1} \times ( \mathbb{R}^5 \sslash (\mathbb{Z}/2) )$ is due to 

* {#Witten95} [[Edward Witten]], _Five-branes And M-Theory On An Orbifold_, Nucl. Phys. B463:383-397, 1996 ([arXiv:hep-th/9512219](https://arxiv.org/abs/hep-th/9512219))


Discussion in terms of [[E11]]-[[U-duality]] and [[current algebra]] is in 

* [[Hirotaka Sugawara]], _Current Algebra Formulation of M-theory based on E11 Kac-Moody Algebra_, International Journal of Modern Physics A, Volume 32, Issue 05, 20 February 2017 ([arXiv:1701.06894](https://arxiv.org/abs/1701.06894))

* [[Shotaro Shiba]], [[Hirotaka Sugawara]], _M2- and M5-branes in E11 Current Algebra Formulation of M-theory_ ([arXiv:1709.07169](https://arxiv.org/abs/1709.07169))

#### Wrapped on hyperblic 3-manifolds

Solutions to [[D=11 N=1 supergravity]] describing [[black brane|black]] [[M5-branes]] [[wrapped brane|wrapped]] on [[hyperbolic 3-manifolds]] (with application to the [[3d-3d correspondence]] and [[proof]] of the [[volume conjecture]]):

* [[Jerome Gauntlett]], [[Nakwoo Kim]], [[Daniel Waldram]], Section 3.1 of: _M-Fivebranes Wrapped on Supersymmetric Cycles_, Phys. Rev. D63 (2001) 126001 ([arXiv:hep-th/0012195](https://arxiv.org/abs/hep-th/0012195))


* Aristomenis Donos, [[Jerome Gauntlett]], [[Nakwoo Kim]], Oscar Varelam, _Wrapped M5-branes, consistent truncations and AdS/CMT_, JHEP 1012:003, 2010 ([arXiv:1009.3805](https://arxiv.org/abs/1009.3805)) 

* {#GangKimLee14a} Dongmin Gang, [[Nakwoo Kim]], Sangmin Lee, _Holography of Wrapped M5-branes and Chern-Simons theory_, Physics Letters B
Volume 733, 2 June 2014, Pages 316-319 ([arXiv:1401.3595](https://arxiv.org/abs/1401.3595))

* {#GangKimLee14b} Dongmin Gang, [[Nakwoo Kim]], Sangmin Lee, _Holography of 3d-3d correspondence at Large $N$_, JHEP04(2015) 091 ([arXiv:1409.6206](https://arxiv.org/abs/1409.6206))

* {#GangKim18} Dongmin Gang, [[Nakwoo Kim]], _Large $N$ twisted partition functions in 3d-3d correspondence and Holography_, Phys. Rev. D 99, 021901 (2019) ([arXiv:1808.02797](https://arxiv.org/abs/1808.02797))

* {#GangKimPandoZayas19} Dongmin Gang, [[Nakwoo Kim]], Leopoldo A. Pando Zayas, _Precision Microstate Counting for the Entropy of Wrapped M5-branes_ ([arXiv:1905.01559](https://arxiv.org/abs/1905.01559))

Discussion of the [[volume conjecture]] by combining the 3d/3d correspondence with [[AdS/CFT]] in these backgrounds:

* [Gang-Kim-Lee 14b, Section 3.2](#GangKimLee14b)

* [Gang-Kim 18, around (21)](#GangKim18)

Enhanced to a [[defect field theory]]:

* Dongmin Gang, [[Nakwoo Kim]], Mauricio Romo, Masahito Yamazaki, _Aspects of Defects in 3d-3d Correspondence_, J. High Energ. Phys. (2016) ([arXiv:1510.05011](https://arxiv.org/abs/1510.05011))



### $\sigma$-Model description
 {#ReferencesSigmaModelDescription}

The [[Green-Schwarz action functional]]-type [[sigma-model]] of the (single) M5-brane of  was found in covariant form in 

* {#PST97} [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for a D=11 Five-Brane with the Chiral Field_, Phys. Lett. B398 (1997) 41 ([arXiv:hep-th/9701037](https://arxiv.org/abs/hep-th/9701037))

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

generally following

* [[Paul Townsend]], section 3.3 of _D-branes from M-branes_, Phys. Lett. B373 (1996) 68-75 ([arXiv:hep-th/9512062](https://arxiv.org/abs/hep-th/9512062))

  (which did not yet have the [[Hopf-Wess-Zumino term]])

and using the covariant mechanism for [[self-dual higher gauge fields]] from 

* [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On Lorentz Invariant Actions for Chiral P-Forms_, Phys.Rev. D55 (1997) 6292-6298 ([arXiv:hep-th/9611100](https://arxiv.org/abs/hep-th/9611100))

based on the non-covariant form of the [[self-dual higher gauge field|self-duality mechanism]] ([[Perry-Schwarz action]]) due to

* {#PerrySchwarz96} [[Malcolm Perry]], [[John Schwarz]], _Interacting Chiral Gauge Fields in Six Dimensions and Born-Infeld Theory_, Nucl. Phys. B489 (1997) 47-64 ([arXiv:hep-th/9611065](http://arxiv.org/abs/hep-th/9611065))

* {#Schwarz97} [[John Schwarz]], _Coupling a Self-Dual Tensor to Gravity in Six Dimensions_, Phys. Lett. B395:191-195, 1997 ([cds:317663](http://cds.cern.ch/record/317663), <a href="https://doi.org/10.1016/S0370-2693(97)00094-4">doi:10.1016/S0370-2693(97)00094-4</a>)

* {#APPS97a} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_, Nucl.Phys. B496 (1997) 191-214 ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))


Discussion of the equivalence of these superficially different action functionals is in 

* [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On the equivalence of different formulations of the M Theory five--brane_, Phys. Lett. B408 (1997) 135-141 ([arXiv:hep-th/9703127](http://arxiv.org/abs/hep-th/9703127))

The [[equations of motion]] in [[super spacetime]] were derived in

* {#HoweSezginWest97} [[Paul Howe]], [[Ergin Sezgin]], [[Peter West]], _Covariant Field Equations of the M Theory Five-Brane_, Phys. Lett. B399 (1997) 49-59 ([arXiv:hep-th/9702008](https://arxiv.org/abs/hep-th/9702008))

and using the [[superembedding approach]] in

* {#HoweSezgin97} [[Paul Howe]], [[Ergin Sezgin]], _$D=11$, $p=5$_, Phys.Lett. B394 (1997) 62-66 ([arXiv:hep-th/9611008](https://arxiv.org/abs/hep-th/9611008))

see

* {#Sorokin99} [[Dmitri Sorokin]], Section 5.2 of _Superbranes and Superembeddings_, Phys.Rept.329:1-101, 2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))


A variant adapted to a 3+3-dimensional split in

* Sheng-Lan Ko, [[Dmitri Sorokin]], Pichet Vanichchapongjaroen, _The M5-brane action revisited_, JHEP11(2013)072 ([arXiv:1308.2231](https://arxiv.org/abs/1308.2231))

The computation of the small fluctuations of this GS-type sigma-model around a solution embedding as the asymptotic boundary of the [[AdS-spacetime]] [[near-horizon geometry]] of a black 5-brane as [above](#ReferencesAsBlackBrane), and the proof, to low order, that the result is the [[6d (2,0)-supersymmetric QFT]] appearing in [[AdS-CFT|AdS7-CFT6 duality]] is due to 

* {#ClausKalloshProeyen97} P. Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl.Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))


A review with emphasis on the coupling to the [[M2-brane]] is in 

* [[Ergin Sezgin]], P. Sundell, _Aspects of the M5-Brane_ ([arXiv:hep-th/9902171](http://arxiv.org/abs/hep-th/9902171))


Further developments include

* Sheng-Lan Ko, [[Dmitri Sorokin]], Pichet Vanichchapongjaroen, _The M5-brane action revisited_ ([arXiv:1308.2231](http://arxiv.org/abs/1308.2231))



[[!include M5-branes in the BMN matrix model -- references]]


### Worldvolume theory
 {#ReferencesWorldvolumeTheory}

The original article suggesting the description of the [[self-dual higher gauge theory]] on the 5-brane [[holographic principle|holographically]] by a dual [[higher dimensional Chern-Simons theory]] is

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J.Geom.Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 

A precise mathematical formulation of the proposal made there is given in

* {#HopkinsSinger} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 

A discussion that embeds this argument into the larger context of [[AdS-CFT duality]] is in 

* {#Witten98} [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 

Discussion of [[S-duality]] in 6d self-dual higher gauge theory via [[non-commutative geometry|non-commutative]]-deformation:

* {#MathaiSati14} [[Varghese Mathai]], [[Hisham Sati]], _Higher abelian gauge theory associated to gerbes on noncommutative deformed M5-branes and S-duality_, J. Geom. Phys. 92:240-251, 2015 ([arXiv:1404.2257](https://arxiv.org/abs/1404.2257)) 

See also the references at _[[6d (2,0)-supersymmetric QFT]]_.

The [[double dimensional reduction]] to the [[D4-brane]] [[D=5 super Yang-Mills theory]] and the relation to [[Khovanov homology]] is discussed in 

* {#Witten11} [[Edward Witten]], _Fivebranes and Knots_, Quantum Topology, Volume 3, Issue 1, 2012, pp. 1-137 ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216), [doi:10.4171/QT/26](https://www.ems-ph.org/journals/show_abstract.php?issn=1663-487X&vol=3&iss=1&rank=1))
 
 
with further comments in 

* Michele Nardelli, _On some equations concerning Fivebranes and Knots, Wilson Loops in Chern-Simons Theory, cusp anomaly and integrability from String theory. Mathematical connections with
some sectors of Number Theory_  (2011) ([pdf](http://empslocal.ex.ac.uk/people/staff/mrwatkin/zeta/nardelli2011b.pdf))

A proposal for a construction as a [[higher gauge theory]] for [[differential string structure|string 2-connections]] is due to 

* {#SaemannSchmidt17b} [[Christian Saemann]], Lennart Schmidt, _Towards an M5-Brane Model I: A 6d Superconformal Field Theory_, J. Math. Phys. 59 (2018) 043502 ([arXiv:1712.06623](https://arxiv.org/abs/1712.06623))

based on 

* {#SaemannSchmidt17a} [[Christian Saemann]], Lennart Schmidt, _The Non-Abelian Self-Dual String and the (2,0)-Theory_ ([arXiv:1705.02353](https://arxiv.org/abs/1705.02353))


### Hopf-Wess-Zumino term
 {#ReferencesHopfWessZuminoTerm}

The [[higher dimensional WZW model|higher WZW term]] of the M5-brane ([[Hopf-Wess-Zumino term]]) was first proposed in

* {#Aharony94} [[Ofer Aharony]], p. 11 of _String theory dualities from M theory_, Nucl. Phys. B476:470-483, 1996 ([arXiv:hep-th/9604103](https://arxiv.org/abs/hep-th/9604103))

and had been settled by the time of 

* [BLNPST 97 (1)](#BLNPST97).

The resemblence of the first summand of the term to the [[Whitehead integral formula]] for the [[Hopf invariant]] was noticed in

* {#Intriligator00} [[Kenneth Intriligator]], _Anomaly Matching and a Hopf-Wess-Zumino Term in 6d, N=(2,0) Field Theories_, Nucl.Phys. B581 (2000) 257-273 ([arXiv:hep-th/0001205](https://arxiv.org/abs/hep-th/0001205))

which hence introduced the terminology "Hopf-Wess-Zumino term". Followup to this terminology includes

* {#KalkkinenStelle02} [[Jussi Kalkkinen]], [[Kellogg Stelle]], Section 3.2 of: _Large Gauge Transformations in M-theory_, J. Geom. Phys. 48 (2003) 100-132 ([arXiv:hep-th/0212081](https://arxiv.org/abs/hep-th/0212081))

* Shan Hu, Dimitri Nanopoulos, _Hopf-Wess-Zumino term in the effective action of the 6d, (2, 0) field theory revisted_, JHEP 1110:054, 2011 ([arXiv:1110.0861](https://arxiv.org/abs/1110.0861))

* [[Alex Arvanitakis]], Section 4.1 of _Brane Wess-Zumino terms from AKSZ and exceptional generalised geometry as an $L_\infty$-algebroid_ ([arXiv:1804.07303](https://arxiv.org/abs/1804.07303))

More on the relation to the Hopf invariant in

* {#Sati13} [[Hisham Sati]], _Framed M-branes, corners, and topological invariants_, J. Math. Phys. 59 (2018), 062304 ([arXiv:1310.1060](http://arxiv.org/abs/1310.1060))

Discussion of the full 6d WZ term is in 

* {#FSS19WZ} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_


### Anomaly cancellation
 {#ReferencesAnomalyCancellation}

The original computation of the total M5-brane anomaly due to 

* [Witten 96](#Witten96)

left a remnant term of $\tfrac{1}{24} p_2$. It was argued in

* {#FreedHarveyMinasianMoore98} [[Dan Freed]], [[Jeff Harvey]], [[Ruben Minasian]], [[Greg Moore]], _Gravitational Anomaly Cancellation for M-Theory Fivebranes_, Adv.Theor.Math.Phys.2:601-618, 1998 ([arXiv:hep-th/9803205](https://arxiv.org/abs/hep-th/9803205))

* {#HarveyMinasianMoore98b} [[Jeff Harvey]], [[Ruben Minasian]], [[Greg Moore]], _Non-abelian Tensor-multiplet Anomalies_, JHEP9809:004, 1998 ([arXiv:hep-th/9808060](https://arxiv.org/abs/hep-th/9808060))

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger, _Anomaly cancellation in M-theory: a critical review_, Nucl.Phys. B675 (2003) 416-446 ([arXiv:hep-th/0307152](https://arxiv.org/abs/hep-th/0307152))

that this term disappears (cancels) when properly taking into account the singularity of the [[supergravity C-field]] at the locus of the [[black brane|black]] [[M5-brane]].

This argument is recalled in

* {#Harvey05} [[Jeffrey Harvey]], Section 5 of : _TASI 2003 Lectures on Anomalies_ ([arXiv:hep-th/0509097](https://arxiv.org/abs/hep-th/0509097), [spire:692082](http://inspirehep.net/record/692082))

* {#BahBonettiMinasianNardoni18} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], [[Emily Nardoni]], _Class $\mathcal{S}$ Anomalies from M-theory Inflow_, Phys. Rev. D 99, 086020 (2019) ([arXiv:1812.04016](https://arxiv.org/abs/1812.04016))

* {#BBMN19} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], [[Emily Nardoni]], _Anomaly Inflow for M5-branes on Punctured Riemann Surfaces_,  J. High Energ. Phys. 2019, 123 (2019)
([arXiv:1904.07250](https://arxiv.org/abs/1904.07250))

Amplification that the term $G_4^{M5}$ needs to be discussed (denoted $\gamma_4$ there:

* {#BBMN19b} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], [[Emily Nardoni]], _Anomalies of QFTs from M-theory and Holography_, J. High Energ. Phys. 2020, 125 (2020) ([arXiv:1910.04166](https://arxiv.org/abs/1910.04166))


* {#BahBonettiMinasian20} [[Ibrahima Bah]], [[Federico Bonetti]], [[Ruben Minasian]], _Discrete and higher-form symmetries in SCFTs from wrapped M5-branes_, J. High Energ. Phys. 2021, 196 (2021) ([arXiv:2007.15003](https://arxiv.org/abs/2007.15003))



Argument that the remaining anomaly term $[G_4^{M5}]^2$ vanishes, by [[schreiber:Hypothesis H]]:

* {#SS20a} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5-brane anomaly cancellation]]_ ([arXiv:2002.07737](https://arxiv.org/abs/2002.07737))


### Double dimensional reduction to D4-brane

The relation of the M5-brane to the [[D4-brane]] and the [[D=5 super Yang-Mills theory]] in its [[worldvolume]] [[physical theory|theory]] by [[double dimensional reduction]]:

* [[Eric Bergshoeff]], Mees de Roo, Tomas Ortin, _The Eleven-dimensional Five-brane_ ([pdf](http://astro.eldoc.ub.rug.nl/FILES/root/Preprints/1996/Eleven-dimensional/eleven-dimensional_five-brane.pdf))

* [APPS 97a, Section 6](#APPS97a)

* {#APPS97b} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], Section 6 of _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))

* [[Neil Lambert]], Constantinos Papageorgakis, Maximilian Schmidt-Sommerfeld, _M5-Branes, D4-Branes and Quantum 5D super-Yang-Mills_, JHEP 1101:083 (2011) ([arXiv:1012.2882](http://arxiv.org/abs/1012.2882))

* [[Chong-Sun Chu]], Sheng-Lan Ko, _Non-abelian Action for Multiple Five-Branes with Self-Dual Tensors_, ([arXiv:1203.4224](http://arxiv.org/abs/1203.4224)) JHEP05(2012)028

* [[Neil Lambert]], Miles Owen, _Charged Chiral Fermions from M5-Branes_ ([arXiv:1802.07766](https://arxiv.org/abs/1802.07766))


See also ([Witten 11](#Witten11)).

### Open M5-branes

Discussion of open M5-branes ending on [[M9-branes]] in a [[Yang monopole]] is in 

* [[Eric Bergshoeff]], [[Gary Gibbons]], [[Paul Townsend]], _Open M5-branes_, Phys.Rev.Lett.97:231601 2006 ([arXiv:hep-th/0607193](http://arxiv.org/abs/hep-th/0607193))




### Nonabelian 2-form fields

The fact that the worldvolume theory of the M5-brane should support fields that are [[self-dual higher gauge theory|self-dual]] [[connections on a 2-bundle]] ($\sim$ a [[gerbe]]) is discussed in 

* {#Witten07} [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_, in [[Ulrike Tillmann]], _Topology, Geometry and Quantum Field Theory: Proceedings of the 2002 Oxford Symposium in Honour of the 60th Birthday of Graeme Segal_,  London Mathematical Society Lecture Note Series (2004) ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))
 

as well as sections 3 and 4 of 

* {#Witten09} [[Edward Witten]], _Geometric Langlands From Six Dimensions_ ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720))
 

Proposals for how to implement this are for instance in

* [[Chong-Sun Chu]], _A Theory of Non-Abelian Tensor Gauge Field with Non-Abelian Gauge Symmetry $G \times G$_ ([arXiv:1108.5131](http://arxiv.org/abs/1108.5131))

* [[Henning Samtleben]], [[Ergin Sezgin]], Robert Wimmer, _(1,0) superconformal models in six dimensions_ ([arXiv:1108.4060](http://arxiv.org/abs/1108.4060))
 {#SSW11}

A formal proposal is [[schreiber:7d Chern-Simons theory and the 5-brane|here]].

### More on the holographic description

* [[Alexei Nurmagambetov]], I. Y. Park, _On the M5 and the AdS7/CFT6 Correspondence_ ([arXiv:hep-th/0110192](http://arxiv.org/abs/hep-th/0110192))

### More on the algebraic topology

* {#Witten2000} [[Edward Witten]], _Duality relations among topological effects in string theory_, J. High Energy Phys. 0005 (2000) 031 ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))
 

* {#Sati10} [[Hisham Sati]], _Geometric and topological structures related to M-branes II: Twisted String and String^c structures_ ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419))
 

* {#Sati} [[Hisham Sati]], _Twisted topological structures related to M-branes II: Twisted $Wu$ and $Wu^c$ structures_ ([arXiv:1109.4461](http://arxiv.org/abs/1109.4461))
 

[[!redirects M5-branes]]

[[!redirects M5-brane]]
[[!redirects M5-branes]]

[[!redirects M5]]

