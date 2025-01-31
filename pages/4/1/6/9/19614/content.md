
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

If one allows [[pseudo-Riemannian manifolds]] with [[conical singularities]] then it makes sense to ask for [[spacetimes]] which are flat ([[isometry|isometric]] to pieces of [[Minkowski spacetime]]) away from [[stratified space|strata]] of [[positive number|positive]] [[codimension]], with all [[curvature]] concentrated in [[conical singularities]] on these lower-dimensional strata.

<center>
<img src="https://ncatlab.org/nlab/files/ConicalSingularity.jpg" width="300">
</center>

Such piecewise flat spacetimes have been considered as discretized models for smooth (non-singular and non-piecewise flat) [[spacetimes]] useful for [[computation]] (see [Williams & Tuckey 1992](#WilliamsTuckey92)): A [[combinatorics|combinatorial]] [[functional]] on piecewise flat spacetimes, depending on the [[edge]] [[lengths]] of a metric [[simplicial complex]], was introduced by [Regge 1961](#Regge61) (see also [Barrett 1987](#Barrett87)) with the idea that in an appropriate [[limit of a sequence|limit]] it approaches the [[Einstein-Hilbert action]] [[functional]] on non-singular [[spacetimes]]. This has become famous as _Regge calculus_. That this [[limit of a sequence|limit]] indeed works out has been proven (only) in [Cheeger, Mueller &Schrader 1984](#CheegerMuellerSchrader84), see [Cheeger 2016](#Cheeger16) for review.

A variant of this perspective, but with the [[conical singularities]] constrained to be [[timelike]] as expected for "physical" singularities, has been initiated in
['t Hooft 2008](#tHooft08) and worked out in some detail by [van de Meent 2011](#vandeMeent11).

In both cases a more speculative motivation for considering piecewise flat spacetimes is the hope that it might help with defining [[quantum gravity]], [[non-perturbative QFT|non-perturbatively]] ([Regge & Williams 2000](#ReggeWilliams00)). A direct attempt to define and compute a [[path integral quantization]] over piecewise flat spacetimes is known as "causal dynamical triangulation" (see [Ambjorn, Jurkiewicz &Loll 20000](#AmbjornJurkiewiczLoll00)).

Piecewise flat spacetimes appear naturally in [[3d quantum gravity|3-dimensional gravity]], which provides much of the inspiration and motivation of various approaches.

But piecewise flat spacetimes also appear naturally as the "[[far-horizon geometry]]" ("[[large 1/N limit|small $N$-limit]]", see there) of [[BPS state|BPS]] [[black brane]] spacetimes in [[supergravity]] theories, where considerations such as discussed at _[[M-theory on G₂-manifolds]]_ suggest that the [[conical singularities]] have to be taken seriously as part of the physical model. These [[cone brane]]-singularities are necessarily time-like, as in ['t Hooft 2008](#tHooft08), [van de Meent 2011](#vandeMeent11), but in contrast to the assumption in general Regge calculus and generally of higher (co)dimension.

## References

### Regge calculus

* {#Regge61} [[Tullio Regge]], _General relativity without coordinates_,  Nuovo Cim (1961) 19: 558 ([doi:10.1007/BF02733251](https://doi.org/10.1007/BF02733251))

* [[Charles Misner]], [[Kip Thorne]], [[John Wheeler]], §42 in: _[[Gravitation]]_, W. H. Freeman (1973) &lbrack;[inspire:95654](https://inspirehep.net/literature/95654)&rbrack;


* {#CheegerMuellerSchrader84} [[Jeff Cheeger]], Werner Müller, Robert Schrader, _On the curvature of piecewise flat spaces_, Comm. Math. Phys. Volume 92, Number 3 (1984), 405-454 ([euclid:1103940867](https://projecteuclid.org/euclid.cmp/1103940867))

* {#Barrett87} [[John Barrett]], _The geometry of classical Regge calculus_, Classical and Quantum Gravity, Volume 4, Number 6, 1987 ([doi:10.1088/0264-9381/4/6/015/meta](http://iopscience.iop.org/article/10.1088/0264-9381/4/6/015/meta))

* {#WilliamsTuckey92} R. M. Williams, P. A. Tuckey, _Regge calculus: a brief review and bibliography_, Classical and Quantum Gravity, Volume 9, Number 5, 1992 ([web](http://iopscience.iop.org/article/10.1088/0264-9381/9/5/021/meta))

* {#ReggeWilliams00} [[Tullio Regge]], Ruth M. Williams, _Discrete structures in gravity_, J. Math. Phys.41:3964-3984, 2000 ([arXiv:gr-qc/0012035](https://arxiv.org/abs/gr-qc/0012035))

* {#Cheeger16} [[Jeff Cheeger]], _Curvature of piecewise flat spaces_, talk at Courant institute 2016 ([pdf](https://www.ethz.ch/content/dam/ethz/special-interest/phys/theoretical-physics/itp-dam/documents/graf/schrader/Cheeger.pdf), [[Cheeger2016.pdf:file]])

* [[Aleksandar Miković]], _Piecewise Flat Metrics and Quantum Gravity_ ([arXiv:2001.11439](https://arxiv.org/abs/2001.11439))

* [[Aleksandar Miković]]: *Finiteness of piecewise flat quantum gravity with matter* &lbrack;[arXiv:2412.17465](https://arxiv.org/abs/2412.17465)&rbrack;


See also

* Wikipedia, _[Regge calculus](https://en.wikipedia.org/wiki/Regge_calculus)_

Application to [[FRW models]] of [[cosmology]]:

* Ren Tsuda, Takanori Fujiwara, _Oscillating 4-Polytopal Universe in Regge Calculus_ ([arXiv:2011.04120](https://arxiv.org/abs/2011.04120))


### 't Hooft-van de Meent

* {#tHooft08} [[Gerard 't Hooft]], _A locally finite model for gravity_, Found. Phys. 38:733-757, 2008 ([arXiv:0804.0328](https://arxiv.org/abs/0804.0328))

* [[Maarten van de Meent]], _Piecewise Flat Gravitational Waves_,  	Class. Quant. Grav.28:075005, 2011 ([arXiv:1012.1991](https://arxiv.org/abs/1012.1991))

* [[Maarten van de Meent]], _Exact Piecewise Flat Gravitational Waves_, Class. Quantum Grav. 28 (2011) 245006 ([arXiv:1106.5380](https://arxiv.org/abs/1106.5380))

* {#vandeMeent11} [[Maarten van de Meent]], _Piecewise Flat Gravity in 3+1 dimensions_ ([arXiv:1111.6468](https://arxiv.org/abs/1111.6468))

### Causal dynamical triangulation

* J. Ambjorn, R. Loll, _Non-perturbative Lorentzian Quantum Gravity, Causality and Topology Change_, Nucl.Phys. B536 (1998) 407-434 ([arXiv:hep-th/9805108](https://arxiv.org/abs/hep-th/9805108))

* J. Ambjorn, J. Jurkiewicz, R. Loll, _Dynamically Triangulating Lorentzian Quantum Gravity_, Nucl.Phys. B610 (2001) 347-382 ([arXiv:hep-th/0105267](https://arxiv.org/abs/hep-th/0105267))

* {#AmbjornJurkiewiczLoll00} J. Ambjorn, J. Jurkiewicz, R. Loll, _A non-perturbative Lorentzian path integral for gravity_, Phys.Rev.Lett. 85 (2000) 924-927 ([arXiv:hep-th/0002050](https://arxiv.org/abs/hep-th/0002050))

* R. Loll, _Quantum Gravity from Causal Dynamical Triangulations: A Review_ ([arXiv:1905.08669](https://arxiv.org/abs/1905.08669))

* Jan Ambjorn, *Lattice Quantum Gravity: EDT and CDT* &lbrack;[arXiv:2209.06555](https://arxiv.org/abs/2209.06555)&rbrack;

Review:

* Dario Benedetti, *Landau Theory of Causal Dynamical Triangulations*, in: *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2212.11043](https://arxiv.org/abs/2212.11043)&rbrack;

* J. Ambjørn, R. Loll, *Causal Dynamical Triangulations: Gateway to Nonperturbative Quantum Gravity*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2401.09399](https://arxiv.org/abs/2401.09399)&rbrack;

* Renate Loll: *Nonperturbative quantum gravity unlocked through computation*, in: *Quantum Gravity and Computation*, Routledge  (2025) &lbrack;[arXiv:2501.17972](https://arxiv.org/abs/2501.17972)&rbrack;

Relation to [[dark energy]]:

* Mingwei Dai, Walter Freeman, Jack Laiho, Marc Schiffer, Judah Unmuth-Yockey: *Dynamical Dark Energy from Lattice Quantum Gravity* &lbrack;[arXiv:2408.08963](https://arxiv.org/abs/2408.08963)&rbrack;










[[!redirects piecewise flat spacetimes]]

[[!redirects Regge calculus]]

[[!redirects causal dynamical triangulation]]
[[!redirects causal dynamical triangulations]]
