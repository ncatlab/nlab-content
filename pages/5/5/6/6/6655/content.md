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

#Martin-L&#246;f dependent type theory#
* table of contents
{:toc}

##Idea
[[Per Martin-Lof|Per Martin-Löf]]'s **dependent type theory**, also known as **intuitionistic type theory**, is a specific form of [[type theory]] developed to support [[constructive mathematics]]. It is notable for several reasons: 

* It embeds first-order [[intuitionistic logic]] by interpreting [[propositions as types]].
* It has a version of the [[axiom of choice]] _as a theorem_.
* In its [[intensional]] form, it has sufficient computational content to even be a programming language.

##Syntax
If $t$ is a term, and $A$ a type, then $t : A$ is a **typing declaration** asserting that $t$ is a term of type $A$. We will define the forms of valid terms and types below; to begin with, we assume we have a stock of atomic terms (variables), atomic types, and parametrised types. 

A **context** is a finite ordered list of typing declarations, defined recursively as follows:

* The empty list is a valid context.
* If $\Gamma$ is a valid context, $x$ is a variable, and $A$ is a valid type in the context $\Gamma$, then the context obtained by appending $x : A$ to $\Gamma$ is also valid.

We write $\Gamma \vdash t : A$ to assert that $t : A$ is a valid typing declaration in the context of $\Gamma$, and by abuse of notation we may write $\Gamma \vdash A : \mathrm{Type}$ to assert that $A$ is a valid type in the context of $\Gamma$.

For any context $\Gamma$, if $A$ is an atomic type, $\Gamma \vdash A : \mathrm{Type}$. 

If $x : A$ is a typing declaration in $\Gamma$, then we have $\Gamma \vdash x : A$.

###Finite product types
If $\Gamma \vdash A : \mathrm{Type}$ and $\Delta \vdash B : \mathrm{Type}$, then $\Gamma, \Delta \vdash A \times B : \mathrm{Type}$. 

If $\Gamma \vdash a : A$ and $\Delta \vdash b : B$ then $\Gamma, \Delta \vdash \langle a, b \rangle : A \times B$.

If $\Gamma \vdash c : A \times B$, then $\Gamma \vdash \pi_0(c) : A$ and $\Gamma \vdash \pi_1(c) : B$.

###Dependent product types
If $\Gamma, x : X \vdash A(x) : \mathrm{Type}$, then $\Gamma \vdash (\Pi x : X) A(x) : \mathrm{Type}$.

If $\Gamma, x : X \vdash a(x) : A(x)$, then $\Gamma \vdash (\lambda x : X) a(x) : (\Pi x : X) A(x)$.

If $\Gamma \vdash f : (\Pi x : X) A(x)$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}(f, t) : A(t)$.

###Function types
Function types may be regarded as a special case of dependent product types, where $A(x)$ does not depend on $x$ at all. Formally, if $\Gamma \vdash X : \mathrm{Type}$ and $\Gamma \vdash A : \mathrm{Type}$, then $\Gamma \vdash X \to A : \mathrm{Type}$.

If $\Gamma, x : X \vdash a(x) : A$, then $\Gamma \vdash (\lambda x : X) a(x) : X \to A$.

If $\Gamma \vdash f : X \to A$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}(f, t) : A$.

###Finite sum types
If $\Gamma \vdash A : \mathrm{Type}$ and $\Gamma \vdash B : \mathrm{Type}$, then $\Gamma \vdash A + B : \mathrm{Type}$. 

If $\Gamma \vdash a : A$ and $\Gamma \vdash A + B : \mathrm{Type}$, then $\Gamma \vdash a : A + B$; and if $\Gamma \vdash b : B$ and $\Gamma \vdash A + B : \mathrm{Type}$, then $\Gamma \vdash b : A + B$.

If $\Gamma \vdash s : A + B$, $\Delta, x : A \vdash c(x) : C(x)$ and $E, y : B \vdash c'(y) : C(y)$, then $\Gamma, \Delta, E \vdash \mathrm{cases}(s, (\lambda x : A) c(x), (\lambda y : B) c'(y)) : C(s)$.

