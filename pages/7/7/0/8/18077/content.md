
\tableofcontents

## Definition

The **law of double negation** is the statement that the [[double negation]] of a [[proposition]] [[implication|implies]] that proposition

$$
  \not \not A \Rightarrow A
  \,.
$$

equivalently, that the double negation of a [[proposition]] is [[logically equivalent]] to that proposition:

$$
  \not \not A \iff A
  \,.
$$

In [[classical logic]], this is simply true.  In [[constructive logic]], it is equivalent to the law of [[excluded middle]] (because $\not \not (P \vee \not P)$ is a constructive theorem), and is not assertable in general.

## In dependent type theory

In [[dependent type theory]], we define the [[negation]] of a type $A$ as the function type from $A$ to the empty type $\mathbb{0}$; $\neg A \coloneqq A \to \mathbb{0}$. The law of double negation states that given a type $A$, one could derive that one could get an element of $A$ in the context of a witness that $A$ is an [[h-proposition]] and a witness of the double negation of $A$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isProp}(A), c:\neg \neg A \vdash \mathrm{doubleneg}_A(p, c):A}$$

Given [[function types]], this could be wrapped up as

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{doubleneg}_A:\mathrm{isProp}(A) \to (\neg \neg A \to A)}$$

The requirement that $A$ be an [[h-proposition]] is necessary; the law of double negation for [[h-sets]] is the [[set-theoretic choice operator]], which implies the [[set-theoretic axiom of choice]] in addition to [[excluded middle]], and the law of double negation for general [[types]] is the [[type-theoretic choice operator]], which implies [[UIP]] in addition to the set-theoretic axiom of choice and excluded middle. 

If one additionally has a [[Russell type of all propositions]] $\Omega$ or a [[Tarski type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, the law of double negation could be expressed as an axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} (\neg \neg P) \to P}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} (\neg \neg \mathrm{El}_\Omega(P)) \to \mathrm{El}_\Omega(P)}\mathrm{Tarski}$$

There is an alternative presentation of the law of double negation, which uses an [[equivalence type]] for [[logical equivalence]] rather than a [[function type]] for [[implication]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{doubleneg}_A:\mathrm{isProp}(A) \to ((\neg \neg A) \simeq A)}$$

In [[dependent type theory]] as [[foundations of mathematics]], the requirement that $A$ be an [[h-proposition]] is also necessary. This alternate law of double negation for general [[types]] implies that all types are [[h-propositions]] a la [[propositional logic as a dependent type theory]], since the double negation of a type is always an [[h-proposition]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{doubleneg}_A:(\neg \neg A) \simeq A}$$

Similarly, if one additionally has a [[Russell type of all propositions]] $\Omega$ or a [[Tarski type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, this alternate law of double negation could be expressed as an axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} (\neg \neg P) \simeq P}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{doubleneg}:\prod_{P:\Omega} (\neg \neg \mathrm{El}_\Omega(P)) \simeq \mathrm{El}_\Omega(P)}\mathrm{Tarski}$$

## Related concepts

* [[excluded middle]]

* [[ex falso quodlibet]]

* [[closed subspace]]

* [[type-theoretic law of double negation]]

## References

* [[eom]], _[Double negation, law of](https://www.encyclopediaofmath.org/index.php/Double_negation,_law_of)_


[[!redirects law of double negation]]
[[!redirects double negation law]]
[[!redirects principle of double negation]]
[[!redirects double negation principle]]
[[!redirects axiom of double negation]]
[[!redirects double negation axiom]]

[[!redirects choice operator for propositions]]
[[!redirects choice operator for h-propositions]]
[[!redirects choice operator for mere propositions]]