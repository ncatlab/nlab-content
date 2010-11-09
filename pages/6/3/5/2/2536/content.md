
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Quantum physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* contents
{:toc}

##Idea##

A **Jordan algebra** is a commutative [[nonassociative algebra]] $J$ satisfying the __Jordan identity__ $(x y) (x x) = x (y (x x))$ for all $x,y$ in $J$.

If $k$ is a [[field]] whose [[characteristic]] is not $2$ (or is any [[commutative ring]] in which $2$ is invertible), then to any [[associative algebra|associative]] $k$-algebra $A$ with product $\cdot$, one associates a Jordan $k$-algebra with the same underlying vector space and whose Jordan product $\circ$ is given by

$$x\circ y \stackrel{def}{=} \frac{x\cdot y + y \cdot x}{2}.$$ 

Such Jordan algebras are called __special__ Jordan algebras; all others are called __exceptional__.

Among the exceptional Jordan algebras over the [[real numbers]], there is a remarkable $27$-dimensional example: the **Albert algebra** $\mathbb{Al}$ of [[self-adjoint matrix|self-adjoint]] $3\times 3$ [[matrix|matrices]] over the [[octonion|octonions]] with the same formula as above for the product in terms of [[matrix product]]. Notice that the octonions and their matrices do *not* form associative algebras, but only [[alternative algebras]], so the Jordan identity for the Albert algebra is not automatic (it does not hold for all alternative algebras) but is a consequence of more special circumstances.

## Formally real Jordan algebras ##

Jordan algebras had their origin in the study of the foundations of [[quantum mechanics|quantum theory]].  In 1932, [[Pascual Jordan]] tried to isolate some axioms that an 'algebra of [[observable]]s' should satisfy:

*  [[Pascual Jordan]], &#220;ber eine Klasse nichtassociativer
hyperkomplexer Algebren, _Nachr. Ges. Wiss. G&#246;ttingen
(1932), 569--575.

The unadorned phrase 'algebra' usually signals an [[associative algebra]], but this not the kind of algebra Jordan was led to.  In both [[classical mechanics|classical]] and [[quantum
mechanics]], [[observable]]s are closed under addition and multiplication by [[real number|real]] scalars.  In classical mechanics we can also multiply observables, but in quantum mechanics this becomes problematic.  After
all, given two [[bounded linear operator|bounded]] [[self-adjoint]] [[linear operator]]s on a complex [[Hilbert space]], their product is self-adjoint if and only if they commute.

However, in quantum mechanics one can still raise an observable to a power and obtain another observable.  From squaring and taking real linear combinations, one can construct a commutative product:
$$    x \circ y = {1\over 2}((x+y)^2 - x^2 - y^2)
                  = {1\over 2}(x y + y x) . $$
This product is not associative, but it is **power-associative**: any way of parenthesizing a product of copies of the same observable $x$ gives the same result.  This led Jordan to define what is now called a **formally real Jordan algebra**: a commutative and power-associative algebra $J$ satisfying
$$  x_1^2 + \cdots + x_n^2 = 0 \quad \implies \quad x_1 = \cdots = x_n = 0  $$
for all $n$.  The last condition gives $J$ a partial ordering: if we write $x \le y$ when the element $y - x$ is a sum of squares, it says that 
$$x \le y \; \& \; y \le x \quad \implies \quad x = y\,.$$
So, in a formally real Jordan algebra we can reasonably talk about one observable being 'greater' than another.

In fact the Jordan identity $(x y) (x x) = x (y (x x)) $
is a _consequence_ of the above definition of formally real Jordan algebra.  So, every formally real Jordan algebra is a Jordan algebra (but not conversely).

In 1934, Jordan published a paper with von Neumann and Wigner classifying finite-dimensional formally real Jordan algebras:

* [[Pascual Jordan]], [[John von Neumann]] and [[Eugene Wigner]], On an algebraic generalization of the quantum mechanical formalism, _Ann. Math._ **35** (1934), 29--64.

They began by defining an **ideal** of a formally real
Jordan algebra $J$ to be a linear subspace $S \subseteq J$ such that $x \in S$ implies $x \circ y \in S$ for all $y \in J$.  Next they defined $J$ to be **simple** when its only ideals were $\{0\}$ and $J$ itself.  Then they proved that any finite-dimensional formally Jordan algebra
is a direct sum of simple ones.

This reduced the classification problem to the task of classifying _simple_ finite-dimensional formally real Jordan algebras.  There are four families of these, and one exception:

* The $n \times n$ self-adjoint real matrices
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint complex matrices
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint quaternionic matrices
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint octonionic matrices
with the product $a \circ b = {1\over 2}(a b + b a)$, where $n \le 3$. 

