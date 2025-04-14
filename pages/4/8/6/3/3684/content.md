
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Overview

Consider a [[symplectic manifold]] (representing say a [[phase space]] of a [[physical system]]) of [[dimension]] $2n$  . 

Recall that a [[Lagrangian submanifold]] is a smooth [[submanifold]] of dimension $n$ whose [[tangent spaces]] at all points are [[Lagrangian subspaces]], i.e. maximal [[isotropic subspaces]] with respect to the [[symplectic form]]. Lagrangian submanifold describes the phase of short-wave oscillations. 

The _Maslov index_ is an invariant of a smooth path in a [[Lagrangian submanifold]]. 

The Maslov index can be reinterpreted as a [[characteristic class]] of theories of [[Lagrangian cobordism|Lagrangian and Legendrean cobordism]]. 


## Definition

### As a universal characteristic class

The first [[ordinary cohomology]] of the stable [[Lagrangian Grassmannian]] with [[integer]] [[coefficients]] is isomorphic to the [[integers]]

$$
  H^1(LGrass, \mathbb{Z}) 
  \simeq
  \mathbb{Z}
  \,.
$$

[[generalized the|The]] generator of this [[cohomology group]] is called the _universal Maslov index_

$$
  u \in H^1(LGrass, \mathbb{Z})
  \,.
$$

Since $LGrass$ is a [[classifying space]] for [[tangent bundles]] of [[Lagrangian submanifolds]], this is a [[universal characteristic class]] for Lagrangian submanifolds.

Specifically, given a [[Lagrangian submanifold]] $Y \hookrightarrow X$ of a [[symplectic manifold]] $(X,\omega)$, its [[tangent bundle]] is [[classifying space|classified]] by a function

$$
  i \;\colon\; Y \to LGrass
  \,.
$$

The _Maslov index of $Y$ is the universal Maslov index pulled back along this map

$$
  i^\ast u \in H^1(Y,\mathbb{Z})
  \,.
$$



## Literature

Original article:

* [[Victor Maslov]], _Th&#233;orie des perturbations et m&#233;thodes asymptotiques_ (1972)

Its cohomological interpretation as a [[universal characteristic class]] was explained in

* [[Vladimir Arnold]], _Characteristic class entering in quantization conditions_, Funct. Anal. its Appl. 1967, 1:1, 1&#8211;13, [doi](http://dx.doi.org/10.1007/BF01075861) (&#1042;. &#1048;. &#1040;&#1088;&#1085;&#1086;&#1083;&#1100;&#1076;, "&#1054; &#1093;&#1072;&#1088;&#1072;&#1082;&#1090;&#1077;&#1088;&#1080;&#1089;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1084; &#1082;&#1083;&#1072;&#1089;&#1089;&#1077;, &#1074;&#1093;&#1086;&#1076;&#1103;&#1097;&#1077;&#1084; &#1074; &#1091;&#1089;&#1083;&#1086;&#1074;&#1080;&#1103; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1072;&#1085;&#1080;&#1103;", &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1:1 (1967), 1&#8211;14, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2802&what=fullt&option_lang=rus)) 

See also:

* Wikipedia, *[Maslov index](https://en.wikipedia.org/wiki/Lagrangian_Grassmannian#Maslov_index)*

A review in the context of [[geometric quantization]] (Maslov correction) is in 

* Sean Bates, [[Alan Weinstein]], section 4.2 of _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)

The interpretation of the Maslov index as a quadratic space is due to 

* T. Thomas. _The Maslov index as a quadratic space_. Math. Res. Lett. 13 no. 6 (2006), 985&#8211;999

and this definition and basic examples are briefly collected in

