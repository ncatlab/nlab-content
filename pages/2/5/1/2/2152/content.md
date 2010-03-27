#Contents#
* automatic table of contents goes here
{:toc}

## Idea
In middle and high schools, analytic geometry refers to elementary methods in the geometry of $n$-dimensional [[Euclidean space]] involving *coordinate calculations*; it is usually combined with linear algebra taught in a geometric way.

In research mathematics, when one says analytic geometry, analytic refers to [[analytic function]]s in the sense of Taylor expansion and by __analytic geometry__ one usually means the study of geometry of complex (holomorphic) [[manifold]]s, their analytic subsets, [[Stein domain]]s and related notions. Similarly to an [[algebraic variety]], an [[analytic variety]] is locally given as a locus of a set of zeros of a finite family of holomorphic functions. A short survey can be found in a chapter of Dieudonne's _Panorama of pure mathematics_. 

In addition to analytic geometry over complex numbers, there is also another formalism which allows for nonarchimedean ground fields. This is the subject of [[rigid analytic geometry]]. Similarly to [[scheme]]s, rigid analytic varieties are glued from [[Bercovich spectrum|Bercovich spectra]] of certain commutative Banach algebras, so-called [[affinoid]]s, in a certain [[Grothendieck topology]]. There are several variants of the formalism (e.g. due Huber). The subject is closely related to [[formal geometry]] and has its main applications in [[arithmetic geometry]] and [[representation theory]]. It is an open problem to find an appropriate analogue of rigid analytic geometry in [[noncommutative geometry]], which is supposed to play an important role in mirror symmetry.

## holomorphic functions of several complex variables
This paragraph is about certain aspects of holomorphic functions $\mathbb{C}^n \to \mathbb{C}$ that are of relevance to the nLab. Right now we will concentrate on aspects that are important in the understanding of [[AQFT]], like a version of the [edge-of-the-wedge] (http://en.wikipedia.org/wiki/Edge-of-the-wedge_theorem) theorem.

From the viewpoint of complex [[manifold]]s this is the _local_ theory that describes the situation in coordinate patches.

* [Wikipedia] (http://en.wikipedia.org/wiki/Several_complex_variables)

When we talk about holomorphic functions in the following and do not specify the domain, we will always assume that the domain is an open, simply connected subset of $\mathbb{C}^n$.

### relevance to quantum field theory (QFT)
In the [[AQFT]] formalism (actually the following description is the Heisenberg picture of quantum mechanics in a nutshell) selfadjoint operators A on a Hilbert space $\mathcal{H}$ are the observables of a physical system, while normed vectors $x, y \in \mathcal{H}$ represent the states the system can be in. The real number $\langle y, Ax \rangle$ represents the probability that a system starting in state x will be in state y after a measurement of A. In [[AQFT]] we often encounter a set of operators indexed by several complex variables $z = (z_1, z_2, ...)$ and try to deduce properties of the theory from the function $f(z) := \langle y, A(z)x \rangle$. In this way, the theory of holomorphic functions of several variables is promoted to an irreplaceable tool in quantum field theory.   

### Hartogs' theorem
One stricing difference of functions of several _real_ variables and several _complex_ variables is described by Hartogs' theorem on separate analyticity:

* Theorem (Hartogs): Let f be a $\mathbb{C}$-valued function defined in an open set $U \subset \mathbb{C}^n$. Suppose that f is analytic in each variable $z_j$ when the other coordinates $z_k$ are fixed. Then f is analytic as a function of all n
coordinates.

_remark_: There are no other assumptions about f necessary, it needs not to be continous or even measurable. Note that in the real case the property of being partially differentiable alone encodes nearly no information about a function.

Reference:

* Paul Garrett: [Hartogs theorem] (http://www.math.umn.edu/~garrett/m/complex/hartogs.pdf)

_relevance_: When reading [[AQFT]] literature you will often encounter the claim that given functions are holomorphic, Hartogs' theorem simplifies the task of checking these claims considerably, because you have to check the holomorphy in every single variable only.

### analogues from the one-dimensional theory
Some results remain true in the multi dimensional case.

* Identity theorem: If a holomorphic function is zero in a neighbourhood of a point, it is the zero function.

_remark_: As usual the domain is supposed to be an open, simply connected (not necessarily proper) subset of $\mathbb{C}^n$, which implies that the point of the precondition of the theorem is an interior point of the domain.

### domains of holomorphy
One of the most notably difference of the theory of _one_ complex variable and of _several_ complex variables is that the [riemann mapping theorem] (http://en.wikipedia.org/wiki/Riemann_mapping_theorem) fails in several complex variables, which is in a certain sense the reason why in several complex variables there are domains which can be enlarged such that _all_ holomorphic functions extend to the larger domain.

_handwaving_ why this is not possible in one dimension: According to the riemann mapping theorem every domain (open, simply connected proper subset of $\mathbb{C}$) is biholomorph equivalent to the open disk $E: = \{ z: |z| \lt 1 \}$, which means that the rings of holomorphic functions are isomorph, too. But the ring of holomorphic functions on E has to every point in the boundary of E a function that has a pole in this point, so that E cannot be enlarged in a way that all holomorphic functions are extentable. Therefore this applies to every domain.

Some domains in $\mathbb{C}^n$ _do_ have the property that they cannot be enlarged, and since this is an interesting property, the name **domain of holomorphy** was coined for these, and the question how they could be described was promoted to an interesting research topic in the beginning of the 20th century.
   
* [Wikipedia] (http://en.wikipedia.org/wiki/Domain_of_holomorphy)

#### edge of the wedge theorems
These theorems desribe situations where holomorphic functions defined on specific domains (the wedges) can be continued to holomorphic functions of larger domains. 

* [Wikipedia] (http://en.wikipedia.org/wiki/Edge-of-the-wedge_theorem)

They are a valuable tool in [[AQFT]] (and were in fact discovered by one of the fathers of the theory, [Nikolay Bogolyubov] (http://en.wikipedia.org/wiki/Nikolay_Bogoliubov)).

We state here one version that will be of use to the nLab:

* theorem (edge of the wedge): Let $K := \{ z \in \mathbb{C}^n: |z| \le r \}$ be a ball in $\mathbb{C}^n$ and let $\mathcal{C} \subset \mathbb{R}^n$ be an open convex cone such that $\mathcal{C} \cap (- \mathcal{C}) \neq \emptyset $. We put $z = x + iy$ with $x, y \in \mathbb{R}^n$ and define an open domain G by $G:= \{ z = x + iy: z \in K, y \in \mathcal{C} \}$. Let $f$ be a holomorphic function in G and assume that 
$$
        \lim_{y \to 0, y \in \mathcal{C}} f(x + iy)
$$
exists for all $x \in B_r \subset \mathbb{R}^n$, where $B_r$ is an open ball with radius r. (The limit may not depend on the specific sequence chosen). Then $f$ is holomorph extendable into an open region $G \cup G_0$ with 
$$
        G_0 := \bigcup_{x \in B_r} \{ z: |z-x| \le \theta \cdot dist(x, \partial U) \}
$$
with $0 \lt \theta \lt 1$ a constant that is independent from $x, B_r$, and $f$.

_proof_: V.S.Vladimirov, "theory of functions of several complex variables" ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0125.31904&format=complete))

## References
...besides those already mentioned by the cited wikipedia articles:

A gentle and modern introduction to complex manifolds that starts with an extensive exposition of the local theory is this:

* Huybrechts, Daniel: "Complex geometry. An introduction." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1055.14001&format=complete))