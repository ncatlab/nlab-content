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

\section{Idea}

In [[type theory]], there is a principle known as [[propositions as types]], which says that [[propositions]] and [[types]] are essentially the same: a proposition is identified with the type of all its [[proofs]], and a type is identified with the proposition that it has a term. 

However, this principle fails in many models of [[dependent type theory]], including the most widely used frameworks of type theories, such as [[Martin-Löf type theory]] and [[cubical type theory]], and the [[homotopy type theories]] based upon the two frameworks. Instead, they follow the weaker [[propositions as some types]] principle: while every proposition is interpreted as a type, not every type is interpreted as a proposition: only the [[(-1)-truncated]] types are interpreted as propositions (see [[h-proposition]] for more details). 

In this article, we create a dependent type theory where the full [[propositions as types]] principle holds: every type is an [[h-proposition]]. In particular, proofs have equality propositions, represented by the [[identity types]], and every proposition is [[propositional truncation|propositionally truncated]], represented in this article by two rules equivalent to two definitions of [[isProp]] in [[dependent type theory]]. In addition, we add rules for the [[empty type]] corresponding to [[false]], the [[unit type]] corresponding to [[true]], [[sum types]] corresponding to [[disjunction]], [[product types]] corresponding to [[conjunction]], [[function types]] corresponding to [[implication]], as well as [[negations]] to the dependent type theory, yielding a model of [[intuitionistic logic|intuitionistic]] [[propositional logic]]. Finally, adding [[excluded middle]] or the [[double negation law]] yields a model of [[classical logic|classical]] propositional logic. 

\section{Presentation}

The [[dependent type theory]] we shall be presenting here is similar to [[objective type theory]] of [[Benno van den Berg]] and [[Martijn den Besten]], in that it doesn't have [[definitional equality]]. The lack of [[definitional equality]] means that the theory is both simpler, and behaves more like traditional [[propositional logic]], which usually also doesn't have definitional equality. 

\subsection{Judgments and contexts}

The dependent type theory model of propositional logic  consists of three judgments: proposition judgments $A \; \mathrm{prop}$, where we judge $A$ to be a proposition, proof judgments, where we judge $a$ to be a proof of $A$, $a:A$, and context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. Contexts are lists of proof judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the rules for the empty context and extending the context by a proof judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{prop}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

\subsection{Structural rules}

The structural rules of this theory include the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a proof judgment if the proof judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

\subsection{Dependent propositions and dependent proofs}

A dependent proposition is a proposition $B$ in the context of the variable judgment $x:A$, $x:A \vdash B \; \mathrm{prop}$, they are sometimes written as $B(x)$. A dependent proof is a proof $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. dependent proofs are likewise sometimes written as $b(x)$. 

\subsection{Equality of proofs}

Equality of proofs of a proposition is represented by a proposition. This in other [[dependent type theories]] is called a [[identity type]] or a [[path type]]. Equality of proofs comes with a formation rule, an introduction rule, an elimination rule, and a computation rule:

Formation rule for equality of proofs:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{prop}}$$

Introduction rule for equality of proofs:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Elimination rule for equality of proofs:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{prop} \quad \Gamma, a:A \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b \vdash J(t, a, b, p):C(a, b, p)}$$

Computation rules for equality of proofs:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{prop} \quad \Gamma, a:A \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b \vdash \beta_{=_A}(a) : J(t, a, a, \mathrm{refl}(a)) =_{C(a, a, \mathrm{refl}_A(a))} t}$$

\subsection{Propositional truncation}

One also adds the propositional truncation rule for propositions:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, b:A \vdash \mathrm{proptrunc}_A:a =_A b}$$

One could equivalently adds the point contraction rule for propositions with a proof:
$$\frac{\Gamma \vdash A \; \mathrm{prop} \quad \Gamma \vdash a:A}{\Gamma, b:A \vdash \mathrm{contr}_A:a =_A b}$$
which states that the given proof is a [[center of contraction]]. 

Both rules ensure that every proposition behaves like an h-proposition in dependent type theory. 

\subsection{False}

The proposition false is the [[empty type]] in [[dependent type theory]]; thus the rules for false are the same as the rules for the empty type in other dependent type theories. 

Formation rules for false:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \bot \; \mathrm{prop}}$$

Elimination rules for false:
$$\frac{\Gamma, x:\bot \vdash C \; \mathrm{prop} \quad \Gamma \vdash p:\bot}{\Gamma \vdash \mathrm{ind}_\bot^C(p):C(p)}$$

Uniqueness rules for false:
$$\frac{\Gamma, x:\bot \vdash C \; \mathrm{prop} \quad \Gamma \vdash p:\bot \quad \Gamma, x:\bot \vdash u:C}{\Gamma \vdash \eta_\bot(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\bot^{C}(p)}$$

\subsection{True}

The proposition true is the [[unit type]] in [[dependent type theory]]; thus the rules for true are the same as the rules for the unit type in other dependent type theories. 

Formation rules for true:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \top \; \mathrm{prop}}$$

