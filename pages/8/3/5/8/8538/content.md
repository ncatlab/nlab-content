
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A system in [[formal logic]] is called _inconsistent_ if it admits a [[proof]] of a _[[contradiction]]_ (that is, usually, a proof of [[false]], or an [[inhabitant]] of the [[empty type]]).

Accordingly an [[axiom]] is called _inconsistent_ or to _lead to an inconsistency_ if adding it to an (implicitly understood) ambient logical system makes that system inconsistent.

In most usual logical systems, it follows that an inconsistent system admits a proof of *every* proposition, by the rule [[ex falso quodlibet]] (which is just the elimination rule for the [[empty type]]).  For this reason, sometimes (especially in [[type theory]]), the adjective "inconsistent" is used to mean a system with this property instead.  If we want to distinguish, then a system which admits a proof of every proposition may be called *trivial*.

As a further complication, a [[paraconsistent logic]] is often described as 'inconsistent but not trivial'.  However, many paraconsistent logics (such as [[dual-intuitionistic logic]]) admit ex falso quadlibet and fail to prove $\bot$; their 'inconsistency' is a proof of $p \wedge \neg{p}$ (or two proofs, one of $p$ and one of $\neg{p}$), which then fails to entail $\bot$.  We thus get three distinct levels of inconsistency:
* triviality (proving everything),
* proving a statement identified as $\bot$,
* proving $p$ and $\neg{p}$ for some statement $p$ and using an operator identified as [[negation]].


## Examples

* [[Russell's paradox]]

* [[Burali-Forti's paradox]]


## Related concepts

* [[consistency]]

* [[paraconsistent logic]]


[[!redirects inconsistency]]
[[!redirects inconsistencies]]
[[!redirects inconsistent system]]
[[!redirects inconsistent systems]]
[[!redirects inconsistent axiom]]
[[!redirects inconsistent axioms]]
[[!redirects inconsistent theory]]
[[!redirects inconsistent theories]]
