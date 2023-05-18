+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

[[Per Martin-Lof|Per Martin-Löf]]'s **[[dependent type theory]]**, also known as **[[intuitionistic logic|intuitionistic]] type theory** ([Martin-Löf 75](#MartinLof75)), or **constructive type theory** is a specific form of [[type theory]] developed to support [[constructive mathematics]].  (Note that both "dependent type theory" and "intuitionistic type theory" may refer more generally to [[type theories]] that contain [[dependent types]] or are [[intuitionistic mathematics|intuitionistic]], respectively.)

Martin-L&#246;f's dependent type theory is notable for several reasons: 

* One can construct an interpretation of first-order [[intuitionistic logic]] by interpreting [[propositions as types]] (this is true of most any dependent type theory).

* It has a version of a variant of the [[axiom of choice]] _as a theorem_ (because of the properties of the above interpretation), see the discussion [below](#AxiomOfChoice).

* In its [[intensional type theory|intensional]] form, it has sufficient computational content to function as a programming language. At the same time, it then has [[identity types]] whose presence shows that one is really dealing with a form of [[homotopy type theory]].

## Formal presentations

There are many different ways to present Martin-Löf dependent type theory in a formal system. In this article, we give two formal presentations of Martin-Löf dependent type theory in the framework of [[natural deduction]], one which has [[judgmental equality]] and only one level, and another which has a very weak [[logic]] over the [[dependent type theory]] as well as [[propositional equality]]. 

### Presentation 1

This first presentation uses [[judgmental equality]], and could be contrasted with the second presentation, which uses [[propositional equality]] and a very weak [[logic]] over [[dependent type theory]]. 



#### Judgments and contexts
 {#JudgmentsAndContexts}

The [[syntax]] of Martin-Löf dependent type theory can be constructed in two stages: 

* The first is the *raw* or *untyped* syntax of the theory consisting of expressions that are readable but not necessarily meaningful. 

* The second stage consists of defining the *derivable judgements* of the type theory [[induction|inductively]] which then pick out the meaningful [[contexts]], [[types]] and [[terms]].

A [[context]] is a [[list]] of succesivley [[dependent types]]. The [[variables]] may be defined as [[de Bruijn indices]], in which case the type of a variable $n$ is given by $n$th type in a [[context]].

One may also define contexts as coming with a variable name, in which case one needs a notion of $\alpha$-equivalence (syntactic identity modulo renaming of bound variables) and of capture-free substitution. De Bruijn indices avoid this step but can be more obfuscating.

Types and terms are built inductively from various constructors. Types, terms and contexts are defined mutually.

We have the basic [[judgement]] forms:

* $\Gamma \; \mathrm{ctx}$ 

  saying that: "$\Gamma$ is a well-formed context";

* $\Gamma \vdash A\; \mathrm{type}$ 

  saying that "$A$ is a well-typed [[dependent type]] in [[context]] $\Gamma$";

* $\Gamma \vdash a : A$ 

  saying that "$a$ is a well-typed [[term]] of [[type]] $A$ in [[context]] $\Gamma$";

The following table indicates the corresponding [[categorical semantics]] [[categorical semantics of dependent types|of these notions of dependent type theory]]:

<center>
<img src="/nlab/files/DependentTermsSyntaxAndSemantics-230326.jpg" width="650">
</center>


We work in the [[logical framework]] of [[natural deduction]], where everything is given by [[inference rules]]. 

To start with, [[contexts]] are built from [[dependent types]] by the following rules (cf. [[type telescope]]):

$$
  \frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}
$$


#### Structural rules
 {#StructuralRules}

Among the *[[structural rules]]* of dependent type theory are (e.g. [Jacobs (1998), p. 122](#Jacobs98), [UFP13, A.2.2](#UFP13), [Rijke (2018), Sec. 1.4](#Rijke18)):

* the [[variable rule]], 

* the [[weakening rule]], 

* the [[substitution rule]]

shown in the following table together with their [[categorical semantics]] [[categorical semantics of dependent types|of dependent types]]:

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>

The weakening and substitution rules are [[admissible rules]]: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

#### Definitional equality

In addition, there are judgments for definitional equality of types and of terms:

* $\Gamma \vdash A \equiv A' \; \mathrm{type}$ - $A$ and $A'$ are judgementally equal well-typed types in context $\Gamma$.
* $\Gamma \vdash a \equiv a' : A$ - $a$ and $a'$ are judgementally equal well-typed terms of type $A$ in context $\Gamma$.

Definitional equality has its own structural rules: reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of definitional equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A \equiv A \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv a:A}$$

* Symmetry of definitional equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b \equiv a:A}$$

* Transitivity of definitional equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash B \equiv C \; \mathrm{type} }{\Gamma \vdash A \equiv C \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A \quad b \equiv c:A }{\Gamma \vdash a \equiv c:A}$$

* Principle of substitution of definitionally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] \equiv c[b/x]: B[b/x]}$$

