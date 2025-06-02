
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

A [[type theory]] with both [[type variables]] (i.e. [[polymorphic type theory]]) and, for any type $A$, [[variables]] of [[terms]] of type $A$ (i.e. [[dependent type theory]]). 

Traditionally, there are two different ways to present [[dependent type theory]]:

* One can present dependent type theory with a [[hierarchy of type universes]] such that every type is a term of a universe of the hierarchy. Examples of such dependent type theories include the one found in the [[HoTT book]] and the proof assistants [[Agda]], [[Coq]], [[Lean]], and its variants like [[Cubical Agda]]. 

* Alternatively, one can present dependent type theory with a separate type [[judgment]] and no [[type universes]] at all. Examples of such dependent type theories include the one found in [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]. 

In the first presentation of dependent type theory, the concept of a "$U_i$-small type variable" exists: since types are terms of universes, type variables are term variables where the [[context]] is extended by a free variable of a universe. Thus, the type theory is polymorphic in the sense that it has *$U_i$-small polymorphism* for all universe $U_i$ in the universe hierarchy. 

In the second presentation of dependent type theory, the theory does not come with the concept of a type variable, since the context can only be extended by term judgments, and not type judgments. While this is sufficient to define [[univalent universes]] and [[higher inductive types]] in the type theory, there are a few reasons why one might want to extend dependent type theory with type variables to form polymorphic dependent type theory: 

* Large recursion principles of inductive types and higher inductive types $T$ are principles where given some existing data one can construct a type family $C(x)_{x:T}$ indexed by the inductive type $T$. (In the other formulation, large recursion principles are just the usual recursion principles for functions $T \to U$ into a type universe $U$.) While the large recursion principles of certain non-recursive inductive types and higher inductive types, such as the [[type of booleans]], the [[circle type]], and [[graph quotients]], can be defined without type variables, the large recursion principles of recursive inductive types and higher inductive types, such as the [[natural numbers type]] and [[W-types]], require type variables in the theory. 

* The concept of [[impredicative polymorphism]] can be implemented as applying to the entire type theory, rather than to a single universe. Impredicative polymorphism is important for: 

  1. defining axioms such as [[UIP]], [[excluded middle]], the [[type theoretic axiom of replacement|axiom of replacement]] and the [[axiom of choice]] as actual axioms rather than unjustified rules. Axioms involving type families can be represented using an auxiliary type and a function to the index type, where the type family itself is represented by the [[fiber types]] of the function. 

  2. defining [[impredicative]] structures in [[dependent type theory]], such as [[frames]], [[Cauchy complete spaces]], [[Grothendieck topoi]], the [[type of all propositions]], etc.

* With type variables, one can define [[identity types]] $A = B$ between types $A$ and $B$. This has a few benefits: 

  1. With identity types between types, it is possible to define the [[univalence axiom]] and thus make the type theory a [[univalent type theory]] without requiring universes in the type theory. This is important since the univalence axiom implies the large recursion principles discussed in the previous point. 

  2. In a [[dependent type theory]] without [[judgmental equality]], such as [[objective type theory]], it is cumbersome to define or explicitly convert types in terms of other types, since one has to equip each definition or explicit conversion with the structure of an [[equivalence of types]]. With identity types between types, one can simply make use of an [[identification]] between types to represent [[definitional equality]] or [[explicit conversion]]. 

  3. The same goes with the weak large recursion principles: in the absence of either judgmental equality or identity types between types, the [[computation rules]] associated with large recursion principles state that one can construct an equivalence of types between certain types given in the [[elimination rules]] of the large recursion principles. With identity types between types, one can simply make use of an [[identification]] between types. 

Polymorphic dependent type theory with type variables is thus similar to [[System F]], which is a non-dependent [[polymorphism|polymorphic]] [[lambda calculus]] with type variables. 

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

