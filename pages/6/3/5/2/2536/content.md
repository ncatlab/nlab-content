
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

The unadorned phrase 'algebra' usually signals an [[associative algebra]], but this is not the kind of algebra Jordan was led to.  In both [[classical mechanics|classical]] and [[quantum
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

In fact the Jordan identity $(x \circ y) \circ (x \circ x) = x \circ (y \circ (x \circ x)) $ is a _consequence_ of the above definition of formally real Jordan algebra.  So, every formally real Jordan algebra is a Jordan algebra (but not conversely).

In 1934, Jordan published a paper with von Neumann and Wigner classifying finite-dimensional formally real Jordan algebras:

* [[Pascual Jordan]], [[John von Neumann]] and [[Eugene Wigner]], On an algebraic generalization of the quantum mechanical formalism, _Ann. Math._ **35** (1934), 29--64.

They began by defining an **ideal** of a formally real
Jordan algebra $J$ to be a linear subspace $S \subseteq J$ such that $x \in S$ implies $x \circ y \in S$ for all $y \in J$.  Next they defined $J$ to be **simple** when its only ideals were $\{0\}$ and $J$ itself.  Then they proved that any finite-dimensional formally Jordan algebra is a direct sum of simple ones.

This reduced the classification problem to the task of classifying _simple_ finite-dimensional formally real Jordan algebras.  There are four families of these, and one exception:

* The $n \times n$ self-adjoint real matrices, $\mathfrak{h}_n(\mathbb{R})$, 
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint complex matrices, $\mathfrak{h}_n(\mathbb{C})$, 
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint quaternionic matrices, $\mathfrak{h}_n(\mathbb{H})$, 
with the product $a \circ b = {1\over 2}(a b + b a)$.

* The $n \times n$ self-adjoint octonionic matrices, $\mathfrak{h}_n(\mathbb{O})$, 
with the product $a \circ b = {1\over 2}(a b + b a)$, where $n \le 3$. 

* The space $\mathbb{R}^n \oplus \mathbb{R}$ with the product $(x,t) \circ (x', t') = (t x' + t' x, x \cdot x' + t t').$

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

## Self-dual homogeneous convex cones ##

The formalism of Jordan algebras seems rather removed from the
actual practice of physics, because in quantum theory we hardly ever
take two observables $a$ and $b$ and form their Jordan product
${1\over 2}(ab + ba)$.  As hinted in the previous section, it is
better to think of this operation as derived from the process of {\it
squaring} an observable, which is something we actually do.  But
still, one must ask: can we see the classification of finite-dimensional formally real Jordan algebras, and thus the special role of normed division algebras, as arising from some axioms more closely  tied to quantum theory as physicists usually practice it?

One answer involves the Koecher--Vinberg classification of  self-dual homogeneous convex cones. Consider first the case of ordinary quantum theory.  If a quantum
system has the Hilbert space $\C^n$, [[observables]] are described by
self-adjoint $n \times n$ complex matrices: elements of the Jordan
algebra $\mathfrac{h}_n(\C)$.  But matrices of this form that are nonnegative and have trace 1 also play another role.  They are called **density matrices**, and they describe [[states]] of our quantum system: not just pure states, but also more general mixed states.  The idea is that any density matrix $\rho \in \mathfrak{h}_n(\C)$ allows us to define expectation values of observables $a \in \mathfrak{h}_n(\C)$ via
\[                   \langle a \rangle = \tr(\rho a) .\]
The map sending observables to their expectation values is
real-linear.  The fact that $\rho$ is nonnegative is equivalent to
\[                 a \ge 0 \; \implies \; \langle a \rangle \ge 0 \]
and the fact that $\rho$ has trace 1 is equivalent to
\[                  \langle 1 \rangle = 1  .\]

All of this generalizes to an arbitrary finite-dimensional formally real Jordan algebra $J$.  Any such algebra automatically has an [[identity]] element.  This lets us define a **state** on $J$ to be a linear functional $\langle \cdot \rangle : J \to \mathbb{R}$ that is **nonnegative**:
$$  a \ge 0  \implies \langle a \rangle \ge 0  $$
and **normalized**:
$$   \langle 1 \rangle = 1 .$$
But in fact, there is a one-to-one correspondence between 
linear functionals on $J$ and elements of $J$.  The reason is that
every finite-dimensional Jordan algebra has a **trace**
$$        \mathrm{tr} : J \to \mathbb{R} $$
defined so that $\mathrm{tr}(a)$ is the trace of the linear operator 'multiplication by $a$'.  Such a Jordan algebra is then formally real if and only if
$$        \langle a, b \rangle = \mathrm{tr}(a \circ b) $$
is a real-valued inner product.   So, when $J$ is a finite-dimensional formally real Jordan algebra, any linear functional 
$\langle \cdot \rangle : J \to \mathbb{R}$ can be written as
$$          \langle a \rangle = \mathrm{tr}(\rho \circ a) $$
for a unique element $\rho \in J$.  Conversely, every element $\rho
\in J$ gives a linear functional by this formula.  While not obvious,
it is true that the linear functional $\langle \cdot \rangle$ is
nonnegative if and only if $\rho \ge 0$ in terms of the ordering on
$J$.  More obviously, $\langle \cdot \rangle$ is normalized if and
only if $\mathrm{tr}(\rho) = 1$.  So, states can be identified with certain special observables: namely, those observables $\rho \in J$ with $\rho \ge 0$ and $\mathrm{tr}(\rho) = 1$.  

This ideas help motivate an important theorem of Koecher and Vinberg.  The idea is to axiomatize the situation we we have just described, in a way that does not mention the Jordan product in $J$, but instead emphasizes:

* the isomorphism between $J$ and its dual space

* the fact that 'positive' elements of $J$ form a cone.

To find appropriate axioms, suppose $J$ is a finite-dimensional
formally real Jordan algebra.  Then seven facts are always
true.  

First, the set of positive observables 
$$              C = \{a \in A \colon a \gt 0\}  .$$
is a **[[cone]]**: that is, $a \in C$ implies that every positive
multiple of $a$ is also in $C$.  Second, this cone is **[[convex]]**:
if $a,b \in C$ then any linear combination $xa + (1-x)b$ with 
$0 \le x \le 1$ also lies in $C$.  Third, it is an open set.  Fourth, it is **regular**, meaning that if $a$ and $-a$ are both in the closure $\overline{C}$, then $a = 0$.  This last condition may seem obscure, but if we note that
$$             \overline{C} = \{ a \in J \colon a \ge 0 \}  $$
we see that $C$ being regular simply means
$$              a \ge 0 \; and \; -a \ge 0 \quad
\implies \quad a = 0 , $$
a perfectly plausible assumption.

Next recall that $J$ has an inner product; this is what lets us
identify linear functionals on $J$ with elements of $J$.  This also
lets us define the **dual cone**
$$           C^* = \{  a \in J \colon \forall b \in A \; \;
\langle a,b \rangle \gt 0 \} $$
which one can check is indeed a cone.  The fifth fact about $C$ is
that it is **self-dual**, meaning $C = C^*$.  This formalizes the fact that states may be identified with special observables.

The sixth fact is $C$ is **homogeneous**: given any two points $a,b \in C$, there is a real-linear linear transformation $T : 
A \to A$ mapping $C$ to itself in a one-to-one and onto way, with 
the property that $Ta = b$.  This says that cone $C$ is highly symmetrical: no point of $C$ is any 'better' than any other, at  least if we only consider the linear structure of the space $A$, ignoring the Jordan product and the trace.

From another viewpoint, however, there is a very special point of $C$, namely the identity $1$ of our Jordan algebra.  And this brings us to our seventh and final fact: the cone $C$ is **pointed** meaning
that it is equipped with a distinguished element (in this case $1 \in
C$).  

In short: when $J$ is a finite-dimensional formally real Jordan
algebra, $C$ is a pointed homogeneous self-dual regular open convex
cone.  All the elements $a \in J$ are positive observables, but
certain special ones, namely those with $\langle a, 1 \rangle = 1$,
can also be viewed as states.

In fact, there is a category of pointed homogeneous self-dual regular
open convex cones, where:

* An object is a finite-dimensional real inner product space 
$V$ equipped with a pointed homogeneous self-dual regular open convex cone $C \subset V$.

* A morphism from one object, say $(V,C)$, to another, say $(V',C')$,
is a linear map $T : V \to V'$ preserving the inner product and
mapping $C$ into $C'$.  

Now for the payoff.  The work of Koecher and Vinberg, nicely explained in Koecher's  Minnesota notes:

* Max Koecher, _The Minnesota Notes on Jordan Algebras and 
Their Applications_, eds. Aloys Krieg and Sebastican Walcher, _Lecture Notes in Mathematics_ **1710**, Springer, Berlin, 
1999.

shows that:

**Theorem:** The category of pointed homogeneous self-dual 
regular open convex cones is equivalent to the category of finite-dimensional formally real Jordan algebras.

This means that the theorem of Jordan, von Neumann and Wigner also classifies the pointed homogeneous self-dual regular convex cones!

**Theorem:** Every pointed homogeneous self-dual regular open convex cones is isomorphic to a direct sum of those on this list:

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{R})$,

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{C})$,

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{H})$,

