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

**Objective type theory** is a [[dependent type theory]] without [[judgmental equality]]. 

This means that in additon to being a [[weak type theory]], where the computation and uniqueness rules ([[beta-reduction]] and [[eta-conversion]]) for each type in the type theory are all propositional computational and uniqueness rules using the [[identity type]], objective type theory is similar to other non-type theory foundations such as the various flavors of set theory, since it also only has one notion of equality, propositional equality, and uses propositional equality in [[definitions]]. 

Objective type theory has [[decidable]] [[type checking]], and the type checking can be done in quadratic time. 

## Formalizations and syntax

### Substitutions

There are two ways one could define [[substitutions]] in [[dependent type theory]], either by [[explicit substitution]] or by showing that the [[substitution rule]] is an [[admissible rule]]. However, for objective type theory, only the latter approach is possible. 

The problem with explicit substitutions is that with explicit substitution approaches, the contexts are usually formalized with [[judgmental equality]] of [[morphisms]] of contexts, such that the [[categorical semantics]] correspond to a functor from the category of contexts $C$ to the [[2-category]] $\mathrm{Cat}$ which takes a context $\Gamma:C$ to the slice category $C/\Gamma$. However, without judgmental equality, $C$ doesn't form a category anymore, since the morphisms in $C$ don't form a [[set]] anymore, and one can no longer express the unit and associatvity laws for composition of morphisms of contexts, which are needed for the unit and associativity laws of explicit substitution. The same holds for explicit substitution via [[telescopes]]; here, substitutions are elements of telescopes, and one has judgmental equalities of the substitutions themselves. 

Alternatively, one can try to define structure indicating that the collection of contexts $C$ forms an [[(infinity,1)-category|$(\infty, 1)$-category]], avoiding the need for judgmental equality entirely, but one quickly runs into [[coherence]] issues, since the structure of an $(\infty, 1)$-category cannot be expressed from nothing using a finite amount of structure. This is similar to the issues in defining an $(\infty, 1)$-category in dependent type theory without using pre-existing [[simplicial set|simplicial]] or [[cubical set|cubical]] structure or [[modal type theory|modalities]]. Thus, it is currently unknown how to avoid this use of judgmental equality for explicit substitution and/or telescopes in dependent type theory, rendering it impossible for those to formulate objective type theory.

The other approach involving an admissible substitution rule doesn't suffer from this issue because the analogue in admissible substitution approaches of the judgmental equality in explicit substitution approaches resides in the metatheory rather than the actual theory itself, so the type theory itself can genuinely be said to not contain any judgmental equalities. 

### Definitions in objective type theory

In section 9 of [Winterhalter2020](#Winterhalter20), [[Theo Winterhalter]] indicates that there are many ways to formalize [[dependent type theory]]. One important aspect is whether to use [[Russell universes]] or a separate [[type]] [[judgment]] to denote types: [van der Berg & den Besten 2021](#BB21) and [UPF 2013](#UPF13) both use [[Russell universes]] in their formal presentation of dependent type theory, while [Rijke 2022](#Rijke22) uses a separate type judgment to denote types. 

In the context of objective type theory, there is no [[judgmental equality]] in the type theory in the traditional sense, so there is the question of how to define aliases of terms and types in the type theory. For the case of terms, that is easily resolved by using identity types. For example, to define $2$ as the successor of the succcessor of zero in the [[natural numbers type]], one could postulate an [[identification]] $\mathrm{def}2:2 =_{\mathrm{N}} s(s(0))$. On the other hand, the situation for types is a bit more complicated. For example, the [[isContr]] [[modality]] $\mathrm{isContr}(A)$ in [[dependent type theory]] indicating whether the type $A$ is a [[contractible type]] is usually defined to be $\sum_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$. But without [[judgmental equality]], one cannot simply write 
$$\mathrm{isContr}(A) \equiv \sum_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$
When presenting [[dependent type theory]] using [[Russell universes]], the answer is as simple as that for terms: one simply uses [[typal equality]] instead, because every type is an element of a Russell universe, and so one could write 
$$\mathrm{defisContr}_A:\mathrm{isContr}(A) =_{\mathrm{Type}_i} \sum_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$
for types $\mathrm{isContr}(A):\mathrm{Type}_i$ and $\sum_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y):\mathrm{Type}_i$. On the other hand, when using a separate type judgment, types are not elements of other types, and thus one cannot compare them for typal equality. Instead, one has to use [[equivalences of types]] instead: 
$$\mathrm{defisContr}_A:\mathrm{isContr}(A) \simeq \sum_{a:A} \prod_{b:A} \mathrm{Id}_A(a, b)$$
This poses another problem: the [[equivalence type]] $A \simeq B$ has not yet been defined yet.  

