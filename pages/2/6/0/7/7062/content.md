
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _interval type_ is an [[axiom|axiomatization]] of the cellular [[interval object]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the interval is given by

    Inductive Interval : Type
      | left : Interval
      | right : Interval
      | segment : Id Interval left right

This says that the type is inductive constructed from two [[terms]] in the interval, whose [[semantics|interpretation]] is as the endpoints of the interval, together with a term in the [[identity type]] of paths between these two terms, which interprets as the 1-cell of the interval

$$
  left \stackrel{segment}{\to} right
  \,.
$$

### Induction principle

The [[induction principle]] for the interval $I$ says that for any $P:I\to Type$ equipped with point $left' : P(left)$ and $right' : P(right)$ and a [[dependent identification]] $segment':left'=_P^{segment} right'$, there is $f:\prod_{(x:I)} P(x)$ such that:

$$f(left)=left' \qquad f(right)=right' \qquad apd_f(segment) = segment'$$

and for every $y:I \vdash g:\prod_{(x:I)} P(x)$ such that 

$$y:I \vdash g(y)(left)=left' \qquad y:I \vdash g(y)(right)=right' \qquad y:I \vdash apd_{g(y)}(segment) = segment'$$

there is an identification $y:I \vdash f = g(y)$. 

As a special case, its [[recursion principle]] says that given any type $I$ with points $x:X$ and $y:X$ and an identification $p:x=y$, there is $f:I \to X$ with 

$$f(left)=x\qquad f(right)=y\qquad ap_f(segment)=p$$

### Syntax

The interval type is defined by the following rules:

Formation rules for the interval type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{I} \; \mathrm{type}}$$

Introduction rules for the interval type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{I}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{I}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash p:0 =_\mathbb{I} 1}$$

Elimination rules for the interval type:
$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma, x:\mathbb{I} \vdash \mathrm{ind}_\mathbb{I}^C(c_0, c_1, c_p)(x):C(x)}$$

Computation rules for the interval type:

* judgmental computational rules
$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p)(0) \equiv c_0:C(0)}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p)(1) \equiv c_1:C(1)}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \mathrm{apd}_C(\mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p), 0, 1, p) \equiv c_p:c_0 =_C^p c_1}$$

* propositional computation rules
$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \beta_\mathbb{I}^{0}(c_0, c_1, c_p): \mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p)(0) =_{C(0)} c_0}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \beta_\mathbb{I}^{1}(c_0, c_1, c_p):\mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p)(1) =_{C(1)} c_1}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \beta_\mathbb{I}^{p}(c_0, c_1, c_p):\mathrm{apd}_C(\mathrm{ind}_\mathbb{I}^{C}(c_0, c_1, c_p), 0, 1, p) =_{c_0 =_C^p c_1} c_p}$$

Uniqueness rules for the interval type:
$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma, x:\mathbb{I} \vdash c:C(x)}{\Gamma, x:\mathbb{I} \vdash \eta_\mathbb{I}(c):c =_{C(x)} \mathrm{ind}_\mathbb{I}^{C}(c(0), c(1), \mathrm{apd}_C(p, c))}$$

The elimination rules and the propositional computation and uniqueness rules for the interval type state that the interval type satisfy the **dependent universal property of the interval type**. If the dependent type theory also has [[dependent sum types]] and [[product types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of the interval type could be simplified to the following rule:

$$\frac{\Gamma, x:\mathbb{I} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_1:C(1) \quad \Gamma \vdash c_p:c_0 =_C^p c_1}{\Gamma \vdash \mathrm{up}_\mathbb{I}^C(c_0, c_1, c_p):\exists!c:\prod_{x:\mathbb{I}} C(x).(c(0) =_{C(0)} c_0) \times (c(1) =_{C(1)} c_1) \times (\mathrm{apd}_{x:\mathbb{I}.C(x)}(c, c_0, c_1, c_p) =_{c_0 =_C^p c_1} c_p)}$$

In type theories with a separate type judgment where not all types are elements of universes, one has to additionally add the following elimination and computation rules:

Elimination rules:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma, x:\mathrm{I} \vdash \mathrm{typerec}_{\mathbb{I}}^{A, B}(e, i) \; \mathrm{type}}$$

Computation rules:

* judgmental computation rules
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{typerec}_{\mathbb{I}}^{A, B}(e, 0) \equiv A \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{typerec}_{\mathbb{I}}^{A, B}(e, 1) \equiv B \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{transport}_{\mathrm{typerec}_{\mathbb{I}}^{A, B}(e)}(0, 1, p_\mathbb{I}) \equiv e:A \simeq B}$$

