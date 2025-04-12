
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[type theory]] a _function type_ $X \to Y$ for two [[types]] $X,Y$ is the [[type]] of [[functions]] from $X$ to $Y$. 

In a [[model]] of the type theory in [[categorical semantics]], this is an [[exponential object]]. In [[set theory]], it is a [[function set]]. In [[dependent type theory]], it is a special case of a [[dependent product type]].

Function types are important because they allow the user to [[quantification|quantify]] over [[functions]] in [[type theory]]. In [[material set theory]] functions are sets and one could quantify over sets, while in [[structural set theory]], while functions are different from sets, one could still quantify over the [[sort]] of functions. However, in [[type theory]], one cannot quantify over families of elements $x:A \vdash b(x):B$, which are the analogue of functions in material and structural set theory, since families of elements are not elements of a single type, and quantification only occurs over a single type. Instead, one uses function types whose elements, called functions, represent families of elements, in the same way that the elements of [[type universes]] represent types. 

## Overview

[[!include function type natural deduction - table]]

## Definition

Like any type constructor in type theory, a function type is specified by rules saying when we can introduce it as a type, how to [[term introduction|construct terms]] of that type, how to use or "[[term elimination|eliminate]]" terms of that type, and how to compute when we combine the constructors with the eliminators.

The [[type formation]] rule to build a function type is easy:

$$\frac{A\colon Type \qquad B \colon Type}{A\to B\colon Type}$$

### As a negative type

Function types are almost always defined as a [[negative type]].  In this presentation, primacy is given to the eliminators.  The natural eliminator of a function type says that we can [[function application|apply]] it to any input:

$$\frac{f\colon A\to B \qquad a\colon A}{f(a) \colon B}$$

The constructor is then determined as usual for a negative type: to construct a term of $A\to B$, we have to specify how it behaves when applied to any input.  In other words, we should have a term of type $B$ containing a free variable of type $A$.  This yields the usual "$\lambda$-abstraction" constructor:

$$\frac{x\colon A\vdash b\colon B}{\lambda x.b\colon A\to B}$$

The [[∞-reduction]] rule is the obvious one (the ur-example of all $\beta$-reductions), saying that when we evaluate a $\lambda$-abstraction, we do it by substituting for the bound variable.

$$(\lambda x.b)(a) \;\to_\beta\; b[a/x]$$

If we want an [[∞-conversion]] rule, the natural one says that every function is a $\lambda$-abstraction:

$$ \lambda x.f(x) \;\to_\eta\; f$$

### As a positive type
{#AsPositiveType}

It is also possible to present function types as a [[positive type]].  However, this requires a stronger metatheory, such as a [[logical framework]].  We use the same constructor ($\lambda$-abstraction), but now the eliminator says that to define an operation using a function, it suffices to say what to do in the case that that function is a lambda abstraction.

$$\frac{(x\colon A \vdash b\colon B) \vdash c\colon C \qquad f\colon A\to B}{funsplit(c,f)\colon C}$$

This rule cannot be formulated in the usual presentation of type theory, since it involves a "higher-order judgment": the context of the term $c\colon C$ involves a "term of type $B$ containing a free variable of type $A$".  However, it is possible to make sense of it.  In [[dependent type theory]], we need additionally to allow $C$ to depend on $A\to B$.

The natural $\beta$-reduction rule for this eliminator is

$$ funsplit(c, \lambda x.g) \;\to_\beta c[g/b] $$

and its $\eta$-conversion rule looks something like

$$ funsplit(c[\lambda x.b / g], f) \;\to_\eta\; c[f/g]. $$

Here $g\colon A\to B \vdash c\colon C$ is a term containing a free variable of type $A\to B$.  By substituting $\lambda x.b$ for $g$, we obtain a term of type $C$ which depends on "a term $b\colon B$ containing a free variable $x\colon A$".  We then apply the positive eliminator at $f\colon A\to B$, and the $\eta$-rule says that this can be computed by just substituting $f$ for $g$ in $c$.

### Positive versus negative

As usual, the positive and negative formulations are equivalent in a suitable sense.  They have the same constructor, while we can formulate the eliminators in terms of each other:

$$
\begin{aligned}
  f(a) &\coloneqq funsplit(b[a/x], f)\\
  funsplit(c, f) &\coloneqq c[f(x)/b]
\end{aligned}
$$

The conversion rules also correspond.

In dependent type theory, this definition of $funsplit$ only gives us a properly typed dependent eliminator if the negative function type satisfies $\eta$-conversion.  As usual, if it satisfies [propositional eta-conversion](/nlab/show/eta-conversion#Propositional) then we can transport along that instead---and conversely, the dependent eliminator allows us to prove propositional $\eta$-conversion.  This is the content of Propositions 3.5, 3.6, and 3.7 in [(Garner)](#GarnerSDP).

### Function types a la Russell and a la Tarski

In [[dependent type theory]], there are two different ways to interpret the term $f:A \to B$: 

1. $f$ is literally a family of terms in $B$ indexed by $A$

1. $f$ is a term representation for a family of terms in $B$ indexed by $A$

This situation is similar to how there are two notions of [[type universe]] where [[small types]] of a universe are interpreted [[Russell universe|a la Russell]], literally as types, or [[Tarski universe|a la Tarski]], as a term representation of types. Thus, in analogy to type universes, we can refer to function types *a la Russell* and function types *a la Tarski*. 

Function types a la Russell and a la Tarski are expressed respectively via the [[elimination rule]] of function types: 

* given types $A$ and $B$ and a term $f:A \to B$, one could form the family of terms $x:A \vdash f(x):B$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma, x:A \vdash f(x):B}$$

* given types $A$ and $B$, one could form the family of terms $f:A \to B, x:A \vdash \mathrm{eval}(f, x):B$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A \vdash \mathrm{eval}(f, x):B}$$

