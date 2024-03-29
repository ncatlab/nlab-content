
# Jordan--Banach algebras
* table of contents
{: toc}

## Idea

Jordan--Banach algebras, $JB$-algebras, and the like fill out the following grand [[analogy]]:

| | | |
|-|-|-|
| [[associative algebra|associative]] $*$-[[star-algebra|algebra]] | [[Jordan algebra]] | [[Jordan–Lie algebra]] |
| associative [[Banach algebra|Banach]] $*$-algebra | Jordan--Banach algebra | [[Jordan–Lie–Banach algebra]] |
| $C^*$-[[C-star-algebra|algebra]] | $JB$-algebra | $JLB$-[[JLB-algebra|algebra]] |
| [[von Neumann algebra]] | $JBW$-algebra | $JLBW$-[[JLBW-algebra|algebra]] |

Just as a [[Jordan algebra]] that happens to be associative is the same thing as an [[associative algebra|associative]] $*$-[[star-algebra|algebra]] with trivial [[involution]] (aka simply an associative algebra) that happens to be [[commutative algebra|commutative]], the analogous result holds in the lower rows.

One can also consider Jordan $*$-algebras and the like, but the interesting thing is that important results about $C^*$-[[C-star-algebra|algebras]] have analogues already for $JB$-algebras. Instead of an involution, we can add a compatible [[Lie algebra]] structure to a Jordan algebra; then even *without* assuming associativity or commutativity, a [[Jordan–Lie algebra]] over the [[real numbers]] is the same thing as an associative $*$-algebra over the [[complex numbers]], up to [[equivalence of categories]], and this extends to lower rows.

The right column is discussed at [[Jordan–Lie–Banach algebra]]; here we discuss the middle column (assuming the top row and left column as known).


## Definitions

Let $A$ be a [[Banach space]], typically over the [[real numbers]], but potentially over any [[topological field]] (or possibly even more general).  We will generally assume the real numbers, and some theorems may rely on this, or at least on the divisibility of $2$ in the [[ground field]].

+-- {: .num_defn}
###### Definition

The Banach space $A$ becomes a __Jordan--Banach algebra__ if it is equipped with a [[binary operation]] $A \times A \to A$, called the _Jordan multiplication_ and often written infix as $\circ$, satisfying these identities:

* [[short map|shortness]]: ${\|x \circ y\|} \leq {\|x\|} {\|y\|}$,
* [[bilinear map|bilinearity]]: $(a x + y) \circ (b u + v) = a b (x \circ u) + a (x \circ v) + b (y \circ u) + y \circ v$,
* commutativity: $x \circ y = y \circ x$,
* Jordan identity: $(x \circ y) \circ (x \circ x) = x \circ (y \circ (x \circ x))$.
=--

For motivation of the first two, see [[Banach algebra]]; for motivation of the last three, see [[Jordan algebra]].

+-- {: .num_defn}
###### Definition

The Jordan--Banach algebra $A$ is __unital__ if the Jordan multiplication has an [[identity element]] in its unit ball, usually denoted $1$:

* $1 \circ x = x$,
* $x \circ 1 = x$,
* ${\|1\|} \leq 1$.
=--

People might state the last clause as ${\|1\|} = 1$, which follows (using shortness of the multiplication) from the existence of any $x \ne 0$.  However, ${\|1\|} = 0$ in the [[trivial ring|trivial algebra]], and this should be allowed.

+-- {: .num_defn}
###### Definition

The Jordan--Banach algebra $A$ is a __$JB$-algebra__ if it satisfies these identities:

* __$B$-identity__: ${\|x \circ x\|} = {\|x\|^2}$,
* _[[formally real algebra|positivity]]_: ${\|x \circ x\|} \leq {\|x \circ x + y \circ y\|}$.
=--

Shortness of the multiplication follows from the $B$-identity (via the [[polarization identities]] and the triangle identity), so it may be left out of a direct definition of $JB$-algebras; the same goes for the norm of $1$ in the unital case.  (Compare the analogous results for $C^*$-[[C-star-algebra|algebras]].)  Conversely, given shortness of multiplication (or even of squaring), these two identities may be combined into the single inequality
$$ {\|x\|}^2 \leq {\|x \circ x + y \circ y\|} .$$

