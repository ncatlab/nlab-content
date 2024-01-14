
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea

In any [[type theory]], judgmental equality is the notion of [[equality]] which is defined to be a [[judgment]]. Judgmental equality is most commonly used in single-level type theories like [[Martin-Löf type theory]] or [[higher observational type theory]] for making [[inductive definitions]], but it is also used in [[cubical type theory]] and [[simplicial type theory]] to define probe shapes for [[(infinity,1)-category theory|(infinity,1)-categorical]] types which could not be coherently defined in vanilla dependent type theory. 

There are two different kinds of judgmental equalities

* Judgmental equality of terms

* Judgmental equality of types, in [[dependent type theories]] with a separate [[type]] [[judgment]]. 

Judgmental equality of types is not necessary for [[dependent type theory]] with a separate type judgment. It behaves similarly to the [[equality]] between [[sets]] in [[structural set theory]], and the equality between sets is not necessary for structural set theory since one could simply work with [[bijections]] or [[one-to-one correspondences]] between sets. 


## Judgmental equality of terms

Judgmental equality of terms is given by the following judgment:

* $\Gamma \vdash a \equiv a' : A$ - $a$ and $a'$ are judgmentally equal well-typed terms of type $A$ in context $\Gamma$.

There are two different notions of judgmental equality of terms which could be distinguished:

* Weak judgmental equality of terms is just a shorthand for the [[identity type]] as [[typal equality]]

* Strict judgmental equality of terms is a strict version of equality, which behaves as the ([[equivalence relation]] interpretation of) [[propositional equality]] of [[sets]] rather than the ([[weak homotopy equivalence]] interpretation of) typal equality of types as [[infinity-groupoids]]. 

Strict judgmental equalities of terms are used in most [[dependent type theories]]. Weak judgmental equalities of terms can be used in [[weak type theories]], where a direct translation of the [[inference rules]] of the types in [[Martin-Löf type theory]] results in a weak version of Martin-Löf type theory. 

Judgmental equality of terms can be contrasted with [[propositional equality]] of terms, where equality is a [[proposition]], and [[typal equality]] of terms, where equality is a [[type]].

### Weak judgmental equality

Weak judgmental equality of terms is simply given by a reflection rule into the [[identity type]]:

$$\frac{\Gamma \vdash a \equiv a':A}{\Gamma \vdash \delta_{a, a'}:a =_A a'}$$

### Strict judgmental equality

Strict judgmental equality is an equivalence relation:

* Reflexivity of judgmental equality

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv a:A}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b \equiv a:A}$$

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A \quad b \equiv c:A }{\Gamma \vdash a \equiv c:A}$$

In addition, strict judgmental equality of terms has congruence rules for substitution, the [[principle of substitution]]:

* Principle of substitution for judgmentally equal terms:
$$\frac{\Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c(x):B}{\Gamma, \Delta(a) \vdash c(a) \equiv c(b): B}$$

If there is a separate [[type]] [[judgment]], then there is also a separate rule for the principle of substitution into type families. 

If one has judgmental equality of types, then the principle of substitution into type families is given by 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash B(x) \; \mathrm{type}}{\Gamma, \Delta(a) \vdash B(a) \equiv B(b) \; \mathrm{type}}$$

This implies the reflection rule of weak judgmental equalities because one could derive the following rule:

$$\frac{\Gamma \vdash a \equiv b:A}{\Gamma \vdash \mathrm{refl}_A(a):a =_A b}$$

Otherwise, the principle of substitution into type families is given by [[strict transport]] across judgmental equality as [[explicit conversion]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash B(x) \; \mathrm{type}}{\Gamma, \Delta(a) \vdash \mathrm{tr}_{B(-)}^{a \equiv b}:B(a) \simeq B(b)}$$

where $A \simeq B$ is the [[type of strict equivalences]] defined using [[natural deduction]] [[inference rules]]. This also implies the reflection rule of weak judgmental equalities because one could derive the following rule

$$\frac{\Gamma \vdash a \equiv b:A}{\Gamma \vdash \mathrm{tr}_{a =_A (-)}^{a \equiv b}(\mathrm{refl}_A(a)):a =_A b}$$

