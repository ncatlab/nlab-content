

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[natural numbers]] $0, 1, 2, \ldots$ are [[poset|partially ordered]] by the divisibility relation: $a|b$ if $b = a k$ for some natural number $k$. This poset is in fact a [[lattice]]. The *greatest common divisor* of $a, b$ is their [[meet]] in this lattice. 

## Remarks 

### In the natural numbers

Spelled out, this means that the greatest common divisor of $a, b \in \mathbb{N}$, denoted $\gcd(a, b)$, is the element $d \in \mathbb{N}$ uniquely characterized by the following two conditions: 

* $d|a$ and $d|b$; 

* if $c|a$ and $c|b$, then $c|d$. 

One could equivalently equip the natural numbers with a [[function]] $\gcd:\mathbb{N} \times \mathbb{N} \to \mathbb{N}$ which satisfies the two conditions:

* $\gcd(a, b)|a$ and $\gcd(a, b)|b$; 

* if $c|a$ and $c|b$, then $c|\gcd(a, b)$. 

It is almost but not quite true that "greatest" means greatest with respect to the usual ordering $\leq$. In particular, $0$ is the maximal element with respect to the divisibility ordering, and $\gcd(0, 0) = 0$ according to the definition above. However, there is no "greatest" common divisor of $0$ with itself if we construe "greatest" in the sense of $\leq$: every natural number is a common divisor of $0$ with itself, and there is no $\leq$-greatest natural number! 

Thus, the convention often seen in textbooks, which replaces the second condition above with 

* if $c|a$ and $c|b$, then $c \leq d$ 

or 

* if $c|a$ and $c|b$, then $c \leq \gcd(a, b)$. 

is slightly more awkward, and certainly less "pure" (mixing two relations $|$ and $\leq$). It is also less robust, because the notion of $gcd$ is at bottom an [[ideal]]-theoretic notion: the divisibility order on elements of a [[principal ideal domain]] is a [[preorder]] whose posetal collapse is the collection of ideals, ordered oppositely to [[inclusion]]. Thus, in [[ring]]-theoretic contexts where there is no sensible notion of $\leq$, for example in the ring of [[Gaussian integers]], the notion of $gcd$ still makes perfectly good sense if we use the first formulation above, expressed purely in terms of divisibility. 

From the point of view of principal ideals in a [[pid]] or [[Bézout domain]] $R$, the gcd corresponds to taking their [[join]]: $(\gcd(a, b)) = (a) + (b)$. Thus the [[Euclidean algorithm]], which applies generally to [[Euclidean domains]] $R$, is a way of calculating a generator of $(a) + (b)$ which consists of $R$-linear combinations of $a$ and $b$. 

### In the integers

In the set of [[integers]], the greatest common divisor only results in a [[prelattice]] rather than a lattice, because the divisibility relation is only a [[preorder]] rather than a [[partial order]], due to the fact that there is more than one element of the [[group of units]] of the integers. 

## Related concepts

* [[least common multiple]]

* [[Hermite normal form]]

* [[coprime integers]]

* [[GCD ring]]

## References

* Wikipedia, _[Greatest common divisor](https://en.wikipedia.org/wiki/Greatest_common_divisor)_

[[!redirects greatest common divisors]]

[[!redirects gcd]]
[[!redirects GCD]]
