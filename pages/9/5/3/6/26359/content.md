
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

In [[dependent type theory]], the *type of finite types* is the [[type universe]] $\mathrm{FinType}$ which contains the [[finite types]] of the type theory, in the sense of [[finite set]] in set theory. The type of finite types is important in the field of [[combinatorics]], as well as for defining mathematical structures like [[finite-dimensional vector spaces]]. 

## Definition

In [[dependent type theory]], given a type $A$, there are many different ways of defining the [[mere proposition]] $\mathrm{isFinite}(A)$ which indicates that $A$ is a [[finite type]]. 

* Given a [[natural numbers type]] $\mathbb{N}$, a type $A$ is finite if [[existential quantifier|there merely exists]] a natural number $n:\mathbb{N}$ such that $A$ is equivalent to the standard finite type $\mathrm{Fin}(n)$ (see at [[family of finite types]]):

$$\mathrm{isFinite}(A) \equiv \exists n:\mathbb{N}.A \simeq \mathrm{Fin}(n)$$

* Given a [[type of propositions]] $\mathrm{Prop}$, a type $A$ is finite if for all [[subtypes]] $S:(A \to \mathrm{Prop}) \to \mathrm{Prop}$ of the [[power set]] of $A$, if the [[empty subset|empty subtype]] $\lambda x:A.\bot$ is in $S$, and for all subtypes $P:A \to \mathrm{Prop}$ and $Q:A \to \mathrm{Prop}$ of $A$ such that $P$ being in $S$, $Q$ being a singleton subtype, and $P$ and $Q$ being [[disjoint subset|disjoint]] together imply that the [[union]] $P \cup Q$ is in $S$, then the [[improper subset|improper subtype]] $\lambda x:A.\top$ is in $S$.

$$
\mathrm{isFinite}(A) \equiv 
\begin{array}{c}
\prod_{S:(A \to \mathrm{Prop}) \to \mathrm{Prop}} (((\lambda x:A.\bot) \in S) \times \prod_{P:A \to \mathrm{Prop}} \prod_{Q:A \to \mathrm{Prop}} (P \in S) \\
\times (\exists!x:A.x \in Q) \times (P \cap Q =_{A \to \mathrm{Prop}} \lambda x:A.\bot) \to (P \cup Q \in S)) \to ((\lambda x:A.\top) \in S)
\end{array}
$$

* Alternatively, if we don't have either a [[natural numbers type]] or a [[type of all propositions]], given the [[boolean domain]] $\mathrm{Bool}$, a type $A$ is finite if for all [[decidable subtypes]] $S:(A \to \mathrm{Bool}) \to \mathrm{Bool}$ of the set of decidable subtypes of $A$, if the [[empty subset|empty decidable subtype]] $\lambda x:A.\bot$ is in $S$, and for all decidable subtypes $P:A \to \mathrm{Bool}$ and $Q:A \to \mathrm{Bool}$ of $A$ such that $P$ being in $S$, $Q$ being a singleton decidable subtype, and $P$ and $Q$ being [[disjoint subset|disjoint]] together imply that the [[union]] $P \cup Q$ is in $S$, then the [[improper subset|improper decidable subtype]] $\lambda x:A.\top$ is in $S$.

$$
\mathrm{isFinite}(A) \equiv 
\begin{array}{c}
\prod_{S:(A \to \mathrm{Bool}) \to \mathrm{Bool}} (((\lambda x:A.\bot) \in S) \times \prod_{P:A \to \mathrm{Bool}} \prod_{Q:A \to \mathrm{Bool}} (P \in S) \\
\times (\exists!x:A.x \in Q) \times (P \cap Q =_{A \to \mathrm{Bool}} \lambda x:A.\bot) \to (P \cup Q \in S)) \to ((\lambda x:A.\top) \in S)
\end{array}
$$

The membership relation and the subtype operations used above are defined in the nLab article on [[subtypes]].

The definitions of the various different types of finite types are agnostic regarding the definition of $\mathrm{isFinite}$, as they uses $\mathrm{isFinite}$ directly rather than a particular definition. 

### The type of all finite types

Unlike the case for the [[type of all types]] $\mathrm{Type}$, the type of all finite types $\mathrm{FinType}$ doesn't run into [[Girard's paradox]], because neither $\mathrm{FinType}$ nor its set truncation is itself a finite type, and so isn't an element of itself. 

The **type of all finite types** $\mathrm{FinType}$ in a [[dependent type theory]] could be presented either as a [[Russell universe]] or a [[Tarski universe]]. The difference between the two is that in the former, every [[finite type]] in the type theory is literally an element of the type of finite types, while in the latter, elements of $\mathrm{FinType}$ are only indices of a type family $\mathrm{El}$; every [[finite type]] in the type theory is only [[essentially small type|essentially $\mathrm{FinType}$-small]] for [[weak Tarski universes]] or [[judgmentally equal]] to an $\mathrm{El}(P)$ for $P:\mathrm{FinType}$ for [[strict Tarski universes]]. 