* typal computation rules
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \beta_{\mathrm{I}}^{0, A, B}(e):\mathrm{typerec}_{\mathbb{I}}^{A, B}(e, 0) \simeq A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \beta_{\mathrm{I}}^{1, A, B}(e):\mathrm{typerec}_{\mathbb{I}}^{A, B}(e, 1) \simeq B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \beta_{\mathrm{I}}^{p_\mathrm{I}, A, B}(e):\beta_{\mathrm{I}}^{1, A, B}(e) \circ \mathrm{transport}_{\mathrm{typerec}_{\mathbb{I}}^{A, B}(e)}(0, 1, p_\mathbb{I}) \circ \beta_{\mathrm{I}}^{0, A, B}(e)^{-1} =_{A \simeq B} e}$$

### Using a function from the type of booleans

The interval type is defined by the following rules:

Formation rules for the interval type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{I} \; \mathrm{type}}$$

Introduction rules for the interval type:
$$\frac{\Gamma \vdash a:\mathbb{2}}{\Gamma \vdash j(a):\mathbb{I}} \qquad \frac{\Gamma \vdash 0:\mathbb{2} \quad \Gamma \vdash 1:\mathbb{2}}{\Gamma \vdash p:j(0) =_\mathbb{I} j(1)}$$

Elimination rules for the interval type:
$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma, a:\mathbb{2} \vdash c:C[j(a)/x] \quad \Gamma \vdash 0:\mathbb{2} \quad \Gamma \vdash 1:\mathbb{2} \quad \Gamma \vdash c_p:c[j(0)/x] =_C^p c[j(1)/x]}{\Gamma, x:\mathbb{I}, a:\mathbb{2} \vdash \mathrm{ind}_\mathbb{I}^C(c[j(a)/x], c_p):C}$$

Computation rules for the interval type:
$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma, a:\mathbb{2} \vdash c:C[j(a)/x] \quad \Gamma \vdash 0:\mathbb{2} \quad \Gamma \vdash 1:\mathbb{2} \quad \Gamma \vdash c_p:c[j(0)/x] =_C^p c[j(1)/x]}{\Gamma, a:\mathbb{2} \vdash \beta_\mathbb{I}^{j}:\mathrm{ind}_\mathbb{I}^{C}(c[j(a)/x], c_p)[j(a)/x] =_{C[j(a)/x]} c[j(a)/x]}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma, a:\mathbb{2} \vdash c:C[j(a)/x] \quad \Gamma \vdash 0:\mathbb{2} \quad \Gamma \vdash 1:\mathbb{2} \quad \Gamma \vdash c_p:c[j(0)/x] =_C^p c[j(1)/x]}{\Gamma, a:\mathbb{2}, \vdash \beta_\mathbb{I}^{p}:\mathrm{apd}_C^p(\mathrm{ind}_\mathbb{I}^{C}(c[j(a)/x], c_p)) =_{c[j(0)/x] =_C^p c[j(1)/x]} c_p}$$

Uniqueness rules for the interval type:

...

## Properties

* An interval type is provably [[contractible type|contractible]].  Conversely, any contractible type satisfies the rules of an interval type up to [[typal equality]].

* An interval type is a [[suspension type]] of the [[unit type]], and the suspension of an interval type is a 2-[[globe]] type. 

* An interval type is a [[cone type]] of the unit type.

* An interval type is a [[cubical type]] $\Box^1$. 

### Induction principle without heterogeneous identifications

There is a version of the induction principle which uses a type $C$ and a function $f:C \to \mathbb{I}$ instead of a type family $P(x)$ indexed by $x:\mathbb{I}$. It has the benefit of not requiring that one has first defined [[heterogeneous identification types]], whether as an [[inductive family]] of types or by using [[transport]]. 

The induction principle of the interval type says that given a type $C$ and a function $f:C \to \mathbb{I}$, as well as 

* elements $c_0:C$ and $c_1:C$

* identifications $c_p:c_0 =_C c_1$, $q_0:f(c_0) =_\mathbb{I} 0$ and $q_1:f(c_q) =_\mathbb{I} 1$ such that $\mathrm{ap}_f(c_p)$, $q_0$, $q_1$, and $p$ form a square