Introduction rules for true:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\top}$$

Elimination rules for true:
$$\frac{\Gamma, x:\top \vdash C \; \mathrm{prop} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\top}{\Gamma \vdash \mathrm{ind}_\top^C(p, c_*):C[p/x]}$$

Computation rules for true:
$$\frac{\Gamma, x:\top \vdash C \; \mathrm{prop} \quad \Gamma \vdash c_*:C[*/x]}{\Gamma \vdash \beta_\top: \mathrm{ind}_\top^C(*, c_*) =_{C[*/x]} c_*}$$

Uniqueness rules for true:
$$\frac{\Gamma, x:\top \vdash C \; \mathrm{prop} \quad \Gamma \vdash c_*:C[*/x] \quad \Gamma \vdash p:\top \quad \Gamma, x:\top \vdash u:C \quad \Gamma \vdash i_*(u):u[*/x] =_{C[*/x]} c_*}{\Gamma \vdash \eta_\top(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\top^{C}(p, c_*)}$$

\subsection{Disjunctions}

The disjunction of two propositions is represented by the [[sum type]] in [[dependent type theory]]. However, in other dependent type theories, while it isn't possible to prove that the sum type of two [[h-propositions]] is indeed a h-proposition, the requirement that all types be propositionally truncated in propositional logic means that the disjunction of two propositions is a propositional truncation. In particular, the sum type of the unit type with itself is the [[booleans type]], but the equivalent of the booleans type in propositional logic, the disjunction of true with itself, is a proposition because of propositional truncation, and can be proven to be equivalent to true. 

Formation rules for disjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{prop} \quad \Gamma \vdash B \; \mathrm{prop}}{\Gamma \vdash A \vee B \; \mathrm{prop}}$$

Introduction rules for disjunctions:
$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A \vee B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A \vee B}$$

Elimination rules for disjunctions:
$$\frac{\Gamma, z:A \vee B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A \vee B}{\Gamma \vdash \mathrm{ind}_{A \vee B}^C(c(x), d(y), e):C(e)}$$

Computation rules for disjunctions:
$$\frac{\Gamma, z:A \vee B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_1:\mathrm{ind}_{A \vee B}^C(c(x), d(y), \mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a)}$$
$$\frac{\Gamma, z:A \vee B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_2:\mathrm{ind}_{A \vee B}^C(c(x), d(y), \mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}$$

Uniqueness rules for disjunctions:
$$\frac{\Gamma, z:A \vee B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c(x):C(\mathrm{inl}(x)) \quad \Gamma, y:B \vdash d(y):C(\mathrm{inr}(y)) \quad \Gamma \vdash e:A \vee B \quad \Gamma, x:A \vee B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{inl}(u):u(\mathrm{inl}(a)) =_{C(\mathrm{inl}(a))} c(a) \quad \Gamma, b:B \vdash i_\mathrm{inr}(u):u(\mathrm{inr}(b)) =_{C(\mathrm{inr}(b))} d(b)}{\Gamma \vdash \eta_{A \vee B}:u(e) =_{C(e)} \mathrm{ind}_{A \vee B}^C(c(\mathrm{inl}(e)), d(\mathrm{inl}(e)), e)}$$

\subsection{Conjunctions}

The conjunction of two propositions is the [[product type]] in [[dependent type theory]]; thus the rules for conjunctions are the same as the rules for the product type in other dependent type theories. 

Formation rules for conjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{prop} \quad \Gamma \vdash B \; \mathrm{prop}}{\Gamma \vdash A \wedge B \; \mathrm{prop}}$$

Introduction rules for conjunctions:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash (a, b):A \wedge B}$$

Elimination rules for conjunctions:
$$\frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \pi_2(z):B}$$

Computation rules for conjunctions:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\wedge 1}:\pi_1(a, b) =_A a} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\wedge 2}:\pi_2(a, b) =_B b}$$

Uniqueness rules for conjunctions:
$$\frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \eta_\wedge:z =_{A \wedge B} (\pi_1(z), \pi_2(z))}$$

\subsection{Implications}

The implication of two propositions is the [[function type]] in [[dependent type theory]]; thus the rules for implications are the same as the rules for the product type in other dependent type theories. 

Formation rules for implications:
$$\frac{\Gamma \vdash A \; \mathrm{prop} \quad \Gamma \vdash B \; \mathrm{prop}}{\Gamma \vdash A \implies B \; \mathrm{prop}}$$

Introduction rules for implications:
$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \implies B}$$

