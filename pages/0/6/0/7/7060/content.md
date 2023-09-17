
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[type theory]] a _type of propositions_ --- typically denoted  $Prop$ or $\Omega$ --- corresponds, under [[categorical semantics]], roughly to a *[[subobject classifier]]*.  

> (To be precise, depending on the type theoretic rules and axioms this may not be quite true: one needs [[propositional resizing]], [[propositional extensionality]], and --- in some type theories where "proposition" is not defined as an [[h-proposition]], such as the [[calculus of constructions]] --- the [[principle of unique choice]].)

Its generalization from [[propositions]] to general [[types]] is a *[[type universe]]*.

The [[subtypes]] of a [[type]] $A$ may typically be identified with the [[function types]] into the type of propositions

$$
  Sub(A)
  \;\;
  =
  \;\;
  Prop_A
  \;\;
  \equiv
  \;\;
  A \to Prop
  \;\;
  \equiv
  \;\;
  A \to \Omega
  \,.
$$

In [[dependent type theory]] such a $P \,\colon\, A \to Prop$ is equivalently an $A$-[[dependent type|dependent]] [[proposition]], to be understood as assingning to any [[term]] $a \colon A$ the assertion that "$a$ is contained in the given subtype".



## Definition

### The type of all propositions

The **type of all propositions** $\Omega$ in a [[dependent type theory]] could be presented either as a [[Russell universe]] or a [[Tarski universe]]. The difference between the two is that in the former, every [[mere proposition]] in the type theory is literally an element of the type of all propositions, while in the latter, elements of $\Omega$ are only indices of a (-1)-truncated type family $\mathrm{El}$; every [[mere proposition]] in the type theory is only [[essentially small type|essentially $\Omega$-small]] for [[weak Tarski universes]] or [[judgmentally equal]] to an $\mathrm{El}(P)$ for $P:\Omega$ for [[strict Tarski universes]]. 

#### As a Russell universe

As a [[Russell universe]], the type of all propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \Omega \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash A \; \mathrm{type}}$$

Propositional truncation for each type reflection
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(A)}$$

Introduction rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash A:\Omega}$$

Univalence:
$$\frac{\Gamma \vdash A:\Omega \quad \Gamma \vdash B:\Omega} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{Id}_\Omega(A, B) \simeq (A \simeq B)}$$

#### As a Tarski universe

As a [[Tarski universe]], the type of all propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \Omega \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash El(A) \; \mathrm{type}}$$

Propositional truncation for each type reflection
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(El(A))}$$

Introduction rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash A_\Omega:\Omega}$$

[[essentially small type|Essential smallness]] of propositions (for weak types of all propositions) or [[judgmental equality]] (for strict types of all propositions):
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash \delta_A:El(A_\Omega) \simeq A}\mathrm{weak} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash El(A_\Omega) \equiv A \; \mathrm{type}}\mathrm{strict}$$

Univalence:
$$\frac{\Gamma \vdash A:\Omega \quad \Gamma \vdash B:\Omega} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### The empty proposition and falsehood

To ensure that the type of all propositions isn't a [[contractible type]], one could include the following axiom, which states that there exists a proposition satisfying [[ex falso quodlibet]]:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{axempty}:\sum_{\bot:\Omega} \prod_{C:\bot \to \Omega} \mathrm{isContr}\left(\prod_{x:\bot} C(x)\right)}\mathrm{Russell} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{axempty}:\sum_{\bot:\Omega} \prod_{C:\mathrm{El}(\bot) \to \Omega} \mathrm{isContr}\left(\prod_{x:\mathrm{El}(\bot)} \mathrm{El}(C(x))\right)}\mathrm{Tarski}$$

### The type of all decidable propositions

Something similar holds for the **type of all decidable propositions** $\Omega_\mathrm{decidable}$ in a [[dependent type theory]], which could be presented either as a [[Russell universe]] or a [[Tarski universe]]. The difference between the two is that in the former, every [[decidable proposition]] in the type theory is literally an element of the type of all decidable propositions, while in the latter, elements of $\Omega_\mathrm{decidable}$ are only indices of a (-1)-truncated type family $\mathrm{El}$; every [[decidable proposition]] in the type theory is only [[essentially small type|essentially $\Omega_\mathrm{decidable}$-small]] for [[weak Tarski universes]] or [[judgmentally equal]] to an $\mathrm{El}(P)$ for $P:\Omega_\mathrm{decidable}$ for [[strict Tarski universes]]. 

