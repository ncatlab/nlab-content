
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

These action functionals were first considered in ([Green-Schwarz 84](#GreenSchwarz84)) for [[superstrings]] in various dimensions. The full interpretation of the action functional as an higher [[Wess-Zumino-Witten theory]]-type action controled by the [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] (or rather of the [[super translation Lie algebra]] inside it)  is due to ([Azc&#225;rraga-Townsend89](#AzcarragaTownsend89)).


### Supercoordinates
 {#Supercoordinates}

We briefly review some basics of the canonical [[coordinates]] and the super [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] and [[super Minkowski space]], which are referred to below ([Azc&#225;rraga-Townsend 89](#AzcarragaTownsend89)).

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

Notice that this then gives the above formula for the differential of the super-[[vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

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

The term $\frac{i}{2}\bar \psi \Gamma^a \psi$ is sometimes called the *supertorsion* of the supervielbein $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \frac{i}{2}\bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{siso})$ which have "all indices contracted". 

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

The Green-Schwarz action has an extra fermionic symmetry, on top of the genuine supersymmetry, first observed in ([Siegel 83](#Siegel83)) for the [[superparticle]] and in ([Siegel 84](#Siegel84)) for the [[superstring]] in 3-dimensions, and finally in ([GreenSchwarz 84](#GreenSchwarz)) for the critical superstring in 10-dimensions. This is also called **$\kappa$-symmetry**. It has a natural interpretation in terms of the [[supergeometry|super]]-[[Cartan geometry]] of [[target space]] ([McArthur](#McArthur), [GKW](#GKW)).

### Dimensions -- the brane scan
 {#BraneScan}

The Green-Schwarz action functional of a $p$-brane propagating on an $d$-dimensional target spacetimes makes sense only for special combinations of $(p,d)$, for which there are suitanble [[Lie algebra cohomology|super Lie algebra cocycles]] on the super translation Lie algebra
(see [above](#DefinitionWZWTerm)).

The corresponding table has been called the **brane scan** in the literature, now often called the "old brane scan", since it has meanwhile been further completed (see below). In ([Duff 87](#Duff)) the "old brane scan" is displayed as follows.

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

### Relation to supergravity equations of motion 

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

This is due to ([Nilsson 81](#Nilsson81)).



## Related concepts

* [[supersymmetry]]

* [[sigma-model]], [[brane]]

  * [[relativistic particle]], [[spinning particle]], [[superparticle]]

  * [[string]], [[spinning string]], [[superstring]]

  * [[membrane]]

## References 

### General

The Green-Schwarz action functional (formulated for the [[superstring]]) is due to

* [[Michael Green]], [[John Schwarz]], _Covariant description of superstrings_, Phys. Lett. B136 (1984), 367&#8211;370 ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))
 {#GreenSchwarz84}

The observation that this is an example of a [[WZW-model]] on [[super-Minkowski spacetime]] is due to 

* [[Marc Henneaux]], Luca Mezincescu, _A Sigma Model Interpretation of Green-Schwarz Covariant Superstring Action_, Phys.Lett. B152 (1985) 340 ([web](http://inspirehep.net/record/15922?ln=en)) 
  {#HenneauxMezincescu85}

For more references on this perspective see [below](#ReferencesWZWTerm).

That the GS-action functionals is consistent on all backgrounds that satisfy the relevant [[supergravity]] [[equations of motion]] was shown in 

* [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Superstring actions in $D = 3, 4, 6, 10$ curved superspace_, Phys.Lett., B169, 191, (1986).

A standard textbook reference is appendix 4.A of volume 1 of

* [[Michael Green]], [[John Schwarz]], [[Edward Witten]], _Superstring theory_

and a brief paragraph in Volume II, section 10.2, page 983 of

* [[Eric D'Hoker]], _String theory -- lecture 10: Supersymmetry and supergravity_ , in part 3 of

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

A more recent and more comprehensive review is

* [[Joan Simón]], _[Brane Effective Actions, Kappa-Symmetry and Applications](http://relativity.livingreviews.org/open?pubNo=lrr-2012-3&page=articlese2.html)_, Living Reviews in relativity ([arXiv:1110.2422](http://arxiv.org/abs/1110.2422))


### WZW terms, super Lie algebra cohomology and the brane scan
 {#ReferencesWZWTerm}

The WZW nature of the second term in the GS action, recognized in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) is 
discussed with its [[infinity-Lie theory|Lie theoretic]] meaning
made fully explicit (in "FDA" language) in chater 8 of

* [[José de Azcárraga]], Izqierdo, _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_, Cambridge monographs of mathematical physics, (1995)
 {#AzcarragaIzqierdo}

The original "brane scan" classification of GS action functionals by WZW terms is due to

* A. Achucarro, J. M. Evans, [[Paul Townsend]] and D. L. Wiltshire, _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441
 {#AETW87}

For $d = 11$ the relevant [[super Lie algebra]] [[Lie algebra cohomology|cocycles]] have also been discussed (but not related to the Green-Schwarz action functional) in 

* [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)
 {#DAuriaFre82}

A review is in 

* [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 (1987) ([scan](http://ccdb4fs.kek.jp/cgi-bin/img/allpdf?198708425))
{#Duff}

from which the above table is taken.

A decent systematic account of the principles of super Lie algebra cohomology in the GS-functional, of these cocycles is in the letter

* [[José de Azcárraga]], [[Paul Townsend]], _Superspace geometry and the classification of supersymmetric extended objects_, Physical Review Letters Volume 62, Number 22 (1989)
 {#AzcarragaTownsend89}

and a detailed account building on this, which also discusses the GS/WZW terms for [[D-branes]] on the [[type II supergravity Lie 2-algebra]] (in its section 6) is in 

* C. Chrysso&#8204;malakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))
 {#CAIB99}



See also

* I. Bars, C. Deliduman and D. Minic, Phys. Rev D59 (1999) 125004;
Phys. Lett. B457 (1999) 275. ([arXiv:hep-th/9812161](http://arxiv.org/abs/hep-th/9812161))

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

The Green-Schwarz-type action for the [[M5-brane]] was found in 

* Igor Bandos, Kurt Lechner, Alexei Nurmagambetov, Paolo Pasti, [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_ ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))
 {#BLNPST}

* Mina Aganagic, Jaemo Park, Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_ ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))
 {#APPS}

The 7-cocycle on the [[supergravity Lie 3-algebra]] which gives the [[supergravity Lie 6-algebra]] appears in these articles (somewhat secretly) in equation ([BLNPST, equation (9)](#BLNPST)).

See also

* Igor Bandos, Paolo Pasti, Dmitri Sorokin, Mario Tonin, _Superbrane Actions and Geometrical Approach_ ([arXiv:hep-th/9705064](http://arxiv.org/abs/hep-th/9705064))
 {#BPST}

The 7-cocycle for the M5-brane on the [[supergravity Lie 3-algebra]] is equation (8.8) there.


See also _[[division algebras and supersymmetry]]_.

A corresponding refinement of the brane scan to a "brane bouquet" of [[super L-∞ algebra]] [[infinity-Lie algebra cohomology|extensions]] (hence in [[infinity-Lie theory]] via [[schreiber:∞-Wess-Zumino-Witten theory]]) is discussed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 {#FiorenzaSatiSchreiber13}

 

These cohomologival arguments also appear in what is called the "ectoplasm" method for invariants in [[super Yang-Mills theory]] in 

* G. Bossard, P.S. Howe, K.S. Stelle, _A note on the UV behaviour of maximally supersymmetric Yang-Mills theories_, Phys. Lett. B682:137-142 (2009) ([arXiv:0908.3883](http://arxiv.org/abs/0908.3883))
 {#BossardHoweStelle09}

* P. S. Howe, T. G. Pugh, K. S. Stelle, C. Strickland-Constable, _Ectoplasm with an Edge_, JHEP 1108:081,2011 ([arXiv:1104.4387](http://arxiv.org/abs/1104.4387))

* G. Bossard, P.S. Howe, U. Lindstrom, K.S. Stelle, L. Wulff, _Integral invariants in maximally supersymmetric Yang-Mills theories_ ([arXiv:1012.3142](http://arxiv.org/abs/1012.3142))

The connection is made in 

* P.S. Howe, O. Raetzel, [[Ergin Sezgin]], _On Brane Actions and Superembeddings_, JHEP 9808 (1998) 011 ([arXiv:hep-th/9804051](http://arxiv.org/abs/hep-th/9804051))


The other brane scan, listing consistent asymptotic AdS geometries is due to 

* M.P. Blencowea, [[Mike Duff]], _Supersingletons_, Physics letters B, Volume 203, Issue 3, 31 March 1988, Pages 229&#8211;236 .

with further developments discussed in 

* [[Michael Duff]], _Near-horizon brane-scan revived_,  Nucl. Phys. B 810:193-209,2009 ([arXiv:0804.3675](http://arxiv.org/abs/0804.3675))


### Supergravity background equations of motion
 {#ReferencesSupergravityBackgroundEquationsOfMotion}

The consistentcy of the Green-Schwarz action functional for the superstring in a [[supergravity]] [[background gauge field|background]] should be equivalent to the background satiyfying the [[supergravity]] [[equations of motion]].

That the [[heterotic supergravity]] equations of motion are sufficient for the 3-form super field strength $H$ to be closed was first argued in

* [[Bengt Nilsson]], _Simple 10-dimensional supergravity in superspace_, Nuclear Physics B188 (1981) 176-192 ([spire](http://inspirehep.net/record/164253?ln=de))
 {#Nilsson81}

and the computation there was highlighted and a little simplified in 

* [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B266 (1986)

Similar arguments for the [[type II string]] in [[type II supergravity]] appeared in 

* [[Marcus Grisaru]], P. Howe, L. Mezincescu, [[Bengt Nilsson]], [[Paul Townsend]], _$N=2$-Superstring in a supergravity background_, Physics Letters Volume 162B, number 1,2,3

and for GS sigma-model [[D-branes]] in 

* [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))

That the supergravity equations of motion of the background are not just sufficient but also necessary for (and hence equivalent to) the GS-string on that background being consistent was then claimed in

* [[Joel Shapiro]], Cyrus Taylor, _Superspace supergravity from the superstring_, Physics letter B volume 186, number 1, 1987


That the [[M2-brane]] [[sigma-model]] is consistent on backgrounds of [[11-dimensional supergravity]] that satisfy their equations of motion is discussed in

* [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _The world in eleven dimensions_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

These authors amplify the role of closed $(p+2)$-forms in super $p$-brane backgrounds (p. 3) and clearly state the consistency conditions for the [[M2-brane]] in a curved backroundin terms of the [[Bianchi identities]] on p. 7-8, amounting to the statment that the 4-form field strenght has to be the pullback of the cocycle $\overline{\psi}\wedge e^a \wedge e^b \wedge \Gamma^{a b} \psi$ plus the [[supergravity C-field]] [[curvature]] and has to be closed.

The role of the 4-form here is also amplified around (2.29) in 

* [[Igor Bandos]], Carlos Meliveo, _Supermembrane interaction with dynamical D=4 N=1 supergravity. Superfield Lagrangian description and spacetime equations of motion_ ([arXiv:arXiv:1205.5885](http://arxiv.org/abs/arXiv:1205.5885))

and in section 2.2 of 

* [[Igor Bandos]], Carlos Meliveo, _Three form potential in (special) minimal supergravity superspace and supermembrane supercurrent_ ([arXiv:1107.3232](arxiv.org/abs/1107.3232))

All this is actually subsumed by imposing the [[Bianchi identities]] of the corresponding [[supergravity Lie 3-algebra]] etc. in "rheonomic parameterization", see at _[[D'Auria-Fré formulation of supergravity]]_.

### Symmetries

That higher WZW functionals and hence Green-Schwarz super $p$-brane action functionals should have "higher" extended symmetry algebras in some sense... is observes in 

* [[José de Azcárraga]], Jerome P. Gauntlett, J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([web](http://inspirehep.net/record/26393?ln=en))

### $\kappa$-Symmetry 

The existence of $\kappa$-symmetry was first noticed around

* Warren Siegel, _Hidden Local Supersymmetry In The Supersymmetric Particle Action_ Phys. Lett. B 128, 397 (1983)
  {#Siegel83}

* Warren Siegel, _Light Cone Analysis Of Covariant Superstring_ , Nucl. Phys. B 236, 311 (1984).
  {#Siegel84}

* [[Michael Green]], [[John Schwarz]], _Covariant Description Of Superstrings_ , Phys. Lett. B 136, 367 (1984) ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))
 {#GreenSchwarz}

The meaning of $\kappa$-symmetry in terms of the [[supergeometry|super]]-[[Cartan geometry]] of super-[[target space]] is discussed in 

* I.N. McArthur, _Kappa-Symmetry of Green-Schwarz Actions in Coset Superspaces_ ([arXiv:hep-th/9908045](http://arxiv.org/abs/hep-th/9908045))
 {#McArthur}

* [[Joaquim Gomis]], Kiyoshi Kamimura, [[Peter West]], _Diffeomorphism, kappa transformations and the theory of non-linear realisations_ ([arXiv:hep-th/0607104](http://arxiv.org/abs/hep-th/0607104))
 {#GKW}

### Open branes ending on other branes

Discussion of the Green-Schwarz action for the open [[M2-brane]] ending on the [[M5-brane]] is in 

* C.S. Chu, [[Ergin Sezgin]], _M-Fivebrane from the Open Supermembrane_,  JHEP 9712 (1997) 001 ([arXiv:hep-th/9710223](http://arxiv.org/abs/hep-th/9710223))

* Ph. Brax, J. Mourad, _Open Supermembranes Coupled to M-Theory Five-Branes_, Phys.Lett. B416 (1998) 295-302 ([arXiv:hep-th/9707246](http://arxiv.org/abs/hep-th/9707246))

### GS superstrings in various backgrounds

* R. R. Metsaev, _Type IIB Green-Schwarz superstring in plane wave Ramond-Ramond background_ ([arXiv:hep-th/0112044](http://arxiv.org/abs/hep-th/0112044))

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
