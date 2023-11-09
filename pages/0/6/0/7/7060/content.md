
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

## Predicate logic

In this section, we assume that [[function extensionality]] or [[weak function extensionality]] is true for all dependent function types. 

### The empty type and falsehood

For Russell types of all propositions, the type $\prod_{P:\mathrm{Prop}} P$ is the [[empty type]] $\emptyset$, which by weak function extensionality is a proposition, so is already in the type of all propositions $\left(\prod_{P:\mathrm{Prop}} P\right):\mathrm{Prop}$. Similarly, for Tarski types of all propositions, the type $\prod_{P:\mathrm{Prop}} \mathrm{El}(P)$ is the [[empty type]], which by weak function extensionality is a proposition, and so one has the element $\left(\prod_{P:\mathrm{Prop}} \mathrm{El}(P)\right)_\mathrm{Prop}:\mathrm{Prop}$. 

In either case, the definition implies that if the empty type has an element, then every proposition has an element and is thus contractible. This implies that the empty type represents falsehood $\bot$ in the type of all propositions. 

### Propositional truncations

Given the type of all propositions $\mathrm{Prop}$ and given a type $A$, the [[propositional truncation]] of a type $A$, which turns $A$ into an element of $\mathrm{Prop}$, is given for Russell types of all propositions by the type 

$$[A] \equiv \prod_{P:\mathrm{Prop}} (A \to P) \to P$$

and for Tarski types of all propositions by the type 

$$[A] \equiv \prod_{P:\mathrm{Prop}} (A \to \mathrm{El}(P)) \to \mathrm{El}(P)$$

By weak function extensionality, both of these types are propositions. 

### Universal quantification

Given any type $A$ and family of propositions $P(x)$ indexed by $x:A$, by [[weak function extensionality]], the [[dependent function type]] $\prod_{x:A} P(x)$ is also a [[proposition]]. This means that the propositional truncation of $\prod_{x:A} P(x)$ is equivalent to $\prod_{x:A} P(x)$, and the dependent function type is used as the [[universal quantifier]].

More generally, given any type $A$ and family of propositions $B(x)$ indexed by $x:A$, the universal quantifier is given by [[propositional truncation]] of the [[dependent product type]]:

$$\forall x:A.B(x) \equiv \left[\prod_{x:A} B(x)\right]$$

### Implication and negation

Given any proposition $Q$ and $P$, by [[weak function extensionality]], the [[function type]] $Q \to P$ is also a [[proposition]]. This means that the propositional truncation of $A \to P$ is equivalent to $Q \to P$, and the function type is used as [[implication]]. If $P$ is the empty type or falsehood defined above, then the function type represents the [[negation]] of $Q$, $\neg Q \equiv Q \to \emptyset$. 

More generally, given any type $A$ and $B$, implication is given by [[propositional truncation]] of the [[function type]]:

$$A \implies B \equiv \left[A \to B\right]$$

### Contractible types and truth

Given any proposition $P$, by [[weak function extensionality]], the [[function type]] $P \to P$ is also a [[proposition]]. Since the function type $P \to P$ has an element, given by [[generalized the|the]] [[identity function]] $\mathrm{id}_P \equiv \lambda x:P.x$, $P \to P$ is a [[contractible type]] for any $P:\mathrm{Prop}$, which means that it represents the concept of [[truth]] $\top$. As shown above, $\emptyset \equiv \prod_{P:\mathrm{Prop}} P$ or $\emptyset \equiv \prod_{P:\mathrm{Prop}} \mathrm{El}(P)$ is the empty proposition, so it suffices to define $\top \equiv \emptyset \to \emptyset$. 

### Biconditionals 

Given any proposition $P$ and $Q$, by [[weak function extensionality]], the [[equivalence type]] $P \simeq Q$ is also a [[proposition]]. This means that the propositional truncation of $P \simeq Q$ is equivalent to $P \simeq Q$, and the equivalence type is used as the biconditional. 

More generally, given any type $A$ and $B$, the biconditional is given by [[propositional truncation]] of the [[equivalence type]]:

$$A \iff B \equiv \left[A \simeq B\right]$$

### Existential quantification