Similarly, for a term $c(x):B(x)$ dependent upon $x:A$, if one has judgmental equality of types, then the principle of substitution across $c(x)$ is given by the rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c(x):B(x)}{\Gamma, \Delta(b) \vdash c(a) \equiv c(b):B(b)}$$

Otherwise, it is given by a judgmental version of [[function application to identifications]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c(x):B(x)}{\Gamma, \Delta(b) \vdash \mathrm{tr}_{B(-)}^{a \equiv b}(c(a)) \equiv c(b):B(b)}$$

### In computation and uniqueness rules

Judgmental equality of terms can be used in the [[computation rules]] and [[uniqueness rules]] of types: 

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) \equiv b(a):B(a)}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

* Computation rules for negative dependent sum types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) \equiv b:B(\pi_1(a, b))}$$

* Uniqueness rules for negative dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

* Computation rules for identity types:
$$\frac{\Gamma, a:A, b:A, p:a =_A b \vdash C(a, b, p) \; \mathrm{type} \quad \Gamma \vdash t:\prod_{c:A} C(c, c, \mathrm{refl}_A(c))}{\Gamma, c:A \vdash J(t, c, c, \mathrm{refl}(c)) \equiv t:C(c, c, \mathrm{refl}_A(c))}$$

## Judgmental equality of types

In [[dependent type theory]] with a separate [[type]] [[judgment]], judgmental equality of types is given by the following judgment:

* $\Gamma \vdash A \equiv A' \; \mathrm{type}$ - $A$ and $A'$ are judgmentally equal well-typed types in context $\Gamma$.

There are two different notions of judgmental equality of types which could be distinguished:

* Weak judgmental equality of types is just a shorthand for equivalence of types 

* Strict judgmental equality of types could be thought of as making explicit the implicit [[coercion]] of [[equivalence of types|equivalent types]] as [[subtypes]], and is preserved throughout the type theory as [[congruences]].

In either case, judgmental equality of types is primarily used for [[definitional equality]] of types. 

### Weak judgmental equality

Weak judgmental equality of types is given by one of the two sets of structural rules:

* The variable conversion rule for judgmentally equal types:
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

or

* Rules for isomorphisms between judgmentally equal types:

$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma, x:A \vdash \delta_{A, B}(x):B} \qquad \frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma, y:B \vdash \delta_{A, B}^{-1}(x):A}$$

$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma, x:A \vdash \delta_{A, B}^{-1}(\delta_{A, B}(x)) \equiv x:A} \qquad \frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma, y:B \vdash \delta_{A, B}(\delta_{A, B}^{-1}(y)) \equiv y:B}$$

In the first case, one could construct isomorphisms from the variable conversion rule, other structural rules, and the rules for function types:

From the generic term rule and the variable conversion rule for judgmentally equal types $A \equiv A'$ we have $x:A' \vdash x:A$ and $x:A \vdash x:A'$, whereby from the introduction and computation rules for function types we have functions $\lambda x:A'.x:A' \to A$ and $\lambda x:A.x:A \to A'$ such that 
$$(\lambda x:A'.x)((\lambda x:A.x)(x)) \equiv (\lambda x:A'.x)(x) \equiv x:A$$ 
$$(\lambda x:A.x)((\lambda x:A'.x)(x)) \equiv (\lambda x:A.x)(x) \equiv x:A'$$ 
making both functions $\lambda x:A'.x$ and $\lambda x:A.x$ isomorphisms.

### Strict judgmental equality

In addition to the variable conversion rule, there are reflexivity, symmetry, and transitivity rules making strict judgmental equality for types an [[equivalence relation]]:

* Reflexivity of judgmental equality

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A \equiv A \; \mathrm{type}}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type}}{\Gamma \vdash B \equiv A \; \mathrm{type}}$$ 

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash B \equiv C \; \mathrm{type} }{\Gamma \vdash A \equiv C \; \mathrm{type}}$$

### Congruence rules for judgmental equality of types

In addition, strict judgmental equalities have [[congruence rules]] for every type in the type theory. 

* Congruence rules for dependent function types

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \prod_{x:A} B(x) \equiv \prod_{x:A'} B'(x)\; \mathrm{type}}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma, x:A \vdash b'(x):B(x) \\ 
	\Gamma, x:A \vdash b(x) \equiv b'(x):B(x)