When expanded out using [[dependent sum types]] and [[function types]], one gets 
$$\sum_{f:A \to B} \mathrm{isEquiv}(f)$$

[UPF 2013](#UPF13) says that the type family $f:A \to B \vdash \mathrm{isEquiv}(f)$ comes with 

* a family of functions 
$$f:A \to B \vdash \mathrm{qinvtoisEquiv}(f):\sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right) \to \mathrm{isEquiv}(f)$$

* a family of functions
$$f:A \to B \vdash \mathrm{isEquivtoqinv}(f):\mathrm{isEquiv}(f) \to \sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right)$$

* a family of identifications
$$f:A \to B, p:\mathrm{isEquiv}(f), q:\mathrm{isEquiv}(f) \vdash \mathrm{proptruncisEquiv}(f, p, q):\mathrm{Id}_{\mathrm{isEquiv}(f)}(p, q)$$

This could be made into inference rules

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{isEquiv}(f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{qinvtoisEquiv}(f):\sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right) \to \mathrm{isEquiv}(f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{isEquivtoqinv}(f):\mathrm{isEquiv}(f) \to \sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, p:\mathrm{isEquiv}(f), q:\mathrm{isEquiv}(f) \vdash \mathrm{proptruncisEquiv}(f, p, q):\mathrm{Id}_{\mathrm{isEquiv}(f)}(p, q)}$$

Breaking the functions down, the inference rules become

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{isEquiv}(f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, g:B \to A, G:\prod_{y:B} \mathrm{Id}_B(f(g(y)), y), H:\prod_{x:A} \mathrm{Id}_A(g(f(x)), x) \vdash \mathrm{qinvtoisEquiv}(f, g, G, H):\mathrm{isEquiv}(f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, p:\mathrm{isEquiv}(f) \vdash \mathrm{isEquivtoqinv}(f, p):\sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, p:\mathrm{isEquiv}(f), q:\mathrm{isEquiv}(f) \vdash \mathrm{proptruncisEquiv}(f, p, q):\mathrm{Id}_{\mathrm{isEquiv}(f)}(p, q)}$$

One could postulate a single equality judgment between types $A \equiv B \; \mathrm{type}$ which reflects into an equivalence:
$$\frac{\Gamma \vdash B \equiv A \; \mathrm{type}}{\Gamma \vdash \mathrm{def}_{A, B}:\sum_{f:A \to B} \mathrm{isEquiv}(f)}$$
A similar equality judgment could be made for terms, with a similar rule to reflect it into an identification:
$$\frac{\Gamma \vdash b \equiv a:A}{\Gamma \vdash \mathrm{def}_{A, a, b}:\mathrm{Id}_A(a, b)}$$
These equalities, while judgmental, are different from the judgmental equality found in other dependent type theories like [[Martin-Löf type theory]] and [[cubical type theory]] in that they have neither the [[structural rules]] nor the [[congruence rules]] found in those theories: they are only a formalization of a notational representation of definitional equality and definitional equivalence otherwise represented by [[identity types]] and [[equivalence types]]. 

### Without a separate type judgment

In this section, we describe a formalization of objective type theory using an infinite hierarchy of Russell universes with cumulativity, in the style of [UPF 2013](#UPF13). 

#### Judgments, contexts, and universes

This presentation of objective type theory consists of the following judgments: 

* Element judgments, where we judge $a$ to be an element of $A$, $a:A$

* Context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. 

In addition, we have a [[countable set|countably]] [[infinite set|infinite]] number of [[inference rules]] for the countably infinite number of [[Russell universes]] $\mathrm{Type}_0, \mathrm{Type}_1, \mathrm{Type}_2, \ldots$ in the theory, here represented by a [[natural numbers]] [[metavariable]] for conciseness:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_i:\mathrm{Type}_{i + 1}}$$

as well as inference rules for either [[cumulativity]], that any type in a universe is also in the next universe of the hierarchy, or [[lifting]], that any type in a universe can be lifted to the next universe of the hierarchy:

$$\frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash A:\mathrm{Type}_{i + 1}}\mathrm{cumul} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_i}{\Gamma \vdash \mathrm{Lift}(A):\mathrm{Type}_{i + 1}}\mathrm{lifting}$$

