
> This article is about the [[type]] of [[h-propositions]] in [[dependent type theory]]. For the [[symmetric monoidal category]], see [[PROP]]. 

---

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

In [[dependent type theory]] the _type of propositions_ --- typically denoted $Prop$ or $\Omega$ --- corresponds, under [[categorical semantics]], roughly to a *[[subobject classifier]]*.  

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

There are many different ways of defining the [[isProp]] [[modality]] in dependent type theory. Some of them include

$$\mathrm{isProp}(A) \coloneqq \prod_{x:A} \prod_{y:A} x =_A y$$
$$\mathrm{isProp}(A) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{isContr}(x =_A y)$$
$$\mathrm{isProp}(A) \coloneqq A \to \mathrm{isContr}(A)$$

We shall be agnostic about the different definitions of $\mathrm{isProp}(A)$, and just directly use $\mathrm{isProp}(A)$. 

The **type of (all) propositions** $\mathrm{Prop}$ in a [[dependent type theory]] could be defined in many different ways:

* in [[dependent type theory with type variables]] and [[impredicative polymorphism]], as a [[positive type|positive]] [[higher inductive-inductive type]] representing the homotopy-[[initial object|initial]] [[frame]] or [[complete Heyting algebra]]. 

* as a homotopy-[[terminal object|terminal]] [[univalent Tarski universe]] of [[h-propositions]], suitably defined. 

* as a [[record type with type fields]], with [[inference rules]] that mimic that of the [[negative type|negative]] [[dependent sum type]] $\sum_{P:U} \mathrm{isProp}(P)$ or $\sum_{P:U} \mathrm{isProp}(T(P))$ respectively, but for all types, not just the $U$-small types. 

In addition, in [[dependent type theory]] defined using a [[universe hierarchy]] instead of a separate type judgment, a universe $U_i$ having the type of all propositions as defined above is equivalent to a local [[propositional resizing]] axiom which says that the [[locally small type|locally $U_i$-small type]] $\sum_{P:U_i} \mathrm{isProp}(P)$ is ([[essentially small type|essentially]]) [[small type|$U_i$-small]]. 

### As a homotopy-initial type

Suppose that the dependent type theory has [[type variables]] and [[impredicative polymorphism]]. Then the **type of (all) propositions** can be defined as any of the following [[higher inductive-inductive types]]:

* As the (homotopy)-initial [[frame]] $\mathrm{Prop}$

* As the (homotopy)-initial [[complete Heyting algebra]] $\mathrm{Prop}$

since these structures can only be defined with [[impredicative polymorphism]] in the absence of an already pre-existing type of all propositions. The Tarski universe type family $P:\mathrm{Prop} \vdash \mathrm{El}(P)$ is given by [[identification]] with [[truth]]

$$\mathrm{El}(P) \coloneqq (P =_{\mathrm{Prop}} \top)$$

and the Tarski universe is univalent by concatenation of identifications in the frame. 

### As a homotopy-terminal type

A **univalent Tarski universe of propositions** consists of a type $A$ and a type family $(B(x))_{x:A}$ such that 

* $B(x)$ is a [[mere proposition]] for all $x:A$,

* the [[transport]] function
$$\mathrm{tr}^B(x, y):x =_A y \to (B(x) \simeq B(y))$$
is an [[equivalence of types]] for all $x:A$ and $y:A$

A morphism of univalent Tarski universe of propositions between Tarski universes of propositions $(A, B)$ and $(A', B')$ consists of a function $f_A:A \to A'$ and a family of functions $f_B(x):B(x) \to B'(f_A(x))$.  

The **type of (all) propositions** $(\mathrm{Prop}, \mathrm{El})$ is the homotopy-terminal univalent Tarski universe of propositions: given any other univalent Tarski universe of propositions $(A, B)$, there exists a unique function $u_A:A \to \mathrm{Prop}$ and a unique family of functions $u_B(x):B(x) \to \mathrm{El}(u_A(x))$. 

