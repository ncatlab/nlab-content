
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Implication
* table of contents
{: toc}

## Definitions

An _implication_ may be either an _entailment_ or a _conditional_ statement; these are closely related but not quite the same thing.

1. __Entailment__ is a [[preorder]] on [[propositions]] within a given [[context]] in a given [[logic]].  

   We say that $p$ entails $q$ _[[syntax|syntactically]]_, written as a [[sequent]] $p \vdash q$, if $q$ can be [[proof|proved]] from the assumption $p$.  

   We say that $p$ entails $q$ _[[semantics|semantically]]_, written $p \vDash q$, if $q$ holds in every [[model]] in which $p$ holds.  

   (These relations are often equivalent, by various [[soundness theorem|soundness]] and [[completeness theorem|completeness]] theorems.) 

1. A __conditional__ statement is the result of a [[binary operation]] on [[propositions]] within a given [[context]] in a given [[logic]].  If $p$ and $q$ are propositions in some context, then so is the conditional statement $p \to q$, at least if the logic has a notion of conditional.  

Notice that $p$, $q$, and $p \to q$ are all statements in the _object_ language (the language that we are talking about), whereas the [[hypothetical judgements]] $p \vdash q$ and $p \vDash q$ are statements in the _[[metalanguage]]_ (the language that we are using to talk about the [[object language]]).

### Relations between the definitions

Depending on what logic one is using, $p \to q$ might be anything, but it\'s probably not fair to consider it a conditional statement unless it is related to entailment as follows:
+-- {: .standout}
If, in some context, $p$ entails $q$ (either syntactically or semantically), then $p \to q$ is a [[theorem]] (syntactically) or a [[tautology]] (semantically) in that context, and conversely.
=--
In particular, this holds for [[classical logic]] and [[intuitionistic logic]].

You can think of entailment as being an [[external hom]] (taking values in the poset of [[truth values]]) and the conditional as being an [[internal hom]] (taking values in the poset of [[propositions]]).  In particular, we expect these to be related as in a [[closed category]]:

*  $ q \to r \vdash (p \to q) \to (p \to r) $,
*  $ p \equiv \top \to p $,
*  $ \top \vdash p \to p $,

where $\top$ is an appropriate constant statement (often satisfying $p \vdash \top$, although not always, as in [[linear logic]] with $\multimap$ for $\to$ and $1$ for $\top$).

Most kinds of logic used in practice have a notion of entailment from a [[list]] of multiple premises; then we expect entailment and the conditional to be related as in a closed [[multicategory]].

Just as we may identify the internal and external hom in [[Set]], so we may identify the entailment and conditional of [[truth values]].  In the $n$Lab, we tend to write this as $\Rightarrow$, a symbol that is variously used by other authors in place of $\vdash$, $\vDash$, and $\rightarrow$.

## In various formalizations

### In Heyting algebras

Although [[Heyting algebras]] were first developed as a way to discuss [[intuitionistic logic]], they appear in other contexts; but their characterstic feature is that they have an operation analogous to the conditional operation in logic, usually called __Heyting implication__ and denoted $\rightarrow$ or $\Rightarrow$.  If you use $\to$ and replace $\vdash$ above with the Heyting algebra\'s partial order $\leq$, then everything above applies.

### In natural deduction

In [[natural deduction]] the [[inference rules]] for implication are given as 

$$\frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma \vdash Q \; \mathrm{prop}}{\Gamma \vdash P \to Q \; \mathrm{prop}} \qquad \frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma, P \; \mathrm{true} \vdash Q \; \mathrm{true}}{\Gamma \vdash P \to Q \; \mathrm{true}} \qquad \frac{\Gamma \vdash P \to Q \; \mathrm{true}}{\Gamma, P \; \mathrm{true} \vdash Q \; \mathrm{true}}$$

### In type theory

In [[type theory]] 

* a _conditional statement_ is, under [[propositions-as-types]] a [[function type]] $p \to q$ (or the [[bracket type]] thereof).

* an _entailment_ is a [[hypothetical judgement]] or [[sequent]].

## Related concepts

* [[function type]]

* [[hypothetical judgement]]

* [[linear implication]]

* [[contrapositive]]

[[!include logic symbols -- table]]



[[!redirects implication]]
[[!redirects implications]]

[[!redirects entailment]]
[[!redirects entailments]]

[[!redirects conditional]]
[[!redirects conditionals]]
[[!redirects conditional statement]]
[[!redirects conditional statements]]

[[!redirects Heyting implication]]
[[!redirects Heyting implications]]
