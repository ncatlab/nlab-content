
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

* On the other hand, postulating an interval type with *definitional* computation rules for `left` and `right` implies [[function extensionality]]. ([Shulman](#Shulman)).

* An interval type is a [[suspension type]] of the [[unit type]], and the suspension of an interval type is a 2-[[globe]] type. 

* An interval type is a [[cone type]] of the unit type.

* An interval type is a [[cubical type]] $\Box^1$. 

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

[[!redirects interval types]]