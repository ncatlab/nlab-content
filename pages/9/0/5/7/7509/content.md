
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Dependent sum types
* table of contents
{: toc}

## Idea

In [[dependent type theory]], a _dependent sum type_ of a [[dependent type]]  $x\colon A\vdash B(x)\colon Type$ is the type whose [[terms]] are [[ordered pairs]] $(a,b)$ with $a\colon A$ and $b\colon B(a)$ (hence also called _dependent pair type_).

In a [[model]] of the type theory in [[categorical semantics]], this is a [[dependent sum]] (indexed [[disjoint union]]).  It includes [[product types]] as the special case when B is not dependent on A, and [[sum types]] as a special case when A is the type of Booleans.

## Overview

[[!include dependent sum natural deduction - table]]

## Definition

Like any [[type formation|type constructor]] in [[type theory]], the dependent sum type is specified by rules saying when we can [[type formation|introduce]] it as a type, how to [[term introduction|construct terms]] of that type, how to use or "[[term elimination|eliminate]]" terms of that type, and how to [[computation rule|compute]] when we combine the constructors with the eliminators.

### In natural deduction

We assume that our dependent sum types have typal [[conversion rules]], as those are the most general of the conversion rules. Both the propositional and judgmental conversion rules imply the typal conversion rules by the structural rules for propositional and judgmental equality respectively. 

The formation and introduction rules are the same for both the positive and negative dependent sum types

Formation rules for dependent sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash \sum_{x:A} B(x) \; \mathrm{type}}$$

Introduction rules for dependent sum types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathrm{in}(x, y):\sum_{x:A} B(x)}$$

#### As a positive type 

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z]}{\Gamma, z:\sum_{x:A} B(x) \vdash \mathrm{ind}_{\sum_{x:A} B(x)}^C(c):C}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z]}{\Gamma, x:A, y:B \vdash \beta_{\sum_{x:A} B(x)}^C(c):\mathrm{ind}_{\sum_{x:A} B(x)}^C(c)[\mathrm{in}(x, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[\mathrm{in}(x, y)/z] \quad \Gamma, z:\sum_{x:A} B(x) \vdash u:C \quad \Gamma, x:A, y:B \vdash i_\mathrm{in}(u):u[\mathrm{in}(x, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}{\Gamma, z:\sum_{x:A} B(x) \vdash \eta_{\sum_{x:A} B(x)}^C(c):u =_{C} \mathrm{ind}_{\sum_{x:A} B(x)}^C(c)}$$

Given a [[pointed type|pointed]] [[h-proposition]] $(A, a)$, the positive dependent sum type results in $\mathrm{in}(a,-)$ being an [[equivalence of types]]. 

#### As a negative type

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \pi_2(z):B[\pi_1(z)/x]}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{\Sigma 1}(x, y):\pi_1(\mathrm{in}(x, y)) =_A x} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{\Sigma 2}(x, y):\pi_2(\mathrm{in}(x, y)) =_{B[\pi_1(\mathrm{in}(x, y))/x]} y}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \eta_{\Sigma}(z):z =_{\sum_{x:A} B(x)} \mathrm{in}(\pi_1(z), \pi_2(z))}$$

Given a [[pointed type|pointed]] [[h-proposition]] $(A, a)$, the negative dependent sum type results in $\pi_2(a,-)$ being a [[quasi-inverse function]] of $\mathrm{in}(a,-)$, rather than an [[equivalence of types]]. Thus, the positive definition is preferred to the negative definition. Alternatively, the negative dependent sum type should be defined as a [[coinductive type]] rather than an [[inductive type]]. 

#### Extensionality principle

