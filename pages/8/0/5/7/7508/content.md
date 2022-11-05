
\tableofcontents

## Idea

In [[logic]] and [[type theory]], $\alpha$-equivalence is the principle that two syntactic expressions ([[types]], [[terms]], [[propositions]], [[contexts]], whatever) are equivalent for all purposes if their only difference is the renaming of bound [[variables]].

Depending on the technicalities of how variables are managed, $\alpha$-equivalence may be a necessary axiom, a provable theorem, or entirely trivial.  In any case, it is often (usually? always?) seen as a technicality devoid of conceptual interest.  However, it can be a technically nontrivial task to implement $\alpha$-conversion (which is necessary to avoid capture of free variables upon [[substitution]]) when programming logic or type theory into a computer.

## See also

* [[equality]]

## References

The distinction between $\alpha$-equivalence and syntactic equality of expressions is briefly discussed in:

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

[[!redirects alpha equivalent]]
[[!redirects alpha-equivalent]]
[[!redirects α-equivalent]]
[[!redirects alpha equivalence]]
[[!redirects alpha-equivalence]]
[[!redirects α-equivalence]]
[[!redirects alpha conversion]]
[[!redirects alpha-conversion]]
[[!redirects α-conversion]]
