
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
$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash c_p:\mathrm{trans}^C(p)(c_0) =_{C[1/x]} c_1 \quad \Gamma \vdash i:\mathbb{I}}{\Gamma \vdash \mathrm{ind}_\mathbb{I}^C(i, c_0, c_1, c_p):C[p/x]}$$

Computation rules for the interval type:
$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash c_p:\mathrm{trans}^C(p)(c_0) =_{C[1/x]} c_1}{\Gamma \vdash \beta_\mathbb{I}^{0}: \mathrm{ind}_\mathbb{I}^{C}(0, c_0, c_1, c_p) =_{C[0/x]} c_0}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash c_p:\mathrm{trans}^C(p)(c_0) =_{C[1/x]} c_1}{\Gamma \vdash \beta_\mathbb{I}^{1}: \mathrm{ind}_\mathbb{I}^{C}(1, c_0, c_1, c_p) =_{C[1/x]} c_1}$$

$$\frac{\Gamma, x:\mathbb{I} \vdash C \; \mathrm{type} \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma \vdash c_1:C[1/x] \quad \Gamma \vdash c_p:\mathrm{trans}^C(p)(c_0) =_{C[1/x]} c_1}{\Gamma \vdash \beta_\mathbb{I}^{p}: \mathrm{apd}_{(\lambda y.\mathrm{ind}_\mathbb{I}^{C}(y, c_0, c_1, c_p))}(p) =_{\mathrm{trans}^C(p)(c_0) =_{C[1/x]} c_1} c_p}$$

Uniqueness rules for the interval type:
...

## Properties

* An interval type is provably [[contractible type|contractible]].  Conversely, any contractible type satisfies the rules of an interval type up to propositional equality.

* An interval type is a [[suspension type]] of the [[unit type]], and the suspension of an interval type is a 2-[[globe]] type. 

* An interval type is a [[cone type]] of the unit type.

* An interval type is a [[cubical type]] $\Box^1$. 

### Relation to identity types

Every [[identity]] $q:a =_A b$ between two terms $a:A$ and $b:A$ of a type $A$ has an associated function $f:\mathbb{I} \to A$ with domain the interval type and codomain $A$, inductively defined by 

* $\beta_f^0:f(0) =_A a$
* $\beta_f^1:f(1) =_A b$
* $\beta_f^p:\mathrm{ap}_f(p) =_{f(0) =_A f(1)} \mathrm{concat}_{f(0), b, f(1)}(\mathrm{concat}_{f(0), a, b}(\beta_f^0, q), \mathrm{inv}_{f(1), b}(\beta_f^1))$

where $\mathrm{ap}_f:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$ is the [[action on identities]], $\mathrm{concat}_{a, b, c}:(a =_A b) \times (b =_A c) \to (a =_A c)$ is concatenation of identities (i.e. [[transitivity]]), and $\mathrm{inv}_{a, b}:(a =_A b) \to (b =_A a)$ is the inverse of identities (i.e. [[symmetry]]).

### Relation to dependent identity types

Given a type $A$, a dependent type $x:A \vdash B$, terms $a_0:A$ and $a_1:A$, identity $q:a_0 =_A a_1$, terms $b_0:B[a_0/x]$ and $b_1:B[a_1/x]$, and [[dependent identity]] $r:b_0 =_B^q b_1$, let us inductively define the dependent function $f:\prod_{x:\mathbb{I}} B(x)$ by

* $\beta_f^0:f(0) =_{B[a_0/x]} b_0$
* $\beta_f^1:f(1) =_{B[a_1/x]} b_1$
* $\beta_f^p:\mathrm{apd}_f(p) =_{f(0) =_B^q f(1)} \mathrm{concat}_{\mathrm{trans}_B^q(f(0)), b_1, f(1)}(\mathrm{concat}_{\mathrm{trans}_B^q(f(0)), \mathrm{trans}_B^q(b_0), b_1}(\mathrm{apd}_{\mathrm{trans}_B^q}(\beta_f^0), r), \mathrm{inv}_{f(1), b}(\beta_f^1))$

