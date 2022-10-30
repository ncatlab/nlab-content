
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyics
+--{: .hide}
[[!include physicscontents]]
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

The _Green-Schwarz action functional_ is the [[action functional]] of a [[sigma-model]] that describes the propagation of a fundamental $p$-[[brane]] $\Sigma$ on a [[supermanifold]] [[spacetime]].

* For $p = 0$ this is the **Green-Schwarz [[superparticle]]**.

* For $p = 1$ the **Green-Schwarz [[superstring]]** (at the center of attention in [[string theory]]).

  This model is in contrast to the [[NSR-string]], which instead has manifest [[worldsheet]] [[supersymmetry]]. See at _[[superstring]]_ for more on this.

## Definition

The Green-Schwarz action functionals are of the standard [[sigma-model]] form for [[target spaces]] that are [[supermanifold|super]]-[[homogeneous spaces]]  $G/H$ for $G$ a [[Lie supergroup]] and $H$ a sub-super-group, and for  [[background gauge fields]] that are 
super-[[WZW model|WZW]]-[[circle n-bundles with connection]]/[[bundle gerbes]] on $G$.

* for branes on [[super Minkowski spacetime]]: $\mathfrak{g}$ is the [[super Poincaré Lie algebra]] and $\mathfrak{h}$ the [[Lorentz Lie algebra]];


