
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

The notion of [[logic over type theory]] for [[dependent type theories]]. 

The dependent type theory consisting of two levels, one level of [[propositions]] for the logic and a second level of [[types]] for the dependent type theory. 

## Formal presentation

It is possible to define [[definitional equality]] in [[dependent type theory]] in the logic layer, similar to [[propositional equality]] in [[set theory]], rather than as a separate judgment in the dependent type theory. 

For example, this presentation of dependent type theory uses a very weak [[logic]] over [[dependent type theory]], in the sense that while it does have a notion of [[proposition]], [[predicate]], and [[truth]], there are no [[conjunctions]], [[disjunctions]], [[implications]], [[universal quantifiers]], or [[existential quantifiers]] in the logic. Here, [[propositional equality]] plays the role of [[definitional equality]] and [[computational equality]] that [[judgmental equality]] played in the first presentation. 

### Judgments and contexts

The syntax of dependent type theory can be constructed in two stages. The first is the *raw* or *untyped* syntax of the theory consisting of expressions that are readable but not meaningful. The second stage consists of defining the *derivable judgements* of the type theory inductively which then pick out the meaningful contexts, types and terms.

A context is a list of types. Variables can be defined as De Bruijn indices in which case the type of a variable $n$ is given by $n$th type in a context.

One may also define contexts as coming with a variable name, in which case one needs a notion of $\alpha$-equivalence (syntactic identity modulo renaming of bound variables) and of capture-free substitution. De Bruijn indices avoid this step but can be more obfuscating.

Types and terms are built inductively from various constructors. Types, terms and contexts are defined mutually.

We have the basic judgement forms:

* $\Gamma \vdash A\; \mathrm{type}$ - $A$ is a well-typed type in context $\Gamma$.
* $\Gamma \vdash a : A$ - $a$ is a well-typed term of type $A$ in context $\Gamma$.
* $\Gamma \vdash \phi \; \mathrm{prop}$ - $\phi$ is a well-formed proposition in context $\Gamma$
* $\Gamma \vdash \phi \; \mathrm{true}$ - $\phi$ is a well-formed true proposition in context $\Gamma$
* $\Gamma \; \mathrm{ctx}$ - $\Gamma$ is a well-formed context. 

Contexts are defined by the following rules:

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash \phi \; \mathrm{prop}}{(\Gamma, \phi \; \mathrm{true}) \; \mathrm{ctx}}$$

### Structural rules

There are three structural rules in dependent type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

### Definitional equality

Definitional equality of types and terms is formed by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \equiv B \; \mathrm{prop}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash a \equiv_A b \; \mathrm{prop}}$$

Definitional equality has its own structural rules:  reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of definitional equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A \equiv A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv_A a \; \mathrm{true}}$$

* Symmetry of definitional equality

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A \equiv B \; \mathrm{true}}{\Gamma \vdash B \equiv A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash a \equiv_A b \; \mathrm{true}}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

* Transitivity of definitional equality

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash A \equiv B \; \mathrm{true} \quad \Gamma \vdash B \equiv C \; \mathrm{true}}{\Gamma \vdash A \equiv C \; \mathrm{true}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash c:A \quad \Gamma \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma \vdash b \equiv_A c \; \mathrm{true}}{\Gamma \vdash a \equiv_A c \; \mathrm{true}}$$

* Principle of substitution of definitionally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] \equiv B[b/x] \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a \equiv_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] \equiv_{B[b/x]} c[b/x] \; \mathrm{true}}$$

* Variable conversion rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A \equiv B \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

### Definitions

In addition, there are judgments for the initialization operator for types and for terms:

* $\Gamma \vdash A' \coloneqq A \; \mathrm{type}$ - $A'$ is defined to be the type $A$ in context $\Gamma$.
* $\Gamma \vdash a' \coloneqq a : A$ - $a'$ is defined to be the term $a:A$ of type $A$ in context $\Gamma$.

The initialization operator has its own structural rules: type formation, term introduction, and equality reflection.

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{true}}$$

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

### Rules for types

Each type in Martin-Löf dependent type theory comes with a type [[formation rule]], a term [[introduction rule]], a term [[elimination rule]], a [[computation rule]], and an optional [[uniqueness rule]]. The elimination rules we give here are not [[contextual elimination rules]], and the conversion rules given here are not [[contextual conversion rules]]. 

