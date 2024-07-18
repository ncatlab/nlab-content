__Runge-Kutta approximation schemes__ are a family of difference schemes used for iterative numerical solution of [[ordinary differential equation]]s. 

### Standard Runge-Kutta methods

In engineering it is rather standard to use the 4th order Runge-Kutta difference schemes. General overview is at 

* wikipedia [Runge-Kutta methods](http://en.wikipedia.org/wiki/Runge%E2%80%93Kutta_methods)

* H. Munthe-Kaas, _High order Runge–Kutta methods on manifolds_, Appl. Num. Math., 29, 115-127 (1999)


### For stochastic ODE-s:

* wikipedia [Runge&#8211;Kutta method (SDE)](http://en.wikipedia.org/wiki/Runge%E2%80%93Kutta_method_%28SDE%29)

### Relation to algebraic problems, Lie theory and renormalization

* J.C. Butcher, _Coefficients for the study of Runge-Kutta integration processes_, J. Austral. Math. Soc. __3__ (1963) 185--201

In the 1972 Butcher's work, Runge-Kutta methods are organized into a group, later called [[Butcher group]]:

* J. C. Butcher, An algebraic theory of integration methods, Math. Comp. __26__ (1972) 79--106.

Brouder has shown a relation of Butcher group to Connes-Kreimer Hopf algebra.

* Ch. Brouder, _Runge-Kutta methods and renormalization_,
Europ. Phys. J. C12 (2000) 512--534.

The Butcher-Connes-Kreimer Hopf algebra is a Hopf subalgebra or Foissy Hopf algebra from work

* L. Foissy, _Les algèbres de Hopf des arbres enracinés décorés, I._, Bulletin des Sciences Mathematiques 126, no. 3 (2002): 193--239 (arXiv:math/0105212). MR1905177 _Les algèbres de Hopf des arbres enracinés décorés. II._ Bulletin des Sciences Mathematiques 126, no. 4 (2002): 249--288 (arXiv:math/0105212) MR1909461 

* Hans Z. Munthe-Kaas, Ari Stern, Olivier Verdier, _Invariant connections, Lie algebra actions, and foundations of numerical integration on manifolds_, SIAM Journal on Applied Algebra and Geometry __4__ (1) 49--68 (2020) [doi](https://doi.org/10.1137/19M1252879)
[arXiv:1903.10056](https://arxiv.org/abs/1903.10056)

> Motivated by numerical integration on manifolds, we relate the algebraic properties of invariant connections to their geometric properties. Using this perspective,
we generalize some classical results of Cartan and Nomizu to invariant connections on algebroids. This has fundamental consequences for the theory of numerical integrators, giving a characterization of the spaces on which Butcher and Lie–Butcher series methods,
which generalize Runge–Kutta methods, may be applied.

Important family of Lie-algebraic methods for generating integrators are introduced in

* P. E. Crouch, R. Grossman, _Numerical integration of ordinary differential equations on manifolds_, J. Nonlinear Sci. __3__: 1--33 (1993) [doi](https://doi.org/10.1007/BF02429858)

### Connections to symplectic geometry

See also [[symplectic integrator]]s.

* [[Alberto S. Cattaneo]], Benoit Dherin, [[Giovanni Felder]], _Formal symplectic groupoid_, Comm. Math. Phys. __253__ (2005), no. 3, 645&#8211;674 [math.SG/0312380](http://arxiv.org/abs/math/0312380) [doi](HTTP://dx.doi.org/10.1007/s00220-004-1199-z)

> The multiplicative structure of the trivial symplectic groupoid over $\mathbb{R}^d$ associated to the zero Poisson structure can be expressed in terms of a generating function. We address the problem of deforming such a generating function in the direction of a non-trivial Poisson structure so that the multiplication remains associative. We prove that such a deformation is unique under some reasonable conditions and we give the explicit formula for it. This formula turns out to be the semi-classical approximation of Kontsevich's deformation formula. For the case of a linear Poisson structure, the deformed generating function reduces exactly to the CBH formula of the associated Lie algebra. The methods used to prove existence are interesting in their own right as they come from an at first sight unrelated domain of mathematics: the Runge--Kutta theory of the numeric integration of ODE's. 

* Robert McLachlan, Klas Modin, Olivier Verdier, _Collective Lie--Poisson integrators on $\mathbb{R}^{3}$_, [arxiv/1307.2387](http://arxiv.org/abs/1307.2387)

> We develop Lie--Poisson integrators for general Hamiltonian systems on $\mathbb{R}^{3}$ equipped with the rigid body bracket. The method uses symplectic realisation of $\mathbb{R}^{3}$ on $T^{*}\mathbb{R}^{2}$ and application of __symplectic Runge--Kutta schemes__. As a side product, we obtain simple [[symplectic integrator]]s for general Hamiltonian systems on the sphere $S^{2}$.

* J. M. Sanz-Serra, Runge-Kutta Schemes for Hamiltonian Systems, Bit __28__, pp. 877-883, (1988).

[[!redirects Runge-Kutta approximation scheme]]
[[!redirects Runge-Kutta methods]]
