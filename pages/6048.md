
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

The theory of [[11-dimensional supergravity]] contains a higher [[gauge field]] -- the [[supergravity C-field]] -- that naturally couples to higher electrically charged 2-[[branes]], [[membranes]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)). By _[[double dimensional reduction]]_, these turn into the [[superstrings]] of [[type IIA string theory]] ([Duff-Howe-Inami-Stelle 87](#DuffHoweInamiStelle87)). (See at _[[duality between M-theory and type IIA string theory]]_.)

When in ([Witten95](#Witten95)) it was argued that the 10-dimensional [[target space]] theories of the five types of [[string theory|superstring theories]] are all limiting cases of one single 11-dimensional target space theory that extends [[11-dimensional supergravity]] ([[M-theory]]), it was natural to guess that this supergravity membrane accordingly yields a 3-dimensional [[sigma-model]] that reduces in limiting cases to the [[string]] [[sigma-models]].

But there were two aspects that make this idea a little subtle, even at this vague level: first, there is no good theory of the [[quantization]] of the membrane [[sigma-model]], as opposed to the well understood quantum [[string]]. Secondly, that hypothetical "theory extending 11-dimensional supergravity" ("M-theory") has remained elusive enough that it is not clear in which sense the membrane would relate to it in a way analogous to how the string relates to its [[target space]] theories (which is fairly well understood).

Later, with the [[BFSS matrix model]] some people gained
more confidence in the idea, by identifying the corresponding degrees
of freedom in a special case ([Nicolai-Helling 98](#NicolaiHelling98), [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)). See also at _[[membrane matrix model]]_. 

In a more modern perspective, the M2-brane [[worldvolume]] theory appears under _[AdS4-CFT3 duality](AdS-CFT#AdS4CFT3)_ as a [[holographic principle|holographic dual]] of a [[4-dimensional Chern-Simons theory]]. Indeed, its [[Green-Schwarz action functional]] is entirely controled by the [[super Lie algebra|super]]-[[Lie algebra cocycle|Lie algebra 4-cocycle]] of [[super Minkowski spacetime]] given by the [[brane scan]]. This exhibits the M2-brane worldvolume theory as a 3-dimensional [[higher dimensional WZW model]].

## Definition

There are two different incarnations of the M2-brane. On the one hand it is defined as a [[Green-Schwarz sigma model]] with [[target space]] a [[spacetime]] that is a solution to the [[equations of motion]] of [[11-dimensional supergravity]]. One would call this the "fundamental" M2 in analogy with the "fundamental string", if only there were an "M2-perturbation series" which however is essentially ruled out.

On the other hand the M2 also appears as a [[black brane]], hence as a solution to the [[equations of motion]] of [[11-dimensional supergravity]] with [[singularity]] that looks from outside like a charged 2 dimensional object. 

### As a Green-Schwarz sigma model

See at _[[Green-Schwarz sigma model]]_ and _[[brane scan]]_.

### As a black brane
 {#AsABlackBrane}

#### In the absence of 4-flux

As a [[black brane]] solution to the [[equations of motion]] of [[11-dimensional supergravity]], with vanishing [[C-field]] [[flux]], the M2 is the [[spacetime]] $\mathbb{R}^{2,1} \times (\mathbb{R}^8-\{0\})$ with [[pseudo-Riemannian metric]] being

$$
  g = H^{-2/3} g_{\mathbb{R}^{2,1}} + H^{1/3}g_{\mathbb{R}^8-\{0\}}
$$

where 

$$
  H = \alpha + \frac{\beta}{r^6}
$$

for $(\alpha,\beta) \in \mathbb{R}^2 \setminus \{(0,0)\}$;

and the [[field strength]] of the [[supergravity C-field]] is 

$$
  F = d vol_{\mathbb{R}^{2,1}} \wedge \mathbf{d} H^{-1}
  \,.
$$

For $\alpha \beta \neq 0$ this is a 1/2 [[BPS state]] of 11d sugra.

In the above [[coordinates]] the metric is ill-defined at $r = - \beta^{1/6} \alpha$, but in fact it may be smoothly continued through this point ([Duff-Gibbons-Townsend 94, section 3](#DuffGibbonsTownsend94)), which is a [[event horizon]]. An actual singularity is at $r = 0$.


The [[near horizon geometry]] of this spacetime is the [[Freund-Rubin compactification]] [[anti de Sitter spacetime|AdS4]]$\times$[[7-sphere|S7]]. For more on this see at _[[AdS-CFT]]_.

[[!include black branes in supergravity -- table]]

{#BlackM2AtADESingularity} More generally, one may classify those solutions of [[11-dimensional supergravity]] of the form $AdS_4 \times X_7$ for some [[closed manifold]] $X_7$, that are at least 1/2 [[BPS states]]. One finds ([Medeiros-Figueroa 10](#MedeirosFigueroa10)) that all these are of the form $AdS_4 \times S^7/G_{ADE}$, where $S^7 / G_{ADE}$ is an [[orbifold]] of the [[7-sphere]] (a [[spherical space form]] in the smooth case, see [there](spherical+space+form#7DSphericalSpaceFormsWithSpinStructure)) by a [[finite subgroup of SU(2)]] $G_{ADE} \hookrightarrow SU(2)$, i.e. a finite group in the [[ADE-classification]]

[[!include ADE -- table]]

Here for $ 5 \leq \mathcal{N} \leq 8$-supersymmetry then the action of $G_{ADE}$ on $S^7$ is via the canonical action of $SU(2)$ as in the [[quaternionic Hopf fibration]] ([Medeiros-Figueroa 10](#MedeirosFigueroa10)), while for $\mathcal{N} = 4$ then there is an extra twist to the action  ([MFFGME 09](#MFFGME09)). See the table [below](#WorldvolumeTheory).


#### In the presence of 4-flux
 {#BlackM2BranesInThePresenceOfG4Flux}

In the presence of non-vanishing [[C-field]] [[flux]] $G_4$, the electric [[flux density]] of [[M2-branes]] is not $G_7 \coloneqq \star G_4$ alone, but receives corrections, first due to the quadratic [[C-field]] self-interaction in [[D=11 supergravity]], but then also due to the [[shifted C-field flux quantization]] expected in [[M-theory]]:

\linebreak

**The [[11d supergravity]] literature** states the corrected 7-flux to be the following combination, also known as the _[[Page charge]]_ (due to [Page 83 (8)](#Page83), [Duff-Stelle 91 (43)](#DuffStelle91), reviewed e.g. in [BLMP 13, p. 21](#BaggerLambertMukhiPapageorgakis13)):

\[
  \label{FirstCorrectionToG7}
  \widetilde G'_7 
  \;\coloneqq\;
  G_7 + \tfrac{1}{2} C_3 \wedge G_4
  \,,
\]

where the second term subtracts the electric flux induced by the self-intersection of the [[field]], and also ensures that the full expression is a [[closed differential form]] if the naive [[11d supergravity]] [[equations of motion]] hold:

$$
  d \widetilde G_7
  \;=\;
  0
  \,.
$$

But in fact (eq:FirstCorrectionToG7) does not quite make general sense, for two reasons:

1. In general $G_4 = 0$ is not an admissible condition and is not the actual vanshing of the [[C-field]], due to the [[shifted C-field flux quantization]].

1. Even if $G_4$ happens to be integrally quantizaed (if $\tfrac{1}{4}p_1$ is integral) the appearance of a globally defined [[C-field]] potential $C_3$ in (eq:FirstCorrectionToG7),means that the total [[flux]] actually does vanish after all.

\linebreak

**Charge-quantized $\widetilde G_7$-flux with [[shifted C-field flux quantization]]** ([FSS 19b, Prop. 4.3](#FSS19b), [FSS 19c, Section 4](#FSS19c))

Both of these issues are solved if the [[C-field]] is taken to be [[charge quantization|charge quantized]] in [[J-homomorphism|J-]][[twisted Cohomotopy]] ([[schreiber:Hypothesis H]]). This gives the corrected formula 

\[
  \label{FullCorrectionToG7}
  \widetilde G_7 
  \;\coloneqq\;
  h^\ast G_7 + \tfrac{1}{2} H_3 \wedge h^\ast \widetilde G_4
\]

where

<div style="float:right;margin:0 10px 10px 0;">
<a href="">
<img src="https://ncatlab.org/schreiber/files/6dWZFromHomotopyLifting.jpg" width="440" />
</a></div>

1. the expression lives on the [[homotopy pullback]] of the [[Sp(2)]]-[[parametrized homotopy theory|parametrized]] [[quaternionic Hopf fibration]] 

   $$
     h \coloneqq h_{\mathbb{H}}\sslash Sp(2)
   $$ 

   to [[spacetime]], along the [[twisted Cohomotopy]]-[[cocycle]] that represents the [[C-field]] under [[schreiber:Hypothesis H]];

1. $\widetilde G_4 \coloneqq h^\ast G_4 + \tfrac{1}{4}h^\ast p_1(\nabla)$ is the integral [[shifted C-field flux quantization|shifted C-field]] pulled back to that 3-[[spherical fibration]] over spacetime;

1. $d H_3 = h^\ast G_4 - \tfrac{1}{4}h^\ast p_1(\nabla)$ trivializes not the C-field itself, but its pullback, and not absolutely but relative to the background charge implied by [[shifted C-field flux quantization]].

With the corrected 7-flux in [[twisted Cohomotopy]] it becomes true that 

1. the integral of $G_7$ around the [[7-sphere]] linking a [[black brane|black]] [[M2-brane]] is always [[integer]] ([FSS 19c, Theorem 4.6](#FSS19c));

1. this integer satisfies the [[C-field tadpole cancellation condition]] ([FSS 19b, Section 4.6](#FSS19b)).




## Properties

### Quantization via BFSS matrix model
 {#QuantizationViaBFSSMatrixModel}

A regularized [[quantization]] of the [[Green-Schwarz sigma-model]] for the [[M2-brane]] yields the [[BFSS matrix model]] ([Nicolai-Helling 98](#NicolaiHelling98), [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)). 

In this correspondence, [[matrix]] blocks around the diagonal correspond to blobs of [[membrane]], while off-diagonal matrix elements correspond to thin tubes of membrane connecting these blobs.

<center>
<img src="https://ncatlab.org/nlab/files/MatrixMembrane.jpg" width="500">
</center>

> graphics grabbed from [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)


### Worldvolume theory -- BLG and ABJM
 {#WorldvolumeTheory}

The [[worldvolume]] [[QFT]] of [[black brane|black]] M2-branes is a [[3d superconformal gauge field theory]]:

[[!include superconformal symmetry -- table]]

Specifically, [[worldvolume]] [[quantum field theory]] of M2-branes sitting at [[ADE singularities]] (as [above](#BlackM2AtADESingularity)) is supposed to be described by [[ABJM theory]] and, for the special case of $SU(2)$ gauge group, by the [[BLG model]]. See also at _[[gauge enhancement]]_.

[[!include 7d spherical space forms -- table]]



### AdS4-CFT3 duality

Under [[AdS-CFT duality]] the M2-brane is given by
_[AdS4-CFT3 duality](AdS-CFT#AdS4CFT3)_. ([Maldacena 97, section 3.2](#Maldacena97), [Klebanov-Torri 10](#KlebanovTorri10)).

\linebreak


### M2/M5 bound states
 {#M2M5BoundStates}

For _[[M2-M5 brane bound states]]_, i.e.
 [[bound states]] of [[M2-branes]] with [[M5-branes]] ([[dyon|dyonic]] M2-branes and [[giant gravitons]]), see the
references [below](#ReferencesDyonic).

For the [[type II string theory]]-version see at _[[NS5-brane]]_ the sectoin _[NS5/D4/D2 bound states](NS5-brane#NS5D4D2BoundStates)_.


\linebreak

[[!include M2-M5 brane bound states in the BMN matrix model -- subsection]]

\linebreak

## Related concepts

* [[membrane instanton]], [[SM2-brane]]

* [[fractional M2-brane]]

* [[triple membrane junction]]

* [[C-field tadpole cancellation]]

* [[BLG model]], [[ABJM model]], [[membrane matrix model]]

  [[M2-brane 3-algebra]]

* [[string theory]]

* [[11-dimensional supergravity]], [[M-theory]]

* [[string]], [[superstring]]

* [[D-brane]]

* [[M5-brane]], [[6d (2,0)-superconformal QFT]]

* [[M9-brane]]

* [[topological membrane]]

* [[supergravity Lie 3-algebra]], [[M-theory super Lie algebra]]

[[!include table of branes]]

## References


### As a fundamental brane (GS-type $\sigma$-model)

The [[Green-Schwarz sigma-model]]-type formulation of the [[supermembrane]] in 11d (as in the [[brane scan]]) first appears in 

* {#BergshoeffSezginTownsend87} [[Eric Bergshoeff]], [[Ergin Sezgin]], and [[Paul Townsend]], _Supermembranes and eleven-dimensional supergravity_, Phys. Lett. B189 (1987) 75&#8211;78. ([spire:248230](http://inspirehep.net/record/248230/))

The [[equations of motion]] of the super membrane are derived via the [[superembedding approach]] in 

* {#BPSTV95} [[Igor Bandos]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], [[Dmitry Volkov]], Chapter 3 of _Superstrings and supermembranes in the doubly supersymmetric geometrical approach_, Nucl. Phys. B446:79-118, 1995 ([arXiv:hep-th/9501113](https://arxiv.org/abs/hep-th/9501113))

and the [[Lagrangian density]] for the super membrane is derived via the [[superembedding approach]] in

* {#HoweSezgin05} [[Paul Howe]], [[Ergin Sezgin]], _The supermembrane revisited_, Class. Quant. Grav. 22 (2005) 2167-2200 ([arXiv:hep-th/0412245](https://arxiv.org/abs/hep-th/0412245))

Discussion from the point of view of [[Green-Schwarz action functional]]-[[schreiber:∞-Wess-Zumino-Witten theory]] is in

* {#FSS2013} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ (2013)


The [[double dimensional reduction]] of the M2-brane to the [[Green-Schwarz superstring]] was observed in

* {#DuffHoweInamiStelle87} [[Michael Duff]], [[Paul Howe]], T. Inami, [[Kellogg Stelle]], _Superstrings in $D=10$ from Supermembranes in $D=11$_, Phys. Lett. B191 (1987) 70 and in [[Michael Duff]] (ed.) _[[The World in Eleven Dimensions]]_ 205-206 (1987) ([spire](http://inspirehep.net/record/245249))

The interpretation of the membrane as an object related to [[string theory]] via [[double dimensional reduction]], hence as the _M2-brane_ was proposed in 

* [[Paul Townsend]], _The eleven-dimensional supermembrane revisited_, Phys. Lett. B350:184-187, 1995 ([arXiv:hep-th/9501068](http://arxiv.org/abs/hep-th/9501068))

around the time when [[M-theory]] became accepted due to

* {#Witten95} [[Edward Witten]], _[[String Theory Dynamics In Various Dimensions]]_ ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))


See also

* [[Paul Howe]], [[Ergin Sezgin]], _The supermembrane revisited_, ([arXiv:hep-th/0412245](http://arxiv.org/abs/hep-th/0412245))

* [[Igor Bandos]], [[Paul Townsend]], _SDiff Gauge Theory and the M2 Condensate_ ([arXiv:0808.1583](http://arxiv.org/abs/0808.1583))

* M.P. Garcia del Moral, C. Las Heras, P. Leon, J.M. Pena, A. Restuccia, _Fluxes, Twisted tori, Monodromy and $U(1)$ Supermembranes_ ([arXiv:2005.06397](https://arxiv.org/abs/2005.06397))

* Pedro D. Alvarez, Pedro García, Maria Pilar Garcia del Moral, Joselen M. Peña, Reginaldo Prado, *Spinning solutions for the bosonic M2-brane with $C_{\pm}$ fluxes* ([arXiv:2104.08927](https://arxiv.org/abs/2104.08927))



[[!include quantization of M2-brane on Minkowski spacetime to BFSS matrix model -- references]]

 

### As a black brane
 {#ReferencesAsABlackBrane}

The [[black brane|black]] membrane solution of [[11-dimensional supergravity]] was found in

* {#DuffStelle91} [[Mike Duff]], [[Kellogg Stelle]], _Multi-membrane solutions of $D = 11$ supergravity_, Phys. Lett. B 253, 113 (1991) ([spire:299386](http://inspirehep.net/record/299386), <a href="https://doi.org/10.1016/0370-2693(91)91371-2">doi:10.1016/0370-2693(91)91371-2</a>)

Its regularity across the [[event horizon]] is due to

* {#DuffGibbonsTownsend94} [[Mike Duff]], [[Gary Gibbons]], [[Paul Townsend]], _Macroscopic superstrings as interpolating solitons_, Phys. Lett. B332:321-328, 1994 ([arXiv:hep-th/9405124](https://arxiv.org/abs/hep-th/9405124))

Further discussion of such _[[Freund-Rubin compactifications]]_:

* {#Page83} [[Don Page]], _Classical stability of round and squashed seven-spheres in eleven-dimensional supergravity_, Phys. Rev. D 28, 2976 (1983) ([spire:14480](http://inspirehep.net/record/14480) [doi:10.1103/PhysRevD.28.2976](https://doi.org/10.1103/PhysRevD.28.2976))


The [[Horava-Witten theory|Horava-Witten]]-[[orientifold]] of the black M2, supposedly yielding the [[black brane|black]] [[heterotic string]] is discussed in

* {#LalakLukasOvrut97} Zygmunt Lalak, Andr&eacute; Lukas, [[Burt Ovrut]], _Soliton Solutions of M-theory on an Orbifold_, Phys. Lett. B425 (1998) 59-70 ([arXiv:hep-th/9709214](https://arxiv.org/abs/hep-th/9709214))

* {#Kashima00} Ken Kashima, _The M2-brane Solution of Heterotic M-theory with the Gauss-Bonnet $R^2$ terms_, Prog.Theor.Phys. 105 (2001) 301-321 ([arXiv:hep-th/0010286](https://arxiv.org/abs/hep-th/0010286))


Meanwhile [[AdS-CFT duality]] was recognized in 

* {#Maldacena97} [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); 
 
where a dual description of the [[worldvolume]] theory of M2-brane appears in section 3.2.  More on this is in 

* {#KlebanovTorri10} [[Igor Klebanov]], Giuseppe Torri, _M2-branes and AdS/CFT_, Int.J.Mod.Phys.A25:332-350,2010 ([arXiv:0909.1580](http://arxiv.org/abs/0909.1580))

An account of the history as of 1999 is in

* {#Duff99} [[Mike Duff]], chapter II of _[[The World in Eleven Dimensions]]: Supergravity, Supermembranes and M-theory_, IoP 1999 ([publisher](https://www.crcpress.com/The-World-in-Eleven-Dimensions-Supergravity-supermembranes-and-M-theory/Duff/9780750306720))

More recent review is in

* Georgios Linardopoulos, chapter 13 of _Classical Strings and Membranes in the AdS/CFT Correspondence_ ([pdf](http://users.uoa.gr/~glinardo/Thesis.pdf), [spire](https://inspirehep.net/record/1391031/))

 
A detailed discussion of this [[black brane]]-realization of the [[M2-brane]] and its relation to [[AdS-CFT]] is in 

* [[Gianguido Dall'Agata]], Davide FabbKri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

The generalization of this to $\geq 1/2$ BPS sugra solutions of the form $AdS_4 \times X_7$ is due to

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* {#MedeirosFigueroa10} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

Discussion of $G7$-[[C-field flux quantization]] in the $G_4$-fluxed case:

 {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Prop. 4.31 of: _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 4 of: _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))


### In $AdS_4/CFT_3$

In [[AdS4-CFT3 duality]]:

Review:

* Kazuo Hosomichi, _M2-branes and AdS/CFT: A Review_ ([arXiv:2003.13914](https://arxiv.org/abs/2003.13914))





### History

Discussion of the history includes

* [[Mike Duff]], ([arXiv:1501.04098](http://arxiv.org/abs/1501.04098))



### Decoupled worldvolume theory

On the [[BLG model]]/[[ABJM model]] for the [[worldvolume]]-theory of [[coindicent branes|coincident]] [[M2-branes]] see there.

Review:

* {#BaggerLambertMukhiPapageorgakis13} [[Jonathan Bagger]], [[Neil Lambert]], [[Sunil Mukhi]], [[Constantinos Papageorgakis]], _Multiple Membranes in M-theory_, Physics Reports, Volume 527, Issue 1, 1 June 2013, Pages 1-100 ([arXiv:1203.3546](http://arxiv.org/abs/1203.3546), [doi:10.1016/j.physrep.2013.01.006](https://doi.org/10.1016/j.physrep.2013.01.006))




 

### Dualities

The role of and the relation to [[duality in string theory]] of the membrane is discussed in the following articles.

Relation to [[T-duality]] is discussed in:

* J.G. Russo, _T-duality in M-theory and supermembranes_ ([arXiv:hep-th/9701188](http://arxiv.org/abs/hep-th/9701188))

* M.P. Garcia del Moral, J.M. Pena, A. Restuccia, _T-duality Invariance of the Supermembrane_ ([arXiv:1211.2434](http://arxiv.org/abs/1211.2434))

Relation to [[U-duality]] is discussed in:

* [[Martin Cederwall]], _M-branes on U-folds_ ([arXiv:0712.4287](http://arxiv.org/abs/0712.4287))

* M.P. Garcia del Moral, _Dualities as symmetries of the Supermembrane Theory_ ([arXiv](http://arxiv.org/abs/1211.6265))

* [pdf](http://streaming.ictp.trieste.it/preprints/P/97/044.pdf)

Discussion from the point of view of [[E11]]-[[U-duality]] and [[current algebra]] is in 

* [[Hirotaka Sugawara]], _Current Algebra Formulation of M-theory based on E11 Kac-Moody Algebra_, International Journal of Modern Physics A, Volume 32, Issue 05, 20 February 2017 ([arXiv:1701.06894](https://arxiv.org/abs/1701.06894))

* [[Shotaro Shiba]], [[Hirotaka Sugawara]], _M2- and M5-branes in $E_{11}$ Current Algebra Formulation of M-theory_ ([arXiv:1709.07169](https://arxiv.org/abs/1709.07169))



### M2-M5 bound states
 {#ReferencesDyonic}

Discussion of [[M2-M5 brane bound states]], i.e.
[[dyon|dyonic]]$\,$[[black brane|black]] [[M2-branes]] ([[M5-branes]] [[wrapped brane|wrapped]] on a [[3-manifold]], see also at _[NS5-branes -- D2/D4/NS5-bound states](NS5-brane#ReferencesNS5D4D2BoundStates)_):

* {#ILPT95} J.M. Izquierdo, [[Neil Lambert]], [[George Papadopoulos]], [[Paul Townsend]], _Dyonic Membranes_, Nucl. Phys. B460:560-578, 1996 ([arXiv:hep-th/9508177](https://arxiv.org/abs/hep-th/9508177))

* [[Michael Green]], [[Neil Lambert]], [[George Papadopoulos]], [[Paul Townsend]], _Dyonic $p$-branes from self-dual $(p+1)$-branes_, Phys. Lett. B384:86-92, 1996 ([arXiv:hep-th/9605146](https://arxiv.org/abs/hep-th/9605146))

* [[Troels Harmark]], Section 3.1 of _Open Branes in Space-Time Non-Commutative Little String Theory_, Nucl.Phys. B593 (2001) 76-98 ([arXiv:hep-th/0007147](https://arxiv.org/abs/hep-th/0007147))

* [[Troels Harmark]],  N.A. Obers, Section 5.1 of _Phase Structure of Non-Commutative Field Theories and Spinning Brane Bound States_, JHEP 0003 (2000) 024 ([arXiv:hep-th/9911169](https://arxiv.org/abs/hep-th/9911169))

* [[George Papadopoulos]], [[Dimitrios Tsimpis]], _The holonomy of the supercovariant connection and Killing spinors_, JHEP 0307:018, 2003 ([arXiv:hep-th/0306117](https://arxiv.org/abs/hep-th/0306117))

* {#Petri18} Nicolò Petri, slide 14 of _Surface defects in massive IIA_, talk at [Recent Trends in String Theory and Related Topics](http://physics.ipm.ac.ir/conferences/stringtheory3/) 2018 ([pdf](http://physics.ipm.ac.ir/conferences/stringtheory3/note/N.Petri.pdf))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 4 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* Jay Armas, Vasilis Niarchos, Niels A. Obers, _Thermal transitions of metastable M-branes_ ([arXiv:1904.13283](https://arxiv.org/abs/1904.13283))

Further [[M2/M5-brane bound states]] to [[giant gravitons]]:

* J. M. Camino, A. V. Ramallo, _M-Theory Giant Gravitons with C field_, Phys. Lett. B525:337-346, 2002 ([arXiv:hep-th/0110096](https://arxiv.org/abs/hep-th/0110096))



[[!redirects M2-branes]]

[[!redirects M2 brane]]
[[!redirects M2 branes]]

[[!redirects M-theory membrane]]
[[!redirects M-theory membranes]]