#### Function types

* Formation rules for function types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

* Introduction rules for function types:

$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \to B}$$

* Elimination rules for function types:

$$\frac{\Gamma \vdash f:A \to B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

* Computation rules for function types:

$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash (x \mapsto b(x))(a) \equiv_{B} b \; \mathrm{true}}$$

* Uniqueness rules for function types:

$$\frac{\Gamma \vdash f:A \to B}{\Gamma \vdash f \equiv_{A \to B} (x \mapsto f(x)) \; \mathrm{true}}$$

#### Dependent product types

* Formation rules for dependent product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

* Elimination rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B[a/x]}$$

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv_{B[a/x]} b[a/x] \; \mathrm{true}}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv_{\prod_{x:A} B(x)} \lambda(x).f(x) \; \mathrm{true}}$$

#### Product types

* Formation rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

* Introduction rules for product types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash (a, b):A \times B}$$

* Elimination rules for product types:

$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_2(z):B}$$

* Computation rules for product types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \pi_1(a, b) \equiv_A a \; \mathrm{true}} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \pi_2(a, b) \equiv_B b \; \mathrm{true}}$$

* Uniqueness rules for product types:

$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash z \equiv_{A \times B} (\pi_1(z), \pi_2(z)) \; \mathrm{true}}$$

#### Dependent sum types

* Formation rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_2(z):B(\pi_1(z))}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) \equiv_A a \; \mathrm{true}} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) \equiv_{B(\pi_1(a, b))} b \; \mathrm{true}}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv_{\sum_{x:A} B(x)} (\pi_1(z), \pi_2(z)) \; \mathrm{true}}$$

#### Sum types

* Formation rules for sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

* Introduction rules for sum types:

$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A + B}$$

* Elimination rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, c, d, e):C[e/z]}$$

* Computation rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, c, d, \mathrm{inl}(a)) \equiv_{C[\mathrm{inl}(a)/z]} c[a/x] \; \mathrm{true}}$$
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash b:B}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, c, d, \mathrm{inr}(b)) \equiv_{C[\mathrm{inr}(b)/z]} d[b/y] \; \mathrm{true}}$$

* Uniqueness rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B \vdash u:C \quad \Gamma, a:A \vdash u[\mathrm{inl}(a)/z] \equiv_{C[\mathrm{inl}(a)/z]} c[a/x] \; \mathrm{true} \quad \Gamma, b:B \vdash u[\mathrm{inr}(b)/z] \equiv_{C[\mathrm{inr}(b)/z]} d[b/y] \; \mathrm{true}}{\Gamma \vdash u[e/z] \equiv_{C[e/z]} \mathrm{ind}_{A + B}(z.C, c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e) \; \mathrm{true}}$$

#### Empty type

* Formation rules for the empty type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

* Elimination rules for the empty type:

$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}(x.C, p):C[p/x]}$$

* Uniqueness rules for the empty type:

$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0} \quad \Gamma, x:\mathbb{0} \vdash u:C}{\Gamma \vdash u[p/x] \equiv_{C[p/x]} \mathrm{ind}_\mathbb{0}(x.C, p) \; \mathrm{true}}$$

#### Unit type

* Formation rules for the unit type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

* Introduction rules for the unit type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

* Elimination rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1}}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, p, c_*):C[p/x]}$$

* Computation rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, *, c_*) \equiv_{C[*/x]} c_* \; \mathrm{true}}$$

* Uniqueness rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1} \quad \Gamma, x:\mathbb{1} \vdash u:C \quad \Gamma \vdash u[*/x] \equiv_{C[*/x]} c_* \; \mathrm{true}}{\Gamma \vdash u[p/x] \equiv_{C[p/x]} \mathrm{ind}_\mathbb{1}(x.C, p, c_*) \; \mathrm{true}}$$

#### Natural numbers

* Formation rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

* Introduction rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(n):\mathbb{N}}$$

* Elimination rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s):C[n/x]}$$

* Computation rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(0, c_0, c_s) \equiv_{C[0/x]} c_0 \; \mathrm{true}}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(s(n), c_0, c_s) \equiv_{C[s(n)/x]} c_s(n, \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s)) \; \mathrm{true}}$$

