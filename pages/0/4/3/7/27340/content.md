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

Higher-order logic is a [[logic]] which contains the notion of [[higher-order predicates]], which are functions between [[predicates]]. Traditionally, higher-order logic, such as [[HOL4]] or [[Isabelle]], is presented as a [[simple type theory]]. In addition, intuitionistic higher-order logic is said to be the [[internal logic]] of an [[elementary topos]], and classical higher-order logic is said to be the internal logic of a [[Boolean topos]]. However, an elementary topos or Boolean topos is a [[locally cartesian closed category]], whose internal logic is a [[dependent type theory]]. This implies that higher-order logic can be presented as a [[dependent type theory]]. 

Dependent type theory already has the ability to form higher-order functions via iterated [[function types]]. The only thing that is missing in dependent type theory is the ability to construct predicates, which are functions into a set of truth values. This is represented by an [[impredicative mathematics|impredicative]] [[type of all propositions]] $\mathrm{Prop}$ in dependent type theory. The idea behind the [[type of all propositions]] in dependent type theory is the principle of [[propositions as codes for subsingletons]], and so for each proposition $P:\mathrm{Prop}$, it is possible to construct a type $\mathrm{El}(P)$ and a witness that $\mathrm{El}(P)$ is a [[subsingleton]] or [[h-propositions]]. 

Adding a [[type of all propositions]] to dependent type theory is sufficient to construct all the usual first-order logical operations and values that are also required for higher-order logic, such as [[truth]], [[falsehood]], [[disjunction]], [[conjunction]], [[implication]], [[negation]], [[exclusive disjunction]], the [[existential quantifier]], the [[uniqueness quantifier]], and the [[universal quantifier]]. This is in contrast to higher-order logic presented as a [[simple type theory]], where each of the logical operations have to be added to the theory using [[axioms]]. 

There are usually two ways to present a [[dependent type theory]]: one which uses a [[hierarchy of universes]] and either no type judgments or an infinite number of type judgments to define types, and a second which uses no universes and a single type judgment to define types. Higher-order logic such as [[HOL]] or [[Isabelle]] has no infinite hierarchy of universes, so the only way to present higher-order logic as a dependent type theory is using a single type judgment. 

\section{Presentation}

\subsection{Judgments and contexts}
 {#JudgmentsAndContexts}

The [[syntax]] of higher-order logic as dependent type theory can be constructed in two stages: 

* The first is the *raw* or *untyped* syntax of the theory consisting of expressions that are readable but not necessarily meaningful. 

* The second stage consists of defining the *derivable judgements* of the type theory [[induction|inductively]] which then pick out the meaningful [[contexts]], [[types]] and [[terms]].

A [[context]] is a [[list]] of succesively [[dependent types]]. The [[variables]] may be defined as [[de Bruijn indices]], in which case the type of a variable $n$ is given by $n$th type in a [[context]].

One may also define contexts as coming with a variable name, in which case one needs a notion of $\alpha$-equivalence (syntactic identity modulo renaming of bound variables) and of capture-free substitution. De Bruijn indices avoid this step but can be more obfuscating.

Types and terms are built inductively from various constructors. Types, terms and contexts are defined mutually.

We have the basic [[judgement]] forms:

* $\Gamma \; \mathrm{ctx}$ 

  saying that: "$\Gamma$ is a well-formed context";

* $\Gamma \vdash A\; \mathrm{type}$ 

  saying that "$A$ is a well-typed [[dependent type]] in [[context]] $\Gamma$";

* $\Gamma \vdash a : A$ 

  saying that "$a$ is a well-typed [[term]] of [[type]] $A$ in [[context]] $\Gamma$";

We work in the [[logical framework]] of [[natural deduction]], where everything is given by [[inference rules]]. 

To start with, [[contexts]] are built from [[dependent types]] by the following rules (cf. [[type telescope]]):

$$
  \frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}}
$$

