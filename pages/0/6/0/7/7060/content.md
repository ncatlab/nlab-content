
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

### Other types of propositions

Other types of propositions include 

* the [[boolean domain]], which is the type of *decidable propositions*.

* any [[dominance]], which is the type of *open propositions*, or the type of *semi-decidable propositions*. 

* For a [[Russell universe]] $U$, the type $\sum_{A:U} \mathrm{isProp}(A)$ is the type of *$U$-small propositions*. Similarly, for a [[Tarski universe]] $(U, T)$, the type $\sum_{A:U} \mathrm{isProp}(T(A))$ is the type of *$U$-small propositions*

* [[sProp]], which is the *type of strict propositions*

* any [[contractible type]], which is (equivalent to) the *type of pointed propositions* or the *type of contractible types*. 

In general, these types of propositions can also be distinguished between their Russell and Tarski variants, where elements of the type of propositions are actual types, or indices for the type family $\mathrm{El}$. 

Most generally, a **type of propositions** is a [[type]] $\Omega$ with a [[type family]] $T$ such that 

* for every elements $P:\Omega$, the type $T(P)$ is an [[h-proposition]]:
$$\prod_{P:\Omega} \prod_{a:T(P)} \prod_{b:T(P)} a =_{T(P)} b$$
* the [[transport]] function
$$\mathrm{trans}^T(P, Q):P =_\Omega Q \to (T(P) \simeq T(Q))$$
is an equivalence of types for all elements $P:\Omega$ and $Q:\Omega$
$$\prod_{P:\Omega} \prod_{Q:\Omega} \mathrm{isEquiv}(\mathrm{trans}^T(P, Q))$$

These axioms imply that $(\Omega, T)$ satisfy [[propositional extensionality]] and thus that $\Omega$ is an [[h-set]] 

## Properties

### The empty type and falsehood

Assuming [[weak function extensionality]], for Russell types of all propositions, the type $\prod_{P:\mathrm{Prop}} P$ is the [[empty type]], which by weak function extensionality is a proposition, so is already in the type of all propositions $\left(\prod_{P:\mathrm{Prop}} P\right):\mathrm{Prop}$. Similarly, for Tarski types of all propositions, the type $\prod_{P:\mathrm{Prop}} \mathrm{El}(P)$ is the [[empty type]], which by weak function extensionality is a proposition, and so one has the element $\left(\prod_{P:\mathrm{Prop}} \mathrm{El}(P)\right)_\mathrm{Prop}:\mathrm{Prop}$. 

In either case, the definition implies that if the empty type has an element, then every proposition has an element and is thus contractible. 

### Propositional truncations

Assuming [[weak function extensionality]], given the type of all propositions $\mathrm{Prop}$ and given a type $A$, the [[propositional truncation]] of a type $A$, which turns $A$ into an element of $\mathrm{Prop}$, is given for Russell types of all propositions by the type 

$$\prod_{P:\mathrm{Prop}} (A \to P) \to P$$

and for Tarski types of all propositions by the type 

$$\prod_{P:\mathrm{Prop}} (A \to \mathrm{El}(P)) \to \mathrm{El}(P)$$

## Related concepts

* [[boolean domain]]

* [[subtype]], [[subobject]]

* [[subobject classifier]]

* [[dominance]]

* [[propositional extensionality]]

* [[type universe]]

* [[type of classes]]

* [[type of strict propositions]]

* [[propositional logic as a dependent type theory]]

* [[type of entire relations]]

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

[[!redirects Prop]]