###Dependent sum types
If $\Gamma, x : X \vdash A(x) : \mathrm{Type}$, then $\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{Type}$.

If $\Gamma \vdash t : X$, $\Gamma \vdash a : A(t)$ and $\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{Type}$, then $\Gamma \vdash (t, a) : (\Sigma x : X) A(x)$.

If $\Gamma \vdash s : (\Sigma x : X) A(x)$ and $\Delta, x : X, y : A(x) \vdash b(x, y) : B((x, y))$, then $\Gamma, \Delta \vdash \mathrm{cases}(s, (\lambda x : X)(\lambda y : A(x)) b(x, y)) : B(s)$.

##Propositions as types

Under the [[Curry-Howard isomorphism|Curry–Howard isomorphism]], we may identify propositions with atomic types and predicates with parametrised types; an inhabitant of such a proposition-as-a-type is interpreted as a 'proof' of that proposition.

We write $\Gamma \vdash A : \mathrm{true}$ for the judgement that $A$ is inhabited: that is, if $\Gamma \vdash a : A$, then $\Gamma \vdash A : \mathrm{true}$. The type-formation rules above are then seen to be the rules of inference for (a fragment of) intuitionistic first-order logic. Indeed, we have:

* Conjunction introduction:
$$\frac{\Gamma \vdash A : \mathrm{true} ; \Delta \vdash B : \mathrm{true}}{\Gamma, \Delta \vdash A \times B : \mathrm{true}}$$
* Conjunction elimination:
$$\begin{aligned}
\frac{\Gamma \vdash A \times B : \mathrm{true}}{\Gamma \vdash A : \mathrm{true}} &
\frac{\Gamma \vdash A \times B : \mathrm{true}}{\Gamma \vdash B : \mathrm{true}} 
\end{aligned}$$
* Universal generalisation:
$$\frac{\Gamma, x : X \vdash A(x) : \mathrm{true}}{\Gamma \vdash (\Pi x : X) A(x) : \mathrm{true}}$$
* Universal instantiation:
$$\frac{\Gamma \vdash (\Pi x : X) A(x) : \mathrm{true} ; \Delta \vdash t : X}{\Gamma, \Delta \vdash A(t) : \mathrm{true}}$$
* Conditional proof:
$$\frac{\Gamma, X : \mathrm{true} \vdash A : \mathrm{true}}{\Gamma \vdash X \to A : \mathrm{true}}$$
* Modus ponens:
$$\frac{\Gamma \vdash X \to A : \mathrm{true} ; \Delta \vdash X : \mathrm{true}}{\Gamma, \Delta \vdash A : \mathrm{true}}$$
* Disjunction introduction:
$$\begin{aligned}
\frac{\Gamma \vdash A : \mathrm{true}}{\Gamma \vdash A + B : \mathrm{true}} &
\frac{\Gamma \vdash B : \mathrm{true}}{\Gamma \vdash A + B : \mathrm{true}}
\end{aligned}$$
* Disjunction elimination:
$$\frac{\Gamma \vdash A + B : \mathrm{true} ; \Delta, A : \mathrm{true} \vdash C : \mathrm{true} ; E, B : \mathrm{true} \vdash C : \mathrm{true}}{\Gamma, \Delta, E \vdash C : \mathrm{true}}$$
* Existential generalisation:
$$\frac{\Gamma \vdash t : X ; \Gamma \vdash A(t) : \mathrm{true}}{\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{true}}$$
* Existential instantiation:
$$\frac{\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{true} ; \Delta, x : X, A(x) : \mathrm{true} \vdash B : \mathrm{true}}{\Gamma, \Delta \vdash B : \mathrm{true}}$$

The only rule of inference we are missing is the rule of _ex falso quodlibet_.

The above justifies the use of the symbols $\forall$, $\exists$, $\wedge$, $\vee$ instead of $\Pi$, $\Sigma$, $\times$, $+$ for propositions-as-types.

##Equality types

