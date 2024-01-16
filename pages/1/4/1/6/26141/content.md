
\tableofcontents

## Idea

A version of [[propositional truncation]] which takes types and turns them into [[strict propositions]].

## Definition

### Direct definition

Provided that [[function types]] and [[dependent function types]] have [[judgmental equality|judgmental]] [[computation rules]], given a [[type of strict propositions]] $\mathrm{sProp}$, the squash type could be defined in the same manner as [[propositional truncations]]:

$$[A]_s \coloneqq \prod_{P:\mathrm{sProp}} (A \to P) \to P$$

### Inference rules

Without a [[type of strict propositions]] $\mathrm{sProp}$, or if either [[function types]] or [[dependent function types]] only have [[typal equality|typal]] [[computation rules]], the squash type would have to be defined  using [[inference rules]].

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash [A]_s \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A]_s, y:[A]_s \vdash x \equiv y:[A]_s} \qquad \frac{\Gamma \vdash x:A}{\Gamma \vdash \mathrm{squash}(x):[A]_s}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash P \; \mathrm{type} \quad \Gamma, p:P, q:P \vdash p \equiv q:P \quad \Gamma \vdash f:A \to P \quad \Gamma \vdash x:[A]_s}{\Gamma \vdash \mathrm{unsquash}_P(f, x):P}$$

Similarly to [[propositional truncations]], the recursion rule for squash types is sufficient to define the induction rule for squash types. 

## Related concepts

* [[judgmental equality]]

* [[propositional truncation]]

* [[strict proposition]]

* [[type of strict propositions]]

## References

* [[Gaëtan Gilbert]], [[Jesper Cockx]], [[Matthieu Sozeau]], [[Nicolas Tabareau]], *Definitional Proof-Irrelevance without K*. Proceedings of the ACM on Programming Languages, Volume 3, Issue POPL, Article 3, pp 1–28, January 2019. ([doi:10.1145/3290316](https://doi.org/10.1145/3290316))

[[!redirects squash type]]
[[!redirects squash types]]