\subsection{Structural rules}
 {#StructuralRules}

Among the *[[structural rules]]* of dependent type theory are (e.g. [Jacobs (1998), p. 122](#Jacobs98), [Rijke (2022), Sec. 1.4](#Rijke22)):

* the [[variable rule]], 

* the [[weakening rule]], 

* the [[substitution rule]]

The weakening and substitution rules are [[admissible rules]]: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

\subsection{Judgmental equality}

In addition, there are judgments for judgmental equality of types and of terms:

* $\Gamma \vdash A \equiv A' \; \mathrm{type}$ - $A$ and $A'$ are judgementally equal well-typed types in context $\Gamma$.
* $\Gamma \vdash a \equiv a' : A$ - $a$ and $a'$ are judgementally equal well-typed terms of type $A$ in context $\Gamma$.

Judgmental equality has its own structural rules: reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of judgmental equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A \equiv A \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv a:A}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b \equiv a:A}$$

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash B \equiv C \; \mathrm{type} }{\Gamma \vdash A \equiv C \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A \quad b \equiv c:A }{\Gamma \vdash a \equiv c:A}$$

* Principle of substitution of judgmentally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta(x) \vdash B(x) \; \mathrm{type}}{\Gamma, \Delta(b) \vdash B(a) \equiv B(b) \; \mathrm{type}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c(x):B(x)}{\Gamma, \Delta(b) \vdash c(a) \equiv c(b): B(b)}$$

* Variable conversion rule:
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

\subsection{Definitions}

In addition, there are judgments for the initialization operator for types and for terms:

* $\Gamma \vdash A' \coloneqq A \; \mathrm{type}$ - $A'$ is defined to be the type $A$ in context $\Gamma$.
* $\Gamma \vdash a' \coloneqq a : A$ - $a'$ is defined to be the term $a:A$ of type $A$ in context $\Gamma$.

The initialization operator has its own structural rules: type formation, term introduction, and equality reflection.

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

\subsection{Rules for types}

Each type in Martin-Löf dependent type theory comes with a type [[formation rule]], a term [[introduction rule]], a term [[elimination rule]], a [[computation rule]], and an optional [[uniqueness rule]]. The elimination rules we give here are not [[contextual elimination rules]], and the conversion rules given here are not [[contextual conversion rules]]. In addition, there are judgmental [[congruence rules]] which says that each of the natural deduction rules preserve [[judgmental equality]], but for the sake of brevity the congruence rules are not included here. 

\subsubsection{Dependent product types}

* Formation rules for dependent product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \prod_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

* Elimination rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B(a)}$$

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv b(a):B(a)}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

\subsubsection{Dependent sum types}

* Formation rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

* Introduction rules for dependent sum types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B(a)}{\Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_2(z):B(\pi_1(z))}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B(a)}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B(a)}{\Gamma \vdash \pi_2(a, b) \equiv b:B(\pi_1(a, b))}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

\subsubsection{Identity types}

There is another version of equality, called the [[identity type]] or **typal equality**, because this equality is a type. The identity type is only be used for equality between terms of a type, and unless one is using [[Russell universes]] where types are represented by terms of a [[Russell universe]], identity types cannot be used for equality of types. 

* Formation rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{type}}$$

* Introduction rule for identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{type} \quad \Gamma \vdash t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))}{\Gamma, a:A, b:A, p:a =_A b \vdash J(t, a, b, p):C(a, b, p)}$$

* Computation rules for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{type} \quad \Gamma \vdash t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))}{\Gamma, x:A \vdash J(t, x, x, \mathrm{refl}(x)) \equiv t(x):C(x, x, \mathrm{refl}_A(x))}$$

\subsubsection{Type of all propositions}

In [[dependent type theory]], a type $A$ is a [[subsingleton]] or [[h-proposition]] if for all $x:A$ and $y:A$ there is $p(x, y):x =_A y$. This is usually represented as a term $p$ of a dependent function type

$$\mathrm{ishProp}(A) \coloneqq \prod_{x:A} \prod_{y:A} x =_A y$$

The type of all propositions is given by the following [[natural deduction]] [[inference rules]]:

* Formation rules for the type of all propositions:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Prop} \; \mathrm{type}}$$