These action functionals were first considered in ([Green-Schwarz 84](#GreenSchwarz84)) for [[superstrings]] in various dimensions. The full interpretation of the action functional as an higher [[Wess-Zumino-Witten theory]]-type action controled by the [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] (or rather of the [[super translation Lie algebra]] inside it)  is due to ([Azc&#225;rraga-Townsend89](#AzcarragaTownsend89)).

* for branes on [[super anti de Sitter spacetime]], $G$ is a [[superconformal group]] (e.g. [Metsaev-Tseytlin 98, section 3](#MetsaevTseytlin98))


### Supercoordinates
 {#Supercoordinates}

We briefly review some basics of the canonical [[coordinates]] and the super [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] and [[super Minkowski space]], which are referred to below (see for instance [Azc&#225;rraga-Townsend 89](#AzcarragaTownsend89), and see at _[[super Cartesian space]]_ and at _[[signs in supergeometry]]_.).

By the general discussion at [[Chevalley-Eilenberg algebra]], we may characterize the [[super Poincaré Lie algebra]] $\mathfrak{siso}(D-1,1)$ by its CE-algebra $CE(\mathfrak{siso}(D-1,1))$ "of [[left-invariant 1-forms]]" on its group manifold.

+-- {: .num_defn #CEAlgebraOfSuperPoincare}
###### Definition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}(d-1,1))$ is generated on 

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
  d_{CE} \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Removing the terms involving $\omega$ here this is the [[super translation algebra]].

=--

In this way the super-Poincar&#233; Lie algebra and its extensions is usefully discussed for instance in ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and in ([Azc&#225;rraga-Townsend 89](AzcarragaTownsend89), [CAIB 99](#CAIB99)). In much of the literature instead the following equivalent notation is popular, which more explicitly involves the [[coordinates]] on [[super Minkowski space]].

+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] (= [[super Minkowski space]]) as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is 

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

Notice that this then gives the above formula for the differential of the [[super-vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

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


+-- {: .num_remark }
###### Remark

The term $\frac{i}{2}\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \frac{i}{2}\bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{siso})$ which have "all indices contracted". (See also at _[[torsion constraints in supergravity]]_.)

Notably we have 

$$
  d \left( 
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \right)
  \propto
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
  \,.
$$

This remaining operation "$e \mapsto \Psi^2$" of the differential acting on Loretz scalars is sometimes denoted "$t_0$", e.g. in ([Bossard-Howe-Stelle 09, equation (8)](#BossardHoweStelle09)).

This relation is what govers all of the exceptional super Lie algebra cocycles that appear as WZW terms for the Green-Schwarz action below: for some combinations of $(D,p)$ a [[Fierz identity]] implies that the term

$$
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
$$

vanishes identically, and hence in these dimensions the term

$$
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a [[cocycle]]. See also the [brane scan](#BraneScan) table below.

=--


### Kinetic term

(...)

[[kinetic action]]

$$
  \int_\Sigma \langle \phi^\ast\Pi^a, \phi^\ast \Pi^b \eta_{a b}\rangle 
$$

(...)

### WZW term
 {#DefinitionWZWTerm}

Let $(e^a, \omega^{a b}, \psi^\alpha)$ be the standard generators
of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}(d,1))$ of the [[super Poincaré Lie algebra]], as discussed there.

The part of the [[Lie algebra cohomology]] of the super translation Lie algebra
that is invariant under the [[special orthogonal Lie algebra|Lorentz]]
transformations is spanned by closed elements of the form

$$
  \mu = 
  (d \bar \theta \Gamma_{a_1, \cdots, a_p} \wedge d \theta)
  \wedge
  \Pi^{a_1} \wedge \cdots \wedge \Pi^{a_p}
  \,.
$$

These exist (are closed) only for certain combinations of
$d$ and $p$. The possible values are listed [below](#BraneScan).

For a bosonic [[WZW model]] the [[background gauge field]]
induced by such a cocycle would be the corresponding [[Lie integration]]
to a [[circle n-bundle with connection]]. Here, since the super
translation group is contractible, a [[Poincaré lemma]] applies
and these circle $n$-connections are simply given by globally
defined [[connection on an infinity-bundle|connection]] form
$\beta$ satisfying

$$
  d \beta = \mu
  \,.
$$

The WZW part of the GS action is then 

$$
  S_{WZW } : \phi \mapsto \int_\Sigma \phi^* \beta
$$

(...) 


## Properties

### Siegel- or $\kappa$-symmetry
 {#KappaSymmetry}

The Green-Schwarz action has an extra fermionic symmetry, on top of the genuine supersymmetry, first observed in ([Siegel 83](#Siegel83)) for the [[superparticle]] and in ([Siegel 84](#Siegel84)) for the [[superstring]] in 3-dimensions, and finally in ([GreenSchwarz 84](#GreenSchwarz)) for the critical superstring in 10-dimensions. This is also called **$\kappa$-symmetry**. It has a natural interpretation in terms of the [[supergeometry|super]]-[[Cartan geometry]] of [[target space]] ([McArthur](#McArthur), [GKW](#GKW)). Discussion from the point of view of the [[D'Auria-Fré formulation of supergravity]] is in ([AFFFTT 98, section 3](#AFFFTT98), [Fr&#233;-Grassi 07, section 2.2](#FreGrassi07)).



### Dimensions -- the brane scan
 {#BraneScan}

The Green-Schwarz action functional of a $p$-brane propagating on an $d$-dimensional target spacetimes makes sense only for special combinations of $(p,d)$, for which there are suitanble [[Lie algebra cohomology|super Lie algebra cocycles]] on the super translation Lie algebra
(see [above](#DefinitionWZWTerm)).

The corresponding table has been called the **brane scan** in the literature, now often called the "old brane scan", since it has meanwhile been further completed (see below). In ([Duff 87](#Duff87)) the "old brane scan" is displayed as follows.

[[branescan.gif:pic]]

In the $D = 10$-row we see the critical [[superstring]] of [[string theory]] and
its [[electric-magnetic duality|magnetic dual]], the [[NS5-brane]].
The top row shows the [[M2-brane]] in [[11-dimensional supergravity]]. 

Moving down and left the diagonals corresponds to _[[double dimensional reduction]]_.


+-- {: .num_remark }
###### Remark

The first non-empty column of the table is a reflection of the exceptional isomorphisms of the [[spin group]] in low dimensions and the [[normed division algebras]]:

[[!include exceptional spinors and division algebras -- table]]

=--

+-- {: .num_remark }
###### Remark

What is missing in the "old brane scan" are the [[D-branes]] in $D = 10$ and the [[M5-brane]] in $D = 11$ (See also [BPST](#BPST)).
The reason is that the M5 corresponds to a 7-cocycle not on the ordinary [[super Poincaré Lie algebra]], but on its [[infinity-Lie algebra cohomology|L-infinity algebra extension]], the [[supergravity Lie 3-algebra]]. The completion in [[super L-infinity algebra]] theory is discussed in ([FSS 13](#FiorenzaSatiSchreiber13)), as _[[schreiber:The brane bouquet]]_.

=--


So (with notation as [above](#Supercoordinates)) we have the following.

[[!include brane scan]]


### On curved spacetime and supergravity equations of motion 
 {#OnCurvedSpacetime}


In the [[first order formulation of gravity]]
a [[field (physics)|field]] configuration on a [[spacetime]]
[[manifold]] $X$ is a [[Cartan connection]]

$$
  \nabla \colon X \to \mathbf{B} SuperPoincare(d-1,1)_{conn}  
$$

hence a [[principal connection]] for the [[super Poincaré group]] such such that at each point $x \in X$ it identifies the [[tangent space]] with $\mathbb{R}^{d;N} = \mathfrak{siso}(d-1,1)/\mathfrak{o}(d-1,1)$

$$
  T_x X \stackrel{\nabla}{\longrightarrow}
  \mathfrak{siso}(d-1,1)
  \longrightarrow
  \mathbb{R}^{d;N}
  \,.
$$ 

Hence given a [[Lie algebra cocycle]] 

$$
  \mathfrak{g} \longrightarrow \mathbb{R}[2]
$$

as for the Green-Schwarz superstring we can [[pullback of differential forms|pull it back]] along this [[Cartan connection]] to a [[differential 3-form]] on [[spacetime]].

In general this 3-form is no longer _closed_. If it is closed, then the Green-Schwarz superstring is again well defined on $(X,\nabla)$ as a [[WZW model]]. 

 The claim now is that requiring this 3-form still to be closed is, as a condition on the field of [[gravity]] $\nabla$, precisely the [[equations of motion]] of [[supergravity]] (the super-[[Einstein equations]]).

This is due to ([Nilsson 81](#Nilsson81), [Bergshoeff-Sezgin-Townsend 86](#BergshoeffSezginTownsend86)) and others, see the references [below](#ReferencesSupergravityBackgroundEquationsOfMotion).

#### Membrane in 11d SuGra background
 {#MembraneIn11dSuGraBackground}

For the [[membrane]]([[M2-brane]]) in a background of [[11-dimensional supergravity]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87))
find that consistency requires that (in a given [[coordinate chart]] with [[super-vielbein field]] $(E^A) = (E^a, \Psi^\alpha)$) the 4-form flux is of the form


\[
  \label{HConstraintEquationForMembraneIn11d}
  \begin{aligned}
     H & = \overline{\Psi}\wedge\Gamma^{ab} \Psi \wedge E_a \wedge E_b + \mathbf{d}C_3
     \\
     & =
     \Gamma_{a b \alpha \beta} E^a \wedge E^b \wedge E^\alpha \wedge E^\beta + 
    \mathbf{d}C_3
  \end{aligned}
\]

where the first summand is the super-Lie algebra cocycle that classifies the [[supergravity Lie 3-algebra]] and the second is the [[field strength]] of the [[supergravity C-field]] proper (hence a purely bosonic differential form). In the second line we have rewritten this more manifestly in terms of the [[super-vielbein]] $(E^A) = (E^a, E^\alpha) = (E^a, \Psi^\alpha)$, this way the expression is directly analogous to that of definite 3-forms in the theory of [[G2-manifolds]] (see [this example](G2+manifold#DefiniteFormsInTermsOfVielbeinFields) for details).

Moreover the [[torsion]] tensor $T$ is to have its $(T^a)^\alpha{}_\beta$-component equal to $(\Gamma^a)^\alpha{}_\beta$, see at _[[torsion constraints in supergravity]]_.

In addition the [[Bianchi identities]] have to hold:

* $\nabla T^A = E^B \wedge R_{B}{}^{A}$

* $\nabla H = 0$ ([[covariant derivative|covariant constancy]]).

All this is implied by the [[equations of motion]] of [[11-dimensional supergravity]].

Notice that in view of the above analogy to [[G2-structure]], the covariant constancy condition is precisely the analog of [[G2-manifold]] structure.  

Discussion of this in the somewhat more streamlined [[D'Auria-Fré formulation of supergravity]] is in ([AFFFTT 98, section 3.1](#AFFFTT98)).

#### Heterotic string

Discussion that for the GS-version of the [[heterotic string]] consistency of the background is equivalent to the equations of motion of [[heterotic supergravity]] is in  ([Shapiro-Taylor 87](#ShapiroTaylor87)).

Discussion with the hetetoric gauge field included is in ([Atick-Dhar-Ratra 86](#AtickDharRatra86)).


#### Type II string

Discussion for the GS-version of the [[type II superstring]] in [[type II supergravity]]-backgrounds is in ([GHMNT 85](#GHMNT85)), and for the [[D-branes]] in type II in ([CGNSW 97](#CGNSW97)).


### Conserved currents
 {#ConservedCurrents}

The super-WZW term of the GS action functionals is invariant under [[supersymmetry] only up to a [[divergence]]. Hence the [[Noether theorem]] in its generality for "weak" symmetries applies and gives that the [[conserved currents]] receive an extra contribution from this divergence term. The resulting algebra is a central extension of the given [[super translation Lie algebra]], extending to the famous [polyvector extensions](super+Poincare+Lie+algebra#PolyvectorExtensions) "by brane charges" of the [[super Poincaré Lie algebra]] ([AGIT 89](#AGIT89)).

### As part of the AdS-CFT correspondence
 {#AsPartOfTheAdSCFTCorrespodence}

By the above discussion, Green-Schwarz super $p$-branes are consistent on [[superspacetimes]] that satisfy the respective higher [[supergravity]] [[equations of motion]]. These turn out to have solutions which exhibit [[black branes]] in essentially just the combinations of dimensions and supersymmetries that the original Green-Schwarz sigma-models exist in, hence they look like precisely like the [[non-perturbative quantum field theory|non-pertrubative]] avatars of whatever these [[sigma models]] give the [[perturbation theory]] of by [[second quantization]]. (See at [[black holes in string theory]] for more on this correspondence between branes in string perturbation theory and black branes in supergravity).

Moreover, the near-horizon geoemtries of these [[black branes]] is always [[anti de Sitter spacetime]] times orthogonal directions-.

Therefore it is natural to consider the perturbation of the Green-Schwarz sigma-models around their asymptotic embeddings into AdS spaces, hence effectively the perturbation theory of the degrees of freedom at those naked singularity at which the corresponding black brane sits.

After [[diffeomorphism]] [[gauge fixing]] one finds that the resulting field theories now on the $p$-brane [[worldvolumes]] are precisely the [[superconformal field theories]] for all the  [allowed superconformal supersymmetries](supersymmetry#ClassificationSuperconformalInDimgt2)

| $d$ | $N$ | [[superconformal super Lie algebra]] | [[R-symmetry]] | [[brane]] [[worldvolume]] theory |
|-----|-----|--|---|--|
| 3   |  $2k+1$ | $B(k,2) \simeq $ [[osp]]$(2k+1/4)$ | $SO(2k+1)$ | |
| 3   | $2k$ | $D(k,2)\simeq $ [[osp]]$(2k/4)$ | $SO(2k)$ | [[M2-brane]] |
| 4   | $k+1$  | $A(3,k)\simeq \mathfrak{sl}(4/k+1)$ | $U(k+1)$ | [[D3-brane]] |
| 5   |  1  | $F(4)$ | $SO(3)$  |  |
| 6   | $k$ | $D(4,k) \simeq$ [[osp]]$(8/2k)$ | $Sp(k)$  | [[M5-brane]] |

This is effectively the [[AdS-CFT correspondence]]. 

Detailed discussion of the above steps is in ([AFFFTT 98](#AFFFTT98), [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99)).

### Quantization

The [[quantization]] of the Green-Schwarz super $p$-brane [[sigma models]] is discussed in the literature in terms of [[light-cone gauge quantization]].

This is actually how the Green-Schwarz superstring was first introduced in ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82)) before its [[general covariance|generally covariant]] formulation was found in ([Green-Schwarz 84](#GreenSchwarz84)). A textbook account of this is in ([Green-Schwarz-Witten, section 5](#GreenSchwarzWitten)).

While, by the [[brane scan]] discussed above, the action functional for the Green-Schwarz superstring exists for target [[super Minkowski spacetimes]] of dimension $d = 3$, 4, 6, and 10, its [[light-cone gauge quantization]] produces a [[quantum anomaly]] for the spacetime [[Lorentz group]] symmetry in dimension $d = 4$ and $d = 6$. For $d = 10$ the anomaly disappears and the thus quantized Green-Schwarz string becomes equivalent to the quantum [[NSR string]], hence to "the" critical string (of [[heterotic string theory]], [[type II string theory]]). 

Curiously, the light-cone gauge quantization of the GS-string also does wor however for $d = 3$, see at _[[super 1-brane in 3d]]_ for more on this.

(...)


## Related concepts

* [[supersymmetry]]

* [[sigma-model]], [[brane]]

  * [[relativistic particle]], [[spinning particle]], [[superparticle]]

  * [[string]], [[spinning string]], [[superstring]]

  * [[membrane]]

## References 

### General

A precursor to the actual Green-Schwarz action functional is

* {#GreenSchwarz81} [[Michael Green]], [[John Schwarz]], _Supersymmetrical Dual String Theory_, Nucl. Phys. B 181 (1981) 502; 

* {#GreenSchwarz82} [[Michael Green]], [[John Schwarz]], _Supersymmetrical Dual String Theory. 2. Vertices and Trees_, Nucl. Phys. B 198 (1982) 252.

which presented a [[light-cone gauge quantization]] of superstring with manifest [[target space|target]] [[spacetime]] [[supersymmetry]]. 

The observation that this has a [[general covariance|generally covriant]] formulation lead to what is now called the Green-Schwarz action functional proper, for the superstring:

* {#GreenSchwarz84} [[Michael Green]], [[John Schwarz]], _Covariant description of superstrings_, Phys. Lett. B136 (1984), 367&#8211;370 ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))

* {#GreenSchwarzWitten} [[Michael Green]], [[John Schwarz]], _Properties of the Covariant Formulation of Superstring Theories_, Nucl. Phys. B 243 (1984) 285.
 
A standard textbook reference for the GS superstring is 

* [[Michael Green]], [[John Schwarz]], [[Edward Witten]], volume 1, section 5 of _Superstring theory_, 3 vols. Cambridge Monographs on Mathematical Physics

and a brief paragraph in Volume II, section 10.2, page 983 of

* [[Eric D'Hoker]], _String theory -- lecture 10: Supersymmetry and supergravity_ , in part 3 of

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

A more recent and more comprehensive review is

* [[Joan Simón]], _[Brane Effective Actions, Kappa-Symmetry and Applications](http://relativity.livingreviews.org/Articles/lrr-2012-3/)_, Living Reviews in relativity ([arXiv:1110.2422](http://arxiv.org/abs/1110.2422))


Review from the bigger perspective that also includes worlsheet supermanifolds is in 

* [[Dmitri Sorokin]], _Superbranes and Superembeddings_, Phys.Rept.329:1-101,2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))

The observation that the Green-Schwarz action functional is an example of a [[WZW-model]] on [[super-Minkowski spacetime]] is due to 

* {#HenneauxMezincescu85} [[Marc Henneaux]], Luca Mezincescu, _A Sigma Model Interpretation of Green-Schwarz Covariant Superstring Action_, Phys.Lett. B152 (1985) 340 ([web](http://inspirehep.net/record/15922?ln=en)) 
  
For more references on this WZW perspective see [below](#ReferencesWZWTerm).


For references on curved backgrounds see [below](#ReferencesSupergravityBackgroundEquationsOfMotion).

### WZW terms, super Lie algebra cohomology and the brane scan
 {#ReferencesWZWTerm}

The WZW nature of the second term in the GS action, recognized in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) is 
discussed in 

* {#Rabin87} [[Jeffrey Rabin]], _Supermanifold Cohomology and the Wess-Zumino Term
of the Covariant Superstring Action_, Cornmun. Math. Phys. 108, 375-389 (1987) ([Euclid](https://projecteuclid.org/euclid.cmp/1104116532))

an with its [[infinity-Lie theory|Lie theoretic]] meaning
made fully explicit (in "FDA" language) in 

* {#AzcarragaIzqierdo} [[José de Azcárraga]], Jos&#233; Izqierdo, chapter 8 of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_, Cambridge monographs of mathematical physics, (1995)
 

The original "brane scan" classification of GS action functionals by WZW terms is due to

* {#AETW87} Anna Ach&#250;carro, [[Jonathan Evans]], [[Paul Townsend]], [[David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire](http://inspirehep.net/record/22286?ln=en))
 

For $d = 11$ the relevant [[super Lie algebra]] [[Lie algebra cohomology|cocycles]] have also been discussed (but not related to the Green-Schwarz action functional) in 

* {#DAuriaFre82} [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)
 

A review is in 

* {#Duff87} [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 (1987) ([spire](https://inspirehep.net/record/248034?ln=de))


from which the above table is taken.

A decent systematic account of the principles of super Lie algebra cohomology in the GS-functional, of these cocycles is in the letter

* {#AzcarragaTownsend89} [[José de Azcárraga]], [[Paul Townsend]], _Superspace geometry and the classification of supersymmetric extended objects_, Physical Review Letters Volume 62, Number 22 (1989) ([spire](http://inspirehep.net/record/284635?ln=en))
 

and a detailed account building on this, which also discusses the GS/WZW terms for [[D-branes]] on the [[type II supergravity Lie 2-algebra]] (in its section 6) is in 

* {#CAIB99} C. Chrysso&#8204;malakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))

Systematic review and discussion of the 3- and 4-cocycles in the old [[brane scan]] via the relation between [[division algebras and supersymmetry]] is in

* {#BaezHuerta10} [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_, Adv. Math. Theor. Phys. 15 (2011), 1373-1410  ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))
 

See also

* I. Bars, C. Deliduman and D. Minic, Phys. Rev D59 (1999) 125004;
Phys. Lett. B457 (1999) 275. ([arXiv:hep-th/9812161](http://arxiv.org/abs/hep-th/9812161))

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

The Green-Schwarz-type action for the [[M5-brane]] was found in 

* {#BLNPST} [[Igor Bandos]], Kurt Lechner, Alexei Nurmagambetov, Paolo Pasti, [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_ ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))
 

* {#APPS} Mina Aganagic, Jaemo Park, Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_ ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))
 

The 7-cocycle on the [[supergravity Lie 3-algebra]] which gives the [[supergravity Lie 6-algebra]] appears in these articles (somewhat secretly) in equation ([BLNPST, equation (9)](#BLNPST)).

See also

* {#BPST} [[Igor Bandos]], Paolo Pasti, [[Dmitri Sorokin]], Mario Tonin, _Superbrane Actions and Geometrical Approach_ ([arXiv:hep-th/9705064](http://arxiv.org/abs/hep-th/9705064))
 

The 7-cocycle for the M5-brane on the [[supergravity Lie 3-algebra]] is equation (8.8) there.


See also _[[division algebras and supersymmetry]]_.

A corresponding refinement of the brane scan to a "brane bouquet" of [[super L-∞ algebra]] [[infinity-Lie algebra cohomology|extensions]] (hence in [[infinity-Lie theory]] via [[schreiber:∞-Wess-Zumino-Witten theory]]) is discussed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 {#FiorenzaSatiSchreiber13}

 

These cohomologival arguments also appear in what is called the "ectoplasm" method for invariants in [[super Yang-Mills theory]] in 

* G. Bossard, [[Paul Howe]], K.S. Stelle, _A note on the UV behaviour of maximally supersymmetric Yang-Mills theories_, Phys. Lett. B682:137-142 (2009) ([arXiv:0908.3883](http://arxiv.org/abs/0908.3883))
 {#BossardHoweStelle09}

* [[Paul Howe]], T. G. Pugh, K. S. Stelle, C. Strickland-Constable, _Ectoplasm with an Edge_, JHEP 1108:081,2011 ([arXiv:1104.4387](http://arxiv.org/abs/1104.4387))

* G. Bossard, [[Paul Howe]], U. Lindstrom, K.S. Stelle, L. Wulff, _Integral invariants in maximally supersymmetric Yang-Mills theories_ ([arXiv:1012.3142](http://arxiv.org/abs/1012.3142))

The connection is made in 

* [[Paul Howe]], O. Raetzel, [[Ergin Sezgin]], _On Brane Actions and Superembeddings_, JHEP 9808 (1998) 011 ([arXiv:hep-th/9804051](http://arxiv.org/abs/hep-th/9804051))


The other brane scan, listing consistent asymptotic AdS geometries is due to 

* M.P. Blencowea, [[Mike Duff]], _Supersingletons_, Physics letters B, Volume 203, Issue 3, 31 March 1988, Pages 229&#8211;236 .

with further developments discussed in 

* [[Michael Duff]], _Near-horizon brane-scan revived_,  Nucl. Phys. B 810:193-209,2009 ([arXiv:0804.3675](http://arxiv.org/abs/0804.3675))

### anti de Sitter backgrounds
 {#ReferencesAdSBackgrounds}

Discussion of Green-Schwarz strings on [[super anti de Sitter spacetimes]] includes the following.


#### $AdS_5$
 {#ReferencesAdS5Background}


For the [[superstring]]:

* {#MetsaevTseytlin98} [[Ruslan Metsaev]], [[Arkaday Tseytlin]], _Type IIB superstring action in AdS_5 \times S^5 background_, Nucl.Phys.B533:109-126, 1998 ([arXiv:hep-th/9805028](http://arxiv.org/abs/hep-th/9805028))

* [[Gleb Arutyunov]], [[Sergey Frolov]], _Foundations of the $AdS_5 x S^5$ Superstring. Part I_ ([arXiv:0901.4937](http://arxiv.org/abs/0901.4937))

* Machiko Hatsuda, Makoto Sakaguchi, _Wess-Zumino term for AdS superstring_, Phys.Rev. D66 (2002) 045020 ([arXiv:hep-th/0205092](http://arxiv.org/abs/hep-th/0205092))

* Machiko Hatsuda, Makoto Sakaguchi, _Wess-Zumino term for the AdS superstring and generalized Inonu-Wigner contraction_, 	Prog.Theor.Phys. 109 (2003) 853-867 ([arXiv:hep-th/0106114](http://arxiv.org/abs/hep-th/0106114))

#### $AdS_4$ and $AdS_7$
 {#ReferencesAdS4Background}

For the [[superstring]]:

* [[Gleb Arutyunov]], [[Sergey Frolov]], _Superstrings on $AdS_4 \times \mathbb{C}P^3$ as a Coset Sigma-model_, JHEP 0809:129,2008 ([arXiv:0806.4940](http://arxiv.org/abs/0806.4940))

* [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure Spinor Formalism for $Osp(N|4)$ backgrounds_ ([arXiv:0807.0044](http://arxiv.org/abs/0807.0044))

* [[Riccardo D'Auria]], [[Pietro Fré]], Pietro Antonio Grassi, Mario Trigiante, _Superstrings on $AdS_4 \times \mathbb{C}P^3$ from Supergravity_ ([arXiv:0808.1282](http://arxiv.org/abs/0808.1282))

* D. V. Uvarov, _$AdS_4 x \mathbb{C}P^3$ superstring in the light-cone gauge_, Nucl.Phys.B826:294-312,2010 ([arXiv:0906.4699](http://arxiv.org/abs/0906.4699))

For the [[M2-brane]]:

* {#deWitPeetersPlefkaSevrin98} [[Bernard de Wit]], [[Kasper Peeters]], [[Jan Plefka]], Alexander Sevrin, _The M-Theory Two-Brane in $AdS_4 \times S^7$ and $AdS_7 \times S^4$_, Phys.Lett. B443 (1998) 153-158 ([arXiv:hep-th/9808052v1](http://arxiv.org/abs/hep-th/9808052v1))

* Makoto Sakaguchi, Hyeonjoon Shin, Kentaroh Yoshida, _Semiclassical Analysis of M2-brane in $AdS_4 \times S^7 / \mathbb{Z}_k$_, JHEP 1012:012,2010 ([arXiv:1007.3354](http://arxiv.org/abs/1007.3354))

For the [[M2-brane]] and the [[M5-brane]]:

* {#Claus98} Piet Claus, _Super M-brane actions in $adS_4 \times S^7$ and $adS_7 \times S^4$_, Phys.Rev. D59 (1999) 066003 ([arXiv:hep-th/9809045](http://arxiv.org/abs/hep-th/9809045))

* Makoto Sakaguchi, Kentaroh Yoshida, _Open M-branes on $AdS_{4/7} \times S^{7/4}$ Revisited_,  Nucl.Phys. B714 (2005) 51-66 ([arXiv:hep-th/0405109](http://arxiv.org/abs/hep-th/0405109))

### Self-dual strings in 6d

Discussion of the [[self-dual string]] in 6d as a Green-Schwarz-type sigma model includes

* Par Arvidsson, Erik Flink, [[Mans Henningson]], _Supersymmetric coupling of a self-dual string to a $(2,0)$ tensor multiplet background_, JHEP0311:015,2003 ([arXiv:hep-th/0309244](http://arxiv.org/abs/hep-th/0309244))

### General curved backgrounds and Supergravity background equations of motion
 {#ReferencesSupergravityBackgroundEquationsOfMotion}

The consistency of the Green-Schwarz action functional for the superstring in a [[supergravity]] [[background gauge field|background]] should be equivalent to the background satiyfying the [[supergravity]] [[equations of motion]] 

* {#BergshoeffSezginTownsend86} [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Superstring actions in $D = 3, 4, 6, 10$ curved superspace_, Phys.Lett., B169, 191, (1986) ([spire](http://inspirehep.net/record/223138/?ln=en))

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _[[The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

These authors amplify the role of closed $(p+2)$-forms in super $p$-brane backgrounds (p. 3) and clearly state the consistency conditions for the [[M2-brane]] in a curved backround in terms of the [[Bianchi identities]] on p. 7-8, amounting to the statment that the 4-form field strenght has to be the pullback of the cocycle $\overline{\psi}\wedge e^a \wedge e^b \wedge \Gamma^{a b} \psi$ plus the [[supergravity C-field]] [[curvature]] and has to be closed.


That the [[heterotic supergravity]] equations of motion are sufficient for the 3-form super field strength $H$ to be closed was first argued in

* {#Nilsson81} [[Bengt Nilsson]], _Simple 10-dimensional supergravity in superspace_, Nuclear Physics B188 (1981) 176-192 ([spire](http://inspirehep.net/record/164253?ln=de))
 
and the computation there was highlighted and a little simplified around p. 17 of

* [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B266 (1986) ([spire](http://inspirehep.net/record/214192/?ln=en))

A more comprehensive result arguing that the heterotic supergravity equations of motion of the background are not just sufficient but also necessary for (and hence equivalent to) the heterotic GS-string on that background being consistent was then claimed in

* {#ShapiroTaylor87} [[Joel Shapiro]], Cyrus Taylor, _Superspace supergravity from the superstring_, Physics letter B volume 186, number 1, 1987 ([pdf](http://ccdb5fs.kek.jp/cgi-bin/img/allpdf?198609078))

Discussion of this with the heterotic gauge-field included (hence including the [[Green-Schwarz anomaly cancellation]]) is in 

* {#AtickDharRatra86} [[Joseph Atick]], Avinash Dhar, Bharat Ratra, _Superspace Formulation of Ten-dimensional $N=1$ Supergravity Coupled to $N=1$ Super Yang-Mills Theory_, Phys.Rev. D33 (1986) 2824 ([spire](https://inspirehep.net/record/219734), [pdf](http://ccdb5fs.kek.jp/cgi-bin/img/allpdf?198602074))

Similar arguments for the [[type II string]] in [[type II supergravity]] appeared in 

* {#GHMNT85} [[Marcus Grisaru]], [[Paul Howe]], L. Mezincescu, [[Bengt Nilsson]], [[Paul Townsend]], _$N=2$-Superstring in a supergravity background_, Physics Letters Volume 162B, number 1,2,3 (1985) ([spire](http://inspirehep.net/record/17010))

and for GS sigma-model [[D-branes]] in 

* {#CGNSW97} [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))



That the [[M2-brane]] [[sigma-model]] is consistent on backgrounds of [[11-dimensional supergravity]] that satisfy their equations of motion is discussed in ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)).

The role of the 4-form here is also amplified around (2.29) in 

* [[Igor Bandos]], Carlos Meliveo, _Supermembrane interaction with dynamical D=4 N=1 supergravity. Superfield Lagrangian description and spacetime equations of motion_ ([arXiv:arXiv:1205.5885](http://arxiv.org/abs/arXiv:1205.5885))

and in section 2.2 of 

* [[Igor Bandos]], Carlos Meliveo, _Three form potential in (special) minimal supergravity superspace and supermembrane supercurrent_ ([arXiv:1107.3232](http://arxiv.org/abs/1107.3232))

following

* {#OvrutWaldram97} [[Burt Ovrut]], [[Daniel Waldram]], _Membranes and Three-form Supergravity_, Nucl.Phys. B506 (1997) 236-266 ([arXiv:hep-th/9704045](http://arxiv.org/abs/hep-th/9704045))

See also

* Bernard de Wit, Kasper Peeters, Jan Plefka, _Superspace Geometry for Supermembrane Backgrounds_, Nucl.Phys. B532 (1998) 99-123 ([arXiv:hep-th/9803209](http://arxiv.org/abs/hep-th/9803209))

All this is actually subsumed by imposing the [[Bianchi identities]] of the corresponding [[supergravity Lie 3-algebra]] etc. in "rheonomic parameterization", of the _[[D'Auria-Fré formulation of supergravity]]_, this is discussed in ([AFFFTT 98, section 3.1](#AFFFTT98), [Fr&#233;-Grassi 07](#FreGrassi07)).

Discussion including also the [[RR-field]] background includes

* R. R. Metsaev, _Type IIB Green-Schwarz superstring in plane wave Ramond-Ramond background_ ([arXiv:hep-th/0112044](http://arxiv.org/abs/hep-th/0112044))

### Relation to AdS-CFT
 {#ReferencesRelationToAdSCFT}

Discussion of how Green-Schwarz action functionals for super $p$-branes in [[anti de Sitter spacetimes]] induce -- after restricting to small fluctuations about a background solution and afzer [[diffeomorphism]] [[gauge fixing]] -- superconformal field theory on the [[worldvolumes]] -- the [[AdS-CFT correspondence]] -- includes

for the [[M2-brane]]:

* {#AFFFTT98} Gianguido Dall'Agata, Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#PastiSorokinTonin99} [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_ ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))

for the [[M5-brane]]:

* {#ClausKalloshProeyen97} Piet Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl.Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))

and more generally:

* {#ClausKalloshKumarTownsend98} Piet Claus, [[Renata Kallosh]], J. Kumar, [[Paul Townsend]], [[Antoine Van Proeyen]], _Conformal Theory of M2, D3, M5 and 'D1+D5' Branes_, JHEP 9806 (1998) 004 ([arXiv:hep-th/9801206](http://arxiv.org/abs/hep-th/9801206))

### Conserved current algebra
 {#ReferencesConservedCurrentAlgebra}

That higher WZW functionals and hence Green-Schwarz super $p$-brane action functionals have [[conserved current]] [[BPS charge]] algebras which are [polyvector extensions](super+Poincare+Lie+algebra#PolyvectorExtensions) of the supersymmetry algebras was observed in

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))

reviewed in  

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.8. of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

This is for branes in the old [[brane scan]] ([[strings]], [[membranes]], [[NS5-branes]]), excluding [[D-branes]] and [[M5-brane]].

The generalization oft this perspective to the [[M5-brane]] is discussed in 

* {#SorokinTownsend97} [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys.Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

and the generalizatin to [[D-branes]] is discussed in

* Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))


### $\kappa$-Symmetry 

The existence of $\kappa$-symmetry was first noticed around

* {#Siegel83} Warren Siegel, _Hidden Local Supersymmetry In The Supersymmetric Particle Action_ Phys. Lett. B 128, 397 (1983)
  

* {#Siegel84} Warren Siegel, _Light Cone Analysis Of Covariant Superstring_ , Nucl. Phys. B 236, 311 (1984).
  

* [[Michael Green]], [[John Schwarz]], _Covariant Description Of Superstrings_ , Phys. Lett. B 136, 367 (1984) ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))
 {#GreenSchwarz}

The meaning of $\kappa$-symmetry in terms of the [[supergeometry|super]]-[[Cartan geometry]] of super-[[target space]] is discussed in 

* {#McArthur} I.N. McArthur, _Kappa-Symmetry of Green-Schwarz Actions in Coset Superspaces_ ([arXiv:hep-th/9908045](http://arxiv.org/abs/hep-th/9908045))
 

* {#GKW} [[Joaquim Gomis]], Kiyoshi Kamimura, [[Peter West]], _Diffeomorphism, kappa transformations and the theory of non-linear realisations_ ([arXiv:hep-th/0607104](http://arxiv.org/abs/hep-th/0607104))
 
Discussion from the point of view of [[D'Auria-Fré formulation of supergravity]] is in 

* {#AFFFTT98} Gianguido Dall'Agata, Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194,1999, ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#FreGrassi07} [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure Spinors, Free Differential Algebras, and the Supermembrane_, Nucl.Phys.B763:1-34,2007 ([arXiv:hep-th/0606171](http://arxiv.org/abs/hep-th/0606171))


### Open branes ending on other branes

Discussion of the Green-Schwarz action for the open [[M2-brane]] ending on the [[M5-brane]] is in 

* C.S. Chu, [[Ergin Sezgin]], _M-Fivebrane from the Open Supermembrane_,  JHEP 9712 (1997) 001 ([arXiv:hep-th/9710223](http://arxiv.org/abs/hep-th/9710223))

* Ph. Brax, J. Mourad, _Open Supermembranes Coupled to M-Theory Five-Branes_, Phys.Lett. B416 (1998) 295-302 ([arXiv:hep-th/9707246](http://arxiv.org/abs/hep-th/9707246))


### Quantization


[[!redirects Green-Schwarz action]]

[[!redirects Green-Schwarz action functionals]]

[[!redirects Green-Schwarz string]]
[[!redirects Green-Schwarz superstring]]

[[!redirects Green-Schwarz strings]]
[[!redirects Green-Schwarz superstrings]]

[[!redirects super p-brane]]
[[!redirects super p-branes]]

[[!redirects Green-Schwarz sigma-model]]
[[!redirects Green-Schwarz sigma-models]]

[[!redirects Green-Schwarz sigma model]]
[[!redirects Green-Schwarz sigma models]]

[[!redirects Green-Schwarz super p-brane sigma model]]
[[!redirects Green-Schwarz super p-brane sigma models]]
[[!redirects Green-Schwarz super p-brane sigma-model]]
[[!redirects Green-Schwarz super p-brane sigma-models]]

[[!redirects Green-Schwarz super p-brane]]
[[!redirects Green-Schwarz super p-branes]]

[[!redirects super p-brane sigma-model]]
[[!redirects super p-brane sigma-models]]

[[!redirects super p-brane sigma model]]
[[!redirects super p-brane sigma models]]

[[!redirects Green-Schwarz-type sigma model]]
[[!redirects Green-Schwarz-type sigma models]]

[[!redirects Green-Schwarz-type sigma-model]]
[[!redirects Green-Schwarz-type sigma-models]]


[[!redirects Green-Schwarz super-p brane sigma model]]
[[!redirects Green-Schwarz super-p brane sigma models]]

[[!redirects Green-Schwarz sigma-model for super p-branes]]
[[!redirects Green-Schwarz sigma-models for super p-branes]]