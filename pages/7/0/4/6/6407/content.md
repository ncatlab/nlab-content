
#Contents#
* table of contents
{:toc}

## Idea

For a commutative [[integral domain]] $D$, the set of all nonzero elements $D^\times$ is a multiplicative set, the corresponding [[commutative localization]] $D\to (D^\times)^{-1} D$ is an injective homomorphism of rings and $Q(D) = (D^\times)^{-1} D$ is a field, called the field of fractions or the quotient field of $D$. Its elements are fractions $a/b$ where $a\in D$ and $b\in D^\times$ which are by the definition the equivalence classes of pairs $(a,b) \in D\times D^\sharp$ and $(a,b)\sim (c,d)$ iff $a d = b c$. The addition is given by the formula
$$
\frac{a}{b}+\frac{c}{d} = \frac{ad+bc}{bd}
$$
and multiplication by $(a/b)(c/d) = (ac)/(bd)$. 

The field of fractions $Q(D)$ is unique minimal field in which the integral domain $D$ is embedded in the sense that every field $K\supset D$ contains the subfield isomorphic to $Q(D)$, namely consisting of all the fractions $a/d$ with $a\in D$, $d\in D^\sharp$ taken in the sense of division in $K$.

In the noncommutative case, the notion of a quotient skewfield is not always, and not uniquely defined. One class where this notion works well is the case or (left or right) [[Ore domain]]s where the set of all nonzero elements form a (left or right) Ore set and the Ore localization at that set defines a [[skewfield of fractions]]. 

Not every noncommutative integral domain can be embedded at all into a division ring. Suppose it does, say $D\hookrightarrow F$. Then all the say left fractions $d^{-1} b$ with $d,b\in D, d\neq 0$ do not form a subfield, namely we can not in general add a fractions to a fraction with common denominator, so this candidate for a subfield may have noninvertible elements. 

## Related concepts

* [[sheaf of rational functions]]

* [[localization]]

[[!redirects fields of fractions]]

[[!redirects quotient field]]

[[!redirects fraction field]]
[[!redirects fraction fields]]