Function types a la Tarski corresponds to the notion of [[exponential object]] in [[category theory]] where the exponential object $B^A$ literally comes with a morphism $\mathrm{eval}:B^A \times A \to B$, but function types a la Russell are the one most commonly used in [[dependent type theory]]. 

The conversion rules for function types a la Russell are as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma, x:A \vdash (\lambda x:A.b(x))(x) \equiv b(x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma \vdash f \equiv \lambda x:A.f(x):A \to B}$$

and the conversion rules for function types a la Tarski are as follows: 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma, x:A \vdash \mathrm{eval}(\lambda x:A.b(x), x) \equiv b(x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash f \equiv \lambda x:A.\mathrm{eval}(f, x):A \to B}$$

For the rest of the article we shall assume the use of function types a la Russell. 

### Weak and strict function types

In [[dependent type theory]], **weak function types** are function types for which the [[computation rules]] ($\beta$-conversion) and [[uniqueness rules]] ($\eta$-conversion) are propositional rather than judgmental:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma, a:A \vdash \beta_{A \to B}^{x:A.b(x)}(a):(\lambda(x:A).b(x))(a) =_{B} b(a)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \eta_{A \to B}(f):f =_{A \to B} \lambda(x:A).f(x)}$$

Weak function types appear in [[weak type theories]]. 

This contrasts with **strict function types** which use judgmental computation and uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B}{\Gamma, a:A \vdash (\lambda(x:A).b(x))(a) \equiv b(a):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash f \equiv \lambda(x:A).f(x):A \to B}$$

Strict function types appear in most dependent type theories such as [[Martin-Löf type theory]], [[observational type theory]], and [[cubical type theory]].

For strict function types, the judgmental computation and uniqueness rules automatically imply the propositional computation and uniqueness rules, as by the rules for [[judgmental equality]] and [[identity types]], judgmental equality of two terms always implies propositional equality of the two terms. 

### As types of anafunctions

In [[dependent type theory]], in the same way that one could define [[equivalence types]] as types of [[one-to-one correspondences]], one could also define function types as types of [[anafunctions]]. This requires both [[identity types]] and [[heterogeneous identity types]] being defined first, which we shall write as $a =_A b$ and $x =_{B}^{p} y$ respectively for $a:A$, $b:A$, $p:a =_A b$, $x:B(a)$, and $y:B(b)$.  

