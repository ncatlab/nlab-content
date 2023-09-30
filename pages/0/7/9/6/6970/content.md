
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

### As a special case of the dependent product

In [[dependent type theory]] a function type $A \to B$ is the
special case the [[dependent product]] over $a : A$ for the 
special case that $B$ is regarded as an $A$-[[dependent type]] that
actually happens to be $A$-independent. The rules are given as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}{\Gamma \vdash A \to B \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}{\Gamma \vdash A \to B \equiv \prod_{x:A} B\; \mathrm{type}}$$

In [[categorical semantics]] this is the statement that a [[section]] of a product [[projection]] $A \times B \to A$ is equivalently just a morphism $A \to B$.

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

A function type is the special case of a [[dependent product type]] for the case where the [[dependent type]] does not actually depend.

$$
  (X \to A)
  = 
  \prod_{x \colon X} A
  \,.
$$

See also at _[[function monad]]_.

### Categorical structure of function types 

Function types have a [[category|categorical structure]]: they have [[identity functions]] and [[function composition]] which together satisfy the associative and unital laws:

* For strict function types, the associative and unital laws are represented by judgmental equality

* For weak function types, the associative and unital laws are represented by [[associator]] and [[unitor]] [[homotopies]], and, assuming [[function extensionality]], also by [[associator]] and [[unitor]] [[identifications]]. In addition, there is also an infinite tower of [[coherence laws]] representing the [[(infinity,1)-category|$(\infty,1)$-categorical structure]] of function types by constructing the [[pentagonator]] and so forth, but this isn't demonstrated in this section, and is unnecessary in the presence of a [[set truncation axiom]] like [[UIP]] or [[axiom K]]. 

#### Strict function types

To be done, but for now see section 2.2 of [Rijke 2022](#Rijke22). 

#### Weak function types

Here we assume that dependent function types still use judgmental computation and uniqueness rules, and for constant type families $x:A \vdash B$ the type $\prod_{x:A} B$ still represents strict function types. 

\begin{definition}
Given a type $A$, we define the **identity function** on $A$ as the function

$$\mathrm{id}_A \equiv \lambda (x:A).x:A \to A$$
\end{definition}

\begin{theorem}
By the computation rules for weak function types, the identity function on a type $A$ comes with a dependent function

$$\beta_{A \to A}^{x:A.x}:\prod_{x:A} \mathrm{id}_A(x) =_{A} x$$
\end{theorem}

\begin{definition}
Given types $A$, $B$, and $C$ and functions $f:A \to B$, and $g:B \to C$, **function composition** of $f$ and $g$ is defined as

$$g \circ_{A, B, C} f \equiv \lambda (x:A).g(f(x)):A \to C$$
\end{definition}

\begin{theorem}
By the computation rules for weak function types, function composition comes with a dependent function 

$$\beta_{A \to C}^{x:A.g(f(x))}:\prod_{x:A} (g \circ_{A, B, C} f)(x) =_{C} g(f(x))$$
\end{theorem}

\begin{theorem}
For all types $A$ and $B$ and functions $f:A \to B$, the dependent function type

$$\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$

has a homotopy. 
\end{theorem}

\begin{proof}
By the computation rule for weak function types, there is a homotopy

$$\beta_{A \to B}^{x:A.\mathrm{id}_B(f(x))}:\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} \mathrm{id}_B(f(x))$$

and a homotopy

$$\beta_{B \to B}^{x:A.f(x)}:\prod_{x:A} \mathrm{id}_B(f(x)) =_{B} f(x)$$

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
By the computation rule for weak function types, there is a homotopy

$$\beta_{A \to B}^{x:A.f(\mathrm{id}_A(x))}:\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(\mathrm{id}_A(x))$$

and also by the action on identifications of the function $f:A \to B$, a homotopy

$$\lambda (x:A).\mathrm{ap}_B(f, \mathrm{id}_A(x), x, \beta_{A \to A}^{x:A.x}(x)):\prod_{x:A} f(\mathrm{id}_A(x)) =_{B} f(x)$$

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
By the computation rule for weak function types, there are homotopies

$$\beta_{A \to D}^{x:A.h((g \circ_{A, B, C} f)(x))}:\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} h((g \circ_{A, B, C} f)(x))$$

$$\beta_{A \to D}^{x:A.(h \circ_{B, C, D} g)(f(x))}:\prod_{x:A} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x) =_{D} (h \circ_{B, C, D} g)(f(x))$$

$$\beta_{A \to D}^{x:A.h(g(f(x)))}:\prod_{x:A} (h \circ_{B, C, D} g)(f(x)) =_{D} h(g(f(x)))$$

and also by the action on identifications of the function $h:C \to D$, there is a homotopy

