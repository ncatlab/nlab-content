+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
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

Since global $N=1$ supersymmetry for a long time has been considered a promising phenomenological model in high energy physics, this fact has induced a lot of interest in [[heterotic string theory on CY3-manifolds]].

### Enhanced supersymmetry

A priori the [[worldsheet]] [[2d SCFT]] describing the quantum heterotic string has $N=(1,0)$ [[supersymmetry]]. Precisely if the corresponding [[target space]] [[effective field theory]] has $N=1$ supersymmetry does the worldsheet theory enhance to $N=(2,0)$ supersymmetry. See at _[[2d (2,0)-superconformal QFT]]_ and at _[[Calabi-Yau manifolds and supersymmetry]]_ for more on this.

### Dualities
 {#Dualities}

Some [[duality in string theory]] involving the heterotic string:

#### Duality with type I string theory

* [[duality between heterotic and type I string theory]]

#### Duality with type II string theory

See _[[duality between heterotic and type II string theory]]_.

#### Duality with M-theory

See _[[duality between heterotic string theory and M-theory]]_

#### Duality with F-theory

See _[[duality between heterotic string theory and F-theory]] 

and see [references below](#DualityWithFTheory).


### Partition function and Witten genus

[[!include genera and partition functions - table]]

### General gauge backgrounds and parameterized WZW models
 {#GeneralGaugeBackgroundsAndParameterizedWZWModels}

The traditional construction of the [[worldsheet]] theory of the heterotic string produces via the [[current algebra]] of the left-moving worldsheet [[fermions]] only those [[E8]]-[[background gauge fields]] which are reducible to $Spin(16)/\mathbb{Z}_2$-[[principal connections]] ([Distler-Sharpe 10, sections 2-4](#DistlerSharpe10)). But it is known that, for instance, the [[duality between F-theory and heterotic string theory]] produces more general gauge backgrounds ([Distler-Sharpe 10, section 5](#DistlerSharpe10)). 

In ([Distler-Sharpe 10, section 7](#DistlerSharpe10)), following ([Gates-Siegel 88](#GatesSiegel88)), it is argued that the way to fix this is to consider [[parameterized WZW models]], parameterized over the [[E8]]-[[principal bundle]] over [[spacetime]]. This does allow the incorporation of all $E_8$-background gauge fields, and the [[Green-Schwarz anomaly]] (and its cancellation) of the heterotic string now comes out as being equivalently the [[obstruction]] (and its lifting) for such a parameterized WZW term to exist.

Moreover, where the traditional construction only produces level-1 [[current algebras]], this construction accommodates all levels, and it is argued ([Distler-Sharpe 10, section 8.5](#DistlerSharpe10)) that the [[elliptic genus]] of the resulting [[parameterized WZW models]] are the [[equivariant elliptic genera]] found by Liu and Ando ([Ando 07](#Ando07)).

However, presently questions remain concerning formulating a [[sigma-model]] for strings propagating on the total space of the bundle, as it is only the chiral part of the geometric WZW model that appears in the heterotic string. (...)

### Superspace formulation

The [[gauge field]] [[field strength|strength]]:

$F_{\alpha \beta} = 0$ ([Witten 86](#Witten86), [Bonora-Bregola-Lechner-Pasti-Tonin 87, above (2.7)](#BonoraBregolaLechnerPastiTonin87), [Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.13)](#BonoraBregolaLechnerPastiTonin87)).

$F_{a \alpha} = \Gamma_{a \alpha \beta} \chi^\beta$ ([Witten 86 (8)](#Witten86), [Atick-Dhar-Ratra 86, (4.14)](#AtickDharRatra86), [Bonora-Pasti-Tonin 87, below (11)](#BonoraPastiTonin87), [Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.27)](#BonoraBregolaLechnerPastiTonin87)).

Here $\chi^\alpha$ is the [[gaugino]].

$F_{a b} = \tfrac{1}{4} (\Gamma_{a b})_\alpha{}^\beta D_\beta \chi^\alpha$ ([Bonora-Pasti-Tonin 87, below (11)](#BonoraPastiTonin87), [Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.28)](#BonoraBregolaLechnerPastiTonin87))

[[equations of motion]]:

$ (D^a \Gamma_a)_{\alpha\beta} \chi^\beta =0 $ ([Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.30)](#BonoraBregolaLechnerPastiTonin87))

$D^b F_{b a} + T_a{}^{b c} F_{b c} = - (\Gamma_a)_{\alpha \beta} \chi^\alpha \chi^\beta - \chi^\alpha L_{\alpha a}$ ([Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.31)](#BonoraBregolaLechnerPastiTonin87)) (where $L_{\alpha a}$ is defined by (2.20) there...)

$\,$

The [[B-field]] [[field strength|strength]]:

$H_{\alpha \beta \gamma} = 0$ ([Atick-Dhar-Ratra 86, (4.2)](#AtickDharRatra86), [Bonora-Pasti-Tonin 87, (15)](#BonoraPastiTonin87), [Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.14)](#BonoraBregolaLechnerPastiTonin87))

$H_{a \alpha \beta} = \phi \Gamma_{a \alpha \beta}$ ([Atick-Dhar-Ratra 86, (4.19)](#AtickDharRatra86), [Bonora-Pasti-Tonin 87, (15)](#BonoraPastiTonin87), [Bonora-Bregola-Lechner-Pasti-Tonin 87, (2.15)](#BonoraBregolaLechnerPastiTonin87))

$\rho \coloneqq D_\alpha \phi$ ([Atick-Dhar-Ratra 86, (4.20)](#AtickDharRatra86))

$H_{a b \alpha} = -\tfrac{1}{2} \Gamma_{a b }_\alpha{}^\beta \rho_\beta$ ([Atick-Dhar-Ratra 86, (4.21)](#AtickDharRatra86))

$H_{a b c} = - \tfrac{3}{2} \phi T_{a b c} + \tfrac{c_1}{4} (\Gamma_{a b c})_{\alpha \beta} tr(\chi^\alpha \chi^\beta)$ ([Atick-Dhar-Ratra 86, (4.22)](#AtickDharRatra86))

According to ([Bonora-Bregola-Lechner-Pasti-Tonin 90](#BonoraBregolaLechnerPastiTonin90)) in fact all these constraints follow from just $T^a_{\alpha \beta}  \propto \Gamma^a_{\alpha \beta}$, up to field redefinition.

See also at _[[torsion constraints in supergravity]]_.


## Related concepts

* [[SemiSpin(16)]], [[SemiSpin(32)]]

* [[small instanton]]

* [[E-string]]

* [[string theory]]

  * **heterotic string theory**

    * [[2d SCFT]], 

      * [[2-spectral triple]], [[Dirac-Ramond operator]]

    * [[2d (2,0)-superconformal QFT]]

    * [[Green-Schwarz mechanism]]

    * [[dual heterotic string theory]]

    * [[heterotic string theory on CY3-manifolds]]

    * [[Witten genus]], [[(2,1)-dimensional Euclidean field theories and tmf]]

  * [[heterotic line bundle]]

  * [[type II string theory]]

  * [[type 0 string theory]]

  * [[landscape of string theory vacua]]

  * [[supersymmetry and Calabi-Yau manifolds]]

* [[string field theory]]

* [[11-dimensional supergravity]]

  * [[Hořava-Witten theory]]

  * [[M-theory]]

* [[AdS-CFT correspondence]]

* [string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)




## References

### General

Heterotic strings were introduced in 

* [[David Gross]], [[Jeffrey Harvey]], [[Emil Martinec]], [[Ryan Rohm]]:

  _Heterotic string theory (I). The free heterotic string_  Nucl. Phys. B 256 (1985), 253 (<a href="https://doi.org/10.1016/0550-3213(85)90394-3">doi:10.1016/0550-3213(85)90394-3</a>)

  _Heterotic string theory (II). The interacting heterotic string_ , Nucl. Phys. B 267 (1986), 75 (<a href="https://doi.org/10.1016/0550-3213(86)90146-X">doi:10.1016/0550-3213(86)90146-X</a>)

* {#CHSW85} [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], [[Edward Witten]], _Vacuum configurations for superstrings_, Nuclear Physics B Volume 258, 1985, Pages 46-74 Nucl. Phys. B 258, 46 (1985) (<a href="https://doi.org/10.1016/0550-3213(85)90602-9">doi:10.1016/0550-3213(85)90602-9</a>)

* {#Schellekens91} [[Bert Schellekens]], _Classification of Ten-Dimensional Heterotic Strings_, Phys.Lett. B277 (1992) 277-284 ([arXiv:hep-th/9112006](http://arxiv.org/abs/hep-th/9112006))

Textbook accounts:

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], vol 3 (which is part 6) of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[Joseph Polchinski]], volume II, section 11 of _[[String theory]]_, 

* [[Eric D'Hoker]], _String theory -- lecture 8: Heterotic strings_  in part 3 (p. 941 of volume II) of

  [[Pierre Deligne]], P. Etingof, [[Dan Freed]], L. Jeffrey, [[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds. . _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

See also:

* [[Eric Sharpe]], _Recent developments in heterotic compactifications_, AMS/IP Stud. Adv. Math. 44 (2008) 209-230 ([arXiv:0801.4080](https://arxiv.org/abs/0801.4080))


* Andrea Fontanella, Tomas Ortin, _On the supersymmetric solutions of the Heterotic Superstring effective action_ ([arxiv:1910.08496](https://arxiv.org/abs/1910.08496))


Relation to [[Donaldson-Thomas theory]] and [[quiver gauge theory]]:

* {#HeLee12} [[Yang-Hui He]], Seung-Joo Lee, _Quiver Structure of Heterotic Moduli_, J. High Energ. Phys. (2012) 2012: 119 ([arXiv:1208.3004](https://arxiv.org/abs/1208.3004))


Discussion of [[higher curvature corrections]]:

* Eric Lescano, Carmen Núñez, Jesús A. Rodríguez, *Supersymmetry, T-duality and Heterotic $\alpha'$-corrections* ([arXiv:2104.09545](https://arxiv.org/abs/2104.09545))




### Orbifold and orientifold compactifications

Heterotic strings on [[orbifolds]]:

* {#DixonHarveyVafaWitten85} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds_, Nuclear Physics B Volume 261, 1985, Pages 678-686 (<a href="https://doi.org/10.1016/0550-3213(85)90593-0">doi:10.1016/0550-3213(85)90593-0</a>)

* {#DixonHarveyVafaWitten86} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds (II)_, Nuclear Physics B Volume 274, Issue 2, 15 September 1986, Pages 285-314 (<a href="https://doi.org/10.1016/0550-3213(86)90287-7">doi:10.1016/0550-3213(86)90287-7</a>)


* Joel Giedt, _Heterotic Orbifolds_ ([arXiv:hep-ph/0204315](https://arxiv.org/abs/hep-ph/0204315))

* Kang-Sin Choi, _Spectra of Heterotic Strings on Orbifolds_, Nucl. Phys. B708: 194-214, 2005 ([arXiv:hep-th/0405195](https://arxiv.org/abs/hep-th/0405195))

Specifically on [[ADE-singularities]]:

* [[Paul Aspinwall]], [[David Morrison]], _Point-like Instantons on K3 Orbifolds_,  Nucl. Phys. B503 (1997) 533-564 ([arXiv:hep-th/9705104](https://arxiv.org/abs/hep-th/9705104))

* {#Witten99} [[Edward Witten]], _Heterotic String Conformal Field Theory And A-D-E Singularities_, JHEP 0002:025, 2000 ([arXiv:hep-th/9909229](https://arxiv.org/abs/hep-th/9909229))





[[!include heterotic string phenomenology -- references]]







### Superspace formulation of Heterotic supergravity 

Discussion of heterotic supergravity in terms of [[superspace]] includes the following.

One solution of the heterotic superspace [[Bianchi identities]] is due to

* {#AtickDharRatra86} [[Joseph Atick]], Avinash Dhar, and Bharat Ratra, _Superspace formulation of ten-dimensional N=1 supergravity coupled to N=1 super Yang-Mills theory_, Phys. Rev. D 33, 2824, 1986 ([doi.org/10.1103/PhysRevD.33.2824](https://doi.org/10.1103/PhysRevD.33.2824))

* {#Witten86} [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B Volume 266, Issue 2, 17 March 1986

A second solution is due to [[Bengt Nilsson]], [[Renata Kallosh]] and others 

* [[Bengt Nilsson]], _Simple 10-dimensional supergravity in superspace_, Nucl. Phys. B188 (1981) 176 (<a href="https://doi.org/10.1016/0550-3213(81)90111-5">doi:10.1016/0550-3213(81)90111-5</a>)


These two solutions are supposed to be equivalent under field redefinition.

See also at _[[torsion constraints in supergravity]]_.

Further references include these:

* {#BonoraPastiTonin87} [[Loriano Bonora]], [[Paolo Pasti]], [[Mario Tonin]], _Superspace formulation of 10D SUGRA+SYM theory a la Green-Schwarz_, Physics Letters B Volume 188, Issue 3, 16 April 1987, Pages 335&#8211;339 (<a href="http://dx.doi.org/10.1016/0370-2693(87)91392-X">doi:10.1016/0370-2693(87)91392-X</a>)

* {#BonoraBregolaLechnerPastiTonin87} [[Loriano Bonora]], M. Bregola, [[Kurt Lechner]], [[Paolo Pasti]], [[Mario Tonin]], _Anomaly-free supergravity and super-Yang-Mills theories in ten dimensions_, Nuclear Physics B
Volume 296, Issue 4, 25 January 1988 (<a href="http://dx.doi.org/10.1016/0550-3213(88)90402-6">doi:10.1016/0550-3213(88)90402-6</a>)

* {#BonoraBregolaLechnerPastiTonin90} [[Loriano Bonora]], M. Bregola; [[Kurt Lechner]], [[Paolo Pasti]], [[Mario Tonin]], _A discussion of the constraints in $N=1$ SUGRA-SYM in 10-D_,  International Journal of Modern Physics A, February 1990, Vol. 05, No. 03 : pp. 461-477 (<a href="https://doi.org/10.1142/S0217751X90000222">doi:10.1142/S0217751X90000222</a>)


* [Castellani-D'Auria-Fre 91, vol 3, part 6](#CastellaniDAuriaFre91)

* {#BBDFLPPRRTZ} L. Bonora, M. Bregola, R. D'Auria, P. Fr&#233; [[Kurt Lechner]], [[Paolo Pasti]], I. Pesando, M. Raciti, F. Riva, [[Mario Tonin]] and D. Zanon, _Some remarks on the supersymmetrization of the Lorentz Chern-Simons form in $D = 10$ $N= 1$ supergravity theories_, Physics Letters B 277 (1992) ([[BonoraSuperGS.pdf:file]])



* {#LechnerTonin08} [[Kurt Lechner]], [[Mario Tonin]], _Superspace formulations of ten-dimensional supergravity_, JHEP 0806:021,2008 ([arXiv:0802.3869](https://arxiv.org/abs/0802.3869))




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







### On elliptic fibrations


Compactified on an [[elliptic curve]] or, more generally, [[elliptic fibration]], heterotic string compactifictions are controled by a choice holomorphic [[stable bundle]] on the compact space. Dually this is an [[F-theory]] compactification on a [[K3]]-bundles.

The basis of this story is discussed in 

* Robert Friedman, [[John Morgan]], [[Edward Witten]], _Vector Bundles And F-Theory_ ([arXiv:hep-th/9701162](http://arxiv.org/abs/hep-th/9701162))

A more formal discussion is in 

* B. Andreas and D. Hernandez Ruiperez, Adv. Theor. Math. Phys. Volume 7, Number 5 (2003), 751-786 _Comments on N = 1 Heterotic String Vacua _ ([project Euclid](http://projecteuclid.org/euclid.atmp/1111510429))

### Dualities

#### With type I superstring theory

The original conjecture is due to 

* {#Witten05} [[Edward Witten]], section 5 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126 (1995) ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

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



[[!include flavor on heterotic M5-branes -- references]]


[[!redirects heterotic superstring]]
[[!redirects heterotic superstrings]]

[[!redirects heterotic string]]
[[!redirects heterotic strings]]

[[!redirects heterotic supergravity]]

[[!redirects HET-theory]]
[[!redirects HET-theories]]



