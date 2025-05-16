
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea
 {#Idea}

In any [[predicate logic over type theory]], **propositional equality** is the notion of [[equality]] which is defined to be a proposition. Propositional equality is most commonly used in [[set theories]] like [[ZFC]] and [[ETCS]], but it could also be used for [[definitional equality]] and [[conversional equality]] in some presentations of [[dependent type theories]] like [[Martin-Löf type theory]] or [[cubical type theory]] in place of [[judgmental equality]]. 

Propositional equality can be contrasted with [[judgmental equality]], where equality is a [[judgment]], and [[typal equality]], where equality is a [[type]].

### Note on terminology

Historically in the [[dependent type theory]] community, the term *propositional equality* was used for [[typal equality]]. This was because under the principle of [[propositions as types]], one interprets all types in a single-layer type theory as being propositions. However, we choose to make a distinction between propositional equality and typal equality. First, propositional equality as defined in this article is used in the most common [[foundations of mathematics]], such as [[ZFC]] and [[ETCS]], and is clearly not a type. Additionally, in some [[logics over type theory]], one can have three distinct notions of equality: [[judgmental equality]], [[propositional equality]], and [[typal equality]]. Finally, in the advent of [[homotopy type theory]] and other type theoretic [[higher foundations]], [[typal equality]] is no longer required to be a [[subsingleton]] or [[h-proposition]], and the alternative principle of [[propositions as some types]] has become the primary interpretation of [[dependent type theory]], where only the [[subsingletons]] or [[h-propositions]] are interpreted as [[propositions]]. 

## Definition

### Typed first-order logic

In any two-layer type theory with a layer of [[types]] and a layer of [[propositions]], or equivalently a [[first order logic]] over [[type theory]] or a [[first-order theory]], every type $A$ has a binary [[relation]] according to which two elements $x$ and $y$ of $A$ are related if and only if they are equal; in this case we write $x =_A y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is called **[[propositional equality]]**. The formation and introduction rules for propositional equality is as follows

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{prop}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash x =_A x \; \mathrm{true}}$$

Then we have the elimination rules for propositional equality:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash P(x, y) \; \mathrm{prop}}{\Gamma \vdash \left(\forall x:A.P(x, x)\right) \implies \left(\forall x:A.\forall y:A.x =_A y \implies P(x, y)\right) \; \mathrm{true}}$$

### Untyped first-order logic

Something similar occurs in untyped [[first-order logic]], where the [[domain of discourse]] has a binary [[relation]] according to which two elements $x$ and $y$ are related if and only if they are equal; in this case we write $x = y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is similarly called **[[propositional equality]]**. The formation and introduction rules for propositional equality is as follows

$$\frac{\Gamma \vdash x \quad \Gamma \vdash y}{\Gamma \vdash x = y \; \mathrm{prop}} \quad \frac{\Gamma \vdash x}{\Gamma \vdash x = x \; \mathrm{true}}$$

Then we have the elimination rules for propositional equality:

$$\frac{\Gamma, x, y \vdash P(x, y) \; \mathrm{prop}}{\Gamma \vdash \left(\forall x.P(x, x)\right) \implies \left(\forall x.\forall y.x = y \implies P(x, y)\right) \; \mathrm{true}}$$

## Properties

### Propositional equality is an equivalence relation

The introduction rule of propositional equality says that propositional equality is reflexive. 

We can show that heterogeneous equality is symmetric, that for all $x:A$ and $y:A$ such that $x =_A y$, we have $y =_A x$. By the introduction rule, we have that for all $x:A$, we have that $x =_A x$, and because all propositions imply themselves, we have that $x =_A x$ implies $x =_A x$. Thus, by the elimination rules for heterogeneous equality, for all $x:A$ and $y:A$ such that $x =_A y$, we have $y =_A x$. 

We can also show that heterogeneous equality is transitive, that for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$, $y =_A z$ implies that $x =_A z$. By the introduction rule, we have that for all $x:A$ and $a:B(x)$, we have that $x =_A x$, and because all propositions imply themselves, we have that $x =_A z$ implies $y =_A z$, and because true propositions imply true propositions, we have that $x =_A x$ implies that $x =_A z$ implies $x =_A z$. Thus, by the elimination rules for heterogeneous equality, for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$, $y =_A z$ implies that $x =_A z$. 

Thus, heterogeneous equality is an equivalence relation. 

### Functions are extensional

For all function $f:A \to B$ and elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{B} f(y)$:

$$\forall f:A \to B.\forall x:A.\forall y:A.x =_A y \implies f(x) =_{B} f(y)$$

This is because for all functions $f:A \to B$, by the introduction rule for propositional equality, for all elements $x:A$, $f(x) =_{B} f(x)$, and the elimination rule for propositional equality states that if for all elements $x:A$, $f(x) =_{B} f(x)$, then for all elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{B} f(y)$. 

### Function extensionality

The extensionality principle for [[function types]] ([[function extensionality]]) states that for all functions $f:A \to B$ and $g:A \to B$, $f =_{A \to B} g$ if and only if for all $a:A$ and $b:A$ such that $a =_A b$, $f(a) =_{B} g(b)$

$$\forall f:A \to B.\forall g:A \to B.f =_{A \to B} g \iff \forall a:A. \forall b:A.a =_A b \implies (f(a) =_{B} g(b))$$

### Relation to heterogeneous propositional equality