$$
\begin{array}{c}
    & f(c_0) & \overset{\mathrm{ap}_{f}(c_p)}= & f(c_1) &  \\
    q_0 & \Vert &  & \Vert & q_1\\
    & 0 & \underset{p}= & 1 & \\
\end{array}
$$

* an identification saying that the square commutes

$$q_p:\mathrm{ap}_f(c_p) \bullet q_1 =_{f(c_0) =_\mathbb{I} f(c_1)} q_0 \bullet p$$

one can construct 

* a function 

$$g:\mathbb{I} \to C$$

* a homotopy witnessing that $g$ is a [[section]] of $f$:

$$\mathrm{sec}_g:\prod_{x:\mathbb{I}} f(g(x)) =_\mathbb{I} x$$

such that 

$$g(0) \equiv c_0 \quad \mathrm{sec}_g(0) \equiv q_0 \quad g(1) \equiv c_1 \quad \mathrm{sec}_g(1) \equiv q_1 \quad \mathrm{ap}_{g}(p) \equiv c_p$$

$$\mathrm{ind}_{=}\left(\lambda x:\mathbb{I}.\mathrm{refl}_{f(g(x)) =_\mathbb{I} x}(\mathrm{sec}_g(x)), 0, 1, p\right) \equiv q_p$$

The last condition needs some explanation. Since $g$ is a section of $f$, the composite $f \circ g$ is [[generalized the|the]] [[identity function]] on the [[interval type]], up to [[identification]]. Now, given any identity function on the interval type $i:\mathbb{I} \to \mathbb{I}$ with homotopy

$$j:\prod_{x:\mathbb{I}} i(x) =_\mathbb{I} x$$

we have the following square for all $x:\mathbb{I}$, $y:\mathbb{I}$, and $q:x =_\mathbb{I} y$:

$$
\begin{array}{c}
    & i(x) & \overset{\mathrm{ap}_{i}(q)}= & i(y) &  \\
    j(x) & \Vert &  & \Vert & j(y)\\
    & x & \underset{q}= & y & \\
\end{array}
$$

This [[commutative square|square commutes]] via the [[J rule]]: it suffices to construct an element of 

$$\mathrm{ap}_{i}(\mathrm{refl}_\mathbb{I}(x)) \bullet j(x) =_{i(x) =_\mathbb{I} x} j(x) \bullet \mathrm{refl}_\mathbb{I}(x)$$

But $\mathrm{ap}_{i}(\mathrm{refl}_\mathbb{I}(x)) \bullet j(x)$ reduces down to $j(x)$ via 
$$\mathrm{ap}_{i}(\mathrm{refl}_\mathbb{I}(x)) \bullet j(x) \equiv \mathrm{refl}_\mathbb{I}(i(x)) \bullet j(x) \equiv j(x)$$ 
and similarly $j(x) \bullet \mathrm{refl}_\mathbb{I}(x)$ reduces down to $j(x)$, so just take reflexivity of $j(x)$. 

So the naturality square is inductively defined by 

$$\mathrm{ind}_{=}\left(\lambda x:\mathbb{I}.\mathrm{refl}_{i(x) =_\mathbb{I} x}(j(x)), x, y, q\right):\mathrm{ap}_{i}(q) \bullet j(y) =_{i(x) =_\mathbb{I} y} j(x) \bullet q$$

When $i \coloneqq f \circ g$, $j \coloneqq \mathrm{sec}_g$, $x \coloneqq 0$, $y \coloneqq 1$, and $q \coloneqq p$, this results in the identification 

$$\mathrm{ind}_{=}\left(\lambda x:\mathbb{I}.\mathrm{refl}_{f(g(x)) =_\mathbb{I} x}(\mathrm{sec}_g(x)), 0, 1, p\right)$$

which is of the same type as $q_p$ due to the [[judgmental equalities]] in the other computation rules. 

One gets back the usual induction principle of the interval type when $C \equiv \sum_{x:\mathbb{I}} P(x)$ and $f \equiv \pi_1$ the first projection function of the dependent sum type, and one gets back the recursion principle of the interval type when $C \equiv \mathbb{I} \times P$ and $f \equiv \pi_1$ the first projection function of the product type.

### Path types and identity types

