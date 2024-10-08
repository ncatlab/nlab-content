
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
[[!include higher algebra - contents]]
=--
#### Quantum physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _Jordan algebra_ is an algebra that may not be [[associativity|associative]], but is [[commutative algebra|commutative]], subject to some further conditions which are modeled after the archetypical example: for $(A, \cdot)$ any [[associative algebra]], equipping it with the _symmetrized product_

$$
  x \circ y \coloneqq \frac{1}{2}(x y + y x) 
$$

makes $(A, \circ)$ a Jordan algebra. It is this relation that originally motivated the notion in discussion of [[quantum mechanics]], for the symmetrized product and hence the Jordan algebra structure of the [[algebra of observables]] of a [[quantum mechanics|quantum mechanical]] system is what remains when one ignores the otherwise all-important [[commutators]] and hence the [[Hamiltonian]] flows on observables.

But later Jordan algebras have been studied largely for their own sake. 

More recently, the [[Bohr topos]] associated to a noncommutative [[algebra of observables]] was found to really see the underlying Jordan algebra structure. See at _[[Bohr topos]]_ and _[[poset of commutative subalgebras]]_ for more on this.


## Definition

A **Jordan algebra** is a [[commutative algebra|commutative]] [[nonassociative algebra]] $J$ satisfying the __Jordan identity__ $(x y) (x x) = x (y (x x))$ for all $x,y$ in $J$.  

It follows (via a nontrivial argument) that $J$ is [[power-associative algebra|power-associative]], and the Jordan identity generalizes to
$$ (x^m y) x^n = x^m (y x^n) $$
for [[natural numbers]] $m, n \geq 1$ (and, trivially, for $m, n \geq 0$ if there is an [[identity element]]).  

Thus, we may equivalently define a Jordan algebra to be a commutative power-associative algebra $J$ such that for any $x \in J$, the operations of multiplication by powers $x^n$ ($n \ge 1$) all commute with each other.
 
If $k$ is a [[field]] whose [[characteristic]] is not $2$ (or is any [[commutative ring]] in which $2$ is invertible), then to any [[associative algebra|associative]] $k$-algebra $A$ with product $\cdot$, one associates a Jordan $k$-algebra with the same underlying vector space and whose Jordan product $\circ$ is given by

$$x\circ y \stackrel{def}{=} \frac{x\cdot y + y \cdot x}{2}.$$ 

Such Jordan algebras are called __special__ Jordan algebras; all others are called __[[exceptional Jordan algebra|exceptional]]__.