* Introduction rules for the type of all propositions:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toProp}_A:\mathrm{ishProp}(A) \to \mathrm{Prop}}$$

* Elimination rules for the type of all propositions:
$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash \mathrm{proptrunc}(A):\mathrm{ishProp}(\mathrm{El}(A))}$$

* Computation rules for the type of all propositions:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{ishProp}(A)}{\Gamma \vdash \mathrm{El}(\mathrm{toProp}_A(p)) \equiv A \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{ishProp}(A)}{\Gamma \vdash \mathrm{proptrunc}(\mathrm{toProp}_A(p)) \equiv p:\mathrm{isProp}(A)}$$

* Uniqueness rules for the type of all propositions:

$$\frac{\Gamma \vdash A:\mathrm{Prop}}{\Gamma \vdash A \equiv \mathrm{toProp}_{\mathrm{El}(A)}(\mathrm{proptrunc}(A)):\mathrm{Prop}}$$

\subsubsection{Weak function extensionality and propositional extensionality}

* Extensionality principle of the type of all propositions:

$$\frac{\Gamma \vdash A:\mathrm{Prop} \quad \Gamma \vdash B:\mathrm{Prop}} {\Gamma \vdash \mathrm{ext}_\mathrm{Prop}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

* Weak function extensionality:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B:A \to \mathrm{Prop}}{\Gamma \vdash \mathrm{wfunext}_A(B):\mathrm{ishProp}\left(\prod_{x:A} \mathrm{El}(B(x))\right)}$$

\subsection{Constructing the logical operators}

TBD: Show how to construct [[truth]], [[falsehood]], [[disjunction]], [[conjunction]], [[implication]], [[negation]], [[exclusive disjunction]], the [[existential quantifier]], the [[uniqueness quantifier]], and the [[universal quantifier]] from [[dependent product types]], [[dependent sum types]], [[identity types]], and the [[type of all propositions]]. 

\subsubsection{Universal quantification}

Given any type $A$ and predicate $P:A \to \mathrm{Prop}$ by [[weak function extensionality]], the [[dependent function type]] $\prod_{x:A} \mathrm{El}(P(x))$ is an [[h-proposition]]: 

$$\mathrm{wfunext}_A(P):\mathrm{ishProp}\left(\prod_{x:A} \mathrm{El}(P(x))\right)$$

This means that the [[universal quantifier]] can be defined via the introduction rules of the type of all propositions as 

$$\forall x:A.P(x) \coloneqq \mathrm{toProp}_{\prod_{x:A} \mathrm{El}(P(x))}(\mathrm{wfunext}_A(P))$$

\subsubsection{Falsehood}

By [[weak function extensionality]], the dependent product type $\prod_{P:\mathrm{Prop}} \mathrm{El}(P)$ is a [[h-proposition]] with witness 

$$\mathrm{wfunext}(\mathrm{Prop}, \mathrm{id}_\mathrm{Prop}):\mathrm{ishProp}\left(\prod_{P:\mathrm{Prop}} \mathrm{El}(P)\right)$$

This dependent product type is the [[empty type]], since the definition implies that if the type has an element, then every proposition has an element and is thus a [[contractible type]]. Since the empty type is the subsingleton / h-proposition representation of [[falsehood]], this means that falsehood $\bot:\mathrm{Prop}$ can be defined via the introduction rules of the type of all propositions as 

$$\bot \coloneqq \mathrm{toProp}_{\prod_{P:\mathrm{Prop}} \mathrm{El}(P)}(\mathrm{wfunext}_\mathrm{Prop}(\mathrm{id}_\mathrm{Prop}))$$

\subsubsection{Implication and negation}

Given any proposition $Q:\mathrm{Prop}$ and $P:\mathrm{Prop}$, one can define the constant predicate $\lambda x:\mathrm{El}(Q).P:\mathrm{El}(Q) \to \mathrm{Prop}$. By definition of [[function type]] in [[dependent type theory]], the function type $\mathrm{El}(Q) \to \mathrm{El}(P)$ is defined as the [[dependent function type]] 

