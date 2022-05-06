
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
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

This page reviews some of the relation between the existence of [[supersymmetry|supersymmetries]] in a [[spacetime]] [[quantum field theory]] which arises as the [[effective quantum field theory]] of some [[string]] [[2d SCFT]], the special geometry of that spacetime (such as [[Calabi-Yau manifold]] structure) as well as increased [[worldsheet]] supersymmetry of the [[superstring]].

### Target space perspective

A solution to the bosonic [[Einstein equations]] of ordinary [[gravity]] -- some [[Riemannian manifold]] -- has a _global symmetry_ if it has a [[Killing vector]].

Accordingly, a configuration that solves the [[supergravity]] [[Euler-Lagrange equations]] is a _[[global supersymmetry]]_ if it has a [[Killing spinor]]: a [[covariantly constant spinor]].

(Here the notion of [[covariant derivative]] includes the usual [[Levi-Civita connection]], but also in general [[torsion]] components and contributions from other [[background gauge fields]] such as a [[Kalb-Ramond field]] and the [[RR-field]]s in [[type II string theory|type II supergravity]] or [[heterotic string theory|heterotic supergravity]].)

Of particular interest to phenomenologists around the turn of the millennium (but maybe less so today with new experimental evidence) has been in [[KK-compactification]] solutions of [[spacetime]] manifolds of the form $M^4 \times Y^6$ for $M^4$ the locally observed [[Minkowski spacetime]] (that plays a role as the background for all available particle accelerator experiments) and a small [[closed manifold|closed]] 6-dimensional [[Riemannian manifold]] $Y^6$. 

In the absence of further fields besides gravity, the condition that such a configuration has precisely one [[Killing spinor]] and hence precisely one [[global supersymmetry]] turns out to be precisely that $Y^6$ is a [[Calabi-Yau manifold]]. One such remaining global supersymmetry in the low energy [[effective field theory]] in 4-dimensions is or was believed to be of relevance in [[phenomenology]], see for instance the supersymmetric _[[MSSM]]_ extension of the [[standard model of particle physics]]. This is where all the interest into these Calabi-Yau manifolds in [[string theory]] comes from. (Notice though that nothing in the theory itself demands such a compactification. It is only the phenomenological assumption of the factorized spacetime compactification together with $N = 1$ supersymmetry that does so).

