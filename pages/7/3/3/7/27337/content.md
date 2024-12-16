
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Traditionally, there are two different ways to present [[dependent type theory]]:

* One can present dependent type theory with a [[hierarchy of type universes]] such that every type is a term of a universe of the hierarchy. Examples of such dependent type theories include the one found in the [[HoTT book]] and the proof assistants [[Agda]], [[Coq]], [[Lean]], and its variants like [[Cubical Agda]]. 

* Alternatively, one can present dependent type theory with a separate type [[judgment]] and no [[type universes]] at all. Examples of such dependent type theories include the one found in [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]. 

In the first presentation of dependent type theory, the concept of a "type variable" exists: since types are terms of universes, type variables are term variables where the [[context]] is extended by a free variable of a universe. 

In the second presentation of dependent type theory, the theory does not come with the concept of a type variable, since the context can only be extended by term judgments, and not type judgments. While this is sufficient to define [[univalent universes]] and [[higher inductive types]] in the type theory, there are a few reasons why one might want to extend dependent type theory with type variables:

* Large recursion principles of inductive types and higher inductive types $T$ are principles where given some existing data one can construct a type family $C(x)_{x:T}$ indexed by the inductive type $T$. (In the other formulation, large recursion principles are just the usual recursion principles for functions $T \to U$ into a type universe $U$.) While the large recursion principles of certain non-recursive inductive types and higher inductive types, such as the [[boolean domain]], the [[circle type]], and [[graph quotients]], can be defined without type variables, the large recursion principles of recursive inductive types and higher inductive types, such as the [[natural numbers type]] and [[W-types]], require type variables in the theory. 

* With type variables, one can define [[identity types]] $A = B$ between types $A$ and $B$. This has a few benefits: 

  1. With identity types between types, it is possible to define the [[univalence axiom]] and thus make the type theory a [[univalent type theory]] without requiring universes in the type theory. This is important since the univalence axiom implies the large recursion principles discussed in the previous point. 

  2. In a [[dependent type theory]] without [[judgmental equality]], such as [[objective type theory]], it is cumbersome to define types in terms of other types, since one has to equip each definition with the structure of an [[equivalence of types]]. With identity types between types, one can simply make use of an [[identification]] between types. 

  3. The same goes with the weak large recursion principles: in the absence of either judgmental equality or identity types between types, the [[computation rules]] associated with large recursion principles state that one can construct an equivalence of types between certain types given in the [[elimination rules]] of the large recursion principles. With identity types between types, one can simply make use of an [[identification]] between types. 

* The concept of [[impredicative polymorphism]] can be implemented as applying to the entire type theory, rather than to a single universe. 

## Definition

We assume [[dependent type theory]] with context judgments $\Gamma \; \mathrm{ctx}$, type judgments $A \; \mathrm{type}$, and term judgments $a:A$ and the usual context-creating rules and [[structural rules]] for the dependent type theory. 

To extend the above theory with type variables, we add the following rule

$$\frac{\Gamma \; \mathrm{ctx}}{(\Gamma, A \; \mathrm{type}) \; \mathrm{ctx}}$$

which states that it is possible to extend the [[context]] by a type judgment, and the following rule

$$\frac{\Gamma, A \; \mathrm{type}, \Delta \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, \Delta \vdash A \; \mathrm{type}}$$

which states that we may derive a type judgment if the type judgment is already in the context. 

It is conjectured in the [Category Theory Zulip](#CTZulip) that the substitution rules and weakening rules for type variables are [[admissible rules]]. 

### Judgmental equality

If the type theory has additional judgments $a \equiv b:A$ and $A \equiv B \; \mathrm{type}$ for [[judgmental equality of terms]] and [[judgmental equality of types]] respectively and the associated [[structural rules]] for judgmental equality, then the corresponding rules for judgmental equality involving type variables (i.e. substitution is a congruence, variable conversion, etc) should also be [[admissible rules]]. 

### Impredicative polymorphism

In the presentation of dependent type theory using a hierarchy of universes, [[impredicative polymorphism]] is a resizing axiom which says that for all [[endofunctions]] $P:U_0 \to U_0$ on the first [[type universe]] $U_0$, the [[dependent product type]] $\prod_{X:U_0} P(X)$ is ([[essentially small type|essentially]]) [[small type|$U_0$-small]]. 

In the presentation of dependent type theory without universes but with a separate type judgment, while there is no universe $U_0$ to quantify over for the dependent product type, using the type variable we can add an untyped version of the dependent product type $\Pi X.P(X)$ to the type theory. This type is similar to [[universal quantification]] $\forall X.P(X)$ in untyped [[first-order logic]], and $\Pi X.P(X)$ plays the same role in this presentation of dependent type theory that the type $\prod_{X:U_0} P(X)$ does for the other presentation of dependnet type theory. The rules for $\Pi X.P(X)$ are as follows:

Formation rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type}}{\Gamma \vdash \Pi X.P(X) \; \mathrm{type}}$$

Introduction rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma \vdash \lambda X.p(X):\Pi X.P(X)}$$

Elimination rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\Pi X.P(X)}{\Gamma, A \; \mathrm{type} \vdash \mathrm{ev}(p, X):P(X)}$$

Computation rules:

* Judgmental computation rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma, X \; \mathrm{type} \vdash \mathrm{ev}(\lambda X.p(X), X) \equiv p(X):P(X)}$$
* Typal computation rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma, X \; \mathrm{type} \vdash \beta_\Pi^{P, p}(X):\mathrm{ev}(\lambda X.p(X), X) =_{P(X)} p(X)}$$

