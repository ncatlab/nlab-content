
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

Moreover,  while every such $\sigma$-model canonically has symmetries given by the left [[action]] of $G$ on $G/H$, the GS action is required to
exhibit "$\kappa$-symmetry", which says that _locally_ a non-canonical
right action of $G$ on $G/H$ is a symmetry.

For coordinate expressions of these terms we adopt the standard
conventions:

Let $(x^a, \theta^\alpha)$ be the canonical 
[[coordinates]] on the [[super translation group]] 
$sISO/SO$. 
In terms of these the standard [[basis]] of [[left invariant forms]] is
$\{\Pi^a, d \theta^\alpha\}$ with

$$
  \Pi^a := d x^a - i \bar \theta \Gamma^\mu \theta
  \,.
$$


### Kinetic term

(...)

### WZW term
 {#DefinitionWZWTerm}

Let $(e^a, \omega^{a b}, \psi^\alpha)$ be the standard generators
of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}(d,1))$ of the 
[[super Poincare Lie algebra]], as discussed there.

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
translation group is contractible, a [[Poincare lemma]] applies
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

The corresponding table has been called the **brane scan** in the literature. In ([Duff](#Duff)) it is displayed as follows.

[[branescan.gif:pic]]

In the $D = 10$-row we see the critical [[superstring]] of [[string theory]] and
its [[electric-magnetic duality|magnetic dual]], the [[NS5-brane]].
The top row shows the [[M2-brane]] in [[11-dimensional supergravity]]. What is missing in the table is the [[M5-brane]] in that top dimension.

The reason is that the M5 corresponds to a 7-cocycle not on the ordinary [[super Poincare Lie algebra]], but on its [[infinity-Lie algebra cohomology|L-infinity algebra extension]], the [[supergravity Lie 3-algebra]]. See the 7-cocycle at [[supergravity Lie 6-algebra]].


## Related concepts

* [[supersymmetry]]

* [[sigma-model]], [[brane]]

  * [[relativistic particle]], [[spinning particle]], [[superparticle]]

  * [[string]], [[spinning string]], [[superstring]]

  * [[membrane]]

## References 

### General

Standard textbook references are

appendix 4.A of volume 1 of

* [[Michael Green]], [[John Schwarz]], [[Edward Witten]], _Superstring theory_

and

* [[Eric D'Hoker]], _String theory -- lecture 10: Supersymmetry and supergravity_ , in part 3 of

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

### WZW terms and super Lie algebra cohomology
 {#ReferencesWZWTerm}

The WZW nature of the second term in the GS action is 
discussed with its [[infinity-Lie theory|Lie theoretic]] meaning
made fully explicit in chater 8 of

* [[José de Azcárraga]], Izqierdo, _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_, Cambridge monographs of mathematical physics, (1995)
 {#AzcarragaIzqierdo}

### Dimensions

The "brane scan" table showing the consistent dimension pairs for the Green-Scharz action functional was depicted in

* [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 (1987) ([scan](http://ccdb4fs.kek.jp/cgi-bin/img/allpdf?198708425))
{#Duff}

going back to

* A. Ach&#250;carro, J. M. Evans, [[Paul Townsend]] and D. L. Wiltshire, _Super $p$-branes_ Physics Letters B Volume 198, Issue 4, 3 (1987)

See also

* I. Bars, C. Deliduman and D. Minic, Phys. Rev D59 (1999) 125004;
Phys. Lett. B457 (1999) 275.

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

See also _[[division algebras and supersymmetry]]_.


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

### GS superstrings in various backgrounds

* R. R. Metsaev, _Type IIB Green-Schwarz superstring in plane wave Ramond-Ramond background_ ([arXiv:hep-th/0112044](http://arxiv.org/abs/hep-th/0112044))

[[!redirects Green-Schwarz action]]

[[!redirects Green-Schwarz string]]
[[!redirects Green-Schwarz superstring]]

[[!redirects Green-Schwarz strings]]
[[!redirects Green-Schwarz superstrings]]