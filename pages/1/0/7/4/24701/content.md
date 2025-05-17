
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[dependent type theory]] where the [[computation rules]] and [[uniqueness rules]] for types use [[identity types]] instead of [[judgmental equality]]. As a result, the results in the dependent type theory are more general than in models which use judgmental equality for computational and uniqueness rules, since judgmental equality implies typal equality, while the converse isn't necessarily the case. 

The dependent type theory has many different names in the existing literature

* *propositional type theory* (e.g. [Spadetto 2023](#Spadetto23))

* *objective type theory* (e.g. [van der Berg & den Besten 2021](#BB21))

* *weak type theory* (e.g. [Winterhalter 2020](#Winterhalter20))

Propositional type theory has [[decidable]] [[type checking]], and the type checking can be done in quadratic time. 

## Definitions in propositional type theory

Propositional type theories come into two general versions, depending on how they treat [[definitions]] in dependent type theory:

* Dependent type theories which have a judgmental [[definitional equality]] (e.g. [Spadetto 2023](#Spadetto23)). 

* Dependent type theories which do not have judgmental [[definitional equality]] (e.g. [van der Berg & den Besten 2021](#BB21)). 

These two approaches differ in whether aliases of terms and types reduce to the original term or type, or are identified or equivalent to the original term or type. They each have their own advantages:

Advantages of not having judgmental definitional equality include 

* a simpler set of inference rules 

* more models

* type theories without any definitional equalities are cofibrant in categories of theories.

Advantages of having judgmental definitional equality include 

* shorter internal proofs and constructions

* avoids “higher transport hell” for aliases of terms and types

### With judgmental definitional equality

For propositional type theory with judgmental definitional equality, definitions of aliases of [[types]] and [[terms]] are still made using [[judgmental equality]]. The [[structural rules]] and [[congruence rules]] have to be postulated explicitly in the theory like in the usual dependent type theories. In addition to the [[congruence rules]] for [[judgmental equality]] for the [[formation rules]], [[introduction rules]], and [[elimination rules]] of each type former, there are additional [[congruence rules]] for the computation and uniqueness rules, since the conversion rules are represented by the structure of an identification rather than judgmental equality, and thus this structure has to be preserved across judgmental equality. 

### Without judgmental definitional equality

For propositional type theory without judgmental definitional equality, [[definitions]] of [[types]] and [[terms]] are made using [[identifications]] or [[equivalences of types]]. Any judgmental equality $\equiv$ in the theory represents [[alpha-equivalence|$\alpha$-equivalence]] or [[syntactic equality]], where the usual [[structural rules]] and [[congruence rules]] are [[admissible rules]].  

Furthermore, in the context of propositional type theory where there is no [[definitional equality]] in the type theory in the traditional sense, there is the question of how to define aliases of terms and types in the type theory. 

For the case of terms, that is easily resolved by using identity types. For example, to define $2$ as the successor of the succcessor of zero in the [[natural numbers type]], one could postulate an [[identification]] $\mathrm{def}2:2 =_{\mathrm{N}} s(s(0))$. On the other hand, the situation for types is a bit more complicated. For example, the [[isProp]] [[modality]] $\mathrm{isProp}(A)$ in [[dependent type theory]] indicating whether the type $A$ is a [[mere proposition]] is usually defined to be $\prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$. But without [[judgmental equality]], one cannot simply write 
$$\mathrm{isProp}(A) \equiv \prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$

When presenting [[dependent type theory]] using [[Russell universes]], the answer is as simple as that for terms: one simply uses [[typal equality]] instead, because every type is an element of a Russell universe, and so one could write 
$$\mathrm{defisProp}_A:\mathrm{isProp}(A) =_{\mathrm{Type}_i} \prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$
for types $\mathrm{isProp}(A):\mathrm{Type}_i$ and $\prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y):\mathrm{Type}_i$. 

On the other hand, when using a separate type judgment, types are not elements of other types, and thus one cannot compare them for typal equality. Instead, one has two alternatives 

* One can use [[polymorphic dependent type theory]] with [[type variables]] and postulate an [[identity type#IdentityTypeBetweenTypes|identity type between types]] $A = B$, where we then have
$$\mathrm{defisProp}_A:\mathrm{isProp}(A) = \prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$
* One can postulate a [[type of equivalences]] $A \simeq B$ as a [[record type]] with propositional computation rules, where we then have
$$\mathrm{defisProp}_A:\mathrm{isProp}(A) \simeq \prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$ 

## Formalizations and syntax

In section 9 of [Winterhalter 2020](#Winterhalter20), [[Theo Winterhalter]] indicates that there are many ways to formalize [[dependent type theory]]. One important aspect is whether to use [[Russell universes]] or a separate [[type]] [[judgment]] to denote types. [van der Berg & den Besten 2021](#BB21) and [Spadetto 2023](#Spadetto23) for example both use [[Russell universes]] in their formal presentation of dependent type theory. 

In this section, we present two separate formalizations, the first using a [[universe hierarchy]] of [[Russell universes]] in the style of [UFP 13](#UFP13), and the second using a separate type judgment in the style of [Rijke 2022](#Rijke22), along with type variables to define identity types between types for explicit conversion. 

### Without a separate type judgment

In this section, we describe a formalization of propositional type theory using an infinite hierarchy of Russell universes with cumulativity, in the style of [UPF 2013](#UPF13). 

#### Judgments, contexts, and universes

This presentation of propositional type theory consists of the following judgments: 

* Element judgments, where we judge $a$ to be an element of $A$, $a:A$

* Context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. 

In addition, we have a [[countable set|countably]] [[infinite set|infinite]] number of [[inference rules]] for the countably infinite number of [[Russell universes]] $\mathrm{Type}_0, \mathrm{Type}_1, \mathrm{Type}_2, \ldots$ in the theory, here represented by a [[natural numbers]] [[metavariable]] for conciseness:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_i:\mathrm{Type}_{i + 1}}$$

as well as inference rules for either [[cumulativity]], that any type in a universe is also in the next universe of the hierarchy, or [[lifting]], that any type in a universe can be lifted to the next universe of the hierarchy:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash A:\mathrm{Type}_{i + 1}}\mathrm{cumul} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash \mathrm{Lift}(A):\mathrm{Type}_{i + 1}}\mathrm{lifting}$$

Contexts are lists of element judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the inference rules for the empty context and extending the context by a element judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A:\mathrm{Type}_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

#### Variable rule

There is one additional [[structural rule]] in propositional type theory, the [[variable rule]]. 

The variable rule states that we may derive a element judgment if the element judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

#### Families of types and elements

A family of elements is an element $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. They are usually written as $b(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the element $b(a)$ is an element dependent upon $a:A$. 

Since types are elements of universe, a family of types is simply a family of elements of universes. 

#### Identity types

Formation rules for identity types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma, a:A, b:A \vdash a =_A b:\mathrm{Type}_i}$$

Introduction rules for identity types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Elimination rule for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y, \Delta(x, y, p) \vdash C(x, y, p):\mathrm{Type}_i}{\Gamma, x:A, t:C(x, x, \mathrm{refl}_A(x), y:A, p:x =_A y, \Delta(x, t, y, p) \vdash \mathrm{ind}_{=_A}(x, t, y, p):C(x, y, p)}$$

Computation rules for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y, \Delta(x, y, p) \vdash C(x, y, p):\mathrm{Type}_i}{\Gamma, x:A, t:C(x, x, \mathrm{refl}_A(x), \Delta(x, t, x, \mathrm{refl}_A(x)) \vdash \beta_{=_A}(x, t):\mathrm{ind}_{=_A}(x, t, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t}$$

#### Definitions

Definitions of a symbol $b$ for the element $a:A$ are made by using [[identity types]] between the symbol and element: $\mathrm{def}_{a, b}:a =_A b$. Definitions of a symbol $B$ for the type $A:\mathrm{Type}_i$ are made in the same way, as $\mathrm{def}_{A, B}:A =_{\mathrm{Type}_i} B$. Thus, the [[identity type]] behaves very similarly to [[explicit conversion]] as discussed in section 9.2 of [Winterhalter 2020](#Winterhalter20). 

#### Dependent function types

Formation rules for dependent function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma \vdash \prod_{x:A} B(x):\mathrm{Type}_i}$$

Introduction rules for dependent function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

Elimination rules for dependent function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, f:\prod_{x:A} B(x), a:A \vdash \mathrm{ind}_{\prod_{x:A} B(x)}(f, a):B(a)}$$

Computation rules for dependent function types
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash \beta_{\prod_{x:A} B(x)}(a):\mathrm{ind}_{\prod_{x:A} B(x)}(\lambda(x:A).b(x), a) =_{B(a)} b(a)}$$

Uniqueness rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, f:\prod_{x:A} B(x) \vdash \eta_{\prod_{x:A} B(x)}(f):f =_{\prod_{x:A} B(x)} \lambda(x:A).\mathrm{ind}_{\prod_{x:A} B(x)}(f, x)}$$

#### Function types

Formation rules for function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma \vdash A \to B:\mathrm{Type}_i}$$

Introduction rules for function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i \quad \Gamma, x:A \vdash b(x):B}{\Gamma \vdash \lambda(x:A).b(x):A \to B}$$

Elimination rules for function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, f:A \to B, a:A \vdash \mathrm{ind}_{A \to B}(f, a):B}$$

Computation rules for function types
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i \quad \Gamma, x:A \vdash b(x):B}{\Gamma, a:A \vdash \beta_{A \to B}(a):\mathrm{ind}_{A \to B}(\lambda(x:A).b(x), a) =_{B} b(a)}$$

Uniqueness rules for function types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, f:A \to B \vdash \eta_{A \to B}(f):f =_{A \to B} \lambda(x:A).\mathrm{ind}_{A \to B}(f, x)}$$

#### Pair types

Formation rules for pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma \vdash A \times B:\mathrm{Type}_i}$$

Introduction rules for pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):A \times B}$$

Elimination rules for pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^A(z):A} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^B(z):B}$$

