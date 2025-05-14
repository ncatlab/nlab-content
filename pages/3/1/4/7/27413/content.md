
\tableofcontents

## Definition

Recall that propositions $P$ and $Q$ are [[mutually exclusive propositions|mutually exclusive]] if and only if $\neg (P \wedge Q)$ holds. Given a [[type of propositions]] $(\mathrm{Prop}, \mathrm{El})$, the **type of [[mutually exclusive propositions]]** is given by the type 
$$\mathrm{Prop}_\pm \coloneqq \sum_{P^+:\mathrm{Prop}} \sum_{P^-:\mathrm{Prop}} \mathrm{El}(\neg (P^+ \wedge P^-))$$ 

We denote the two projection functions as $(-)^+:\mathrm{Prop}_\pm \to \mathrm{Prop}$ and $(-)^-:\mathrm{Prop}_\pm \to \mathrm{Prop}$. 

In the [[antithesis interpretation]] of [[affine logic]] into [[constructive mathematics]], an affine proposition $P$ is interpreted as a pair $(P^+, P^-)$ of mutually exclusive propositions. Similarly, an affine predicate $P$ on a type $A$ is interpreted as a pair $(P^+, P^-)$ of predicates on $A$ in intuitionistic logic which are pointwise mutually exclusive in that $\neg (P^+(x) \wedge P^-(x))$ holds for all $x:A$. This is equivalently a function $P:A \to \mathrm{Prop}_\pm$. 

## Affine logic of mutually exclusive propositions

We have the following propositional and predicate [[affine logic|affine]] logical operations on mutually exclusive propositions:

* [[truth]] is an element of $\mathrm{Prop}_\pm$ defined as

$$1 \coloneqq (\top, \bot)$$

We say that a pair of mutually exclusive propositions $(P^+, P^-)$ holds if there is an element $p:(P^+, P^-) =_{\mathrm{Prop}_\pm} 1$

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

### Affirmation, refutation, and stability

A pair of mutually exclusive propositions is **affirmative** if we have $!(P^+, P^-) = (P^+, P^-)$ and a pair of mutually exclusive propositions is **refutative** if we have $?(P^+, P^-) = (P^+, P^-)$. By definition, affirmative pairs consist of an intuitionistic proposition and its negation, and refutative pairs are the affine negation of an affirmative pair. As a result, we have equivalences of types

$$\mathrm{Prop} \simeq \sum_{P:\Omega_\pm} !(P) =_{\Omega_\pm} P \qquad \mathrm{Prop} \simeq \sum_{P:\Omega_\pm} ?(P) =_{\Omega_\pm} P$$

Given an affirmative pair $P$, the intuitionistic [[negation]] of $P$ is given by $\neg P \coloneqq !(P^\bot)$, and given a refutative pair $P$, the intuitionistic [[negation]] of $P$ is given by $\neg P \coloneqq ?(P^\bot)$. 

A pair of mutually exclusive propositions is **[[stable proposition|stable]]**  if $!(P^+, P^-) =_{\Omega_\pm} ?(P^+, P^-)$. This automatically implies that $P^+ =_\Omega \neg P^-$ and $\neg P^+ =_\Omega P^-$ by definition of [[exponential conjunction]] and [[exponential disjunction]], which in turn implies that $P^+ =_\Omega \neg \neg P^+$ and $P^- =_\Omega \neg \neg P^-$, hence the term *stable*. 

### Decidable propositions

A pair of mutually exclusive propositions $P$ is **decidable** if $P \sqcup P^\bot = 1$. The type of all decidable pairs of mutually exclusive propositions is equivalent to the [[type of booleans]]

$$\mathrm{bool} \simeq \sum_{P:\Omega_\pm} P \sqcup P^\bot =_{\Omega_\pm} 1$$

### Properties

The [[exponential conjunction]] and [[exponential disjunction]] can be defined entirely in terms of the [[multiplicative disjunction]] and [[multiplicative conjunction]] respectively:

$$!P \coloneqq P \boxtimes P \quad ?P \coloneqq P \boxplus P$$

The type of mutually exclusive propositions is a [[De Morgan algebra]] where the [[distributive lattice]] structure is given by the [[additive conjunction]] and [[additive disjunction]] of the [[affine logic]] of mutually exclusive propositions, and the [[involution]] is given by the [[linear negation]]. 

### Excluded middle

Suppose that the [[law of excluded middle]] holds in the [[intuitionistic logic]], so that the logic becomes [[classical logic]]. Then $\mathrm{Prop}$ is equivalent to the [[type of booleans]] $\mathbb{2}$, and $\mathrm{Prop}_\pm$ is equivalent to the three-element set $\{(\top, \bot), (\bot, \bot), (\bot, \top)\}$ representing the propositions in [[Łukasiewicz logic]]. As a result, the affine predicate logic in the antithesis interpretation becomes predicate Łukasiewicz logic. The affirmative and refutative pairs of mutually exclusive propositions are all decidable. 

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

[[!redirects type of mutually exclusive propositions]]
[[!redirects types of mutually exclusive propositions]]