Type variables allow for the formation of [[identity type#IdentityTypesBetweenTypes|identity types between types]]. 

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

There are many consequences of having identity types between types in the dependent type theory. One such example is that any time one uses an [[equivalence of types]] in a definition, such as [[weak Tarski universes]] or typal large recursion principles for inductive types, one can instead use identity types between types in the definition. In addition, one can add [[univalence]] to the dependent type theory itself, which makes the identity types between types and equivalence types coincide with each other. 

#### Univalence axiom

The [[univalence axiom]] states that the function 

$$\mathrm{idtoequiv}(A, B):(A = B) \to (A \simeq B)$$

inductively defined by 

$$\mathrm{idtoequiv}(A, A, \mathrm{refl}(A)) \coloneqq \mathrm{id}_A$$

is an [[equivalence of types]] for all types $A$ and $B$, 

$$\mathrm{isEquiv}(\mathrm{idtoequiv}(A, B))$$

where $\mathrm{id}_A \coloneqq \lambda x:A.x$ is the [[identity function]] on the type $A$. In [[impredicative polymorphism]], this is given by the following axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ua}:\Pi A.\Pi B.\mathrm{isEquiv}(\lambda p:A = B.\mathrm{idtoequiv}(A, B, p))}$$

Unlike the other presentation of dependent type theory in terms of universes, in this presentation of dependent type theory with a type judgment and type variables, it *is consistent* to assume both the [[univalence axiom]] and an [[axiom of set truncation]] like [[UIP]] or [[axiom K]], since here there is no universe, provided one doesn't have any higher types, such as the [[circle type]]. 

#### Large recursion principles

