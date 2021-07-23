
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
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _type I string theory_ is [[type IIB string theory]] on [[orientifold]] [[spacetimes]], hence on [[O9-planes]]. 

Its [[T-duality|T-dual]], called _type I' string theory_, is  [[type IIA string theory]] on [[O8-planes]], which under the [[duality between M-theory and type IIA string theory]] is M-theory [[KK-compactification|KK-compactified]] on the [[orientifold]] $S^1 \times S^1 \sslash \mathbb{Z}_2$ (see also _[[M-theory on S1/G_HW times H/G_ADE]]_):

$$
  \array{
    M 
    \\
    {}^{ \mathllap{S^1 \times S^1/\mathbb{Z}_2 }}\big\downarrow
    \\
    I' &\underset{T}{\leftrightarrow}& I
  }
$$

<center>
<img src="https://ncatlab.org/nlab/files/OrientifoldLocalTadpoleCancellation.jpg" width="520">
</center>

> table from [BLT 13](#BlumenhagenLustTheisen13)


## Properties

### Tadpole cancellation and $SO(32)$-GUT in Type I
 {#TadpoleCancellationAndSO32GUT}

For type I string theory on [[flat orbifold|flat]] ([[toroidal orbifold|toroidal]]) [[target spacetime]] [[orientifolds]] $\mathbb{R}^{9,1}$
(i.e. for [[type IIB string theory]] on flat toroidal [[O9-planes]])
[[RR-field tadpole cancellation]] requires 32 [[D-branes]] (see [this Remark](orientifold+plane#ContingOfDBranesOnOrientifolds) for counting D-branes in [[orientifolds]]) to cancel the [[O-plane charge]] of -32 ([here](orientifold+plane#OPlaneChargeForFlatOrientifolds)).

Under the [[duality between type I and heterotic string theory]] this translates to the [[semi-spin group|semi-spin]] [[gauge group]] [[SemiSpin(32)]] of [[heterotic string theory]].

Discussion of type-I [[string phenomenology]] and [[grand unified theory]] based on [[SO(32)]] type-I strings: ([MMRB 86](#MMRB86), [Ibanez-Munoz-Rigolin 98](#IbanezMunozRigolin98), [Yamatsu 17](#Yamatsu17)).

### Tadpole cancellation and $SO(16) \times SO(16)$-GUT in Type I'

For type I' string theory on [[flat orbifold|flat]] ([[toroidal orbifold|toroidal]]) [[target spacetime]] [[orientifolds]] $X^{8,1} \times \mathbb{S}^1/\mathbb{Z}_2$
(i.e. for [[type IIA string theory]] on two flat toroidal [[O8-planes]])
[[RR-field tadpole cancellation]] requires 16 [[D-branes]] (see [this Remark](orientifold+plane#ContingOfDBranesOnOrientifolds) for counting D-branes in [[orientifolds]]) on each of the two [[O8-planes]] to cancel the total [[O-plane charge]] of $-32 = 2 \cdot (-16)$ ([here](orientifold+plane#OPlaneChargeForFlatOrientifolds)).

Discussion of [[Spin(16)]]-[[GUT]] phenomenology:

(...)


### Orbifolds of type I

Type I' on [[toroidal orbifold|toroidal]] [[orientifolds]] with [[ADE-singularities]] (e.g. [Bergman&Rodriguez-Gomez 12, Sec. 3](#BergmanRodriguezGomez12))

[[duality in string theory|dual]] to [[heterotic M-theory on ADE-orbifolds]].



(...)


### Dualities

#### String-string dualities

See at _[[duality between type I and heterotic string theory]]_

#### Horava-Witten theory

One considers the [[KK-compactification]] of [[M-theory]] on a [[cyclic group of order 2|Z/2]]-[[orbifold]] of a [[torus]], hence of the [[Cartesian product]] of two [[circles]] 

$$  
  \array{
    & S^1_A &\times& S^1_B
    \\
    \text{radius}: &  R_{11} && R_{10}
  }
$$

such that the reduction on the first factor $S^1_A$ corresponds to the [[duality between M-theory and type IIA string theory]], hence so that subsequent [[T-duality]] along the second factor yields [[type IIB string theory]] (in its [[F-theory]]-incarnation). Now the diffeomorphism which exchanges the two circle factors and hence should be a symmetry of M-theory is interpreted as [[S-duality]] in [[type II string theory]]:

$$
  IIB \overset{S}{\leftrightarrow} IIB
$$

<center>
<img src="https://ncatlab.org/nlab/files/HoaravaWittenCompactifications.jpg" width="500">  
</center>


> graphics taken from [Horava-Witten 95, p. 15](#HoravaWitten95) 

If one considers this situation additionally with a $\mathbb{Z}/2\mathbb{Z}$-[[orbifold]] quotient of the first circle factor, one obtains the [[duality between M-theory and heterotic string theory]] ([[Horava-Witten theory]]). If instead one performs it on the second circle factor, one obtains [[type I string theory]].

Here in both cases the [[involution]] [[action]] is by [[reflection]] of the circle at a line through its center. Hence if we identify $S^1 \simeq \mathbb{R} / \mathbb{Z}$ then the action is by multiplication by /1 on the [[real line]].

In summary:

M-theory on

* $(S^1_A \sslash \mathbb{Z}_2 ) \times S^1_B$ yields [[heterotic string theory]]

* $S^1_A \times \left( S^1_B \sslash \mathbb{Z}_2 \right)$ yields [[type I' string theory]]

Hence the [[S-duality]] that swaps the two circle factors corresponds to _[[duality between type I and heterotic string theory]]_. 



$$
  \array{
     HE 
       &\overset{KK/\mathbb{Z}^A_2}{\leftrightarrow}& 
     M 
       &\overset{KK/\mathbb{Z}^B_2}{\leftrightarrow}& 
     I'
     \\
     \mathllap{T}\updownarrow
     &&  && 
     \updownarrow \mathrlap{T}  
     \\
     HO 
     && \underset{\phantom{A}S\phantom{A}}{\leftrightarrow} && 
     I
  }
$$

<center>
<img src="https://ncatlab.org/nlab/files/HoravaWittenCompactificationsII.jpg" width="500">  
</center>

> graphics taken from [Horava-Witten 95, p. 16](#HoravaWitten95) 



## Related concepts

[[!include string theory and cohomology theory -- table]]


## References

### General

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 4.4.3 of: _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Section 9.4 and 10.6 of: _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics, Springer 2013

Relation to [[M-theory]] (via [[Horava-Witten theory]]):

* {#HoravaWitten95} [[Petr Hořava]], [[Edward Witten]], _Heterotic and Type I string dynamics from eleven dimensions_, Nucl. Phys. B460 (1996) 506 ([arXiv:hep-th/9510209](http://arxiv.org/abs/hep-th/9510209))

* {#HoravaWitten96} [[Petr Hořava]], [[Edward Witten]],  _Eleven dimensional supergravity on a manifold with boundary_, Nucl. Phys. B475 (1996) 94 ([arXiv:hep-th/9603142](http://arxiv.org/abs/hep-th/9603142))

A comprehensive discussion of the ([[differential cohomology|differential]]) [[cohomology|cohomological]] nature of general type II/type I [[orientifold]] backgrounds is in 

* {#DFM09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

with details in

* {#Freed} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_ ([[FreedESI2012.pdf:file]])
 
* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_, Surveys in Differential Geometry, Volume 15 (2010) ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581), [doi:10.4310/SDG.2010.v15.n1.a4](http://dx.doi.org/10.4310/SDG.2010.v15.n1.a4))
 
Related lecture notes / slides include

* [[Jacques Distler]], _Orientifolds and Twisted KR-Theory_ (2008) ([pdf](http://www.perimeterinstitute.ca/pdf/files/731c5f3a-928f-453a-b569-db5c574d2a6c.pdf))

* [[Daniel Freed]], _Dirac charge quantiation, K-theory, and orientifolds_, talk at a workshop _Mathematical methods in general relativity and quantum field theories_, November, 2009 ([pdf](http://www.ma.utexas.edu/users/dafr/paris_nt.pdf))

* {#Moore10} [[Greg Moore]], _The RR-charge of an orientifold_, Oberwolfach talk 2010 ([pdf](https://www.physics.rutgers.edu/~gmoore/Oberwolfach_June2010_FINAL.pdf), [[MooreOrientifold2010.pdf:file]], [ppt](http://www.physics.rutgers.edu/~gmoore/AnnArbor_Feb2010_FINAL.ppt))

### Type I'

Original articles on [[type I' string theory]]:

* {#Schwarz00} [[John Schwarz]], _Some Properties of Type I' String Theory_, in: [[Mikhail Shifman]] (ed.), _[[The Many Faces of the Superworld]]_, pp. 388-397 (2000) ([arXiv:hep-th/9907061](https://arxiv.org/abs/hep-th/9907061), [doi:10.1142/9789812793850_0023](https://doi.org/10.1142/9789812793850_0023))

* Justin R. David, Avinash Dhar, Gautam Mandal, _Probing Type I' String Theory Using D0 and D4-Branes_, Phys. Lett. B415 (1997) 135-143 ([arXiv:hep-th/9707132](https://arxiv.org/abs/hep-th/9707132))

Type I' on [[toroidal orbifold|toroidal]] [[orientifolds]] with [[ADE-singularities]] ([[duality in string theory|dual]] to [[heterotic M-theory on ADE-orbifolds]]):

* {#BergmanRodriguezGomez12} [[Oren Bergman]], Diego Rodriguez-Gomez, _5d quivers and their $AdS_6$ duals_, JHEP07 (2012) 171 ([arxiv:1206.3503](https://arxiv.org/abs/1206.3503))



### Phenomenology
 {#Phenomenology}

Type I [[string phenomenology]] and discussion of [[GUT]]s based on [[SO(32)]] type I strings (see also at [heterotic phenomenology](https://ncatlab.org/nlab/show/heterotic+string+theory#ReferencesPhenomenology)):

* {#MMRB86} H.S. Mani, A. Mukherjee, R. Ramachandran, A.P. Balachandran, _Embedding of $SU(5)$ GUT in $SO(32)$ superstring theories_, Nuclear Physics B Volume 263, Issues 3–4, 27 January 1986, Pages 621-628 (<a href="https://doi.org/10.1016/0550-3213(86)90277-4">arXiv:10.1016/0550-3213(86)90277-4</a>)

* {#IbanezMunozRigolin98} [[Luis Ibáñez]], C. Muñoz, S. Rigolin, _Aspects of Type I String Phenomenology_, Nucl.Phys. B553 (1999) 43-80 ([arXiv:hep-ph/9812397](https://arxiv.org/abs/hep-ph/9812397))

* {#Dudas00} Emilian Dudas, _Theory and Phenomenology of Type I strings and M-theory_, Class. Quant. Grav.17:R41-R116, 2000 ([arXiv:hep-ph/0006190](https://arxiv.org/abs/hep-ph/0006190))


* {#Yamatsu17} Naoki Yamatsu, _String-Inspired Special Grand Unification_, Progress of Theoretical and Experimental Physics, Volume 2017, Issue 10, 1  ([arXiv:1708.02078](https://arxiv.org/abs/1708.02078), [doi:10.1093/ptep/ptx135](https://doi.org/10.1093/ptep/ptx135))


### Duality

Discussion of [[duality in string theory|duality]] with [[heterotic string theory]] includes the following.

The original conjecture is due to 

* {#Witten05} [[Edward Witten]], section 5 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126 (1995) ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

More details are then in

* {#PolchinskiWitten96} [[Joseph Polchinski]], [[Edward Witten]], _Evidence for Heterotic - Type I String Duality_, Nucl.Phys.B460:525-540,1996 ([arXiv:hep-th/9510169](http://arxiv.org/abs/hep-th/9510169))

### Geometric engineering of $D=6$ $\mathcal{N}=(1,0)$ SCFT

On [[D=6 N=(1,0) SCFTs]] via [[geometric engineering of QFT|geometric engineering]] on [[M5-branes]]/[[NS5-branes]] at D-, E-type [[ADE-singularities]], notably from [[M-theory on S1/G_HW times H/G_ADE]], hence from [[orbifolds]] of [[type I' string theory]] (see at [half NS5-brane](NS5-brane#NSHalfBranes)):

* Michele Del Zotto, [[Jonathan Heckman]], [[Alessandro Tomasiello]], [[Cumrun Vafa]], _6d Conformal Matter_, JHEP02(2015)054 ([arXiv:1407.6359](https://arxiv.org/abs/1407.6359))

* {#GaiottoTomasiello14} [[Davide Gaiotto]], [[Alessandro Tomasiello]], _Holography for $(1,0)$ theories in six dimensions_, JHEP12(2014)003 ([arXiv:1404.0711](https://arxiv.org/abs/1404.0711))

* Kantaro Ohmori, Hiroyuki Shimizu, _$S^1/T^2$ Compactifications of 6d $\mathcal{N} = (1,0)$ Theories and Brane Webs_, J. High Energ. Phys. (2016) 2016: 24 ([arXiv:1509.03195](https://arxiv.org/abs/1509.03195))

* {#HKLY15} Hirotaka Hayashi, Sung-Soo Kim, Kimyeong Lee, Futoshi Yagi, _6d SCFTs, 5d Dualities and Tao Web Diagrams_, JHEP05 (2019)203 ([arXiv:1509.03300](https://arxiv.org/abs/1509.03300))

* Ibrahima Bah, Achilleas Passias, [[Alessandro Tomasiello]], _$AdS_5$ compactifications with punctures in massive IIA supergravity_, JHEP11 (2017)050 ([arXiv:1704.07389](https://arxiv.org/abs/1704.07389))



[[!redirects type I superstring]]
[[!redirects type I superstring theory]]

[[!redirects type I' string theory]]