Rules for function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A, y:B \vdash \mathcal{F}_{A, B}(f, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B}{\Gamma \vdash x \mapsto f(x):A \to B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B}{\Gamma, x:A \vdash \alpha(x):\mathcal{F}_{A, B}(x \mapsto f(x), x, f(x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A \vdash \mathrm{ev}(f, x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A \vdash \beta(f, x):\mathcal{F}_{A, B}(f, x, \mathrm{ev}(f, x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A, y:B,  u:\mathcal{F}_{A, B}(f, x, y) \vdash \kappa(f, x, y, u):\mathrm{ev}(f, x) =_B y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B, x:A, y:B,  u:\mathcal{F}_{A, B}(f, x, y) \vdash \eta(f, x, y, u):\beta(f, x) =_{\mathcal{F}_{A, B}(f, x)}^{\kappa(f, x, y, u)} u}$$

By the rules for [[dependent sum types]] and [[dependent product types]], one could derive that 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \eta(f):\prod_{x:A} \mathrm{isContr}\left(\sum_{y:B} \mathcal{F}_{A, B}(f, x, y) \right)}$$

which is precisely the statement that $\mathcal{F}_{A, B}(f)$ is an [[anafunction]] for all functions $f:A \to B$. 

## Properties

### Relation to dependent product types

In [[dependent type theory]] a function type $A \to B$ is the special case the [[dependent product type]] over $a : A$ for the special case that $B$ is regarded as an $A$-[[dependent type]] $x:A \vdash B$ that actually happens to be $A$-independent; this type family $x:A \vdash B$ can always be constructed by the [[weakening rule]] of dependent type theory, which is an [[admissible rule]]. 

$$
  (X \to A)
  = 
  \prod_{x \colon X} A
  \,.
$$

In [[categorical semantics]] this is the statement that a [[section]] of a product [[projection]] $A \times B \to A$ is equivalently just a morphism $A \to B$. 

See also at _[[function monad]]_.

### Typal congruence rules and uniqueness rules

The typal computation rule for function types is provable from the other four typal type formers of function types. Given types $A$ and $B$ and function $f:A \to B$, we have, by the elimination rule and the introduction rule, a function $\lambda x:A.f(x):A \to B$, which by the uniqueness rules of dependent product types are equal to each other 
$$\eta_{A \to B}(f):f =_{A \to B} \lambda x:A.f(x)$$ 
By the inductively defined function $\mathrm{idtohomotopy}$ which takes [[identifications]] between functions to [[homotopies]] between functions]], we have that 
$$\mathrm{idtohomotopy}(f, \lambda x:A.f(x))(\eta_{A \to B}(f)):\prod_{x:A} f(x) =_{A \to B} (\lambda x:A.f(x))(x)$$
which is the typal computation rule for function types. 

### Function types as hom-objects
 {#AsHomObjects}

Function types play the role of [[hom-objects]] in a kind of [[enriched category]] whose objects are the [[types]]. (In fact, in the presence of compatible [[product types]] this is a [[cartesian closed category]]-structure, cf. [Lambek & Scott 1986](relation+between+type+theory+and+category+theory#LambekScott86)). They have [[identity functions]] and a [[composition]]-operation which together satisfy the [[associativity]] and [[unitality]] laws:

* For strict function types, the associative and unital laws are represented by judgmental equality

* For weak function types, the associative and unital laws are represented by [[associator]] and [[unitor]] [[homotopies]], and, assuming [[function extensionality]], also by [[associator]] and [[unitor]] [[identifications]]. In addition, there is also an infinite tower of [[coherence laws]] representing the [[(infinity,1)-category|$(\infty,1)$-categorical structure]] of function types by constructing the [[pentagonator]] and so forth, but this isn't demonstrated in this section, and is unnecessary in the presence of a [[set truncation axiom]] like [[UIP]] or [[axiom K]]. 

#### Strict function types 

\begin{definition}
Given a type $A$, we define the **identity function** on $A$ as the function

$$\mathrm{id}_A \equiv \lambda (x:A).x:A \to A$$
\end{definition}

\begin{theorem}
By the computation rules for strict function types, the identity function on a type $A$ comes with a family of judgmental equalities

$$x:A \vdash \mathrm{id}_A(x) \equiv x:A$$
\end{theorem}

\begin{definition}
Given types $A$, $B$, and $C$ and functions $f:A \to B$, and $g:B \to C$, **function composition** of $f$ and $g$ is defined as

$$g \circ_{A, B, C} f \equiv \lambda (x:A).g(f(x)):A \to C$$
\end{definition}

\begin{theorem}
By the computation rules for strict function types, function composition comes with a family of judgmental equalities

$$x:A \vdash (g \circ_{A, B, C} f)(x) \equiv g(f(x)):C$$
\end{theorem}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, there is a family of judgmental equalities

$$x:A \vdash (\mathrm{id}_B \circ_{A, B, B} f)(x) \equiv f(x):B$$
\end{theorem}

\begin{proof}
By the computation rule for strict function types, there is a family of judgmental equalities

$$x:A \vdash (\mathrm{id}_B \circ_{A, B, B} f)(x) \equiv \mathrm{id}_B(f(x)):B$$

and a family of judgmental equalities

$$x:A \vdash \mathrm{id}_B(f(x)) \equiv f(x):B$$

Now, by the [[structural rules]] for [[judgmental equality]], there is a family of judgmental equalities

$$x:A \vdash (\mathrm{id}_B \circ_{A, B, B} f)(x) \equiv f(x):B$$
\end{proof}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, there is a family of judgmental equalities

$$x:A \vdash (f \circ_{A, A, B} \mathrm{id}_A)(x) \equiv f(x):B$$
\end{theorem}

\begin{proof}
By the computation rule for strict function types, there is a family of judgmental equalities

$$x:A \vdash (f \circ_{A, A, B} \mathrm{id}_A)(x) \equiv f(\mathrm{id}_A(x)):B$$

and a family of identifications

$$x:A \vdash f(\mathrm{id}_A(x)) \equiv f(x):B$$

Now, by the [[structural rules]] for [[judgmental equality]], there is a family of judgmental equalities

$$x:A \vdash (f \circ_{A, A, B} \mathrm{id}_A)(x) \equiv f(x):B$$
\end{proof}

\begin{theorem}
For all types $A$, $B$, $C$, and $D$, and functions $f:A \to B$, $g:B \to C$, and $h:C \to D$, there is a family of judgmental equalities

$$x:A \vdash (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) \equiv ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x):D$$
\end{theorem}

\begin{proof}
By the computation rule for strict function types, there are families of judgmental equalities

$$x:A \vdash (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) \equiv h((g \circ_{A, B, C} f)(x)):D$$

$$x:A \vdash ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x) \equiv (h \circ_{B, C, D} g)(f(x)):D$$

$$x:A \vdash (h \circ_{B, C, D} g)(f(x)) \equiv h(g(f(x))):D$$

$$x:A \vdash h((g \circ_{A, B, C} f)(x)) \equiv h(g(f(x)):D$$

Now, by the [[structural rules]] for [[judgmental equality]], there is a family of judgmental equalities

$$x:A \vdash (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) \equiv ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x):D$$
\end{proof}

Now, the judgmental [[uniqueness rule]] for strict function types implies function extensionality for judgmental equality: for types $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$ such that there is a family of judgmental equalities $x:A \vdash f(x) \equiv g(x):B$, there is a judgmental equality $f \equiv g:A \to B$. (See exercise 2.1 of [Rijke 2022](#Rijke22))

As a result, the associative and unital laws hold for functions:

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, there is a judgmental equality 

$$\mathrm{id}_B \circ_{A, B, B} f \equiv f:A \to B$$
\end{theorem}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, there is a judgmental equality 

$$f \circ_{A, A, B} \mathrm{id}_A \equiv f:A \to B$$
\end{theorem}

\begin{theorem}
For all types $A$, $B$, $C$, and $D$, and functions $f:A \to B$, $g:B \to C$, and $h:C \to D$, there is a judgmental equality

$$(h \circ_{A, C, D} (g \circ_{A, B, C} f)) \equiv ((h \circ_{B, C, D} g) \circ_{A, B, D} f):A \to D$$
\end{theorem}

#### Weak function types

\begin{definition}
Given a type $A$, we define the **identity function** on $A$ as the function

$$\mathrm{id}_A \equiv \lambda (x:A).x:A \to A$$
\end{definition}

\begin{theorem}
By the computation rules for weak function types, the identity function on a type $A$ comes with a family of identifications

$$x:A \vdash \beta_{A \to A}^{x:A.x}(x):\mathrm{id}_A(x) =_{A} x$$
\end{theorem}

\begin{definition}
Given types $A$, $B$, and $C$ and functions $f:A \to B$, and $g:B \to C$, **function composition** of $f$ and $g$ is defined as

$$g \circ_{A, B, C} f \equiv \lambda (x:A).g(f(x)):A \to C$$
\end{definition}

\begin{theorem}
By the computation rules for weak function types, function composition comes with a family of identifications

$$x:A \vdash \beta_{A \to C}^{x:A.g(f(x))}(x):(g \circ_{A, B, C} f)(x) =_{C} g(f(x))$$
\end{theorem}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, the dependent function type

$$\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$

has a homotopy. 
\end{theorem}

\begin{proof}
By the computation rule for weak function types, there is a family of identifications

$$x:A \vdash \beta_{A \to B}^{x:A.\mathrm{id}_B(f(x))}(x):(\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} \mathrm{id}_B(f(x))$$

and a family of identifications

$$x:A \vdash \beta_{B \to B}^{x:A.f(x)}(x):\mathrm{id}_B(f(x)) =_{B} f(x)$$

Now, by concatenating the individual identifications together and then using lambda abstraction, we have the homotopy

$$\lambda (x:A).\beta_{A \to B}^{x:A.\mathrm{id}_B(f(x))}(x) \bullet \beta_{B \to B}^{x:A.f(x)}(x):\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **left unitor homotopy** as the homotopy 

$$\mathrm{lunith}_{A, B}(f) \equiv \lambda (x:A).\beta_{A \to B}^{x:A.\mathrm{id}_B(f(x))}(x) \bullet \beta_{B \to B}^{x:A.f(x)}(x):\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$
\end{definition}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, the dependent function type

$$\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)$$

has a homotopy. 
\end{theorem}

\begin{proof}
By the computation rule for weak function types, there is a family of identifications

$$x:A \vdash \beta_{A \to B}^{x:A.f(\mathrm{id}_A(x))}(x):(f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(\mathrm{id}_A(x))$$

and also by the action on identifications of the function $f:A \to B$, a family of identifications

$$x:A \vdash \mathrm{ap}_B(f, \mathrm{id}_A(x), x, \beta_{A \to A}^{x:A.x}(x)):f(\mathrm{id}_A(x)) =_{B} f(x)$$

Now, by concatenating the individual identifications together and then using lambda abstraction, we have the homotopy

$$\lambda (x:A).\beta_{A \to B}^{x:A.f(\mathrm{id}_A(x))}(x) \bullet \mathrm{ap}_B(f, \mathrm{id}_A(x), x, \beta_{A \to A}^{x:A.x}(x)):\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **right unitor homotopy** as the homotopy 

$$\mathrm{runith}_{A, B}(f) \equiv \lambda (x:A).\beta_{A \to B}^{x:A.f(\mathrm{id}_A(x))}(x) \bullet \mathrm{ap}_B(f, \mathrm{id}_A(x), x, \beta_{A \to A}^{x:A.x}(x)):\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)$$
\end{definition}

\begin{theorem}
For all types $A$, $B$, $C$, and $D$, and functions $f:A \to B$, $g:B \to C$, and $h:C \to D$, the dependent function type

$$\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)$$

has a homotopy. 
\end{theorem}

\begin{proof}
By the computation rule for weak function types, there are families of identifications

$$x:A \vdash \beta_{A \to D}^{x:A.h((g \circ_{A, B, C} f)(x))}(x):(h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} h((g \circ_{A, B, C} f)(x))$$

$$x:A \vdash \beta_{A \to D}^{x:A.(h \circ_{B, C, D} g)(f(x))}(x):((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x) =_{D} (h \circ_{B, C, D} g)(f(x))$$

$$x:A \vdash \beta_{A \to D}^{x:A.h(g(f(x)))}(x):(h \circ_{B, C, D} g)(f(x)) =_{D} h(g(f(x)))$$

and also by the action on identifications of the function $h:C \to D$, there is a family of identifications

$$x:A \vdash \mathrm{ap}_D(h, (g \circ_{A, B, C} f)(x), g(f(x)), \beta_{A \to C}^{x:A.g(f(x))}(x)):h((g \circ_{A, B, C} f)(x)) =_{D} h(g(f(x))$$

Now, by concatenating and inverting the individual identifications together and then using lambda abstraction, we have the homotopy

$$\begin{array}{c}
	\lambda (x:A).\beta_{A \to D}^{x:A.h((g \circ_{A, B, C} f)(x))}(x) \bullet \mathrm{ap}_D(h, (g \circ_{A, B, C} f)(x), g(f(x)), \beta_{A \to C}^{x:A.g(f(x))}(x)) \\
	 \bullet \beta_{A \to D}^{x:A.h(g(f(x)))}(x)^{-1} \bullet \beta_{A \to D}^{x:A.(h \circ_{B, C, D} g)(f(x))}(x)^{-1}:\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)
\end{array}
$$
\end{proof}

\begin{definition}
For types $A$, $B$, $C$, and $D$ and functions $f:A \to B$, $f:B \to C$, and $h:C \to D$, we define the **associator homotopy** as the homotopy 

$$\begin{array}{c}
	\mathrm{assoch}_{A, B, C, D}(f, g, h) \equiv \lambda (x:A).\beta_{A \to D}^{x:A.h((g \circ_{A, B, C} f)(x))}(x) \bullet \mathrm{ap}_D(h, (g \circ_{A, B, C} f)(x), g(f(x)), \beta_{A \to C}^{x:A.g(f(x))}(x)) \\
	 \bullet \beta_{A \to D}^{x:A.h(g(f(x)))}(x)^{-1} \bullet \beta_{A \to D}^{x:A.(h \circ_{B, C, D} g)(f(x))}(x)^{-1}:\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)
\end{array}
$$
\end{definition}

Now, recall that the canonical $\mathrm{idtohomotopy}$ function 

$$\mathrm{idtohomotopy}_{A, B}(f, g):f =_{A \to B} g \to \prod_{x:A} f(x) =_{B} g(x)$$

is inductively defined by

$$\mathrm{idtohomotopy}_{A, B}(f, f)(\mathrm{refl}_{A \to B}(f)) \equiv \lambda (x:A).\mathrm{refl}_{B}(f(x)):\prod_{x:A} f(x) =_{B} g(x)$$

[[function extensionality]] states that $\mathrm{idtohomotopy}_{A, B}(f, g)$ is an [[equivalence of types]] for all functions $f:A \to B$ and $g:A \to B$

$$\mathrm{funext}_{A, B}:\prod_{f:A \to B} \prod_{g:A \to B} \mathrm{isEquiv}(\mathrm{idtohomotopy}_{A, B}(f, g))$$

Thus, there is an [[inverse function]] 

$$\mathrm{idtohomotopy}_{A, B}(f, g)^{-1}:\left(\prod_{x:A} \mathrm{Id}_{B}(f(x), g(x))\right) \to f =_{A \to B} g$$

With function extensionality, we can now prove the associative and unital laws, showing that function are a category:

\begin{theorem}
Assuming function extensionality, for all types $A$ and $B$ and functions $f:A \to B$, the identity type

$$\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$

has an identification.
\end{theorem}

\begin{proof}
By function extensionality, the function 

$$\mathrm{idtohomotopy}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f):(\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f) \to \prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$ 

has an inverse function 

$$\mathrm{idtohomotopy}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}:\left(\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)\right) \to (\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f)$$

