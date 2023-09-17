
\tableofcontents

## Idea

In [[dependent type theory]] the type $\mathrm{sProp}$ is a type of [[strict propositions]]. 

The type of strict proposition is used to formalize [[logic over type theory]] in [[dependent type theory]] without having to postulate a separate proposition judgment, since strict propositions are judgmentally proof irrelevant, and thus behave as propositions in traditional [[propositional logic]]. 

## Definition

### The type of all strict propositions

The **type of all strict propositions** $\mathrm{sProp}$ in a [[dependent type theory]] could be presented either as a [[Russell universe]] or a [[Tarski universe]]. The difference between the two is that in the former, every [[strict proposition]] in the type theory is literally an element of the type of all strict propositions, while in the latter, elements of $\mathrm{sProp}$ are only indices of a type family $\Box$ of strict propositions; every [[strict proposition]] in the type theory is only [[essentially small type|essentially $\mathrm{sProp}$-small]] for [[weak Tarski universes]] or [[judgmentally equal]] to an $\Box P$ for $P:\mathrm{sProp}$ for [[strict Tarski universes]]. 

#### As a Russell universe

As a [[Russell universe]], the type of all strict propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{sProp} \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\mathrm{sProp}}{\Gamma \vdash A \; \mathrm{type}}$$

Strictness for each type reflection
$$\frac{\Gamma \vdash A:\mathrm{sProp}}{\Gamma, x:A, y:A \vdash x \equiv y:A}$$

Introduction rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash x \equiv y:A}{\Gamma \vdash A:\mathrm{sProp}}$$

Univalence:
$$\frac{\Gamma \vdash A:\mathrm{sProp} \quad \Gamma \vdash B:\mathrm{sProp}} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{Id}_\mathrm{sProp}(A, B) \simeq (A \simeq B)}$$

#### As a Tarski universe

As a [[Tarski universe]], the type of all propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{sProp} \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\mathrm{sProp}}{\Gamma \vdash \Box A \; \mathrm{type}}$$

Strictness for each type reflection
$$\frac{\Gamma \vdash A:\mathrm{sProp}}{\Gamma, x:A, y:A \vdash x \equiv y:A}$$

Introduction rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash x \equiv y:A}{\Gamma \vdash A_\Omega:\mathrm{sProp}}$$

[[essentially small type|Essential smallness]] of propositions (for weak types of all propositions) or [[judgmental equality]] (for strict types of all propositions):
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash x \equiv y:A}{\Gamma \vdash \delta_A:\Box A_\Omega \simeq A}\mathrm{weak} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash x \equiv y:A}{\Gamma \vdash \Box A_\Omega \equiv A \; \mathrm{type}}\mathrm{strict}$$

Univalence:
$$\frac{\Gamma \vdash A:\mathrm{sProp} \quad \Gamma \vdash B:\mathrm{sProp}} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\box(A, B))}$$

## Related concepts

* [[judgmental equality]]

* [[type of propositions]]

* [[strict proposition]]

* [[squash type]]

## References

* [[Gaëtan Gilbert]], [[Jesper Cockx]], [[Matthieu Sozeau]], [[Nicolas Tabareau]], *Definitional Proof-Irrelevance without K*. Proceedings of the ACM on Programming Languages, Volume 3, Issue POPL, Article 3, pp 1–28, January 2019. ([doi:10.1145/3290316](https://doi.org/10.1145/3290316))

[[!redirects sProp]]

[[!redirects type of strict propositions]]
[[!redirects types of strict propositions]]

[[!redirects type of all strict propositions]]
[[!redirects types of all strict propositions]]