+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
 {#Idea}

Just as a [[monoid]] can [[action|act]] on a [[set]], a [[monoidal category]] can [[actegory|act]] on a [[category]] (such a structure is often called an **actegory**). A **multiactegory** is the appropriate generalisation from monoidal categories to [[multicategories]].

Given a multicategory $M$, a (left) $M$-multiactegory $A$ has a collection of **objects**, and for each list $m_1, \ldots, m_n$ of objects of $M$ and each pair of objects $a, a' \in A$, a collection of **multimorphisms**
$$m_1, \ldots, m_n, a \to a'$$
along with composition operations that cohere with the composition and identities in $M$.

## Representability

Just as monoidal categories can be identified with [[representable multicategories]], actegories can be identified with **representable multiactegories** (see §3.4 of [SZ24](#SZ24)).

## Related Concepts

* [[actegory]]

* [[multicategory]], [[representable multicategory]]


## References

Multiactegories were introduced in Definition 6.9 of the following paper, in the additional generality of [[skew-multicategories]]. Ordinary multiactegories are skew-multicategories that are **left-** and **right-normal** in the terminology ibid.

* [[Nathanael Arkor]], [[Dylan McDermott]], _The formal theory of relative monads_, Journal of Pure and Applied Algebra 107676. (2024) &lbrack;[arXiv:2302.14014](https://arxiv.org/abs/2302.14014)&rbrack.

The theory of [[representable multicategory|representability]] for multiactegories is developed in §3.4 of:

* {#SZ24} Mateusz Stroiński and Tony Zorman, _Reconstruction of module categories in the infinite and non-rigid settings_, [arXiv:2409.00793](https://arxiv.org/abs/2409.00793) (2024).

[[!redirects multiactegories]]