* Variable conversion rule:
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

#### Definitions

In addition, there are judgments for the initialization operator for types and for terms:

* $\Gamma \vdash A' \coloneqq A \; \mathrm{type}$ - $A'$ is defined to be the type $A$ in context $\Gamma$.
* $\Gamma \vdash a' \coloneqq a : A$ - $a'$ is defined to be the term $a:A$ of type $A$ in context $\Gamma$.

The initialization operator has its own structural rules: type formation, term introduction, and equality reflection.

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

#### Rules for types

Each type in Martin-Löf dependent type theory comes with a type [[formation rule]], a term [[introduction rule]], a term [[elimination rule]], a [[computation rule]], and an optional [[uniqueness rule]]. The elimination rules we give here are not [[contextual elimination rules]], and the conversion rules given here are not [[contextual conversion rules]]. 

#### Function types

* Formation rules for function types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

* Introduction rules for function types:

$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \to B}$$

* Elimination rules for function types:

$$\frac{\Gamma \vdash f:A \to B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

* Computation rules for function types:

$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash (x \mapsto b(x))(a) \equiv b:B}$$

* Uniqueness rules for function types:

$$\frac{\Gamma \vdash f:A \to B}{\Gamma \vdash f \equiv (x \mapsto f(x)):A \to B}$$

#### Dependent product types

* Formation rules for dependent product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

* Elimination rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B[a/x]}$$

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv b[a/x]:B[a/x]}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

#### Product types

* Formation rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

* Introduction rules for product types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash (a, b):A \times B}$$

* Elimination rules for product types:

$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:A \times B}{\Gamma \vdash \pi_2(z):B}$$

* Computation rules for product types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \pi_2(a, b) \equiv b:B}$$

* Uniqueness rules for product types:

$$\frac{\Gamma \vdash z:A \times B}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):A \times B}$$

#### Dependent sum types

* Formation rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent sum types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_2(z):B(\pi_1(z))}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash \pi_2(a, b) \equiv b:B(\pi_1(a, b))}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

#### Sum types

* Formation rules for sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A + B \; \mathrm{type}}$$

* Introduction rules for sum types:

$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A + B}$$

* Elimination rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A + B}{\Gamma \vdash \mathrm{ind}_{A + B}^C(c(x), d(y), e):C(e)}$$

* Computation rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{A + B}^C(c(x), d(y), \mathrm{inl}(a)) \equiv c(a):C(\mathrm{inl}(a))}$$
$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash b:B}{\Gamma \vdash \mathrm{ind}_{A + B}^C(c(x), d(y), \mathrm{inr}(b)) \equiv d(b):C(\mathrm{inr}(b))}$$

* Uniqueness rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A + B \quad \Gamma, x:A + B \vdash u:C \quad \Gamma, a:A \vdash u(\mathrm{inl}(a)) \equiv c(a):C(\mathrm{inl}(a)) \quad \Gamma, b:B \vdash u(\mathrm{inr}(b)) \equiv d(b):C(\mathrm{inr}(b))}{\Gamma \vdash u(e) \equiv \mathrm{ind}_{A + B}^C(c(\mathrm{inl}(e)), d(\mathrm{inl}(e)), e):C(e)}$$

#### Empty type