In general, functions from $\mathbb{I}$ to a type $A$ can be thought of as the [[paths]] in $A$ in [[Martin-Löf type theory]], and the [[function type]] $\mathbb{I} \to A$ can be thought of as the **[[path types]]** of $A$, similar to how in [[topology]] paths in a (topological) space $A$ are (continuous) functions from the unit interval, and how in [[cubical type theory]] the [[cubical paths]] are a kind of function type out of the pre-defined interval pre-type. 

The recursion principle of the interval type allows for paths to be defined from a given [[identification]], and [[function application to identifications]] allows for identifications to be defined from a given path:

\begin{theorem}
Every [[identification]] $q:a =_A b$ between two terms $a:A$ and $b:A$ of a type $A$ has an associated path $\mathrm{rec}_{\mathbb{I}}(a, b, p):\mathbb{I} \to A$, recursively defined by 

* $\beta_\mathbb{I}^0(a, b, q):\mathrm{rec}_{\mathbb{I}}(a, b, q)(0) =_A a$
* $\beta_\mathbb{I}^1(a, b, q):\mathrm{rec}_{\mathbb{I}}(a, b, q)(1) =_A b$
* $\beta_\mathbb{I}^p(a, b, q):\mathrm{ap}_{\mathrm{rec}_{\mathbb{I}}(a, b, q)}(p) =_{f(0) =_A f(1)} \beta_\mathbb{I}^0(a, b, q) \bullet q \bullet \beta_\mathbb{I}^p(a, b, q)^{-1}$

where 
$$\mathrm{ap}_{\mathrm{rec}_{\mathbb{I}}(a, b, q)}:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$$ 
is the [[function application to identities]], 
$$(-)\bullet(-):(a =_A b) \times (b =_A c) \to (a =_A c)$$ 
is concatenation of identities (i.e. [[transitivity]]), and 
$$(-)^{-1}:(a =_A b) \to (b =_A a)$$ 
is the inverse of identities (i.e. [[symmetry]]).
\end{theorem}

\begin{theorem}
Given a path $q:\mathbb{I} \to A$ and terms $a:A$ and $b:A$ with identities $\delta_a:q(0) =_A a$ and $\delta_b:q(1) =_A b$, there is an identity 

$$\delta_a^{-1} \bullet \mathrm{ap}_{q}(p) \bullet \delta_b:a =_{A} b$$
\end{theorem}

The path version of [[reflexivity]] of an element $x:A$ is represented by the [[constant function]] $\lambda i:\mathbb{I}.x:\mathbb{I} \to A$. By definition of [[function application to identifications]], one has 

$$\mathrm{ap}_{\lambda i:\mathbb{I}.x}(i, j, q) \equiv \mathrm{refl}_A(x)$$

for all $i, j:\mathbb{I}$ and $q:i =_\mathbb{I} j$. 

This allows us to posit versions of [[path induction]] using functions from the interval type, which states that:

\begin{theorem}
Given a type $A$, a type family $C(z)$ indexed by $z:\mathbb{I} \to A$, and a family of elements $t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)$, one could construct a dependent function $f(t):\prod_{z:\mathbb{I} \to A} C(z)$ such that $f(t, \lambda i:\mathbb{I}.x) \equiv t:C(\lambda i:\mathbb{I}.x)$. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma \vdash \mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma, x:A \vdash \mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t:C(\lambda i:\mathbb{I}.x)}$$
\end{theorem}

The alternate induction principle of the path type, which uses functions into the path type rather than families indexed by the path type, is given by:

\begin{theorem}
Given any type $C$ and function $f:C \to (\mathbb{I} \to A)$ into the path type in $A$, and given a function $c:A \to C$ and a homotopy 
$$p:\prod_{x:A} f(c(x)) =_{\mathbb{I} \to A} \lambda i:\mathbb{I}.x$$
which states that the composite of $f$ and $c$ is the canonical function which takes elements of $A$ to constant paths into $A$, one can construct a function $g:\left(\mathbb{I} \to A\right) \to C$ and a homotopy witnessing that $g$ is a [[section]] of $f$:
$$\mathrm{sec}_g:\prod_{z:\mathbb{I} \to A} f(g(z)) =_{\mathbb{I} \to A} z$$
such that for all $x:A$, $g(\lambda i:\mathbb{I}.x) \equiv c(x)$ and $\mathrm{sec}_g(\lambda i:\mathbb{I}.x) \equiv p(x)$.

