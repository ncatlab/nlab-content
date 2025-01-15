
\tableofcontents

## Definition

In the [[antithesis interpretation]] of [[affine logic]] into [[constructive mathematics]], an affine proposition $P$ is interpreted as a pair $(P^+, P^-)$ of propositions in intuitionistic logic which are mutually exclusive in that $\neg (P^+ \wedge P^-)$ holds. Thus, given a [[type of propositions]] $(\mathrm{Prop}, \mathrm{El})$, we can define the **type of affine propositions** as the type 
$$\mathrm{Prop}_\pm \coloneqq \sum_{P^+:\mathrm{Prop}} \sum_{P^-:\mathrm{Prop}} \mathrm{El}(\neg (P^+ \wedge P^-))$$ 

Similarly, an affine predicate $P$ on a type $A$ is interpreted as a pair $(P^+, P^-)$ of predicates on $A$ in intuitionistic logic which are pointwise mutually exclusive in that $\neg (P^+(x) \wedge P^-(x))$ holds for all $x:A$. This is equivalently a function $P:A \to \mathrm{Prop}_\pm$. 

## Predicate logic

We have the following propositional and predicate affine logical operations:

* [[truth]] is an element of $\mathrm{Prop}_\pm$ defined as

$$1 \coloneqq (\top, \bot)$$

We say that an affine proposition $P$ holds if there is an element $p:P =_{\mathrm{Prop}_\pm} 1$

* [[falsehood]] is an element of $\mathrm{Prop}_\pm$ defined a

$$0 \coloneqq (\bot, \top)$$

* [[additive conjunction]] is a function from $\mathrm{Prop}_\pm \times \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-) \sqcap (Q^+, Q^-) \coloneqq (P^+ \wedge Q^+, P^- \vee Q^-)$$

* [[additive disjunction]] is a function from $\mathrm{Prop}_\pm \times \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-) \sqcup (Q^+, Q^-) \coloneqq (P^+ \vee Q^+, P^- \wedge Q^-)$$

* [[multiplicative conjunction]] is a function from $\mathrm{Prop}_\pm \times \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-) \boxtimes (Q^+, Q^-) \coloneqq (P^+ \wedge Q^+, (P^+ \Rightarrow Q^-) \wedge (Q^+ \Rightarrow P^-))$$

* [[multiplicative disjunction]] is a function from $\mathrm{Prop}_\pm \times \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-) \boxplus (Q^+, Q^-) \coloneqq ((P^- \Rightarrow Q^+) \wedge (Q^- \Rightarrow P^+), P^- \wedge Q^-)$$

* [[linear implication]] is a function from $\mathrm{Prop}_\pm \times \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-) \multimap (Q^+, Q^-) \coloneqq ((P^+ \Rightarrow Q^+) \wedge (Q^- \Rightarrow P^-), P^+ \wedge Q^-)$$

* [[linear negation]] is a function from $\mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$(P^+, P^-)^\bot \coloneqq (P^-, P^+)$$
* the linear [[existential quantifier]] for a type $A$ is a function from $A \to \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$\bigsqcup_{x:A} (P^+(x), P^-(x)) \coloneqq (\exists x:A.P^+(x), \forall x:A.P^-(x))$$

* the linear [[universal quantifier]] for a type $A$ is a function from $A \to \mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$\bigsqcap_{x:A} (P^+(x), P^-(x)) \coloneqq (\forall x:A.P^+(x), \exists x:A.P^-(x))$$

* [[exponential conjunction]] is a function from $\mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$!(P^+, P^-) \coloneqq (P^+, \neg P^+)$$

* [[exponential disjunction]] is a function from $\mathrm{Prop}_\pm$ to $\mathrm{Prop}_\pm$ defined as

$$?(P^+, P^-) \coloneqq (\neg P^-, P^-)$$

### Affirmative and refutative propositions

An affine proposition is **affirmative** if we have $!(P) = P$ and an affine proposition is **refutative** if we have $?(P) = P$. Affirmative propositions consist of an intuitionistic proposition and its negation, and refutative propositions are the affine negation of an affirmative proposition. As a result, we have equivalences of types

$$\mathrm{Prop} \simeq \sum_{P:\Omega_\pm} !(P) =_{\Omega_\pm} P \qquad \mathrm{Prop} \simeq \sum_{P:\Omega_\pm} ?(P) =_{\Omega_\pm} P$$

Given an affirmative proposition $P$, the intuitionistic [[negation]] of $P$ is given by $\neg P \coloneqq !(P^\bot)$, and given a refutative proposition $P$, the intuitionistic [[negation]] of $P$ is given by $\neg P \coloneqq ?(P^\bot)$. 

### Decidable propositions

An affine proposition $P$ is **decidable** if $P \sqcup P^\bot = 1$. The type of all decidable affine propositions is equivalent to the [[boolean domain]]

$$\mathrm{bool} \simeq \sum_{P:\Omega_\pm} P \sqcup P^\bot =_{\Omega_\pm} 1$$

### Properties

The [[exponential conjunction]] and [[exponential disjunction]] can be defined entirely in terms of the [[multiplicative disjunction]] and [[multiplicative conjunction]] respectively:

$$!P \coloneqq P \boxtimes P \quad ?P \coloneqq P \boxplus P$$

### Excluded middle

Suppose that the [[law of excluded middle]] holds in the [[intuitionistic logic]], so that the logic becomes [[classical logic]]. Then $\mathrm{Prop}$ is equivalent to the [[boolean domain]] $\mathbb{2}$, and $\mathrm{Prop}_\pm$ is equivalent to the three-element set $\{(\top, \bot), (\bot, \bot), (\bot, \top)\}$ representing the propositions in [[Łukasiewicz logic]]. As a result, the affine predicate logic in the antithesis interpretation becomes predicate Łukasiewicz logic. The affirmative and refutative affine propositions are all decidable. 

The law of excluded middle can be expressed in the affine logic as 

$$!P =_{\Omega_\pm} P \sqcup P \; \mathrm{or} \; ?P =_{\Omega_\pm} P \sqcap P$$

## Related concepts

* [[type of propositions]]

* [[antithesis interpretation]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects affine proposition]]
[[!redirects affine propositions]]

[[!redirects type of affine propositions]]
[[!redirects types of affine propositions]]