Elimination rules for implications:
$$\frac{\Gamma \vdash f:A \implies B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

Computation rules for implications:
$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\implies}:(x \mapsto b(x))(a) =_{B} b}$$

Uniqueness rules for implications:
$$\frac{\Gamma \vdash f:A \implies B}{\Gamma \vdash \eta_{\implies}:f =_{A \implies B} (x \to f(x))}$$

\subsection{Negations}

A negation is just an implication of false. However, we introduce separate rules for negations specifically for the use of the notation $\neg A$ rather than the longer $A \implies \bot$. 

Formation rules for negations:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma \vdash \neg A  \; \mathrm{prop}}$$

Introduction rules for negations:
$$\frac{\Gamma, x:A \vdash b(x):\bot}{\Gamma \vdash (x \mapsto b(x)):\neg A}$$

Elimination rules for negations:
$$\frac{\Gamma \vdash f:\neg A \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):\bot}$$

Computation rules for negations:
$$\frac{\Gamma, x:A \vdash b(x):\bot \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\neg}:(x \mapsto b(x))(a) =_{\bot} b}$$

Uniqueness rules for negations:
$$\frac{\Gamma \vdash f:\neg A}{\Gamma \vdash \eta_{\implies}:f =_{\neg A} (x \to f(x))}$$

The above rules makes the dependent type theory into a model of intuitionistic propositional logic. 

\subsection{Decidable and stable propositions}

A proposition $A$ is said to be **decidable** or satisfy **[[excluded middle]]** if there is a proof $p:A \vee \neg A$. $A$ is said to be **stable** or satisfy the **[[double negation law]]** if there is a proof $p:\neg \neg A \implies A$. Every decidable propositions is stable, and every stable proposition is decidable, which means that the two notions are equivalent to each other. 

If every proposition is decidable or stable, then the dependent type theory is a model of classical propositional logic. One could add one of the following rules to make the propositional logic classical:

$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma \vdash \mathrm{lem}_A:A \vee \neg A} \qquad \frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma \vdash \mathrm{doubleneg}_A:\neg \neg A \implies A}$$

\section{Categorical semantics}

The [[categorical semantics]] of intuitionistic propositional logic is a [[(0,1)-category]] which is closed under [[finite products]], [[finite coproducts]], and [[internal homs]], or equivalently, a [[Heyting algebra]]. If the propositional logic is classical, then the categorical semantics is a [[Boolean algebra]]. 

\section{Typed predicate logic as a dependent type theory}

In the same way that [[propositional logic]] could be expressed as a dependent type theory, [[type theory|typed]] [[predicate logic]] could also be expressed as a type theory with two layers, a layer of 'types' which is the usual type theory, and a layer of propositional logic over the type layer. 

Thus, in addition to the theory above, we also have the judgments $A \; \mathrm{type}$ and $a \in A$, as well as similar rules for judgments and contexts

$$\frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a \in A) \; \mathrm{ctx}}$$

\subsection{Structural rules}

We also have the variable, weakening and substitution structural rules for types which are in the same format as the structural rules for propositions. 

$$\frac{\Gamma, a \in A, \Delta \; \mathrm{typectx}}{\Gamma, a \in A, \Delta \vdash a \in A}$$

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a \in A, \Delta \vdash \mathcal{J}}$$

$$\frac{\Gamma \vdash a \in A \quad \Gamma, b \in A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

\subsection{Predicates}

A **[[predicate]]** is defined in the usual manner, as a proposition in the [[term in context|context]] of a term of a type
$$\Gamma, x \in A \vdash P \; \mathrm{prop}$$
and the predicate $P$ is usually written as $P(x)$ to indicate its dependence upon the variable $x \in A$. 

A predicate proof is a proof of a proposition in the context of a term of a type
$$\Gamma, x \in A \vdash p:P$$
and the proof $p:P$ is similarly written as $p(x):P(x)$ to indicate its dependence upon the variable $x \in A$. 

\subsection{Universal quantification}

In this model of predicate logic, [[universal quantification]] is represented by a variant of the [[dependent product type]] where the dependent type hypothesis in the usual [[dependent product type]] in [[dependent type theory]] is replaced by a predicate hypothesis. 

Formation rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop}}{\Gamma \vdash \forall x \in A. B(x) \; \mathrm{prop}}$$

Introduction rules for the universal quantifier:
$$\frac{\Gamma, x \in A \vdash b(x):B(x)}{\Gamma \vdash \lambda x.b(x):\forall x \in A.B(x)}$$

Elimination rules for the universal quantifier:
$$\frac{\Gamma \vdash f:\forall x \in A. B(x) \quad \Gamma \vdash a \in A}{\Gamma \vdash f(a):B[a/x]}$$