One then gets the identification

$$\mathrm{idtohomotopy}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}(\mathrm{lunith}_{A, B}(f)):\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **left unitor** as the identification 

$$\mathrm{lunit}_{A, B}(f) \equiv \mathrm{idtohomotopy}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}(\mathrm{lunith}_{A, B}(f)):\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$
\end{definition}

\begin{theorem}
Assuming function extensionality, for all types $A$ and $B$ and functions $f:A \to B$, the identity type

$$f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$

has an identification.
\end{theorem}

\begin{proof}
By function extensionality, the function 

$$\mathrm{idtohomotopy}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f):(f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f) \to \prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)$$ 

has an inverse function 

$$\mathrm{idtohomotopy}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}:\left(\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)\right) \to (f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f)$$

One then gets the identification

$$\mathrm{idtohomotopy}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}(\mathrm{runith}_{A, B}(f)):f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **right unitor** as the identification 

$$\mathrm{runit}_{A, B}(f) \equiv \mathrm{idtohomotopy}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}(\mathrm{runith}_{A, B}(f)):f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$
\end{definition}

\begin{theorem}
Assuming function extensionality, for all types $A$, $B$, $C$, and $D$ and functions $f:A \to B$, $f:B \to C$, and $h:C \to D$, the identity type

$$h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f$$

