\tableofcontents

\section{Idea}

In [[type theory]], there is a principle known as [[propositions as types]], which says that [[propositions]] and [[types]] are essentially the same: a proposition is identified with the type of all its [[proofs]], and a type is identified with the proposition that it has a term. 

However, this principle fails in many models of [[dependent type theory]], including the most widely used frameworks of type theories, such as [[Martin-Löf type theory]] and [[cubical type theory]], and the [[homotopy type theories]] based upon the two frameworks. Instead, they follow the weaker "propositions as some types" principle: while every proposition is interpreted as a type, not every type is interpreted as a proposition: only the [[(-1)-truncated]] types are interpreted as propositions (see [[h-proposition]] for more details). 

In this article, we create a model of dependent type theory where the full [[propositions as types]] principle holds: every type is an [[h-proposition]]. In particular, proofs have equality propositions, represented by the [[identity types]], and every proposition is [[propositional truncation|propositionally truncated]], represented in this article by two rules equivalent to two definitions of [[isProp]] in [[dependent type theory]]. In addition, we add rules for the [[empty type]] corresponding to [[false]], the [[unit type]] corresponding to [[true]], [[sum types]] corresponding to [[disjunction]], [[product types]] corresponding to [[conjunction]], [[function types]] corresponding to [[implication]], as well as [[negations]] to the dependent type theory, yielding a model of [[intuitionistic logic]]. Finally, adding [[excluded middle]] or the [[double negation law]] yields a model of [[classical logic]]. 

\section{Presentation}

The type theory we shall be presenting here is the [[objective type theory]] version of [[dependent type theory]], because the lack of [[definitional equality]] means that the theory is both simpler, and behaves more like traditional [[propositional logic]], which usually doesn't have definitional equality. 

\subsection{Judgments and contexts}

The objective type theory model of propositional logic  consists of three judgments: proposition judgments $A \; \mathrm{prop}$, where we judge $A$ to be a proposition, proof judgments, where we judge $a$ to be a proof of $A$, $a:A$, and context judgments, where we judge $\Gamma$ to be a context, $\Gamma \; \mathrm{ctx}$. Contexts are lists of proof judgments $a:A$, $b:B$, $c:C$, et cetera, and are formalized by the rules for the empty context and extending the context by a proof judgment

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{prop}}{(\Gamma, a:A) \; \mathrm{ctx}}$$

\subsection{Structural rules}

The structural rules of this theory include the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a proof judgment if the proof judgment is in the context already:

$$\frac{\vdash \Gamma, a:A, \Delta \; \mathrm{ctx}}{\vdash \Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

\subsection{Predicates and dependent proof}

A [[predicate]] is a proposition $B$ in the context of the variable judgment $x:A$, $x:A \vdash B \; \mathrm{prop}$, they are usually written as $B(x)$ to indicate its dependence upon $x$. 

A dependent proof is a proof $b:B$ in the context of the variable judgment $x:A$, $x:A \vdash b:B$. dependent proofs are likewise usually written as $b(x)$ to indicate its dependence upon $x$. 

\subsection{Equality}

Equality of proofs of a proposition is represented by a proposition known as the **equality predicate**. The elements of the equality predicate are called **equalities**. 

Equality comes with a formation rule, an introduction rule, an elimination rule, and a computation rule:

Formation rule for the equality predicate:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, b:A \vdash a =_A b \; \mathrm{prop}}$$

Introduction rule for the equality predicate:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A \vdash \mathrm{refl}_A(a) : a =_A a}$$

Elimination rule for the equality predicate:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{prop} \quad \Gamma, a:A \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b \vdash J(t, a, b, p):C(a, b, p)}$$

Computation rules for the equality predicate:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{prop} \quad \Gamma, a:A \vdash t:C(a, a, \mathrm{refl}_A(a))}{\Gamma, a:A, b:A, p:a =_A b \vdash \beta_{=_A}(a) : J(t, a, a, \mathrm{refl}(a)) =_{C(a, a, \mathrm{refl}_A(a))} t}$$

