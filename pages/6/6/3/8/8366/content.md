
#Contents#
* table of contents
{:toc}

## Idea

For $a,b \in \mathbb{N}$ two positive [[natural numbers]], their **least common multiple** $LCM(a,b) \in \mathbb{N}$ is the smallest natural number that is divisible by both $a$ and $b$, i.e. such that there exist $n_a, n_n \in \mathbb{N}$ with $n_a \cdot a = n_b \cdot b = LCM(a,b)$.

## Remarks

### In the natural numbers

Spelled out, this means that the least common multiple of $a, b \in \mathbb{N}$, denoted $\mathrm{lcm}(a, b)$, is the element $d \in \mathbb{N}$ uniquely characterized by the following two conditions: 

* $a|d$ and $b|d$; 

* if $a|c$ and $b|c$, then $d|c$. 

One could equivalently equip the natural numbers with a [[function]] $\mathrm{lcm}:\mathbb{N} \times \mathbb{N} \to \mathbb{N}$ which satisfies the two conditions:

* $a|\mathrm{lcm}(a, b)$ and $b|\mathrm{lcm}(a, b)$; 

* if $a|c$ and $b|c$, then $\mathrm{lcm}(a, b)|c$. 

It is not true that "least" means least with respect to the usual ordering $\leq$. In particular, $1$ is the minimal element with respect to the divisibility ordering, and $\mathrm{lcm}(1, 1) = 1$ according to the definition above. However, if we construe "least" in the sense of $\leq$, since every natural number is a common multiple of $1$ with itself, then $0$ is the $\leq$-least natural number! 

Furthermore, it is also less robust, because the notion of $lcm$ is at bottom an [[ideal]]-theoretic notion: the divisibility order on elements of a [[principal ideal domain]] is a [[preorder]] whose posetal collapse is the collection of ideals, ordered oppositely to [[inclusion]]. Thus, in [[ring]]-theoretic contexts where there is no sensible notion of $\leq$, for example in the ring of [[Gaussian integers]], the notion of $\mathrm{lcm}$ still makes perfectly good sense if we use the first formulation above, expressed purely in terms of divisibility. 

From the point of view of principal ideals in a [[pid]] or [[Bézout domain]] $R$, the lcm corresponds to taking their [[meet]]: $(\mathrm{lcm}(a, b)) = (a) \cap (b)$. 

### In an arbitrary Bézout unique factorization domain

In an arbitrary [[Bézout domain|Bézout]] [[unique factorization domain]] $R$, the least common multiple function is only a [[prelattice]], because the minimum elements with respect to the least common multiple are given by the group of units $R^\times$. One usually takes the [[quotient monoid]] of the multiplicative structure on $R$ by the group of units $R^\times$ to get a [[lattice]]: thus, the least common multiple is a function $\mathrm{lcm}:R \times R \to R/R^\times$. In particular, in a [[discrete field]] $K$, the quotient $K/K^\times$ is the [[boolean domain]] $\mathrm{bool}$ and the lcm is thus a function $\mathrm{lcm}:K \times K \to \mathrm{bool}$, and in a [[Heyting field]] $F$, the quotient $F/F^\times$ is the [[set]] of [[truth values]] $\Omega$ whose divisibility partial order is the [[opposite poset]] of the usual partial order via [[entailment]], and the lcm is thus a function $\mathrm{lcm}:F \times F \to \Omega$, defined as $\mathrm{lcm}(a, b) \coloneqq \mathrm{isInvertible}(a) \wedge \mathrm{isInvertible}(b)$

## Related concepts

* [[greatest common divisor]]

## References

* Wikipedia, _[Least common multiple](https://en.wikipedia.org/wiki/Least_common_multiple)_

[[!redirects lcm]]
[[!redirects LCM]]

[[!redirects smallest common multiple]]
[[!redirects lowest common multiple]]