#### As a strict Tarski universe

As a [[strict Tarski universe]], the type of all finite types is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all finite types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{FinType} \; \mathrm{type}}$$

Introduction rules for the type of all finite types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:\mathrm{isFinite}(A) \to \mathrm{FinType}}$$

Elimination rules for the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{finWitn}(A):\mathrm{isFinite}(\mathrm{El}(A))}$$

Computation rules for the type of all finite types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \mathrm{El}(\mathrm{toElem}_A(p)) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \mathrm{finWitn}(\mathrm{toElem}_A(p)) \equiv p:\mathrm{isFinite}(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \beta_\mathrm{FinType}^{\mathrm{finWitn},A}(p):\mathrm{finWitn}(\mathrm{toElem}_A(p)) =_{\mathrm{isFinite}(A)} p}$$

Uniqueness rules for the type of all finite types:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{finWitn}(A)) \equiv A:\mathrm{FinType}}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \eta_{\mathrm{FinType}}(A):\mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{finWitn}(A)) =_{\mathrm{FinType}} A}$$

[[univalence axiom|Extensionality principle]] of the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType} \quad \Gamma \vdash B:\mathrm{FinType}} {\Gamma \vdash \mathrm{ext}_\mathrm{FinType}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### As a weak Tarski universe

As a [[weak Tarski universe]], the type of all finite types is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all finite types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{FinType} \; \mathrm{type}}$$

Introduction rules for the type of all finite types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:\mathrm{isFinite}(A) \to \mathrm{FinType}}$$

Elimination rules for the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{finWitn}(A):\mathrm{isFinite}(\mathrm{El}(A))}$$

Computation rules for the type of all finite types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \beta_\mathrm{FinType}^{\mathrm{El}, A}(p):\mathrm{El}(\mathrm{toElem}_A(p)) \simeq A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \mathrm{congform}_\mathrm{isFinite}(\beta_\mathrm{FinType}^{\mathrm{El}, A}(p))(\mathrm{finWitn}(\mathrm{toElem}_A(p))) \equiv p:\mathrm{isFinite}(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \beta_\mathrm{FinType}^{\mathrm{finWitn},A}(p):\mathrm{congform}_\mathrm{isFinite}(\beta_\mathrm{FinType}^{\mathrm{El}, A}(p))(\mathrm{finWitn}(\mathrm{toElem}_A(p))) =_{\mathrm{isFinite}(A)} p}$$

where the equivalence
$$\mathrm{congform}_\mathrm{isFinite}(\beta_\mathrm{FinType}^{\mathrm{El}, A}(p)):\mathrm{isFinite}(\mathrm{El}(\mathrm{toElem}_A(p))) \simeq \mathrm{isFinite}(A)$$
can always be constructed in a type theory with [[dependent product types]], [[dependent sum types]], [[identity types]], and a [[type of all propositions]], as given types $A$ and $B$ and an equivalence $e:A \simeq B$, it is possible to form the equivalence $\mathrm{congform}_\mathrm{isFinite}(e):\mathrm{isFinite}(A) \simeq \mathrm{isFinite}(B)$ through [[function application to identifications|application of equivalences to identifications]] and the typal congruence rules of [[function types]], [[dependent product types]], [[product types]], and [[dependent sum types]]. 

Uniqueness rules for the type of all finite types:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash A \equiv \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{finWitn}(A)):\mathrm{FinType}}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \eta_{\mathrm{FinType}}(A):A =_{\mathrm{FinType}} \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{finWitn}(A))}$$

[[univalence axiom|Extensionality principle]] of the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType} \quad \Gamma \vdash B:\mathrm{FinType}} {\Gamma \vdash \mathrm{ext}_\mathrm{FinType}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### As a Russell universe

As a [[Russell universe]], the type of all finite types is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all finite types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{FinType} \; \mathrm{type}}$$

Introduction rules for the type of all finite types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:\mathrm{isFinite}(A) \to \mathrm{FinType}}$$

Elimination rules for the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{finWitn}(A):\mathrm{isFinite}(A)}$$

Computation rules for the type of all finite types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \mathrm{toElem}_A(p) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \mathrm{finWitn}(\mathrm{toElem}_A(p)) \equiv p:\mathrm{isFinite}(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isFinite}(A)}{\Gamma \vdash \beta_\mathrm{FinType}^{\mathrm{finWitn},A}(p):\mathrm{finWitn}(\mathrm{toElem}_A(p)) =_{\mathrm{isFinite}(A)} p}$$

Uniqueness rules for the type of all finite types:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \mathrm{toElem}_{A}(\mathrm{finWitn}(A)) \equiv A:\mathrm{FinType}}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{FinType}}{\Gamma \vdash \eta_{\mathrm{FinType}}(A):\mathrm{toElem}_{A}(\mathrm{finWitn}(A)) =_{\mathrm{FinType}} A}$$