Computation rules for pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^A(x, y):\mathrm{ind}_{A \times B}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^B(x, y):\mathrm{ind}_{A \times B}^B(\mathrm{in}(x, y)) =_B y}$$

Uniqueness rules for pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, z:A \times B \vdash \eta_{A \times B}(z):z =_{A \times B} \mathrm{in}(\mathrm{ind}_{A \times B}^A(z), \mathrm{ind}_{A \times B}^B(z))}$$

#### Dependent pair types

Formation rules for dependent pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma \vdash \sum_{x:A} B(x):\mathrm{Type}_i}$$

Introduction rules for dependent pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, x:A, y:B(x) \vdash \mathrm{in}(x, y):\sum_{x:A} B(x)}$$

Elimination rules for dependent pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^A:\left(\sum_{x:A} B(x)\right) \to A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^B:\prod_{z:\sum_{x:A} B(x)} B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(z))}$$

Computation rules for dependent pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, x:A, y:B(x) \vdash \beta_{\sum_{x:A} B(x)}^A(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^B(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^B(\mathrm{in}(x, y)) =_{B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)))} y}$$

Uniqueness rules for dependent pair types:
$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma, z:\sum_{x:A} B(x) \vdash \eta_{\sum_{x:A} B(x)}(z):z =_{\sum_{x:A} B(x)} \mathrm{in}(\mathrm{ind}_{\sum_{x:A} B(x))}^A(z), \mathrm{ind}_{\sum_{x:A} B(x)}^B(z))}$$

