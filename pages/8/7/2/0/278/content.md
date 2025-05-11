
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Scope

__Differential geometry__ is a mathematical discipline studying geometry of spaces using differential and integral calculus. Classical differential geometry studied submanifolds (curves, surfaces...) in Euclidean spaces. The traditional objects of differential geometry are finite and infinite-dimensional [[differentiable manifold|differentiable manifolds]] modelled locally on [[topological vector space|topological vector spaces]]. Techniques of differential calculus can be further stretched to [[generalized smooth space|generalized smooth spaces]]. One often distinguished analysis on manifolds from differential geometry: analysis on manifolds focuses on functions from a manifold to the ground field and their properties, together with applications like PDEs on manifolds. Differential geometry on the other hand studies objects embedded into the manifold like submanifolds, their relations and additional structures on manifolds like bundles, connections etc. while the topological aspects are studied in a younger branch (from 1950s on) which is called [[differential topology]].

## Generalized smooth spaces from $n$POV

See also [[generalized smooth space]].

Finite-dimensional differential geometry is the [[geometry]] modeled on [[Cartesian space|Cartesian spaces]] and [[smooth functions]] between them.

Formally, it is the [[higher geometry|geometry]] modeled on 
the [[pregeometry (for structured (infinity,1)-toposes)|pre-geometry]] $\mathcal{G} = $[[CartSp]].

This includes a sequence of concepts of [[generalized smooth spaces]]:

* A [[smooth manifold]] (see there for details) is a locally $CartSp$-representable object in the [[sheaf topos]] $Sh(CartSp)$.

* A [[diffeological space]] (see there) is a [[concrete sheaf]] in the [[cohesive topos]] $Sh(CartSp)$.

* a [[Lie groupoid]] is a locally representable object in the [[(2,1)-sheaf]] [[(2,1)-topos]] $Sh_{(2,1)}(CartSp)$;

* an [[∞-Lie groupoid]] is an object in the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$.

Similarly, standard models of [[synthetic differential geometry]] in [[higher geometry]] are modeled on the [[pregeometry (for structured (infinity,1)-toposes)|pre-geometry]] $\mathcal{G} = $[[ThCartSp]]. To wit, the [[cohesive topos]] $Sh(ThCartSp)$ is the [[smooth topos]] called the [[Cahiers topos]]:

* an [[infinitesimal space]] is a certain object in $ThCartSp$;

* an [[∞-Lie algebroid]] is a certain object in the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(ThCartSp)$.


## Related concepts

* [[trigonometry]]

* [[differential geometry of curves and surfaces]]

* [[synthetic differential geometry]]

* [[higher differential geometry]], [[derived differential geometry]]

  * [[higher differential geometry applied to plain differential geometry]]

* [[differential cohesive homotopy type theory]]

* [[differential equations]], [[geometric analysis]]
  
* [[prequantum geometry]], [[higher prequantum geometry]]

* [[D-geometry]]

* [[arithmetic differential geometry]]

* [[Lie theory]]

* [[fiber bundles in physics]]

* [[tangent]], [[tangent vector]], [[tangent bundle]]

* some modern subfields of differential geometry include:

  * [[symplectic geometry]], 

  * [[contact geometry]], 

  * [[complex geometry]],

  * [[Riemannian geometry]], 
  
  * [[Finsler geometry]], 

  * [[symmetric spaces]], 
  
  * [[Fréchet manifolds]]

$\,$

 local model                |   global geometry
----------------------------|-----------------
 [[Klein geometry]]         |   [[Cartan geometry]]
 [[Klein 2-geometry]]       |   [[Cartan 2-geometry]]
 [[higher Klein geometry]]  |   [[higher Cartan geometry]]

$\,$

[[!include geometries of physics -- table]]



