
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A long list of mathematical structures happens to have a classification that is in [[bijection]] with the [[simply laced Dynkin diagrams]] of types A, D and E (but excluding type B and C), for instance 

* [[Platonic solids]]

* [[finite group|finite]] [[subgroups]] of the [[special orthogonal group]] $SO(3)$ and of the [[special unitary group]] $SU(2)$ (see at [[classification of finite rotation groups]]) ([Milnor 57](#Milnor57), see e.g. [Keenan 03, theorem 4](#Keenan03))

* [[simply laced Dynkin diagrams]] (their [[simple Lie groups]])

\begin{imagefromfile}
  "file_name": "ADEDynkin.jpg",
  "width": 490
\end{imagefromfile}

* connected [[quivers]] with a [[finite number]] of [[indecomposable object|indecomposable]] [[quiver representations]] over an [[algebraically closed field]] 

  ([[Gabriel's theorem]])

* 7d [[spherical space forms]] with [[spin structure]] carrying $N \geq 4$ [[Killing vectors]] (see at [spherical space form -- 7d with spin structure](spherical+space+form#7DSphericalSpaceFormsWithSpinStructure)) 

  equivalently: [[near horizon geometries]] of smooth (i.e. non-[[orbifold]]) $\geq \tfrac{1}{2}$ [[BPS state|BPS]] [[black brane|black]] [[M2-brane]]-solutions of the [[equations of motion]] of [[11-dimensional supergravity]]

  This is due to [MFFGME 09](#MFFGME09).


[[!include 7d spherical space forms -- table]]


* [[du Val singularities]] (see [[ADE singularity]])


* [[singularities]] of [[elliptic fibrations]] (see there are _[classification of singular fibers](elliptic+fibration#ClassificationOfSingularFibers)_)

* certain 4d [[ALE spaces]] ([Kronheimer 89](#Kronheimer89))

* certain [[2d CFTs]]

* certain [[6d (2,0)-supersymmetric QFT|6d CFTs]]

* intersection diagrams of vanishing 2-cycles in [[K3]]s (e.g. [BBS 07, p.423](#BBS07))

and many more. 

[[!include ADE -- table]]

The obvious question for what might be the conceptual origin of this joint classification is attributed to ([Arnold 76](#Arnold76)). 

Starting with ([Douglas-Moore 96](#DouglasMoore96)) is the observation that many of these structures are naturally aspects of the description of [[string theory]] [[KK-compactification|KK-compactified]] on _[[orbifolds]] with [[ADE singularities]]_ of the form $\mathbb{C}^n \sslash \Gamma$ for $\Gamma$ a [[finite group|finite]] [[subgroup]] of $SL_2(\mathbb{C})$.

## Via $N=2 $ super Yang-Mills theory
 {#ViaSuperYangMillsTheory}

Various seemingly unrelated structures in mathematics fall into an "ADE classification". Notably [[finite group|finite]] [[subgroups]] of [[special unitary group|SU(2)]] and [[compact Lie group|compact]] [[simple Lie groups]] do. The way this works usually is that one tries to classify these structures somehow, and ends up finding that the classification is governed by the combinatorics of [[Dynkin diagrams]] (see also _[[McKay correspondence]]_).

While that does explain a bit, it seems the statement that both the [[icosahedral group]] and the Lie group [[E8]] are related to the same [[Dynkin diagram]] somehow is still more a question than an answer. Why is that so?

The first key insight is due to [Kronheimer 89](ADE+singularity#Kronheimer89a). He showed that the (resolutions of) the [[orbifold]] quotients $\mathbb{C}^2/\Gamma$ for finite subgroups $\Gamma$ of $SU(2)$ are precisely the generic form of the [[gauge group|gauge]] [[orbits]] of the [[direct product group]] of $U(n_i)$s acting in the evident way on the [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, where $i$ and $j$ range over the vertices of the [[Dynkin diagram]], and $(i,j)$ over its edges.

This becomes more illuminating when interpreted in terms of [[gauge theory]]: in a [[quiver gauge theory]] the [[gauge group]] is a [[direct product group]] of  $U(n_i)$ factors associated with vertices of a [[quiver]], and the [[particles]] which are [[charged particle|charged]] under this gauge group arrange, as a [[linear representation]], into a [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, for each edge of the quiver. 

Pick one such particle, and follow it around as the gauge group transforms it. The space swept out is its gauge [[orbit]], and [Kronheimer 89](#Kronheimer89) says that if the quiver is a Dynkin diagram, then this gauge orbit looks like $\mathbb{C}^2/\Gamma$.

On the other extreme, gauge theories are of interest whose gauge group is not a big direct product, but is a [[simple Lie group]], such as [[special unitary group|SU(N)]] or [[E8]]. The mechanism that relates the two classes of examples is [[spontaneous symmetry breaking]] ("[[Higgs field|Higgsing]]"): the ground state energy of the field theory may happen to be achieved by putting the fields at any one point in a higher dimensional space of field configurations, acted on by the gauge group, and fixing any one such point "spontaneously" singles out the corresponding [[stabilizer subgroup]]. 

Now here is the final ingredient: it is [[N=2 D=4 super Yang-Mills theory]] ("[[Seiberg-Witten theory]]") which have a potential that is such that its [[vacua]] break a simple gauge group such as $SU(N)$ down to a Dynkin diagram [[quiver gauge theory]]. One place where this is reviewed, physics style, is in [Albertsson 03, section 2.3.4](N=2+D=4+super+Yang-Mills+theory#Albertsson03).

More precisely, these theories have two different kinds of vacua, those on the "[[Coulomb branch]]" and those on the "[[Higgs branch]]" depending on whether the scalars of the "[[vector multiplets]]" (the gauge field sector) or of the "[[hypermultiplet]]" (the matter field sector) vanish. The statement above is for the Higgs branch, but the Coulomb branch is supposed to behave "dually".

So that then finally is the relation, in the ADE classification, between the simple Lie groups and the finite subgroups of SU(2): start with an N=2 super Yang Mills theory with gauge group a simple Lie group. Let it spontaneously find its vacuum and consider the orbit space of the remaining spontaneously broken symmetry group. That is (a resolution of) the orbifold quotient of $\mathbb{C}^2$ by a discrete subgroup of $SU(2)$.




## Related concepts

* [[McKay correspondence]]

## References

### General Surveys

* {#Arnold76} [[Vladimir Arnold]], _Problems in present day mathematics_, (1976) in Felix E. Browder, _Mathematical developments arising from Hilbert problems_, Proceedings of symposia in pure mathematics 28, American Mathematical Society, p. 46, _Problem VIII. The A-D-E classifications_ (V. Arnold).



A survey is in

* Michael Hazewinkel, W Hesseling, Dirk Siersma, and Ferdinand Veldkamp, _The ubiquity of Coxeter Dynkin diagrams (an introduction to the ADE problem)_, Nieuw Archief voor Wiskunde 25 (1977), 257-307. ([pdf](http://oai.cwi.nl/oai/asset/10039/10039A.pdf))

which in turn is summarized in

* {#Siegel14} Kyler Siegel, _The Ubiquity of the ADE classification in Nature_ , 2014 ([pdf](http://math.stanford.edu/~ksiegel/ADEClassifications.pdf))

See also

* Wikipedia, _[ADE classification](http://en.wikipedia.org/wiki/ADE_classification)_

Discsssion of the free finite group actions on spheres goes back to

* {#Milnor57} [[John Milnor]], _Groups which act on $S^n$ without fixed points_, American Journal of Mathematics Vol. 79, No. 3 (Jul., 1957), pp. 623-630 ([JSTOR](http://www.jstor.org/stable/2372566))

Review inclues

* {#Keenan03} [[Adam Keenan]], _Which finite groups act freely on spheres?_, 2003 ([pdf](http://www.math.utah.edu/~keenan/actions.pdf))

Discussion of [[ALE spaces]] via ADE include

* {#Kronheimer89} [[Peter Kronheimer]], _The construction of ALE spaces as hyper-K&#228;hler quotients_, J. Differential Geom. Volume 29, Number 3 (1989), 665-683. ([Euclid](https://projecteuclid.org/euclid.jdg/1214443066))


Related stuff includes...

on [[immersions]] of [[3-spheres]] into $\mathbb{R}^4$:

* Shumi Kinjo, _Immersions of 3-sphere into 4-space associated with Dynkin diagrams of types A and D_ ([arXiv:1309.6526](http://arxiv.org/abs/1309.6526))

### In string theory

The original articles explaining the appearance of ADE classification from within [[string theory]] include

* {#DouglasMoore96} [[Michael Douglas]], [[Gregory Moore]], _D-branes, Quivers, and ALE Instantons_ ([arXiv:hep-th/9603167](http://arxiv.org/abs/hep-th/9603167))

* [[Clifford Johnson]], [[Robert Myers]], _Aspects of Type IIB Theory on ALE Spaces_, Phys.Rev. D55 (1997) 6382-6393 ([arXiv:hep-th/9610140](http://arxiv.org/abs/hep-th/9610140))

* [[Michael Douglas]], [[Brian Greene]], [[David Morrison]], _Orbifold Resolution by D-Branes_, Nucl.Phys. B506:84-106,1997 ([arXiv:hep-th/9704151](http://arxiv.org/abs/hep-th/9704151))

* [[Brian Greene]], [[Calin Lazaroiu]], Mark Raugas, _D-branes on Nonabelian Threefold Quotient Singularities_, Nucl.Phys. B553 (1999) 711-749 ([arXiv:hep-th/9811201](http://arxiv.org/abs/hep-th/9811201))

* Andrea Cappelli, Jean-Bernard Zuber, _A-D-E Classification of Conformal Field Theories_ ([arXiv:0911.3242](http://arxiv.org/abs/0911.3242))

Surveys include

* MO discussion, _[ADE classification from string theory](http://mathoverflow.net/a/34680/381)_

Discussion of an ADE-classification of BPS [[Freund-Rubin compactifications]] is in 

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))


Specifically the ADE classfication involved in the [[6d (2,0)-supersymmetric QFT]] on the [[M5-brane]] is discussed in 

* {#Witten95} [[Edward Witten]], _Some Comments On String Dynamics_ ([arXiv:hep-th/9507121](http://arxiv.org/abs/hep-th/9507121))

* {#HeckmannMorrisonVafa13} [[Jonathan Heckman]], [[David Morrison]], [[Cumrun Vafa]], _On the Classification of 6D SCFTs and Generalized ADE Orbifolds_ ([arXiv:1312.5746](http://arxiv.org/abs/1312.5746))

Discussion in the context of [[M-theory on G2-manifolds]] includes

* {#Acharya02} [[Bobby Acharya]], section 3.1.1 of _M Theory, $G_2$-manifolds and Four Dimensional Physics_,  Classical and Quantum Gravity Volume 19 Number 22, 2002  ([pdf](http://users.ictp.it/~pub_off/lectures/lns013/Acharya/Acharya_Final.pdf))

* {#BBS07} [[Katrin Becker]], [[Melanie Becker]], [[John Schwarz]], p. 423 of _String Theory and M-Theory: A Modern Introduction_, 2007


[[!redirects ADE classifications]]

[[!redirects ADE-classification]]
[[!redirects ADE-classifications]]


[[!redirects A-D-E classification]]
[[!redirects A-D-E classifications]]

