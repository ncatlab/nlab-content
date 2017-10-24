+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea {#sec:org4b65bd2}

In the same way that in [[nonstandard
analysis]] one passes to [[elementary
extension|elementary extensions]] of the field
$\mathbb{R}$ which realizes more [[type (in model
theory)|types]] (in particular the types of infinite and
infinitesimal numbers), one can extend the standard model
$(\mathbb{N}, 0, 1, +, \times, S)$ of first-order [[Peano
arithmetic]] to proper elementary extensions that have
infinite natural numbers.

These "points at infinity" that live in the nonstandard part tend to
embody the uniform behavior of the numbers from the standard part. (For
example, by [[compactness
theorem|compactness]], the twin prime conjecture is true
if and only if in some nonstandard model of arithmetic there exists just
a single pair of nonstandard twin primes, and similarly Dirichlet's
theorem on arithmetic progressions can be reformulated as saying that
for every coprime positive pair of numbers $a$ and $b$ there exists just
one nonstandard prime congruent to $a$ modulo $b$.)

## Definition {#sec:org1621e14}

A **nonstandard model of arithmetic** is a proper
[[elementary extension]] of the *standard
model* $(\mathbb{N}, 0, 1, +, \times, S)$ of first-order
[[Peano arithmetic]].

## Examples {#sec:orgc18facb}

-   In the same way the [[hyperreal
    numbers]] are obtained by taking a countable
    ultrapower $\mathbb{R}^{\mathcal{U}}$ of $\mathbb{R}$, we can obtain
    the **hypernatural numbers** by taking a countable ultrapower
    $\mathbb{N}^{\mathcal{U}}$.

## Remarks {#sec:orgc4f9a0e}

This is all discussed in e.g. ([Gitman](#Gitman)).

-   While the standard model of arithmetic has no automorphisms, there
    exist countable models of arithmetic with
    [[continuum]]-many automorphisms.

-   A theorem due to Harvey Friedman states that every nonstandard model
    of arithemetic is isomorphic to some initial segment (in terms of
    the ordering discussed below) of itself.

-   A theorem due to Stanley Tennenbaum states that there is no
    countable nonstandard model of arithmetic for which there is an
    algorithm to compute addition or multiplication on the
    nonstandard part.

-   The usual ordering on the natural numbers is definable in
    [[Peano arithmetic|PA]] since
    $a \leq b \iff \exists c$ such that $a + c = b$.

## Denseness of ordering on nonstandard part {#sec:orgf41355d}

As remarked above, the usual ordering on $\mathbb{N}$ is definable in
$\mathsf{PA}$. Since the theory defines it, every nonstandard model of
arithmetic is linearly ordered. For every nonstandard number $\omega$,
one can generate using addition and subtraction a copy of $\mathbb{Z}$
around $\omega$, like so:

$$\left\{ \dots \omega - n, \dots, \omega - 1, \omega, \omega + 1, \dots, \omega + n, \dots\right\}$$

Since addition respects the ordering, $\omega + \omega$ is greater than
anything in this copy of $\mathbb{Z}$, and since multiplication respects
the ordering also, $\omega \times \omega$ is greater than
$n \times \omega$ for any finite $n$.

Similarly, if $\omega_1 &lt; \omega_2$, then the copy of $\mathbb{Z}$
around $\omega_1$ is below the copy of $\mathbb{Z}$ around $\omega_2$ in
the ordering.

It turns out that if you quotient out these copies of $\mathbb{Z}$ in
the nonstandard part of (any) nonstandard model of arithmetic, the
resulting order on the nonstandard part is [[DLO|dense and
without endpoints]].

Let's prove this. We'll give two proofs; they're really the same proof,
but one uses the language of an
[[ultrapower]] (the "hypernatural numbers")
while the other doesn't.

+-- {: .num_prop}
###### Proposition

The ordering of the copies of $\mathbb{Z}$ in the nonstandard part of a
nonstandard model of arithmetic is dense and without endpoints.

=--

+-- {: .proof}
###### Proof

(First proof.)

The theory of arithmetic proves that every other element
is divisible by $2$, so pick even representatives from every copy of
$\mathbb{Z}$ in the nonstandard part. Let $a$ represent a copy of
$\mathbb{Z}$ below a copy of $\mathbb{Z}$ represented by $b$. The theory
of arithmetic also proves that when $a$ and $b$ are even,

$$\models a &lt; \frac{a+b}{2} &lt; b$$

and since we have that $\models a + n &lt; b$ for each finite $n$, we
can also see that

$$\models a + n &lt; \frac{a + b}{2} &lt; b$$

for each finite $n$ (resp. &lt; $b - n$ for all finite $n$). This order
is dense and has no endpoints, since for any copy of $\mathbb{Z}$ in the
nonstandard part we can take an even representative and divide by $2$ to
obtain another nonstandard number which is below this copy of
$\mathbb{Z}$ (to see it has no upper bound, we can just look at
$\omega, \omega^2, \omega^3, \dots$.)

=--

+-- {: .proof}
###### Proof

(Second proof.)

Let $^*\mathbb{N}$ be any ultrapower nonstandard model of arithmetic. This is an uncountable and (at least) $\aleph_{1}$-saturated model of $\mathsf{PA}$, and its elements are equivalence classes ([[germs]]) of sequences $\overline{x}$ of natural numbers. The nonstandard part still consists of copies of $\mathbb{Z}$. Let $\overline{a}$ and $\overline{b}$ be nonstandard numbers such that $\overline{a}$ belongs to a lower copy of $\mathbb{Z}$ than $\overline{b}$ does. By the [[Los ultraproduct theorem]], $\overline{a}$ and $\overline{b}$ must therefore differ as sequences $\mathcal{U}$-often, with an unbounded sequence of differences. We can assume $\overline{a}$ and $\overline{b}$ are sequences of even numbers, since any perturbation of $\overline{a}$ and $\overline{b}$ by a sequence of $0$s and $1$s doesn't change what copy of $\mathbb{Z}$ $\overline{a}$ and $\overline{b}$ are in. Then the sequence $\overline{c}$ of their pointwise average will be between them, and will have unbounded $\mathcal{U}$-often difference from $\overline{a}$ and $\overline{b}$.

Again by the [[Los ultraproduct theorem]], the arithmetic operations in $^*\mathbb{N}$ are computed pointwise, so this argument will work in any elementary submodel of $^*\mathbb{N}$. In particular, any nonstandard model $M \models \mathsf{PA}$ embeds diagonally into its ultrapower $M^{\mathcal{U}}$.

=--

## Countable nonstandard models of arithmetic {#sec:org8d7c98e}

Peano arithmetic is the quintessential [[stability in
model theory|unstable theory]], and so there are plenty of
countable nonstandard models of [[Peano
arithmetic]] ($2^{\aleph_0}$-many.) One can
see this directly by [[type (in model
theory)|omitting]] the types of nonstandard numbers whose
only finite prime divisors is an arbitrary set of finite primes.

By the discussion above, the nonstandard part is linearly ordered and
can be partitioned into copies of $\mathbb{Z}$, and in fact these copies
of $\mathbb{Z}$ are densely ordered without endpoints.

Since the [[DLO|theory of dense linear orders without
endpoints]] has the unique countable model
$(\mathbb{Q}, &lt;)$, this means that for any countable nonstandard
model of arithmetic, the order type of the nonstandard part is
$\mathbb{Q} \mathbb{Z}$, i.e. $\mathbb{Q}$, but every time there's a
rational number, you have a copy of the integers instead.

So in a way, the wild divergence among the countable models of
$\mathsf{PA}$ comes very concretely from the arithmetic part of
$\mathsf{PA}$, and not at all from the ordering. However, this niceness
("categoricity") of the ordering on nonstandard models of arithmetic is
also being controlled by the arithmetic part of $\mathsf{PA}$ (since
that was all we used in the proofs of denseness above): if we were looking at just
elementary extensions of $(\mathbb{N}, &lt;)$, you would need to
stipulate $\omega$-saturation to force the order type on the
nonstandard part to be $\mathbb{Q} \mathbb{Z}$, because otherwise
there would be nothing wrong with just adjoining a single point at infinity and
generating a single copy of $\mathbb{Z}$ (possible with just the order because you can ask for the next or previous element in the ordering) around that for a countable
elementary extension of $(\mathbb{N}, &lt;)$.

## Related entries {#sec:orgb56552f}

-   [[natural number]]

-   [[nonstandard analysis]]

-   [[ultraproduct]]

-   [[Peano arithmetic]]

## References {#sec:org926dcee}

-   {#Gitman}Victoria Gitman, [An introduction to nonstandard models
    of arithmetic](https://boolesrings.org/victoriagitman/2015/04/22/an-introduction-to-nonstandard-models-of-arithmetic)

-   R. Kossak and J. H. Schmerl, The structure of models of Peano arithmetic, The Clarendon Press, Oxford University Press, Oxford, 2006, vol. 50. 

[[!redirects nonstandard arithmetic]]
[[!redirects hypernatural numbers]]
[[!redirects nonstandard models of arithmetic]]
[[!redirects nonstandard model of Peano arithmetic]]
[[!redirects nonstandard models of Peano arithmetic]]