\end{array}
}{\Gamma \vdash \lambda x:A.b(x) \equiv \lambda x:A.b'(x):\prod_{x:A}.B(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash f:\prod_{x:A} B(x) \quad f':\prod_{x:A} B(x) \\
	\Gamma \vdash f \equiv f':\prod_{x:A} B(x)
\end{array}
}{\Gamma, x:A \vdash f(x) \equiv f'(x):B(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma, x:A \vdash b'(x):B(x) \\ 
	\Gamma, x:A \vdash b(x) \equiv b'(x):B(x)
\end{array}
}{\Gamma \vdash \beta_{\prod}^{A, B} x:A.b(x) \equiv \beta_{\prod}^{A, B} x:A.b'(x):\prod_{x:A} b(x) =_{B(x)} (\lambda x:A.b(x))(x)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash B'(x) \; \mathrm{type} \\
	\Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \eta_{\prod}^{A, B} \equiv \eta_{\prod}^{A, B'}:\prod_{f:\prod_{x:A} B(x)} f =_{\prod_{x:A} B(x)} \lambda x:A.f(x)}$$

* Congruence rules for dependent pair types:

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \sum_{x:A} B(x) \equiv \sum_{x:A'} B'(x)\; \mathrm{type}}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}
\end{array}
}{\Gamma, x:A, y:B(x) \vdash \mathrm{pair}_{\sum}^{A, B} \equiv \mathrm{pair}_{\sum}^{A', B'}:\sum_{x:A} B(x)}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C(z) \equiv C'(z) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \mathrm{ind}_{\sum}^{A, B, C} \equiv \mathrm{ind}_{\sum}^{A', B', C'}:\prod_{g:\prod_{x:A} \prod_{y:B(x)} C(\mathrm{pair}_{\sum}^{A, B}(x, y))} \prod_{z:\sum_{x:A} B(x)} C(z)}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} B(x) \vdash C(z) \equiv C'(z) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \beta_{\sum}^{A, B, C} \equiv \beta_{\sum}^{A', B', C'}:\prod_{g:\prod_{x:A} \prod_{y:B(x)} C(\mathrm{pair}_{\sum}^{A, B}(x, y))} \prod_{x:A} \prod_{y:B(x)} \mathrm{ind}_{\sum}^{A, B, C}(g, \mathrm{pair}_{\sum}^{A, B}(x, y)) =_{C(\mathrm{pair}_{\sum}^{A, B}(x, y))} g(x, y)}$$

* Congruence rules for identity types:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \equiv x =_{A'} y}$$

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type}}{\Gamma \vdash \mathrm{refl}_A \equiv \mathrm{refl}_{A'}:\prod_{x:A} x =_A x}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \equiv C'(x, y, p) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \mathrm{ind}_{=}^{A, C} \equiv \mathrm{ind}_{=}^{A', C'}:\prod_{t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))} \prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)}$$

$$\frac{
\begin{array}{c}
	\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A, y:A, p:x =_A y \vdash C(x, y, p) \equiv C'(x, y, p) \; \mathrm{type}
\end{array}
}{\Gamma \vdash \beta_{ \mathrm{ind}_=}^{A, C} \equiv \beta_{\mathrm{ind}_=}^{A', C'}:\prod_{t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))} \prod_{x:A} \mathrm{ind}_{=}^{A, C}(t, x, x, \mathrm{refl}_A(x)) =_{C(x, x, \mathrm{refl}_A(x))} t(x)}$$

* Congruence rules for the empty type:

$$\frac{\Gamma, x:\emptyset \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\emptyset^C \equiv \mathrm{ind}_\emptyset^{C'}:\prod_{x:\emptyset} C(x) \; \mathrm{type}}$$

* Congruence rules for the type of booleans:

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\mathbb{2}^C \equiv \mathrm{ind}_\mathbb{2}^{C'}:\prod_{a:C(0)} \prod_{b:C(1)} \prod_{x:\mathbb{2}} C(x)}$$

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{2}^{0, C} \equiv \beta_\mathbb{2}^{0, C'}:\prod_{a:C(0)} \prod_{b:C(1)} \mathrm{ind}_\mathbb{2}^C(a, b, 0) =_{C(0)} a}$$

$$\frac{\Gamma, x:\mathbb{2} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{2}^{1, C} \equiv \beta_\mathbb{2}^{1, C'}:\prod_{a:C(0)} \prod_{b:C(1)} \mathrm{ind}_\mathbb{2}^C(a, b, 1) =_{C(1)} b}$$

* Congruence rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C \equiv \mathrm{ind}_\mathbb{N}^{C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \prod_{x:\mathbb{N} C(x)}}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{N}^{0, C} \equiv \beta_\mathbb{N}^{0, C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \mathrm{ind}_\mathbb{N}^C(c_0, c_s, 0) =_{C(0)} c_0}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \equiv C'(x) \; \mathrm{type}}{\Gamma \vdash \beta_\mathbb{N}^{s, C} \equiv \beta_\mathbb{N}^{s, C'}:\prod_{c_0:C(0)} \prod_{c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))} \prod_{x:\mathbb{N}} \mathrm{ind}_\mathbb{N}^C(c_0, c_s, s(x)) =_{C(s(x))} c_s(x)(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, x))}$$

Similarly, we have congruence rules for every [[axiom]] in the dependent type theory, such as 

* congruence rule for [[function extensionality]]:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{funext}_{A, B} \equiv \mathrm{funext}_{A', B'}:\prod_{f;\prod_{x:A} B(x)} \prod_{g:\prod_{x:A} B(x)} (f =_{\prod_{x:A} B(x)} g) \simeq \prod_{x:A} f(x) =_{B(x)} g(x)}$$

* congruence rule for the [[axiom of choice]]:

$$\frac{\Gamma \vdash A \equiv A' \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \equiv B'(x) \; \mathrm{type} \quad \Gamma, x:A, y:B(x) \vdash C(x, y) \equiv C'(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{choice}_{A, B, C} \equiv \mathrm{choice}_{A', B', C'}:\left(\mathrm{isSet}(A) \times \prod_{x:A} \mathrm{isSet}(B(x))\right) \to \forall x:A.\exists y:B(x).C(x, y) \to \exists g:\prod_{x:A} B(x).\forall x:A.C(x, g(x))}$$

## Judgmental equality of contexts

In some [[dependent type theories]], there is also judgmental equality of [[contexts]], which is given by the following [[judgment]]:

* $\Gamma \equiv \Gamma' \; \mathrm{ctx}$ - $\Gamma$ and $\Gamma'$ are judgmentally equal contexts.

In addition to the variable conversion rule, there are reflexivity, symmetry, and transitivity rules making judgmental equality for contexts an [[equivalence relation]]:

* Reflexivity of judgmental equality

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \equiv \Gamma \; \mathrm{ctx}}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \equiv \Delta \; \mathrm{ctx}}{\Delta \equiv \Gamma \; \mathrm{ctx}}$$

* Transitivity of judgmental equality
$$\frac{\Gamma \equiv \Delta \; \mathrm{ctx} \quad \Delta \equiv \Xi \; \mathrm{ctx}}{\Gamma \equiv \Xi \; \mathrm{ctx}}$$

## See also

* [[equality]]

* [[propositional equality]], [[typal equality]]

* [[coercion]]

## References

* Robin Adams, _Pure type systems with judgemental equality_, Journal of Functional Programming, Volume 16 Issue 2(2006)   ([web](http://dl.acm.org/citation.cfm?id=1114675))

* Vincent Siles, Hugo Herbelin, _Equality is typable in semi-full pure type systems_ ([pdf](http://pauillac.inria.fr/~herbelin/publis/lics-SilHer10-pts-typed-conv.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

[[!redirects judgmental equality]]
[[!redirects judgmental equalities]]

[[!redirects judgemental equality]]
[[!redirects judgemental equalities]]

[[!redirects weak judgmental equality]]
[[!redirects weak judgmental equalities]]

[[!redirects weak judgemental equality]]
[[!redirects weak judgemental equalities]]

[[!redirects strict judgmental equality]]
[[!redirects strict judgmental equalities]]

[[!redirects strict judgemental equality]]
[[!redirects strict judgemental equalities]]

[[!redirects judgmentally equal]]