Uniqueness rules:

* Judgmental uniqueness rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\Pi X.P(X)}{\Gamma \vdash \lambda X.\mathrm{ev}(p, X) \equiv p:\Pi X.P(x)}$$
* Typal uniqueness rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\Pi X.P(X)}{\Gamma \vdash \eta_\Pi^P(p):\lambda X.\mathrm{ev}(p, X) =_{\Pi X.P(x)} p}$$

### Identity types between types

Type variables allow for the formation of [[identity types]] between types. 

* Formation rule for identity types between types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type} \vdash A = B \; \mathrm{type}}$$

* Introduction rule for identity types between types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type} \vdash \mathrm{refl}(A):A = A}$$

* Elimination rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash \mathrm{ind}_=^{C, t}(A, B, p):C(A, B, p)}$$

* Judgmental computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A ; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash \mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) \equiv t(A):C(A, A, \mathrm{refl}(A))}$$

* Typal computation rule for identity types between types

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A ; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash \beta_{=}^{C, t}(A):\mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) =_{C(A, A, \mathrm{refl}(A))} t(A)}$$

If the dependent type theory has [[impredicative polymorphism]], then the $\Delta$ contexts can be removed from the elimination and computation rules of the identity types between types, simplifying the rules down to the following: 

* Elimination rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma \vdash \mathrm{ind}_=^{C}(t):\Pi A.\Pi B.\Pi (p:A = B).C(A, B, p)}$$

* Judgmental computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma, A \; \mathrm{type} \vdash \mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) \equiv t(A):C(A, A, \mathrm{refl}(A))}$$

* Typal computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma \vdash \beta_{=}^{C}(t):\Pi A.\mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) =_{C(A, A, \mathrm{refl}(A))} t(A)}$$

### Univalence

The [[univalence axiom]] states that the function 

$$\mathrm{idtoequiv}(A, B):(A = B) \to (A \simeq B)$$

inductively defined by 

$$\mathrm{idtoequiv}(A, A, \mathrm{refl}(A)) \coloneqq \mathrm{id}_A$$

is an [[equivalence of types]] for all types $A$ and $B$, 

$$\mathrm{isEquiv}(\mathrm{idtoequiv}(A, B))$$

where $\mathrm{id}_A \coloneqq \lambda x:A.x$ is the [[identity function]] on the type $A$. In [[impredicative polymorphism]], this is given by the following axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ua}:\Pi A.\Pi B.\mathrm{isEquiv}(\lambda p:A = B.\mathrm{idtoequiv}(A, B, p))}$$

Unlike the other presentation of dependent type theory in terms of universes, in this presentation of dependent type theory with a type judgment and type variables, it *is consistent* to assume both the [[univalence axiom]] and an [[axiom of set truncation]] like [[UIP]] or [[axiom K]], since here there is no universe. 

### Tarski universes

There are now three different notions of [[Tarski universes]] in dependent type theory with type variables and identity types between types. 

There is the usual notion of [[strict Tarski universe]] which states that, for example, 

* the Tarski universe $(U, T)$ is strictly closed under dependent sum types if for $A:U$ and $B:T(A) \to U$ there is $\Sigma(A, B):U$ with a [[judgmental equality]] $T(\Sigma(A, B)) \equiv \sum_{x:T(A)} T(B(X))$

* the Tarski universe $(U, T)$ is strictly closed under dependent product types if for $A:U$ and $B:T(A) \to U$ there is $\Pi(A, B):U$ with a [[judgmental equality]] $T(\Pi(A, B)) \equiv \prod_{x:T(A)} T(B(X))$

There is the usual notion of [[weak Tarski universe]] which states that, for example, 

* the Tarski universe $(U, T)$ is weakly closed under dependent sum types if for $A:U$ and $B:T(A) \to U$ there is $\Sigma(A, B):U$ with an equivalence $e_\Sigma(A, B):T(\Sigma(A, B)) \simeq \sum_{x:T(A)} T(B(X))$

* the Tarski universe $(U, T)$ is weakly closed under dependent product types if for $A:U$ and $B:T(A) \to U$ there is $\Pi(A, B):U$ with an equivalence $e_\Pi(A, B):T(\Pi(A, B)) \simeq \prod_{x:T(A)} T(B(X))$

Then there is a stronger notion of weak Tarski universe which is only possible if there are identity types between types, which states that 

* the Tarski universe $(U, T)$ is weakly closed under dependent sum types if for $A:U$ and $B:T(A) \to U$ there is $\Sigma(A, B):U$ with an [[identification]] $p_\Sigma(A, B):T(\Sigma(A, B)) = \sum_{x:T(A)} T(B(X))$

* the Tarski universe $(U, T)$ is weakly closed under dependent product types if for $A:U$ and $B:T(A) \to U$ there is $\Pi(A, B):U$ with an [[identification]] $p_\Pi(A, B):T(\Pi(A, B)) = \prod_{x:T(A)} T(B(X))$

This is similar to the case for Tarski universes in the presentation of dependent type theory with a hierarchy of universes, which also has three different kinds of Tarski universes involving judgmental equality, identity types between types, and equivalences of types respectively. 

### Large recursion principles

TODO: explain how type variables are necessary for certain large recursion principles, such as that of the natural numbers type. Explain how there are now three versions of large recursion principles in general, rather than two, due to the existence of identity types between types. 

## Related concepts

* [[identity type]]

* [[polymorphism]], [[impredicative polymorphism]]

## References

Some discussion about extending dependent type theory with type variables occurs in:

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))