#### isContr, uniqueness quantifiers, isEquiv, and equivalence types

Now that we have [[identity types]], [[dependent sum types]], and [[dependent product types]], we can use that to define 

* the [[isContr]] [[modality]]:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash \mathrm{isContr}(A):\mathrm{Type}_i} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash \mathrm{defisContr}(A):\mathrm{isContr}(A) =_{\mathrm{Type}_i} \sum_{y:A} \prod_{z:A} y =_{A} z}$$

* the [[uniqueness quantifier]]:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma \vdash \exists!x:A.B(x):\mathrm{Type}_i} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma, x:A \vdash B(x):\mathrm{Type}_i}{\Gamma \vdash \mathrm{def}\exists!_{x:A.B(x)}:\exists!x:A.B(x) =_{\mathrm{Type}_i} \mathrm{isContr}\left(\sum_{x:A} B(x)\right)}$$

* the [[isEquiv]] [[type family]]:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, f:A \to B \vdash \mathrm{isEquiv}(f):\mathrm{Type}_i} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma, f:A \to B \vdash \mathrm{defisEquiv}_{A, B}(f):\mathrm{isEquiv}(f) =_{\mathrm{Type}_i} \prod_{y:B} \exists!x:A.f(x) =_{B} y}$$

* the [[equivalence type]]:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma \vdash A \simeq B:\mathrm{Type}_i} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma \vdash \mathrm{def}_{A \simeq B}:(A \simeq B) =_{\mathrm{Type}_i} \sum_{f:A \to B} \mathrm{isEquiv}(f)}$$

