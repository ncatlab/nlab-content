
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _symplectic integrator_ is a numerical discretization scheme for solving [[Hamilton's equations]] which takes into account the [[symplectic structure]] and, in particular, the [[conservation laws]], at the discretization level, thus resulting in better long-time behaviour of numerical solutions than that of generic discretization schemes. There are analogues for [[classical field theory]], which take into account the resulting [[multisymplectic geometry|multisymplectic structure]]. 

## References

* wikipedia [symplectic integrator](http://en.wikipedia.org/wiki/Symplectic_integrator), [multisymplectic integrator](http://en.wikipedia.org/wiki/Multisymplectic_integrator)

* Denis Donnelly, Edwin Rogers, _Symplectic integrators: An introduction_,  Am. J. Phys. __73__, 938 (2005) [doi](http://dx.doi.org/10.1119/1.2034523)
* [symplectic numerical integration](http://www.maths.cam.ac.uk/undergrad/course/na/ib/symplectic_integrators/symplectic_integrators.php) at DAMTP
* Daniel W. Markiewicz, _Survey on symplectic integrators_, 
[pdf](http://math.berkeley.edu/~alanw/242papers99/markiewicz.pdf)   
* Robert McLachlan, Klas Modin, Olivier Verdier, _Collective Lie--Poisson integrators on $\mathbb{R}^{3}$_, [arxiv/1307.2387](http://arxiv.org/abs/1307.2387)
* A. Lew, J. E. Marsden, M. Ortiz, M. West, _An overview of variational integrators_, In L. P. Franca (ed.), Finite Element Methods: 70's and Beyond. Barcelona (2003).
* Jerrold E. Marsden, George W. Patrick, Steve Shkoller, _Multisymplectic geometry, variational integrators, and nonlinear PDEs_, Commun. Math. Physics __199__:2 (1998) 351-395 [math.DG/9807080](http://arxiv.org/abs/math/9807080), [doi](http://dx.doi.org/10.1007/s002200050505)
* Fran&#231;ois Demoures, Fran&#231;ois Gay-Balmaz, Tudor S. Ratiu, _Multisymplectic variational integrators and space/time symplecticity_, [arxiv/1310.4772](http://arxiv.org/abs/1310.4772)
* Ernst Hairer, _Backward analysis of numerical integrators and symplectic methods_, [ps](www.unige.ch/~hairer/preprints/symplect.ps)
* Sebastian Reich, _Backward error analysis for numerical integrators_, SIAM J. Numer. Anal. 36, 1549--1570, 1996 [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.28.6972)
* Y. B. Suris, _Hamiltonian Runge-Kutta type methods and their variational formulation_ (1990)

The idea can be adapted to dissipative systems as well:

* Guilherme França, Michael I. Jordan, René Vidal, _On dissipative symplectic integration with applications to gradient-based optimization_, [arxiv/2004.06840](https://arxiv.org/abs/2004.06840)

category: applications
[[!redirects multisymplectic integrator]]