$$\lambda (x:A).\mathrm{ap}_D(h, (g \circ_{A, B, C} f)(x), g(f(x)), \beta_{A \to C}^{x:A.g(f(x))}(x)):\prod_{x:A} h((g \circ_{A, B, C} f)(x)) =_{D} h(g(f(x))$$

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

Now, recall that the happly function 

$$\mathrm{happly}_{A, B}(f, g):f =_{A \to B} g \to \prod_{x:A} f(x) =_{B} g(x)$$

is inductively defined by

$$\mathrm{happly}_{A, B}(f, f)(\mathrm{refl}_{A \to B}(f)) \equiv \lambda (x:A).\mathrm{refl}_{B}(f(x)):\prod_{x:A} f(x) =_{B} g(x)$$

[[function extensionality]] states that $\mathrm{happly}_{A, B}(f, g)$ is an [[equivalence of types]] for all functions $f:A \to B$ and $g:A \to B$

$$\mathrm{funext}_{A, B}:\prod_{f:A \to B} \prod_{g:A \to B} \mathrm{isEquiv}(\mathrm{happly}_{A, B}(f, g))$$

Thus, there is an [[inverse function]] 

$$\mathrm{happly}_{A, B}(f, g)^{-1}:\left(\prod_{x:A} \mathrm{Id}_{B}(f(x), g(x))\right) \to f =_{A \to B} g$$

With function extensionality, we can now prove the associative and unital laws, showing that function are a category:

\begin{theorem}
Assuming function extensionality, for all types $A$ and $B$ and functions $f:A \to B$, the identity type

$$\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$

has an identification.
\end{theorem}

\begin{proof}
By function extensionality, the function 

$$\mathrm{happly}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f):(\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f) \to \prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)$$ 

has an inverse function 

$$\mathrm{happly}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}:\left(\prod_{x:A} (\mathrm{id}_B \circ_{A, B, B} f)(x) =_{B} f(x)\right) \to (\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f)$$

One then gets the identification

$$\mathrm{happly}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}(\mathrm{lunith}_{A, B}(f)):\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **left unitor** as the identification 

$$\mathrm{lunit}_{A, B}(f) \equiv \mathrm{happly}_{A, B}(\mathrm{id}_B \circ_{A, B, B} f, f)^{-1}(\mathrm{lunith}_{A, B}(f)):\mathrm{id}_B \circ_{A, B, B} f =_{A \to B} f$$
\end{definition}

\begin{theorem}
Assuming function extensionality, for all types $A$ and $B$ and functions $f:A \to B$, the identity type

$$f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$

has an identification.
\end{theorem}

\begin{proof}
By function extensionality, the function 

$$\mathrm{happly}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f):(f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f) \to \prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)$$ 

has an inverse function 

$$\mathrm{happly}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}:\left(\prod_{x:A} (f \circ_{A, A, B} \mathrm{id}_A)(x) =_{B} f(x)\right) \to (f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f)$$

One then gets the identification

$$\mathrm{happly}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}(\mathrm{runith}_{A, B}(f)):f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$
\end{proof}

\begin{definition}
For types $A$ and $B$ and function $f:A \to B$, we define the **right unitor** as the identification 

$$\mathrm{runit}_{A, B}(f) \equiv \mathrm{happly}_{A, B}(f \circ_{A, A, B} \mathrm{id}_A, f)^{-1}(\mathrm{runith}_{A, B}(f)):f \circ_{A, A, B} \mathrm{id}_A =_{A \to B} f$$
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
	\mathrm{happly}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f): \\
	(h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f) \\
	\to \prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)
\end{array}
$$ 

has an inverse function 

$$
\begin{array}{c}
	\mathrm{happly}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}: \\
	\left(\prod_{x:A} (h \circ_{A, C, D} (g \circ_{A, B, C} f))(x) =_{D} ((h \circ_{B, C, D} g) \circ_{A, B, D} f)(x)\right) \\
	\to (h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f)
\end{array}
$$ 

One then gets the identification

$$
\begin{array}{c}
	\mathrm{happly}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}(\mathrm{assoch}_{A, B, C, D}(f, g, h)):\\
	h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f
\end{array}
$$
\end{proof}

\begin{definition}
For types $A$, $B$, $C$, and $D$ and functions $f:A \to B$, $f:B \to C$, and $h:C \to D$, we define the **associator** as the identification 

$$
\begin{array}{c}
	\mathrm{assoc}_{A, B, C, D}(f, g, h) \equiv \mathrm{happly}_{A, D}(h \circ_{A, C, D} (g \circ_{A, B, C} f), (h \circ_{B, C, D} g) \circ_{A, B, D} f)^{-1}(\mathrm{assoch}_{A, B, C, D}(f, g, h)):\\
	h \circ_{A, C, D} (g \circ_{A, B, C} f) =_{A \to D} (h \circ_{B, C, D} g) \circ_{A, B, D} f
\end{array}
$$
\end{definition}

### Application in logic

In [[logic]], functions types express [[implication]]. More precisely, for $\phi, \psi$ two [[propositions]], under [[propositions as types]] the [[implication]] $\phi \Rightarrow \psi$ is the function type $\phi \to \psi$ (or rather the [[bracket type]] of that if one wishes to force this to be of type $Prop$ again ).

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