* The space $\mathbb{R}^n \oplus \mathbb{R}$ with the product $(v,\alpha) \circ (w, \beta) = (\alpha w + \beta v, \langle v,w\rangle + \alpha \beta).$

Here we say a square matrix with entries in the $\ast$-algebra $A$ is **hermitian** if it equals its conjugate transpose.   (Note that $\mathbb{R}$, $\mathbb{C}$, $\mathbb{H}$ and $\mathbb{O}$ are all $\ast$-algebras.)   

Because the octonions are an [[alternative algebra]] but not associative, we cannot go beyond $3 \times 3$ matrices and still get a Jordan algebra.  The $1 \times 1$ self-adjoint octonionic matrices are just the real numbers, and the $2 \times 2$ ones are isomorphic to the spin factor $\mathbb{R}^9 \oplus \mathbb{R}$.   The $3 \times 3$ self-adjoint octonionic matrices form the Albert algebra.

Jordan algebras in the fifth family are called **spin
factors**.   This family has some overlaps with the others.  Most notably:

* The Jordan algebra of $2 \times 2$ self-adjoint real matrices is isomorphic to the spin factor $\mathbb{R}^2 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint complex matrices is isomorphic to the spin factor $\mathbb{R}^3 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint quaternionic matrices is isomorphic to the spin factor $\mathbb{R}^5 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint octonionic matrices is isomorphic to the spin factor $\mathbb{R}^9 \oplus \mathbb{R}$.

Because the spin factor $\mathbb{R}^n \oplus \mathbb{R}$ can be identified with $(n+1)$-dimensional [[Minkowski space]], this sets up a relation between the real numbers, complex numbers, quaternions and octonions and Minkowski space in 3,4,6 and 10 dimensions --- a pattern which becomes important in [[string theory]].  For more details, see  [[division algebras and supersymmetry]].

* [[John Baez]], The octonions, Sec. 3.3: $\mathbb{O}P^1$ and Lorentzian geometry.  ([web](http://math.ucr.edu/home/baez/octonions/node11.html))

* [[John Baez]] and [[John Huerta]], Division algebras and supersymmetry I.  ([arXiv](http://arxiv.org/abs/0909.0551))

In 1983, Zelmanov drastically generalized the result of Jordan, von Neumann and Wigner by classifying all simple Jordan algebras, including infinite-dimensional ones:

* E. I. Zelmanov, On prime Jordan algebras. II,
_Sibirsk Mat. J._ **24** (1983), 89-104.

## Self-dual convex homogeneous cones ##

Every finite-dimensional formally real Jordan algebra automatically has an [[identity]] element.  This lays the groundwork for an observation Max Koecher made in 1957-58.  Namely: the [[category]] of formally real Jordan algebras is [[equivalence of categories|equivalent]] to the category of self-dual convex homogeneous cones in finite-dimensional vector spaces (say $C \subset V$) equipped with a base point $p \in C$.  Here a cone $C \subset V$ is said to be **homogeneous** if it does not contain any straight lines and the group $GL(V)$ acts transitively on $V$.

Starting from a formally real Jordan algebra $J$, we get a self-dual convex homogeneous cone by taking $V = J$ and taking $C = \{x \in J: x \ge 0\}$.  As a basepoint we can take $p = 1$.  

The relation between (mixed) [[state]]s and [[observable]]s is well-known in traditional quantum mechanics: a self-adjoint $n \times n$ complex matrix can be regarded as an 'observable', but a nonnegative matrix of this form with trace equal to 1 is called a **[[density matrix]]** and describes a 'state' of the corresponding quantum system.    Koecher's result sets up a close relation between states and observables for any form of quantum theory based on a finite-dimensional formally real Jordan algebra.  In particular, the self-duality of the cone $C$ says that for a finite-dimensional algebra of observables, we can identify nonnegative observables with nonnegative linear functionals on the algebra of observables.  A nonnegative linear functional on the algebra of observables can be considered an 'unnormalized state', since a **[[state]]** is defined to be a [[linear functional]] 
$$    \mu : J \to \mathbb{R} $$
that is **nonnegative** ($x \ge 0 \Rightarrow \mu(x) \ge 0$) and **normalized** ($\mu(1) = 1$).   

## References

*  Harald Hanche-Olsen and Erling Stormer: _Jordan Operator Algebras_. ([web](http://www.math.ntnu.no/~hanche/joa/))

Kevin McCrimmon, Jordan algebras and their applications,
_Bull. Amer. Math. Soc._ **84** (1978), 612--627.  ([AMS website](http://www.ams.org/bull/1978-84-04/S0002-990\
4-1978-14503-0/home.html)) and ([Project Euclid website](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540925)