Also, positivity implies that $A$ is [[formally real algebra|formally real]]: if $x^2 + y^2 = 0$, then $x, y = 0$ (and so on for any number of terms).  Given this, the Jordan identity is equivalent to [[power-associative algebra|power-associativity]] (which it implies regardless) in a direct definition of $JB$-algebra.

+-- {: .num_defn}
###### Definition

The $JB$-algebra $A$ is a __$JBW$-algebra__ if it is unital and if its [[underlying]] Banach space has a [[predual]] $A_*$.
=--

See [[von Neumann algebra]] for motivation of the predual.  As with $C^*$-algebras, the predual (if it exists) is [[unique up to unique isomorphism]].

+-- {: .num_defn}
###### Definition

A __[[homomorphism]]__ from a Jordan--Banach algebra $A$ to a Jordan--Banach algebra $B$ is a [[bounded linear map]] $T\colon A \to B$ of Banach spaces (everywhere defined) such that $T(x \circ y) = T(x) \circ T(y)$ always holds.  If $A$ and $B$ are unital, then the homomorphism is __unital__ if $T(1) = 1$.
=--

To get the right notion of [[isomorphism]], the [[morphisms]] in the [[category]] of Jordan--Banach algebras should be the *[[short linear map|short]]* homomorphisms (see [Ban#morphisms](Ban#morphisms) for discussion).  However, if $A$ and $B$ are $JB$-algebras, then every homomorphism is short (as with $C^*$-algebras); in fact, we do not even have to assume that $T$ is bounded.  Similarly, a morphism of unital Jordan--Banach algebras should be unital.

+-- {: .num_defn}
###### Definition

Given a Jordan--Banach algebra $A$ and a [[Hilbert space]] $H$, a __[[representation]]__ $\pi$ of $A$ on $H$ is a homomorphism from $A$ to the algebra of [[Hermitian operators]] on $H$ (which is a $JB$-algebra, in fact a $JBW$-algebra, under the symmetrized product, as described in the examples).  Such a representation is __[[faithful representation|faithful]]__ if it\'s an [[injective function]].
=--

Again, we should really look only at the short representations (which is automatic for a $JB$-algebra) and look especially at the unital representations of a unital Jordan--Banach algebra.

Recall that a Jordan algebra is __[[special Jordan algebra|special]]__ if it has a faithful representation on a [[vector space]] (which follows if it has any injective homomorphism to the Jordanization of any associative algebra).

+-- {: .num_defn}
###### Definition

A __$JC$-algebra__ is $JB$-algebra that has a faithful representation on a Hilbert space.  A __$JW$-algebra__ is a $JBW$-algebra that\'s also a $JC$-algebra.
=--

This follows if the $JB$-algebra has any injective homomorphism to the algebra of [[Hermitian operators]] in any $C^*$-algebra, by the theorem that every abstract $C^*$-algebra may be made concrete.  But this theorem does *not* itself have an analogue for $JB$-algebras; the [[Albert algebra]] $\mathfrak{h}_3(\mathbb{O})$ is a $JB$-algebra (even a $JBW$-algebra) that is not a $JC$-algebra.

This is probably unfortunate terminology (compare '$B^*$-algebra' vs '$C^*$-algebra' and '$W^*$-algebra' vs 'von Neumann algebra'); it would probably be better just to call such $JB$-algebras __special__ (but somebody might think that this just means that the underlying Jordan algebra is special, which is weaker).  We do need some term, however, thanks to the Albert algebra.


## Examples

The main example of a $JB$-algebra is the algebra of [[self-adjoint operators]] in a $C^*$-[[C-star-algebra|algebra]].  For a $JBW$-algebra, try the algebra of self-adjoint operators in a [[von Neumann algebra]].  In particular, the algebra of Hermitian operators on a [[Hilbert space]] is a $JBW$-algebra, in fact a $JW$-algebra.  Still more particularly, the [[trivial ring|trivial algebra]] (which is the algebra of self-adjoint operators on the zero Hilbert space) is a $JW$-algebra (although it won\'t fit definitions by authors who require ${\|1\|} = 1$).

Every $JB$-algebra is [[formally real algebra|formally real]]; conversely, all of the formally real Jordan algebras in [[finite-dimensional space|finite dimensions]] are $JBW$-algebras, and all of the special ones are $JW$-algebras.  This leaves the [[Albert algebra]] $\mathfrak{h}_3(O)$ as the basic example of a $JBW$-algebra that is not a $JW$-algebra.  (See [Jordan algebra#frc](Jordan+algebra#frc) for the classification of the finite-dimensional formally real Jordan algebras.)


## Properties

$JB$-algebras have nice properties like those of $C^*$-algebras, and $JBW$-algebras have nicer properties like those of von Neumann algebras.  They are generally proved in the analogous ways.  Some properties are different, however.

An associative $JB$-algebra is the same thing as a commutative $C^*$-algebra with trivial involution, which (over the [[real numbers]]) is in turn the same thing as the algebra of (real-valued) [[continuous maps]] vanishing at infinity on a [[local compactum]] (which is a [[compactum]] iff the algebra is unital, and then every continuous map vanishes at infinity).

Like any Jordan algebra, a $JB$-algebra $A$ is [[power-associative algebra|power-associative]], so each element $x$ generates an associative (and of course commutative) [[subalgebra]] and hence a local compactum.  In a unital $JB$-algebra, each element generates an associative unital subalgebra and hence a compactum $Spec(x)$.  Any [[continuous map]] $f\colon Spec(x) \to \mathbb{R}$ therefore defines an element $f(x)$ of $A$.  More generally, any associative unital subalgebra $X$ generates a compactum $Spec(X)$, its [[spectrum]], and any continuous map on $Spec(X)$ defines an element of $A$ (in fact belonging to $X$).  Thus we have a [[functional calculus]] on $JB$-algebras.  In a $JBW$-algebra, we may instead interpret the spectrum as a [[localizable measure space]], with $X$ identified as the algebra of [[essentially bounded function|essentially bounded]] [[measurable functions]] (modulo [[almost equality]]) on the spectrum, so that the functional calculus extends to measurable functions.

Since every $JB$-algebra $A$ is [[formally real algebra|formally real]], it comes equipped with a [[partial order]]: $x \leq y$ iff $y - x$ is a sum of squares.

The [[order-theoretic structure in quantum mechanics]] fixes the $JB$-algebra structure of a $C^*$-algebra, but not the $JLB$-algebra structure.


## Related concepts

* [[JBW-algebraic quantum mechanics]]


## References

Basic stuff is at

* [Jordan operator algebra](https://en.wikipedia.org/wiki/Jordan_operator_algebra) on the English Wikipedia;

and most of that appears to be from

* Harald Hanche-Olsen and Erling St&#248;rmer (1984); _Jordan operator algebras_; Monographs and Studies in Mathematics 21 (Pitman); [web](http://www.math.ntnu.no/~hanche/joa/),

which I have only begun to read.

There is also

* Harald Upmeier (1987); _Jordan Algebras in Analysis, Operator Theory, and Quantum Mechanics_; CBMS Regional Conference Series in Mathematics 67 (AMS),

of which a lot is already on pages 1--4 (the only ones that Google Books would show me).


## Related pages

* [[Jordan algebra]]
* **Jordan--Banach algebra**
* [[Jordan–Lie–Banach algebra]]


[[!redirects Jordan Banach algebra]]
[[!redirects Jordan Banach algebras]]
[[!redirects Jordan-Banach algebra]]
[[!redirects Jordan-Banach algebras]]
[[!redirects Jordan–Banach algebra]]
[[!redirects Jordan–Banach algebras]]
[[!redirects Jordan--Banach algebra]]
[[!redirects Jordan--Banach algebras]]

[[!redirects JB-algebra]]
[[!redirects JB-algebras]]
[[!redirects JB algebra]]
[[!redirects JB algebras]]

[[!redirects JBW-algebra]]
[[!redirects JBW-algebras]]
[[!redirects JBW algebra]]
[[!redirects JBW algebras]]

[[!redirects JC-algebra]]
[[!redirects JC-algebras]]
[[!redirects JC algebra]]
[[!redirects JC algebras]]

[[!redirects JW-algebra]]
[[!redirects JW-algebras]]
[[!redirects JW algebra]]
[[!redirects JW algebras]]

[[!redirects B-identity]]