### As a record type with type fields

The **type of (all) propositions** $\mathrm{Prop}$ is a [[record type]] where one of the fields is a [[type]], consisting of 

* a type $A \; \mathrm{type}$

* a witness $p:\mathrm{isProp}(A)$ that $A$ is a [[mere proposition]]. 

As a result, the type of all propositions behaves as a [[type universe]]. 

Similar to other [[type universes]] and [[record types with type fields]], the type of all propositions can be presented [[a la Tarski]] or [[a la Russell]]

#### A la Tarski

The type of all propositions [[a la Tarski]] is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all propositions:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Prop} \; \mathrm{type}}$$

Introduction rules for the type of all propositions:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toProp}_A:\mathrm{isProp}(A) \to \mathrm{Prop}}$$

Elimination rules for the type of all propositions:
$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(\mathrm{El}(A))}$$

Computation rules for the type of all propositions:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{El}(\mathrm{toProp}_A(p)) \equiv A \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{proptrunc}(\mathrm{toProp}_A(p)) \equiv p:\mathrm{isProp}(A)}$$

Uniqueness rules for the type of all propositions:

$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash A \equiv \mathrm{toProp}_{\mathrm{El}(A)}(\mathrm{proptrunc}(A)):\mathrm{Prop}}$$

Extensionality principle of the type of all propositions:
$$\frac{\Gamma \vdash A:\mathrm{Prop} \quad \Gamma \vdash B:\mathrm{Prop}} {\Gamma \vdash \mathrm{ext}_\mathrm{Prop}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### A la Russell

The type of all propositions [[a la Russell]] is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all propositions:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Prop} \; \mathrm{type}}$$

Introduction rules for the type of all propositions:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toProp}_A:\mathrm{isProp}(A) \to \mathrm{Prop}}$$

Elimination rules for the type of all propositions:
$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{isProp}(A)}$$

Computation rules for the type of all propositions:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{toProp}_A(p) \equiv A \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{proptrunc}(\mathrm{toProp}_A(p)) \equiv p:\mathrm{isProp}(A)}$$

Uniqueness rules for the type of all propositions:

$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash A \equiv \mathrm{toProp}_{A}(\mathrm{proptrunc}(A)):\mathrm{Prop}}$$

Extensionality principle for the type of all propositions:
$$\frac{\Gamma \vdash A:\mathrm{Prop} \quad \Gamma \vdash B:\mathrm{Prop}} {\Gamma \vdash \mathrm{ext}_\mathrm{Prop}(A, B):(A =_\mathrm{Prop} B) \simeq (A \simeq B)}$$

## Predicate logic

In this section, we assume that [[function extensionality]] or [[weak function extensionality]] is true for all dependent function types. 

### The empty type and falsehood

For Russell types of all propositions, the type $\prod_{P:\mathrm{Prop}} P$ is the [[empty type]] $\emptyset$, which by weak function extensionality is a proposition, so is already in the type of all propositions $\left(\prod_{P:\mathrm{Prop}} P\right):\mathrm{Prop}$. Similarly, for Tarski types of all propositions, the type $\prod_{P:\mathrm{Prop}} \mathrm{El}(P)$ is the [[empty type]], which by weak function extensionality is a proposition, and so one has the element $\left(\prod_{P:\mathrm{Prop}} \mathrm{El}(P)\right)_\mathrm{Prop}:\mathrm{Prop}$. 

In either case, the definition implies that if the empty type has an element, then every proposition has an element and is thus contractible. This implies that the empty type represents falsehood $\bot$ in the type of all propositions. 

### The type of pointed propositions and truth

