

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A hyperbolic [[Kac-Moody Lie algebra]] in the E-series 

... [[E6]], [[E7]], [[E8]], [[E9]], [[E10]], $E_{11}$, ...

## Properties

### As U-duality group of 0d supergravity

$E_{11}$ is conjectured ([West 01](#West01)) to be the [[U-duality]] group (see there) of [[11-dimensional supergravity]] [[KK-compactification|compactified]] to 0 dimensions.

[[!include U-duality -- table]]

### Fundamental representation and brane charges
 {#FundamentalRepresentationAndBraneCharges}

The first [[fundamental representation]] of $E_{11}$, usually denoted $l_1$, is argued, since ([West 04](#West04)), to contain in its decomposition into [[representations]] of $GL(11)$ the representations in which the [[charges]] of the [[M-branes]] and other [[BPS states]] transform.

According to ([Nicolai-Fischbacher 03, first three rows of table 2 on p. 72](#NicolaiFischbacher03), [West 04](#West04), [Kleinschmidt-West 04](#KleinschmidtWest04)) and concisely stated for instance in ([West 11, (2.17)](#West11)), the level decomposition of $l_1$ under $GL(11)$ starts out as so:

$$
  l_1 
  \simeq
  \underset{level\,0}{
  \underbrace{
    \mathbb{R}^{10,1}
  }}
  \oplus
  \underset{level\,1}{
  \underbrace{
    \wedge^2 (\mathbb{R}^{10,1})^\ast
  }}
  \oplus
  \underset{level\,2}{
  \underbrace{
    \wedge^5 (\mathbb{R}^{10,1})^\ast
  }}
  \oplus
  \underset{level\,3}{\underbrace{
    \wedge^7 (\mathbb{R}^{10,1})^\ast \otimes_s (\mathbb{R}^{10,1})^\ast
    \oplus
    \wedge^8 (\mathbb{R}^{10,1})^\ast
  }}
  \oplus 
  \cdots
$$

Here the $level \leq 2$-truncation happens to coincide with the bosonic [[body]] underlying the [[M-theory super Lie algebra]] and via the relation of that to [[BPS charges]] in [[11-dimensional supergravity]]/[[M-theory]], the [[direct sums|direct summands]] here have been argued to naturally correspond to 

* level 0: [[momentum]]

* level 1: [[M2-brane]] charge

* level 2: [[M5-brane]] charge

* level 3: [[dual graviton]] charge ([West 11, section N](#West11)) (has two components [^ThanksToKleinschmidt])

[^ThanksToKleinschmidt]: private communication with [[Axel Kleinschmidt]] 


## References

### General 

* [[Peter West]], section 16.7 of _[[Introduction to Strings and Branes]]_

* {#NicolaiFischbacher03} [[Hermann Nicolai]], Thomas Fischbacher, _Low Level Representations for E10 and E11_ ([arXiv:hep-th/0301017](http://arxiv.org/abs/hep-th/0301017))

* H. Mkrtchyan, R. Mkrtchyan, _$E_{11},K_{11}$ and $EE_{11}$_ ([arXiv:hep-th/0407148](http://arxiv.org/abs/hep-th/0407148))

### Relation to supergravity
 {#ReferencesRelationToSupergravity}

Literature discussing $E_{11}$ [[U-duality]] and in the context of [[exceptional generalized geometry]] of [[11-dimensional supergravity]].

Review includes

* [[Peter West]], section 17.5 of _[[Introduction to Strings and Branes]]_

* [[Fabio Riccioni]], _$E_{11}$ and M-theory_, talk at [Strings07](http://www.ift.uam.es/strings07/) ([pdf slides](http://member.ipmu.jp/yuji.tachikawa/stringsmirrors/2007/riccioni.pdf))

* [[Fabio Riccioni]], [[Peter West]], _The $E_{11}$ origin of all maximal supergravities_, JHEP 0707:063,2007 ([arXiv:0705.0752](http://arxiv.org/abs/0705.0752), [spire](http://inspirehep.net/record/749966/))

* [[Paul Cook]], _Connections between Kac-Moody algebras and M-theory_ PhD thesis ([arXiv:0711.3498](http://arxiv.org/abs/0711.3498))

* {#West16} [[Peter West]], _A brief review of E theory_ ([arXiv:1609.06863](http://arxiv.org/abs/1609.06863))


Original articles include the following:

The observation that $E_{11}$ seems to neatly organize the structures in [[11-dimensional supergravity]]/[[M-theory]] is due to

* {#West01} [[Peter West]], _$E_{11}$ and M theory_, Class. Quant. Grav., 18:4443&#8211;4460, 2001. ([arXiv:hep-th/0104081](http://arxiv.org/abs/hep-th/0104081))

A precursor to ([West 01](#West01)) is 

* [[Bernard Julia]], _Dualities in the classical supergravity limits_ ([arXiv:hep-th/9805083](http://arxiv.org/abs/hep-th/9805083))

as explained in ([Henneaux-Julia-Levie 10](#HenneauxJuliaLevie10)).

The derivation of the [[equations of motion]] of [[11-dimensional supergravity]] and maximally supersymmetric [[5d supergravity]] from a [[vielbein]] with values in the [[semidirect product]] $E_{11}$ with its [[fundamental representation]] is due to

* {#West11} [[Peter West]], _Generalised geometry, eleven dimensions and $E_{11}$_, J. High Energ. Phys. (2012) 2012: 18 ([arXiv:1111.1642](http://arxiv.org/abs/1111.1642))

* Alexander G. Tumanov, [[Peter West]], _$E_{11}$ must be a symmetry of strings and branes_, Physics Letters B Volume 759, 10 August 2016, Pages 663&#8211;671 ([arXiv:1512.01644](https://arxiv.org/abs/1512.01644))

* Alexander G. Tumanov, [[Peter West]], _$E_{11}$ in $11d$_, Physics Letters B Volume 758, 10 July 2016, Pages 278&#8211;285 ([arXiv:1601.03974](https://arxiv.org/abs/1601.03974))


This way that elements of [[cosets]] of the [[semidirect product]] $E_{11}$ with its [[fundamental representation]] may encode [[equations of motion]] of [[11-dimensional supergravity]] follows previous considerations for [[Einstein equations]] in 

* [[Abdus Salam]], J. Strathdee, _Nonlinear realizations. 1: The Role of Goldstone bosons, Phys. Rev. 184 (1969) 1750, 

* [[Chris Isham]], [[Abdus Salam]], J. Strathdee, _Spontaneous, breakdown of conformal symmetry_, Phys. Lett. 31B (1970) 300.

* A. Borisov, V. Ogievetsky, _Theory of dynamical affine and conformal symmetries as the theory of the gravitational field_, Theor. Math. Phys. 21 (1973) 1179-1188 ([web](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=tmf&paperid=3902&option_lang=eng)) 

* V. Ogievetsky, _Infinite-dimensional algebra of general covariance group as the closure of the finite dimensional algebras of conformal and linear groups_, Nuovo. Cimento, 8 (1973) 988.

Further developments of the proposed $E_{11}$ formulation of [[M-theory]] include

* [[Peter West]], _$E_{11}$, ten forms and supergravity_, JHEP0603:072,2006 ([arXiv:hep-th/0511153](http://arxiv.org/abs/hep-th/0511153))

* [[Fabio Riccioni]], [[Peter West]], _Dual fields and $E_{11}$_, Phys.Lett.B645:286-292,2007 ([arXiv:hep-th/0612001](http://arxiv.org/abs/hep-th/0612001))

* [[Fabio Riccioni]], [[Peter West]], _E(11)-extended spacetime and gauged supergravities_, JHEP 0802:039,2008 ([arXiv:0712.1795](http://arxiv.org/abs/0712.1795))

* [[Fabio Riccioni]], Duncan Steele, [[Peter West]], _The E(11) origin of all maximal supergravities - the hierarchy of field-strengths_, 	JHEP 0909:095 (2009) ([arXiv:0906.1177](http://arxiv.org/abs/0906.1177))

* [[Eric Bergshoeff]], I. De Baetselier, T. Nutma, _E(11) and the Embedding Tensor_ ([arXiv:0705.1304](http://arxiv.org/abs/0705.1304), [poster](http://mms.technologynetworks.net/posters/0364.pdf))

* Guillaume Bossard, [[Axel Kleinschmidt]], Jakob Palmkvist, [[Christopher Pope]], [[Ergin Sezgin]], _Beyond $E_{11}$_ ([arXiv:1703.01305](https://arxiv.org/abs/1703.01305))

Discussion of the [[semidirect product]] of $E_{11}$ with its $l_1$-[[representation]], and arguments that the [[charges]] of the [[M-theory super Lie algebra]] and in fact further brane charges may be identified inside $l_1$ originate in

* {#West04} [[Peter West]], _$E_{11}$, $SL(32)$ and Central Charges_, Phys.Lett.B575:333-
342,2003 ([arXiv:hep-th/0307098](http://arxiv.org/abs/hep-th/0307098))

and was further explored in 

* {#KleinschmidtWest04} [[Axel Kleinschmidt]], [[Peter West]], _Representations of $G^{+++}$ and the role of space-time_, JHEP 0402 (2004) 033 ([arXiv:hep-th/0312247](http://arxiv.org/abs/hep-th/0312247))

* [[Paul Cook]], [[Peter West]], _Charge multiplets and masses for $E(11)$_, JHEP 11 (2008) 091 ([arXiv:0805.4451](http://arxiv.org/abs/0805.4451))

* [[Peter West]], _$E_{11}$ origin of Brane charges and U-duality multiplets_, JHEP 0408 (2004) 052 ([arXiv:hep-th/0406150](http://arxiv.org/abs/hep-th/0406150))



Relation to [[exceptional field theory]] is discussed in

* Alexander G. Tumanov, [[Peter West]], _$E_{11}$ and exceptional field theory_ ([arXiv:1507.08912](http://arxiv.org/abs/1507.08912))

Relation to [[Borcherds superalgebras]] is discussed in

* Pierre Henry-Labordere, [[Bernard Julia]], Louis Paulot, _Borcherds symmetries in M-theory_, JHEP 0204 (2002) 049 ([arXiv:hep-th/0203070](http://arxiv.org/abs/hep-th/0203070))

* {#HenneauxJuliaLevie10} [[Marc Henneaux]], [[Bernard Julia]], J&#233;r&#244;me Levie, _$E_{11}$, Borcherds algebras and maximal supergravity_ ([arxiv:1007.5241](http://arxiv.org/abs/1007.5241))

* {#Palmkvist12} Jakob Palmkvist, _Tensor hierarchies, Borcherds algebras and $E_{11}$_, JHEP 1202 (2012) 066 ([arXiv:1110.4892](http://arxiv.org/abs/1110.4892))


On [[E11]]-[[exceptional field theory]]:

* [[Guillaume Bossard]], [[Axel Kleinschmidt]], [[Ergin Sezgin]], _On supersymmetric E11 exceptional field theory_ ([arXiv:1907.02080](https://arxiv.org/abs/1907.02080))



* [[Guillaume Bossard]], [[Axel Kleinschmidt]], [[Ergin Sezgin]], _A master exceptional field theory_ ([arXiv:2103.13411](https://arxiv.org/abs/2103.13411))