* Formation rules for the empty type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{0} \; \mathrm{type}}$$

* Elimination rules for the empty type:

$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}^C(p):C(p)}$$

* Uniqueness rules for the empty type:

$$\frac{\Gamma, x:\mathbb{0} \vdash C \; \mathrm{type} \quad \Gamma \vdash p:\mathbb{0} \quad \Gamma, x:\mathbb{0} \vdash u:C}{\Gamma \vdash u[p/x] \equiv \mathrm{ind}_\mathbb{0}^{C}(p):C[p/x]}$$

#### Unit type

* Formation rules for the unit type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

* Introduction rules for the unit type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

* Elimination rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1}}{\Gamma \vdash \mathrm{ind}_\mathbb{1}^C(p, c_*):C[p/x]}$$

* Computation rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{1}^C(*, c_*) \equiv c_*:C[*/x]}$$

* Uniqueness rules for the unit type:

$$\frac{\Gamma, x:\mathbb{1} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\mathbb{1} \quad \Gamma, x:\mathbb{1} \vdash u:C \quad \Gamma \vdash u[*/x] \equiv c_*:C[*/x]}{\Gamma \vdash u[p/x] \equiv \mathrm{ind}_\mathbb{1}^{C}(p, c_*):C[p/x]}$$

#### Natural numbers

* Formation rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

* Introduction rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(n):\mathbb{N}}$$

* Elimination rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s):C[n/x]}$$

* Computation rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(0, c_0, c_s) \equiv c_0:C[0/x]}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(s(n), c_0, c_s) \equiv c_s(n, \mathrm{ind}_\mathbb{N}^C(n, c_0, c_s)):C[s(n)/x]}$$

* Uniqueness rules for the natural numbers:
$$\frac{\Gamma, x:\mathbb{N} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, c:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N} \quad \Gamma, x:\mathbb{N} \vdash u:C \quad \Gamma \vdash i_0(u):u[0/x] =_{C[0/x]} c_0 \quad \Gamma, x:\mathbb{N} \vdash i_s(u):u[s(x)/x] =_{C[s(x)/x]} c_s[u/c]}{\Gamma \vdash u[n/x] \equiv \mathrm{ind}_\mathbb{N}^{C}(p, c_0, c_s):C[n/x]}$$

#### Identity types

There is another version of equality, called the [[identity type]] or **typal equality**, because this equality is a type. The identity type is only be used for equality between terms of a type, and unless one is using [[Russell universes]] where types are represented by terms of a [[Russell universe]], identity types cannot be used for equality of types. 

* Formation rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

* Introduction rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, a:A, b:A, p:a =_A b \vdash J(t, a, b, p):C}$$

* Computation rules for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C \; \mathrm{type} \quad \Gamma, c:A \vdash t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}{\Gamma, c:A \vdash J(t, c, c, \mathrm{refl}(c)) \equiv t:C[c/a, c/b, \mathrm{refl}_A(c)/p]}$$

* Optional uniqueness rules for identity types:

...

#### Intensional and extensional type theories

In Martin-Löf dependent type theory, one makes a distinction between intensional and extensional type theories. A Martin-Löf dependent type theory is an [[extensional type theory]] if there is an equality reflection rule where from typal equality of terms, one could derive definitional equality of terms:

$$\frac{\Gamma, a:A, b:A \vdash p:a =_A b}{\Gamma, a:A, b:A \vdash a \equiv b:A}$$

The type theory is an [[intensional type theory]] if it doesn't have the equality reflection rule. 

### Presentation 2

This presentation of Martin-Löf dependent type theory uses  a very weak [[logic]] over [[dependent type theory]], in the sense that while it does have a notion of [[proposition]], [[predicate]], and [[truth]], there are no [[conjunctions]], [[disjunctions]], [[implications]], [[universal quantifiers]], or [[existential quantifiers]] in the logic. Here, [[propositional equality]] plays the role of [[definitional equality]] and [[computational equality]] that [[judgmental equality]] played in the first presentation. 

#### Judgments and contexts

