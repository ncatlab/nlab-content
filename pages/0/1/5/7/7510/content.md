
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Dependent product types
* table of contents
{: toc}

## Idea

In [[dependent type theory]], a _dependent product type_ $\prod_{x\colon A} B(x)$, for a [[dependent type]] $x\colon A\vdash B(x)\colon Type$ is the [[type]] of "dependently typed [[functions]]" assigning to each $x\colon A$ an element of $B(x)$.

In a [[model]] of the type theory in [[categorical semantics]], this is a [[dependent product]].  In [[set theory]], it is an element of an indexed product.

It includes [[function types]] as the special case when $B$ is not dependent on $A$, [[product types]] as a special case when $A$ is the type of [[Booleans]], and [[dependent sequence types]] as a special case when $A$ is the [[natural numbers type]]. 

## Overview

[[!include dependent product natural deduction - table]]

## Definition

Like any type constructor in type theory, a dependent product type is specified by rules saying when we can introduce it as a type, how to construct terms of that type, how to use or "eliminate" terms of that type, and how to compute when we combine the constructors with the eliminators.

The [[type formation rule]] for dependent product type is:

$$\frac{A\colon Type \qquad x\colon A \vdash B(x) \colon Type}{\prod_{x\colon A} B(x)\colon Type}$$


### As a negative type

Dependent product types are almost always defined as [[negative types]].  In this presentation, primacy is given to the eliminators.  The natural eliminator of a dependent product type says that we can *apply* it to any input:

$$\frac{f\colon \prod_{x\colon A} B(x) \qquad a\colon A}{f(a) \colon B(a)}$$

The constructor is then determined as usual for a negative type: to construct a term of $\prod_{x\colon A} B(x)$, we have to specify how it behaves when applied to any input.  In other words, we should have a term of type $B(x)$ containing a free variable $x\colon A$.  This yields the usual "$\lambda$-abstraction" constructor:

$$\frac{x\colon A\vdash b\colon B(x)}{\lambda x.b\colon \prod_{x\colon A} B(x)}$$

The [[beta-reduction]] rule is the obvious one, saying that when we evaluate a $\lambda$-abstraction, we do it by substituting for the bound variable.

$$(\lambda x.b)(a) \;\to_\beta\; b[a/x]$$

If we want an [[eta-conversion]] rule, the natural one says that every dependently typed function is a $\lambda$-abstraction:

$$ \lambda x.f(x) \;\to_\eta\; f$$


### As a positive type

It is also possible to present dependent product types as a [[positive type]].  However, this requires a stronger metatheory, such as a [[logical framework]].  We use the same constructor ($\lambda$-abstraction), but now the eliminator says that to define an operation using a function, it suffices to say what to do in the case that that function is a lambda abstraction.

$$\frac{(x\colon A \vdash b\colon B(x)) \vdash c\colon C \qquad f\colon \prod_{x\colon A} B(x)}{funsplit(c,f)\colon C}$$

This rule cannot be formulated in the usual presentation of type theory, since it involves a "higher-order judgment": the context of the term $c\colon C$ involves a "term of type $B(x)$ containing a free variable $x\colon A$".  However, it is possible to make sense of it.  In [[dependent type theory]], we need additionally to allow $C$ to depend on $\prod_{x\colon A} B(x)$.

The natural $\beta$-reduction rule for this eliminator is

$$ funsplit(c, \lambda x.g) \;\to_\beta c[g/b] $$

and its $\eta$-conversion rule looks something like

$$ funsplit(c[\lambda x.b / g], f) \;\to_\eta\; c[f/g]. $$

Here $g\colon \prod_{x\colon A} B(x) \vdash c\colon C$ is a term containing a free variable of type $\prod_{x\colon A} B(x)$.  By substituting $\lambda x.b$ for $g$, we obtain a term of type $C$ which depends on "a term $b\colon B(x)$ containing a free variable $x\colon A$".  We then apply the positive eliminator at $f\colon \prod_{x\colon A} B(x)$, and the $\eta$-rule says that this can be computed by just substituting $f$ for $g$ in $c$.


