
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An *Ackermann groupoid* is a particular type of [[algebra|algebraic]] [[mathematical structure]] that provides [[semantics]] for a flavour of [[relevance logic]], a weak form of [[substructural logic]]. 

Note that "groupoid" here does not mean *[[groupoid]]*, but *[[magma]]*. The terminology comes from logic, rather than category theory.

## Definition


An *Ackermann groupoid* is a [[partially ordered set|partially ordered]] [[magma]] $(M,\circ, 1,\leq)$ that is left unital ($1\circ a = a$ for all $a\in M$), and has a binary operation, "implication", written $b\to c$ satisfying $a \leq b\to c$ if and only if $a\circ b \leq c$.

This might be called an _implicational Ackermann groupoid_, since it provides semantic models for an implicational fragment of logic, together with [[intensional conjunction]] (here $\to$ models implication, analogous to [[linear implication]] in [[linear logic]]). A _positive_ Ackermann groupoid upgrades the underlying [[poset]] to a [[distributive lattice]], permitting the interpretation of additional logical connectives, namely (classical) [[logical conjunction]] and [[logical disjunction]].

## Example

Every [[Church monoid]] is an Ackermann groupoid.


## Related concepts

* [[relevance monoidal category]]
* [[relevance logic]]
* [[Church monoid]]
* [[Heyting algebra]]

## References

Ackermann groupoids were introduced in

* Robert K. Meyer and Richard Routley, _Algebraic analysis of entailment I_, Logique et Analyse NOUVELLE SÉRIE, Vol. 15, No. 59/60 (1972) pp407-428, [JSTOR](https://www.jstor.org/stable/44083856)

and named for [[Wilhelm Ackermann]].