has an identification.
\end{theorem}

\begin{proof}
By function extensionality, the function 

$$
\begin{array}{c}
	\mathrm{idtohomotopy}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f): \\
	(h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f) \\
	\to \prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)
\end{array}
$$ 

has an inverse function 

$$
\begin{array}{c}
	\mathrm{idtohomotopy}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}: \\
	\left(\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)\right) \\
	\to (h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f)
\end{array}
$$ 

One then gets the identification

$$
\begin{array}{c}
	\mathrm{idtohomotopy}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}(\mathrm{assoch}_{A, B, C, D}(f, g, h)):\\
	h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f
\end{array}
$$
\end{proof}

\begin{definition}
For types $A$, $B$, $C$, and $D$ and functions $f:A \to B$, $f:B \to C$, and $h:C \to D$, we define the **associator** as the identification 

$$
\begin{array}{c}
	\mathrm{assoc}_{A, B, C, D}(f, g, h) \equiv \mathrm{idtohomotopy}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}(\mathrm{assoch}_{A, B, C, D}(f, g, h)):\\
	h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f
\end{array}
$$
\end{definition}

### Typal congruence rules

These are called *typal congruence rules* because they are the analogue of the judgmental [[congruence rules]] which use [[identity types]] and [[equivalence types]] instead of [[judgmental equality]].

#### Strict function types