### Positive versus negative

As usual, the positive and negative formulations are equivalent in a suitable sense.  They have the same constructor, while we can formulate the eliminators in terms of each other:

$$
\begin{aligned}
  f(a) &\coloneqq funsplit(b[a/x], f)\\
  funsplit(c, f) &\coloneqq c[f(x)/b]
\end{aligned}
$$

The conversion rules also correspond.

In dependent type theory, this definition of $funsplit$ only gives us a properly typed dependent eliminator if the negative dependent product type satisfies $\eta$-conversion.  As usual, if it satisfies [propositional eta-conversion](/nlab/show/eta-conversion#Propositional) then we can transport along that instead---and conversely, the dependent eliminator allows us to prove propositional $\eta$-conversion.  This is the content of Propositions 3.5, 3.6, and 3.7 in [(Garner)](#GarnerSDP).

### Dependent product types a la Russell and a la Tarski

In [[dependent type theory]], there are two different ways to interpret the term $f:\prod_{x:A} B(x)$: 

1. $f$ is literally a family of terms in the family of types $B(x)$ indexed by $A$

1. $f$ is a term representation for a family of terms in the family of types $B(x)$ indexed by $A$

This situation is similar to how there are two notions of [[type universe]] where [[small types]] of a universe are interpreted [[Russell universe|a la Russell]], literally as types, or [[Tarski universe|a la Tarski]], as a term representation of types. Thus, in analogy to type universes, we can refer to dependent product types *a la Russell* and function types *a la Tarski*. 

Dependent product types a la Russell and a la Tarski are expressed respectively via the [[elimination rule]] of function types: 

* given type $A$ and the type family $x:A \vdash B(x)$ and an element $f:\prod_{x:A} B(x)$, one could form the family of terms $x:A \vdash f(x):B$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma, x:A \vdash f(x):B(x)}$$

* given type $A$ and the type family $x:A \vdash B(x)$ one could form the family of terms $f:\prod_{x:A} B(x), x:A \vdash \mathrm{eval}(f, x):B(x)$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x), x:A \vdash \mathrm{eval}(f, x):B(x)}$$

Dependent product types a la Tarski corresponds to the notion of [[dependent product]] in [[category theory]] where the dependent product $\Pi(A, B)$ literally comes with a morphism $\mathrm{eval}:\Pi(A, B) \times A \to \Sigma(A, B)$ in the [[slice category]] $C/A$, but dependent product types a la Russell are the one most commonly used in [[dependent type theory]]. 

The conversion rules for dependent product types a la Russell are as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, x:A \vdash (\lambda x:A.b(x))(x) \equiv b(x):B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda x:A.f(x):\prod_{x:A} B(x)}$$

and the conversion rules for dependent product types a la Tarski are as follows: 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, x:A \vdash \mathrm{eval}(\lambda x:A.b(x), x) \equiv b(x):B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x) \vdash f \equiv \lambda x:A.\mathrm{eval}(f, x):\prod_{x:A} B(x)}$$

For the rest of the article we shall assume the use of dependent product types a la Russell. 

### Weak and strict dependent product types

In [[dependent type theory]], **weak dependent product types** are dependent product types for which the [[computation rules]] ($\beta$-conversion) and [[uniqueness rules]] ($\eta$-conversion) are propositional rather than judgmental:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash \beta_{A \to B}^{x:A.b(x)}(a):(\lambda(x:A).b(x))(a) =_{B(x)} b(a)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x) \vdash \eta_{A \to B}(f):f =_{\prod_{x:A} B(x)} \lambda(x:A).f(x)}$$

Weak dependent product types appear in [[weak type theories]]. 

