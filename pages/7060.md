
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

#Contents#
* table of contents
{:toc}

## Idea

In [[type theory]] a _type of propositions_ $Prop$ or $\Omega$ corresponds roughly under [[categorical semantics]] to a [[subobject classifier]].  (To be precise, depending on the type theoretic rules and axioms this may not be quite true: one needs [[propositional resizing]], [[propositional extensionality]], and --- in some type theories where "proposition" is not defined as an [[h-proposition]], such as the [[calculus of constructions]] --- the [[principle of unique choice]].)

Its generalization from [[propositions]] to general [[types]] is the [[type universe]]. 

## Definition

### The type of all propositions

The type of all propositions is given by the following rules:

Formation rules:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \Omega \; \mathrm{type}}$$

Type reflection:
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash El(A) \; \mathrm{type}}$$

Introduction rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash A_\Omega:\Omega}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \mathrm{proptrunc}_A:\mathrm{isProp}(A)}{\Gamma \vdash El(A_\Omega) \equiv A}$$

Propositional truncation for each type reflection
$$\frac{\Gamma \vdash A:\Omega}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(El(A))}$$

Univalence:
$$\frac{\Gamma \vdash A:\Omega \quad \Gamma \vdash B:\Omega} {\Gamma \vdash \mathrm{univalence}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

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
in a [[Tarski universe]] $(U, T)$ is a type of propositions. 

## Related concepts

* [[propositional extensionality]]

* [[subobject classifier]]

* [[type universe]]

* [[propositional logic as a dependent type theory]]

## References

Detailed discussion of the type of propositions in [[Coq]] is in

* [[Adam Chlipala]], _[Certified programming with dependent types](http://adam.chlipala.net/cpdt/)_ -- _[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)_ 

[[!redirects types of propositions]]
[[!redirects universe of propositions]]

[[!redirects Prop]]

