
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

### Using dependent sum types

There is another way of defining the interval type, as the higher inductive type $\mathbb{I}$ generated by an element of the dependent sum type

$$\mathrm{path}:\sum_{0:\mathbb{I}} \sum_{1:\mathbb{I}} 0 =_\mathbb{I} 1$$

Then the induction principle says that for every type family $C(x)$ indexed by $x:\mathbb{I}$ and every 
$$c_\mathrm{path}:\sum_{c_0:C(\pi_1(\mathrm{path}))} \sum_{c_1:C(\pi_1(\pi_2(\mathrm{path})))} c_0 =_C^{\pi_2(\pi_2(\mathrm{path}))} c_1$$ 
we have a dependent function 

$$\mathrm{ind}_{\mathbb{I}}^{C(-)}(c_\mathrm{path}):\prod_{x:\mathbb{I}} C(x)$$

such that 

$$(\mathrm{ind}_{\mathbb{I}}^{C(-)}(c_\mathrm{path})(\pi_1(\mathrm{path})), (\mathrm{ind}_{\mathbb{I}}^{C(-)}(c_\mathrm{path})(\pi_1(\pi_2(\mathrm{path}))), \mathrm{apd}_{\mathrm{ind}_{\mathbb{I}}^{C(-)}(c_\mathrm{path})}(\pi_2(\pi_2(\mathrm{path}))))) \equiv c_\mathrm{path}$$

### Using a function from the boolean domain

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

### Relation to identity types

Every [[identity]] $q:a =_A b$ between two terms $a:A$ and $b:A$ of a type $A$ has an associated [[term in context]] $x:\mathbb{I} \vdash f(x):A$, inductively defined by 

* $\beta_f^0:f(0) =_A a$
* $\beta_f^1:f(1) =_A b$
* $\beta_f^p:\mathrm{ap}_f(p) =_{f(0) =_A f(1)} \beta_f^0 \bullet q \bullet (\beta_f^1)^{-1}$

where 
$$\mathrm{ap}_f:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$$ 
is the [[function application to identities]], 
$$(-)\bullet(-):(a =_A b) \times (b =_A c) \to (a =_A c)$$ 
is concatenation of identities (i.e. [[transitivity]]), and 
$$(-)^{-1}:(a =_A b) \to (b =_A a)$$ 
is the inverse of identities (i.e. [[symmetry]]).

Conversely, given a function $f:\mathbb{I} \to A$ and terms $a:A$ and $b:A$ with identities $\delta_a:f(0) =_A a$ and $\delta_b:f(1) =_A b$, there is an identity 

$$\delta_a^{-1} \bullet \mathrm{ap}_{f}(p) \bullet \delta_b:a =_{A} b$$

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

An interval type is the [[propositional truncation]] of the [[boolean domain]] $\mathbb{2}$. We use the definition of an interval type using a function from $\mathbb{2}$. Since the interval type has identities 

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

Both show that the interval type is the propositional truncation of the boolean domain. 

The converse is true as well: the propositional truncation of the boolean domain is the interval type. Recall that $\left[\mathbb{2}\right]$ is inductively generated by a function $j:\mathbb{2} \to \left[\mathbb{2}\right]$ and a dependent function

$$f:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} j(a) =_{\left[\mathbb{2}\right]} j(b)$$

which makes $\left[\mathbb{2}\right]$ into an [[h-proposition]]. By definition of an h-proposition, for each element $a:\mathbb{2}$ and $b:\mathbb{2}$, the identity type $j(a) =_{\left[\mathbb{2}\right]} j(b)$ is a [[contractible type]]. In particular, by induction on $\mathbb{2}$, this means that there are identities 
$$\beta_{f}(0, 0):f(0)(0) =_{j(0) =_{\left[\mathbb{2}\right]} j(0)} \mathrm{refl}_{\left[\mathbb{2}\right]}(j(0))$$ 
$$\beta_{f}(1, 1):f(1)(1) =_{j(1) =_{\left[\mathbb{2}\right]} j(1)} \mathrm{refl}_{\left[\mathbb{2}\right]}(j(1))$$
and for every identity $p:0 =_{\left[\mathbb{2}\right]} 1$, there are identities
$$\beta_{f}(0, 1):f(0)(1) =_{j(0) =_{\left[\mathbb{2}\right]} j(1)} p$$ 
$$\beta_{f}(1, 0):f(1)(0) =_{j(1) =_{\left[\mathbb{2}\right]} j(0)} \mathrm{inv}_{j(0), j(1)}(p)$$ 

Thus, one could simply take $j(0)$ and $j(1)$ as the term constructors and $f(0)(1)$ as the identity constructor of the interval type. 

If both propositional truncations and the boolean domain have [[judgmental equality|judgmental]] [[computation rules]], the the interval type also has judgmental computation rules. See ([this file](https://www.cs.bham.ac.uk/~mhe/truncation-and-extensionality/hsetfunext.html))

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