**elimination rules** for path induction:
$$\frac{
\begin{array}{c}
    \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to (\mathbb{I} \to A) \\ 
    \Gamma \vdash c:A \to C \quad \Gamma \vdash p:\prod_{x:A} f(c(x)) =_{\mathbb{I} \to A} \lambda i:\mathbb{I}.x \\ 
\end{array}
}{\Gamma, z:\mathbb{I} \to A \vdash \mathrm{ind}_{\mathbb{I} \to A}^{C}(f, c, p, z):C}$$

$$\frac{
\begin{array}{c}
    \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to (\mathbb{I} \to A) \\ 
    \Gamma \vdash c:A \to C \quad \Gamma \vdash p:\prod_{x:A} f(c(x)) =_{\mathbb{I} \to A} \lambda i:\mathbb{I}.x \\ 
\end{array}
}{\Gamma, z:\mathbb{I} \to A \vdash \mathrm{indsec}_\mathrm{Unit}^{C}(f, c, p, z):f(\mathrm{ind}_\mathrm{Unit}^{C}(f, c, p, z)) =_{\mathbb{I} \to A} z}$$

**computation rules** for path induction:
$$\frac{
\begin{array}{c}
    \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to (\mathbb{I} \to A) \\ 
    \Gamma \vdash c:A \to C \quad \Gamma \vdash p:\prod_{x:A} f(c(x)) =_{\mathbb{I} \to A} \lambda i:\mathbb{I}.x \\ 
\end{array}
}{\Gamma, x:A \vdash \mathrm{ind}_{\mathbb{I} \to A}^{C}(f, c, p, \lambda i:\mathbb{I}.x) \equiv c(x):C}$$

$$\frac{
\begin{array}{c}
    \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to (\mathbb{I} \to A) \\ 
    \Gamma \vdash c:A \to C \quad \Gamma \vdash p:\prod_{x:A} f(c(x)) =_{\mathbb{I} \to A} \lambda i:\mathbb{I}.x \\
\end{array}
}{\Gamma, x:A \vdash \mathrm{indsec}_{\mathbb{I} \to A}^{C}(f, c, p, \lambda i:\mathbb{I}.x) \equiv p(x):f(\mathrm{ind}_{\mathbb{I} \to A}^{C}(f, c, p, z)) =_{\mathbb{I} \to A} z}$$
\end{theorem}

\begin{theorem}
Suppose that path induction for function types out of the interval type is true. 

Then the [[J-rule]] is true: given a type $A$ and given a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$, and a dependent function $t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))$, one can construct a dependent function

$$\mathrm{ind}_{=, A}(t):\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)$$

such that for all $x:A$, 

$$J(t, x, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

\begin{proof}
By path induction on the type family $C(f(0), f(1), \mathrm{toId}_A(f))$ indexed by $f:\mathbb{I} \to A$, we can construct a dependent function

$$\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{f:\mathbb{I} \to A} C(f(0), f(1), \mathrm{toId}_A(f))$$

such that for all $x:A$,

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$$ 

since by definition of constant function and reflexivity, one has

$$(\lambda i:\mathbb{I}.x)(0) \equiv x \quad (\lambda i:\mathbb{I}.x)(1) \equiv x \quad \mathrm{ap}_{\lambda i:\mathbb{I}.x}(\mathcal{p}) \equiv \mathrm{refl}_A(x)$$

We define 

$$J(t, x, y, p) \equiv \mathrm{ind}_{\mathbb{I} \to A}(t, \mathrm{rec}_\mathbb{I}^A(x, y, p))$$

since by interval recursion one has a path $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$ such that

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x \quad \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y \quad \mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}(0, 1, \mathcal{p}) \equiv p$$
\end{proof}

### Relation to dependent identity types

Given a type $A$, a dependent type $x:A \vdash B(x)$, terms $a_0:A$ and $a_1:A$, identity $q:a_0 =_A a_1$, terms $b_0:B(a_0)$ and $b_1:B(a_1)$, and [[dependent identity]] $r:b_0 =_B^q b_1$, let us inductively define the family of elements $x:\mathbb{I} \vdash f(x):B(x)$ by

* $\beta_f^0:f(0) =_{B(a_0)} b_0$
* $\beta_f^1:f(1) =_{B(a_1)} b_1$
* $\beta_f^p:\mathrm{apd}_f(p) =_{f(0) =_B^q f(1)} \mathrm{concat}_{\mathrm{trans}_B^q(f(0)), b_1, f(1)}(\mathrm{concat}_{\mathrm{trans}_B^q(f(0)), \mathrm{trans}_B^q(b_0), b_1}(\mathrm{apd}_{\mathrm{trans}_B^q}(\beta_f^0), r), \mathrm{inv}_{f(1), b}(\beta_f^1))$

