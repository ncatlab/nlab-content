
# Radix notation
* table of contents
{: toc}

## Idea

At least in [[classical mathematics]], every [[real number]] may be written in _base $n$_ for any [[natural number]] $n \geq 2$ (binary for $n = 2$, decimal for $n = 10$, etc), which can be generalized to fractional $n \gt 1$ (especially $n = \mathrm{e} \approx 2.718$) and beyond.

For [[integers]], this idea goes back to the Old Babylonians using base $60$ (around 2000 BCE), perfected in the Gupta Empire using base $10$ (around 400), and popularized in Europe by [[Fibonacci]] (in 1202).  For arbitrary real numbers, these were first used by [[Abu'l-Hasan al-Uqlidisi]] (around 952) and popularized by [[Simon Stevin]] (in 1585).  This notation (in base $10$) is now ubiquitous, and (despite the technical difficulties of doing so rigorously) serves as a de facto definition of the [[real numbers]] in elementary mathematics.

Radix notation in base $2$ is the basis of [[floating point arithmetic]], the fast but imprecise method of calculation with real numbers usually used in modern [[computing]].


## Definition

Given a [[natural number]] $n \geq 2$, let $[n]$ be the set of natural numbers (including [[zero]]) strictly less than $n$: $[n] = \{0, 1, 2, \ldots, n - 2, n - 1\}$; in this context, an element of $[n]$ is called a __digit__ (in base $n$).  Let $\mathbb{Z}$ be the set of [[integers]]: $\mathbb{Z} = \{\ldots, -2, -1, 0, 1, 2, \ldots\}$; in this context, an element of $\mathbb{Z}$ is called a __place value__.  Then a [[function]] from $\mathbb{Z}$ to $[n]$ is a doubly-infinite [[sequence]] of digits, one digit for each place value.  Such a sequence $a = (a_i)_{i\colon{\mathbb{Z}}}$ defines a doubly-infinite [[series]] of [[rational numbers]]:
$$ \sum_{-\infty \lt i \lt \infty} a_i n^{-i} .$$
This series converges (to a [[real number]]) if and only if there is a place value $N$ such that $a_i = 0$ for all $i \lt N$.  That is, we can write the series as
$$ \sum_{i = N}^\infty a_i n^{-i} .$$
In this way, a sequence of digits (finite on one end, infinite on the other) represents a nonnegative [[real number]].

As a representation of real numbers, this is almost unique.  Specifically, two distinct sequences $a$ and $b$ of digits represent the same real number (meaning that the sums of the series are equal) if and only if there is some place value $m$ such that

* $a_i = b_i$ for every place value $i \lt m$,
* $a_m = b_m + 1$ (or the reverse), and
* $a_i = n - 1$ for every $i \gt m$ while $b_i = 0$ for every $i \gt m$.

In this case, the sequence with $0$s is generally considered standard.  The real numbers arising in this way are precisely the positive $n$-[[adic rational]] numbers, that is the [[rational numbers]] that are positive integer multiples of $n^{-m}$ for some integer $m$ (the same $m$ as above).

In [[classical mathematics]], every nonnegative real number may be represented in this way.  Given such a number $x$ and a place value $i$, let $a_i$ be the [[remainder]] modulo $n$ of the [[floor]] of $x n^i$: that is, $a_i \coloneqq \lfloor{x n^i}\rfloor \mod n$; then $x = \sum_i a_i n^{-i}$.  (For $n$-adic rational $x$, this will produce the representation with $0$s; to automatically produce the other representation, use $a_i = (\lceil{x n^i} - 1\rceil) \mod n$.)  The number $0$ is represented only by a sequence of all $0$s.

Given $n$ unique symbols for the $n$ digits, the real number represented by a sequence of digits may be written by, beginning at the smallest place value whose digit is nonzero, writing the symbols in order, with a dot (or comma), called the __radix point__, between place value $0$ and place value $1$ (and padding zeroes after the radix point if the first nonzero digit has not yet been reached).  Of course, the sequence is still infinite and cannot be written down, but we may write any finite portion.  The $n$-adic rationals can be represented exactly by leaving out the infinitely repeating digit $0$; arbitrary [[rational numbers]] may be represented exactly by a bar over a list of digits that repeats infinitely.  (It is a theorem that every non-$n$-adic rational number can be uniquely represented in this way; in fact, only rational numbers can be so represented.)  A subscript may be used to indicate the base $n$ (with a default base $10$ in practice).  Finally, a negative real number is written by writing its [[absolute value]] after a minus sign.


## Generalizations

Given any number $n$ (not necessarily a natural number), still called the _base_, and any set $D$ of numbers, whose elements are called _digits_, we may consider finite or infinite sequences of digits, indexed by integers (still called _place values_).  Such a sequence should include a smallest place value $N$ as part of its data (since $0$ may not be one of the digits), so the place values are all (or perhaps only some) of the integers $i \geq N$.  Then the infinite series
$$ \sum_{i=N}^\infty a_i n^{-i} $$
still converges to a real number.

If $n \geq 2$ is a natural number and $D$ is $[n]$, then we recover the representation above of all nonnegative real numbers, unique except for the positive $n$-adic rationals.  More generally, if $n \gt 1$ is any real number and $D$ is $[\lceil{n}\rceil]$, then we get a representation of all nonnegative real numbers, which (for non-integer $n$) is never unique (although in practice one uses the last sequence in [[lexicographic ordering]]).

If $n \geq 2$ is a natural number and $D$ is $[n] + 1 = \{1, 2, 3, \ldots, n - 1, n\}$, then we get a representation of all positive real numbers (but not $0$).  If $n = 1$ and $D$ is again $[n] + 1 = \{1\}$, then every infinite sequence gives a divergent series, but the finite sequences represent all positive integers, uniquely up to a [[shift]] of place value; this is called __tally notation__.  In the other direction, if $n \geq 3$ is a natural number and $D$ is a set of $n$ consecutive integers that includes both $-1$ and $1$, then we get a representation of all real numbers (positive, negative, and zero), which is unique except for a few rational numbers (in the case of $n = 3$ and so $D = \{-1, 0, 1\}$, those which are half of a power of $1/3$); this is called __balanced__ radix notation.


## Examples

Here are some representations of well-known real numbers in well-known radixes:

<table><tr><th>Number</th><th markdown="1">Decimal ($n = 10$, $D = [10]$</th><th markdown="1">Binary ($n = 2$, $D = \{0, 1\}$)</th><th markdown="1">Positive binary ($n = 2$, $D = \{1, 2\}$)</th><th markdown="1">Natural ($n = \mathrm{e}$, $D = \{0, 1, 2\}$)</th><th markdown="1">Ternary ($n = 3$, $D = \{0, 1, 2\}$)</th><th markdown="1">Balanced ternary ($n = 3$, $D = \{-1, 0, 1\}$</th><th markdown="1">Tally ($n = 1$, $D = \{1\}$)</th></tr>
<tr><td markdown="1">$0$</td><td markdown="1">$0$ (or $-0$)</td><td markdown="1">$0$ (or $-0$)</td><td markdown="1">$0$ (nonce symbol, or [[empty list]])</td><td markdown="1">$0$ (or $-0$)</td><td markdown="1">$0$ (or $-0$)</td><td markdown="1">$0$</td><td markdown="1">$0$ (nonce symbol, or [[empty list]])</td></tr>
<tr><td markdown="1">$1$</td><td markdown="1">$1$ (or $0.\overline{9}$)</td><td markdown="1">$1$ (or $0.\overline{1}$)</td><td markdown="1">$1$ (as a finite list, or $0.\overline{1}$ with padding $0$, or $0.0\overline{2}$)</td><td markdown="1">$1$ (or $0.2121111212001\ldots$, etc)</td><td markdown="1">$1$ (or $0.\overline{2}$)</td><td markdown="1">$1$</td><td markdown="1">$1$</td></tr>
<tr><td markdown="1">$2$</td><td markdown="1">$2$ (or $1.\overline{9}$)</td><td markdown="1">$10$ (or $1.\overline{1}$)</td><td markdown="1">$2$ (as a finite list, or $1.\overline{1}$, or $0.\overline{2}$ with padding $0$)</td><td markdown="1">$2$ (or $1.2121111212001\ldots$, etc)</td><td markdown="1">$2$ (or $1.\overline{2}$)</td><td markdown="1">$2$</td><td markdown="1">$11$</td></tr>
<tr><td markdown="1">$\mathrm{e}$</td><td markdown="1">$2.7182818284590\ldots$</td><td markdown="1">$10.10110111111\ldots$</td><td markdown="1">$1.21221222222\ldots$</td><td markdown="1">$10$ (or $2.121111212001\ldots$, etc)</td><td markdown="1">$2.2011011212211\ldots$</td><td markdown="1">$10.{-}0111{-}{-}0{-}0{-}\ldots$</td><td>(not possible)</td></tr>
<tr><td markdown="1">$3$</td><td markdown="1">$3$ (or $2.\overline{9}$)</td><td markdown="1">$11$ (or $10.\overline{1}$)</td><td markdown="1">$11$ (as a finite list, or $2.\overline{1}$, or $1.\overline{2}$)</td><td markdown="1">$10.020011200001\ldots$ (etc)</td><td markdown="1">$10$ (or $2.\overline{2}$)</td><td markdown="1">$10$</td><td markdown="1">$111$</td></tr>
<tr><td markdown="1">$\pi$</td><td markdown="1">$3.14159265358979\ldots$</td><td markdown="1">$11.001001000011\ldots$</td><td markdown="1">$2.112112111122\ldots$</td><td markdown="1">$10.101002020002$ (etc)</td><td markdown="1">$10.010211012222\ldots$</td><td markdown="1">$10.011{-}111{-}000{-}\ldots$</td><td>(not possible)</td></tr>
<tr><td markdown="1">$1/2$</td><td markdown="1">$0.5$ (or $0.4\overline{9}$)</td><td markdown="1">$0.1$ (or $0.0\overline{1}$)</td><td markdown="1">$0.1$ (as a finite list with padding $0$, or $0.0\overline{1}$ with padding $0$, or $0.00\overline{2}$)</td><td markdown="1">$0.1021200201202\ldots$ (etc)</td><td markdown="1">$0.\overline{1}$</td><td markdown="1">$0.\overline{1}$ (or $1.\overline{-}$)</td><td>(not possible)</td></tr>
<tr><td markdown="1">$1/3$</td><td markdown="1">$0.\overline{3}$</td><td markdown="1">$0.0\overline{10}$</td><td markdown="1">$0.00\overline{21}$ (with padding $0$)</td><td markdown="1">$0.021012102010201\ldots$ (etc)</td><td markdown="1">$0.1$ (or $0.0\overline{2}$)</td><td markdown="1">$0.1$</td><td>(not possible)</td></tr>
<tr><td markdown="1">$-1$</td><td markdown="1">$-1$ (or $-0.\overline{9}$)</td><td markdown="1">$-1$ (or $-0.\overline{1}$)</td><td markdown="1">$-1$ (as a finite list, or $-0.\overline{1}$ with padding $0$, or $-0.0\overline{2}$)</td><td markdown="1">$-1$ (or $-0.2121111212001\ldots$, etc)</td><td markdown="1">$-1$ (or $-0.\overline{2}$)</td><td markdown="1">$-1$</td><td markdown="1">$-1$</td></tr></table>


## Foundational issues

In [[constructive mathematics]], it is not generally true that every [[real number]] has a radix expansion. However, one does have the following results:

* In the presence of [[weak countable choice]], [[existential quantifier|there exists]] a [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) for every [[Cauchy real number]] iff $\mathrm{LLPO}_\mathbb{N}$ holds; there exists a radix expansion for every [[Dedekind real number]] has iff the analytic $\mathrm{LLPO}$ holds. Without [[weak countable choice]], [[Lifschitz realizability]] gives a model in which $\mathrm{LLPO}_\mathbb{N}$ holds but it is not true that there exists a radix expansion in any base for every [[Cauchy real number]], which implies that there are models in which the analytic LLPO holds but it is not true that there exists a radix expansion in any base for every [[Dedekind real number]]. See [[Andrew Swan]]'s answer to [Birchfield (2024)](#Swan). In addition, the analytic $\mathrm{LLPO}$ holds for the [[Dedekind real numbers]] in [[condensed sets]], but every function from the Dedekind real numbers to the [[boolean domain]] $\mathbb{2}$ is a [[constant function]], which implies that it is not true that there exists a radix expansion in any base for every [[Dedekind real number]]. 

* In the presence of [[countable choice]], $\mathrm{LLPO}_\mathbb{N}$ is equivalent to the claim that the rings of radix expansions in any two bases are isomorphic. See Daniel Mehkeri\'s answer to [Feldman (2010)](#Mehkeri).

* That every Cauchy real number has a choice of radix expansion in any base implies that the [[weak limited principle of omniscience]] (WLPO) for the natural numbers holds; that every Dedekind real number has a choice of radix expansion implies that the [[analytic WLPO]] holds. 

[[Fred Richman]] considered a number system (a noncancellable [[rig]]) of nonnegative decimal sequences in which $0.\overline{9} \lt 1$; the usual rig of nonnegative real numbers is a subrig; see [Richman 1999](#Richman1999).  Although Richman is a prominent constructivist, the development was not (and probably cannot be made) constructive.

Usenet legend [[Alexander Abian]], before branching into speculative physics, advocated polemically that the real numbers should be defined as finite or infinite sequences of decimal digits; see [Abian 1981](#Abian1981).  While not favoured by most mathematicians due to the inelegance of the definitions and proofs, this is the form in which the real numbers are often presented to elementary students.


## References

* [[Alexander Abian]]. 1981. Calculus must consist of the study of real numbers in their decimal representation and not of the study of an abstract complete ordered field or nonstandard real numbers. International Journal of Mathematical Education in Science and Technology 12(4). [Doi:10.1080/0020739810120417](https://doi.org/10.1080/0020739810120417).
  {#Abian1981}

* [[Fred Richman]], *Is 0.999… = 1?*. Mathematics Magazine, Volume 72, Issue 5, 1999, Pages 396-400, &lbrack;[doi:10.1080/0025570X.1999.11996777](https://doi.org/10.1080/0025570X.1999.11996777)&rbrack;
  {#Richman1999}

* {#Mehkeri} David Feldman (2010) on Math.Overflow, [Radix notation and toposes](http://mathoverflow.net/questions/49775/radix-notation-and-toposes/)

* {#Swan} Madeleine Birchfield (2024) on Category Theory Zulip, [Radix expansions in constructive mathematics](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Radix.20expansions.20in.20constructive.20mathematics)

[[!redirects radix notation]]
[[!redirects positional notation]]
[[!redirects place-value notation]]
[[!redirects place value notation]]

[[!redirects radix expansion]]
[[!redirects expansion in base]]

[[!redirects decimal notation]]
[[!redirects decimal expansion]]