## Formally real Jordan algebras and their origin in quantum physics 
 {#OriginInQuantumPhysics}

Jordan algebras had their origin in the study of the foundations of [[quantum mechanics|quantum theory]].  In 1932, [[Pascual Jordan]] tried to isolate some axioms that an 'algebra of [[observable]]s' should satisfy ([Jordan 32](#Jordan32)).


The unadorned phrase 'algebra' usually signals an [[associative algebra]], but this is not the kind of algebra Jordan was led to.  In both [[classical mechanics|classical]] and [[quantum
mechanics]], [[observables]] are closed under addition and multiplication by [[real number|real]] scalars.  In classical mechanics we can also multiply observables, but in quantum mechanics this becomes problematic.  After
all, given two [[bounded linear operator|bounded]] [[self-adjoint]] [[linear operators]] on a complex [[Hilbert space]], their product is self-adjoint if and only if they commute.

However, in quantum mechanics one can still raise an observable to a power and obtain another observable.  From squaring and taking real linear combinations, one can construct a commutative product using the [[polarization identity]]:

$$    
  x \circ y \coloneqq \frac{1}{2}((x+y)^2 - x^2 - y^2)
                  = \frac{1}{2}(x y + y x) 
  \,.
$$

This is sometimes called the _anti-commutator_ (or more precisely, half the anti-commutator). Notice that it is analogous to the more famous [[commutator]]

$$
  [x,y] \coloneqq x y - y x
$$

and that both together recover the full algebra of observables in that

$$
  x y = \frac{1}{2}[x,y] + x \circ y
$$

for all $x,y$. (A [[JLB-algebra]] is a [[Banach space]] equipped with the compatible structures of both a [[Jordan algebra]] and a [[Lie algebra]], and these are equivalent to $C^*$-[[C-star-algebra|algebras]] in just this way, using $\circ$ and ${\bullet} \coloneqq \frac{1}{2} \mathrm{i} [{-},{-}]$ as the operations.)

From the point of view of [[deformation quantization]] of [[Poisson manifolds]], one can read this as follows: the deformation quantization of a Poisson manifold $(X,\{-,-\})$ breaks up into two pieces:

1. the [[Poisson bracket]] $\{-,-\}$ on $C^\infty(X)$ deforms to the [[commutator]];

2. the pointwise multiplication on $C^\infty(X)$ deforms into the Jordan algebra structure.

This perspective on deformation quantization making the role of Jordan algebras explicit is mentioned for instance in ([Bates-Weinstein, p. 80](#BatesWeinstein)).


The symmetrized product $(-) \circ (-)$ is not associative, in general, but it is power-associative: any way of parenthesizing a product of copies of the same observable $x$ gives the same result.  This led Jordan to define what is now called a **formally real Jordan algebra**: a commutative and power-associative algebra $J$ satisfying
$$  x_1^2 + \cdots + x_n^2 = 0 \quad \implies \quad x_1 = \cdots = x_n = 0  $$
for all $n$.  The last condition (as in any [[formally real algebra]]) gives $J$ a partial ordering: if we write $x \le y$ when the element $y - x$ is a sum of squares, it says that 
$$x \le y \; \& \; y \le x \quad \implies \quad x = y\,.$$
So, in a formally real Jordan algebra we can reasonably talk about one observable being 'greater' than another.

In fact the Jordan identity $(x \circ y) \circ (x \circ x) = x \circ (y \circ (x \circ x)) $ is a _consequence_ of the above definition of formally real Jordan algebra.  So, every formally real Jordan algebra is a Jordan algebra (but not conversely).

For more on this see also at _[order-theoretic structure in quantum mechanics -- Relation to non-commutative geometry](order-theoretic+structure+in+quantum+mechanics#RelationToTheNonCommutativePhaseSpace)_.

## Examples

### Classification of formally real Jordan algebras
{#frc}

In 1934, Jordan published a paper with von Neumann and Wigner classifying finite-dimensional formally real Jordan algebras ([Jordan-vonNeumann-Wigner 34](#JordanvNeumannWigner34)).


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

Because the octonions are an [[alternative algebra]] but not associative, we cannot go beyond $3 \times 3$ matrices and still get a Jordan algebra.  The $1 \times 1$ self-adjoint octonionic matrices are just the real numbers, and the $2 \times 2$ ones are isomorphic to the spin factor $\mathbb{R}^9 \oplus \mathbb{R}$.   The $3 \times 3$ self-adjoint octonionic matrices form the [[Albert algebra]].

Jordan algebras in the fifth family are called **spin
factors**.   This family has some overlaps with the others.  Most notably:

* The Jordan algebra of $2 \times 2$ self-adjoint real matrices is isomorphic to the spin factor $\mathbb{R}^2 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint complex matrices is isomorphic to the spin factor $\mathbb{R}^3 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint quaternionic matrices is isomorphic to the spin factor $\mathbb{R}^5 \oplus \mathbb{R}$.

* The Jordan algebra of $2 \times 2$ self-adjoint octonionic matrices is isomorphic to the spin factor $\mathbb{R}^9 \oplus \mathbb{R}$.

Because the spin factor $\mathbb{R}^n \oplus \mathbb{R}$ can be identified with $(n+1)$-dimensional [[Minkowski space]], this sets up a relation between the real numbers, complex numbers, quaternions and octonions and Minkowski space in 3,4,6 and 10 dimensions --- a pattern which becomes important in [[string theory]].  For more details, see  [[division algebras and supersymmetry]].

* [[John Baez]], The octonions, Sec. 3.3: $\mathbb{O}P^1$ and Lorentzian geometry.  ([web](http://math.ucr.edu/home/baez/octonions/node11.html))

* [[John Baez]] and [[John Huerta]], Division algebras and supersymmetry I.  ([arXiv](http://arxiv.org/abs/0909.0551))

In 1983, Zelmanov drastically generalized the result of Jordan, von Neumann and Wigner by classifying all simple Jordan algebras, including infinite-dimensional ones ([Zelmanov 83](#Zelmanov83)).

### Exceptional Jordan algebras

Among the exceptional Jordan algebras over the [[real numbers]], there is a remarkable $27$-dimensional example: the **[[Albert algebra]]** $\mathbb{Al}$ of [[self-adjoint matrix|self-adjoint]] $3\times 3$ [[matrix|matrices]] over the [[octonion|octonions]] with the same formula as above for the product in terms of [[matrix product]]. Notice that the octonions and their matrices do *not* form associative algebras, but only [[alternative algebras]], so the Jordan identity for the Albert algebra is not automatic (it does not hold for all alternative algebras) but is a consequence of more special circumstances.



## Self-dual homogeneous convex cones

The formalism of Jordan algebras seems rather removed from the
actual practice of [[physics]], because in quantum theory we hardly ever take two observables $a$ and $b$ and form their Jordan product
${1\over 2}(a b + b a)$.  As hinted in the previous section, it is better to think of this operation as derived from the process of _squaring_ an observable, which is something we actually do.  But
still, one must ask: can we see the classification of finite-dimensional formally real Jordan algebras, and thus the special role of [[normed division algebras]], as arising from some [[axioms]] more closely  tied to [[quantum theory]] as physicists usually practice it?

One answer involves the Koecher--Vinberg classification of  self-dual homogeneous [[convex cone]]s. 
Consider first the case of ordinary [[quantum theory]].  If a quantum
system has the [[Hilbert space]] $\mathbb{C}^n$, [[observables]] are described by
self-adjoint $n \times n$ complex [[matrix|matrices]]: elements of the Jordan algebra $\mathfrak{h}_n(\mathbb{C})$.  But matrices of this form that are nonnegative and have [[trace]] 1 also play another role.  They are called **[[density matrix|density matrices]]**, and they describe [[states]] of our quantum system: not just pure [[states]], but also more general mixed states.  The idea is that any density matrix $\rho \in \mathfrak{h}_n(\mathbb{C})$ allows us to define [[expectation value]]s of [[observable]]s $a \in \mathfrak{h}_n(\mathbb{C})$ via

\[                   
  \langle a \rangle = \tr(\rho a) 
  \,.
\]

The map sending observables to their expectation values is
real-linear.  The fact that $\rho$ is nonnegative is equivalent to

\[
  a \ge 0 \; \implies \; \langle a \rangle \ge 0 
\]

and the fact that $\rho$ has trace 1 is equivalent to

\[
  \langle 1 \rangle = 1 
  \,.
\]

All of this generalizes to an arbitrary finite-dimensional formally real Jordan algebra $J$.  Any such algebra automatically has an [[identity]] element.  This lets us define a **[[state]]** on $J$ to be a [[linear functional]] $\langle \cdot \rangle : J \to \mathbb{R}$ that is 

* **nonnegative**:
  $$  
    a \ge 0  \implies \langle a \rangle \ge 0  
  $$

* and **normalized**:

  $$   
    \langle 1 \rangle = 1 
    \,.
  $$

But in fact, there is a [[bijection|bijective]] correspondence between 
linear functionals on $J$ and elements of $J$.  The reason is that
every finite-dimensional Jordan algebra has a **[[trace]]**

$$
  \mathrm{tr} : J \to \mathbb{R} 
$$

defined so that $\mathrm{tr}(a)$ is the trace of the linear operator 'multiplication by $a$'.  Such a Jordan algebra is then formally real if and only if

$$
  \langle a, b \rangle = \mathrm{tr}(a \circ b) 
$$

is a real-valued [[inner product]]. So, when $J$ is a finite-dimensional formally real Jordan algebra, any linear functional 
$\langle \cdot \rangle : J \to \mathbb{R}$ can be written as

$$
  \langle a \rangle = \mathrm{tr}(\rho \circ a) 
$$

for a unique element $\rho \in J$.  Conversely, every element $\rho
\in J$ gives a linear functional by this formula.  While not obvious,
it is true that the linear functional $\langle \cdot \rangle$ is
nonnegative if and only if $\rho \ge 0$ in terms of the ordering on
$J$.  More obviously, $\langle \cdot \rangle$ is normalized if and
only if $\mathrm{tr}(\rho) = 1$.  So, states can be identified with certain special observables: namely, those observables $\rho \in J$ with $\rho \ge 0$ and $\mathrm{tr}(\rho) = 1$.  

These ideas help motivate an important theorem of Koecher and Vinberg.  The idea is to axiomatize the situation we we have just described, in a way that does not mention the Jordan product in $J$, but instead emphasizes:

* the [[isomorphism]] between $J$ and its [[dual vector space|dual space]]

* the fact that 'positive' elements of $J$ form a [[cone]].

To find appropriate axioms, suppose $J$ is a finite-dimensional
formally real Jordan algebra.  Then seven facts are always
true.  

1. The set of positive observables 

   $$
     C = \{a \in A \colon a \gt 0\}
     \,.
   $$

   is a **[[cone]]**: that is, $a \in C$ implies that every positive
multiple of $a$ is also in $C$.  

1. This cone is **[[convex space|convex]]**:

   if $a,b \in C$ then any linear combination $x a + (1-x) b$ with 
$0 \le x \le 1$ also lies in $C$.  

1. It is an open set.  

1. It is **regular**, meaning that if $a$ and $-a$ are both in the closure $\overline{C}$, then $a = 0$.  

   This condition may seem obscure, but if we note that

   $$             
     \overline{C} = \{ a \in J \colon a \ge 0 \}  
   $$

   we see that $C$ being regular simply means

   $$
    a \ge 0 \; and \; -a \ge 0 \quad \implies \quad a = 0 , 
   $$

   a perfectly plausible assumption.

1. Recall that $J$ has an inner product; this is what lets us
identify linear functionals on $J$ with elements of $J$.  This also
lets us define the **dual cone**

   $$
     C^* = \{  a \in J \colon \forall b \in A \; \; \langle a,b \rangle \gt 0 \} 
   $$

   which one can check is indeed a cone.  

   The fifth fact about $C$ is that it is **self-dual**, meaning $C = C^*$.  

   This formalizes the fact that states may be identified with special observables.

1. $C$ is **homogeneous**: given any two points $a,b \in C$, there is a real-linear transformation $T : A \to A$ mapping $C$ to itself in a [[bijection|bijective]] way, with  the property that $T a = b$.  This says that cone $C$ is highly symmetrical: no point of $C$ is any 'better' than any other, at  least if we only consider the linear structure of the space $A$, ignoring the Jordan product and the trace.

1. From another viewpoint, however, there is a very special point of $C$, namely the identity $1$ of our Jordan algebra.  And this brings us to our seventh and final fact: the cone $C$ is **pointed** meaning
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

Now for the payoff.  The work of Koecher and Vinberg, nicely explained in Koecher's  Minnesota notes ([Koecher](#Koecher)) shows that:


+-- {: .num_theorem}
###### Theorem

The [[category]] of pointed homogeneous self-dual 
regular open convex cones is [[equivalence of categories|equivalent]] to the category of finite-dimensional formally real Jordan algebras.

=--

This means that the theorem of Jordan, von Neumann and Wigner also classifies the pointed homogeneous self-dual regular convex cones!

+-- {: .num_theorem}
###### Theorem

Every pointed homogeneous self-dual regular open convex cone is [[isomorphic]] to a [[direct sum]] of those on this list:

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{R})$,

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{C})$,

* the cone of positive elements in $\mathfrak{h}_n(\mathbb{H})$,

* the cone of positive elements in $\mathfrak{h}_3(\mathbb{O})$, 

* the future lightcone in $\mathbb{R}^n \oplus \mathbb{R}$.

=--

Some of this deserves a bit of explanation.  For $\mathbb{K} = \mathbb{R}, \mathbb{C}, \mathbb{H}$, an element $T \in \mathfrak{h}_n(\mathbb{K})$ is **positive** if and only if the corresponding operator $T : \mathbb{K}^n \to \mathbb{K}^n$ has 
$$            \langle v, T v \rangle \gt 0  $$
for all nonzero $v \in \mathbb{K}^n$.  A similar trick works for defining positive elements of $\mathfrak{h}_3(\mathbb{O})$, but we do not need the details here. We say an element $(x,t) \in \mathbb{R}^n \oplus \mathbb{R}$ lies in the **future lightcone** if $t \gt 0$ and $t^2 - x \cdot x \gt 0$.  This of course fits in nicely with the idea that the spin factors are connected to Minkowski spacetimes.  Finally, there is an obvious notion of direct sum for Euclidean spaces with cones, where the direct sum of $(V,C)$ and $(V',C')$ is $V \oplus V'$ equipped with the cone
$$             C \oplus C' = \{(v,v') \in V\oplus V' \colon \; 
v \in C, v' \in C' \} . $$

In short: finite-dimensional formally real Jordan algebras arise fairly naturally as observables starting from a formalism where nonnegative observables form a cone, as long as we insist on some properties of this cone.


## Relation to commutative subalgebras

For every associative algebra there is its [[semilattice of commutative subalgebras]]  $ComSub(A)$. At least for $A, B$ [[von Neumann algebra]]s without type $I_2$ [[von Neumann algebra factor]]-subfactors, the isomorphisms $ComSub(A) \to ComSub(B)$ correspond to isomorphisms between the corresponding Jordan algebras $A_J \to B_J$.

For more details see [[semilattice of commutative subalgebras]].


## Related concepts

* [[Jordan-Lie-Banach algebra]]

* [[JBW-algebra]], [[JBW-algebraic quantum mechanics]]

* [[Kantor-Koecher-Tits construction]]

* [[order-theoretic structure in quantum mechanics]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[W-algebra]]

* [[Jordan superalgebra]]

* [[exceptional Jordan algebra]]/[[Albert algebra]]

## References

The original articles:

* {#Jordan32} [[Pascual Jordan]], *Über eine Klasse nichtassociativer hyperkomplexer Algebren*, Nachr. Ges. Wiss. Göttingen (1932) 569-575 &lbrack;[eudml:59403](https://eudml.org/doc/59403), [[Jordan-Algebren.pdf:file]]&rbrack;
 
* {#JordanvNeumannWigner34} [[Pascual Jordan]], [[John von Neumann]], [[Eugene Wigner]], *On an algebraic generalization of the quantum mechanical formalism*, Ann. Math. **35** (1934) 29-64 &lbrack;[jstor:1968117](https://www.jstor.org/stable/1968117), [doi:10.1007/978-3-662-02781-3_21](https://doi.org/10.1007/978-3-662-02781-3_21)&rbrack;
 

 
Textbooks:

*  Harald Hanche-Olsen and Erling Stormer: _Jordan Operator Algebras_, Pitman, 1984.  ([web](http://www.math.ntnu.no/~hanche/joa/))

* Nathan Jacobson, _Structure and Representations of Jordan Algebras_, American Mathematical Society, 1968.

* Kevin McCrimmon, _A Taste of Jordan Algebras_, Springer, 2006.  ([pdf](http://math.nsc.ru/LBRT/a1/files/mccrimmon.pdf))

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], Chapter 5 of _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000.

* Harald Upmeier, _Jordan Algebras in Analysis, Operator Theory, and 
Quantum Mechanics_, AMS, 1987.

Introductions and surveys include:

* Kevin McCrimmon, _Jordan algebras and their applications_,
_Bull. Amer. Math. Soc._ **84** (1978), 612--627.  ([AMS website](http://www.ams.org/bull/1978-84-04/S0002-990\
4-1978-14503-0/home.html)) and ([Project Euclid website](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540925)).

* {#Koecher} Max Koecher, _The Minnesota Notes on Jordan Algebras and 
Their Applications_, eds. Aloys Krieg and Sebastican Walcher, _Lecture Notes in Mathematics_ **1710**, Springer, Berlin, 1999. doi:[10.1007/BFb0096285](http://dx.doi.org/10.1007/BFb0096285) (paywalled)

* [[Paul Townsend]], _The Jordan formulation of quantum mechanics: a review_ ([arXiv:1612.09228](https://arxiv.org/abs/1612.09228))

More on the physical motivation for regarding any [[algebra of quantum observables]] (just) as a Jordan algebra:

* [[John Baez]], *Jordan algebras*, Section 4 of: *Getting to the Bottom of Noether's Theorem* &lbrack;[arXiv:2006.14741](https://arxiv.org/abs/2006.14741)&rbrack;


See also: 

* Wikipedia, *[Jordan algebra](https://en.wikipedia.org/wiki/Jordan_algebra)*

* {#Zelmanov83} E. I. Zelmanov, On prime Jordan algebras. II,
_Sibirsk Mat. J._ **24** (1983), 89-104.


Remarks on Jordan algebras as [[algebras of observables]] in quantum physics are for instance in 

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], p. 80 of: _[[Lectures on the geometry of quantization]]_, Berkeley Mathematics Lecture Notes series, American Mathematical Society (1997) &lbrack;[ams:bmln-8](https://bookstore.ams.org/bmln-8), [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf), [[BatesWeinstein-Lectures.pdf:file]]&rbrack;



Discussion of [[spectral triples]] over Jordan algebras in the [[Connes-Lott model]]:

* [[Latham Boyle]], [[Shane Farnsworth]], _The standard model, the Pati-Salam model, and "Jordan geometry"_ ([arxiv:1910.11888](https://arxiv.org/abs/1910.11888))

* [[Shane Farnsworth]], _The geometry of physical observables_ ([arXiv:2003.01708](https://arxiv.org/abs/2003.01708))

* Fabien Besnard, Shane Farnsworth, *Particle models from special Jordan backgrounds and spectral triples* $[$[arXiv:2206.07039](https://arxiv.org/abs/2206.07039)$]$

 


[[!redirects Jordan algebra]]
[[!redirects Jordan algebras]]

[[!redirects formally real Jordan algebra]]
[[!redirects formally real Jordan algebras]]

[[!redirects special Jordan algebra]]
[[!redirects special Jordan algebras]]

[[!redirects Jordan product]]
[[!redirects Jordan products]]