Given elements $x:A$ and $y:A$ such that $x =_A y$ and $a:B(x)$ and $b:B(y)$, [[heterogeneous propositional equality]] is given by the relation $a =_{\underline{ }.B}^{x =_A y} b$. Given elements $x:A$, and for all $a:B(x)$ and $b:B(x)$, $a =_{\underline{ }.B}^{x =_A x} b$ if and only if $a =_{B(x)} b$

$$\forall a:B(x).\forall b:B(x). a =_{\underline{ }.B}^{x =_A x} b \iff a =_{B(x)} b$$

This is because by the introduction rules of propositional equality and heterogeneous propositional equality, we have that for all $a:B(x)$, $a =_{B(x)} a$ and $a =_{\underline{ }.B}^{x =_A x} a$, and since true propositions imply true propositions, we have $a =_{B(x)} a$ implies $a =_{\underline{ }.B}^{x =_A x} a$ and $a =_{\underline{ }.B}^{x =_A x} a$ implies $a =_{B(x)} a$. By the elimination rules for propositional equality, for all $a:B(x)$ and $b:B(x)$, we have $a =_{B(x)} b$ implies $a =_{\underline{ }.B}^{x =_A x} b$, and by the elimination rules for heterogeneous propositional equality, we have $a =_{\underline{ }.B}^{x =_A x} b$ implies $a =_{B(x)} b$. Thus, $a =_{\underline{ }.B}^{x =_A x} b$ if and only if $a =_{B(x)} b$. 

### Transport and the principle of substitution

The analogue of [[identity functions]] on a type $A$, a function $f:A \to A$ such that $x =_A f(x)$ for all elements $x:A$, is the notion of [[transport functions]] between a family of types $B(x)$ indexed by elements $x:A$. 

Given elements $x:A$ and $y:A$ such that $x =_A y$, a [[transport function]] is a function $f:B(x) \to B(y)$ such that for all $a:B(x)$, $a =_{\underline{ }.B}^{x =_A y} f(a)$

$$\forall a:B(x).a =_{\underline{ }.B}^{x =_A y} f(a)$$

These transport functions, if they exist, are [[uniqueness quantifier|unique up to equality]]. Suppose we have a second function $g:B(x) \to B(y)$ such that $x =_A y$ implies that for all $a:B(x)$, $a =_{\underline{ }.B}^{x =_A y} g(a)$. Then by symmetry and transitivity of heterogeneous equality, we have $f(a) =_{\underline{ }.B}^{y =_A y} g(a)$, which is logically equivalent to $f(a) =_{B(y)} g(a)$. Then by function extensionality, we have $f =_{B(x) \to B(y)} g$, which implies that transport functions, if they exist, are unique up to equality. 

Suppose that for all elements $x:A$ and $y:A$ such that $x =_A y$, there exists a transport function $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \to B(y)$. Then for all $a:B(x)$ and $b:B(y)$, $a =_{\underline{ }.B}^{x =_A y} b$ if and only if $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a) =_{B(y)} b$

$$\forall a:B(x).\forall b:B(y). a =_{\underline{ }.B}^{x =_A y} b \iff \mathrm{tr}_{\underline{ }.B}^{x =_A y}(a) =_{B(y)} b$$

In particular, this means that we have $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b) =_{B(x)} a$, and by the fact that functions preserve equality, $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)) =_{B(x)} \mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)$, which by transitivity of propositional equality implies that $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)) =_{B(x)} a$. Similarly, we have $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)) =_{B(y)} \mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)$, which by transitivity of propositional equality implies that $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)) =_{B(y)} b$. Thus, the transport functions $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \to B(y)$ and $\mathrm{tr}_{\underline{ }.B}^{y =_A x}:B(y) \to B(x)$ are [[inverse functions]] of each other, and thus both transport functions are [[bijections]], and could be written as $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \cong B(y)$ and $\mathrm{tr}_{\underline{ }.B}^{y =_A x}:B(y) \cong B(x)$ respectively. 

Thus, provided that [[transport functions]] exist, we have the following derivable rules for the [[principle of substitution]] of propositionally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{tr}_{\underline{ }.B}^{a =_A b}:B(a) \to B(b)}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A \vdash c(x):B(x)}{\Gamma \vdash \mathrm{tr}_{\underline{ }.B}^{a =_A b}(c(a)) =_{B(b)} c(b) \; \mathrm{true}}$$

### In computation and uniqueness rules

Propositional equality can be used in the [[computation rules]] and [[uniqueness rules]] of types in [[dependent type theory]]: 

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) =_{B(a)} b(a) \; \mathrm{true}}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f =_{\prod_{x:A} B(x)} \lambda(x).f(x) \; \mathrm{true}}$$

* Computation rules for negative dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) =_A a \; \mathrm{true}} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) =_{B(\pi_1(a, b))} b \; \mathrm{true}}$$

* Uniqueness rules for negative dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z =_{\sum_{x:A} B(x)} (\pi_1(z), \pi_2(z)) \; \mathrm{true}}$$

* Computation rules for identity types:

$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma \vdash t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x)) \quad \Gamma \vdash c:A}{\Gamma \vdash J(t, c, c, \mathrm{refl}(c)) =_{C(c, c, \mathrm{refl}_A(c))} t(c) \; \mathrm{true}}$$

## See also

* [[equality]]

* [[judgmental equality]], [[typal equality]]

* [[logic over dependent type theory]]

[[!redirects propositional equality]]
[[!redirects propositional equalities]]
[[!redirects propositionally equal]]