More generally, in the presence of other [[background gauge fields]], the Calabi-Yau condition here is deformed. One also speaks of [[generalized Calabi-Yau space]]s. (For instance ([GMPT05](#GMPT))).

Alternatively, if one starts the [[KK-compactification]] not from 10-dimensional [[string theory]] but from [[11-dimensional supergravity]]/[[M-theory]], then the condition for the [[KK-compactification]] to preserved precisely one global supersymmetry is that it be on a [[G2-manifold]]. For more on this see at _[[M-theory on G2-manifolds]]_.

### Worldvolume perspective
 {#WorldvolumePerspective}

On the other hand, the enhanced _global_ [[supersymmetry]] of [[target space]] is also reflected in enhanced _local_ supersymmetry on the [[worldsheet]] of the string. For instance for the [[heterotic string]] whose worldsheet [[2d SCFT]] apriori has $N=(1,0)$ supersymmetry, the target space theory has $N=1$ supersymmetry precisely if the worldsheet theory's supersymmetry enhanced to $N=(2,0)$. ([BDFF 88](#BDFF88)). For more on this see at _[[2d (2,0)-superconformal QFT]]_.

Similar comments apply to [[type II superstring theory]], where $N=1$ target space supersymmetry enhanced the worldsheet symmetry from $N=(1,1)$ to $N=(2,2)$. This is reflected notably in the [[mirror symmetry]] of the target Calabi-Yau manifolds.

### Non-perturbative description

The above analysis in [[perturbative string theory]] is expected to find a non-perturbative lift to [[M-theory]]/[[F-theory]]. Under this lift, compactification on a Calabi-Yau complex-3-fold (CY3) lifts to compactification on a [[G2-manifold]]/CY4-fold, respectively:

[[!include N=1 susy compactifications -- table]]

## Related concepts

* [[supergravity]], [[supersymmetry]]

* [[Kaluza-Klein mechanism]]

* [[spontaneously broken symmetry]]

* [[hierarchy problem]]

* [string theory FAQ -- What does it mean to say that string theory has a "landscape" of solutions?](string%20theory%20FAQ#WhatDoesItMeanToSayStringTheoryHasALandscapeOfSolutions)

* [[M-theory on Calabi-Yau manifolds]]

* [[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]

## References
 {#References}

The idea, in the context of [[heterotic string theory on CY3-manifolds]], originates in 

* {#CandelasHorowitzStromingerWitten85} [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], and [[Edward Witten]], _Vacuum Configurations for Superstrings_ , Nucl. Phys. B 258 (1985), p. 46. 

where in the introduction it says the following

> Recently, the discovery [6] of anomaly cancellation in a modified version of $d = 10$ supergravity and superstring theory with gauge group $O(32)$ or $E_8 \times E_8$ has opened the possibility that these theories might be phenomenologically realistic as well as mathematically consistent. A new string theory with  $E_8 \times E_8$ gauge group has recently been constructed [7] along with a second $O(32)$ theory.

> For these theories to be realistic, it is necessary that the vacuum state be of the form $M_4 \times K$, where $M_4$ is four-dimensional Minkowski space and K is some compact six-dimensional manifold. (Indeed, Kaluza-Klein theory -- with its now widely accepted interpretation that all dimensions are on the same logical footing -- was first proposed [8] in an effort to make sense out of higher-dimensional string theories). Quantum numbers of quarks and leptons are then determined by topological invariants of $K$ and of an $O(32)$ or $E_8 \times E_8$ gauge field defined on $K$ [9]. Such considerations, however, are far from uniquely determining $K$.

> In this paper, we will discuss some considerations, which, if valid, come very close to determining $K$ uniquely. We require

> (i) The geometry to be of the form $H_4 \times K$, where $H_4$ is a maximally symmetric spacetime.

> (ii) There should be an unbroken $N = 1$ supersymmetry in four dimensions. General arguments [10] and explicit demonstrations [11] have shown that supersymmetry may play an essential role in resolving the gauge hierarchy or Dirac large numbers problem. These arguments require that supersymmetry is unbroken at the Planck (or compactification) scale.

> (iii) The gauge group and fermion spectrum should be realistic. 

> These requirements turn out to be extremely restrictive. In previous ten-dimensional supergravity theories, supersymmetric configurations have never given rise to chiral fermions -- let alone to a realistic spectrum. However, the modification introduced by Green and Schwarz to produce an anomaly-free field theory also makes it possible to satisfy these requirements. We will see that unbroken $N = 1$ supersymmetry requires that $K$ have, for perturbatively accessible configurations, $SU(3)$ holonomy and that the four-dimensional cosmological constant vanish. The existence of spaces with $SU(3)$ holonomy was conjectured by Calabi [12] and proved by Yau [13].

(Of course later it was understood that Calabi-Yau spaces, even those of complex dimension 3, are not "very close to unique".)

Lecture notes include

* {#Greene97} [[Brian Greene]], _String Theory on Calabi-Yau Manifolds_, lectures at TASI96 ([arXiv:hep-th/9702155](https://arxiv.org/abs/hep-th/9702155))

Further original references include

* {#BDFF88} [[Tom Banks]], [[Lance Dixon]], [[Dan Friedan]], [[Emil Martinec]], _Phenomenology and Conformal Field Theory or Can String Theory Predict the Weak Mixing Angle?_, Nucl. Phys. B299 (1988) 613.  ([pdf](http://www.slac.stanford.edu/cgi-wrap/getdoc/slac-pub-4377.pdf))

* [[Jacques Distler]], [[Brian Greene]], _Aspects Of $(2,0)$ String Compactifications_, Nucl. Phys. B304 (1988) 

* [[Andrew Strominger]], _Special Geometry_, Comm. Math. Phys. 133 (1990) 163.

* [[Philip Candelas]] and X. De la Ossa, _Moduli Space of Calabi-Yau Manifolds_, Nucl. Phys. B355 (1991) 455.

* [[Edward Witten]], _Phases of N=2 Theories in Two Dimensions_, Nucl. Phys. B403 (1993) 159 ([arXiv:hep-th/9301042](http://arxiv.org/abs/hep-th/9301042))

and chapters 12 - 16 of

* [[Michael Green]], [[John Schwarz]], [[Edward Witten]], _Superstring Theory_ , Vol. 2, Cambridge University Press, (1987) 

A canonical textbook reference for the role of Calabi-Yau manifolds in compactifications of 10-dimensional [[supergravity]] is 

* [[Andrew Strominger]] (notes by [[John Morgan]]), _Kaluza-Klein compactifications, Supersymmetry and Calabi-Yau spaces_ , volume II, starting on page 1091 in

* [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]],  [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  , _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

Lecure notes in a more general context of [[string phenomenology]] include

* {#Wijhnholt14} [[Martin Wijnholt]], _String compactification_, [PITP 2014](https://pitp2014.ias.edu) lecture notes ([[WijnholtCompactification14.pdf:file]], [slides for lecture 1](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P1_wijnholt.pdf), [slides for lecture 2](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P2_wijnholt.pdf), [slides for lecture 3](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P3_wijnholt.pdf))

Discussion of generalized Calabi-Yau backgrounds is for instance in 

* {#GMPT} [[Mariana Graña]], Ruben Minasian, Michela Petrini, Alessandro Tomasiello, _Generalized structures of $N=1$ vacua_ ([arXiv:hep-th/0505212](http://arxiv.org/abs/hep-th/0505212))
  
Mathematical background:

* [[Tristan Hübsch]], _Calabi-Yau Manifolds -- A Bestiary for Physicists_, World Scientific 1992 ([doi:10.1142/1410](https://doi.org/10.1142/1410))





[[!redirects supergravity and Calabi-Yau manifolds]]

[[!redirects Calabi-Yau manifolds and supersymmetry]]
[[!redirects Calabi-Yau manifolds and supersymmetry]]