The type of pointed propositions $\mathrm{Prop}_*$ is given by the type $\sum_{P:\mathrm{Prop}} P$ for Russell types of propositions and $\sum_{P:\mathrm{Prop}} \mathrm{El}(P)$ for Tarski types of propositions, and because pointed propositions are contractible types, pointed propositions are equivalent to each other, and thus by the extensionality principle of $\mathrm{Prop}$, they are equal to each other; thus, the type of pointed propositions is a proposition. 

Because $\mathrm{Prop}_*$ is itself a proposition, $\mathrm{Prop}_*$ is an element of itself, and thus a pointed proposition and a contractible type. This implies that the type of pointed propositions represents [[truth]] $\top$ in the type of all propositions. 

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

## Impredicative polymorphism

Given a universe of all propositions $\mathrm{Prop}$, [[impredicative polymorphism]] of $\mathrm{Prop}$ is equivalent to [[weak function extensionality]]. 

More generally, a universe of propositions $\Omega$ has [[impredicative polymorphism]] if and only if $\Omega$ is closed under [[dependent product types]] of [[predicates]] valued in $\Omega$. 

## Propositional resizing

\begin{theorem}
Any universe of propositions satisfying [[propositional resizing]] is a [[contractible type]].
\end{theorem}

\begin{proof}
Given a universe of propositions $\Omega$, the type of all propositions in $\Omega$ is $\Omega$ itself. Then [[propositional resizing]] says that $\Omega$ has an element $\Omega':\Omega$ such that its type reflection is $\Omega$ itself. This implies that $\Omega$ itself a [[mere proposition]] by definition of universe of proposiions, which implies that $\Omega$ is a contractible type by the element $\Omega':\Omega$ and the fact that for all other elements $P:\Omega$, $P = \Omega'$. 
\end{proof}

\begin{theorem}
Any universe of propositions $\Omega$ closed under the [[empty type]] does not satisfy [[propositional resizing]]. 
\end{theorem}

\begin{proof}
Suppose that $\Omega$ is closed under the empty type $\emptyset$ represented in $\Omega$ by the element $\bot:\Omega$, and satisfies [[propositional resizing]]. Then one has that $\bot = \Omega'$ since $\Omega$ is a [[mere proposition]], and by transport one has $\emptyset \simeq \Omega$, but since $\Omega$ is contractible by propositional resizing, the empty type is also contractible, which is [[false]]. 
\end{proof}

\begin{theorem}
The [[universe of all propositions]] $\mathrm{Prop}$ does not satisfy [[propositional resizing]]. 
\end{theorem}

## Directed univalence

Suppose that the [[dependent type theory]] has [[hom-types]] $\mathrm{hom}_A(a, b)$. Then [[directed univalence]] for a type of propositions $(\Omega, \mathrm{El})$ with $P:\Omega \vdash \mathrm{El}(P)$ a [[covariant type family]] states that for all propositions $P$ and $Q$, there is an [[equivalence of types]] between $\mathrm{hom}_\Omega(P, Q)$ and $\mathrm{El}(P) \to \mathrm{El}(Q)$. Directed univalence for the type of propositions implies [[propositional extensionality]]. 

## Categorical semantics

The [[categorical semantics]] of the type of all propositions is the [[subobject classifier]]. 

## Other types of propositions

There are other types which can also be considered "types of propositions", that only contain some propositions instead of all propositions. These include 

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

These axioms imply that $(\Omega, T)$ satisfy [[propositional extensionality]] and thus that $\Omega$ is an [[h-set]]. 

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

* [[impredicative polymorphism]]

* [[impredicative dependent type theory]]

* [[sigma-frame of propositions]]

## References