This contrasts with **strict dependent product types** which use judgmental computation and uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma, a:A \vdash (\lambda(x:A).b(x))(a) \equiv b(a):B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:\prod_{x:A} B(x) \vdash f \equiv \lambda(x:A).f(x):\prod_{x:A} B(x)}$$

Strict dependent product types appear in most dependent type theories such as [[Martin-Löf type theory]], [[observational type theory]], and [[cubical type theory]].

For strict dependent product types, the judgmental computation and uniqueness rules automatically imply the propositional computation and uniqueness rules, as by the rules for [[judgmental equality]] and [[identity types]], judgmental equality of two terms always implies propositional equality of the two terms. 

### As types of dependent anafunctions

In the same way that one could define [[equivalence types]] as types of [[one-to-one correspondences]] and [[function types]] as types of [[anafunctions]], one could define dependent function types as types of [[dependent anafunctions]]. This requires both [[identity types]] and [[heterogeneous identity types]] being defined first, which we shall write as $a =_A b$ and $x =_{B}^{p} y$ respectively for $a:A$, $b:A$, $p:a =_A b$, $x:B(a)$, and $y:B(b)$. We use Agda notation $(x:A) \to B(x)$ for dependent function types rather than the dependent product type notation $\prod_{x:A} B(x)$ or $\Pi(x:A).B(x)$ in this section. 

Rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash (x:A) \to B(x) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x) \vdash \mathcal{F}_{A, B}(f, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B(x)}{\Gamma \vdash \lambda x.f(x):(x:A) \to B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B(x)}{\Gamma, x:A \vdash \alpha(x):\mathcal{F}_{A, B}(\lambda x.f(x), x, f(x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A \vdash \mathrm{ev}(f, x):B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A \vdash \beta(f, x):\mathcal{F}_{A, B}(f, x, \mathrm{ev}(f, x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x), u:\mathcal{F}_{A, B}(f, x, y) \vdash \kappa(f, x, y, u):\mathrm{ev}(f, x) =_{B(x)} y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x), u:\mathcal{F}_{A, B}(f, x, y) \vdash \eta(f, x, y, u):\beta(f, x) =_{\mathcal{F}_{A, B}(f, x)}^{\kappa(f, x, y, u)} u}$$

By the rules for [[dependent pair types]] and [[dependent function types]], one could derive that 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x) \vdash \eta(f):(x:A) \to \mathrm{isContr}\left((y:B) \times \mathcal{F}_{A, B}(f, x, y)\right)}$$

which is precisely the statement that $\mathcal{F}_{A, B}(f)$ is a [[dependent anafunction]] for all dependent functions $f:(x:A) \to B(x)$. 

## Properties

### Typal congruence rules

These are called *typal congruence rules* because they are the analogue of the judgmental [[congruence rules]] which use [[identity types]] and [[equivalence types]] instead of [[judgmental equality]]. 

#### Strict dependent product types

Since [[dependent product types]] are negative types, we first present the typal congruence rule for the elimination rule of dependent product types

\begin{theorem}
Given a type $A$ and a type family $x:A \vdash B(x)$, dependent functions $f:\prod_{x:A} B(x)$ and $g:\prod_{x:A} B(x)$ and an identification $p:f =_{\prod_{x:A} B(x)} g$ there are families of identifications $x:A \vdash \mathrm{compelim}(f, g, p)(x):f(x) =_{B(x)} g(x)$. 
\end{theorem}

\begin{proof}
We simply define the dependent function $\mathrm{compelim}$ to be happly, which is inductively defined on [[identity types]]. 
\end{proof}

The next is the typal congruence rule for the introduction rule of dependent function types. However, unlike the case for the other two rules, one needs dependent function extensionality. 

\begin{theorem}
Assuming dependent [[function extensionality]], given type $A$ and family of types $x:A \vdash B(x)$, families of elements $x:A \vdash b(x):B(x)$ and $x:A \vdash b'(x):B(x)$, and families of [[identifications]] $x:A \vdash p(x):b(x) =_{B(x)} b'(x)$, there is a identification 
$$\mathrm{congintro}_{x:A.p(x)}:\lambda (x:A).b(x) =_{\prod_{x:A} B(x)} \lambda (x:A).b'(x)$$
\end{theorem}