#### Univalence

The [[univalence axiom]] states that the identity type between two types of a universe is equivalent to the equivalence type between said types:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i \quad \Gamma \vdash B:\mathrm{Type}_i}{\Gamma \vdash \mathrm{ua}_i(A, B):(A =_{\mathrm{Type}_i} B) \simeq (A \simeq B)}$$

#### Positive types

Now that we have the [[uniqueness quantifier]] we can combine the [[elimination rule]], the [[computation rule]], and the [[uniqueness rule]] for any [[positive type]] into one rule, the [[induction]] rule. 

##### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1}:\mathrm{Type}_i}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

Induction rule for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x):\mathrm{Type}_i \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\exists!c:\prod_{x:\mathbb{1}} C(x).(c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})}$$

##### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0}:\mathrm{Type}_i}$$

Induction rule for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C(x):\mathrm{Type}_i}{\Gamma \vdash \mathrm{up}_\mathbb{0}^C:\mathrm{isContr}\left(\prod_{x:\mathbb{0}} C(x)\right)}$$

##### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2}:\mathrm{Type}_i}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Induction rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x):\mathrm{Type}_i \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\exists!c:\prod_{x:\mathbb{2}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)}$$

##### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N}:\mathrm{Type}_i}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Induction rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x):\mathrm{Type}_i \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{N}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

### With a separate type judgment and type variables

In this section, we describe a formalization of propositional type theory using a type judgment, in the style of [Rijke 2022](#Rijke22), as well as [[dependent type theory with type variables|type variables]]. 

#### Judgments and contexts

This presentation of propositional type theory consists of the following judgments: 

* Type judgments, where we judge $A$ to be a type, $A \; \mathrm{type}$

* Element judgments, where we judge $a$ to be an element of $A$, $a:A$

* Context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. 

Contexts are lists of type judgments and element judgments, et cetera, and are formalized by the rules for the empty context and extending the context by a type judgment and by an element judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx}}{(\Gamma, A \; \mathrm{type}) \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

#### Variable rules

There are two additional [[structural rules]] in propositional type theory, the [[variable rule]] for types and elements. 

The variable rule for types states that we may derive a type judgment if the type judgment is in the context already:

$$\frac{\Gamma, A \; \mathrm{type}, \Delta \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, \Delta \vdash A \; \mathrm{type}}$$

The variable rule for elements states that we may derive a element judgment if the element judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

#### Families of types and elements

A family of types is a type $B$ in the context of the element judgment $x:A$, $x:A \vdash B \; \mathrm{type}$, they are usually written as $B(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the type $B(a)$ is a type dependent upon $a:A$. 

A family of elements is an element $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. They are likewise usually written as $b(x)$ to indicate its dependence upon $x$. Given a particular element $a:A$, the element $b(a)$ is an element dependent upon $a:A$. 

A universal family of types is a type $B$ in the context of a type variable judgment $X \; \mathrm{type}$, $X \; \mathrm{type} \vdash B \; \mathrm{type}$, they are usually written as $B(X)$ to indicate its dependence upon $X$. Given a particular type $A \; \mathrm{type}$, the type $B(A)$ is a type dependent upon $A$. 

A universal family of elements is an element $b:B$ in the context of the type variable judgment $X \; \mathrm{type}$, $X \; \mathrm{type} \vdash b:B$. They are likewise usually written as $b(X)$ to indicate its dependence upon $x$. Given a particular type $A \; \mathrm{type}$, the element $b(A)$ is an element dependent upon $A \; \mathrm{type}$. 

#### Identity types

Formation rules for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

Introduction rules for identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{refl}_A(x) : x =_A x}$$

Elimination rule for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, x:A, t:C(x, x, \mathrm{refl}_A(x), y:A, p:x =_A y, \Delta(x, t, y, p) \vdash \mathrm{ind}_{=_A}(x, t, y, p):C(x, y, p)}$$

Computation rules for identity types:
$$\frac{\Gamma, x:A, y:A, p:x =_A y, \Delta(x, y, p) \vdash C(x, y, p) \; \mathrm{type}}{\Gamma, x:A, t:C(x, x, \mathrm{refl}_A(x) \vdash \beta_{=_A}(x, t):\mathrm{ind}_{=_A}(x, t, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t}$$

#### Identity types between types

Formation rule for identity types between types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type} \vdash A = B \; \mathrm{type}}$$

Introduction rule for identity types between types:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type} \vdash \mathrm{refl}(A):A = A}$$

