

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

Perturbative [[string theory]] is defined in terms of certain classes of 2d [[CFT]]s. Depending on which class that is, one speaks of different _types_ of string theory.

* In _type II string theory_ the CFTs in question are $(1,1)$-supersymmetric and defined on [[orientation|oriented]] [[worldsheet]]s;

* In _[[heterotic string theory]]_ the CFTs in question are $(0,1)$-supersymmetric and defined on [[orientation|oriented]] [[worldsheet]]s;

* In ...

The Type II string theory referred to here is defined on spaces in [[Lorentzian geometry]]. It is thought that Type II (and the other string theories) can also be defined in spaces with other metric signatures, such as [[type II* string theory]]. See [[non-Lorentzian type II string theory]].

## Properties

### Effective QFT

The [[effective quantum field theory]] of type II string theory containts --besides [[type II supergravity]] -- the [[self-dual higher gauge theory]] of [[RR-fields]] and [[Kalb-Ramond field]]s.


### Anomaly cancellation

Apart from the [[Weyl anomaly]], which cancels for 10-dimensional [[target space]]s, the [[action functional]] of the [[string]]-[[sigma-model]] also in general has an _[anomalous action functional](http://ncatlab.org/nlab/show/quantum+anomaly#AnomalousActionFunctional)_ , for two reasons:

1. The [[holonomy|higher holonomy]] of the higher [[background gauge field]]s is in general not a function, but a [[section]] of a [[line bundle]];

1. The fermionic [[path integral]] over the [[worldsheet]]-[[spinor]]s of the [[superstring]] produces as section of a [[Pfaffian line bundle]].

In order for the action functional to be well-defined, the [[tensor product]] of these different anomaly [[line bundle]]s over the bosonic [[configuration space]] must have trivial class (as [[connection on a bundle|bundles with connection]], even). This gives rise to various further anomaly cancellation conditions:

For the open [[type II string]] the condition is known as the [[Freed-Witten anomaly cancellation]] condition: it says that the restriction of the [[B-field]] to any [[D-brane]] must consistute the twist of a [[twisted spin^c structure]] on the brane.

A more detailed analysis of these type II anomalies is in ([DFMI](#DFMI)) and ([DFMII](#DFMII)).

### Background fields and orientifolding


[[!include string theory and cohomology theory -- table]]

* [[intersecting D-brane models]]

### Dualities

Some [[dualities in string theory]] involving [[type II string theory]]:

#### Duality with heterotic string theory

See _[[duality between type II and heterotic string theory]]_.

#### Duality with M-theory

See _[[duality between type IIA string theory and M-theory]]_.

#### Duality with F-theory 

See _[[F-theory]]_.


### Holographic dual

By a [[holographic principle]] realized in this case as [[AdS/CFT correspondence]] (see the references there), type II string theory is supposed to be dual to 4-dimensional [[super Yang-Mills theory]].

### Partition function and elliptic genus

[[!include genera and partition functions - table]]


## Related concepts

* [[string theory]]

  * [[heterotic string theory]]

    * [[Green-Schwarz mechanism]]

    * [[dual heterotic string theory]]

    * [[Witten genus]], [[string orientation of tmf]]

  * **type II string theory**
   
    * [[massive type IIA string theory]]


    [[Diaconescu-Moore-Witten anomaly]]

    [[type II geometry]]

    [[elliptic genus]]
 
    4d [[super Yang-Mills theory]]

  * **[[type I string theory]]**

  * [[type 0 string theory]]

* [[landscape of string theory vacua]]


## References

### General

Physics textbook accounts include

* [[Joseph Polchinski]], _[[String theory]]_, volume II, section 10

* [[Eric D'Hoker]], _String theory -- lecture 7: Free superstrings_ , in part 3 of

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

A comprehensive discussion of the ([[differential cohomology|differential]]) [[cohomology|cohomological]] nature of general type II/type I [[orientifold]] backgrounds is in 

* {#DFM09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

with details in

* {#Freed} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_ ([[FreedESI2012.pdf:file]])
 
* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_, Surveys in Differential Geometry, Volume 15 (2010) ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581), [doi:10.4310/SDG.2010.v15.n1.a4](http://dx.doi.org/10.4310/SDG.2010.v15.n1.a4))


 
Related lecture notes / slides include

* [[Jacques Distler]], _Orientifolds and Twisted KR-Theory_ (2008) ([pdf](http://www.perimeterinstitute.ca/pdf/files/731c5f3a-928f-453a-b569-db5c574d2a6c.pdf))

* [[Daniel Freed]], _Dirac charge quantiation, K-theory, and orientifolds_, talk at a workshop _Mathematical methods in general relativity and quantum field theories_, November, 2009 ([pdf](http://www.ma.utexas.edu/users/dafr/paris_nt.pdf))

* [[Greg Moore]], _The RR-charge of an orientifold_ ([ppt](http://www.physics.rutgers.edu/~gmoore/AnnArbor_Feb2010_FINAL.ppt))


 

### $(p,q)$-Strings and S-duality

* [[John Schwarz]], opening talk at [Strings 2013](http://strings2013.sogang.ac.kr/), ([pdf](http://strings2013.sogang.ac.kr/design/default/data/john_schwarz.pdf))

### Quantum anomalies

Discussion of type II [[quantum anomalies]] is in 

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#DFMI}

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_ ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581))
  {#DFMII} 

An exposition is at

* [[Dan Freed]], _Lectures on K-theory and orientifolds_ (2012) ([pdf](http://www.ma.utexas.edu/users/dafr/ESI.pdf))

### Classical solutions / vacua

Description of type II backgrounds in terms of [[generalized complex geometry]]/[[Courant Lie 2-algebroids]] is in 

* [[Mariana Grana]], Francesco Orsi, _$N=1$ vacua in Exceptional Generalized Geometry_ ([arXiv:1105.4855](http://arxiv.org/abs/1105.4855))

### Holography

A [[holographic principle|holographic]] description of type II by [[higher dimensional Chern-Simons theory]] is discussed in

* Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))


[[!redirects type II superstring]]
[[!redirects type II string]]
[[!redirects type II superstrings]]
[[!redirects type II strings]]

[[!redirects type II superstring theory]]

[[!redirects type II String Theory]]


[[!redirects type IIA string theory]]
[[!redirects type IIB string theory]]
[[!redirects Type IIB string theory]]

[[!redirects type IIA superstring theory]]
[[!redirects type IIB superstring theory]]

[[!redirects type IIA superstring]]
[[!redirects type IIB superstring]]
[[!redirects type IIA superstrings]]
[[!redirects type IIB superstrings]]