Given any type $A$ and family of types $B(x)$ indexed by $x:A$, the [[existential quantifier]] is given by the type 

$$\exists x:A.B(x) \equiv \prod_{P:\mathrm{Prop}} \left(\prod_{x:A} B(x) \to P\right) \to P$$

for Russell types of propositions and
$$\exists x:A.B(x) \equiv \prod_{P:\mathrm{Prop}} \left(\prod_{x:A} B(x) \to \mathrm{El}(P)\right) \to \mathrm{El}(P)$$
for Tarski types of propositions. 

If the type theory also has [[dependent sum types]], the existential quantifier is equivalently given by the propositional truncation of the [[dependent sum type]]

$$\exists x:A.B(x) \equiv \left[\sum_{x:A} B(x)\right]$$

since by [[currying]] there is an equivalence 

$$\left(\left(\sum_{x:A} B(x)\right) \to P\right) \simeq \left(\prod_{x:A} B(x) \to P\right)$$

### Conjunction

Given types $A$ and $B$, the [[conjunction]] of $A$ and $B$ is given by the type 

$$A \wedge B \equiv \prod_{P:\mathrm{Prop}} \left(A \to (B \to P)\right) \to P$$

for Russell types of propositions and
$$A \wedge B \equiv \prod_{P:\mathrm{Prop}} \left(A \to (B \to \mathrm{El}(P))\right) \to \mathrm{El}(P)$$
for Tarski types of propositions. 

If the type theory also has [[product types]], the existential quantifier is equivalently given by the propositional truncation of the [[product type]]

$$A \wedge B \equiv \left[A \times B\right]$$

since by [[currying]] there is an equivalence 

$$\left((A \times B) \to P\right) \simeq \left(A \to (B \to P)\right)$$

### Disjunctions

Given types $A$ and $B$, the [[disjunction]] of $A$ and $B$ is given by the type 

$$A \vee B \equiv \prod_{P:\mathrm{Prop}} (A \to P) \to (B \to P) \to P$$

for Russell types of propositions and
$$A \vee B \equiv \prod_{P:\mathrm{Prop}} (A \to \mathrm{El}(P)) \to (B \to \mathrm{El}(P)) \to \mathrm{El}(P)$$
for Tarski types of propositions. 

If the type theory also has [[product types]], the existential quantifier is equivalently given by the type

$$A \vee B \equiv \prod_{P:\mathrm{Prop}} ((A \to P) \times (B \to P)) \to P$$

for Russell types of propositions and
$$A \vee B \equiv \prod_{P:\mathrm{Prop}} ((A \to \mathrm{El}(P)) \times (B \to \mathrm{El}(P))) \to \mathrm{El}(P)$$
for Tarski types of propositions, 

and if the type theory also has [[coproduct types]], the existential quantifier is equivalently given by the propositional truncation of the [[coproduct type]]

$$A \vee B \equiv \left[A + B\right]$$

since by [[currying]] there is an equivalence 

$$\left((A \to P) \times (B \to P)\right) \simeq \left((A + B) \to P\right)$$

### Decidable propositions and booleans

A [[decidable proposition]] is a proposition $P$ with a witness $p:P \vee \neg P$ that the disjunction of $P$ and its negation holds. 

The [[type of booleans]] is the type of all decidable propositions in $\mathrm{Prop}$, 
$$\mathrm{Bool} \equiv \sum_{P:\mathrm{Prop}} P \vee \neg P$$
for Russell types of propositions, and 
$$\mathrm{Bool} \equiv \sum_{P:\mathrm{Prop}} \mathrm{El}(P) \vee \neg \mathrm{El}(P)$$
for Tarski types of propositions. 

The [[law of excluded middle]] states that every proposition is decidable $\mathrm{lem}:\prod_{P:\mathrm{Prop}} P \vee \neg P$, or equivalently that there is an equivalence $\mathrm{lem}':\mathrm{Bool} \simeq \mathrm{Prop}$ between the type of propositions and the type of booleans. 

## Categorical semantics

The [[categorical semantics]] of the type of all propositions is the [[subobject classifier]]. 

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

* {#UFP13} [[Univalent Foundations Project]], *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

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