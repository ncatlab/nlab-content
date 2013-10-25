
# $JB$-algebras
* table of contents
{: toc}

## Idea

Jordan--Banach algebras, $JB$-algebras, and the like fill out the following grand [[analogy]]:

| | | | |
|-|-|-|-|
| [[associative algebra]] | associative $*$-[[star-algebra|algebra]] | [[Jordan algebra]] | [[Jordan–Lie algebra]] |
| [[Banach algebra]] | Banach $*$-algebra | Jordan--Banach algebra | [[Jordan–Lie–Banach algebra]] |
| | $C^*$-[[C-star-algebra|algebra]] | $JB$-algebra | $JLB$-[[JLB-algebra|algebra]] |
| | [[von Neumann algebra]] | $JBW$-algebra | $JLBW$-algebra |

Just as a [[Jordan algebra]] that happens to be associative is the same thing as an [[associative algebra]] that happens to be [[commutative algebra|commutative]], the analogous result holds in the next row.  Similarly, an associative Jordan algebra is the same thing as a commutative $*$-[[star-algebra|algebra]] whose [[involution]] $*$ is trivial; this extends to all rows.

One can also consider Jordan $*$-algebras and the like, but the interesting thing is that important results about $C^*$-[[C-star-algebra|algebras]] have analogues already for $JB$-algebras. Instead of an involution, we can add a compatible [[Lie algebra]] structure to a Jordan algebra; then even *without* assuming associativity or commutativity, a [[Jordan–Lie algebra]] over the [[real numbers]] is the same thing as an associative $*$-algebra over the [[complex numbers]], up to [[equivalence of categories]], and this extends to lower rows.

The rightmost column is discussed at [[JLB-algebra]]; here we discuss the next-to-rightmost column (assuming the top row as known).  I also think that something might be done with the bottom half of the left column, but not here.


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

* $B$-identity: ${\|x \circ x\|} = {\|x\|^2}$,
* positivity: ${\|x \circ x\|} \leq {\|x \circ x + y \circ y\|}$.
=--

Shortness of the multiplication follows from the $B$-identity (via the [[polarization identities]] and the triangle identity), so it may be left out of a direct definition of $JB$-algebras; the same goes for the norm of $1$ in the unital case.  (Compare the analogous results for $C^*$-[[C-star-algebra|algebras]].)

+-- {: .num_defn}
###### Definition

The $JB$-algebra $A$ is a __$JBW$-algebra__ if it is unital and if its [[underlying]] Banach space has a [[predual]] $A_*$.
=--

See [[von Neumann algebra]] for motivation of the predual.  (Is it unique?  Should be!)


## Properties

Coming ... but basically, $JB$-algebras have nice properties like those of $C^*$-algebras, and $JBW$-algebras have nicer properties like those of von Neumann algebras.


## Examples

The main example of a $JB$-algebra is the algebra of [[self-adjoint operator]]s in a $C^*$-[[C-star-algebra|algebra]].  For a $JBW$-algebra, try the algebra of self-adjoint operators in a [[von Neumann algebra]].

In particular, the algebra of self-adjoint operators on a [[Hilbert space]] is a $JBW$-algebra.  (Note that a real Hilbert space and its complexification have the same algebra of self-adjoint operators.)

The [[trivial ring|trivial algebra]] (which is the algebra of self-adjoint operators on the zero Hilbert space) is a $JBW$-algebra, although it might not fit definitions by authors who mistakenly require ${\|1\|} = 1$.


## References

Most of what appears here is from

* [Jordan operator algebra](https://en.wikipedia.org/wiki/Jordan_operator_algebra) on the English Wikipedia;

and most of that appears to be from

* Harald Hanche-Olsen and Erling St&#248;rmer (1984), _Jordan operator algebras_, Monographs and Studies in Mathematics 21 (Pitman); [web](http://www.math.ntnu.no/~hanche/joa/),

which I have only begun to read.


## Related pages

* [[Jordan algebra]]
* **$JB$-algebra**
* [[JLB-algebra]]


[[!redirects JB-algebra]]
[[!redirects JB-algebras]]
[[!redirects JB algebra]]
[[!redirects JB algebras]]

[[!redirects Jordan Banach algebra]]
[[!redirects Jordan Banach algebras]]
[[!redirects Jordan-Banach algebra]]
[[!redirects Jordan-Banach algebras]]
[[!redirects Jordan–Banach algebra]]
[[!redirects Jordan–Banach algebras]]
[[!redirects Jordan--Banach algebra]]
[[!redirects Jordan--Banach algebras]]