* the cone of positive elements in $\mathfrak{h}_3(\mathbb{O})$, 

* the future lightcone in $\mathbb{R}^n \oplus \mathbb{R}$.

Some of this deserves a bit of explanation.  For $\mathbb{K} = \mathbb{R}, \mathbb{C}, \mathbb{H}$, an element $T \in \mathbf{h}_n(\mathbb{K})$ is **positive** if and only if the 
corresponding operator $T : \mathbb{K}^n \to \mathbb{K}^n$ has 
$$            \langle v, T v \rangle \gt 0  $$
for all nonzero $v \in \mathbb{K}^n$.  A similar trick works for defining positive elements of $\mathbf{h}_3(\mathbb{O})$, but we do not need the details here. We say an element $(x,t) \in \mathbb{R}^n \oplus \mathbb{R}$ lies in the **future lightcone** if $t \gt 0$ and $t^2 - x \cdot x \gt 0$.  This of course fits in nicely with the idea that the spin factors are connected to Minkowski spacetimes.  Finally, there is an obvious notion of direct sum for Euclidean spaces with cones, where the direct sum of $(V,C)$ and $(V',C')$ is $V \oplus V'$ equipped with the cone
$$             C \oplus C' = \{(v,v') \in V\oplus V' \colon \; 
v \in C, v' \in C' \} . $$

In short: finite-dimensional formally real Jordan algebras arise fairly naturally as observables starting from a formalism where nonnegative observables form a cone, as long as we insist on some properties of this cone.

## References

*  Harald Hanche-Olsen and Erling Stormer: _Jordan Operator Algebras_. ([web](http://www.math.ntnu.no/~hanche/joa/))

* Kevin McCrimmon, Jordan algebras and their applications,
_Bull. Amer. Math. Soc._ **84** (1978), 612--627.  ([AMS website](http://www.ams.org/bull/1978-84-04/S0002-990\
4-1978-14503-0/home.html)) and ([Project Euclid website](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540925)).