#### As a Russell universe

As a [[Russell universe]], the type of all decidable propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \Omega_\mathrm{decidable} \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash A \; \mathrm{type}}$$

Propositional truncation for each type reflection
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(A)}$$

Excluded middle for each type reflection
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash \mathrm{lem}(A):\mathrm{isProp}(A) \to (A \vee \neg A)}$$

Introduction rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A) \quad \Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to (A \vee \neg A)}{\Gamma \vdash A:\Omega_\mathrm{decidable}}$$

Univalence:
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable} \quad \Gamma \vdash B:\Omega_\mathrm{decidable}} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{Id}_{\Omega_\mathrm{decidable}}(A, B) \simeq (A \simeq B)}$$

#### As a Tarski universe

As a [[Tarski universe]], the type of all decidable propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \Omega_\mathrm{decidable} \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash El(A) \; \mathrm{type}}$$

Propositional truncation for each type reflection
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(El(A))}$$

Excluded middle for each type reflection
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable}}{\Gamma \vdash \mathrm{lem}(A):\mathrm{isProp}(El(A)) \to (El(A) \vee \neg El(A))}$$

Introduction rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A) \quad \Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to A \vee \neg A}{\Gamma \vdash A_\Omega:\Omega_\mathrm{decidable}}$$

[[essentially small type|Essential smallness]] of propositions (for weak types of all decidable propositions) or [[judgmental equality]] (for strict types of all decidable propositions):

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A) \quad \Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to (A \vee \neg A)}{\Gamma \vdash \delta_A:El(A_\Omega) \simeq A}\mathrm{weak} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A) \quad \Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to (A \vee \neg A)}{\Gamma \vdash El(A_\Omega) \equiv A \; \mathrm{type}}\mathrm{strict}$$

Univalence:
$$\frac{\Gamma \vdash A:\Omega_\mathrm{decidable} \quad \Gamma \vdash B:\Omega_\mathrm{decidable}} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

### The type of booleans

The **type of booleans** or **booleans type** is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{bool} \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\mathrm{bool}}{\Gamma \vdash El(A) \; \mathrm{type}}$$

Introduction rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{false}:\mathrm{bool}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \delta_\mathbb{0}:El(\mathrm{false}) \simeq \mathbb{0}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{true}:\mathrm{bool}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \delta_\mathbb{1}:El(\mathrm{true}) \simeq \mathbb{1}}$$

Univalence:
$$\frac{\Gamma \vdash A:\mathrm{bool} \quad \Gamma \vdash B:\mathrm{bool}} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

Unlike a generic [[two-valued type]] defined as the [[sum type]] of two copies of the [[unit type]] or directly defined in terms of natural deduction rules, having a type of booleans is inconsistent with every type being an [[h-proposition]]. If $\mathrm{bool}$ were an h-proposition, that means that the identity type $\mathrm{false} = \mathrm{true}$ is pointed, and by [[transport]] across $\mathrm{El}$, there is an equivalence between the empty type and the unit type, which is a contradiction. 

### Other types of propositions

We work in an [[intensional type theory]] with [[propositional truncations]] $\left[T\right]$ for types $T$. A **type of propositions** is a [[type]] $\Omega$ with a [[type family]] $T$ such that 

* for every proposition $P:\Omega$, the type $T(P)$ is an [[h-proposition]]:
$$\prod_{P:\Omega} \prod_{a:T(P)} \prod_{b:T(P)} a =_{T(P)} b$$
* the [[transport]] function
$$\mathrm{trans}^T(P, Q):P =_\Omega Q \to (T(P) \simeq T(Q))$$
is an equivalence of types for all propositions $P:\Omega$ and $Q:\Omega$
$$\prod_{P:\Omega} \prod_{Q:\Omega} \mathrm{isEquiv}(\mathrm{trans}^T(P, Q))$$
* $(\Omega, T)$ is weakly closed under truth: there is an element $\top_\Omega:\Omega$ and an equivalence $\mathrm{canonical}_\top: T(\top_\Omega) \simeq \mathbb{1}$
* $(\Omega, T)$ is weakly closed under conjunction: there is a function $(-)\wedge(-):\Omega \times \Omega \to \Omega$ and an equivalence $\mathrm{canonical}_\wedge(P, Q): T(P \wedge Q) \simeq \left[T(P) \times T(Q)\right]$
* $(\Omega, T)$ is weakly closed under implication: there is a function $(-)\implies(-):\Omega \times \Omega \to \Omega$ and an equivalence $\mathrm{canonical}_\implies(P, Q): T(P \implies Q) \simeq \left[T(P) \to T(Q)\right]$
* $(\Omega, T)$ is weakly closed under falsehood: there is an element $\bot_\Omega:\Omega$ and an equivalence $\mathrm{canonical}_\bot: T(\bot_\Omega) \simeq \mathbb{0}$
* $(\Omega, T)$ is weakly closed under disjunction: there is a function $(-)\vee(-):\Omega \times \Omega \to \Omega$ and an equivalence $\mathrm{canonical}_\vee(P, Q): T(P \vee Q) \simeq \left[T(P) + T(Q)\right]$