* {#UFP13} [[Univalent Foundations Project]], *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

Detailed discussion of the type of propositions in [[Coq]] is in

* [[Adam Chlipala]], _[Certified programming with dependent types](http://adam.chlipala.net/cpdt/)_ -- _[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)_ 

[[!redirects type of propositions]]
[[!redirects types of propositions]]
[[!redirects weak type of propositions]]
[[!redirects weak types of propositions]]
[[!redirects strict type of propositions]]
[[!redirects strict types of propositions]]

[[!redirects Russell type of propositions]]
[[!redirects Russell types of propositions]]
[[!redirects weak Russell type of propositions]]
[[!redirects weak Russell types of propositions]]
[[!redirects strict Russell type of propositions]]
[[!redirects strict Russell types of propositions]]

[[!redirects Tarski type of propositions]]
[[!redirects Tarski types of propositions]]
[[!redirects weak Tarski type of propositions]]
[[!redirects weak Tarski types of propositions]]
[[!redirects strict Tarski type of propositions]]
[[!redirects strict Tarski types of propositions]]

[[!redirects universe of propositions]]
[[!redirects universes of propositions]]
[[!redirects weak universe of propositions]]
[[!redirects weak universes of propositions]]
[[!redirects strict universe of propositions]]
[[!redirects strict universes of propositions]]

[[!redirects Russell universe of propositions]]
[[!redirects Russell universes of propositions]]
[[!redirects weak Russell universe of propositions]]
[[!redirects weak Russell universes of propositions]]
[[!redirects strict Russell universe of propositions]]
[[!redirects strict Russell universes of propositions]]

[[!redirects Tarski universe of propositions]]
[[!redirects Tarski universes of propositions]]
[[!redirects weak Tarski universe of propositions]]
[[!redirects weak Tarski universes of propositions]]
[[!redirects strict Tarski universe of propositions]]
[[!redirects strict Tarski universes of propositions]]

[[!redirects type of all propositions]]
[[!redirects types of all propositions]]
[[!redirects weak type of all propositions]]
[[!redirects weak types of all propositions]]
[[!redirects strict type of all propositions]]
[[!redirects strict types of all propositions]]

[[!redirects Russell type of all propositions]]
[[!redirects Russell types of all propositions]]
[[!redirects weak Russell type of all propositions]]
[[!redirects weak Russell types of all propositions]]
[[!redirects strict Russell type of all propositions]]
[[!redirects strict Russell types of all propositions]]

[[!redirects Tarski type of all propositions]]
[[!redirects Tarski types of all propositions]]
[[!redirects weak Tarski type of all propositions]]
[[!redirects weak Tarski types of all propositions]]
[[!redirects strict Tarski type of all propositions]]
[[!redirects strict Tarski types of all propositions]]

[[!redirects Coquand type of all propositions]]
[[!redirects Coquand types of all propositions]]
[[!redirects weak Coquand type of all propositions]]
[[!redirects weak Coquand types of all propositions]]
[[!redirects strict Coquand type of all propositions]]
[[!redirects strict Coquand types of all propositions]]

[[!redirects universe of all propositions]]
[[!redirects universes of all propositions]]
[[!redirects weak universe of all propositions]]
[[!redirects weak universes of all propositions]]
[[!redirects strict universe of all propositions]]
[[!redirects strict universes of all propositions]]

[[!redirects Russell universe of all propositions]]
[[!redirects Russell universes of all propositions]]
[[!redirects weak Russell universe of all propositions]]
[[!redirects weak Russell universes of all propositions]]
[[!redirects strict Russell universe of all propositions]]
[[!redirects strict Russell universes of all propositions]]

[[!redirects Tarski universe of all propositions]]
[[!redirects Tarski universes of all propositions]]
[[!redirects weak Tarski universe of all propositions]]
[[!redirects weak Tarski universes of all propositions]]
[[!redirects strict Tarski universe of all propositions]]
[[!redirects strict Tarski universes of all propositions]]

[[!redirects Coquand universe of all propositions]]
[[!redirects Coquand universes of all propositions]]
[[!redirects weak Coquand universe of all propositions]]
[[!redirects weak Coquand universes of all propositions]]
[[!redirects strict Coquand universe of all propositions]]
[[!redirects strict Coquand universes of all propositions]]

[[!redirects Prop]]

[[!redirects local propositional resizing]]