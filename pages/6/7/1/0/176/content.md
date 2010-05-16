<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>

## Idea ##
Recall that a [[TQFT]] is an [[FQFT]] defined on the $(\infty,n)$-[[(infinity,n)-category of cobordisms|category of cobordisms]] whose morphisms are plain cobordisms and diffeomorphisms between these.

In a _conformal_ quantum field theory the cobordisms are equipped with a conformal structure (a Riemannian structure modulo a pointwise rescaling).

A conformal field theory (CFT) is accordingly a functor on such a richer category of conformal [[cobordism]]s.

See the discussion at [[FQFT]] for more details.

The low dimensional case of $2$-dimensional CFT is the least understood and the most interesting one. In d>2, the global transformations, i.e. the elements of the [[conformal group]], are given by the Poincare algebra, dilations and special conformal transformations. In $2$ dimensions, there are additionaly infinitely many local generators of conformal transformations whose commutation relations are given by the Virasoro algebra. In most of the literature, CFT is understood to be $2$-dimensional.

$2$-dimensional conformal field theories have two major applications:

* they describe critical phenomena on surfaces in condensed matter physics;

* they are the building blocks used in [[string theory]]

In the former application it is mostly the _local_ behaviour of the CFT that is relevant. This is encoded in [[vertex operator algebra]]s.

In the [[string theory|string theoretic]] applications the extension of the local theory to a full representation of the 2d conformal cobordism category is crucial. This extension is called _solving the sewing constraints_ .

## Definition ##

### Definition in Terms of the Osterwalder-Schrader Axioms ###
A definition of conformal field theories can be formulated using the appropriate version of the [[Osterwalder--Schrader axioms]], that is by a system of axioms of the [[correlation functions]]. From the correlation functions it is then possible to deduce the existence of field operators in the sense of the [[Wightman axioms]], that is fields aka field operators are operator valued distributions. Both the Hilbert space and the field operators are therefore not defined in the axioms, but reconstructed from the correlations functions defined in the first three axioms.

Let
$$
M_n := \{(z_1, ..., z_n) \in \mathbb{C}^n : z_i \neq z_j \; \text{for} \; i \neq j  \}
$$
be the **space of configuration points**.
Let $B_0$ be a countable index set and $B := \bigcup_{n \in \mathbb{N}} B_0^{n}$.

The correlation functions are a family $(G_i)_{i \in B}$ of continuous and polynomially bound functions
$$
   G_{i_1, ..., i_n}: M_n \to \mathbb{C} 
$$

+-- {: .un_defn}
###### Axiom 1
**locality**

For all indexes $(i_1, ..., i_n)$, configuration points $(z_1, ..., z_n)$ and permutations $\pi: \{1,..., n \} \to \{1,..., n \}$ one has
$$
G_{(i_1,..., i_n)}(z_1,..., z_n) = G_{(\pi(i_1),..., \pi(i_n))}(\pi(z_1),..., \pi(z_n))
$$
=--

In this context, covariance is meant with respect to the [[Euclidean group]] $E = E_2$.

+-- {: .un_defn}
###### Axiom 2
**covariance**

For every index $i \in B_0$ there are **conformal weights** $h_i, \overline{h_i} \in \mathbb{R}$ ($\overline{h_i}$ is completly independent from $h_i$, it is _not_ the complex conjugate, this notation is widly used in the physics literature so we use it here, too) such that for $n \ge 1$, $w \in E$ and $w_i := w(z_i)$, $h_j := h_{i_j}$ one has
$$
G_{(i_1,..., i_n)}(z_1, \overline{z_i}, ..., z_n, \overline{z_n}) = \prod (\frac{dw}{dz} (z_j))^{h_j} (\overline{\frac{dw}{dz}(z_j)})^{\overline{h_j}}   G_{(i_1,..., i_n)}(w_1, \overline{w_1}..., w_n, \overline{w_n})
$$

=--

The $s_i := h_i - \overline{h_i}$ are called **conformal spin** (for the index $i$) and $d_i := h_i + \overline{h_i}$ is the **scaling dimension**. As an axiom 2.2 we assume that all conformal spins and scaling dimensions are integers.

+-- {: .un_defn}
###### Axiom 3
**reflection positivity**

TODO
=--

+-- {: .un_prop}
###### Proposition
Both a Hilbert space and the field operators of the theory can be (re-) constructed from axioms 1, 2 and 3.

TODO: Details
=--

+-- {: .un_defn}
###### Axiom 4
**scaling covariance**

The correlation functions satisfy the covariance condition also for dilatations $w(z) = e^t (t), t \in \mathbb{R}$.
=--

Explicitly, the last condition says that
$$
G_i(z_1, ..., z_n) = (e^t)^{h_1 + \overline{h_1} +...+ h_n + \overline{h_n}} G_i(e^t(z_1), ..., e^t(z_n))
$$

Given axioms 1-4, the 2-point functions can be fully classified, see below.

+-- {: .un_defn}
###### Axiom 4
**existence of the energy-momentum tensor**

There are four fields $T{\mu, \nu}, \mu. \nu \in \{0, 1\}$ with the following properties:
$$

$$

$$

$$

$$

$$
=--


...

## Properties ##
+-- {: .un_prop}
###### Proposition
Any 2-point function satisfying axioms 1-4 has the following form:
$$
G_{ij}(z_1, z_2) = C_{ij} (z_1 - z_2)^{-(h_i + h_j)} (\overline{z_1} - \overline{z_2})^{-(\overline{h_i} + \overline{h_j})}
$$
with some constant $C_{ij} \in \mathbb{C}$.
=--

## Remarks ##

...

* The target space structure corresponding to [[defect line]]s in 2d CFT are [[bi-brane]]s.

...

## References ##

Useful references are at [[vertex operator algebra]].

The special case of _rational_ conformal field theory has been essentially entirely formalized and classified. The classification result for full rational 2d CFT was given by Fjelstad--Fuchs--[[Ingo Runkel|Runkel]]--Schweigert

* [FRS reviews](http://golem.ph.utexas.edu/string/archives/000747.html)

* [The FRS theorem of RCFT](http://golem.ph.utexas.edu/string/archives/000813.html)

A textbook directed at mathematicians and explaining the "classical" concept of a CFT, i.e. without reference to categories, is this:

* Martin Schottenloher: _A mathematical introduction to conformal field theory_ (2nd edition, [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1161.17014&format=complete))

[[!redirects CFT]]