The syntax of Martin-Löf dependent type theory can be constructed in two stages. The first is the *raw* or *untyped* syntax of the theory consisting of expressions that are readable but not meaningful. The second stage consists of defining the *derivable judgements* of the type theory inductively which then pick out the meaningful contexts, types and terms.

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

#### Structural rules

There are three structural rules in dependent type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

#### Definitional equality

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

#### Definitions

In addition, there are judgments for the initialization operator for types and for terms:

* $\Gamma \vdash A' \coloneqq A \; \mathrm{type}$ - $A'$ is defined to be the type $A$ in context $\Gamma$.
* $\Gamma \vdash a' \coloneqq a : A$ - $a'$ is defined to be the term $a:A$ of type $A$ in context $\Gamma$.

The initialization operator has its own structural rules: type formation, term introduction, and equality reflection.

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{true}}$$

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

#### Rules for types

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

#### Intensional and extensional type theories

In Martin-Löf dependent type theory, one makes a distinction between intensional and extensional type theories. A Martin-Löf dependent type theory is an [[extensional type theory]] if there is an equality reflection rule where from typal equality of terms, one could derive definitional equality of terms:

$$\frac{\Gamma, a:A, b:A \vdash p:a =_A b}{\Gamma, a:A, b:A \vdash a \equiv_A b \; \mathrm{true}}$$

The type theory is an [[intensional type theory]] if it doesn't have the equality reflection rule. 

#### Propositional reflection and predicate logic

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

#### Bounded separation

A predicate on a type $A$ is a proposition $P \; \mathrm{prop}$ in the context of the free variable $x:A$. Bounded separation states that given a predicate $P$ on a set $A$, one could construct the set $\vert P \vert$ with an injection $i:\vert P \vert \hookrightarrow A$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma \vdash \vert P \vert \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma \vdash i:\vert P \vert \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{prop}}{\Gamma, x:A, y:A \vdash \varphi_{x =_A y} \iff \varphi{i(x) =_B i(y)} \; \mathrm{true}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash P \; \mathrm{prop}}{\Gamma, x \in A \vdash P(x) \iff \varphi_{\sum_{y:\vert P \vert} i(y) = x} \; \mathrm{true}}$$

#### Propositions as types

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

## Properties

### Models and categorical semantics

The [[models]] of ML type theory depend crucially on whether one considers
the variant of [[extensional type theory]] or that of [[intensional type theory]].

The models of the extensional version are (just) [[locally cartesian closed categories]].