* [[Andrew Ranicki]], _The Maslov Index_, seminar notes 2010/11 ([pdf](http://www.maths.ed.ac.uk/~aar/maslovnotes.pdf))


See also

* Gérard Lion, [[Michèle Vergne]]: *The Weil representation, Maslov index and Theta series*, Progress in Mathematics **6**, Birkhäuser (1980) &lbrack;[doi:10.1007/978-1-4684-9154-8](https://doi.org/10.1007/978-1-4684-9154-8)&rbrack;

* [[Alan Weinstein]], _The Maslov gerbe_, Lett. Math. Phys. __69__, 1-3, July, 2004, [doi](http://dx.doi.org/10.1007/s11005-004-0342-2). ([arXiv:0312274](http://arxiv.org/abs/math/0312274))

* [[Jean Leray]], _Lagrangian analysis and quantum mechanics. A mathematical structure related to asymptotic expansions and the Maslov index_, (trans. from French), MIT Press 1981. xvii+271 pp. 

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Geometric asymptotics_, AMS 1977, [online](http://www.ams.org/online_bks/surv14);   _Semi-classical analysis_, 499 pages, [pdf](http://www-math.mit.edu/~vwg/semistart.pdf) 


* J. J. Duistermaat, _On the Morse index in variational calculus_, Adv. Math. __21__ (1976), 2, 173--195, [pdf](http://www.maths.ed.ac.uk/~aar/papers/duistermaat.pdf). 

* D. Salamon, E. Zehnder, _Morse theory for periodic solutions of Hamiltonian systems and the Maslov index_, Comm. Pure Appl. Math. __45__ (1992), no. 10, 1303--1360, [doi](http://dx.doi.org/10.1002/cpa.3160451004)

* [[Joel Robbin]], [[Dietmar Salamon]], _The Maslov index for paths_, Topology __32__ (1993), no. 4, 827--844, ([doi](http://dx.doi.org/10.1016/0040-9383%2893%2990052-W); preprint version [pdf](http://www.math.ethz.ch/~salamon/PREPRINTS/maslov.pdf)); _The spectral flow and the Maslov index_, Bull. London Math. Soc. __27__ (1995), no. 1, 1--33 ([doi](http://dx.doi.org/10.1112/blms/27.1.1)) 

* A. B. Givental', _Global properties of the Maslov index and Morse theory_, Funct. Anal. Its. Appl. __22__, 2, 1988, [doi](http://dx.doi.org/10.1007/BF01077609) (Rus. orig: &#1092;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;&#1086;&#1078;&#1077;&#1085;&#1080;&#1103; __22__, 1988, &#1074;&#1099;&#1087;. 2, 69&#8212;70: [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1113&volume=22&year=1988&issue=2&fpage=69&what=fullt&option_lang=eng))

* A. B. Givental&#697;, _The nonlinear Maslov index_, in "Geometry of low-dimensional manifolds" vol. 2 (Durham, 1989), 35--43,
London Math. Soc. Lec. Note Ser. __151__, Cambridge Univ. Press 1990. 

* Maurice A. de Gosson, _Maslov classes, metaplectic representation and Lagrangian quantization_, Math. Research __95__, Akademie-Verlag, Berlin, 1997. 186 pp.; _Symplectic geometry, Wigner-Weyl-Moyal calculus, and quantum mechanics in phase space_, 385 pp. [pdf](http://opus.kobv.de/ubp/volltexte/2009/3021/pdf/2006_06.pdf)

* Leo T. Butler, _The Maslov cocycle, smooth structures and real-analytic complete integrability_, [arxiv/0708.3157](http://uk.arxiv.org/abs/0708.3157v2)

* S. Merigon, _L'indice de Maslov en dimension infinie_, [J. Lie Theory 18](http://www.heldermann.de/JLT/JLT18/JLT181/jlt18010.htm) (2008), no. 1, 161--180.

* S. E. Cappell, R. Lee, E. Y. Miller, _On the Maslov index_, Comm. Pure Appl. Math. __47__ (1994), no. 2, 121--186. 

* K. Furutani, _Fredholm&#8211;Lagrangian&#8211;Grassmannian and the Maslov index_, J. Geom. Phys. __51__, 3, July 2004, 269--331, [doi](http://dx.doi.org/10.1016/j.geomphys.2004.04.001)

* Many links are at [[Andrew Ranicki]]'s [Maslov index seminar](http://www.maths.ed.ac.uk/~aar/maslov.htm) page. 

* [[Paolo Piccione]], [[Daniel V. Tausk]]: _A student's guide to symplectic spaces, Grassmannians and Maslov index_, Instituto de Matemática Pura e Aplicada (2011) &lbrack;[pdf](http://www.impa.br/opencms/pt/biblioteca/pm/PM_27.pdf), [[PiccioneTausk-SymplecticSpaces.pdf:file]]&rbrack;


* M. V. Finkelberg, _Orthogonal Maslov index_, Funct. Anal. Appl. 29(1) 72–74 (1995) [doi](https://doi.org/10.1007/bf01077047)

* [[Alan Weinstein]], _The Maslov cycle as a Legendre singularity and projection of a wavefront set_, Bull. Braz. Math. Soc., N.S. 44, 593--610 (2013) [doi](https://doi.org/10.1007/s00574-013-0026-6)

Application in the theory of Schroedinger operators:

* Yuri Latushkin, Alim Sukhtayev, Selim Sukhtaiev, _The Morse and Maslov indices for Schr&#246;dinger operators_, [arxiv/1411.1656](http://arxiv.org/abs/1411.1656); Yuri Latushkin, Alim Sukhtayev, _Hadamard-type formulas via the Maslov form_, [arxiv/1601.07509](http://arxiv.org/abs/1601.07509)

On stability and [[Maslov indices]] of [[geodesics]] in [[pseudo-Riemannian manifold|(semi-)]][[Riemannian manifolds]]:

* [[Paolo Piccione]], [[Alessandro Portaluri]], [[Daniel V. Tausk]]: *Spectral Flow, Maslov Index and Bifurcation of Semi-Riemannian Geodesics*, Annals of Global Analysis and Geometry **25** (2004) 121–149 \[<a href="https://doi.org/10.1023/B:AGAG.0000018558.65790.db">doi:10.1023/B:AGAG.0000018558.65790.db</a>\]



[[!redirects Maslov indices]]

[[!redirects Maslov class]]
[[!redirects Maslov classes]]
