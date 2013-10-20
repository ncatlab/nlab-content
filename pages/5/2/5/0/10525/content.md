
# $JB$-algebras
* table of contents
{: toc}

## Idea

A Jordan--Banach algebra is what fills in the following [[analogy]]:

+-- {: .standout}
[[associative algebra]] $:$ [[Jordan algebra]] $::$ [[Banach algebra]] $:$ Jordan--Banach algebra
=--

Just as a Jordan algebra that happens to be associative is the same thing as an associative algebra that happens to be [[commutative algebra|commutative]], the analogous result holds for Jordan--Banach algebras.

A $JB$-algebra is a Jordan--Banach algebra that satisfies some additional properties analogous to the additional properties satisfied by a $C^*$-[[C-star algebra|algebra]].  However, the analogy above cannot be extended; instead we have the following analogy:

+-- {: .standout}
associative $*$-[[star-algebra|algebra]] $:$ Jordan algebra $::$ Banach $*$-algebra $:$ Jordan--Banach algebra $::$ $C^*$-algebra $:$ $JB$-algebra $::$ [[von Neumann algebra]] $:$ $JBW$-algebra
=--

Now, an associative algebra on the right is the same thing as a commutative algebra on the left whose [[involution]] $*$ is trivial.

One can also consider Jordan $*$-algebras and the like, but the interesting thing is that important results about $C^*$-algebras have analogues already for $JB$-algebras.

Instead of an involution, we can add a compatible [[Lie algebra]] structure to a Jordan algebra.  Then even *without* assuming associativity or commutativity, an item on the left below (over the [[complex numbers]]) is the same thing as an item on the right below (over the [[real numbers]]), up to [[equivalence of categories]]:

+-- {: .standout}
associative $*$-algebra $:$ [[Jordan–Lie algebra]] $::$ Banach $*$-algebra $:$ Jordan--Lie--Banach algebra $::$ $C^*$-algebra $:$ $JLB$-algebra $::$ von Neumann algebra $:$ $JLBW$-algebra
=--

This is discussed (at least one line) at [[JLB-algebra]].


## Definitions

Let $A$ be a [[Banach space]], typically over the [[real numbers]], but potentially over any [[topological field]] (or possibly even more general).  We will generally assume the real numbers, but some theorems 

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

The Jordan--Banach algebra $A$ is __unital__ if the Jordan multiplication has an [[identity element]], usually denoted $1$:

* $1 \circ x = x$,
* $x \circ 1 = x$.
=--

+-- {: .num_defn}
###### Definition

The Jordan--Banach algebra $A$ is a __$JB$-algebra__ if it satisfies these identities:

* $B$-identity: ${\|x \circ x\|} = {\|x\|^2}$,
* positivity: ${\|x \circ x\|} \leq {\|x \circ x + y \circ y\|}$.
=--

Shortness of the multiplication follows from the $B$-identity (via the [[polarization identities]] and the triangle identity), so it may be left out of a direct definition of $JB$-algebras.  (Compare the analogous result for $C^*$-[[C-star-algebra|algebras]].)

+-- {: .num_defn}
###### Definition

The $JB$-algebra $A$ is a __$JBW$-algebra__ if it is unital and if its [[underlying]] Banach space has a [[predual]] $A_*$.
=--

See [[von Neumann algebra]] for motivation of the predual.


## Properties

Coming ... but basically, $JB$-algebras have nice properties like those of $C^*$-algebras, and $JBW$-algebras have nicer properties like those of von Neumann algebras.


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