Elimination rule for identity types between types:
$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash \mathrm{ind}_=^{C, t}(A, B, p):C(A, B, p)}$$

Computation rule for identity types between types
$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A ; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash \beta_{=}^{C, t}(A):\mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) =_{C(A, A, \mathrm{refl}(A))} t(A)}$$

#### Definitions

Definitions of a symbol $b$ for the element $a:A$ are made by using [[identity types]] between the symbol and element: $\mathrm{def}_{a, b}:a =_A b$. Definitions of a symbol $B$ for the type $A$ are made in the same way using [[identity type#IdentityTypesBetweenTypes|identity types between types]], as $\mathrm{def}_{A, B}:A = B$. Thus, the [[identity type]] behaves very similarly to [[explicit conversion]] as discussed in section 9.2 of [Winterhalter 2020](#Winterhalter20), even though we do not have universes here. 

#### Dependent function types

Formation rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

Elimination rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x), a:A \vdash \mathrm{ind}_{\prod_{x:A} B(x)}(f, a):B(a)}$$

Computation rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \beta_{\prod_{x:A} B(x)}^{x:A.b(x)}:\prod_{a:A} \mathrm{ind}_{\prod_{x:A} B(x)}(\lambda(x:A).b(x), a) =_{B(a)} b(a)}$$

Uniqueness rules for dependent function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x) \vdash \eta_{\prod_{x:A} B(x)}(f):f =_{\prod_{x:A} B(x)} \lambda(x:A).\mathrm{ind}_{\prod_{x:A} B(x)}(f, x)}$$

#### Function types

Formation rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

Introduction rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma \vdash \lambda(x:A).b(x):A \to B}$$

Elimination rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, a:A \vdash \mathrm{ind}_{A \to B}(f, a):B}$$

Computation rules for function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma \vdash \beta_{A \to B}^{x:A.b(x)}:\prod_{a:A} \mathrm{ind}_{A \to B}(\lambda(x:A).b(x), a) =_{B} b(a)}$$

Uniqueness rules for function types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \eta_{A \to B}:\prod_{f:A \to B} f =_{A \to B} \lambda(x:A).\mathrm{ind}_{A \to B}(f, x)}$$

#### Pair types

Formation rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):A \times B}$$

Elimination rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^A(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^B(z):B}$$

Computation rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^A(x, y):\mathrm{ind}_{A \times B}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^B(x, y):\mathrm{ind}_{A \times B}^B(\mathrm{in}(x, y)) =_B y}$$

Uniqueness rules for pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \eta_{A \times B}(z):z =_{A \times B} \mathrm{in}(\mathrm{ind}_{A \times B}^A(z), \mathrm{ind}_{A \times B}^B(z))}$$

#### Dependent pair types

Formation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \mathrm{in}(x, y):\sum_{x:A} B(x)}$$

Elimination rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^A:\left(\sum_{x:A} B(x)\right) \to A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^B:\prod_{z:\sum_{x:A} B(x)} B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(z))}$$

Computation rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\sum_{x:A} B(x)}^A(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)) =_A x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:B(x) \vdash \beta_{\Sigma(x:A).B(x)}^B(x, y):\mathrm{ind}_{\sum_{x:A} B(x)}^B(\mathrm{in}(x, y)) =_{B(\mathrm{ind}_{\sum_{x:A} B(x)}^A(\mathrm{in}(x, y)))} y}$$

Uniqueness rules for dependent pair types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \eta_{\sum_{x:A} B(x)}(z):z =_{\sum_{x:A} B(x)} \mathrm{in}(\mathrm{ind}_{\sum_{x:A} B(x))}^A(z), \mathrm{ind}_{\sum_{x:A} B(x)}^B(z))}$$

#### isContr, uniqueness quantifiers, isEquiv, and equivalence types