Computation rules for the universal quantifier:
$$\frac{\Gamma, x \in A \vdash b(x):B(x) \quad \Gamma \vdash a \in A}{\Gamma \vdash \beta_\forall:\lambda x.b(x)(a) =_{B[a/x]} b[a/x]}$$

Uniqueness rules for the universal quantifier:
$$\frac{\Gamma \vdash f:\forall x \in A. B(x)}{\Gamma \vdash \eta_\forall:f =_{\forall x \in A. B(x)} \lambda(x).f(x)}$$

\subsection{Existential quantification}

Similarly, [[existential quantification]] is represented by a variant of the [[dependent sum type]] where the dependent type hypothesis in the usual [[dependent sum type]] in [[dependent type theory]] is replaced by a predicate hypothesis. In the same way that [[sum types]] are always propositionally truncated in propositional logic as a dependent type theory, existential quantification is similarly always propositionally truncated, due to the rules of propositional logic. 

Formation rules for the existential quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop}}{\Gamma \vdash \exists x \in A. B(x) \; \mathrm{prop}}$$

Introduction rules for the existential quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop}}{\Gamma, x \in A, y \in B(x) \vdash \mathrm{in}(x, y):\exists x \in A.B(x)}$$

Elimination rules for the existential quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop} \quad \Gamma, z:\exists x \in A.B(x) \vdash C(z) \; \mathrm{prop} \quad \Gamma, x \in A, y \in B(x) \vdash c:C(\mathrm{in}(x, y))}{\Gamma, z:\exists x \in A.B(x) \vdash \mathrm{ind}_{\exists x \in A.B(x)}^C(c)(z):C(z)}$$

Computation rules for the existential quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop} \quad \Gamma, z:\exists x \in A.B(x) \vdash C(x) \; \mathrm{prop} \quad \Gamma, x \in A, y \in B(x) \vdash c:C(\mathrm{in}(x, y))}{\Gamma, x \in A, y \in B(x) \vdash \beta_{\exists x \in A.B(x)}^C(c):\mathrm{ind}_{\exists x \in A.B(x)}^C(c)(\mathrm{in}(x, y)) =_{C(\mathrm{in}(x, y)/z)} c}$$

Uniqueness rules for the existential quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x \in A \vdash B(x) \; \mathrm{prop} \quad \Gamma, z:\exists x \in A.B(x) \vdash C(x) \; \mathrm{prop} \quad \Gamma, x \in A, y \in B \vdash c:C(\mathrm{in}(x, y)) \quad \Gamma, z:\exists x \in A.B(x) \vdash u:C \quad \Gamma, x \in A, y \in B(x) \vdash i_\mathrm{in}(u):u(\mathrm{in}(x, y)) =_{C(\mathrm{in}(x, y))} c}{\Gamma, z:\exists x \in A.B(x) \vdash \eta_{\exists x \in A.B(x)}^C(c):u(z) =_{C(z)} \mathrm{ind}_{\exists x \in A.B(x)}^C(c)(z)}$$

\subsection{Equality of types}

In modern presentations of this subject, typed predicate logic usually comes with a notion of [[equality]] on the types. Equality of types is a proposition, and is represented here by $\equiv$ to indicate it is an [[equivalence relation]]. It is defined by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a \in A, b \in A \vdash a \equiv_A b \; \mathrm{prop}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a \in A \vdash \mathrm{refl}_A(a):a \equiv_A a}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a \in A, b \in A \vdash \mathrm{sym}_A(a, b):(a \equiv_A b) \implies (b \equiv_A a)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a \in A, b \in A, c \in A \vdash \mathrm{trans}_A(a, b, c):(a \equiv_A b) \wedge (b \equiv_A c) \implies (a \equiv_A c)}$$

\section{Internalization in a type theory}

In all forms of [[dependent type theory]] with [[identity types]], [[dependent product types]], [[dependent sum types]], [[empty types]], [[unit types]], [[sum types]], and [[propositional truncations]], [[propositional logic]] and [[predicate logic]] could be internalized in the type theory itself through the definition of a [[univalent]] [[type of propositions]] in the type theory. 

\section{See also}

* [[dependent type theory]]
* [[propositional logic]]
* [[propositions as types]]
* [[h-proposition]]
* [[type of propositions]]
* [[two-level type theory]]
* [[type theory with shapes]]
* [[logic over dependent type theory]]
* [[higher order logic as a dependent type theory]]

\section{Bibliography}

* [[Per Martin-Löf]], _Intuitionistic Type Theory_, Notes by Giovanni Sambin of a series of lectures given in Padua, June 1980. Bibliopolis, Napoli, 1984.

* [[UF-IAS-2012|Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (**[web](http://homotopytypetheory.org/book/)**, **[pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)**, **[[Planet Math|PM]] [wiki version](http://planetmath.org/node/87534)**)

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

[[!redirects predicate logic as a dependent type theory]]