* Uniqueness rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N} \quad \Gamma, x:\mathbb{N} \vdash u:C \quad \Gamma \vdash i_0(u):u[0/x] =_{C[0/x]} c_0 \quad \Gamma, x:\mathbb{N} \vdash i_s(u):u[s(x)/x] =_{C[s(x)/x]} c_s[u/c]}{\Gamma \vdash u[n/x] =_{C[n/x]} \mathrm{ind}_\mathbb{N}^{C}(p, c_0, c_s) \; \mathrm{true}}$$

#### Identity types

There is another version of equality, called the [[identity type]] or **typal equality**, because this equality is a type. The identity type is only be used for equality between terms of a type, and unless one is using [[Russell universes]] where types are represented by terms of a [[Russell universe]], identity types cannot be used for equality of types. 

* Formation rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

* Introduction rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:

$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, a:A, b:A, p:a =_A b \vdash J(t, a, b, p):C}$$

* Computation rules for identity types:

$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, c:A \vdash J(t, c, c, \mathrm{refl}(c)) \equiv_{C[c/a, c/b, \mathrm{refl}_A(c)/p]} t \; \mathrm{true}}$$

* Optional uniqueness rules for identity types:

...

### Intensional and extensional type theories

In Martin-Löf dependent type theory, one makes a distinction between intensional and extensional type theories. A Martin-Löf dependent type theory is an [[extensional type theory]] if there is an equality reflection rule where from typal equality of terms, one could derive definitional equality of terms:

$$\frac{\Gamma, a:A, b:A \vdash p:a =_A b}{\Gamma, a:A, b:A \vdash a \equiv_A b \; \mathrm{true}}$$

The type theory is an [[intensional type theory]] if it doesn't have the equality reflection rule. 

### Propositional reflection and predicate logic

One could add an additional set of rules in this second presentation of Martin-Löf dependent type theory which isn't available in the first presentation: propositional reflections. Unlike the first presentation, in this presentation, there are two notions of propositions: the external propositions and the internal propositions. The external propositions are the judgmental propositions in the logic layer of Martin-Löf dependent type theory, and correspond to the external logic. On the other hand, the internal propositions are [[types]] equipped with a witness of the [[isProp]] [[modality]] and correspond to the [[internal logic]]. They are also called [[subsingletons]] or [[h-propositions]]. We could make the internal logic imply the external logic with the following proposition reflection rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \phi_A \; \mathrm{prop}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A) \quad \Gamma \vdash a:A}{\Gamma \vdash \phi_A \; \mathrm{true}}$$

and similar rules for [[predicates]]:

$$\frac{\Gamma, x:A, \Delta \vdash B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash p:\mathrm{isProp}(B)}{\Gamma, x:A, \Delta \vdash \phi_B \; \mathrm{prop}} \qquad \frac{\Gamma, x:A, \Delta \vdash B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash p:\mathrm{isProp}(B) \quad \Gamma, x:A, \Delta \vdash b:B}{\Gamma, x:A, \Delta \vdash \phi_B \; \mathrm{true}}$$

If the [[identity types]] of Martin-Löf dependent type theory have a uniqueness rule such as the [[K rule]] or [[uniqueness of identity proofs]], then propositional reflection implies that the type theory is an [[extensional type theory]]. 

In addition, since the [[product type]] and [[function type]] preserve types being a subsingleton, the dependent product of a subsingleton-valued type family, and the [[unit type]] and [[empty type]] are always subsingletons, one could also add the following propositional reflection rules to the theory, defining [[conjunction]], [[implication]], [[true]], [[false]], and bounded [[universal quantification]]:

$$\frac{\Gamma \vdash A \times B \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A) \quad \Gamma \vdash q:\mathrm{isProp}(B)}{\Gamma \vdash \phi_A \wedge \phi_B \; \mathrm{prop}}$$ 
$$\frac{\Gamma \vdash A \to B \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A) \quad \Gamma \vdash q:\mathrm{isProp}(B)}{\Gamma \vdash \phi_A \implies \phi_B \; \mathrm{prop}}$$
$$\frac{\Gamma \vdash \mathbb{0} \; \mathrm{type}}{\Gamma \vdash \bot \; \mathrm{prop}} \qquad \frac{\Gamma \vdash \mathbb{1} \; \mathrm{type}}{\Gamma \vdash \top \; \mathrm{prop}}$$
$$\frac{\Gamma, \Delta \vdash \prod_{x:A} B(x) \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash q:\mathrm{isProp}(B(x))}{\Gamma, \Delta \vdash \forall x:A.\phi_B(x) \; \mathrm{prop}}$$