[[univalence axiom|Extensionality principle]] of the type of all finite types:
$$\frac{\Gamma \vdash A:\mathrm{FinType} \quad \Gamma \vdash B:\mathrm{FinType}} {\Gamma \vdash \mathrm{ext}_\mathrm{FinType}(A, B):\mathrm{isEquiv}(\mathrm{idToEquiv}(A, B))}$$

### Type of small finite types

Given an already existing [[Russell universe]] $U$, the type of $U$-small finite types is given by the [[dependent sum type]]

$$\sum_{A:U} \mathrm{isFinite}(A)$$

Similarly, given an already existing [[Tarski universe]] $(U, T)$, the type of $U$-small finite types is given by the [[dependent sum type]]

$$\sum_{A:U} \mathrm{isFinite}(T(A))$$

## Properties

### Closure under type formers

The type of finite types is closed under the [[empty type]], the [[unit type]], [[function types]],  [[dependent product types]], [[product types]], [[dependent sum types]], and [[sum types]]. 

### Relation to the natural numbers type

The [[natural numbers type]] is equivalent to the [[set truncation]] of the type of finite types:

$$\mathbb{N} \simeq [\mathrm{FinType}]_0$$ 

This is the type theoretic analogue of the [[decategorification]] of the [[permutation category]] resulting in the set of [[natural numbers]]. 

This also means that the [[axiom of infinity]] for a [[type universe]] $U$ could be defined as a resizing axiom similar to [[propositional resizing]], since [[set truncations]] could be defined from $\mathrm{Prop}_U$ the [[type of propositions]] in $U$:

$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} \mathbb{N} \simeq \left[\sum_{A:U} \mathrm{isFinite}(A)\right]_0$$

$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} T(\mathbb{N}) \simeq \left[\sum_{A:U} \mathrm{isFinite}(T(A))\right]_0$$

The arithmetic operations and order relations on the [[natural numbers type]] can be defined by induction on [[set truncation]]:

For all finite types $A:\mathrm{FinType}$ and $B:\mathrm{FinType}$ and finite families $C:A \to \mathrm{FinType}$, we have

$$0 =_\mathbb{N} [\emptyset]_0 \quad 1 =_\mathbb{N} [\mathbb{1}]_0$$
$$[A]_0 + [B]_0 =_\mathbb{N} [A + B]_0$$
$$\sum_{x = 1}^{[A]_0} [C]_0(x) =_\mathbb{N} \left[\sum_{x:A} C(x)\right]_0$$
$$[A]_0 \cdot [B]_0 =_\mathbb{N} [A \times B]_0$$
$$\prod_{x = 1}^{[A]_0} [C]_0(x) =_\mathbb{N} \left[\prod_{x:A} C(x)\right]_0$$
$$[B]_0^{[A]_0} =_\mathbb{N} [A \to B]_0$$

$$[A]_0 =_\mathbb{N} [B]_0 \coloneqq [A \simeq B]_{(-1)} \; \mathrm{or} \; [A =_\mathrm{FinType} B]_{(-1)}$$
$$[A]_0 \leq [B]_0 \coloneqq [A \hookrightarrow B]_{(-1)}$$ 

## Categorical semantics

The categorical semantics of the type of finite types is the finite object classifier, the [[object classifier]] which classifies [[finite objects]] of a [[category]]. 

## Related concepts

* [[type of propositions]]

* [[type universe]]

* [[natural numbers type]]

* [[axiom of infinity]]

## References

For the fact that binary sum types, finite dependent sum types, and binary product types of finite types are finite types, see section 16.3 of: 

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

For the fact that function types between finite types are finite types, see Exercise 16.1 of the above reference. These imply that the type of finite types are closed under binary sum types, finite dependent sum types, binary product types, and function types. 

[[!redirects type of finite types]]
[[!redirects types of finite types]]

[[!redirects Russell type of finite types]]
[[!redirects Russell types of finite types]]
[[!redirects Tarski type of finite types]]
[[!redirects Tarski types of finite types]]
[[!redirects weak Tarski type of finite types]]
[[!redirects weak Tarski types of finite types]]
[[!redirects strict Tarski type of finite types]]
[[!redirects strict Tarski types of finite types]]

[[!redirects universe of finite types]]
[[!redirects universes of finite types]]
[[!redirects Russell universe of finite types]]
[[!redirects Russell universes of finite types]]
[[!redirects Tarski universe of finite types]]
[[!redirects Tarski universes of finite types]]
[[!redirects weak Tarski universe of finite types]]
[[!redirects weak Tarski universes of finite types]]
[[!redirects strict Tarski universe of finite types]]
[[!redirects strict Tarski universes of finite types]]

[[!redirects type of all finite types]]
[[!redirects types of all finite types]]

[[!redirects Russell type of all finite types]]
[[!redirects Russell types of all finite types]]
[[!redirects Tarski type of all finite types]]
[[!redirects Tarski types of all finite types]]
[[!redirects weak Tarski type of all finite types]]
[[!redirects weak Tarski types of all finite types]]
[[!redirects strict Tarski type of all finite types]]
[[!redirects strict Tarski types of all finite types]]

[[!redirects FinType]]