\subsection{Propositional truncation}

One also adds the propositional truncation rule for propositions:
$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma, a:A, b:A \vdash \mathrm{proptrunc}_A:a =_A b}$$

One could equivalently adds the point contraction rule for propositions with a proof:
$$\frac{\Gamma \vdash A \; \mathrm{prop} \quad \Gamma \vdash a:A}{\Gamma, b:A \vdash \mathrm{contr}_A:a =_A b}$$
which states that the given proof is a [[center of contraction]]. 

Both rules ensure that every proposition behaves like an h-proposition in dependent type theory. 

\subsection{False}

Formation rules for false:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \bot \; \mathrm{prop}}$$

Elimination rules for false:
$$\frac{\Gamma, x:\bot \vdash C \; \mathrm{prop} \quad \Gamma \vdash p:\bot}{\Gamma \vdash \mathrm{ind}_\bot^C(p):C(p)}$$

Uniqueness rules for false:
$$\frac{\Gamma, x:\bot \vdash C \; \mathrm{prop} \quad \Gamma \vdash p:\bot \quad \Gamma, x:\bot \vdash u:C}{\Gamma \vdash \eta_\bot(p, u):u[p/x] =_{C[p/x]} \mathrm{ind}_\bot^{C}(p)}$$

\subsection{True}

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

Formation rules for disjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \vee B \; \mathrm{type}}$$

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

Formation rules for conjunctions:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \wedge B \; \mathrm{type}}$$

Introduction rules for conjunctions:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash (a, b):A \wedge B}$$

Elimination rules for conjunctions:
$$\frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \pi_2(z):B}$$

Computation rules for conjunctions:
$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\wedge 1}:\pi_1(a, b) =_A a} \qquad \frac{\Gamma \vdash a:A \quad \Gamma \vdash b:B}{\Gamma \vdash \beta_{\wedge 2}:\pi_2(a, b) =_B b}$$

Uniqueness rules for conjunctions:
$$\frac{\Gamma \vdash z:A \wedge B}{\Gamma \vdash \eta_\wedge:z =_{A \wedge B} (\pi_1(z), \pi_2(z))}$$

\subsection{Implications}

Formation rules for implications:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \implies B \; \mathrm{type}}$$

Introduction rules for implications:
$$\frac{\Gamma, x:A \vdash b(x):B}{\Gamma \vdash (x \mapsto b(x)):A \implies B}$$

Elimination rules for implications:
$$\frac{\Gamma \vdash f:A \implies B \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B}$$

Computation rules for implications:
$$\frac{\Gamma, x:A \vdash b(x):B \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\implies}:(x \mapsto b(x))(a) =_{B} b}$$

Uniqueness rules for implications:
$$\frac{\Gamma \vdash f:A \implies B}{\Gamma \vdash \eta_{\implies}:f =_{A \implies B} (x \to f(x))}$$

\subsection{Negations}

A negation is just an implication to false. However, we introduce separate rules for negations specifically for the use of the notation $\neg A$ rather than the longer $A \implies \bot$. 

Formation rules for negations:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \neg A  \; \mathrm{type}}$$

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

A proposition $A$ is said to be **decidable** or satisfy **[[excluded middle]]** if there is a proof $p:A \vee \neg A$. $A$ is said to be **stable** or satisfy the **[[double negation law]]** if there is a proof $p:\neg \neg A \implies A$. Every decidable propositions is stable, and every stable proposition is decidable, which means that the two notions are the same. 

If every proposition is decidable or stable, then the dependent type theory is a model of classical or Boolean propositional logic. One could add one of the following rules to make the propositional logic classical:

$$\frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma \vdash p:A \vee \neg A} \qquad \frac{\Gamma \vdash A \; \mathrm{prop}}{\Gamma \vdash p:\neg \neg A \implies A}$$

\section{See also}

* [[dependent type theory]]
* [[propositional logic]]
* [[propositions as types]]
* [[h-proposition]]