In the usual dependent type theory without type variables, large recursion of [[inductive types]] and [[higher inductive types]] is usually expressed in terms of [[equivalence of types|equivalences]] and [[transport]]. For example, the strict large recursion principle of the [[circle type]] $S^1$ usually states that given a type $A$ and an [[autoequivalence]] $e:A \simeq A$, one can form the type family $x:S^1 \vdash \mathrm{lrec}_{S^1}^{A, e}(x)$ such that 
$$\mathrm{lrec}_{S^1}^{A, e}(\mathrm{base}) \equiv A \; \mathrm{type} \quad \mathrm{and} \quad \mathrm{tr}_{S^1}^{\mathrm{lrec}_{S^1}^{A, e}}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv e:A \simeq A$$
However, with type variables, instead of using equivalences and transport, one can instead use [[identity type#IdentityTypesBetweenTypes|identity types between types]] and the [[action on identifications]] for type families. For example, an alternative strict large recursion principle of the [[circle type]] $S^1$ states that given a type $A$ and an [[identification]] $p:A = A$, one can form the type family $x:S^1 \vdash \mathrm{lrec}_{S^1}^{A, p}(x)$ such that 
$$\mathrm{lrec}_{S^1}^{A, p}(\mathrm{base}) \equiv A \; \mathrm{type} \quad \mathrm{and} \quad \mathrm{ap}_{S^1}^{\mathrm{lrec}_{S^1}^{A, p}}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv p:A = A$$

In addition, traditionally without type variables, there are strict and weak versions of large recursion principles: the strict large recursion principles use [[judgmental equality]] between types for the computation and uniqueness rules, while the weak large recursion principles use [[equivalences of types]] for the computation and uniqueness rules. For example, the strict large recursion principle for the [[type of booleans]] $\mathbb{2}$ says that given types $A$ and $B$, one can construct a type family $x:\mathbb{2} \vdash \mathrm{lrec}_\mathbb{2}^{A, B}(x)$ such that 
$$\mathrm{lrec}_\mathbb{2}^{A, B}(0) \equiv A \quad \mathrm{and} \quad \mathrm{lrec}_\mathbb{2}^{A, B}(1) \equiv B$$
and the weak large recursion principle for the type of booleans says that the type family above comes with [[equivalences of types]]
$$\mathrm{l}\beta_\mathbb{2}^{A}:\mathrm{lrec}_\mathbb{2}^{A, B}(0) \simeq A \quad \mathrm{and} \quad \mathrm{l}\beta_\mathbb{2}^{B}:\mathrm{lrec}_\mathbb{2}^{A, B}(1) \simeq B$$ 
However, with type variables and [[identity type#IdentityTypesBetweenTypes|identity types between types]], one can also use identifications of types instead of equivalences of types to express weak large recursion of the type of booleans:
$$\mathrm{l}\beta_\mathbb{2}^{A}:\mathrm{lrec}_\mathbb{2}^{A, B}(0) = A \quad \mathrm{and} \quad \mathrm{l}\beta_\mathbb{2}^{B}:\mathrm{lrec}_\mathbb{2}^{A, B}(1) = B$$ 
This third notion of weak large recursion in dependent type theory with a single type judgment and type variables parallels the usual notion of weak large recursion in the other formulation of dependent type theory involving a hierarchy of universes, where large recursion simply means the usual recursion principle into one of the predefined universes in the hierarchy. 

### Large recursion principles of recursive inductive types

Independently of the consequences of having [[identity type#IdentityTypesBetweenTypes|identity types between types]], having type variables allows for the formulation of certain large recursion principles which are not possible in the dependent type theory with a single type judgment but no type variables. These include large recursion for recursive inductive types and recursive higher inductive types such as the [[natural numbers type]], [[W-types]], and [[localizations of a type]]. 

For example, the usual recursion principle for the [[natural numbers type]] is given by the following: given 

1. a type $C$

1. an element $c_0:C$

1. a family of elements $n:\mathbb{N}, x:C \vdash c_s(n, x):C$

one can construct a family of elements

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{C, c_0, c_s}(n):C$$

such that 

$$\mathrm{rec}_\mathbb{N}^{C, c_0, c_s}(0) \equiv c_0:C$$

and 

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{C, c_0, c_s}(s(n)) \equiv c_s(n, \mathrm{rec}_\mathbb{N}^{C, c_0, c_s}(n):C$$

In the other formulation of dependent type theory in terms of a hierarchy of universes and no type judgment, large recursion of the natural numbers is simply the recursion principle for a universe $U_i$ in the hierarchy: given 

1. a universe $U$

1. an type $T_0:U$

1. a family of elements $n:\mathbb{N}, X:U \vdash T_s(n, X):U$

one can construct a family of elements

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{U, T_0, T_s}(n):U$$

such that 

$$\mathrm{rec}_\mathbb{N}^{U, T_0, T_s}(0) \equiv T_0:U$$

and 

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{U, T_0, T_s}(s(n)) \equiv T_s(n, \mathrm{rec}_\mathbb{N}^{U, T_0, T_s}(n):U$$

However, in dependent type theory with a single type judgment, the universe $U$ is not needed and in fact non-existent. Translating the large recursion principle into type judgments, we get the following: given 

1. a type $T_0 \; \mathrm{type}$

1. a family of types $n:\mathbb{N}, X \; \mathrm{type} \vdash T_s(n, X) \; \mathrm{type}$

one can construct a family of types

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{T_0, T_s}(n) \; \mathrm{type}$$

such that 

$$\mathrm{rec}_\mathbb{N}^{T_0, T_s}(0) \equiv T_0 \; \mathrm{type}$$

and 

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{T_0, T_s}(s(n)) \equiv T_s(n, \mathrm{rec}_\mathbb{N}^{T_0, T_s}(n)) \; \mathrm{type}$$

It is clear that type variables are needed, since otherwise the second requirement in the large recursion principle that we have a family of types $n:\mathbb{N}, X \; \mathrm{type} \vdash T_s(n, X) \; \mathrm{type}$ will not be possible. 

Similar requirements of type variables apply to the large recursion principles of more general recursive inductive types like [[W-types]]. 

## Type family variables

### With function types

Given a [[dependent type theory]] with [[type variables]], [[dependent sum types]], [[identity types]], and [[function types]], type families indexed by type $A$ and functions to $A$ are equivalent to each other: 

* By the inference rules of [[dependent sum types]], a type family $x:A \vdash B(x)$ is equivalently a type $\sum_{x:A} B(x)$ with a [[function]] $\pi_A$ to $A$. 

* Similarly, a type $B$ with a function $f:B \to A$ is equivalently a type family $x:A \vdash \sum_{y:B} f(x) =_A y$. 

If the type theory is formulated using a [[hierarchy of universes]] $U_i$, one can show for all types $A:U_i$ that the above operations form an [[equivalence of types]] between the following types:

$$(A \to U_i) \simeq \left(\sum_{B:U_i} B \to A\right)$$

As a result, a *type family variable* or a *variable of type families* simply consists of a type variable and a term variable of a function type:

$$(\Gamma, B \; \mathrm{type}, f:B \to A, \Delta)$$

### With type telescopes

On the other hand, if the dependent type theory does not have [[function types]], such as the case for a hypothetical [[geometric homotopy type theory]] as the [[internal logic]] of a [[Grothendieck (infinity,1)-topos|Grothendieck $(\infty,1)$-topos]], then one would have to add [[type telescopes]] to the theory. Via telescopes, we have, for each type $A$, a separate [[judgment]]: 

$$B \; \mathrm{type} / (x:A)$$  

where $(x:A)$ is the telescope consisting of the judgment $x:A$. 

With type telescopes, there [[inference rules]] which mimic the inference rules for [[function types]] $A \to U_i$ for a [[type universe]] $U_i$ are derivable from the inference rules for telescopes:

$$\frac{\Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \lambda x:A.B(x) \; \mathrm{type} / (x:A)}$$

$$\frac{\Gamma \vdash B \; \mathrm{type} / (x:A)}{\Gamma, x:A \vdash B(x) \; \mathrm{type}}$$

$$\frac{\Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A \vdash B(x) \equiv (\lambda x:A.B(x))(x) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash B \; \mathrm{type} / (x:A)}{\Gamma \vdash B \equiv \lambda x:A.B(x) \; \mathrm{type} / (x:A)}$$

Then we have additional context forming rules that says that given a type judgment $A \; \mathrm{type}$ in context $\Gamma$, we can add the judgment to $B \; \mathrm{type} / (x:A)$ the context:

$$\frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, B \; \mathrm{type} / (x:A)) \; \mathrm{ctx}}$$

In addition, the judgment $b : B / (x:A)$ behaves as a dependent function, and we also have [[inference rules]] which mimic the inference rules for [[dependent function types]] $(x:A) \to B(x)$: 

$$\frac{\Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda x:A.b(x) : \lambda x:A.B(x) / (x:A)}$$

$$\frac{\Gamma \vdash B \; \mathrm{type} \; \mathrm{at} \; A \quad \Gamma \vdash b: B / (x:A)}{\Gamma, x:A \vdash b(x):B(x)}$$

$$\frac{\Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash b(x) \equiv (\lambda x:A.b(x))(x):B(x)}$$

$$\frac{\Gamma \vdash B \; \mathrm{type} \; \mathrm{at} \; A \quad \Gamma \vdash b: B / (x:A)}{\Gamma \vdash b \equiv \lambda x:A.b(x) : B / (x:A)}$$

Then we have additional context forming rules that says that given the judgment $B \; \mathrm{type} / (x:A)$ in context $\Gamma$, we can add the judgment $b : B / (x:A)$ to the context:

$$\frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash B \; \mathrm{type} \; \mathrm{at} \; A}{(\Gamma, b : B  / (x:A)) \; \mathrm{ctx}}$$

Collectively, the additions of [[type telescopes]] to the dependent type theory behave as if it is a [[modal type theory]] whose mode theory is given by the original [[dependent type theory]] and represents, for an $(\infty,1)$-topos $\mathcal{E}$, the [[(infinity,2)-category|$(\infty,2)$-category]] of [[slice (infinity,1)-topos|slice $(\infty,1)$-toposes]] $\mathcal{E} / A$. 

## Related concepts

* [[type theory]]

  * [[simple type theory]]

  * [[polymorphic type theory]]

  * [[dependent type theory]]

  * **polymorphic dependent type theory**

* [[identity type]]

* [[univalence axiom]]

* [[univalent type theory]]

* [[polymorphism]]

* [[impredicative polymorphism]]

* [[System F]]

* [[explicit conversion]]

## References

Some discussion about extending dependent type theory with type variables occurs in:

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

[[!redirects polymorphic dependent type theory]]
[[!redirects polymorphic dependent type theories]]

[[!redirects dependent type theory with type variables]]
[[!redirects dependent type theories with type variables]]

[[!redirects polymorphic type theory with dependent types]]
[[!redirects polymorphic type theories with dependent types]]

[[!redirects small polymorphism]]

[[!redirects type family variable]]
[[!redirects type family variables]]

[[!redirects variable of type families]]
[[!redirects variables of type families]]