## References
 {#References}

> See also references at *[[Riemannian geometry]]*.


### Diff geometry of curves and surfaces
 {#ReferencesDiffGeometryOfCurvesAndSurfaces}

The study of differential geometry goes back to the special case of [[differential geometry of curves and surfaces]]: 

the study of [[curves]]  and [[surfaces]] [[embedding of smooth manifolds|embedded]] into [[Euclidean space]] $\mathbb{R}^3$:

* {#Gauss1827} [[Carl Friedrich Gauss]], _General Investigations of Curved Surfaces_ (1827) ([Gutenberg](http://www.gutenberg.org/ebooks/36856))

* Manfredo P. Do Carmo, *Differential Geometry of Curves and Surfaces*, Prentice-Hall (1976) &lbrack;[pdf](http://www2.ing.unipi.it/griff/files/dC.pdf)&rbrack;

* [[Heinrich W. Guggenheimer]], *Differential Geometry*, Dover (1977) &lbrack;[isbn:9780486634333](https://store.doverpublications.com/products/9780486634333), [ark:/13960/t9t22sk9n](https://archive.org/details/differentialgeom0000gugg/)&rbrack;


* Victor A. Toponogov, *Differential Geometry of Curves and Surfaces --- A Concise Guide*, Springer (2006) &lbrack;[doi:10.1007/b137116](https://doi.org/10.1007/b137116)&rbrack;

* Kristopher Tapp, *Differential Geometry of Curves and Surfaces*, Springer (2016) $[$[doi:10.1007/978-3-319-39799-3](https://doi.org/10.1007/978-3-319-39799-3),  [pdf](https://link.springer.com/content/pdf/10.1007/978-3-319-39799-3.pdf)$]$

* Anton Petrunin, Sergio Zamora Barrera, *What is differential geometry: curves and surfaces* $[$[arXiv:2012.11814](https://arxiv.org/abs/2012.11814)$]$


### General but traditional diff geometry

* [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], _Foundations of differential geometry_, Volume 1 (1963), Volume 2 (1969) Interscience Publishers, reprint: Wiley Classics Library (1996) &lbrack;[ISBN:978-0-470-55558-3](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+2+Volume+Set-p-9780470555583), [Wikipedia entry](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry)&rbrack; 

* [[Michael Spivak]], _[[Calculus on Manifolds]]_ (1971) &lbrack;[pdf](http://www.strangebeautiful.com/other-texts/spivak-calc-manifolds.pdf)&rbrack;


* [[Victor Guillemin]], [[Shlomo Sternberg]], *Geometric asymptotics*, Mathematical Surveys and Monographs **14**, AMS (1977) &lbrack;[ams:surv-14](https://bookstore.ams.org/surv-14)&rbrack;



* [[Yvonne Choquet-Bruhat]], [[Cécile DeWitt-Morette]], *Analysis, manifolds and physics*, North Holland (1982, 2001) &lbrack;[ISBN:9780444860170](https://www.elsevier.com/books/analysis-manifolds-and-physics-revised-edition/choquet-bruhat/978-0-444-86017-0)&rbrack;

  > (with an eye towards [[mathematical physics]])


* Thomas A. Ivey and J.M. Landsberg, *Cartan for Beginners: Differential Geometry via Moving Frames and Exterior Differential Systems*, Graduate Studies in Mathematics **61**, AMS (2003) &lbrack;[doi:10.1090/gsm/061](https://doi.org/10.1090/gsm/061), [pdf](https://people.tamu.edu/~jml//EDSpublic.pdf), [pdf](https://people.tamu.edu/~jml//EDSpublic.pdf)&rbrack;

* [[Michael Spivak]], _A comprehensive introduction to differential geometry_, 5 Volumes 2005

* [[M M Postnikov]], _Lectures on geometry_ 2001 (6 vols.: 1 "Analytic geometry", 2 "Linear algebra", 3 "Diff. manifolds"; 4 "Diff. geometry" (covers extensively fibre bundles and connections); 5 "Lie groups"; 6 "Riemannian geometry")

* [[Sigurdur Helgason]], *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) &lbrack;[ams:gsm-34](https://bookstore.ams.org/gsm-34)&rbrack;

* [[Peter W. Michor]], _Topics in Differential Geometry_, Graduate Studies in Mathematics 93 (2008) &lbrack;[pdf](https://www.mat.univie.ac.at/~michor/dgbook.pdf)&rbrack;

* {#Lee12} [[John Lee]], *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;

* [[Mikhail O. Katanaev]], *Geometrical methods in mathematical physics* (in Russian) &lbrack;[arXiv1311.0733](https://arxiv.org/abs/1311.0733)&rbrack;


* [[Loring Tu]], _Differential Geometry -- Connections, Curvature, and Characteristic Classes_, Springer (2017) &lbrack;[ISBN:978-3-319-55082-4](https://www.springer.com/gp/book/9783319550824)&rbrack;

* {#GallierQuaintance20a} [[Jean Gallier]], [[Jocelyn Quaintance]],  *Differential Geometry and Lie Groups -- A computational perspective*, Geometry and Computing **12**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-46040-2](https://doi.org/10.1007/978-3-030-46040-2), [webpage](https://www.cis.upenn.edu/~jean/gbooks/manif.html)&rbrack;

* {#GallierQuaintance20b} [[Jean Gallier]], [[Jocelyn Quaintance]],  *Differential Geometry and Lie Groups -- A second course*, Geometry and Computing **13**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-46047-1](https://doi.org/10.1007/978-3-030-46047-1), [webpage](https://www.cis.upenn.edu/~jean/gbooks/manif.html)&rbrack;

* [[Andrzej Derdzinski]], *Differential Geometry*, lecture notes &lbrack;[pdf](https://people.math.osu.edu/derdzinski.1/courses/851-852-notes.pdf), [[Derdzinski-DifferentialGeometry.pdf:file]]&rbrack;


With emphasis on [[G-structures]]:

* {#Sternberg64} [[Shlomo Sternberg]], _Lectures on differential geometry_, Prentice-Hall (1964), AMS (1983) &lbrack;ISBNJ:978-0-8218-1385-0, [ams:chel-316](https://bookstore.ams.org/chel-316), [ark:/13960/t1pg9dv6k](https://archive.org/details/lecturesondiffer0000ster)&rbrack;


With emphasis on [[natural bundles]]:


* {#KolarSlovakMichor93} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[book webpage](http://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3)
[pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;

With emphasis on [[Cartan geometry]]:

* [[Richard W. Sharpe]], *Differential geometry -- Cartan's generalization of Klein's Erlagen program*, Graduare Texts in Mathematics **166**, Springer (1997) &lbrack;[ISBN:9780387947327](https://link.springer.com/book/9780387947327)&rbrack;


Lecture notes:

* {#Conrad} [[Brian Conrad]]: *Handouts on Differential Geometry* &lbrack;[web](http://math.stanford.edu/~conrad/diffgeomPage/handouts.html)&rbrack;

* [[Liviu Nicolaescu]], _Lectures on the Geometry of Manifolds_, 2018 ([pdf](https://www3.nd.edu/~lnicolae/Lectures.pdf))

 
Introductions with an eye towards applications in ([[mathematical physics|mathematical]])[[physics]], specifically to [[gravity]] and [[gauge theory]]:

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_, Cambridge University Press (1997, 2004, 2012) &lbrack;[doi:10.1017/CBO9781139061377](https://doi.org/10.1017/CBO9781139061377), [website](http://www.math.ucsd.edu/~tfrankel/) with errata and preface for 3rd edition)&rbrack;

* [[Chris Isham]]: *[[Modern Differential Geometry for Physicists]]*, Lecture Notes in Physics **61**, World Scientific  (1999, 2001) &lbrack;[doi:10.1142/0894](https://doi.org/10.1142/0894), [pdf](https://cdn.preterhuman.net/texts/science_and_technology/physics/Mathematical_Physics/Modern%20Differential%20Geometry%20for%20Physicists%202nd%20ed.,%20-%20C.%20Isham.pdf), [pdf](https://homepages.uc.edu/~herronda/Diff_Geometry/DG4physics.pdf)&rbrack;

A discussion in the context of [[Frölicher spaces]] and [[diffeological spaces]]:

* [[Andreas Kriegl]], [[Peter Michor]], _[[The convenient setting of global analysis]]_, Math. Surveys and Monographs __53__, Amer. Math. Soc. 1997. 618 pages




See also

* Sigmundur Gudmundsson, _An Introduction to Riemannian Geometry_ ([pdf](http://www.maths.lth.se/matematiklu/personal/sigma/Riemann.pdf))

* Wikipedia, _[differential geometry](http://en.wikipedia.org/wiki/Differential_geometry)_

### Higher diff geometry

See at _[[higher differential geometry]]_.

### Derived diff geometry

For [[derived differential geometry]] see

* [[Dominic Joyce]], _D-manifolds and d-orbifolds: a theory of derived differential geometry_ ([web](http://people.maths.ox.ac.uk/joyce/dmanifolds.html))

* [[Urs Schreiber]], _[[schreiber:Seminar on derived differential geometry]]_

