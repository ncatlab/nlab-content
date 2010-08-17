# Quantifiers
* table of contents
{: toc}

## Idea

A quantifier is an operation in [[logic]] that moves a [[predicate]] from one [[type]] to a related type.


## Quantification in first-order logic

In [[first-order logic]], we have two basic quantifiers, each of which moves a predicate on one type to a [[proposition]] (a predicate on no types), or more generally moves a predicate on $n + 1$ types to a predicate on $n$ types.

Given a predicate $P$ on a type $S$, the __universal quantification__ of $P$, denoted $\forall\, x\colon S,\; P(x)$ (and with many variations in punctuation), is intended to be true if and only if $P(a)$ is true for every possible element $a$ of $S$.  Similarly, the __existential quanification__ of $P$ (also called its __particular quantification__), denoted $\exists\, x\colon S\; P(x)$, is intended to be true if and only if $P(a)$ is true for at least one element $a$ of $S$.  However, it is quite possible that $P(a)$ may be provable (in a given [[context]] $\Gamma$) for every term $a$ of type $S$ that can be constructed (in $\Gamma$), yet $\forall\, x\colon S,\; P(x)$ cannot be proved; conversely, it is quite possible that $\exists\, x\colon S,\; P(x)$ can be proved (in a given context) but there $P(a)$ cannot be proved for any term $a$ of type $S$ that can be constructed.

Therefore, we must define the quantifiers more carefully; one way to do this is as follows:

***

Topics:

*  existential quantification
*  universal quantification
*  uniquness quantification
*  Lawvere quantification
*  bounded quantification


[[!redirects quantifier]]
[[!redirects quantifiers]]
[[!redirects quantification]]

[[!redirects existential quantifier]]
[[!redirects existential quantifiers]]
[[!redirects existential quantification]]
[[!redirects particular quantifier]]
[[!redirects particular quantifiers]]
[[!redirects particular quantification]]

[[!redirects universal quantifier]]
[[!redirects universal quantifiers]]
[[!redirects universal quantification]]

[[!redirects uniqueness quantifier]]
[[!redirects uniqueness quantifiers]]
[[!redirects uniqueness quantification]]
[[!redirects unicity quantifier]]
[[!redirects unicity quantifiers]]
[[!redirects unicity quantification]]

[[!redirects Lawvere quantifier]]
[[!redirects Lawvere quantifiers]]
[[!redirects Lawvere quantification]]

[[!redirects bounded quantifier]]
[[!redirects bounded quantifiers]]
[[!redirects bounded quantification]]
[[!redirects guarded quantifier]]
[[!redirects guarded quantifiers]]
[[!redirects guarded quantification]]
