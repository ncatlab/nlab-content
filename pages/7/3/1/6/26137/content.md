
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea 

A form of [[equality]] which allows for elements of [[families]] of [[types]] to be compared for equality. 

## Definition 

### Typal heterogeneous equality

In the [[type theory]] literature, there are different kinds of [[types]] which are called *heterogeneous equality* types:

* *[[heterogeneous identity types]]* are a variant of [[identity types]] but parameterized over pairs of possibly different types,

* *[[fibered heterogeneous identity types]]* are the [[dependent sum]] of heterogeneous identity types over all relevant [[identifications]]. 

### Propositional heterogeneous equality

In any two-layer type theory with a layer of [[types]] and a layer of [[propositions]], or equivalently a [[first order logic]] over [[type theory]] or a [[first-order theory]], every type $A$ has a binary [[relation]] called [[propositional equality]], according to which two elements $x$ and $y$ of $A$ are related if and only if they are equal; in this case we write $x =_A y$. Similarly, every type family $B(x)$ indexed by $x:A$ has a family of binary relations, according to which, given two elements $x$ and $y$ of $A$ where $x =_A y$, and two elements $a$ of $B(x)$ and $b$ of $B(y)$, $a$ and $b$ are related if and only if they are equal across the equality $x =_A y$. Since relations are propositions in the context of a term variable judgment in the type layer, this is called **[[propositional heterogeneous equality]]** or **[[heterogeneous propositional equality]]**. The formation and introduction rules for propositional heterogeneous equality is as follows

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, y:A, x =_A y \; \mathrm{true}, a:B(x), b:B(y) \vdash a =_{\underline{ }.B}^{x =_A y} b \; \mathrm{prop}} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, a:B(x) \vdash a =_{\underline{ }.B}^{x =_A x} a \; \mathrm{true}}$$

Then we have the elimination rules for propositional heterogeneous equality:

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\ 
\Gamma, x:A, y:A, x =_A y \; \mathrm{true}, a:B(x), b:B(y), a =_{\underline{ }.B}^{x =_A y} b \; \mathrm{true} \vdash P(a, b, x, y) \; \mathrm{prop} \\ 
\Gamma, x:A, a:B(x), \vdash P(x, x, a, a) \; \mathrm{true}
\end{array}
}{\Gamma, x:A, y:A, x =_A y \; \mathrm{true}, a:B(x), b:B(y), a =_{\underline{ }.B}^{x =_A y} b \; \mathrm{true} \vdash P(a, b, x, y) \; \mathrm{true}}$$

## Properties

### Heterogeneous equalities are equivalence relations

The introduction rule of heterogeneous equality says that heterogeneous equality is reflexive. 

We can show that heterogeneous equality is symmetric, that for all $x:A$ and $y:A$ such that $x =_A y$, and for all $a:B(x)$ and $b:B(y)$ such that $a =_{\underline{ }.B}^{x =_A y} b$, we have $b =_{\underline{ }.B}^{y =_A x} a$. Non-heterogeneous equality is symmetric, which means that for all $x:A$ and $y:A$ such that $x =_A y$, $y =_A x$. By the introduction rule, we have that for all $x:A$ and $a:B(x)$, we have that $a =_{\underline{ }.B}^{x =_A x} a$, and because all propositions imply themselves, we have that $a =_{\underline{ }.B}^{x =_A x} a$ implies $a =_{\underline{ }.B}^{x =_A x} a$. Thus, by the elimination rules for heterogeneous equality, for all $x:A$ and $y:A$ such that $x =_A y$, and for all $a:B(x)$ and $b:B(y)$ such that $a =_{\underline{ }.B}^{x =_A y} b$, we have $b =_{\underline{ }.B}^{y =_A x} a$. 

We can also show that heterogeneous equality is transitive, that for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$ and $y =_A z$, and for all $a:B(x)$, $b:B(y)$, and $c:B(z)$ such that $a =_{\underline{ }.B}^{x =_A y} b$, $b =_{\underline{ }.B}^{y =_A y} c$ implies $a =_{\underline{ }.B}^{x =_A z} c$. Non-heterogeneous equality is transitive, that for all $x:A$, $y:A$, and $z:A$ such that $x =_A y$ and $y =_A z$, $x =_A z$. By the introduction rule, we have that for all $x:A$ and $a:B(x)$, we have that $a =_{\underline{ }.B}^{x =_A x} a$, and because all propositions imply themselves, we have that $a =_{\underline{ }.B}^{x =_A z} c$ implies $a =_{\underline{ }.B}^{x =_A z} c$, and because true propositions imply true propositions, we have that $a =_{\underline{ }.B}^{x =_A x} a$ implies that $a =_{\underline{ }.B}^{x =_A z} c$ implies $a =_{\underline{ }.B}^{x =_A z} c$. Thus, by the elimination rules for heterogeneous equality, or all $x:A$, $y:A$, and $z:A$ such that $x =_A y$ and $y =_A z$, and for all $a:B(x)$, $b:B(y)$, and $c:B(z)$ such that $a =_{\underline{ }.B}^{x =_A y} b$, $b =_{\underline{ }.B}^{y =_A y} c$ implies $a =_{\underline{ }.B}^{x =_A z} c$. 

Thus, heterogeneous equality is an equivalence relation. 

### Dependent functions are extensional

For all dependent function $f:\prod_{x:A} B(x)$ and elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{\underline{ }.B}^{x =_A y} f(y)$:

$$\forall f:\prod_{x:A} B(x).\forall x:A.\forall y:A.x =_A y \implies f(x) =_{\underline{ }.B}^{x =_A y} f(y)$$