Adding [[propositional truncations]] to Martin-Löf dependent type theory allows for the full [[intuitionistic logic]] to be defined, as [[disjunctions]] could be defined from the propositional truncation of the [[sum type]], and the [[existential quantifier]] could be defined from the propositional truncation of the [[dependent sum type]]:

$$\frac{\Gamma \vdash [A + B] \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isProp}(A) \quad \Gamma\vdash q:\mathrm{isProp}(B)}{\Gamma \vdash \phi_A \vee \phi_B \; \mathrm{prop}}$$ 
$$\frac{\Gamma, \Delta \vdash \left[\sum_{x:A} B(x)\right] \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash q:\mathrm{isProp}(B(x))}{\Gamma, \Delta \vdash \exists x:A.\phi_B(x) \; \mathrm{prop}}$$

The rules above reflect the [[propositions as some types]] philosophy in [[type theory]]. 

### Bounded separation

A predicate on a type $A$ is a proposition $P \; \mathrm{prop}$ in the context of the free variable $x:A$. Bounded separation states that given a predicate $P$ on a set $A$, one could construct the set $\vert P \vert$ with an injection $i:\vert P \vert \hookrightarrow A$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma \vdash \vert P \vert \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma \vdash i:\vert P \vert \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma, x:A, y:A \vdash \varphi_{x =_A y} \iff \varphi{i(x) =_B i(y)} \; \mathrm{true}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash P \; \mathrm{prop}}{\Gamma, x \in A \vdash P(x) \iff \varphi_{\sum_{y:\vert P \vert} i(y) = x} \; \mathrm{true}}$$

### Propositions as types

An alternative to the [[propositions as some types]] philosophy is the [[propositions as types]] philosophy, where instead of reflecting the [[subsingletons]] to propositions and the [[singletons]] to true propositions, we reflect all types to propositions, and the [[pointed types]] to true propositions. The rules are given as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \phi_A \; \mathrm{prop}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \phi_A \; \mathrm{true}}$$

and similar rules for [[predicates]]:

$$\frac{\Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, x:A, \Delta \vdash \phi_B \; \mathrm{prop}} \qquad \frac{\Gamma, x:A, \Delta \vdash B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash b:B}{\Gamma, x:A, \Delta \vdash \phi_B \; \mathrm{true}}$$

There is no need for [[propositional truncations]] in this interpretation: the full [[intuitionistic logic]] results from reflecting all type formers except for the [[natural numbers type]] and [[identity types]]:

$$\frac{\Gamma \vdash A + B \; \mathrm{type}}{\Gamma \vdash \phi_A \vee \phi_B \; \mathrm{prop}}$$ 
$$\frac{\Gamma \vdash A \times B \; \mathrm{type}}{\Gamma \vdash \phi_A \wedge \phi_B \; \mathrm{prop}}$$ 
$$\frac{\Gamma \vdash A \to B \; \mathrm{type}}{\Gamma \vdash \phi_A \implies \phi_B \; \mathrm{prop}}$$
$$\frac{\Gamma \vdash \mathbb{0} \; \mathrm{type}}{\Gamma \vdash \bot \; \mathrm{prop}} \qquad \frac{\Gamma \vdash \mathbb{1} \; \mathrm{type}}{\Gamma \vdash \top \; \mathrm{prop}}$$
$$\frac{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}{\Gamma \vdash \exists x:A.\phi_B(x) \; \mathrm{prop}}$$
$$\frac{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}{\Gamma \vdash \forall x:A.\phi_B(x) \; \mathrm{prop}}$$

## Related concepts

* [[type theory]], [[logic over type theory]]

* [[Martin-Löf type theory]]

* [[type theory with shapes]]

* [[propositional logic]], [[predicate logic]]

* [[propositional logic as a dependent type theory]]

* [[higher order logic as a dependent type theory]]

* [[dependently sorted set theory]]

* [[propositional equality]], [[definitional equality]]

* [[propositions as types]]

[[!redirects logic over dependent type theory]]
[[!redirects logic over dependent type theories]]
