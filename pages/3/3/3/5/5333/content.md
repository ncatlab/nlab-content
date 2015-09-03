+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* tale of contents
{:toc}

## Idea

In [[string theory]] a [[spacetime]] [[landscape of string theory vacua|vacuum]] is encoded by a [[sigma-model]] 2-dimensional [[SCFT]]. In _heterotic string theory_ that SCFT is assumed to be the sum of a supersymmetric chiral piece and a  non-supersymmetric piece (therefore "heterotic").

## Properties

### Compactifications

An effective [[target space]] [[quantum field theory]] induced from a given heterotic 2d [[CFT]] [[sigma model]] that has a [[spacetime]] of the form $M^4 \times Y^6$ for $M^4$ the 4-dimensional [[Minkowski space]] that is experimentally observed locally (say on the scale of a particle accelerator) has $N= 1$ global [[supersymmetry]] precisely if the remaining 6-dimensional [[Riemannian manifold]] $Y^6$ is a [[Calabi-Yau manifold]]. See the [references below](#ReferencesNEqOne). 

Since global $N=1$ supersymmetry for a long time has been considered a promising phenomenological model in high energy physics, this fact has induced a lot of interest in heterotic string background with a Calabi-Yau factor.

### Enhanced supersymmetry

A priori the [[worldsheet]] [[2d SCFT]] describing the quantum heterotic string has $N=(1,0)$ [[supersymmetry]]. Precisely if the corresponding [[target space]] [[effective field theory]] has $N=1$ supersymmetry does the worldsheet theory enhance to $N=(2,0)$ supersymmetry. See at _[[2d (2,0)-superconformal QFT]]_ and at _[[Calabi-Yau manifolds and supersymmetry]]_ for more on this.

### Dualities

Some [[duality in string theory]] involving the heterotic string:

#### Relation to M-theory

For the moment see at _[[Horava-Witten theory]]_.

#### Relation to F-theory, type II and type I superstring theory

For [[duality between F-theory and heterotic string theory]] see there
and see [references below](#DualityWithFTheory).



### Partition function and Witten genus

[[!include genera and partition functions - table]]

### General gauge backgrounds and parameterized WZW models
 {#GeneralGaugeBackgroundsAndParameterizedWZWModels}

The traditional construction of the [[worldsheet]] theory of the heterotic string produces via the [[current algebra]] of the left-moving worldheet [[fermions]] only those [[E8]]-[[background gauge fields]] which are reducible to $Spin(16)/\mathbb{Z}_2$-[[principal connections]] ([Distler-Sharpe 10, sections 2-4](#DistlerSharpe10)). But is in known that instance the [[duality between F-theory and heterotic string theory]] produces more general gauge backgrounds ([Distler-Sharpe 10, section 5](#DistlerSharpe10)). 

In ([Distler-Sharpe 10, section 7](#DistlerSharpe10)), following ([Gates-Siegel 88](#GatesSiegel88)), it is argued that the way to fix this is to consider [[parameterized WZW models]], parameterized over the [[E8]]-[[principal bundle]] over [[spacetime]]. This does allow to incorporate all $E_8$-background gauge fields, and the [[Green-Schwarz anomaly]] (and its cancellation) of the heterotic string now comes out as being equivalently the [[obstruction]] (and its lifting) for such a parameterized WZW term to exist.

Moreover, where the traditional construction only produces level-1 [[current algebras]], this construction accomodates all levels, and it is argued ([Distler-Sharpe 10, section 8.5](#DistlerSharpe10)) that the [[elliptic genus]] of the resulting [[parameterized WZW models]] are the [[equivariant elliptic genera]] found by Liu and Ando ([Ando 07](#Ando07))

However, presently questions remain concerning formulating a [[sigma-model]] for strings propagating on the total space of the bundle, as it is only the chiral part of the geometric WZW model that appears in the heterotic string. (...)


## Related concepts

* [[string theory]]

  * **heterotic string theory**

    * [[2d SCFT]], 

      * [[2-spectral triple]], [[Dirac-Ramond operator]]

    * [[2d (2,0)-superconformal QFT]]

    * [[Green-Schwarz mechanism]]

    * [[dual heterotic string theory]]

    * [[Witten genus]], [[(2,1)-dimensional Euclidean field theories and tmf]]

  * [[type II string theory]]

  * [[landscape of string theory vacua]]

  * [[supersymmetry and Calabi-Yau manifolds]]

* [[string field theory]]

* [[11-dimensional supergravity]]

  * [[Ho?ava-Witten theory]]

  * [[M-theory]]

* [[AdS-CFT correspondence]]

* [string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)




## References

### General

Heterotic strings were introduced in 

* [[David Gross]], J. A. Harvey, E. Martinec and R. Rohm, 

  _Heterotic string theory (I). The free heterotic string_  Nucl. Phys. B 256 (1985), 253. 

  _Heterotic string theory (I). The interacting heterotic string_ , Nucl. Phys. B 267 (1986), 75. 

* [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], [[Edward Witten]], Nucl. Phys. B258 (1985) 46

* {#Schellekens91} [[Bert Schellekens]], _Classification of Ten-Dimensional Heterotic Strings_, Phys.Lett. B277 (1992) 277-284 ([arXiv:hep-th/9112006](http://arxiv.org/abs/hep-th/9112006))

Textbook accounts include


* [[Joseph Polchinski]], _[[String theory]]_, volume II, section 11

* [[Eric D'Hoker]], _String theory -- lecture 8: Heterotic strings_  in part 3 (p. 941 of volume II) of

  [[Pierre Deligne]], P. Etingof, [[Dan Freed]], L. Jeffrey, [[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds. . _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

### In elliptic cohomology

For more mathematically precise discussion in the context of [[elliptic cohomology]] and the [[Witten genus]] see also the references at _[Witten genus -- Heterotic (twisted) Witten genus, loop group representations and parameterized WZW models](Witten+genus#TwistedWittenGenus)_.

### General flux backgrounds and parameterized WZW models

Discussion of heterotic strings whoe [[current algebra]]-sector is parameterized by a [[principal bundle]] originates with

* {#GatesSiegel88} [[Jim Gates]], [[Warren Siegel]], _Leftons, Rightons, Nonlinear $\sigma$-Models, and Superstrings_, Phys.Lett. B206 (1988) 631 ([spire](https://inspirehep.net/record/251286/))

* [[Jim Gates]], _Strings, superstrings, and two-dimensional lagrangian field theory_, pp. 140-184 in Z. Haba, J. Sobczyk (eds.) _Functional integration, geometry, and strings_, proceedings of the XXV Winter School of Theoretical Physics, Karpacz, Poland (Feb. 1989), , Birkh&#228;user, 1989.

* {#GKKS91} [[Jim Gates]], S. Ketov, S. Kozenko, O. Solovev, _Lagrangian chiral coset construction of heterotic string theories in $(1,0)$ superspace_, Nucl.Phys. B362 (1991) 199-231 ([spire](http://inspirehep.net/record/314337/?ln=en))

and is further expanded on in

* {#DistlerSharpe10} [[Jacques Distler]], [[Eric Sharpe]], _Heterotic compactifications with principal bundles for general groups and general levels_, Adv. Theor. Math. Phys. 14:335-398, 2010 ([arXiv:hep-th/0701244](http://arxiv.org/abs/hep-th/0701244))

reviewed in

* {#Sharpe08} [[Eric Sharpe]], _Recent developments in heterotic compactifications_, in [[Eric Sharpe]], [[Arthur Greenspoon]], _[Advances in String Theory: The First Sowers Workshop in Theoretical Physics](http://www.ams.org/bookstore-getitem/item=AMSIP-44)_, AMS 2008 ([pdf slides (39-49)](http://www.phys.vt.edu/sowers/talks/sharpe-sowers.pdf))


The relation of this to [[equivariant elliptic cohomology]] is amplified in

* {#Ando07} [[Matthew Ando]], _Equivariant elliptic cohomology and the Fibered WZW models of Distler and Sharpe_, [talk 2007](http://www.math.ucsb.edu/~drm/GTPseminar/2007-fall.php) ([lecture notes pdf](http://www.math.ucsb.edu/~drm/GTPseminar/notes/20071026-ando/20071026-malmendier.pdf))



### As higher super-GS-WZW type $\sigma$-models

Discussion from the point of view of [[Green-Schwarz action functional]]-[[schreiber:∞-Wess-Zumino-Witten theory]] is in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_





#### On elliptic fibrations


Compactified on an [[elliptic curve]] or, more generally, [[elliptic fibration]], heterotic string compactifictions are controled by a choice holomorphic [[stable bundle]] on the compact space. Dually this is an [[F-theory]] compactification on a [[K3]]-bundles.

The basis of this story is discussed in 

* Robert Friedman, [[John Morgan]], [[Edward Witten]], _Vector Bundles And F-Theory_ ([arXiv:hep-th/9701162](http://arxiv.org/abs/hep-th/9701162))

A more formal discussion is in 

* B. Andreas and D. Hernandez Ruiperez, Adv. Theor. Math. Phys. Volume 7, Number 5 (2003), 751-786 _Comments on N = 1 Heterotic String Vacua _ ([project Euclid](http://projecteuclid.org/euclid.atmp/1111510429))

### Dualities

#### With type I superstring theory

The original conjecture is due to 

* {#Witten05} [[Edward Witten]], section 5 of _String Theory Dynamics In Various Dimensions_, Nucl.Phys.B443:85-126 (1995) ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

More details are then in

* {#PolchinskiWitten96} [[Joseph Polchinski]], [[Edward Witten]], _Evidence for Heterotic - Type I String Duality_, Nucl.Phys.B460:525-540,1996 ([arXiv:hep-th/9510169](http://arxiv.org/abs/hep-th/9510169))

#### With $F$-theory
 {#DualityWithFTheory}

The [[duality between F-theory and heterotic string theory]] originates in

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_ ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))

* {#FriedmanMorganWitten97} Robert Friedman, [[John Morgan]], [[Edward Witten]], _Vector Bundles And F Theory_ ([arXiv:hep-th/9701162](http://arxiv.org/abs/hep-th/9701162))

Reviews include

* {#Donagi98} [[Ron Donagi]], _ICMP lecture on heterotic/F-theory duality_ ([arXiv:hep-th/9802093](http://arxiv.org/abs/hep-th/9802093))

* Bj&#246;rn Andreas, _$N=1$ Heterotic/F-theory duality_ PhD thesis ([pdf](http://edoc.hu-berlin.de/dissertationen/physik/andreas-bjoern/PDF/Andreas.pdf))

### "Open" heterotic string

A kind of unusual boundary condition for heterotic strings, (analogous to open [[M5-branes]] ending in 
[[Yang monopoles]] on [[M9-branes]]) is discussed in

* [[Joseph Polchinski]], _Open Heterotic Strings_, JHEP 0609 (2006) 082 ([arXiv:hep-th/0510033](http://arxiv.org/abs/hep-th/0510033))

[[!redirects heterotic superstring]]
[[!redirects heterotic superstrings]]

[[!redirects heterotic string]]
[[!redirects heterotic strings]]

[[!redirects heterotic supergravity]]