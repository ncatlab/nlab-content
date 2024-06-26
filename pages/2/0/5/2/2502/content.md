[[!redirects super Poincare Lie algebra]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _super Poincar&#233; Lie algebra_ is a [[super Lie algebra]] extension of a [[Poincaré Lie algebra]]. 

The corresponding [[super Lie group]] is the [[super Euclidean group]] (except for the signature of the metric).

## Definition
 {#Definition}

Let $d \in \mathbb{N}$ and consider [[Minkowski spacetime]] $\mathbb{R} ^{d-1,1}$ of [[dimension]] $d$. For $Spin(d-1,1)$ the corresponding [[spin group]], let 

$$
  S \in Rep(Spin(d-1,1))
$$

be a real [[spin representation]] ([[Majorana spinor]]), which has the property ([def.](Majorana+spinor#SpinorToVectorBilinearPairing), [prop.](Majorana+spinor#SpinorToVectorPairing)) that there exists a [[linear map]]

$$
  \Gamma \;\colon\; S \otimes S \longrightarrow \mathbb{R}^{d-1,1}
$$

which is

1. symmetric:

1. $Spin(V)$ [[equivariance|equivariant]] (a [[homomorphism]] of [[spin representations]]).

For a classification of spin representations with this property see at _[[spin representations]]_ the sections _[real irreducible spin representations in Lorentz signature](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature)_ and _[super Poincar&#233; brackets](spin+representation#SuperPoincareBrackets)_. For explicit construction in components see at _[[Majorana spinor]]_ the section _[The spinor pairing to vectors](Majorana+spinor#TheSpinorPairingToVectors)_.

+-- {: .num_defn #SuperPoincare}
###### Definition

The **super Poincar&#233; Lie algebra** $\mathfrak{siso}_S(d-1,1)$ of $d$-dimensional [[Minkowski spacetime]] with respect to the [[spin representation]] $S$ with symmetric and $Spin(V)$-equivariant pairing $\Gamma \colon S \otimes S \to \mathbb{R}^{d-1,1}$ is the [[super Lie algebra|super]] [[Lie algebra extension]] of the [[Poincaré Lie algebra]] by $\Pi S$ (the [[vector space]] underlying $S$ taken in odd degree)

$$
  \Pi S \longrightarrow \mathfrak{siso}_S(d-1,1)
  \longrightarrow \mathfrak{iso}(d-1,1) \simeq \mathbb{R}^{d-1,1} \ltimes \mathfrak{so}(d-1,1)
  \,,
$$

where the [[Lie bracket]] of elements in $\mathfrak{so}(d-1,1)$ with those in $S$ is the given [[action]], the Lie bracket of elements of $\mathbb{R}^{d-1,1}$ with those on $S$ is trivial, and the Lie bracket of two elements $s_1, s_2 \in S$ is given by $\Gamma$:

$$
  [s_1,s_2] \coloneqq \Gamma(s_1,s_2)
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

It is precisely the symmetry and $Spin(V)$-equivariant assumption on $\Gamma$ that makes this a well defined [[super Lie algebra]]: the symmetry corresponds to the graded skew-symmetry of the [[Lie bracket]] on elements in $S$, which are regarded as odd, and the $Spin(V)$-equivariance yields the nontrivial [[Jacobi identity]] for $o \in \mathfrak{so}(d-1,1)$ and $s_1, s_2 \in S$:

$$
  \Gamma([o,s_1], s_2)
  +
  \Gamma(s_1, [o,s_2])
  = 
  [o, \Gamma(s_1,s_2)]
  \,.
$$

=--

+-- {: .num_remark #CEAlgebraOfSuperPoincare}
###### Remark

By the general discussion at [[Chevalley-Eilenberg algebra]], we may characterize the [[super Poincaré Lie algebra]] $\mathfrak{siso}_S(D-1,1)$ by its CE super-[[dg-algebra]] $CE(\mathfrak{siso}_S(D-1,1))$ "of [[left-invariant 1-forms]]" on its group manifold.

Write $\{\omega_a{}^b\}_{a,b}$ for the canonical basis of the [[special orthogonal Lie algebra|special orthogonal]] [[matrix Lie algebra]] $\mathfrak{so}(D-1,1)$ and write $\{\psi_\alpha\}_\alpha$ for a corresponding [[basis]] of the [[spin representation]] $S$.

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}_N(d-1,1))$ is generated on 

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \psi = \frac{1}{4} \omega^{ a b} \wedge \Gamma_{a b} \psi
  \,.
$$


=--

+-- {: .num_remark }
###### Remark

Removing all terms involving $\omega$ here yields the [[Chevalley-Eilenberg algebra]] of the [[super translation algebra]] $\mathbb{R}^{D;N}$.

=--


+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is 

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

This then gives the formula for the differential of the super-[[vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

$$ 
  \begin{aligned}
    d e^a & = d (d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta)
    \\
    & = \frac{i}{2} d \overline{\theta}\Gamma^a d \theta
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$


=--



## Properties

### Lie algebra cohomology
 {#LieAlgebraCohomology}

The super Poincar&#233; Lie algebra has, on top of the [[Lie algebra cohomology|Lie algebra cocycles]] that it inherits from $\mathfrak{so}(n)$, a discrete number of exceptiona cocycles bilinear in the spinors, on the [[super translation algebra]], that exist only in very special dimensions.

The following theorem has been stated at various placed in the physics literature (known there as the _[[brane scan]]_ for $\kappa$-symmetry in _[[Green-Schwarz action functionals]]_ for super-$p$-[[branes]] on [[super-Minkowski spacetime]]). A full proof is in [Brandt 12-13](#Brandt12-13). The following uses the notation in terms of [[division algebras]] ([Baez-Huerta 10](#BaezHuerta10)).

**Theorem**

* In dimensional $d =  3,4,6, 10$, $\mathfrak{siso}(d-1,1)$ has a nontrivial 3-cocycle given by

  $$
    (\psi, \phi, A) \mapsto g(\psi \cdot \phi, A)
  $$

  for spinors $\psi, \phi \in \mathcal{S}$ and vectors $A \in \mathcal{T}$, and 0 otherwise.

* In dimensional $d =  4,5,7, 11$, $\mathfrak{siso}(d-1,1)$ has a nontrivial 4-cocycle given by
 
  $$
    (\Psi, \Phi, \mathcal{A}, \mathcal{B}) \mapsto 
    \langle \Psi , (\mathcal{A}\mathcal{B}- \mathcal{B} \mathcal{A})\Phi \rangle
  $$

  for spinors $\Psi, \Phi \in \mathcal{S}$ and vectors $\mathcal{A}, \mathcal{B} \in \mathcal{V}$, with the commutator taken in the Clifford algebra.

The 4-cocycle in $d = 11$ is the one that induces the [[supergravity Lie 3-algebra]].

All these cocycles are controled by the relevant [[Fierz identities]].

### Extensions 

#### Super $L_\infty$-algebra extensions

The [[super L-infinity algebra]] [[infinity-Lie algebra cohomology]] of the super Poincar&#233; Lie algebra corresponding to the [above](#LieAlgebraCohomology) cocycles involves

[[supergravity Lie 6-algebra]] $\to$ [[supergravity Lie 3-algebra]] $\to$ **super-Poincar&#233; Lie algebra**


#### Extended super Poincar&#233; Lie algebra -- Polyvector extensions
 {#PolyvectorExtensions}

The super-Poincar&#233; Lie algebra has a class of super [[Lie algebra extensions]] called _[[extended supersymmetry]]_ algebras or _polyvector extensions_ , because they involve additional generators that transforn as skew-symmetric [[tensors]]. A complete classification is in ([ACDP](#ACDP)).

For instance the "[[M-theory Lie algebra]]" is a polyvector extension of the super Poincar&#233; Lie algebra $\mathfrak{siso}_{N=1}(10,1)$ by polyvectors of rank $p = 2$ and $p=5$ (the [[M2-brane]] and the [[M5-brane]] in the [[brane scan]]), see below [Polyvector extensions as automorphism Lie algebras](#PolyvectorExtensionsAsAutomorphismLieAlgebras).

##### As current algebras of the GS super $p$-branes

The polyvector extensions arise as the super Lie algebras of [[conserved currents]] of the [[Green-Schwarz super p-brane sigma-models]] ([AGIT 89](#AGIT89)).

##### As automorphism Lie algebras of Lie $n$-superalgebras
 {#PolyvectorExtensionsAsAutomorphismLieAlgebras}

At least some of the [polyvector extensions](#PolyvectorExtensions) of the super Poincar&#233; Lie algebra arise as the [[automorphism]] super Lie algebras of the [[Lie n-algebra]] 
[[infinity-Lie algebra cohomology|extensions]] classified by the cocycles discussed above.

For instance the automorphisms of the [[supergravity Lie 3-algebra]] gives the "[[M-theory Lie algebra]]"-extension of super-Poincar&#233; in 11-dimensions ([FSS 13](#FSS13)). This is also discussed at _[supergravity Lie 3-algebra -- Polyvector extensions](supergravity+Lie+3-algebra#Polyvector)_.

### Contractions
 {#Contractions}

One may consider [[symmetry breaking|breaking]] super-Poincaré invariance by passage to non-relativistic or ultrarelativistic limits, formally understood as taking the [[speed of light]] to [[infinity|$\infty$]] or to [[zero|0]], respectively, referred to as *Galilean* of *Carrollian* [[limit of a sequence|limits]], respectively. This is achieved via the process of [[Lie algebra contraction|contraction]], as described in [İnönü & Wigner 1953](#IW53).

The corresponding super Lie algebras are defined as follows (see e.g. Section 2 of [Koutrolikos & Najafizadeh 2023](#KN23)). We denote the generators of the $4d$ $N=1$ super-Poincaré algebra as $\{ J_{\mu\nu}, P_{\mu}, Q_{\alpha}, \bar{Q}_{\dot \alpha} \}$.

The **super-Carroll** algebra is defined by the rescaled generators 

$$
  \Big\{K^C _i \coloneqq c J_{0i} , P^C _0 \coloneqq c P_0, J_{ij} ^C \coloneqq J_{ij} , P_{i} ^C \coloneqq P_{i}, Q^C _{\alpha} \coloneqq \sqrt{c} Q_{\alpha} , \bar{Q}^C _{\dot \alpha} \coloneqq \bar{Q} _{\dot \alpha} \Big\}
$$ 
satisfying the commutation relations inherited from the super-Poincaré algebra, with the exceptions that now the commutators


$$
  \begin{array}{lcl}
  [K^{^{(\rm{C})}}_i ,J^{C}_{jk} ] 
  &=&
  - i \delta_{i[j} K^{C}_{k]}
  \\
  [J^{C}_{ij} ,J^{C}_{kl} ] 
  &=&
  i \big(
    \delta_{[i|k|} J^{C}_{j]l}  
    - \delta_{[i|l|} J^{C}_{j]k} 
  \big)
  \\
  [K^{C}_i ,P^{C}_j ] 
  &=&
  -i \delta_{ij} P^{C}_0
  \\
  [J^{C}_{ij} ,P^{C}_k ] 
  &=&
  i \delta_{[i|k|}P^{C}_{j]}
  \\
  [J^{C}_{ij}, Q^{C}_{\alpha} ] 
  &=&
  (\sigma_{ij} )_{\alpha} ^{\beta} Q^{C}_{\beta}
  \\
  [J^{C}_{ij}, \bar{Q}^{C}_{\dot\alpha} ] 
  &=&
  (\bar{\sigma }_{ij})_{\dot\alpha}^{\dot\beta} 
  \bar{Q}^{C}_{\dot\beta}
  \\
  \{Q^{C}_{\alpha},\bar{Q}^{C}_{\dot\alpha}\} 
  &=&
  -(\sigma^0 )_{\alpha\dot\alpha} P^{C}_0
  \,.
  \end{array}
$$

The **super-Galilean** algebra is defined with generators

$$
  \Big\{
    K^{G}_i = \frac{1}{c} J_{0i} , P^{G}_0 = c P_0 , Q^{G}_{\alpha} = Q_{\alpha}, J^{G}_{ij} = J_{ij}, P^{G}_{i} = P_{i}, \bar{Q}^{G}_{\dot\alpha} =
Q_{\dot\alpha} 
  \Big\}
$$ 

and the following non-zero commutators:

$$
  \begin{array}{lcl}
  [K^{G}_i ,J^{G}_{jk} ] 
  &=&
  -i \delta_{i[j} K^{G}_{k]}
  \\
  [J^{G}_{ij}, J^{G}_{kl} ] 
  &=&
  i(\delta_{[i|k|} J^{G}_{j]l} - \delta_{[i|l|}J^{G}_{j]k} )
  \\
  [K^{G}_i ,P^{G}_0 ] 
  &=&
  - i P^{G}_i
  \\
  [J^{G}_{ij}, P^{G}_k ] 
  &=&
  i \delta_{[i|k|} P^{G}_{j]}
  \\
  [J^{G}_{ij},Q^{G}_{\alpha} ] 
  &=&
  (\sigma_{ij} )_{\alpha}^{\beta} Q^{G}_{\beta}
  \\
  [J^{G}_{ij}, \bar{Q}^{G}_{\dot\alpha} ] 
  &=&
  (\bar{\sigma}_{ij})_{\dot\alpha}^{\dot\beta} \bar{Q}^{G}_{\dot\beta}
  \\
  \{Q^{G}_{\alpha},\bar{Q}^{G}_{\dot\alpha}\} 
  &=& 
  -(\sigma^i)_{\alpha\dot\alpha} P^{G}_i
  \,.
  \end{array}
$$

See [Bergshoeff et al. 2023](#BFG23) and the references therein for more.

## Related concepts

* [[super Minkowski spacetime]], [[signs in supergeometry]]

* [[super Poincaré group]], [[supersymmetry]]

* [[supermultiplet]], [[BPS state]]

* [[division algebra and supersymmetry]]

* [[R-symmetry]]

* [[super translation algebra]]

* [[Green-Schwarz action functional]], [[brane scan]]

* [[4d supergravity Lie 2-algebra]], [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]

## References

Introducing the [[super Poincaré Lie algebra]] ("[[supersymmetry]]"):

* {#GolfandLikhtman72} [[Yuri Golfand]], [[Evgeny Likhtman]],_On the Extensions of the Algebra of the Generators of the Poincaré Group by the Bispinor Generators_, in: [[Victor Ginzburg]] et al. (eds.) _I. E. Tamm Memorial Volume Problems of Theoretical Physics_, (Nauka, Moscow 1972), page 37, 

  translated and reprinted in: [[Mikhail Shifman]] (ed.) _[[The Many Faces of the Superworld]]_ pp. 44-53,  World Scientific (2000) ([doi:10.1142/9789812793850_0006](https://doi.org/10.1142/9789812793850_0006))

### General

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.2.1 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)


The seminal classification result of simple supersymmetry algebras is due to 

* [[Werner Nahm]], _Supersymmetries and their Representations_, Nucl.Phys. B135 (1978) 149 ([spire](http://inspirehep.net/record/120988?ln=en))


Lecture notes include

* _Super spacetimes and super Poincar&#233;-group_ ([pdf](http://www.math.ucla.edu/~vsv/papers/ch6.pdf))

* {#Freed01} [[Daniel Freed]], lecture 6 of _Classical field theory and Supersymmetry_, IAS/Park City Mathematics Series Volume 11 (2001) ([pdf](https://www.ma.utexas.edu/users/dafr/pcmi.pdf))

* [[Daniel Freed]], _Lecture 4 of [[Five lectures on supersymmetry]]_

* {#Varadarajan04} [[Veeravalli Varadarajan]], section 7 of _[[Supersymmetry for mathematicians]]: An introduction_, Courant lecture notes in mathematics, American Mathematical Society, Providence, R.I (2004)
  


See also

* {#CAIB99} C. Chrysso‌malakos, [[José de Azcárraga]], [[José M. Izquierdo]], C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nucl. Phys. B **567** (2000) 293-330  &lbrack;[arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137), <a href="https://doi.org/10.1016/S0550-3213(99)00512-X">doi:10.1016/S0550-3213(99)00512-X</a>&rbrack;

for discussion in the view of the [[brane scan]] and [[schreiber:The brane bouquet]] of super-$p$-[[brane]] [[Green-Schwarz sigma-models]].


### Polyvector extensions
 {#PolyvectorExtensionRefs}

The Polyvector extensions of $\mathfrak{Iso}(\mathbb{R}^{10,1|32})$ (the "[[M-theory super Lie algebra]]") were first considered in 

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]] _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 

 * [[Jan-Willem van Holten]], [[Antoine Van Proeyen]], _$N=1$ supersymmetry algebras in $d=2,3,4 \,mod\, 8$_ J.Phys. A15, 3763 (1982).

Polyvector extensions were found as the algebra of [[conserved currents]] of the [[Green-Schwarz super p-branes]] in

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys.Rev.Lett. 63 (1989) 2443 ([spire](https://inspirehep.net/record/26393?ln=en))

reviewed in section 8.8. of 

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

and specifically for super-[[D-branes]] this discussion is in 

* Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))

The role of polyvector extended supersymmetry algebras in [[supergravity]] and [[string theory]] is further highlighted in

* [[Paul Townsend]], _$p$-Brane Democracy_ ([arXiv:hep-th/9507048](http://arxiv.org/abs/hep-th/9507048))


A comprehensive account and classification of the polyvector extensions of the super Poincar&#233; Lie algebras is in

* {#ACDP} [[Dmiti Alekseevsky]], [[Vicente Cortés]], C. Devchand, [[Antoine Van Proeyen]], _Polyvector Super-Poincar&#233; Algebras_ Commun.Math.Phys. 253 (2004) 385-422 ([arXiv:hep-th/0311107](http://arxiv.org/abs/hep-th/0311107))
 



### Super Lie algebra cohomology
 {#ReferencesLieAlgebraCohomology}

Discussion of the super-[[Lie algebra cohomology]] of the [[super Poincare Lie algebra]] goes back to work on [[Green-Schwarz sigma models]] in

* {#AzcarragaTownsend89} [[José de Azcárraga]], [[Paul Townsend]], *Superspace geometry and classification of supersymmetric extended objects*, Phys. Rev. Lett. **62**  (1989) 2579-2582 &lbrack;[doi:10.1103/PhysRevLett.62.2579](https://doi.org/10.1103/PhysRevLett.62.2579), [spire:284635](https://inspirehep.net/literature/284635)&rbrack;
 

A rigorous classification of these cocycles was later given in

* {#Brandt12-13} [[Friedemann Brandt]], _Supersymmetry algebra cohomology_ 

  _I: Definition and general structure_  J. Math. Phys.51:122302, 2010, ([arXiv:0911.2118](http://arxiv.org/abs/0911.2118))

  _II: Primitive elements in 2 and 3 dimensions_, J. Math. Phys. 51 (2010) 112303 ([arXiv:1004.2978](http://arxiv.org/abs/1004.2978))

  _III: Primitive elements in four and five dimensions_, J. Math. Phys. 52:052301, 2011 ([arXiv:1005.2102](http://arxiv.org/abs/1005.2102))

  _IV: Primitive elements in all dimensions from $D=4$ to $D=11$_, J. Math. Phys. 54, 052302 (2013) ([arXiv:1303.6211](http://arxiv.org/abs/1303.6211))
 

A classification of some special cases of signature/supersymmetry of this is also in the following (using a computer algebra system):

* [[Mikhail Movshev]], [[Albert Schwarz]], Renjun Xu, _Homology of Lie algebra of supersymmetries_ ([arXiv:1011.4731](http://arxiv.org/abs/1011.4731)) 

* [[Mikhail Movshev]], [[Albert Schwarz]], Renjun Xu, _Homology of Lie algebra of supersymmetries and of super Poincar&#233; Lie algebra_, Nuclear Physics B Volume 854, Issue 2, 11 January 2012, Pages 483&#8211;503 ([arXiv:1106.0335](http://arxiv.org/abs/1106.0335))

For applications of this classification see also at _[[Green-Schwarz action functional]]_ and at _[[brane scan]]_.

An introduction to the exceptional fermionic cocycles on the super Poincar&#233; Lie algebra, and their description using 
[[normed division algebras]], are discussed here:

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_ ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))
 {#BaezHuerta10}

* [[John Huerta]], _Division Algebras, Supersymmetry and Higher Gauge Theory_, ([arXiv:1106.3385](http://arxiv.org/abs/1106.3385))

This subsumes some of the results in ([Azc&#225;rraga-Townend](#AzcarragaTownsend89))

Discussion of the corresponding [[super L-∞ algebra]] [[L-∞ extensions]] in the context of [[Green-Schwarz action functionals]] and [[schreiber:∞-Wess-Zumino-Witten theory]] is in 

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 

A direct constructions of ordinary (Lie algebraic) extensions of the super Poincar&#233; Lie algebra by means of [[division algebras]] is in

* Jerzy Lukierski, Francesco Toppan, _Generalized Space-time Supersymmetries, Division Algebras and Octonionic M-theory_ ([pdf](http://cbpfindex.cbpf.br/publication_pdfs/NF00102.2010_08_03_10_47_48.pdf))

For more on this see at _[[division algebra and supersymmetry]]_.

On the notion of contraction used for non-Lorentzian limits:

* {#IW53} [[Erdal İnönü]], [[Eugene Wigner]]. *On the Contraction of Groups and Their Representations*. Proceedings of the National Academy of Sciences 39, no. 6 (1953): 510-524. ([doi](https://doi.org/10.1073/pnas.39.6.510)).

Discussion of the Carrollian- and Galilean limits:

* {#KN23} Konstantinos Koutrolikos, Mojtaba Najafizadeh. *Super-Carrollian and super-Galilean field theories.* Physical Review D 108, no. 12 (2023): 125014. ([doi](https://doi.org/10.1103/PhysRevD.108.125014)).

* {#BFG23} [[Eric Bergshoeff]], [[José Figueroa-O'Farrill]], and [[Joaquim Gomis]]. *A non-lorentzian primer.* SciPost Physics Lecture Notes (2023): 069. ([doi](https://doi.org/10.21468/SciPostPhysLectNotes.69)).


[[!redirects super Poincare Lie algebras]]

[[!redirects super Poincaré Lie algebra]]
[[!redirects super Poincaré Lie algebras]]

[[!redirects super Poincaré super Lie algebra]]
[[!redirects super Poincaré super Lie algebras]]

[[!redirects super-Poincaré Lie algebra]]
