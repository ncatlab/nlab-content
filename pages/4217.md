
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Logical disjunction
* table of contents
{: toc}

## Definitions

In [[logic]], logical disjunction is the [[join]] in the [[poset]] of [[truth values]].

Assuming that (as in [[classical logic]]) the only truth values are true ($T$) and false ($F$), then the disjunction $p \vee q$ of the truth values $p$ and $q$ may be defined by a truth table:

|$p$|$q$| |$p \vee q$|
|---|---|-|------------|
|$T$|$T$| |$T$|
|$T$|$F$| |$T$|
|$F$|$T$| |$T$|
|$F$|$F$| |$F$|

That is, $p \vee q$ is true if and only if at least one of $p$ and $q$ is true.  Disjunction also exists in nearly every non-classical logic.

More generally, if $p$ and $q$ are any two [[relations]] on the same domain, then we define their disjunction pointwise, thinking of a relation as a [[function]] to truth values.  If instead we think of a relation as a [[subset]] of its domain, then disjunction becomes [[union]].


## Remarks

Disjunction as defined above is sometimes called __inclusive disjunction__ to distinguish it from [[exclusive disjunction]], where *exactly* one of $p$ and $q$ must be true.

In the context of [[substructural logics]] such as [[linear logic]], we often have both _additive disjunction_ $\oplus$ and _[[multiplicative disjunction]]_ $\parr$; see the [Rules of Inference](#RoI) below for the distinction.  In [[linear logic]], additive disjunction is the [[join]] under the [[entailment]] relation, just like disjunction in [[classical logic]] (and [[intuitionistic logic]]), while multiplicative disjunction is something different.

Disjunction is [[de Morgan dual]] to [[logical conjunction|conjunction]].

Like any join, disjunction is an associative operation, so we can take the disjunction of any finite positive whole number of truth values; the disjunction is true if and only if at least one of the various truth values is true.  Disjunction also has an [[identity element]], which is the [[falsity|false]] truth value.  Some logics allow a notion of infinitary disjunction.  Indexed disjunction is [[existential quantification]].

In [[homotopy type theory]], the disjunction of two [[mere propositions]], $P$ and $Q$, is the [[bracket type]] of their [[sum type]], $\| P + Q \|$. Disjunction types in general could also be regarded as a particular sort of [[higher inductive type]]. In [[Coq]] syntax:

    Inductive disjunction (P Q:Type) : Type :=
    | inl : P -> disjunction P Q
    | inr : Q -> disjunction P Q
    | contr0 : forall (p q : disjunction P Q) p == q

## Classical vs constructive

There are a variety of connectives that are distinct in [[intuitionistic logic]] but are all equivalent to disjunction in [[classical logic]].  Here is a Hasse diagram of some of them, with the strongest statement at the bottom and the weakest at the top (so that each statement entails those above it):
$$ \array {           &          & \neg(\neg{P} \wedge \neg{Q}) \\
                      & &#x21d7; &          & &#x21d6; \\
\neg{P} \rightarrow Q &          &          &          & P \leftarrow \neg{Q} \\
                      & &#x21d6; &          & &#x21d7; \\
                      &          & (\neg{P} \rightarrow Q) \wedge (P \leftarrow \neg{Q}) \\
                      &          & \Uparrow \\
                      &          & P \vee Q } $$
(A single arrow is implication in the object language; a double arrow is entailment in the metalanguage.)  Note that $\neg{P} \wedge \neg{Q}$ is the [[negation]] of every item in this diagram.

In the [[double-negation interpretation]] of classical logic in intuitionistic logic, $\neg(\neg{P} \wedge \neg{Q})$ is the interpretation in intuitionistic logic of disjunction in classical logic.  For this reason, $\neg(\neg{P} \wedge \neg{Q})$ is sometimes called _classical disjunction_.  But this doesn\'t mean that it should always be used when turning classical mathematics into [[constructive mathematics]].  Indeed, a stronger statement is almost always preferable, if one is valid; $\neg(\neg{P} \wedge \neg{Q})$ is merely the fallback position when nothing better can be found.  (And as can be seen in the example in the paragraph after next, sometimes even this is not valid.)

In the [[antithesis interpretation]] of [[affine logic]] in intuitionistic logic, $(\neg{P} \rightarrow Q) \wedge (P \leftarrow \neg{Q})$ is the interpretation of the [[multiplicative disjunction]] $P \parr Q$ for affirmative propositions.  More generally, a statement $P$ in affine logic is interpreted as a pair $(P^+,P^-)$ of mutually contradictory statements in intuitionistic logic; $P^-$ is simply the negation of $P^+$ for affirmative propositions, but in general, $P^-$ only entails $\neg{P^+}$.  Then $P \parr Q$ is interpreted as $\big((P^- \rightarrow Q^+) \wedge (P^+ \leftarrow Q^-), P^- \wedge Q^-\big)$; that is, $(P \parr Q)^+$ is $(P^- \rightarrow Q^+) \wedge (P^+ \leftarrow Q^-)$, and $(P \parr Q)^-$ is $P^- \wedge Q^-$.  (In contrast, the additive disjunction $P \oplus Q$ is interpreted as $(P^+ \vee Q^+, P^- \wedge Q^-)$.  Note that $P \oplus Q$ entails $P \parr Q$ in affine logic, even though they are independent in linear logic.)

For a non-affirmative example, in the arithmetic of (located) [[real numbers]], it is not constructively valid to derive $(a = 0) \vee (b = 0)$ from $a b = 0$, and it\'s not even valid to derive $\neg\big(\neg(a = 0) \wedge \neg(b = 0)\big)$ without [[Markov's principle]] (or at least some weak version of it), but it *is* valid to derive $(a \# 0) \rightarrow (b = 0)$ (and conversely), where $\#$ is the usual [[apartness relation]] between real numbers.  (Here, $P^+$ is $a = 0$ and $P^-$ is $a \# 0$, and similarly for $Q$ and $b$.)  Of course, it\'s also valid to derive $\neg\big((a \# 0) \wedge (b \# 0)\big)$ (which is actually equivalent).


## Rules of inference {#RoI}

The [[rule of inference|rules of inference]] for disjunction in [[sequent calculus]] are dual to those for [[logical conjunction|conjunction]]:
$$ \begin {gathered}
   \frac { \Gamma , p , \Delta \vdash \Sigma ; \; \Gamma , q , \Delta \vdash \Sigma } { \Gamma , p \vee q , \Delta \vdash \Sigma } \; \text {left additive} \\
   \frac { \Gamma \vdash \Delta , p , \Sigma } { \Gamma \vdash \Delta , p \vee q , \Sigma } \; \text {right additive 0} \\
   \frac { \Gamma \vdash \Delta , q , \Sigma } { \Gamma \vdash \Delta , p \vee q , \Sigma } \; \text {right additive 1} \\
\end {gathered} $$

Equivalently, we can use the following rules with weakened contexts:
$$ \begin {gathered}
   \frac { \Gamma , p \vdash \Delta ; \; q , \Sigma \vdash \Pi } { \Gamma , p \vee q , \Sigma \vdash \Delta , \Pi } \; \text {left multiplicative} \\
   \frac { \Gamma \vdash \Delta , p , q , \Sigma } { \Gamma \vdash \Delta , p \vee q , \Sigma } \text {right multiplicative} \\
\end {gathered} $$

The rules above are written so as to remain valid in logics without the [[exchange rule]].  In [[linear logic]], the first batch of sequent rules apply to additive disjunction (interpret $p \vee q$ in these rules as $p \oplus q$), while the second batch of rules apply to multiplicative disjunction (interpret $p \vee q$ in those rules as $p \parr q$).

The [[natural deduction]] rules for disjunction are a little more complicated than those for conjunction:
$$ \begin {gathered}
   \frac { \Gamma , p \vdash r ; \; \Gamma , q \vdash r } { \Gamma , p \vee q \vdash r } \; \text {elimination} \\
   \frac { \Gamma \vdash p } { \Gamma \vdash p \vee q } \; \text {introduction 0} \\
   \frac { \Gamma \vdash q } { \Gamma \vdash p \vee q } \; \text {introduction 1} \\
\end {gathered} $$


## Related concepts

[[!include logic symbols -- table]]


## References

* Landon D. C. Elkind, Richard Zach, _The Genealogy of $\vee$_ ([arXiv:2012.06072](https://arxiv.org/abs/2012.06072))


[[!redirects disjunction]]
[[!redirects logical disjunction]]
[[!redirects inclusive disjunction]]
[[!redirects or]]
[[!redirects inclusive or]]

[[!redirects additive disjunction]]