This is because for all dependent function $f:\prod_{x:A} B(x)$, by the introduction rule for heterogeneous equality, for all elements $x:A$, $f(x) =_{\underline{ }.B}^{x =_A x} f(x)$, and the elimination rule for heterogeneous equality states that if for all elements $x:A$, $f(x) =_{\underline{ }.B}^{x =_A x} f(x)$, then for all elements $x:A$ and $y:A$ such that $x =_A y$, $f(x) =_{\underline{ }.B}^{x =_A y} f(y)$. 

### Dependent function extensionality

The extensionality principle for [[dependent product types]] (dependent [[function extensionality]]) states that for all dependent functions $f:\prod_{x:A} B(x)$ and $g:\prod_{x:A} B(x)$, $f =_{\prod_{x:A} B(x)} g$ if and only if for all $a:A$ and $b:A$ such that $a =_A b$, $f(a) =_{\underline{ }.B}^{a =_A b} g(b)$

$$\forall f:\prod_{x:A} B(x).\forall g:\prod_{x:A} B(x).f =_{\prod_{x:A} B(x)} g \iff \forall a:A. \forall b:A.a =_A b \implies (f(a) =_{\underline{ }.B}^{a =_A b} g(b))$$

### Relation to non-heterogeneous propositional equality

Given elements $x:A$, and for all $a:B(x)$ and $b:B(x)$, $a =_{\underline{ }.B}^{x =_A x} b$ if and only if $a =_{B(x)} b$

$$\forall a:B(x).\forall b:B(x). a =_{\underline{ }.B}^{x =_A x} b \iff a =_{B(x)} b$$

This is because by the introduction rules of propositional equality and heterogeneous propositional equality, we have that for all $a:B(x)$, $a =_{B(x)} a$ and $a =_{\underline{ }.B}^{x =_A x} a$, and since true propositions imply true propositions, we have $a =_{B(x)} a$ implies $a =_{\underline{ }.B}^{x =_A x} a$ and $a =_{\underline{ }.B}^{x =_A x} a$ implies $a =_{B(x)} a$. By the elimination rules for propositional equality, for all $a:B(x)$ and $b:B(x)$, we have $a =_{B(x)} b$ implies $a =_{\underline{ }.B}^{x =_A x} b$, and by the elimination rules for heterogeneous propositional equality, we have $a =_{\underline{ }.B}^{x =_A x} b$ implies $a =_{B(x)} b$. Thus, $a =_{\underline{ }.B}^{x =_A x} b$ if and only if $a =_{B(x)} b$. 

### Transport functions

The analogue of [[identity functions]] on a type $A$, a function $f:A \to A$ such that $x =_A f(x)$ for all elements $x:A$, is the notion of [[transport functions]] between a family of types $B(x)$ indexed by elements $x:A$. 

Given elements $x:A$ and $y:A$ such that $x =_A y$, a [[transport function]] is a function $f:B(x) \to B(y)$ such that for all $a:B(x)$, $a =_{\underline{ }.B}^{x =_A y} f(a)$

$$\forall a:B(x).a =_{\underline{ }.B}^{x =_A y} f(a)$$

These transport functions, if they exist, are [[uniqueness quantifier|unique up to equality]]. Suppose we have a second function $g:B(x) \to B(y)$ such that $x =_A y$ implies that for all $a:B(x)$, $a =_{\underline{ }.B}^{x =_A y} g(a)$. Then by symmetry and transitivity of heterogeneous equality, we have $f(a) =_{\underline{ }.B}^{y =_A y} g(a)$, which is logically equivalent to $f(a) =_{B(y)} g(a)$. Then by function extensionality, we have $f =_{B(x) \to B(y)} g$, which implies that transport functions, if they exist, are unique up to equality. 

Suppose that for all elements $x:A$ and $y:A$ such that $x =_A y$, there exists a transport function $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \to B(y)$. Then for all $a:B(x)$ and $b:B(y)$, $a =_{\underline{ }.B}^{x =_A y} b$ if and only if $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a) =_{B(y)} b$

$$\forall a:B(x).\forall b:B(y). a =_{\underline{ }.B}^{x =_A y} b \iff \mathrm{tr}_{\underline{ }.B}^{x =_A y}(a) =_{B(y)} b$$

In particular, this means that we have $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b) =_{B(x)} a$, and by the fact that functions preserve equality, $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)) =_{B(x)} \mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)$, which by transitivity of propositional equality implies that $\mathrm{tr}_{\underline{ }.B}^{y =_A x}(\mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)) =_{B(x)} a$. Similarly, we have $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)) =_{B(y)} \mathrm{tr}_{\underline{ }.B}^{x =_A y}(a)$, which by transitivity of propositional equality implies that $\mathrm{tr}_{\underline{ }.B}^{x =_A y}(\mathrm{tr}_{\underline{ }.B}^{y =_A x}(b)) =_{B(y)} b$. Thus, the transport functions $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \to B(y)$ and $\mathrm{tr}_{\underline{ }.B}^{y =_A x}:B(y) \to B(x)$ are [[inverse functions]] of each other, and thus both transport functions are [[bijections]], and could be written as $\mathrm{tr}_{\underline{ }.B}^{x =_A y}:B(x) \cong B(y)$ and $\mathrm{tr}_{\underline{ }.B}^{y =_A x}:B(y) \cong B(x)$ respectively. 

## Related concepts

* [[equality]]

[[!redirects heterogeneous equality]]
[[!redirects heterogeneous equalities]]

[[!redirects heterogeneous propositional equality]]
[[!redirects heterogeneous propositional equalities]]

[[!redirects heterogeneous typal equality]]
[[!redirects heterogeneous typal equalities]]

[[!redirects propositional heterogeneous equality]]
[[!redirects propositional heterogeneous equalities]]

[[!redirects typal heterogeneous equality]]
[[!redirects typal heterogeneous equalities]]