We introduce a family of equality types for each type and each pair of terms of that type: if $\Gamma \vdash a : A$ and $\Delta \vdash a' : A$, then $\Gamma \vdash a = a' : \mathrm{Type}$.

The equality type is reflexive, symmetric, and transitive. That means, for example, if $\Gamma \vdash a : A$, $\Gamma \vdash b : A$, $\Gamma \vdash c : A$, $\Gamma \vdash a = b : \mathrm{true}$ and $\Gamma \vdash b = c : \mathrm{true}$ then $\Gamma \vdash a = c : \mathrm{true}$.

###Finite product types
If $\Gamma \vdash a : A$, and $\Gamma \vdash b : B$, then $\Gamma \vdash a = \pi_0 (\langle a, b \rangle) : \mathrm{true}$ and $\Gamma \vdash \pi_1 (\langle a, b \rangle) = b : \mathrm{true}$.

If $\Gamma \vdash c : A \times B$, then $c = \langle \pi_0 (c), \pi_1 (c) \rangle : \mathrm{true}$.

###Dependent product types
If $\Gamma, x : X \vdash a(x) : A(x)$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}((\lambda x : X) a(x), t) = a(t) : \mathrm{true}$.

If $\Gamma \vdash f : (\Pi x : X) A(x)$, then $\Gamma \vdash f = (\lambda x : X) \mathrm{apply}(f, x) : \mathrm{true}$.

###Function types
If $\Gamma, x : X \vdash a(x) : A$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}((\lambda x : X) a(x), t) = a(t) : \mathrm{true}$.

If $\Gamma \vdash f : X \to A$, then $\Gamma \vdash f = (\lambda x : X) \mathrm{apply}(f, x) : \mathrm{true}$.

###Finite sum types
If $\Gamma \vdash a : A$ and $\Gamma \vdash A + B : \mathrm{Type}$, $\Delta, x : A \vdash c(x) : C(x)$ and $\Epsilon, y : B \vdash c'(y) : C(y)$, then $\Gamma, \Delta, E \vdash \mathrm{cases}(a, (\lambda x : A) c(x), (\lambda y : B) c(y)) = c(a) : \mathrm{true}$ and $\Gamma, \Delta, E \vdash \mathrm{cases}(b, (\lambda x : A) c(x), (\lambda y : B) c'(y)) = c'(b) : \mathrm{true}$

###Dependent sum types
If $\Gamma \vdash t : X$, $\Gamma \vdash a : A(t)$ and $\Delta, x : X, y : A(x) \vdash b(x, a) : B((x, a))$, then $\Gamma, \Delta \vdash \mathrm{cases}((t, a), (\lambda x : X)(\lambda y : A(x)) b(x, y)) = b(t, a) : \mathrm{true}$.

The other equality rule for dependent sum types is derivable from the above.

##Axiom of choice

The following form of the [[axiom of choice]] is _derivable_ in Martin-L&#246;f dependent type theory: If $\Gamma, x : A, y : B(x) \vdash C(x, y) : \mathrm{Type}$,

$$\Gamma \vdash (\forall x : A) (\exists y : B(x)) C(x, y) \to (\exists f : (\Pi x : A)B(x) )(\forall x : A) C(x, \mathrm{apply}(f, x)) : \mathrm{true}$$

One should note carefully that this is only "the axiom of choice" under the above propositions-as-types interpretation of the quantifiers $\forall$ and $\exists$.  Category-theoretically, using the propositions-as-types logic corresponds roughly to working with the subobject lattices in the [[ex/lex completion]] of a [[locally cartesian closed category]]; the axiom of choice then follows since every object of the original category becomes [[projective object|projective]] in its ex/lex completion.

If we use instead a different logic over the same type theory, such as [[bracket type]]s to model the actual subobject lattices in an arbitrary lccc (not necessarily the ex/lex completion of anything), or the hProp logic in [[homotopy type theory]], then the axiom of choice in that logic will not be derivable.

##References

* Martin-L&#246;f, Per (1984), _Intuitionistic type theory_.
