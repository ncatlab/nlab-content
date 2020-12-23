
# Contents
* automatic table of contents goes here
{: toc}

## Idea

The _successor_ of something is the thing one step after it.


## Successors of natural numbers

Given a [[natural number]] $n$, the __successor__ $n^+$ of $n$ is simply $n + 1$.  In a topos, a [[natural numbers object]] $\mathbb{N}$ is equipped with a successor morphism $\mathbb{N}\to\mathbb{N}$, which, together with its zero element $1\to \mathbb{N}$, is used to characterize its abstract universal property of [[recursion]].

The formula $n^+ \coloneqq n + 1$ may be usefully generalized to other types of numbers; for example, in the [[real numbers]], the [[golden ratio]] $\Phi \approx 0.618$ is the positive number whose successor equals its [[reciprocal]] (or more commonly, the golden ratio $\phi \approx 1.618$ is the common successor and reciprocal of $\Phi$).


## Successors in well-orderings and cardinals

Generalizing successors in $\mathbb{N}$, in any [[well-ordered set]] $S$, the **successor** $w^+$ of an element $w$ is the least element of $S$ which is (strictly) greater than $w$ (if such an element exists).  If $S$ has no [[maximal element]], then the successor map $w \mapsto w^+$ is always defined; it is sometimes used to make recursive definitions.  We say that an element of a well-ordered set *is a successor* if it is the successor of something.

This notion is sometimes also used for some well-ordered proper classes, for example for the classes $\mathbf{Ord}$ of [[ordinal number]]s and $Card$ of [[cardinal numbers]].  (The latter is only well-ordered if we assume the [[axiom of choice]].)  Thus the **successor ordinal** of an ordinal $\alpha$ is the least ordinal greater than $\alpha$, which, if we use the von Neumann definition of ordinals, is $\alpha \cup \{\alpha\}$.  Similarly, the **successor cardinal** of a cardinal $\kappa$ is the least cardinal greater than $\kappa$.  We speak of "a successor ordinal" or "a successor cardinal" to mean an ordinal or cardinal which is the successor of some other ordinal or cardinal, respectively.

Note that if we identify a cardinal number with the least ordinal having that cardinality, as is common in [[material set theory]], then the *successor ordinal* and the *successor cardinal* of that cardinal are different.  For instance, the successor ordinal of $\omega = \aleph_0$ is $\omega+1$ (which is not a cardinal), whereas its successor cardinal is $\aleph_1$ (which is an ordinal but not a successor ordinal).

For definitions by [[transfinite recursion]], one usually specifies the value at $0$, the rule for recursion along the successor map, and a separate rule of recursion for the limiting ordinals (infinite ordinals which are not successors). (For example, the [[von Neumann hierarchy]] of well-founded [[pure set]]s is defined in that way.)  One can (and in [[constructive mathematics]] must) also handle all three cases at once, and the successor function is used there as well.

In [[constructive mathematics]], we take the successor of an ordinal to be $\alpha^+ \coloneqq \alpha \cup \{\alpha\}$ again, but it\'s not clear in what sense this is the smallest ordinal strictly greater than $\alpha$.  (On the one hand, given any [[truth value]] $P$, $\alpha_P \coloneqq \alpha \cup \{\alpha \mid P\}$ satisfies $\alpha \leq \alpha_P \leq \alpha^+$, but we cannot prove that $\alpha_P$ equals either $\alpha$ or $\alpha^+$; on the other hand, $(\alpha_P)^+$ is provably strictly greater than $\alpha$ in a sense, but we cannot prove that $\alpha^+ \leq (\alpha_P)^+$.)


## Successors of material sets

In [[material set theory]], the formula $\alpha^+ \coloneqq \alpha \cup \{\alpha\}$ is generalized from von Neumann ordinals to arbitrary [[pure sets]] (or material sets with [[urelements]]).  The successor $X^+ \coloneqq X \cup \{X\}$ of a material set $X$ is the smallest material set that contains $X$ as both a [[subset]] and a [[member]].


## Related concepts

* [[zero]]

* [[natural numbers object]]

* [[numeral]]

* [[Hartogs number]]

* [[Lindenbaum number]]


[[!redirects successor]]
[[!redirects successors]]

[[!redirects successor ordinal]]
[[!redirects successor cardinal]]
[[!redirects successor ordinals]]
[[!redirects successor cardinals]]

[[!redirects predecessor]]
[[!redirects predecessors]]