Since [[function types]] are negative types, we first present the typal congruence rule for the elimination rule of function types

\begin{theorem}
Given types $A$ and $B$, functions $f:A \to B$ and $g:A \to B$ and an identification $p:f =_{A \to B} g$ there are families of identifications $x:A \vdash \mathrm{compelim}(f, g, p)(x):f(x) =_B g(x)$. 
\end{theorem}

\begin{proof}
We simply define the dependent function $\mathrm{compelim}$ to be the canonical inductively defined function $\mathrm{idtohomotopy}$ which takes identifications between functions to homotopies between functions. 
\end{proof}

The next is the typal congruence rule for the introduction rule of function types. However, unlike the case for the other two rules, one needs function extensionality. 

\begin{theorem}
Assuming [[function extensionality]], given types $A$ and $B$, families of elements $x:A \vdash b(x):B$ and $x:A \vdash b'(x):B$, and families of [[identifications]] $x:A \vdash p(x):b(x) =_B b'(x)$, there is an identification 
$$\mathrm{congintro}_{x:A.p(x)}:\lambda (x:A).b(x) =_{A \to B} \lambda (x:A).b'(x)$$
\end{theorem}

\begin{proof}
By the computation rule of strict function types, there are families of judgmental equalities 

$$x:A \vdash ((\lambda x:A.b(x))(x) \equiv b(x):B$$
$$x:A \vdash ((\lambda x:A.b'(x))(x) \equiv b'(x):B$$

Thus, by the [[structural rules]] of [[judgmental equality]], there are families of identificaitons 

$$x:A \vdash p(x):(\lambda x:A.b(x))(x) =_B (\lambda x:A.b'(x))(x)$$

and by $\lambda$-abstraction, one gets the dependent function

$$\lambda (x:A).p(x):\prod_{x:A} (\lambda x:A.b(x))(x) =_B (\lambda x:A.b'(x))(x)$$

By [[function extensionality]], there is an [[equivalence of types]]

$$\mathrm{funext}:(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x)) \simeq \prod_{x:A} \mathrm{Id}_B((\lambda x:A.b(x))(x), (\lambda x:A.b'(x))(x))$$

which yields an identification 

$$\mathrm{funext}^{-1}(\lambda (x:A).p(x)):(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x))$$

We define 

$$\mathrm{congintro}_{x:A.p(x)} \coloneqq \mathrm{funext}^{-1}(\lambda (x:A).p(x)):(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x))$$
\end{proof}

Finally, we present the typal congruence rule for the formation rule of function types, which relies upon the previous two results. 

\begin{theorem}
Given types $A$, $A'$, $B$, $B'$ and equivalences $e_A:A \simeq A'$ and $e_B:B \simeq B'$, there is an equivalence 
$$\mathrm{congform}(e_A, e_B):(A \to B) \simeq (A' \to B')$$
\end{theorem}

\begin{proof}
We define the function $\mathrm{congform}(e_A, e_B):(A \to B) \to (A' \to B')$ by 

$$\mathrm{congform}(e_A, e_B) \coloneqq \lambda (f:A \to B).\lambda x:A'.e_B(f(e_A^{-1}(x)))$$

and the inverse function by

$$\mathrm{congform}(e_A, e_B)^{-1} \coloneqq \lambda (g:A' \to B').\lambda x:A.e_B^{-1}(g(e_A(x)))$$

Now it suffices to construct homotopies 

$$\prod_{f:A \to B} \mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{A \to B} f$$

$$\prod_{g:A' \to B'} \mathrm{congform}(e_A, e_B)(\mathrm{congform}(e_A, e_B)^{-1}(g)) =_{A' \to B'} g$$

from where it implies that $\mathrm{congform}(e_A, e_B)$ has a coherent inverse and contractible fibers and is thus an [[equivalence of types]]. 

By definition, 
$$\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) \equiv \lambda x:A.e_B^{-1}((\lambda x:A'.e_B(f(e_A^{-1}(x))))(e_A(x)))$$

By the computation rules of strict function types, there is a family of judgmental equalities
$$x:A \vdash (\lambda x:A'.e_B(f(e_A^{-1}(x))))(e_A(x)) \equiv e_B(f(e_A^{-1}(e_A(x))))$$
and thus by the structural rules of [[judgmental equalities]] and the judgmental congruence rules for function types, a judgmental equality
$$\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) \equiv \lambda x:A.e_B^{-1}(e_B(f(e_A^{-1}(e_A(x)))))$$

The equivalence $e_B:B \simeq B'$ has a family of identifications 
$$x:B \vdash \mathrm{ret}_{e_B}(x):e_B^{-1}(e_B(x)) =_{B} x$$
witnessing that $e_B^{-1}$ is a [[retraction]] of $e_B$. 

This means that by applying the canonical inductively defined function $\mathrm{idtohomotopy}$ which takes identifications between functions to homotopies between functions, one gets the family of identifications
$$\mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))):e_B^{-1}(e_B(f(e_A^{-1}(e_A(x))))) =_{B} f(e_A^{-1}(e_A(x)))$$

Similarly, the equivalence $e_A:A \simeq A'$ has a family of identifications 
$$x:B \vdash \mathrm{ret}_{e_A}(x):e_A^{-1}(e_A(x)) =_{A} x$$
witnessing that $e_A^{-1}$ is a [[retraction]] of $e_A$. 

This means by applying $f$ to the above family of identifications, one gets the family of identifications
$$x:A \vdash \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x)):f(e_A^{-1}(e_A(x))) =_{B} f(x)$$

