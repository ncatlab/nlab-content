# Admissible rule

## Idea

An admissible rule in a [[deductive system]], such as a [[logic]] or [[type theory]], is a "rule" for which there is some algorithm for constructing a derivation of the conclusion from derivations of the premises.  It is *not* one of the "specified" or [[primitive rules]] of the deductive system, but its admissibility means that it could be added as a primitive rule without changing the set of derivable judgments.

Compare to a [[derivable rule]], which is an admissible rule that is given by a "parametric" proof, or more formally by simply applying a finite number of primitive rules.  In contrast, the admissibility algorithm for an admissible rule is allowed to inspect and arbitrarily deconstruct the given derivations of the premises.

Unlike primitive and derivable rules, an admissible rule need *not* be satisfied by all semantics.  However, for most deductive systems there is a specified set of "important" admissible rules, and one considers only semantics that do satisfy these rules.

## Examples

* the [[cut rule]] and the identity in [[sequent calculus]]
* [[substitution]] in [[natural deduction]]
* [[negation]] in [[classical logic|classical]] [[linear logic]]

## Related Concepts

* [[focusing]]