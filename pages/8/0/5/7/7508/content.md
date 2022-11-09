
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[logic]] and [[type theory]], $\alpha$-equivalence is the principle that two syntactic expressions ([[types]], [[terms]], [[propositions]], [[contexts]], whatever) are equivalent for all purposes if their only difference is the renaming of bound [[variables]].

Depending on the technicalities of how variables are managed, $\alpha$-equivalence may be a necessary axiom, a provable theorem, or entirely trivial.  In any case, it is often (usually? always?) seen as a technicality devoid of conceptual interest.  However, it can be a technically nontrivial task to implement $\alpha$-conversion (which is necessary to avoid capture of free variables upon [[substitution]]) when programming logic or type theory into a computer.

## See also

* [[equality]], [[syntactic equality]], [[definitional equality]]

## References

* [[Roy L. Crole]], *Alpha equivalence equalities*, Theoretical Computer Science, Volume 433, 18 May 2012, Pages 1-19, ([doi:10.1016/j.tcs.2012.01.030](https://doi.org/10.1016/j.tcs.2012.01.030))

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