Contexts are lists of element judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the inference rules for the empty context and extending the context by a element judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A:\mathrm{Type}_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

#### Variable rule

There is one additional [[structural rule]] in objective type theory, the [[variable rule]]. 

The variable rule states that we may derive a element judgment if the element judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

#### Admissible structural rules

The [[weakening rule]] and the [[substitution rule]] are [[admissible rules]]: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

Let $\mathcal{J}$ be any arbitrary judgment. Then the weakening rule is
$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A:\mathrm{Type}_i}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$
and the substitution rule is
$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta(b) \vdash \mathcal{J}(b)}{\Gamma, \Delta(a) \vdash \mathcal{J}(a)}$$

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

Definitions of a symbol $b$ for the element $a:A$ are made by using [[identity types]] between the symbol and element: $\mathrm{def}_{a, b}:a =_A b$. Definitions of a symbol $B$ for the type $A:\mathrm{Type}_i$ are made in the same way, as $\mathrm{def}_{A, B}:A =_{\mathrm{Type}_i} B$. Thus, the [[identity type]] behaves very similarly to [[explicit conversion]] as discussed in section 9.2 of [Winterhalter2020](#Winterhalter20). 

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

In this section, we describe a formalization of objective type theory using a type judgment, in the style of [Rijke 2022](#Rijke22), as well as [[dependent type theory with type variables|type variables]]. 

#### Judgments and contexts

This presentation of objective type theory consists of the following judgments: 

* Type judgments, where we judge $A$ to be a type, $A \; \mathrm{type}$

* Element judgments, where we judge $a$ to be an element of $A$, $a:A$

* Context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. 

Contexts are lists of type judgments and element judgments, et cetera, and are formalized by the rules for the empty context and extending the context by a type judgment and by an element judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx}}{(\Gamma, A \; \mathrm{type}) \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

#### Variable rules

There are two additional [[structural rules]] in objective type theory, the [[variable rule]] for types and elements. 

The variable rule for types states that we may derive a type judgment if the type judgment is in the context already:

$$\frac{\Gamma, A \; \mathrm{type}, \Delta \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, \Delta \vdash A \; \mathrm{type}}$$

The variable rule for elements states that we may derive a element judgment if the element judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

#### Admissible structural rules

The [[weakening rules]] and the [[substitution rules]] are [[admissible rules]]: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

Let $\mathcal{J}$ be any arbitrary judgment. Then the weakening rules are
$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}} \qquad \frac{\Gamma, \Delta \vdash \mathcal{J}}{\Gamma, A \; \mathrm{type}, \Delta \vdash \mathcal{J}}$$
and the substitution rules are
$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta(b) \vdash \mathcal{J}(b)}{\Gamma, \Delta(a) \vdash \mathcal{J}(a)} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, B \; \mathrm{type}, \Delta(B) \vdash \mathcal{J}(B)}{\Gamma, \Delta(A) \vdash \mathcal{J}(A)}$$

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

Definitions of a symbol $b$ for the element $a:A$ are made by using [[identity types]] between the symbol and element: $\mathrm{def}_{a, b}:a =_A b$. Definitions of a symbol $B$ for the type $A$ are made in the same way using [[identity type#IdentityTypesBetweenTypes|identity types between types]], as $\mathrm{def}_{A, B}:A = B$. Thus, the [[identity type]] behaves very similarly to [[explicit conversion]] as discussed in section 9.2 of [Winterhalter2020](#Winterhalter20), even though we do not have universes here. 

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

The fragment of objective type theory consisting of only [[identity types]] and [[dependent product types]] can be interpreted in any [[path category]] with weak homotopy $\Pi$-types. 

## See also

* [[weak type theory]]

* [[judgmental equality]], [[identity type]]

* [[dependent type theory]], [[Martin-Löf type theory]], [[homotopy type theory]]

## References

The original paper on this topic:

* {#BB21} [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

General dependent type theory references used for the formalizations of objective type theory in this article:

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#Winterhalter20} [[Theo Winterhalter]], *Formalisation and Meta-Theory of Type Theory* ([github](https://github.com/TheoWinterhalter/phd-thesis/releases/tag/v1.2.1))

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

[[!redirects objective type theory]]
[[!redirects objective type theories]]