The faithful models of the intensional version with [[identity types]] are however certain [[(∞,1)-categories]], notably [[(∞,1)-toposes]], presented by [[simplicial model categories]] ([Warren](#Warren)). For this reason one speaks of _[[homotopy type theory]]_.

For a more detailed discussion of these matters see at _[[relation between type theory and category theory]]_.


### Axiom of choice
 {#AxiomOfChoice}

In dependent type theory we can verify the following "logical form of the [[axiom of choice]]" ([Bell](#Bell), [Tait](#Tait)), see also ([Rijke, section 2.5.1](#Rijke)).

+-- {: .num_theorem }
###### Theorem 
**(ACL)**

$$
  x : A, y : B(x) \vdash C(x, y) : Type
  \;
  \vdash 
  \;
  acl
  :
  (\forall x : A) (\exists y : B(x)) C(x, y) \to (\exists f : (\Pi x : A)B(x) )(\forall x : A) C(x, \mathrm{apply}(f, x)) 
  \,.
$$

=--

One should note carefully that this "is" only "the axiom of choice" under the above propositions-as-types interpretation of the quantifiers $\forall$ and $\exists$.  

+-- {: .num_remark}
###### Remark

In the [[categorical semantics]] of this expression, using the 
[[propositions-as-types]] logic corresponds roughly to working with the [[subobject lattices]] in the [[ex/lex completion]] of a [[locally cartesian closed category]]; the ACL then follows since every object of the original category becomes [[projective object|projective]] in its ex/lex completion.

=--

+-- {: .num_remark}
###### Remark

If we use instead a different logic over the same type theory, such as [[bracket types]] to model the actual subobject lattices in an arbitrary 
[[locally cartesian closed category|lccc]] (not necessarily the ex/lex completion of anything), or the 
[[hProp]] logic in [[homotopy type theory]], then the ACL in that logic will not be derivable.

=--


## Related concepts

* [[initiality conjecture]]

[[!include notions of type]]


## References
 {#References}

See also the references at _[[type theory]]_ and at *[[dependent type theory]]*.

The original articles:

* [[Per Martin-Löf]], *A Theory of Types*, unpublished note (1971) &lbrack;[pdf](https://raw.githubusercontent.com/michaelt/martin-lof/master/pdfs/martin-loef1971%20-%20A%20Theory%20of%20Types.pdf), [[MartinLoef1971-ATheoryOfTypes.pdf:file]]&rbrack;

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80**, Elsevier (1975) 73-118 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926)&rbrack;

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) ([pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]])

As a [[programming language]]:

* [[Per Martin-Löf]], *Constructive Mathematics and Computer Programming*, in: *Proceedings of the Sixth International Congress of Logic, Methodology and Philosophy of Science (1979)*, Studies in Logic and the Foundations of Mathematics **104** (1982) 153-175 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>, [ISBN:978-0-444-85423-0](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/104/suppl/C)&rbrack;

* Bengt Nordström, Kent Petersson, Jan M. Smith, *Programming in Martin-Löf's Type Theory*, Oxford University Press 1990 ([webpage](http://www.cse.chalmers.se/research/group/logic/book/), [pdf](http://www.cse.chalmers.se/research/group/logic/book/book.pdf))

Further discussion:

* {#Hofmann95} [[Martin Hofmann]], *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

also published as:

* [[Martin Hofmann]], *Syntax and semantics of dependent types*, in *Semantics and logics of computation*, Publ. Newton Inst. **14**, Cambridge Univ. Press (1997) 79-130 &lbrack;[doi:10.1017/CBO9780511526619.004](https://doi.org/10.1017/CBO9780511526619.004)&rbrack;

Textbook accounts on general [[dependent type theory]]:

* {#Thompson91} [[Simon Thompson]], §6.3 in: *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)&rbrack;

* {#Jacobs98} [[Bart Jacobs]], Chapter 10 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], §A of *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])


A philosophical examination:

* [[Göran Sundholm​]], _Proof Theory and Meaning_ (1986), ([pdf](https://openaccess.leidenuniv.nl/bitstream/handle/1887/11978/9_05?sequence=1))

An introduction and survey (with an eye towards [[homotopy type theory]]):

* {#Warren} [[Michael Warren]], chapter 1 of: _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))
 
as well as

* {#Rijke} [[Egbert Rijke]], _Homotopy type theory_ (2012) ([pdf](http://hottheory.files.wordpress.com/2012/08/hott2.pdf))
 

A discussion of ML dependent type theory as the [[internal language]] of [[locally cartesian closed categories]] is in 

* [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

Discussion of the logical [[axiom of choice]] in dependent type theory is in 

* {#Bell} John Bell, _The Axiom of choice in type theory_, Stanford Encyclopedia of philosophy, 2008 ([web](http://plato.stanford.edu/entries/axiom-choice/choice-and-type-theory.html)) 
 

* {#Tait} Tait (1994)



[[!redirects Martin-Löf type theory]]
[[!redirects Martin-Löf type theories]]
[[!redirects Martin-Löf dependent type theories]]

[[!redirects Martin-Löf's dependent type theory]]
[[!redirects Martin-Löf's dependent type theories]]


[[!redirects Martin-Lof type theory]]
[[!redirects Martin-Lof type theories]]
[[!redirects Martin-Lof dependent type theory]]
[[!redirects Martin-Löf dependent type theory]]


[[!redirects Martin-Loef type theory]]
[[!redirects Martin-Loef type theories]]
[[!redirects Martin-Loef dependent type theory]]
[[!redirects Martin-Loef dependent type theories]]


[[!redirects constructive type theory]]

[[!redirects intuitionistic type theory]]
[[!redirects intuitionistic type theories]]

[[!redirects intuitionistic dependent type theory]]
[[!redirects intuitionistic dependent type theories]]


[[!redirects MLTT]]


