#Idea#

A Hopf algebra is a generalization of:

* the [[group algebra]] of a [[group]]

* the algebra of functions on a finite group, and more generally, the algebra of regular function on an affine algebraic $k$-group

* the [[universal enveloping algebra]] of a [[Lie algebra]]

All these algebras are actually [[bialgebra|bialgebras]], but furthermore they have a 'antipode' operation which mimics the inverse operation of a group.

#Definition#

A $k$-[[bialgebra]] $(A,m,\eta,\Delta,\epsilon)$ with multiplication $m$, comultiplication $\Delta$, unit $\eta: k\to A$ and counit $\epsilon:A\to k$ is a **Hopf algebra**
if there exists a $k$-linear map

$$S : A \to A$$

called the **antipode** (or coinverse) such that $m\circ(\mathrm{id}\otimes S)\circ \Delta = m\circ(S\otimes\mathrm{id})\circ\Delta = \eta\circ\epsilon$ (as a map $A\to A$). If an antipode exists then it is unique.

The identity for the antipode looks like a $k$-linear version of the identity satisfied by the inverse map in a group bimonoid: taking a group element $g$, duplicating by the diagonal map $\Delta$ to obtain $(g,g)$, taking the inverse of either component of this ordered pair, and then multiplying the two components, we obtain the identity element of our group. A characterization of Hopf algebras among the bialgebras is the validity of the fundamental theorem on [[Hopf module|Hopf modules]]: the category of Hopf modules over a bialgebra is canonically equivalent to the category of vector spaces over the ground ring iff the bialgebra is a Hopf algebra. This categorical fact enables to define Hopf bimonoids in some setups not allowing for a sensible definition of the antipode. 

An equivalent, more abstract definition of a commutative Hopf algebra is as a [[group|group object]] in $CAlg^{op}$, where $CAlg$ is the category of commutative algebras.  This works because the tensor product of commutative algebras is the categorical [[coproduct]], and hence the [[product]] in its [[opposite category]].

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

_Word of caution_: In algebraic topology, it is common to talk of Hopf algebra without mentioning the antipode since in many topological cases of interest it exists automatically.  For example, this is the case if it is [[graded object|graded]] and "connected" in the sense that its degree-0 part is just the ground field (a property possessed by the homology or cohomology of any connected space). In algebraic topology also the strict coassociativity is not always taken for granted.