$$\mathrm{El}(Q) \to \mathrm{El}(P) \coloneqq \prod_{x:\mathrm{El}(Q)} \mathrm{El}(P) \equiv \prod_{x:\mathrm{El}(Q)} \mathrm{El}((\lambda x:\mathrm{El}(Q).P)(x))$$

which is an [[h-proposition]] by [[weak function extensionality]]: 

$$\mathrm{wfunext}_{\mathrm{El}(Q)}(\lambda x:\mathrm{El}(Q).P):\mathrm{ishProp}\left(\prod_{x:\mathrm{El}(Q)} \mathrm{El}((\lambda x:\mathrm{El}(Q).P)(x))\right)$$

This means that implication $Q \Rightarrow P$ can be defined as the following proposition:

$$Q \Rightarrow P \coloneqq \mathrm{toProp}_{\prod_{x:\mathrm{El}(Q)} \mathrm{El}((\lambda x:\mathrm{El}(Q).P)(x))}(\mathrm{wfunext}_{\mathrm{El}(Q)}(\lambda x:\mathrm{El}(Q).P))$$

The negation $\neg P$ of a proposition $P:\mathrm{Prop}$ is given by implication into falsehood:

$$\neg P \coloneqq P \Rightarrow \bot$$

\subsubsection{Truth}

There are many different ways of defining truth $\top:\mathrm{Prop}$. One definition is defining truth as false implying false, i.e. the negation of false:

$$\top \coloneqq \bot \Rightarrow \bot$$

\subsubsection{Existential quantifier}

In [[dependent type theory]] which uses the [[propositions as subsingletons]] interpretation, given a type $A$ and a family of [[h-propositions]] $(P(x))_{x:A}$, the existential quantifier is defined as the [[propositional truncation]] of the [[dependent sum type]] $\sum_{x:A} P(x)$. Given a [[type of all propositions]], the propositional truncation $[A]$ of a type $A$ is defined as the dependent product type

$$\prod_{Q:\mathrm{Prop}} (A \to \mathrm{El}(Q)) \to \mathrm{El}(Q)$$

Assuming that we have a predicate $P:A \to \mathrm{Prop}$, substituting the dependent sum type $\sum_{x:A} \mathrm{El}(P(x))$ in for $A$, we get the following type

$$\prod_{Q:\mathrm{Prop}} \left(\left(\sum_{x:A} \mathrm{El}(P(x))\right) \to \mathrm{El}(Q)\right) \to \mathrm{El}(Q)$$

which by [[currying]] is equivalent to the type

$$\prod_{Q:\mathrm{Prop}} \left(\prod_{x:A} (\mathrm{El}(P(x)) \to \mathrm{El}(Q))\right) \to \mathrm{El}(Q)$$

This type is an h-proposition by repeated applications of weak function extensionality: 

...

\subsection{Excluded middle}

The above rules are sufficient for [[intuitionistic logic|intuitionistic]] [[higher-order logic]]. However, higher-order logics like [[HOL]] and [[Isabelle]] are classical logics, and so require an additional axiom: the [[law of excluded middle]], which says that the propositin $P$ is either true or false:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \prod_{P:\mathrm{Prop}} \mathrm{El}(P) \vee \neg \mathrm{El}(P)}$$

\section{Related concepts}

* [[dependent type theory]]

* [[higher-order logic]]

* [[h-proposition]]

* [[predicate]], [[subtype]]

* [[type of propositions]]

* [[impredicative dependent type theory]]

* [[propositional logic as a dependent type theory]]

\section{References}

* {#Jacobs98} [[Bart Jacobs]], Chapter 10 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#HOLSystem} Michael Norrish and Konrad Slind, *The HOL System LOGIC* ([pdf](https://master.dl.sourceforge.net/project/hol/hol/trindemossen-1/trindemossen-1-logic.pdf?viasf=1))

[[!redirects higher-order logic as a dependent type theory]]
[[!redirects higher order logic as a dependent type theory]]

[[!redirects higher-order logics as dependent type theories]]
[[!redirects higher order logics as dependent type theories]]