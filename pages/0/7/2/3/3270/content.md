
> This entry is about discontinuities in parameter dependence of (often asymptotic) solutions of [[differential equations]] and similar phenomena (notably in the context of [[BPS states]]) with stability parameters (and their stability slopes) in [[algebraic geometry]] which are often interpreted as crossing the walls of marginal stability in [[physics]]. For the different notions of the same name in [[Morse theory]] see at _[[Cerf wall crossing]]_ and for the (Weyl chamber wall) crossing functors in representation theory see [[wall crossing functor]]. 

# Contents
* table of contents
{: toc}

## Overview

In the study of [[solitons]], one may try a [[WKB approximation|WKB-style approximation]] to a nonlinear [[wave equation]] (see also _[[eikonal equation]]_, _[[Maslov index]]_, etc.). Stokes has observed that when trying to connect the local solutions, one has discontinuities along certain lines, now called **Stokes lines**. This is called the [[Stokes phenomenon]]. Similar issues appear in study of [[isomonodromic deformation]]s of nonlinear [[ODEs]] in the [[complex plane]], which is also relevant in [[soliton]] theory, and [[integrable systems]], and special functions like [[Painlevé transcendent]]s. This has especially been studied by the Kyoto school (Jimbo, Miwa, Sato, [[Masaki Kashiwara|Kashiwara]] etc.), including the use of [[D-modules]] and [[microlocal analysis]]. The Kyoto school found a connection of isomonodromic theory to what is called [[holonomic quantum field]]s. 

The solutions of meromorphic differential equations can be expressed in terms of [[meromorphic connection]]s. Then the slopes related to the solutions can be viewed as features of particular objects in a category of $D$-[[D-module|modules]]. More generally, slope filtrations are structures which appear in many other additive categories, e.g. in [[Hodge theory]], theory of Dieudonn&#233; modules and so on. Many of those are related to the stability of the objects, which is important in the construction of [[moduli spaces]]. 

