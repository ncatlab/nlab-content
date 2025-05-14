
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
 {#Idea}

In [[dependent type theory]], what is traditionally called the _dependent sum type_ (really: dependent [[coproduct]]) of a [[dependent type]]  $d \,\colon\, D \;\;\vdash\;\; C_d \,\colon\, Type$ is the type whose [[terms]] are [[ordered pairs]] $(d,c)$ with $d \,\colon\, D$ and $c \,\colon\, C_d$ --- whence also called the _dependent pair type_.

In the [[categorical semantics]] [[categorical model of dependent type theory|of dependent type theory]] in [[fibration categories]], the dependent sum corresponds to internal [[coproducts]] over an index type.

In the special case that $C_d \,=\, C$ is independent of $A$ this reduces to the [[product type]] $D \times C$, while in the special case that $D =$ [[type of booleans|Bool]] it reduces to a binary [[coproduct]].

This notion is dual (in fact: adjoint) to the corresponding notion of [[dependent product type]]:

[[!include dependent functions and dependent pairs -- table]]
 




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
 {#ExtensionalityPrinciple}

The extensionality principle for the dependent sum type states that there is an [[equivalence of types]] between the [[identity type]] $(a, b) =_{\sum_{x:A} B(x)} (a', b')$ of a dependent sum type and the dependent sum $\sum_{p:a =_A a'} b =_B^p b'$ of its component's identity types:

$$
\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B(a) \quad \Gamma \vdash a':A \quad \Gamma \vdash b':B(a')}{\Gamma \vdash \mathrm{ext}_{\Sigma}(a, b, a', b'):(a, b) =_{\sum_{x:A} B(x)} (a', b') \simeq \sum_{p:a =_A a'} b =_B^p b'}
$$

The comparison function itself is readily obtained by [[Id-induction]]. That this indeed constitutes an [[equivalence of types]] is shown in [UFP13, Thm. 2.7.2](#UFP13).

{#ExtensionalityForDependentPairs} In the notation of [[dependent pairs]] ([[dependent functions and dependent pairs -- table|here]]) this reads:

<img src="/nlab/files/DependentPairExtensionality-230121.jpg" width="700">

Compare to the analogous extensionality principle for [[dependent functions]] (see at *[[function extensionality]]*, [here](function+extensionality#StatementForDependentFunctions)):

<img src="/nlab/files/DependentFunctionExtensionality-230121.jpg" width="700">

(In this dependent generality this is a special case of [UFP13, Lem. 2.9.7](#UFP13).)

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

### Using universes and dependent product types

Dependent sum types could be defined directly from universes, dependent product types, and function types - the last of which are definable from dependent product types. Given a [[type universe]] $U$, the dependent sum type of the type family $x:A \vdash B(x)$ is defined as the dependent product type

$$\sum_{x:A} B(x) \coloneqq \prod_{P:U} \prod_{x:A} (B(x) \to P) \to P$$

This was the first definition of dependent sum types in dependent type theory, appearing in [[Per Martin-Löf]]'s [original 1971 paper](#ML71) on dependent type theory. 

## Properties

### Descent and large elimination

The [[descent]] for the positive dependent sum type $\Sigma x:A.B(x)$ states that given any type family $x:A, y:B(x) \vdash C(x, y)$ one can construct a type family $z:\Sigma x:A.B(x) \vdash \mathrm{descFam}_{\Sigma x:A.B(x)}^{C}(z)$ with families of [[equivalences of types]] 
$$x:A, y:B(x) \vdash \mathrm{descEquiv}_{\Sigma x:A.B(x)}^C:\mathrm{descFam}_{\Sigma x:A.B(x)}^{C}(\mathrm{in}(x, y)) \simeq C(x, y)$$
Large elimination for positive dependent sum types strengthens the equivalences of types in descent to [[judgmental equality of types]] 
$$x:A, y:B(x) \vdash \mathrm{descFam}_{\Sigma x:A.B(x)}^{C}(\mathrm{in}(x, y)) \equiv C(x, y) \; \mathrm{type}$$

### Typal congruence rules

These are called *typal congruence rules* because they are the analogue of the judgmental [[congruence rules]] which use [[identity types]] and [[equivalence types]] instead of [[judgmental equality]]:

\begin{theorem}
Given types $A$ and $A'$ and type families $x:A \vdash B(x)$ and $x:A \vdash B'(x)$ and equivalences $e_A:A \simeq A'$ and dependent function of equivalences $e_B:\prod_{x:A} B(x) \simeq B'(e_A(x))$, there is an equivalence 
$$\mathrm{congform}_\Sigma(e_A, e_B):\left(\prod_{x:A} B(x)\right) \simeq \left(\prod_{x:A} B(x)\right)$$
\end{theorem}

\begin{proof}
This is theorem 11.1.6 of [Rijke 2022](#Rijke22), and a proof of this is given in that reference.
\end{proof}

The typal congruence rules for dependent sum types are very important for proving various other theorems in dependent type theory. For example, 

\begin{theorem}
Given a [[univalent]] [[Tarski universe]] $(U, T)$ and a $U$-small type $A:U$, the dependent sum type $\sum_{B:U} T(B) \simeq T(A)$ is contractible. 
\end{theorem}

\begin{proof}
By univalence, for all $A:U$ and $B:U$, transport across the universal type family $T$ is an equivalence of types
$$\mathrm{ua}(A, B):\mathrm{isEquiv}(\mathrm{transport}_{x:U.T(x)}(A, B))$$
and thus we have the equivalence 
$$\mathrm{pair}(\mathrm{transport}_{x:U.T(x)}(A, B), \mathrm{ua}(A, B)):(A =_U B) \simeq (T(B) \simeq T(A))$$
and thus by the typal congruence rule of dependent sum types, we have
$$\mathrm{congform}_\Sigma(\mathrm{id}_U, \lambda B:U.\mathrm{pair}(\mathrm{transport}_{x:U.T(x)}(A, B), \mathrm{ua}(A, B))):\left(\sum_{B:U} (A =_U B)\right) \simeq \left(\sum_{B:U} (T(B) \simeq T(A))\right)$$
Since the type $\sum_{B:U} (A =_U B)$ is contractible for all $A:U$, the above equivalence implies that $\sum_{B:U} (T(B) \simeq T(A))$ is also contractible. 
\end{proof}

### Quantification in dependent type theory

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

Under [[categorical semantics]], a dependent type $x\colon A \vdash B(x)\colon Type$ corresponds to a [[fibration]] or [[display map]] $B\to A$. In this case, the dependent sum is just the [[object]] $B$. This requires the dependent sum type to satisfy both $\beta$- and $\eta$-conversion. 

There is also another interpretation in category theory of the dependent sum type over $x:A \vdash B(x) \; \mathrm{type}$ as the [[initial]] $A$-indexed [[wide cospan]] over $B(x)$, the object $\sum_{x:A} B(x)$ with a family of morphisms 

$$\mathrm{in}_A(x):B(x) \to \sum_{x:A} B(x)$$

such that for any other object $C$ with a family of morphisms $f(x):B(x) \to C$, there exists a unique morphism $u_C:\sum_{x:A} B(x) \to C$ such that 

$$u_C \circ \mathrm{in}_A(x) = f(x)$$

This corresponds to the positive dependent sum types. 

## Related concepts

* [[dependent sum]], [[disjoint union]]

* [[telescope type]]

* [[product type]]

* [[dependent product type]]

* [[dependent pushout type]]

* [[record type]]

## References

A textbook account could be found in section 4.6 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

Discussion in a context of [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

For the definition of dependent sum types in terms of universes, dependent product types, and function types, see:

* {#ML71} [[Per Martin-Löf]], *A Theory of Types*, unpublished note (1971) &lbrack;[pdf](https://raw.githubusercontent.com/michaelt/martin-lof/master/pdfs/martin-loef1971%20-%20A%20Theory%20of%20Types.pdf), [[MartinLoef1971-ATheoryOfTypes.pdf:file]]&rbrack;

See also most references at *[[dependent type theory]]*.


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