where $\mathrm{trans}_B^q:B(a_0) \to B(a_1)$ is [[transport]], $\mathrm{ap}_f:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$ is the [[function application to identities]], $\mathrm{concat}_{a, b, c}:(a =_A b) \times (b =_A c) \to (a =_A c)$ is concatenation of identities (i.e. [[transitivity]]), and $\mathrm{inv}_{a, b}:(a =_A b) \to (b =_A a)$ is the inverse of identities (i.e. [[symmetry]]).

Let $A$ and $B$ be types, and let $e:A \simeq B$ be an equivalence between $A$ and $B$. Then there is a type family $x:\mathbb{I} \vdash C(x) \; \mathrm{type}$ defined by $C(0) \coloneqq A$, $C(1) \coloneqq B$, and $\mathrm{trans}_C^p \coloneqq e:A \simeq B$. 

### Relation to function extensionality

Postulating an interval type with [[judgmental equality|judgmental]] [[computation rules]] for the point constructors of the interval type implies [[function extensionality]]. ([Shulman](#Shulman)). 

The proof assumes a typal [[uniqueness rule]] for [[function types]]. First it constructs a function $k:A \to (\mathbb{I} \to B)$ from a dependent function $h:\prod_{x:A} f(x) =_B g(x)$, inductively defined by

* $\beta_{k(x)}^0:k(x)(0) =_B f(x)$
* $\beta_{k(x)}^1:k(x)(1) =_B g(x)$
* $\beta_{k(x)}^p:\mathrm{ap}_{k(x)}(p) =_{k(x)(0) =_B k(x)(1)} \beta_{k(x)}^0 \bullet h(x) \bullet (\beta_{k(x)}^1)^{-1}$

Then it uses the properties of function types, product types, currying, uncurrying, and the symmetry of products $A \times B \simeq B \times A$, to construct a function $k':\mathbb{I} \to (A \to B)$, inductively defined by

* $\beta_{k'}^0(x):k'(0)(x) =_B f(x)$
* $\beta_{k'}^1(x):k'(1)(x) =_B g(x)$
* $\beta_{k'}^p(x):\mathrm{ap}_{k'}(p)(x) =_{k'(0)(x) =_B k'(1)(x)} \beta_{k'}^0(x) \bullet h(x) \bullet (\beta_{k'}^1(x))^{-1})$

If the interval type has judgmental computation rules for the point constructors, then $k'(x)(0) \equiv f(x)$ and $k'(x)(1) \equiv g(x)$ for all $x:A$, which implies that $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$, and subsequently that $k'(0) \equiv f$ and $k'(1) \equiv g$. This means that there are identities $\beta_{k'}^0:k'(0) =_{A \to B} f$ and $\beta_{k'}^1:k'(1) =_{A \to B} g$, and an identity 

$$(\beta_{k'}^0)^{-1} \bullet \mathrm{ap}_{k'}(p) \bullet \beta_{k'}^1:f =_{A \to B} g$$

thus proving function extensionality. 

An interval type with only typal computation rules for the point constructors does not imply function extensionality. This is because the proof with the judgmental computation rules uses the fact that $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$ implies that $k'(0) \equiv f$ and $k'(1) \equiv g$. However, if the computation rules are typal, then the equivalent statement is that having identities $\beta_{k'}^0(x):k'(0)(x) =_B f(x)$ and $\beta_{k'}^1(x):k'(1)(x) =_B g(x)$ for all $x:A$ implies that there are identities $\beta_{k'}^0:k'(0) =_{A \to B} f$ and $\beta_{k'}^1:k'(1) =_{A \to B} g$, which is precisely [[function extensionality]], and so cannot be used to prove function extensionality. 

### Relation to propositional truncations

An interval type is the [[propositional truncation]] of the [[type of booleans]] $\mathbb{2}$. We use the definition of an interval type using a function from $\mathbb{2}$. Since the interval type has identities 

* $\mathrm{refl}_\mathbb{I}(j(0)):j(0) =_\mathbb{I} j(0)$, 
* $p:j(0) =_\mathbb{I} j(1)$, 
* $\mathrm{inv}_{j(0), j(1)}(p):j(1) =_\mathbb{I} j(0)$,
* $\mathrm{refl}_\mathbb{I}(j(1)):j(1) =_\mathbb{I} j(1)$, 

there is a dependent function 
$$f:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} j(a) =_\mathbb{I} j(b)$$
inductively defined by the identities
$$\beta_{f}(0, 0):f(0)(0) =_{j(0) =_\mathbb{I} j(0)} \mathrm{refl}_\mathbb{I}(j(0))$$ 
$$\beta_{f}(0, 1):f(0)(1) =_{j(0) =_\mathbb{I} j(1)} p$$ 
$$\beta_{f}(1, 0):f(1)(0) =_{j(1) =_\mathbb{I} j(0)} \mathrm{inv}_{j(0), j(1)}(p)$$ 
$$\beta_{f}(1, 1):f(1)(1) =_{j(1) =_\mathbb{I} j(1)} \mathrm{refl}_\mathbb{I}(j(1))$$

If [[dependent product types]] have [[judgmental equality|judgmental]] [[computation rules]], then the above becomes

$$f(0)(0) \equiv \mathrm{refl}_\mathbb{I}(j(0)):j(0) =_\mathbb{I} j(0)$$ 
$$f(0)(1) \equiv p:j(0) =_\mathbb{I} j(1)$$ 
$$f(1)(0) \equiv \mathrm{inv}_{j(0), j(1)}(p):j(1) =_\mathbb{I} j(0)$$ 
$$f(1)(1) \equiv \mathrm{refl}_\mathbb{I}(j(1)):j(1) =_\mathbb{I} j(1)$$

Both show that the interval type is the propositional truncation of the type of booleans. 

The converse is true as well: the propositional truncation of the type of booleans is the interval type. Recall that $\left[\mathbb{2}\right]$ is inductively generated by a function $j:\mathbb{2} \to \left[\mathbb{2}\right]$ and a dependent function

$$f:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} j(a) =_{\left[\mathbb{2}\right]} j(b)$$

which makes $\left[\mathbb{2}\right]$ into an [[h-proposition]]. By definition of an h-proposition, for each element $a:\mathbb{2}$ and $b:\mathbb{2}$, the identity type $j(a) =_{\left[\mathbb{2}\right]} j(b)$ is a [[contractible type]]. In particular, by induction on $\mathbb{2}$, this means that there are identities 
$$\beta_{f}(0, 0):f(0)(0) =_{j(0) =_{\left[\mathbb{2}\right]} j(0)} \mathrm{refl}_{\left[\mathbb{2}\right]}(j(0))$$ 
$$\beta_{f}(1, 1):f(1)(1) =_{j(1) =_{\left[\mathbb{2}\right]} j(1)} \mathrm{refl}_{\left[\mathbb{2}\right]}(j(1))$$
and for every identity $p:0 =_{\left[\mathbb{2}\right]} 1$, there are identities
$$\beta_{f}(0, 1):f(0)(1) =_{j(0) =_{\left[\mathbb{2}\right]} j(1)} p$$ 
$$\beta_{f}(1, 0):f(1)(0) =_{j(1) =_{\left[\mathbb{2}\right]} j(0)} \mathrm{inv}_{j(0), j(1)}(p)$$ 

Thus, one could simply take $j(0)$ and $j(1)$ as the term constructors and $f(0)(1)$ as the identity constructor of the interval type. 

If both propositional truncations and the type of booleans have [[judgmental equality|judgmental]] [[computation rules]], the the interval type also has judgmental computation rules. See ([this file](https://www.cs.bham.ac.uk/~mhe/truncation-and-extensionality/hsetfunext.html))

## Related concepts

* [[interval]], [[interval object]]

* [[booleans type]]

* [[suspension type]]

* [[circle type]]

* [[cone type]]

* [[square type]]

* [[line type]]

* [[cubical type theory]]

## References

Proofs of [[function extensionality]] using an interval type with [[judgmental equality|judgmental]] [[computation rules]] for point constructors could be found here

* [[Mike Shulman]], _An interval type implies functional extensionality_ ([blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/))
 {#Shulman11}

* Carlo Angiuli, _Univalence implies function extensionality_ ([blog](http://homotopytypetheory.org/2011/12/05/hott-in-prose/), [pdf](http://hottheory.files.wordpress.com/2011/12/hott2.pdf))

[[!redirects interval types]]