Now that we have [[identity types]], [[identity types#IdentityTypesBetweenTypes|identity types between types]], [[dependent sum types]], and [[dependent product types]], we can use that to define 

* the [[isContr]] [[modality]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isContr}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{defisContr}(A):\mathrm{isContr}(A) = \sum_{y:A} \prod_{z:A} y =_{A} z}$$

* the [[uniqueness quantifier]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \exists!x:A.B(x) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{def}\exists!_{x:A.B(x)}:\exists!x:A.B(x) = \mathrm{isContr}\left(\sum_{x:A} B(x)\right)}$$

* the [[isEquiv]] [[type family]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{isEquiv}(f) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{defisEquiv}_{A, B}(f):\mathrm{isEquiv}(f) = \prod_{y:B} \exists!x:A.f(x) =_{B} y}$$

* the [[equivalence type]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{def}_{A \simeq B}:(A \simeq B) = \sum_{f:A \to B} \mathrm{isEquiv}(f)}$$

#### Univalence

The [[univalence axiom]] states that the identity type between two types is equivalent to the equivalence type between said types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{ua}(A, B):(A = B) \simeq (A \simeq B)}$$

#### Positive types

Now that we have the [[uniqueness quantifier]] we can combine the [[elimination rule]], the [[computation rule]], and the [[uniqueness rule]] for any [[positive type]] into one rule, the [[induction]] rule. 

##### Empty type

Formation rules for the empty type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

Recursion rule for the empty type:
$$\frac{\Gamma \vdash C \; \mathrm{type}}{\Gamma \vdash \mathrm{up}_\mathbb{0}^C:\mathrm{isContr}\left(\mathbb{0} \to C\right)}$$

Induction rule for the empty type:
$$\frac{\Gamma, x:\mathbb{0} \vdash C(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{dup}_\mathbb{0}^C:\mathrm{isContr}\left(\prod_{x:\mathbb{0}} C(x)\right)}$$

##### Unit type

Formation rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

Introduction rules for the unit type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{pt}:\mathbb{1}}$$

Recursion rule for the unit type:
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C}{\Gamma \vdash \mathrm{up}_\mathbb{1}^C(c_\mathrm{pt}):\exists!c:\mathbb{1} \to C.(c(\mathrm{pt}) =_{C} c_\mathrm{pt})}$$

Induction rule for the unit type:
$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{pt}:C(\mathrm{pt})}{\Gamma \vdash \mathrm{dup}_\mathbb{1}^C(c_\mathrm{pt}):\exists!c:\prod_{x:\mathbb{1}} C(x).(c(\mathrm{pt}) =_{C(\mathrm{pt})} c_\mathrm{pt})}$$

##### Booleans type

Formation rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{2} \; \mathrm{type}}$$

Introduction rules for the booleans type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{2}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{2}}$$

Recursion rule for the booleans type:
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash c_1:C}{\Gamma \vdash \mathrm{up}_\mathbb{2}^C(c_0, c_1):\exists!c:\mathbb{2} \to C.(c(0) =_{C} c_0) \times (c(1) =_{C} c_1)}$$

Induction rule for the booleans type:
$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1)}{\Gamma \vdash \mathrm{dup}_\mathbb{2}^C(c_0, c_1):\exists!c:\prod_{x:\mathbb{2}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1)}$$

##### Natural numbers type

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Recursion rule for the natural numbers type:
$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash c_s:C \to C}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\exists!c:\mathbb{N} \to C.(c(0) =_{C} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C} c_s(c(x))}$$

Induction rule for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{dup}_\mathbb{N}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{N}} C(x).(c(0) =_{C(0)} c_0) \times \prod_{x:\mathbb{N}} c(s(x)) =_{C(s(x))} c_s(c(x))}$$

## Categorical semantics

The fragment of propositional type theory consisting of only [[identity types]] and [[dependent product types]] can be interpreted in any [[path category]] with weak homotopy $\Pi$-types. 

## Open problems

There are plenty of questions which are currently unresolved in propositional type theory. Van der Berg and Besten listed the following problems:

* Does [[univalence]] imply [[function extensionality]] for types in the universe in [[propositional type theory]]?

* Is (the [[homotopy type theory]] based upon) [[Martin-Löf type theory]] conservative over (the [[homotopy type theory]] based upon) [[propositional type theory|propositional]] Martin-Löf type theory?

* How much of the [[HoTT book]] could be done in [[propositional type theory]]?

* Does [[propositional type theory]] have [[homotopy canonicity]] and [[normalization]]?

Other problems include

