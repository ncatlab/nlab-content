
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

In [[natural deduction]] the [[inference rules]] for disjunction are given as 

$$\frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma \vdash Q \; \mathrm{prop}}{\Gamma \vdash P \vee Q \; \mathrm{prop}} \qquad \frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma \vdash Q \; \mathrm{prop}}{\Gamma, P \; \mathrm{true} \vdash P \vee Q \; \mathrm{true}} \qquad \frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma \vdash Q \; \mathrm{prop}}{\Gamma, Q \; \mathrm{true} \vdash P \vee Q \; \mathrm{true}}$$ 

$$\frac{\Gamma \vdash P \; \mathrm{prop} \quad \Gamma \vdash Q \; \mathrm{prop} \quad \Gamma, P \vee Q \; \mathrm{true} \vdash R \; \mathrm{prop} \quad \Gamma, P \; \mathrm{true} \vdash R \; \mathrm{true} \quad \Gamma, Q \; \mathrm{true} \vdash R \; \mathrm{true}}{\Gamma, P \vee Q \; \mathrm{true} \vdash R \; \mathrm{true}}$$ 

## Remarks

Disjunction as defined above is sometimes called __inclusive disjunction__ to distinguish it from [[exclusive disjunction]], where *exactly* one of $p$ and $q$ must be true.

In the context of [[substructural logics]] such as [[linear logic]], we often have both _[[additive disjunction]]_ $\oplus$ and _[[multiplicative disjunction]]_ $\parr$; see the [Rules of Inference](#RoI) below for the distinction.  In [[linear logic]], additive disjunction is the [[join]] under the [[entailment]] relation, just like disjunction in [[classical logic]] (and [[intuitionistic logic]]), while multiplicative disjunction is something different.

Disjunction is [[de Morgan dual]] to [[logical conjunction|conjunction]].

Like any join, disjunction is an associative operation, so we can take the disjunction of any finite positive whole number of truth values; the disjunction is true if and only if at least one of the various truth values is true.  Disjunction also has an [[identity element]], which is the [[falsity|false]] truth value.  Some logics allow a notion of infinitary disjunction.  Indexed disjunction is [[existential quantification]].

## In dependent type theory

In [[dependent type theory]], the disjunction of two [[mere propositions]], $P$ and $Q$, is the [[bracket type]] of their [[sum type]], $\| P + Q \|$. Disjunction types in general could also be regarded as a particular sort of [[higher inductive type]]. In [[Coq]] syntax:

    Inductive disjunction (P Q:Type) : Type :=
    | inl : P -> disjunction P Q
    | inr : Q -> disjunction P Q
    | contr0 : forall (p q : disjunction P Q) p == q

If the [[dependent type theory]] has a [[type of propositions]] $\mathrm{Prop}$, such as the one derived from a type universe $U$ - $\sum_{A:U} \mathrm{isProp}(A)$, then the disjunction of two types $A$ and $B$ is defined as the [[dependent function type]]

$$A \vee B \equiv \prod_{P:\mathrm{Prop}} ((A \to P) \times (B \to P)) \to P$$

By [[weak function extensionality]], the disjunction of two types is a proposition. 

\begin{theorem}
The two definitions above are equivalent. 
\end{theorem}

\begin{proof}
The [[propositional truncation]] of a type $A$ is equivalent to the following dependent function type

$$\| A \| \simeq \prod_{P:\mathrm{Prop}} (A \to P) \to P$$

Substituting the sum type $A + B$ for $A$, we have 

$$\| A + B \| \simeq \prod_{P:\mathrm{Prop}} ((A + B) \to P) \to P$$

Given any type $C$, there is an equivalence 

$$((A + B) \to C) \simeq (A \to C) \times (B \to C)$$
and if $A \simeq B$, then $(A \to C) \simeq (B \to C)$. In addition, for all type families $x:A \vdash B(x)$, and $x:A \vdash C(x)$, if there is a family of equivalences $e:\prod_{x:A} B(x) \simeq C(x)$, then there is an equivalence $\left(\prod_{x:A} B(x)\right) \simeq \left(\prod_{x:A} C(x)\right)$. All this taken together means that there are equivalences 

$$\| A + B \| \simeq \left(\prod_{P:\mathrm{Prop}} ((A + B) \to P) \to P\right) \simeq \left(\prod_{P:\mathrm{Prop}} ((A \to P) \times (B \to P)) \to P\right)$$
\end{proof}

If one has the [[type of booleans]] and the [[existential quantifier]], then the disjunction of two types $A$ and $B$ is given by the following type:

$$A \vee B \coloneqq \exists b:\mathrm{bool}.((b = \mathrm{true}) \to A) \times ((b = \mathrm{false}) \to B)$$

The [[disjunction]] $P \vee Q$ of two [[mere propositions]] $P$ and $Q$ is also the [[join type]] of the two types $P * Q$. This is because every mere proposition is a [[subtype]] of the [[unit type]], and the disjunction of $P$ and $Q$ is the [[union]] of $P$ and $Q$ as two subtypes of the unit types, and the union of $P$ and $Q$ as subtypes of the unit type is defined to be the [[join type]] of $P$ and $Q$, the [[pushout type]] of the two product projection functions from the [[product type]] $P \times Q$ to $P$ and $Q$ respectively. 

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

The definition of the disjunction of two types in dependent type theory as the propositional truncation of the sum type is found in:

* {#UFP13} [[Univalent Foundations Project]], §3.7 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

The definition of the disjunction of two mere propositions in dependent type theory as the [[join type]] of propositions is found in:

* {#Shulman13} [[Mike Shulman]], *Cohomology*, Homotopy type theory blog ([web](http://homotopytypetheory.org/2013/07/24/cohomology/))

And the disjunction of two types defined from the type of propositions and dependent product types can be found in:

* Madeleine Birchfield, *Constructing coproduct types and boolean types from universes*, MathOverflow ([web](https://mathoverflow.net/questions/457904/constructing-coproduct-types-and-boolean-types-from-universes))

[[!redirects disjunction]]
[[!redirects disjunctions]]
[[!redirects logical disjunction]]
[[!redirects inclusive disjunction]]
[[!redirects or]]
[[!redirects inclusive or]]

