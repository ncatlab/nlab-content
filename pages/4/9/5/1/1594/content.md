+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
 {:toc}

## Idea

An [[orbifold]] is much like a [[smooth manifold]] but possibly with [[singularities]] of the form of [[fixed points]] of [[finite group|finite]] [[group]]-[[actions]].

\begin{imagefromfile}
  "file_name": "OrbifoldTypes.jpg",
  "width": 240,
  "float": "right",
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [Hyde-Ramsden-Robins 14](#HydeRamsdenRobins14))" 
\end{imagefromfile}

Where a [[smooth manifold]] is a [[space]] locally modeled on [[Cartesian spaces]]/[[Euclidean spaces]] $\mathbb{R}^n$, an _orbifold_ is, more generally, a [[space]] that is locally modeled on [[Lie groupoid|smooth]] [[action groupoids]] ([[homotopy quotients]]) $\mathbb{R}^n\sslash G$ of a [[finite group]] $G$ [[action|acting]] on a [[Cartesian space]].

This turns out to be broadly captured ([Moerdijk-Pronk 97](#MoerdijkPronk97), [Moerdijk 02](#Moerdijk02)) by saying that an orbifold is a [[proper groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoid]]. ([[Morita equivalence|Morita equivalent]] Lie groupoids correspond to the same orbifolds.)

The word _orbifold_ was introduced in ([Thurston 1992](#Thurston)), while the original name was _$V$-manifold_ ([Satake](#Satake)), and was taken in a more restrictive sense, assuming that the [[actions]] of [[finite groups]] on the charts are always [[effective group action|effective]]. Nowadays these are called _effective orbifolds_ and those which are global quotients by a finite group are _[[global quotient orbifolds]]_.  

There is also a notion of finite stabilizers in [[algebraic geometry]]. A singular variety is called an (algebraic) _orbifold_ if it has only so-called _orbifold singularities_.

## Definition

An orbifold is a stack presented by an [[orbifold groupoid]].

## Properties

### General

* One can consider a [[bicategory]] of proper &#233;tale Lie groupoids and the orbifolds will be the objects of certain bicategorical [[localization]] of this bicategory (a result of [Moerdijk-Pronk 97](#MoerdijkPronk97)). 


* Equivalently, every orbifold is globally a quotient of a smooth manifold by an [[action]] of finite-dimensional [[Lie group]] with finite [[stabilizer subgroup|stabilizers]] in each point. (eg ([Adem-Leida-Ruan 2007](#ALR07)), Corollary 1.24)


### Global quotient orbifolds
 {#GlobalQuotientOrbifolds}

In ([ALR 07, theorem 1.23](#ALR07)) it is asserted that every effective orbifold $X$ (paracompact, Hausdorff) is isomorphic to a [[global quotient orbifold]], specifically to a global quotient of $O(n)$ (where $n$ is the dimension of $X$) acting on the [[frame bundle]] of $X$ (which is a manifold).

### (Co)homology

It has been noticed that the topological invariants of the underlying topological space of an orbifold as a topological space with an orbifold structure are not appropriate, but have to be corrected leading to [[orbifold Euler characteristics]], [[orbifold cohomology]] etc. One of the constructions which is useful in this respect is the [[inertia orbifold]] (the inertia stack of the original orbifold) which gives rise to "twisted sectors" in Hilbert space of a quantum field theory on the orbifold, and also to twisted sectors in the appropriate cohomology spaces. A further generalization gives multitwisted sectors. 




## Examples

* Some basic building blocks of orbifolds:

  The quotient of a  [[ball]] by a [[discrete group|discrete]] [[subgroup]] of the [[special orthogonal group]] of rotations is an orbifold, and orbifolds may be obtained by cutting out balls from ordinary [[smooth manifolds]] and gluing in these orbifold quotients.

* The [[moduli stack of elliptic curves]] over the [[complex numbers]] is an orbifold, being the [[homotopy quotient]] of the [[upper half plane]] by the [[special linear group]] acting by [[Möbius transformations]].

* For $\mathcal{G}$ any orbifold, then the [[mapping space]] $\mathcal{G}^{\Pi(S^1)} = \mathcal{G}^{B\mathbb{Z}}$ is again an orbifold, called the [[inertia orbifold]].

* [[G2-orbifolds]]

* [[lens spaces]]

* [[ADE singularities]]

* [[metric cones]]


## Related concepts

* [[étale groupoid]], [[differentiable stack]]

* [[orbispace]], [[topological stack]]

* [[Riemannian orbifold]]

  * [[flat orbifold]]

* [[Lorentzian orbifold]]

* [[complex orbifold]]

* [[symplectic orbifold]]

* [[super-orbifold]]

* [[discrete torsion]]

* [[motivation for higher differential geometry]]

* [[orbifold Euler characteristic]]

* [[orbifold K-theory]], [[orbifold differential K-theory]]

Orbifolds are in [[differential geometry]] what [[Deligne-Mumford stacks]] are in [[algebraic geometry]]. See also at _[[geometric invariant theory]]_ and _[[GIT-stable point]]_.

Orbifolds may be regarded as a kind of _[[stratified spaces]]_.

See also 

* [[étale groupoid]]

* [[stable map]]

* [[orbifold cohomology]]

* [[Gromov-Witten theory]]

Orbifolds in [[string theory]]:

* [[fractional D-brane]]

  [[permutation D-brane]]

* [[ADE singularity]]

* [[orientifold]]



## References

### General

The original articles:

* {#Satake} [[Ichiro Satake]], _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363 ([doi:10.1073/pnas.42.6.359]( https://doi.org/10.1073/pnas.42.6.359))

* [[Ichiro Satake]], _The Gauss&#8211;Bonnet theorem for $V$-manifolds_, J. Math. Soc. Japan 9 (1957), 464&#8211;492 ([euclid:1261153826](https://projecteuclid.org/euclid.jmsj/1261153826))

* {#Thurston} [[William Thurston]], _Three-dimensional geometry and topology,_ preliminary draft, University of Minnesota, Minnesota, (1992)
  
  which in completed and revised form is available as his book: 

  _The Geometry and Topology of Three-Manifolds;_ ([web](http://library.msri.org/books/gt3m/))

  in particular the orbifold discussion is in [chapter 13](http://library.msri.org/books/gt3m/PDF/13.pdf)

* [[André Haefliger]], _Groupoides d'holonomie et classifiants_, Astérisque no. 116 (1984), p. 70-97 ([numdam:AST_1984__116__70_0/](http://www.numdam.org/item/AST_1984__116__70_0/))

and specifically for orbifolds in [[complex geometry]]:

* [[Walter Lewis Baily]], _On the quotient of an analytic manifold by a group of analytic homeomorphisms_, PNAS 40 (9) 804-808 (1954) ([doi:10.1073/pnas.40.9.804](https://doi.org/10.1073/pnas.40.9.804))

* [[Walter Lewis Baily]], _The Decomposition Theorem for V-Manifolds_, American Journal of Mathematics Vol. 78, No. 4 (Oct., 1956), pp. 862-888 ([jstor:2372472](https://www.jstor.org/stable/2372472))

For careful comparative review of the definitions in these original articles see [IKZ 10](#IKZ10).



Survey of basic orbifold theory:

* Daryl Cooper, Craig Hodgson, Steve Kerckhoff, _Three-dimensional Orbifolds and Cone-Manifolds_,  MSJ Memoirs Volume 5, 2000 ([pdf](https://web.math.ucsb.edu/~cooper/37.pdf), [euclid:1389985812](https://projecteuclid.org/euclid.msjm/1389985812))

* [[Ieke Moerdijk]], [[Janez Mrčun]], Section 2.4 of: _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics  __91__, 2003. x+173 pp. ISBN: 0-521-83197-0 ([doi:10.1017/CBO9780511615450](https://doi.org/10.1017/CBO9780511615450))


* {#BoyerGalicki07} [[Charles Boyer]], [[Krzysztof Galicki]], Chapter 4 of: _Sasakian Geometry_, Oxford Mathematical Monographs, Oxford University Press, 2007 ([doi:10.1093/acprof:oso/9780198564959.001.0001](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780198564959.001.0001/acprof-9780198564959))

* {#Kaye07} Adam Kaye, _Two-Dimensional Orbifolds_, 2007 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2007/REUPapers/FINALFULL/Kaye.pdf))

* Michael Davis, _Lectures on orbifolds and reflection groups_, 2008 ([pdf](https://math.osu.edu/sites/math.osu.edu/files/08-05-MRI-preprint.pdf))

* {#Porti09} Joan Porti, _An introduction to orbifolds_, 2009 ([pdf](http://mat.uab.es/~porti/orbifoldLeiden.pdf))

* {#Snowden11} Andrew Snowden, _Introduction to orbifolds_, 2011 ([pdf](https://ocw.mit.edu/courses/mathematics/18-904-seminar-in-topology-spring-2011/final-paper/MIT18_904S11_finlOrbifolds.pdf))

* {#AdemKlaus} [[Alejandro Adem]], Michele Klaus, _Lectures on orbifolds and group cohomology_ ([pdf](http://www.math.ubc.ca/~adem/hangzhou.pdf), [[AdemKlausOrbifolds.pdf:file]])

* Francisco C. Caramello Jr, _Introduction to orbifolds_ ([arXiv:1909.08699](https://arxiv.org/abs/1909.08699))

See also

* Wikipedia,  _[Orbifolds](http://en.wikipedia.org/wiki/Orbifold)_ 

  (which is mainly tailored toward [Thurston's approach](#Thurston)). 


Textbook account:

* {#Ratcliffe06} [[John Ratcliffe]], _Geometric Orbifolds_, chapter 13 in _Foundations of Hyperbolic Manifolds_, Graduate Texts in Mathematics 149, Springer 2006 ([doi:10.1007/978-0-387-47322-2](https://doi.org/10.1007/978-0-387-47322-2), <a href="http://entsphere.com/pub/pdf/Ratcliffe%20-%20Foundations%20of%20hyperbolic%20manifolds%20(2e)%20-%20GTM%20149.pdf">pdf</a>)

* [[Michael Kapovich]], Chapter 6 of: _Hyperbolic Manifolds and Discrete Groups_,  Modern Birkhäuser Classics, Birkhäuser 2008 ([doi:10.1007/978-0-8176-4913-5](https://link.springer.com/book/10.1007/978-0-8176-4913-5))

Application to [[moduli spaces of curves]] and [[moduli spaces of Riemann surfaces]]:

* Lizhen Ji, [[Shing-Tung Yau]], _Transformation Groups and Moduli Spaces of Curves_, International Press of Boston 2011 ([ISBN:9781571462237](https://www.intlpress.com/site/pub/pages/books/items/00000353/index.php))

On [[Riemannian orbifolds]]:

* Christian Lange, _Orbifolds from a metric viewpoint_ ([arXiv:1801.03472](https://arxiv.org/abs/1801.03472))

* Renato G. Bettiol, Andrzej Derdzinski, Paolo Piccione, _Teichmüller theory and collapse of flat manifolds_, Annali di Matematica (2018) 197: 1247 ([arXiv:1705.08431](https://arxiv.org/abs/1705.08431), [doi:10.1007/s10231-017-0723-7](https://doi.org/10.1007/s10231-017-0723-7))

* {#HydeRamsdenRobins14} S. T. Hyde, S. J. Ramsden and V. Robins, _Unification and classification of two-dimensional crystalline patterns using orbifolds_, Acta Cryst. (2014). A70, 319-337 ([doi:10.1107/S205327331400549X](https://doi.org/10.1107/S205327331400549X))


Survey of applications in [[mathematical physics]] and notably in [[string theory]]:

* {#AdemMoravaRuan02} [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]], _[[Orbifolds in Mathematics and Physics]]_, Contemporary Mathematics 310 American Mathematical Society, 2002


Orbifolds often appear as [[moduli spaces]] in differential geometric setting:

* [[Dietmar Salamon]], [[Joel Robbin|Joel W. Robbin]], _A construction of the Deligne--Mumford orbifold_, J. Eur. Math. Society, ISSN 1435-9855, Vol. 8, N&#186; 4, 2006, 611-699 ([arXiv](http://arxiv.org/abs/math/0407090))

The generalization of orbifolds to _weighted [[branched manifolds]]_ is discussed in

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_, J. Symplectic Geom. Volume 4, Number 3 (2006), 259-315 ([project euclid](http://projecteuclid.org/euclid.jsg/1180135649)).

On [[orbifolds]], [[orbifold cohomology]] and specifically on [[Chen-Ruan cohomology]] and [[orbifold K-theory]]:

* {#ALR07} [[Alejandro Adem]], [[Johann Leida]], [[Yongbin Ruan]], _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))


### As Lie groupoids
 {#ReferencesAsLieGroupoids}


Discussion of orbifolds as [[Lie groupoids]]/[[differentiable stacks]]:
 
* {#MoerdijkPronk97} [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf), [doi:10.4171/LEM/56-3-4](http://dx.doi.org/10.4171/LEM/56-3-4))

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

* {#Lerman08} [[Eugene Lerman]], _Orbifolds as stacks?_, Enseign. Math. (2), 56 3-4 (2010) ([arXiv:0806.4160](http://arxiv.org/abs/0806.4160), [doi:10.4171/LEM/56-3-4](http://dx.doi.org/10.4171/LEM/56-3-4))

Review:

* Alexander Amenta, _The Geometry of Orbifolds via Lie Groupoids_, ANU 2012 ([arXiv:1309.6367](https://arxiv.org/abs/1309.6367))

Analogous discussion for topological orbifolds as [[topological stacks]]:

* Vesta Coufal, [[Dorette Pronk]], Carmen Rovi, [[Laura Scull]], Courtney Thatcher, _Orbispaces and their Mapping Spaces via Groupoids: A Categorical Approach_, Contemporary Mathematics 641 (2015): 135-166 ([arXiv:1401.4772](https://arxiv.org/abs/1401.4772))


Discussion of the corresponding perspective in [[algebraic geometry]], via [[Deligne-Mumford stacks]]:

* {#Kresch09} [[Andrew Kresch]], _On the geometry of Deligne-Mumford stacks_ ([doi:10.5167/uzh-21342](https://doi.org/10.5167/uzh-21342), [pdf](https://www.zora.uzh.ch/id/eprint/21342/1/geodm.pdf)), in:  D. Abramovich, A. Bertram, L. Katzarkov, R. Pandharipande, M. Thaddeus (eds.) _Algebraic Geometry: Seattle 2005_, Proceedings of Symposia in Pure Mathematics 80, Providence, Rhode Island: American Mathematical Society 2009, 259-271 ([pspum-80-1](https://bookstore.ams.org/pspum-80-1))


The [[mapping stacks]] of orbifolds are discussed in

* W. Chen, _On a notion of maps between orbifolds_, I. Function spaces, Commun. Contemp. Math. 8 (2006), no. 5, 569&#8211;620.

* {#RobertsVozzo18} [[David Roberts]], [[Raymond Vozzo]], _The Smooth Hom-Stack of an Orbifold_, In : Wood D., de Gier J., Praeger C., Tao T. (eds) 2016 MATRIX Annals. MATRIX Book Series, vol 1. Springer, Cham (2018) ([arXiv:1610.05904](https://arxiv.org/abs/1610.05904), [doi:10.1007/978-3-319-72299-3_3](https://doi.org/10.1007/978-3-319-72299-3_3))

Discussion of [[principal bundles]] and [[fiber bundles]] over orbifolds:

* [[Camille Laurent-Gengoux]], [[Jean-Louis Tu]], [[Ping Xu]], _Chern-Weil map for principal bundles over groupoids_, Math. Z. 255, 451–491 (2007) ([arXiv:math/0401420](https://arxiv.org/abs/math/0401420), [doi:10.1007/s00209-006-0004-4](https://doi.org/10.1007/s00209-006-0004-4))

* Christopher Seaton, _Characteristic Classes of Bad Orbifold Vector Bundles_, Journal of Geometry and Physics 57 (2007), no. 11, 2365--2371 ([arXiv:math/0606665](https://arxiv.org/abs/math/0606665))


An expected relation of orbifolds ([[orbispaces]]) to [[global equivariant homotopy theory]]:

* [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019)) (on the relation to [[orbispaces]]/[[topological stacks]])


### As diffeological spaces
  {#ReferencesAsDiffeologicalSpaces}

Discussion of orbifolds regarded as naive local quotient [[diffeological spaces]]:

* {#IKZ10} [[Patrick Iglesias-Zemmour]], [[Yael Karshon]], Moshe Zadka, _Orbifolds as diffeologies_, Transactions of the American Mathematical Society 362 (2010), 2811-2831 ([arXiv:math/0501093](https://arxiv.org/abs/math/0501093))

* {#Watts15} [[Jordan Watts]], _The Differential Structure of an Orbifold_, Rocky Mountain Journal of Mathematics, Vol. 47, No. 1 (2017), pp. 289-327 ([arXiv:1503.01740](https://arxiv.org/abs/1503.01740))


### Orbifold cobordism

Orbifold [[cobordisms]] are discussed in 

* K. S. Druschel, _Oriented Orbifold Cobordism_, Pacific J. Math., 164(2) (1994), 299-319 ([doi:10.2140/pjm.1994.164.299](http://dx.doi.org/10.2140/pjm.1994.164.299), [pdf](https://msp.org/pjm/1994/164-2/pjm-v164-n2-p04-p.pdf))

* K. S. Druschel, _The Cobordism of Oriented Three Dimensional Orbifolds_, Pacific J. Math., bf 193(1) (2000), 45-55.

* Andres Angel, _Orbifold cobordism_ ([pdf](http://www.math.uni-bonn.de/people/aangel79/Orbifold%20cobordism.pdf)) 

See also at _[[orbifold cobordism]]_.

[[tangential structure]] on [[orbifolds]] (in the context of [[factorization homology]]):

* [[Tim Weelinck]], _Equivariant factorization homology of global quotient orbifolds_ ([arXiv:1810.12021](https://arxiv.org/abs/1810.12021), [talk pdf](https://www.maths.ed.ac.uk/~tweelinck/efhqsp.pdf))

* John Pardon, _Orbifold bordism and duality for finite orbispectra_ ([arXiv:2006.12702](https://arxiv.org/abs/2006.12702))

### In string theory
 {#ReferencesInStringTheory}


\begin{imagefromfile}
  "file_name": "GreenStringOrbifold.jpg",
  "width": 700,
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [Green 86](string+theory#Green86))" 
\end{imagefromfile}


In [[perturbative string theory]], orbifolds as [[target spaces]] for a [[string]] [[sigma-model]] were first considered in 

* {#DixonHarveyVafaWitten85} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds_, Nuclear Physics B Volume 261, 1985, Pages 678-686 (<a href="https://doi.org/10.1016/0550-3213(85)90593-0">doi:10.1016/0550-3213(85)90593-0</a>)

* {#DixonHarveyVafaWitten86} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds (II)_, Nuclear Physics B Volume 274, Issue 2, 15 September 1986, Pages 285-314 (<a href="https://doi.org/10.1016/0550-3213(86)90287-7">doi:10.1016/0550-3213(86)90287-7</a>)

and then further developed notably in 

* {#DVVV89} [[Robbert Dijkgraaf]], [[Cumrun Vafa]], [[Erik Verlinde]], [[Herman Verlinde]], _The operator algebra of orbifold models_, Comm. Math. Phys. Volume 123, Number 3 (1989), 485-526 ([euclid:1104178892](https://projecteuclid.org/euclid.cmp/1104178892))

* [[Eric Zaslow]], _Topological orbifold models and quantum cohomology rings_, Comm. Math. Phys. 156 (1993), no. 2, 301&#8211;331.

Discussion of [[blow-up]] of orbifold [[singularities]] in string theory:

* [[Paul Aspinwall]], _Resolution of Orbifold Singularities in String Theory_ ([arXiv:hep-th/9403123](https://arxiv.org/abs/hep-th/9403123))

In terms of [[vertex operator algebras]]:

* [[Yi-Zhi Huang]], _Representation theory of vertex operator algebras and orbifold conformal field theory_ ([arXiv:2004.01172](https://arxiv.org/abs/2004.01172))

For [[orbifolds]] in [[string theory]] also the references at 

* _[[Riemannian orbifold]]_, _[[toroidal orbifold]]_

* _[[fractional D-brane]]_

* _[[Gepner model]]_

* _[[orientifold]]_

* _[[RR-field tadpole cancellation]]_

Review of orbifolds in the context of string [[KK-compactifications]] and [[intersecting D-brane models]] includes

* {#BailibLove99} D. Bailin, A. Love, _Orbifold compactifications of string theory_, Phys. Rept. 315 (1999) 285-408 (<a href="https://doi.org/10.1016/S0370-1573(98)00126-4">doi:10.1016/S0370-1573(98)00126-4</a>, [spire:504382](https://inspirehep.net/literature/504382))

* {#Wendland01} [[Katrin Wendland]], _Orbifold Constructions of K3: A Link between Conformal Field Theory and Geometry_, in _[[Orbifolds in Mathematics and Physics]]_ ([arXiv:hep-th/0112006](https://arxiv.org/abs/hep-th/0112006))

* {#Giedt02} Joel Giedt, _Heterotic Orbifolds_ ([arXiv:hep-ph/0204315](https://arxiv.org/abs/hep-ph/0204315))

* [[Dieter Lüst]], S. Reffert, E. Scheidegger, S. Stieberger, _Resolved Toroidal Orbifolds and their Orientifolds_, Adv.Theor.Math.Phys.12:67-183, 2008 ([arXiv:hep-th/0609014](https://arxiv.org/abs/hep-th/0609014))

* {#Reffert07} Susanne Reffert, _The Geometer's Toolkit to String Compactifications_, lectures at _[String and M theory approaches to particle physics and cosmology](https://www.ggi.infn.it/showevent.pl?id=11)_, 2007 ([arXiv:0706.1310](https://arxiv.org/abs/0706.1310))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], Chapter 8 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012 ([doi:10.1017/CBO9781139018951](https://doi.org/10.1017/CBO9781139018951))



* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Chapter 10.5 _Toroidal orbifolds_,  of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013

and for orbifolds of [[G2-manifolds]] for [[M-theory on G2-manifolds]]

* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ ([arXiv:1512.05114](http://arxiv.org/abs/1512.05114))

* [[Frank Reidegeld]], _$G_2$-orbifolds with ADE-singularities_ ([pdf](https://core.ac.uk/download/pdf/159317626.pdf))


For [[topological strings]] the [[path integral as a pull-push transform]] for target orbifolds -- in analogy to what [[Gromov-Witten theory]] is for [[Deligne-Mumford stacks]] -- has first been considered in 

* {#ChenRuan01} Weimin Chen, [[Yongbin Ruan]], _Orbifold Gromov-Witten Theory_, in _[[Orbifolds in Mathematics and Physics]]_ (Madison, WI, 2001), 25&#8211;85, Contemp. Math., 310, Amer. Math. Soc., Providence, RI, 2002 ([arXiv:math/0103156](http://arxiv.org/abs/math/0103156))
 A review with further pointers is in 

* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))
 

category: Lie theory



[[!redirects orbifolds]]

[[!redirects effective orbifold]]
[[!redirects effective orbifolds]]

