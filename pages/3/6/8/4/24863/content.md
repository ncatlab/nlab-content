
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

**Typed predicate logic** or **logic over type theory** can be represented in the language of [[natural deduction]] as a two-[[layered type theory]] consisting of a layer of [[propositions]] represented by the judgment $P \; \mathrm{prop}$, over a layer of [[types]] represented by the judgment $A \; \mathrm{type}$. A [[predicate]] $P$ on a type $A$ in typed predicate logic is simply a [[proposition]] $P$ in the context of a variable of $A$, $x:A \vdash P \; \mathrm{prop}$. 

One could add additional logical operations to the proposition layer, such as rules for [[false]], [[true]], [[conjunction]], [[disjunction]], [[implication]], [[universal quantifier]], and [[existential quantifier]], as well as additional rules to the type layer, such as rules for [[propositional equality]]. 

The type layer could either be a [[simple type theory]] or [[dependent type theory]], examples of the former include [[ZFC]] and [[fully formal ETCS]], while the latter includes the [[SEAR]], as well as presentations of [[dependent type theory]] which use [[propositional equality]] instead of [[judgmental equality]] for [[definitional equality]] and [[conversional equality]].

Typed predicate logic is used in many type theories, including [[simplicial type theory]] and [[cubical type theory]], where the main [[dependent type theory]] is built over a typed predicate logic. 

## Presentation

### Judgments and contexts

Typed predicate logic is a type theory which consists of two layers, a layer for types and a layer for propositions over the layer for types. 

We have the basic judgement forms of the type layer:

* $\Gamma \vdash A\; \mathrm{type}$ - $A$ is a well-typed type in context $\Gamma$.
* $\Gamma \vdash a : A$ - $a$ is a well-typed term of type $A$ in context $\Gamma$.

And the basic judgement forms of the proposition layer:

* $\Gamma \vdash \phi \; \mathrm{prop}$ - $\phi$ is a well-formed proposition in context $\Gamma$
* $\Gamma \vdash \phi \; \mathrm{true}$ - $\phi$ is a well-formed true proposition in context $\Gamma$

As well as context judgments:

* $\Gamma \; \mathrm{ctx}$ - $\Gamma$ is a well-formed context. 

Contexts are defined by the following rules:

$$\frac{}{() \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash A \; \mathrm{type}}{(\Gamma, a:A) \; \mathrm{ctx}} \qquad \frac{\Gamma \; \mathrm{ctx} \quad \Gamma \vdash \phi \; \mathrm{prop}}{(\Gamma, \phi \; \mathrm{true}) \; \mathrm{ctx}}$$

### Structural rules

There are three structural rules in logic over type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma, \Delta \vdash \mathcal{J} \quad \Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta\vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

## Typed predicate logic with equality

Sometimes, typed predicate logic comes with a notion of equality on all the types, [[propositional equality]], and the theory then becomes **typed predicate logic with equality**. 

Propositional equality of types and terms is formed by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A = B \; \mathrm{prop}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash a =_A b \; \mathrm{prop}}$$

Propositional equality has its own structural rules:  reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Reflexivity of propositional equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A = A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a =_A a \; \mathrm{true}}$$

* Symmetry of propositional equality

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true}}{\Gamma \vdash B = A \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash a =_A b \; \mathrm{true}}{\Gamma \vdash b =_A a \; \mathrm{true}}$$

* Transitivity of propositional equality

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true} \quad \Gamma \vdash B = C \; \mathrm{true}}{\Gamma \vdash A = C \; \mathrm{true}}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash c:A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma \vdash b =_A c \; \mathrm{true}}{\Gamma \vdash a =_A c \; \mathrm{true}}$$

* Principle of substitution of propositionally equal terms:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash B[a/x] = B[b/x] \; \mathrm{true}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a : A \quad \Gamma \vdash b : A \quad \Gamma \vdash a =_A b \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] =_{B[b/x]} c[b/x] \; \mathrm{true}}$$

* Variable conversion rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash A = B \; \mathrm{true} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

### Definitions

In any typed predicate logic with equality, we could formally define the [[single assignment operator]] $\coloneqq$ used in [[definitions]] in the theory itself. 

We add the following judgments to the theory:

* $\Gamma \vdash A' \coloneqq A \; \mathrm{type}$ - $A'$ is defined to be the type $A$ in context $\Gamma$.
* $\Gamma \vdash a' \coloneqq a : A$ - $a'$ is defined to be the term $a:A$ of type $A$ in context $\Gamma$.

The single assignment operator has its own structural rules: type formation, term introduction, and equality reflection.

* Formation and equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B = A \; \mathrm{true}}$$

* Introduction and equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b =_A a \; \mathrm{true}}$$

## Examples

* [[ZFC]]
* [[ETCS]]
* [[SEAR]]
* the first two layers of [[cubical type theory]] representing the theory of an [[interval]] primitive. 
* Some presentations of [[book HoTT]], where the first two layers of the presentation represent the theory of the [[natural numbers]] primitive. This additionally requires the theory to have [[split contexts]]. 

## See also

* [[predicate logic]]

* [[layered type theory]]

[[!redirects typed predicate logic]]
[[!redirects typed predicate logics]]
[[!redirects logic over type theory]]
[[!redirects logics over type theory]]
[[!redirects propositional logic over type theory]]
[[!redirects propositional logics over type theory]]
[[!redirects predicate logic over type theory]]
[[!redirects predicate logics over type theory]]
[[!redirects typed predicate logic with equality]]
[[!redirects typed predicate logics with equality]]