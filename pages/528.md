[[!redirects antipode]]
[[!redirects Hopf monoid]]
[[!redirects Hopf monoids]]
[[!redirects Hopf algebras]]

#Idea#

A Hopf algebra is a generalization of:

* the [[group algebra]] of a [[group]]

* the algebra of functions on a finite group, and more generally, the algebra of regular function on an affine algebraic $k$-group

* the [[universal enveloping algebra]] of a [[Lie algebra]]

All these algebras are actually [[bialgebra|bialgebras]], but furthermore they have a 'antipode' operation which reflects or mimics the inverse operation of a group.


#Definition#

A $k$-[[bialgebra]] $(A,m,\eta,\Delta,\epsilon)$ with multiplication $m$, comultiplication $\Delta$, unit $\eta: k\to A$ and counit $\epsilon:A\to k$ is a **Hopf algebra**
if there exists a $k$-linear map

$$S : A \to A$$

called the **antipode** (or coinverse) such that $m\circ(\mathrm{id}\otimes S)\circ \Delta = m\circ(S\otimes\mathrm{id})\circ\Delta = \eta\circ\epsilon$ (as a map $A\to A$). If an antipode exists then it is unique, just the way that if inverses exist in a monoid they are unique.

The axiom that must be satisfied by the antipode looks like a $k$-linear version of the identity satisfied by the inverse map in a group bimonoid: taking a group element $g$, duplicating by the diagonal map $\Delta$ to obtain $(g,g)$, taking the inverse of either component of this ordered pair, and then multiplying the two components, we obtain the identity element of our group.

Just as an [[algebra]] is a [[monoid]] in [[Vect]] and a [[bialgebra]] is a [[bimonoid]] in $Vect$, a Hopf algebra is a [[Hopf monoid]] in $Vect$.


#Hopf algebras versus groups#

Note that the definition of Hopf algebra (or, really, of [[Hopf monoid]]) is [[duality|self-dual]]: a Hopf monoid in a symmetric monoidal category $V$ is the same as a Hopf monoid in $V^{op}$ (i.e. a "Hopf comonoid").  Thus we can view a Hopf algebra as "like a group" in two different ways, depending on whether the group multiplication corresponds to the multiplication or the comultiplication of the Hopf algebra.  The formal connections between Hopf monoids and group objects are:

1. A Hopf monoid in a [[cartesian monoidal category]] $V$ is the same as a group object in $V$.  Such Hopf monoids are always _cocommutative_ (that is, their underlying comonoid is cocommutative).  This is because every object of a cartesian monoidal category is a cocommutative comonoid object in a unique way, and every morphism is a comonoid homomorphism.

1. A _commutative_ Hopf monoid in a [[symmetric monoidal category]] $V$ is the same as a group object in $CMon(V)^{op}$, where $CMon(V)$ is the category of commutative monoids in $V$.  This works because the tensor product of commutative algebras is the categorical [[coproduct]], and hence the [[product]] in its [[opposite category]]. In particular, a commutative Hopf algebra is the same as a group object in the category $Alg^{op}$ of affine schemes.

Corresponding to these two, an ordinary group $G$ gives us two different Hopf algebras (here $k$ is the ground ring):

1. The [[group algebra]] $k[G]$ (the free vector space on the set $G$), with multiplication given by the group operation of $G$ and comultiplication given by the diagonal $g\mapsto g\otimes g$.  This Hopf algebra is always cocommutative, and is commutative iff $G$ is abelian.  It can be viewed as the result of applying the [[strong monoidal functor]] $k[-]:Set \to k Mod$ to the Hopf monoid $G$ in $Set$.

1. The function algebra $k(G)$ (the set of functions $G\to k$), with comultiplication given by precomposition with the group operation
$$k(G) \to k(G\times G) \cong k(G)\otimes k(G),$$
and multiplication given by pointwise multiplication in $k$.  In this case we need some finiteness or algebraicity of $G$ in order to guarantee $k(G\times G) \cong k(G)\otimes k(G)$.  This Hopf algebra is always commutative, and is cocommutative iff $G$ is abelian.

Note that if $G$ is finite, then $k[G]\cong k(G)$ as $k$-modules, but the Hopf algebra structure is quite different.


# The theorem of Hopf modules #

Hopf algebras can be characterized among bialgebras by the fundamental theorem on [[Hopf module|Hopf modules]]: the category of Hopf modules over a bialgebra is canonically equivalent to the category of vector spaces over the ground ring iff the bialgebra is a Hopf algebra.  This categorical fact enables a definition of Hopf monoids in some setups that do not allow a sensible definition of antipode.


#References#

For a diagrammatic definition of a Hopf algebra, see the [Wikipedia entry](http://en.wikipedia.org/wiki/Hopf_algebra#Formal_definition).

Eiichi Abe: Hopf algebras. Cambridge UP 1980.

Pierre Cartier: A primer on Hopf algebras. IHES 2006, 81p,
at www.ihes.fr

V. G. Drinfel'd, Quantum groups. Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 2 798--820, AMS 1987.

G. Hochschild, Introduction to algebraic group schemes, 1971

S. Majid, Foundations of quantum group theory. Cambridge University Press 1995, 2000.

John Milnor, J. Moore: The structure of Hopf algebras.
Annals of Math. 81 (1965), 211-264.

Susan Montgomery: Hopf algebras and their action on rings.
AMS 1994, 240p.

B. Parshall, J.Wang, Quantum linear groups. Mem. Amer. Math. Soc. 89(1991), No. 439, vi+157 pp.

M. Sweedler: Hopf algebras. Benjamin 1969.

William C. Waterhouse, Introduction to affine group schemes, Graduate Texts in Mathematics 66. Springer-Verlag, New York-Berlin, 1979. xi+164 pp.

# A Word of caution #

In algebraic topology, it is common to define Hopf algebras without mentioning the antipode, since in many topological cases of interest it exists automatically.  For example, this is the case if it is [[graded object|graded]] and "connected" in the sense that its degree-0 part is just the ground field (a property possessed by the homology or cohomology of any connected space).  In algebraic topology also the strict coassociativity is not always taken for granted.