* What is the [[categorical semantics]] of the [[homotopy type theory]] based upon [[propositional type theory]], with all [[higher inductive types]] and [[weakly Tarski]] [[univalent universes]]? 

* Is [[weak function extensionality]] equivalent to [[function extensionality]] in [[propositional type theory]]?

* Does [[product extensionality]] hold in [[propositional type theory]]? Namely, given types $A$ and $B$ and elements $a:A \times B$ and $b:A \times B$, is the canonical function $\mathrm{idtoprojectionids}:(a =_{A \times B} b) \to (\pi_1(a) \simeq \pi_1(b)) \times (\pi_2(a) \simeq \pi_2(b))$ an [[equivalence of types]]?

* Is [[function extensionality]] still provable in propositional [[cubical type theory]]?

See also [[open problems in homotopy type theory]]

## Related concepts

* [[judgmental equality]], [[identity type]]

* [[dependent type theory]], [[Martin-Löf type theory]], [[homotopy type theory]]

## References

* {#Winterhalter20} [[Théo Winterhalter]], *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;

* {#Spadetto23} [[Matteo Spadetto]], *Relating homotopy equivalences to conservativity in dependendent type theories with propositional computation* ([arXiv:2303.05623](https://arxiv.org/abs/2303.05623))

On quadratic type checking in propositional type theory:

* {#BB21} [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

Talks at *Strength of Weak Type Theory*, hosted by *[[DutchCATS]]*:

* [[Daniël Otten]], *Models for Propositional Type Theory* (11 May 2023) &lbrack;[slides pdf](https://dutchcats.github.io/Weak_type_theories/slides_otten.pdf)&rbrack;

* [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))

* [[Sam Speight]], *Higher-Dimensional Realizability for Intensional Type Theory*, 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_speight.pdf))

* [[Matteo Spadetto]], *Weak type theories: a conservativity result for homotopy elementary types* (12 May 2023) &lbrack;[slides pdf](https://dutchcats.github.io/Weak_type_theories/slides_spadetto.pdf)&rbrack;

* [[Benno van den Berg]], *Towards homotopy canonicity for propositional type theory*, 12 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_van_den_berg.pdf))

* [[Rafaël Bocquet]], *Towards coherence theorems for equational extensions of type theories*, 12 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_bocquet.pdf))

Project to convert [[extensional type theory]] to [[weak type theory]]:

* Github, [ett-to-wtt](https://github.com/TheoWinterhalter/ett-to-wtt)

Additional general dependent type theory references used for the formalizations of propositional type theory in this article:

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

[[!redirects objective type theory]]
[[!redirects objective type theories]]

[[!redirects objective dependent type theory]]
[[!redirects objective dependent type theories]]

[[!redirects propositional type theory]]
[[!redirects propositional type theories]]

[[!redirects propositional dependent type theory]]
[[!redirects propositional dependent type theories]]

[[!redirects weak type theory]]
[[!redirects weak type theories]]

[[!redirects weak dependent type theory]]
[[!redirects weak dependent type theories]]

[[!redirects dependent type theory with explicit conversion]]
[[!redirects dependent type theories with explicit conversion]]

[[!redirects dependent type theory with explicit conversions]]
[[!redirects dependent type theories with explicit conversions]]

[[!redirects homotopy type theory with explicit conversion]]
[[!redirects homotopy type theories with explicit conversion]]

[[!redirects homotopy type theory with explicit conversions]]
[[!redirects homotopy type theories with explicit conversions]]

[[!redirects dependent type theory with propositional computation]]
[[!redirects dependent type theories with propositional computation]]

[[!redirects dependent type theory with propositional computation rules]]
[[!redirects dependent type theories with propositional computation rules]]

[[!redirects dependent type theory with typal computation]]
[[!redirects dependent type theories with typal computation]]

[[!redirects dependent type theory with typal computation rules]]
[[!redirects dependent type theories with typal computation rules]]

[[!redirects homotopy type theory with propositional computation]]
[[!redirects homotopy type theories with propositional computation]]

[[!redirects homotopy type theory with propositional computation rules]]
[[!redirects homotopy type theories with propositional computation rules]]

[[!redirects homotopy type theory with typal computation]]
[[!redirects homotopy type theories with typal computation]]

[[!redirects homotopy type theory with typal computation rules]]
[[!redirects homotopy type theories with typal computation rules]]