The extensionality principle for the dependent sum type states that there is an [[equivalence of types]] between the types $(a, b) =_{\sum_{x:A} B(x)} (a', b')$ and $\sum_{p:a =_A a'} b =_B^p b'$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma \vdash a':A \quad \Gamma \vdash b':B(a')}{\Gamma \vdash \mathrm{ext}_{\Sigma}(a, b, a', b'):(a, b) =_{\sum_{x:A} B(x)} (a', b') \simeq \sum_{p:a =_A a'} b =_B^p b'}$$

### In lambda-calculus

The presentation of dependent sum type is almost exactly the same as that of [[product types]], with the simple change that $B$ may depend on $A$.  In particular, they can be presented both as a [[negative type]] or as a [[positive type]].  In both cases, the rule for building the dependent sum type is the same:

$$ \frac{A\colon Type \qquad x\colon A\vdash B(x)\colon Type}{\sum_{x\colon A} B(x)\colon Type} $$

but the constructors and eliminators may be different.

#### As a negative type

When presented negatively, primacy is given to the eliminators.  We specify that there are two ways to eliminate a term of type $\sum_{x\colon A} B(x)$: by projecting out the first component, or by projecting out the second.

$$ \frac{p \colon \sum_{x\colon A} B(x)}{\pi_1 p\colon A} \qquad \frac{p\colon \sum_{x\colon A} B(x)}{\pi_2 p\colon B(\pi_1 p)}$$

This then determines the form of the constructors: in order to construct a term of type $\sum_{x\colon A} B(x)$, we have to specify what value that term should yield when all the eliminators are applied to it.  In other words, we have to specify a pair of elements, one $a\colon A$ (to be the value of $\pi_1 p$) and one $b\colon B(a)$ (to be the value of $\pi_2 p$).

$$ \frac{a\colon A \qquad b\colon B(a)}{(a,b)\colon \sum_{x\colon A} B(x)} $$

Finally, we have computation rules which say that the relationship between the constructors and the eliminators is as we hoped.  We always have [[beta reduction]] rules

$$ \pi_1(a,b) \to_\beta a \qquad \pi_2(a,b) \to_\beta b $$

and we may or may not choose to have an [[eta reduction]] rule

$$ (\pi_1 p, \pi_2 p) \to_\eta p $$

#### As a positive type

When presented positively, primacy is given to the constructors.  We specify that the way to construct something of type $\sum_{x\colon A} B(x)$ is to give a term $a\colon A$ and a term $b\colon B(a)$:

$$ \frac{a\colon A \qquad b\colon B(a)}{(a,b)\colon \sum_{x\colon A} B(x)} $$

Of course, this is the same as the constructor obtained from the negative presentation.  However, the eliminator is different.  Now, in order to say how to *use* something of type $\sum_{x\colon A} B(x)$, we have to specify how we should behave for all possible ways that it could have been constructed.  In other words, we have to say, *assuming* that $p$ were of the form $(a,b)$, what we want to do.  Thus we end up with the following rule:

$$ \frac{z\colon \sum_{x\colon A} B(x) \vdash C(z)\colon Type\qquad
p\colon \sum_{x\colon A} B(x) \qquad x\colon A, y\colon B(x) \vdash c\colon C((x,y))}{let (x,y) = p in c \;\colon C(p)} $$

We need a term $c$ in the context of two variables of types $A$ and $B$, and the destructor or match "binds those variables" to the two components of $p$.  Note that the "ordered pair" $(x,y)$ in the destructor is just a part of the syntax; it is not an instance of the *constructor* ordered pair.

Now we have the [[beta reduction]] rule:

$$ let (x,y) = (a,b) \,in c \;\to_\beta\; c[a/x, b/y] $$

In other words, if we build an ordered pair and then break it apart, what we get is just the things we put into it.  (The notation $c[a/x, b/y]$ means to substitute $a$ for $x$ and $b$ for $y$ in the term $c$).

And (if we wish) the [[eta reduction]] rule, which is a little more subtle:

$$ let (x,y) = p in c[(x,y)/z] \;\to_\eta\; c[p/z] $$

This says that if we break something of type $ \sum_{x\colon A} B(x)$ into its components, but then we only use those two components by way of putting them back together into an ordered pair, then we might as well just not have broken it down in the first place.

Positively defined dependent sum types are naturally expressed as [[inductive types]].  For instance, in [[Coq]] syntax we have

    Inductive sig (A:Type) (B:A->Type) : Type :=
    | exist : forall (x:A), B x -> sig A B.

(Coq then implements beta-reduction, but not eta-reduction.  However, eta-equivalence is provable with the internally defined [[identity type]], using the dependent eliminator mentioned above.)

Arguably, negatively defined products should be naturally expressed as [[coinductive type]]s, but this is not exactly the case for the presentation of coinductive types used in Coq.

#### Positive versus negative

In ordinary "nonlinear" [[type theory]], the positive and negative dependent sum types are equivalent, just as in the case of [[product types]].  They manifestly have the same constructor, while we can define the eliminators in terms of each other as follows:

$$
\begin{aligned}
  \pi_1 p &\;\coloneqq\; let (x,y) = p \,in\, x\\
  \pi_2 p &\;\coloneqq\; let (x,y) = p \,in\, y\\
  let (x,y) = p in c &\;\coloneqq\; c[\pi_1 p / x, \pi_2 p / y]
\end{aligned}
$$

The [[computation rules]] then also correspond, just as for [[product types]].

Also just as for [[product types]], in order to recover the important *dependent* eliminator for the positive product type from the eliminators for the negative product type, we need the latter to satisfy the $\eta$-conversion rule so as to make the above definition well-typed.  By inserting a transport, we can make do with a [propositional](/nlab/show/eta-conversion#Propositional) $\eta$-conversion, which is also provable from the dependent eliminator.

One might expect that in "[[dependent linear type theory]]" the positive and negative dependent sums would become different.  However, the meaning of the quoted phrase is unclear.

## Quantification in dependent type theory

Given a family of types $x:A \vdash B(x)$, the [[existential quantifier]] is defined as the [[bracket type]] of the dependent sum type

$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$

The [[uniqueness quantifier]] is defined as the [[isContr]] [[modality]] of the dependent sum type

$$\exists! x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

There is also a quantifier which states that $B$ holds for at most one element $x:A$, defined by the [[isProp]] [[modality]] of the dependent sum type:
$$\mathrm{isProp}\left(\sum_{x:A} B(x)\right)$$
In each of the last two cases, one could prove that each dependent type $B(x)$ has to be a [[mere proposition]]. 

Given a natural number $n:\mathbb{N}$ and given a family of types $x:A \vdash B(x)$, we can similarly write down [[quantifiers]] to say that

* $B$ holds for exactly $n$ elements:
$$\left[\left(\sum_{x:A} \left[B(x)\right]\right) \simeq \mathrm{Fin}(n)\right]$$
* $B$ holds for at most $n$ elements: 
$$\left[\left(\sum_{x:A} \left[B(x)\right]\right) \hookrightarrow \mathrm{Fin}(n)\right]$$
* $B$ holds for at least $n$ elements: 
$$\left[\mathrm{Fin}(n) \hookrightarrow \left(\sum_{x:A} \left[B(x)\right]\right)\right]$$
where $A \simeq B$ is the [[equivalence type]] between $A$ and $B$, $A \hookrightarrow B$ is the type of [[embeddings]] between $A$ and $B$, and $\mathrm{Fin}(n)$ is the [[finite set]] with $n$ elements. 

## Categorical interpretation

Under [[categorical semantics]], a dependent type $x\colon A \vdash B(x)\colon Type$ corresponds to a [[fibration]] or [[display map]] $B\to A$.  In this case, the dependent sum is just the [[object]] $B$.  This requires the dependent sum type to satisfy both $\beta$- and $\eta$-conversion.


## Related concepts

* [[dependent sum]], [[disjoint union]]
* [[product type]]
* [[dependent product type]]


[[!redirects dependent sum type]]
[[!redirects dependent sum types]]
[[!redirects dependent pair type]]
[[!redirects dependent pair types]]

[[!redirects Σ type]]
[[!redirects Σ types]]
[[!redirects Σ-type]]
[[!redirects Σ-types]]

[[!redirects Sigma type]]
[[!redirects Sigma types]]
[[!redirects Sigma-type]]
[[!redirects Sigma-types]]

[[!redirects dependent pair]]
[[!redirects dependent pairs]]