By concatenation of identifications, one gets the family of identifications

$$x:A \vdash \mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))) \bullet \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x)):e_B^{-1}(e_B(f(e_A^{-1}(e_A(x))))) =_{B} f(x)$$

By lambda abstraction, one gets the homotopy
$$\lambda x:A.\mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))) \bullet \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x)):\prod_{x:A} e_B^{-1}(e_B(f(e_A^{-1}(e_A(x))))) =_{B} f(x)$$
and by function extensionality, this is the same as 
$$\mathrm{funext}^{-1}(\lambda x:A.\mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))) \bullet \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x))):\lambda (x:A).e_B^{-1}(e_B(f(e_A^{-1}(e_A(x))))) =_{A \to B} \lambda x:A.f(x)$$

By the computation rules of strict function types and the structural rules of judgmental equality, the type 
$$\lambda (x:A).e_B^{-1}(e_B(f(e_A^{-1}(e_A(x))))) =_{A \to B} \lambda x:A.f(x)$$ 
is judgmentally equal to $\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{A \to B} f$, so we have 
$$\mathrm{funext}^{-1}(\lambda x:A.\mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))) \bullet \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x))):\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{A \to B} f$$

$\lambda$-abstraction on functions $f:A \to B$ leads to the dependent function

$$\lambda (f:A \to B).\mathrm{funext}^{-1}(\lambda x:A.\mathrm{idtohomotopy}(\lambda x:A.e_B^{-1}(e_B(x)), \lambda x:A.x, f(e_A^{-1}(e_A(x))) \bullet \mathrm{ap}(f, e_A^{-1}(e_A(x)), x, \mathrm{ret}_{e_A}(x))):\prod_{f:A \to B} \mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{A \to B} f$$

By a similar argument swapping the types around and the corresponding equivalences with inverse equivalences; one also has 
$$\lambda (g:A' \to B').\mathrm{funext}^{-1}(\lambda x:A'.\mathrm{idtohomotopy}(\lambda x:A'.e_B(e_B^{-1}(x)), \lambda x:A'.x, g(e_A(e_A^{-1}(x))) \bullet \mathrm{ap}(g, e_A(e_A^{-1}(x)), x, \mathrm{ret}_{e_A^{-1}}(x))):\prod_{g:A' \to B'} \mathrm{congform}(e_A, e_B)(\mathrm{congform}(e_A, e_B)^{-1}(g)) =_{A' \to B'} g$$

Thus, $\mathrm{congform}(e_A, e_B):(A \to B) \to (A' \to B')$ is an equivalence of types. 
\end{proof}

#### Weak function types

\begin{theorem}
Given types $A$, $A'$, $B$, $B'$ and equivalences $e_A:A \simeq A'$ and $e_B:B \simeq B'$, there is an equivalence 
$$\mathrm{congform}(e_A, e_B):(A \to B) \simeq (A' \to B')$$
\end{theorem}

\begin{proof}
We define the function $\mathrm{congform}(e_A, e_B):(A \to B) \to (A' \to B')$ by 

$$\mathrm{congform}(e_A, e_B) \coloneqq \lambda (f:A \to B).\lambda x:A'.e_B(f(e_A^{-1}(x)))$$

and the inverse function by

$$\mathrm{congform}(e_A, e_B)^{-1} \coloneqq \lambda (g:A' \to B').\lambda x:A.e_B^{-1}(g(e_A(x)))$$

Now it suffices to construct homotopies 

$$\prod_{f:A \to B} \mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{A \to B} f$$

$$\prod_{g:A' \to B'} \mathrm{congform}(e_A, e_B)(\mathrm{congform}(e_A, e_B)^{-1}(g)) =_{A' \to B'} g$$

from where it implies that $\mathrm{congform}(e_A, e_B)$ has a coherent inverse and contractible fibers and is thus an [[equivalence of types]]. 

To be finished...
\end{proof}

Since [[function types]] are negative types, we first present the typal congruence rule for the elimination rule of function types

\begin{theorem}
Given types $A$ and $B$, functions $f:A \to B$ and $g:A \to B$ and an identification $p:f =_{A \to B} g$ there are families of identifications $x:A \vdash \mathrm{compelim}(f, g, p)(x):f(x) =_B g(x)$. 
\end{theorem}

\begin{proof}
We simply define the dependent function $\mathrm{compelim}$ to be the canonical inductively defined function $\mathrm{idtohomotopy}$ which takes identifications between functions to homotopies between functions. 
\end{proof}

The next is the typal congruence rule for the uniqueness rule of function types.

\begin{theorem}
Given types $A$ and $B$, functions $f:A \to B$ and $g:A \to B$, and an identification $p:f =_{A \to B} g$, there is an identification 

$$\mathrm{etaCong}_{A \to B}(f, g, p):\mathrm{transport}_{h:A \to B.h =_{A \to B} \lambda x:A.h(x)}(f, g, p)(\eta_{A \to B}(f)) =_{g =_{A \to B} \lambda x:A.g(x)} \eta_{A \to B}(g)$$
\end{theorem}

\begin{proof}
We simply define $\mathrm{etaCong}_{A \to B}(f, g, p)$ to be the [[dependent function application to identifications]] 
$$\mathrm{apd}_{h:A \to B.h =_{A \to B} \lambda x:A.h(x)}(\lambda x:A \to B.\eta_{A \to B}(x), f, g, p)$$ 
where
$$f:A \to B \vdash \eta_{A \to B}(f):f =_{A \to B} \lambda x:A.f(x)$$
is the family of elements in the conclusion of the uniqueness rule for weak function types. 
\end{proof}

The next is the typal congruence rule for the introduction rule of function types. However, unlike the case for the other two rules, one needs function extensionality. 

\begin{theorem}
Assuming [[function extensionality]], given types $A$ and $B$, families of elements $x:A \vdash b(x):B$ and $x:A \vdash b'(x):B$, and families of [[identifications]] $x:A \vdash p(x):b(x) =_B b'(x)$, there is an identification 
$$\mathrm{congintro}_{x:A.p(x)}:\lambda (x:A).b(x) =_{A \to B} \lambda (x:A).b'(x)$$
\end{theorem}

\begin{proof}
By the computation rule of weak function types, there are families of identifications 

$$x:A \vdash \beta_{A \to B}^{x:A.b(x)}(b(x)):((\lambda x:A.b(x))(x) =_{B} b(x)$$
$$x:A \vdash \beta_{A \to B}^{x:A.b'(x)}(b'(x)):((\lambda x:A.b'(x))(x) =_{B} b'(x)$$

Thus, there are families of identifications 

$$x:A \vdash \beta_{A \to B}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{A \to B}^{x:A.b'(x)}(b'(x))^{-1}:(\lambda x:A.b(x))(x) =_B (\lambda x:A.b'(x))(x)$$

and by $\lambda$-abstraction, one gets the dependent function

$$\lambda (x:A).\beta_{A \to B}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{A \to B}^{x:A.b'(x)}(b'(x))^{-1}:\prod_{x:A} (\lambda x:A.b(x))(x) =_B (\lambda x:A.b'(x))(x)$$

By [[function extensionality]], there is an [[equivalence of types]]

$$\mathrm{funext}:(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x)) \simeq \prod_{x:A} (\lambda x:A.b(x))(x) =_B (\lambda x:A.b'(x))(x)$$

which yields an identification 

$$\mathrm{funext}^{-1}(\lambda (x:A).\beta_{A \to B}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{A \to B}^{x:A.b'(x)}(b'(x))^{-1}):(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x))$$

We define 

$$\mathrm{congintro}_{x:A.p(x)} \coloneqq \mathrm{funext}^{-1}(\lambda (x:A).\beta_{A \to B}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{A \to B}^{x:A.b'(x)}(b'(x))^{-1}):(\lambda x:A.b(x)) =_{A \to B} (\lambda x:A.b'(x))$$
\end{proof}

### Application in logic

In [[logic]], functions types express [[implication]]. More precisely, for $\phi, \psi$ two [[propositions]], under [[propositions as types]] the [[implication]] $\phi \Rightarrow \psi$ is the function type $\phi \to \psi$ (or rather the [[bracket type]] of that if one wishes to force this to be of type $Prop$ again ).

### Graph of a function

Given a type $A$ and $B$, there is a function 

$$\mathrm{graph}:\left(A \to B\right) \to \left(A \to A \times B\right)$$

which takes a function $f:A \to B$ and returns the **[[graph of a function]]** 
$$\mathrm{graph}(f):A \to (A \times B)$$ 
defined by $\mathrm{graph}(f)(x) \equiv (x, f(x))$ for all $x:A$. As a [[dependent anafunction]] the graph of the function is represented by the [[identity type]] family

$$x:A, y:B \vdash f(x) =_{B} y$$

and so is equivalently the [[dependent sum type]]

$$\mathrm{graph}(f) \coloneqq \sum_{x:A} \sum_{y:B} f(x) =_{B} y$$

## Related concepts

* [[function application]]

* [[function monad]]

* [[dependent product type]]

* [[equivalence type]], [[embedding type]]

* [[partial function type]]

* [[lambda calculus]]

* [[implication]], [[linear implication]]

* [[extension type]]

## References

A textbook account in the context of [[programming languages]] is in section III of

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_

Another textbook account could be found in section 2.2 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

See also

* [[Richard Garner]], *On the strength of dependent products in the type theory of Martin-L&#246;f*.
 {#GarnerSDP}

[[!redirects function type]]
[[!redirects function types]]

[[!redirects strict function type]]
[[!redirects strict function types]]

[[!redirects weak function type]]
[[!redirects weak function types]]

[[!redirects Russell function type]]
[[!redirects Russell function types]]

[[!redirects strict Russell function type]]
[[!redirects strict Russell function types]]

[[!redirects weak Russell function type]]
[[!redirects weak Russell function types]]

[[!redirects function type a la Russell]]
[[!redirects function types a la Russell]]

[[!redirects strict function type a la Russell]]
[[!redirects strict function types a la Russell]]

[[!redirects weak function type a la Russell]]
[[!redirects weak function types a la Russell]]

[[!redirects Tarski function type]]
[[!redirects Tarski function types]]

[[!redirects strict Tarski function type]]
[[!redirects strict Tarski function types]]

[[!redirects weak Tarski function type]]
[[!redirects weak Tarski function types]]

[[!redirects function type a la Tarski]]
[[!redirects function types a la Tarski]]

[[!redirects strict function type a la Tarski]]
[[!redirects strict function types a la Tarski]]

[[!redirects weak function type a la Tarski]]
[[!redirects weak function types a la Tarski]]