In [[algebraic geometry]], [[Grothendieck]] has shown how to correctly define and construct some fundamental [[moduli spaces]], like Hilbert schemes and Quot schemes for [[coherent sheaves]]. The work has been continued by [[David Mumford]] who geometrized classical invariant theory into [[geometric invariant theory]]. To keep moduli under control, one needs to impose stability conditions on objects and also look at classes with some fixed data: those involve slopes or equivalently phase factors. This is thus  similar to the phases of eikonal in the case of Stokes phenomenon. 
Cf. also Harder-Narasimhan filtration, [[Castelnuovo-Mumford regularity]] (cf. [wikipedia](http://en.wikipedia.org/wiki/Castelnuovo%E2%80%93Mumford_regularity)) etc. 

### In supersymmetric field theory

In [[super Yang-Mills theory]] the number of [[BPS states]] is locally constant as a function of the parameters of the theory, but it may jump at certain "walls" in the [[moduli spaces]] of parameters. The precise behaviour of the BPS states as one crosses these walls is studied as "wall crossing phenomena". 

Another example are the [[moduli spaces]] of [[Higgs bundles]], studied by [[Carlos Simpson]] and others, which have special cases with interpretations both in geometry and in the gauge theory (instantons). It appears that sometimes they can be linked to the geometric picture. [[Riemann-Hilbert correspondence]], spectral transform and similar correspondences again play a major role. 

Surely, one often works at the derived level. An adaptation of the  notion of stability into the setup of [[triangulated categories]] has been introduced by Bridgeland. Bridgeland stability for the derived categories of (boundary conditions of) D-branes (B-model) are relevant for string theory.


## Related concepts

* [[BPS state]], [[D-module]], [[cluster algebra]], [[quiver]], [[representation theory]], [[Donaldson-Thomas invariant]].

[[!include field theory with boundaries and defects - table]]


## References


### Introductions and lectures

* Sergio Cecotti, _Trieste lectures on wall-crossing invariants_ (2010) ([pdf](http://people.sissa.it/~cecotti/ictptext.pdf))

* [[Greg Moore]], _PiTP Lectures on BPS states and wall-crossing in $d = 4$, $\mathcal{N} = 2$ theories_ ([pdf](http://www.physics.rutgers.edu/~gmoore/PiTP_July26_2010.pdf))

* {#Dimofte10} [[Tudor Dimofte]], _Refined wall crossing_ ([pdf](http://thesis.library.caltech.edu/5808/4/TD_part1.pdf)), part I of _Refined BPS invariants, Chern-Simons theory, and the quantum dilogarithm_, 2010 ([pdf](http://thesis.library.caltech.edu/5808/1/DimofteTDofficial.pdf), [web](http://thesis.library.caltech.edu/5808/))


### Original articles

#### General

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](http://arxiv.org/abs/0811.2435); _Motivic Donaldson-Thomas invariants: summary of results_, [0910.4315](http://arxiv.org/abs/0910.4315); _Wall-crossing structures in Donaldson-Thomas invariants, integrable systems and Mirror Symmetry_, [arxiv/1303.3253](http://arxiv.org/abs/1303.3253)

* Arend Bayer, [[Yuri Manin|Yuri I. Manin]], _Stability conditions, wall-crossing and weighted Gromov-Witten invariants_, [math.AG/0607580](http://arxiv.org/abs/math.AG/0607580), Mosc. Math. J. __9__ (1), 2009.

* Mina Aganagic, Hirosi Ooguri, Cumrun Vafa, Masahito Yamazaki, _Wall crossing and M-theory_, [arxiv/0908.1194](http://arxiv.org/abs/0908.1194)

* M. Aganagic, _Wall crossing, quivers and crystals_, [arxiv/1006.2113](http://arxiv.org/abs/1006.2113)

* S. Cecotti, [[Cumrun Vafa]], _BPS wall crossing and topological strings_, 
[arXiv/0910.2615](http://arxiv.org/abs/0910.2615)

* [[Davide Gaiotto]], [[Greg Moore]], [[Andrew Neitzke]], _Wall-crossing, Hitchin systems, and the WKB approximation, ([arxiv/0907.3987](http://arxiv.org/abs/0907.3987))

* E. Diaconescu, [[Greg Moore]], _Crossing the wall: branes vs. bundles_, [arXiv/0706.3193](http://arxiv.org/abs/0706.3193)

* E. Andriyash, [[Frederik Denef]], [[Daniel Jafferis]], [[Greg Moore|G. W. Moore]], _Wall-crossing from supersymmetric galaxies_, [arxiv/1008.0030](http://arxiv.org/abs/1008.0030)

* Tom Bridgeland, [[Valerio Toledano-Laredo]], _Stability conditions and Stokes factors_, [arxiv/0801.3974](http://arxiv.org/abs/0801.3974)

* M. C. N. Cheng, E. P. Verlinde, _Wall crossing, discrete attractor flow and Borcherds algebra_, SIGMA 4 (2008), 068, 33 pages, [pdf](http://www.emis.de/journals/SIGMA/2008/068/sigma08-068.pdf)

* Masahito Yamazaki, _Crystal melting and wall crossing phenomena_, Ph.D. thesis, [arxiv/1002.1709](http://arxiv.org/abs/1002.1709)

* Michele Cirafici, Annamaria Sinkovics, [[Richard Szabo]], _Instanton counting and wall-crossing for orbifold quivers_, [arxiv/1108.3922](http://arxiv.org/abs/1108.3922)

* H.-Y. Chen, N. Dorey, K. Petunin, _Moduli space and wall-crossing formulae in higher-rank gauge theories_, JHEP 11 (2011) 020, <a href="http://dx.doi.org/10.1007/JHEP11(2011)020">doi</a>; _Wall crossing and instantons in compactified gauge theory_, JHEP 06 (2010) 024 [arXiv:1004.0703](ttp://arxiv.org/abs/1004.0703)

### In supergravity

* {#Denef00} [[Frederik Denef]], _Supergravity flows and D-brane stability_, JHEP 0008:050,2000 ([arXiv:hep-th/0005049](http://arxiv.org/abs/hep-th/0005049))

* [[Frederik Denef]], _Quantum Quivers and Hall/Hole Halos_, JHEP 0210:023,2002 ([arXiv:hep-th/0206072](http://arxiv.org/abs/hep-th/0206072))

* [[Daniel Jafferis]], [[Gregory Moore]], _Wall crossing in local Calabi Yau manifolds_ ([arXiv:0810.4909](http://arxiv.org/abs/0810.4909))

### Conferences and seminars

* (past) [[Kontsevich]] in Aarhus, August 2010, [master class on wall crossing](http://qgm.au.dk/events/show/artikel/masterclass-aug-2010/); we will keep a [[wall crossing in Aarhus|nlab page]] on it

* (past) [Focus Week on New Invariants and Wall Crossing](http://member.ipmu.jp/domenico.orlando/FocusInvariants.html), May 18-22, 2009, Kashiwa Campus of the University of Tokyo

* (past) [Wall-crossing in Mathematics and Physics](http://www.math.uiuc.edu/wallcrossing), May 24-28, 2010,
Department of Mathematics, University of Illinois at Urbana-Champaign

* Description of seminar on stability conditions and Stokes factors in Bonn, [pdf](http://www.math.uni-bonn.de/people/compgeo/Hall.pdf)

Also ([Gaiotto-Moore-Witten 15](#GaiottoMooreWitten15)).

### Categorification

A [[categorification]] of wall crossing formulas to an [[(infinity,2)-category]] of sorts is discussed in 

* {#GaiottoMooreWitten15} [[Davide Gaiotto]], [[Gregory Moore]], [[Edward Witten]], _An Introduction To The Web-Based Formalism_ ([arXiv.1506.04086](http://arxiv.org/abs/1506.04086))


[[!redirects wall crossing]]
[[!redirects wall-crossing]]