where $\mathrm{trans}_B^q:B[a_0/x] \to B[a_1/x]$ is [[transport]], $\mathrm{ap}_f:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$ is the [[action on identities]], $\mathrm{concat}_{a, b, c}:(a =_A b) \times (b =_A c) \to (a =_A c)$ is concatenation of identities (i.e. [[transitivity]]), and $\mathrm{inv}_{a, b}:(a =_A b) \to (b =_A a)$ is the inverse of identities (i.e. [[symmetry]]).

### Relation to function extensionality

Postulating an interval type with [[judgmental equality|judgmental]] [[computation rules]] for the point constructors of the interval type implies [[function extensionality]]. ([Shulman](#Shulman)). 

The proof assumes the [[uniqueness rule]] for [[function types]]. First it constructs a function $k:A \to (\mathbb{I} \to B)$ from a dependent function $h:\prod_{x:A} f(x) =_B g(x)$, inductively defined by

* $\beta_{k(x)}^0:k(x)(0) =_B f(x)$
* $\beta_{k(x)}^1:k(x)(1) =_B g(x)$
* $\beta_{k(x)}^p:\mathrm{ap}_{k(x)}(p) =_{k(x)(0) =_B k(x)(1)} \mathrm{concat}_{k(x)(0), f(x), k(x)(1)}(\mathrm{concat}_{k(x)(0), f(x), g(x)}(\beta_{k(x)}^0, h(x)), \mathrm{inv}_{k(x)(1), g(x)}(\beta_{k(x)}^1))$

Then it uses the properties of function types, product types, currying, uncurrying, and the symmetry of products $A \times B \simeq B \times A$, to construct a function $k':\mathbb{I} \to (A \to B)$, inductively defined by

* $\beta_{k'}^0(x):k'(0)(x) =_B f(x)$
* $\beta_{k'}^1(x):k'(1)(x) =_B g(x)$
* $\beta_{k'}^p(x):\mathrm{ap}_{k'}(p)(x) =_{k'(0)(x) =_B k'(1)(x)} \mathrm{concat}_{k'(0)(x), f(x), k'(1)(x)}(\mathrm{concat}_{k'(0)(x), f(x), g(x)}(\beta_{k'}^0(x), h(x)), \mathrm{inv}_{k'(1)(x), g(x)}(\beta_{k'}^1(x)))$

If the interval type has judgmental computation rules for the point constructors, the above simplifies to 

* $k'(0)(x) \equiv f(x)$
* $k'(1)(x) \equiv g(x)$
* $\mathrm{ap}_{k'}(p)(x) =_{f(x) =_B g(x)} h(x)$

Finally it use the [[judgmental equality]] in the [[computation rules]] for the interval type and the [[uniqueness rule]] for function types to construct an identity $h':f =_{A \to B} g$. Since $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$, this means that $k'(0) \equiv f$ and $k'(1) \equiv g$ and there is an identity $\mathrm{ap}_{k'}(p):f =_{A \to B} g$. 

An interval type with only typal computation rules for left and right does not imply function extensionality. This is because the proof with the judgmental computation rules uses the fact that $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$ implies that $k'(0) \equiv f$ and $k'(1) \equiv g$. However, if the computation rules are typal, then the equivalent statement is $k'(0)(x) =_B f(x)$ and $k'(1)(x) =_B g(x)$ for all $x:A$ implies that $k'(0) =_{A \to B} f$ and $k'(1) =_{A \to B} g$, which is precisely [[function extensionality]], and so cannot be used to prove function extensionality. 

## Related concepts

* [[interval]], [[interval object]]

* [[booleans type]]

* [[suspension type]]

* [[circle type]]

* [[cone type]]

* [[square type]]

* [[cubical type theory]]

## References

* [[Mike Shulman]], _An interval type implies functional extensionality_ ([blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/))
 {#Shulman}

Another proof that the interval type with definitional [[eta-conversion]] rules for point constructors could be found here

* Carlo Angiuli, _Univalence implies function extensionality_ ([blog](http://homotopytypetheory.org/2011/12/05/hott-in-prose/), [pdf](http://hottheory.files.wordpress.com/2011/12/hott2.pdf))

[[!redirects interval types]]