These axioms imply that $(\Omega, T)$ satisfy [[propositional extensionality]] and that $\Omega$ is an [[h-set]] and a [[Heyting algebra]]. 

## Examples

The type of all internal propositions 
$$\sum_{A:U} \mathrm{isProp}(T(A))$$
in a [[Tarski universe]] $(U, T)$ is a type of propositions. If the Tarski universe has all propositions, then 
$$\sum_{A:U} \mathrm{isProp}(T(A))$$
is the type of all propositions. 

## Related concepts

* [[subtype]], [[subobject]]

* [[subobject classifier]]

* [[dominance]]

* [[propositional extensionality]]

* [[type universe]]

* [[type of classes]]

* [[type of strict propositions]]

* [[propositional logic as a dependent type theory]]

## References

Detailed discussion of the type of propositions in [[Coq]] is in

* [[Adam Chlipala]], _[Certified programming with dependent types](http://adam.chlipala.net/cpdt/)_ -- _[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)_ 

[[!redirects type of propositions]]
[[!redirects types of propositions]]

[[!redirects Russell type of propositions]]
[[!redirects Russell types of propositions]]
[[!redirects Tarski type of propositions]]
[[!redirects Tarski types of propositions]]
[[!redirects weak Tarski type of propositions]]
[[!redirects weak Tarski types of propositions]]
[[!redirects strict Tarski type of propositions]]
[[!redirects strict Tarski types of propositions]]

[[!redirects universe of propositions]]
[[!redirects universes of propositions]]
[[!redirects Russell universe of propositions]]
[[!redirects Russell universes of propositions]]
[[!redirects Tarski universe of propositions]]
[[!redirects Tarski universes of propositions]]
[[!redirects weak Tarski universe of propositions]]
[[!redirects weak Tarski universes of propositions]]
[[!redirects strict Tarski universe of propositions]]
[[!redirects strict Tarski universes of propositions]]

[[!redirects type of all propositions]]
[[!redirects types of all propositions]]

[[!redirects Russell type of all propositions]]
[[!redirects Russell types of all propositions]]
[[!redirects Tarski type of all propositions]]
[[!redirects Tarski types of all propositions]]
[[!redirects weak Tarski type of all propositions]]
[[!redirects weak Tarski types of all propositions]]
[[!redirects strict Tarski type of all propositions]]
[[!redirects strict Tarski types of all propositions]]

[[!redirects type of decidable propositions]]
[[!redirects types of decidable propositions]]

[[!redirects Russell type of decidable propositions]]
[[!redirects Russell types of decidable propositions]]
[[!redirects Tarski type of decidable propositions]]
[[!redirects Tarski types of decidable propositions]]
[[!redirects weak Tarski type of decidable propositions]]
[[!redirects weak Tarski types of decidable propositions]]
[[!redirects strict Tarski type of decidable propositions]]
[[!redirects strict Tarski types of decidable propositions]]

[[!redirects type of all decidable propositions]]
[[!redirects types of all decidable propositions]]

[[!redirects Russell type of all decidable propositions]]
[[!redirects Russell types of all decidable propositions]]
[[!redirects Tarski type of all decidable propositions]]
[[!redirects Tarski types of all decidable propositions]]
[[!redirects weak Tarski type of all decidable propositions]]
[[!redirects weak Tarski types of all decidable propositions]]
[[!redirects strict Tarski type of all decidable propositions]]
[[!redirects strict Tarski types of all decidable propositions]]

[[!redirects Prop]]

[[!redirects booleans type]]
[[!redirects type of booleans]]

[[!redirects decidable subset classifier]]