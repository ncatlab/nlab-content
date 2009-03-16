##Big picture##

Monads in any 2-category $C$ make themselves a 2-category $\mathrm{Mnd}$ in which 1-cells are either lax or colax morphisms of monads;
by dualization the same is true for comonads. Monads internal to the 2-category of monads are called distributive laws. In particular, distributive laws themselves make a 2-category. There are other variants like distributive laws between a monad and an endofunctor, mixed distributive laws between a monad and a comonad (the variants for algebras and coalgebras called entwining strcutures), distributive laws between actions of two different monoidal categories on the same category, for PROPS and so on. Having a distributive law $l$ from one monad to another enables to define the composed monad $\mathbf T\circ_l\mathbf P$. This corerspondence extends to a 2-functor $\mathrm{comp}:\mathrm{Mnd}(\mathrm{Mnd}(C))\to\mathrm{Mnd}(C)$. The analogue in mixed setup is a homomorphism of bicategories from the bicategory of entwinings to a bicategory of corings.

##Explicit definition##

A _distributive law_ from a monad  ${\mathbf T} = (T, \mu^T, \eta^T)$ in $A$ to an endofunctor
$P$ is a 2-cell $l : TP \Rightarrow PT$ such that
$l \circ (\eta^T)_P = P(\eta^T)$ and
$l \circ (\mu^T)_P = P(\mu^T) \circ l_T \circ T(l)$.
Such distributive laws are in bijection with lifts of $P$ 
to a unique endofunctor $P^{\mathbf T}$ in the Eilenberg-Moore category $A^{\mathbf T}$,
in the sense that $U^{\mathbf T} P^{\mathbf T} = P U^{\mathbf T}$.
Indeed, the endofunctor $P^{\mathbf T}$
is given by $(M,\nu) \mapsto (PM,P(\nu)\circ l_M)$.

A _distributive law_ from a monad  ${\mathbf T} = (T, \mu^T, \eta^T)$ to a monad
${\mathbf P} = (P, \mu^P, \eta^P)$ in $A$ 
(or of $\mathbf T$ over $\mathbf P$)
is a distributive law from $\mathbf T$ to the endofunctor $P$,
compatible with $\mu^P,\eta^P$ in the sense that
$l \circ T(\eta^P) = (\eta^P)_T$ and
$l \circ T(\mu^P) = (\mu^P)_T \circ P(l) \circ l_P$. Thus all together a distributive law from a monad to an endofunctor is a 2-cell for which 2 triangles and 2 pentagons commute. In the entwining case, 
Brzezi&#324;ski and Majid combined the 4 diagrams into one picture which they call the bow-tie diagram. 

##Literature##
H. Appelgate, M. Barr, J. Beck, F. W. Lawvere, F. E. J. Linton, E, Manes, M. Tierney, F. Ulmer, Seminar on triples and categorical homology theory, ETH 1966/67, edited by B. Eckmann, LNM 80, Springer 1969.
(includes article Jon Beck, Distributive laws, pages 119--140).

G. B&#246;hm, Internal bialgebroids, entwining structures
and corings, AMS Contemp. Math. 376 (2005) 207-226; 
<a href="http://front.math.ucdavis.edu/math.QA/0311244">arXiv:math.QA/0311244</a>

T. Brzezi&#324;ski, S. Majid, Coalgebra bundles, Comm. Math. Phys.  191  (1998),  no. 2, 467--492.

T. Brzezi&#324;ski, R. Wisbauer, Corings and comodules, London Math. Soc. Lec. Note Series 309, Cambridge 2003.

T. F. Fox, M. Markl, Distributive laws, bialgebras, and cohomology.  Operads: Proceedings of Renaissance Conferences (Hartford, CT/Luminy, 1995),  167-205, 
Contemp. Math. 202, AMS 1997. 

S. Lack, Composing PROPS, Theory Appl. Categ. 13 (2004), No. 9, 147-163.

S. Lack, R. Street, The formal theory of monads II, Special volume celebrating the 70th birthday of Professor Max Kelly.
J. Pure Appl. Algebra 175 (2002), no. 1-3, 243-265. 

M. Markl, Distributive laws and Koszulness.  Ann. Inst. Fourier (Grenoble)  46  (1996),  no. 2, 307--323.

R. Street, The formal theory of monads, J. Pure Appl. Alg. 2, 149-168 (1972)

Z. &#352;koda, Distributive laws for monoidal categories (<a href="http://front.math.ucdavis.edu/math.CT/0406310">arXiv:0406310</a>); Equivariant monads and equivariant lifts versus a 2-category of distributive laws(<a href="http://front.math.ucdavis.edu/math.CT/0406310">arXiv:0707.1609</a>); Bicategory of entwinings  (<a href="http://arxiv.org/abs/0805.4611">arXiv:0805.4611</a>)

Z. &#352;koda, Some equivariant constructions in noncommutative geometry, Georg. Math. J. (to appear) 
(<a href="http://front.math.ucdavis.edu/0811.4770"> arXiv:0811.4770</a>)

R. Wisbauer, Algebras versus coalgebras.  Appl. Categ. Structures  16  (2008),  no. 1-2, 255--295.