\begin{proof}
By the computation rule of strict function types, there are families of judgmental equalities 

$$x:A \vdash ((\lambda x:A.b(x))(x) \equiv b(x):B(x)$$
$$x:A \vdash ((\lambda x:A.b'(x))(x) \equiv b'(x):B(x)$$

Thus, by the [[structural rules]] of [[judgmental equality]], there are families of identifications 

$$x:A \vdash p(x):(\lambda x:A.b(x))(x) =_{B(x)} (\lambda x:A.b'(x))(x)$$

and by $\lambda$-abstraction, one gets the dependent function

$$\lambda (x:A).p(x):\prod_{x:A} (\lambda x:A.b(x))(x) =_{B(x)} (\lambda x:A.b'(x))(x)$$

By dependent [[function extensionality]], there is an [[equivalence of types]]

$$\mathrm{funext}:(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x)) \simeq \prod_{x:A} (\lambda x:A.b(x))(x) =_{B(x)} (\lambda x:A.b'(x))(x)$$

which yields an identification 

$$\mathrm{funext}^{-1}(\lambda (x:A).p(x)):(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x))$$

We define 

$$\mathrm{congintro}_{x:A.p(x)} \coloneqq \mathrm{funext}^{-1}(\lambda (x:A).p(x)):(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x))$$
\end{proof}

Finally, we present the typal congruence rule for the formation rule of function types, which relies upon the previous two results. 

\begin{theorem}
Given types $A$ and $A'$ and type families $x:A \vdash B(x)$, $x:A' \vdash B'(x)$ and equivalence $e_A:A \simeq A'$ and dependent function $e_B:\prod_{x:A} B(x) \simeq B'(e_A(x))$, there is an equivalence 
$$\mathrm{congform}(e_A, e_B):\left(\prod_{x:A} B(x)\right) \simeq \left(\prod_{x:A'} B'(x)\right)$$
\end{theorem}

\begin{proof}
We define the function 
$$\mathrm{congform}(e_A, e_B):\left(\prod_{x:A} B(x)\right) \to \left(\prod_{x:A'} B'(x)\right)$$ 
by 
$$\mathrm{congform}(e_A, e_B) \coloneqq \lambda (f:\prod_{x:A} B(x)).\lambda x:A'.\mathrm{transport}_{x:A'.B'(x)}(e_A(e_A^{-1}(x)), x, \mathrm{sec}_{e_A}(x), e_B(e_A^{-1}(x))(f(e_A^{-1}(x))))$$

and the inverse function by

$$\mathrm{congform}(e_A, e_B)^{-1} \coloneqq \lambda (f:\prod_{x:A'} B'(x)).\lambda x:A.e_B(x)^{-1}(f(e_A(x)))$$

where the equivalence $e_A:A \simeq A'$ has families of identifications
$$x':A \vdash \mathrm{sec}_{e_A}(x):e_A(e_A^{-1}(x)) =_{A'} x$$
$$x:A \vdash \mathrm{ret}_{e_A}:e_A^{-1}(e_A(x)) =_A x$$
witnessing that $e_A^{-1}$ is a [[section]] and [[retraction]] of $e_A$ respectively.  

Now it suffices to construct homotopies 

$$\prod_{f:\prod_{x:A} B(x)} \mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) =_{\prod_{x:A} B(x)} f$$

$$\prod_{g:\prod_{x:A'} B'(x)} \mathrm{congform}(e_A, e_B)(\mathrm{congform}(e_A, e_B)^{-1}(g)) =_{\prod_{x:A'} B'(x)} g$$

from where it implies that $\mathrm{congform}(e_A, e_B)$ has a coherent inverse and contractible fibers and is thus an [[equivalence of types]]. 

By definition, 
$$\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) \equiv \lambda x:A.e_B(x)^{-1}((\lambda x:A'.\mathrm{transport}_{x:A'.B'(x)}(e_A(e_A^{-1}(x)), x, \mathrm{sec}_{e_A}(x), e_{B'}(e_A^{-1}(x))(f(e_A^{-1}(x)))))(e_A(x)))$$

By the computation rules of strict function types, there is a family of judgmental equalities
$$x:A \vdash (\lambda x:A'.\mathrm{transport}_{x:A'.B'(x)}(e_A(e_A^{-1}(x)), x, \mathrm{sec}_{e_A}(x), e_B(e_A^{-1}(x))(f(e_A^{-1}(x)))))(e_A(x)) \equiv \mathrm{transport}_{x:A'.B'(x)}(e_A(e_A^{-1}(e_A(x))), e_A(x), \mathrm{sec}_{e_A}(e_A(x)), e_B(e_A^{-1}(x))(f(e_A^{-1}(e_A(x)))))$$
and thus by the structural rules of [[judgmental equalities]] and the judgmental congruence rules for function types, a judgmental equality
$$\mathrm{congform}(e_A, e_B)^{-1}(\mathrm{congform}(e_A, e_B)(f)) \equiv \lambda x:A.e_B(x)^{-1}(\mathrm{transport}_{x:A'.B'(x)}(e_A(e_A^{-1}(e_A(x))), e_A(x), \mathrm{sec}_{e_A}(e_A(x)), e_B(e_A^{-1}(e_A(x)))(f(e_A^{-1}(e_A(x))))))$$
\end{proof}

#### Weak dependent product types

\begin{theorem}
Assuming dependent function extensionality, given types $A$ and $A'$ and type families $x:A \vdash B(x)$ and $x:A \vdash B'(x)$ and equivalences $e_A:A \simeq A'$ and dependent function of equivalences $e_B:\prod_{x:A} B(x) \simeq B'(e(x))$, there is an equivalence 
$$\mathrm{congform}(e_A, e_B):\left(\prod_{x:A} B(x)\right) \simeq \left(\prod_{x:A'} B'(x)\right)$$
\end{theorem}

Since [[dependent function types]] are negative types, we first present the typal congruence rule for the elimination rule of dependent function types

\begin{theorem}
Given a type $A$ and a type family $x:A \vdash B(x)$, dependent functions $f:\prod_{x:A} B(x)$ and $g:\prod_{x:A} B(x)$ and an identification $p:f =_{\prod_{x:A} B(x)} g$ there are families of identifications $x:A \vdash \mathrm{compelim}(f, g, p)(x):f(x) =_{B(x)} g(x)$. 
\end{theorem}

\begin{proof}
We simply define the dependent function $\mathrm{compelim}$ to be happly, which is inductively defined on [[identity types]]. 
\end{proof}

The next is the typal congruence rule for the uniqueness rule of dependent function types.

\begin{theorem}
For weak dependent product types with dependent function
$$\eta:\prod_{f:\prod_{x:A} B(x)} f =_{\prod_{x:A} B(x)} \lambda x:A.f(x)$$

given 

* a type $A$

* a type family $x:A \vdash B(x)$ 

* dependent functions $f:\prod_{x:A} B(x)$ and $f':\prod_{x:A} B(x)$

* an identification $p:f =_{\prod_{x:A} B(x)} f'$, 

there is a family of identifications 

$$\mathrm{etaCong}_{\prod}(f, f', p):\mathrm{transport}(f, f', p)(\eta_{\prod_{x:A} B(x)}(f)) =_{f =_{\prod_{x:A} B(x)} \lambda x:A.f(x)} \eta_{\prod_{x:A} B(x)}(f')$$
\end{theorem}

\begin{proof}
We simply define $\mathrm{etaCong}_{\prod}(f, f', p)$ to be the [[dependent function application to identifications]] $\mathrm{apd}(\eta, f, f' p)$. 
\end{proof}

The next is the typal congruence rule for the introduction rule of function types. However, unlike the case for the other two rules, one needs dependent function extensionality. 

\begin{theorem}
Assuming dependent function extensionality, given a type $A$ and a type family $x:A \vdash B(x)$, families of elements $x:A \vdash b(x):B(x)$ and $x:A \vdash b'(x):B(x)$, and families of [[identifications]] $x:A \vdash p(x):b(x) =_{B(x)} b'(x)$, there is an identification 
$$\mathrm{congintro}_{x:A.p(x)}:\lambda (x:A).b(x) =_{\prod_{x:A} B(x)} \lambda (x:A).b'(x)$$
\end{theorem}

\begin{proof}
By the computation rule of weak dependent function types, there are families of identifications 

$$x:A \vdash \beta_{\prod_{x:A} B(x)}^{x:A.b(x)}(b(x)):((\lambda x:A.b(x))(x) =_{B(x)} b(x)$$
$$x:A \vdash \beta_{\prod_{x:A} B(x)}^{x:A.b'(x)}(b'(x)):((\lambda x:A.b'(x))(x) =_{B(x)} b'(x)$$

Thus, there are families of identificaitons 

$$x:A \vdash \beta_{\prod_{x:A} B(x)}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{\prod_{x:A} B(x)}^{x:A.b'(x)}(b'(x))^{-1}:(\lambda x:A.b(x))(x) =_{B(x)} (\lambda x:A.b'(x))(x)$$

and by $\lambda$-abstraction, one gets the dependent function

$$\lambda (x:A).\beta_{\prod_{x:A} B(x)}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{\prod_{x:A} B(x)}^{x:A.b'(x)}(b'(x))^{-1}:(\lambda x:A.b(x))(x) =_{B(x)} (\lambda x:A.b'(x))(x)$$

By dependent function extensionality, there is an [[equivalence of types]]

$$\mathrm{funext}:(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x)) \simeq \prod_{x:A} \mathrm{Id}_{B(x)}((\lambda x:A.b(x))(x), (\lambda x:A.b'(x))(x))$$

which yields an identification 

$$\mathrm{funext}^{-1}(\lambda (x:A).\beta_{\prod_{x:A} B(x)}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{\prod_{x:A} B(x)}^{x:A.b'(x)}(b'(x))^{-1}):(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x))$$

We define 

$$\mathrm{congintro}_{x:A.p(x)} \coloneqq \mathrm{funext}^{-1}(\lambda (x:A).\beta_{\prod_{x:A} B(x)}^{x:A.b(x)}(b(x)) \bullet p(x) \bullet \beta_{\prod_{x:A} B(x)}^{x:A.b'(x)}(b'(x))^{-1}):(\lambda x:A.b(x)) =_{\prod_{x:A} B(x)} (\lambda x:A.b'(x))$$
\end{proof}

### Application in logic

In [[logic]], dependent functions types express [[universal quantifications]]. More precisely, for $x:A \vdash \phi(x)$ a [[predicate]] on a type $A$, under [[propositions as types]] the [[universal quantification]] $\forall x:A.\phi(x)$ is the dependent product type $\prod_{x:A} \phi(x)$ (or rather the [[bracket type]] of that if one wishes to force this to be of type $Prop$ again ).

### Graph of a dependent function

Given a type $A$ and a type family $x:A \vdash B(x)$, there is a function 

$$\mathrm{graph}:\left(\prod_{x:A} B(x)\right) \to \left(A \to \sum_{x:A} B(x)\right)$$

which takes a dependent function $f:\prod_{x:A} B(x)$ and returns the **[[graph of a function|graph of a dependent function]]** 
$$\mathrm{graph}(f):A \to \sum_{x:A} B(x)$$ 
defined by $\mathrm{graph}(f)(x) \equiv (x, f(x))$ for all $x:A$. As a [[dependent anafunction]] the graph of the dependent function is represented by the [[identity type]] family

$$x:A, y:B(x) \vdash f(x) =_{B(x)} y$$

## Related concepts

* [[dependent product]]
* [[dependent sum type]]
* [[function type]]
* [[dependent sequence type]]
* [[dependent extension type]]

## References

The standard rules for type-formation, term introduction/elimination and computation of dependent product type are listed for instance in [part I](http://www.math.unipa.it/~ngambino/Research/Lectures/lecture1.pdf)  of

* [[Nicola Gambino]], _Lectures on dependent type theory_ ([pdf](http://www.cs.le.ac.uk/events/mgs2009/courses/gambino/lecturenotes-gambino.pdf))

Another textbook account could be found in section 2.1 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

See also:

* {#GarnerSDP} [[Richard Garner]], *On the strength of dependent products in the type theory of Martin-L&#246;f*, [arXiv](http://arxiv.org/abs/0803.4466).
  
On the [[categorical semantics]] of [[dependent product types]] as *[[relative adjoint functor|relative]]* [[right adjoints]] to [[context extension]] in [[comprehension categories]]:

* [[Michael Lindgren]], *Dependent products as relative adjoints*, Stockholm (2021) &lbrack;[[Lindgren-DependentProductsAsRelativeAdjoints.pdf:file]]&rbrack;


[[!redirects dependent product type]]
[[!redirects dependent product types]]
[[!redirects dependent function type]]
[[!redirects dependent function types]]
[[!redirects Pi-type]]
[[!redirects Pi-types]]
[[!redirects Pi type]]
[[!redirects Pi types]]
[[!redirects Π-type]]
[[!redirects Π-types]]
[[!redirects Π type]]
[[!redirects Π types]]

[[!redirects Russell dependent product type]]
[[!redirects Russell dependent product types]]
[[!redirects Russell dependent function type]]
[[!redirects Russell dependent function types]]
[[!redirects Russell Pi-type]]
[[!redirects Russell Pi-types]]
[[!redirects Russell Pi type]]
[[!redirects Russell Pi types]]
[[!redirects Russell Π-type]]
[[!redirects Russell Π-types]]
[[!redirects Russell Π type]]
[[!redirects Russell Π types]]

[[!redirects dependent product type a la Russell]]
[[!redirects dependent product types a la Russell]]
[[!redirects dependent function type a la Russell]]
[[!redirects dependent function types a la Russell]]
[[!redirects Pi-type a la Russell]]
[[!redirects Pi-types a la Russell]]
[[!redirects Pi type a la Russell]]
[[!redirects Pi types a la Russell]]
[[!redirects Π-type a la Russell]]
[[!redirects Π-types a la Russell]]
[[!redirects Π type a la Russell]]
[[!redirects Π types a la Russell]]

[[!redirects Tarski dependent product type]]
[[!redirects Tarski dependent product types]]
[[!redirects Tarski dependent function type]]
[[!redirects Tarski dependent function types]]
[[!redirects Tarski Pi-type]]
[[!redirects Tarski Pi-types]]
[[!redirects Tarski Pi type]]
[[!redirects Tarski Pi types]]
[[!redirects Tarski Π-type]]
[[!redirects Tarski Π-types]]
[[!redirects Tarski Π type]]
[[!redirects Tarski Π types]]

[[!redirects dependent product type a la Tarski]]
[[!redirects dependent product types a la Tarski]]
[[!redirects dependent function type a la Tarski]]
[[!redirects dependent function types a la Tarski]]
[[!redirects Pi-type a la Tarski]]
[[!redirects Pi-types a la Tarski]]
[[!redirects Pi type a la Tarski]]
[[!redirects Pi types a la Tarski]]
[[!redirects Π-type a la Tarski]]
[[!redirects Π-types a la Tarski]]
[[!redirects Π type a la Tarski]]
[[!redirects Π types a la Tarski]]