
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

What is called _higher observational type theory_ (HOTT) is a flavor of  [[intensional type theory]] that is a [[higher homotopy]] version of [[observational type theory]] (OTT). 

{#MayBeRegarded} It may be regarded as a [[homotopy type theory]] ([[HoTT]]): the [[propositions]] of OTT correspond to the [[h-propositions]] of HoTT, the [[sets]] in OTT correspond to [[h-sets]] in HoTT, and so forth. The notion of [[equality]] on HOTT in a [[type universe]] is based on [[bijection|one-to-one]] [[correspondences]], but is usually defined as a primitive [[identity type]] for types outside a universe. Since equality is defined type-by-type, HOTT enjoys [[function extensionality]].

There are a few technical differences (e.g. [[proofs]] of [[types]] in a [[universe]] are [[definitional equality|definitionally equal]] in HOTT, whereas proofs of types in a universe are only [[propositional equality|propositionally equal]] in HoTT) but on the whole HoTT looks a lot like HOTT.

## Overview ##

We are working in a [[dependent type theory]]. 

### Telescopes ###

Telescopes represent lists of terms in the context. 

Rules for the empty telescope

$$\frac{}{\epsilon\ \mathrm{tel}}$$

Rules for telescopes given a telescope and a type

$$\frac{\Delta\ \mathrm{tel} \quad \Delta \vdash A \mathrm{type}}{(\Delta,x:A)\ \mathrm{tel}}$$

Rules for the empty context in a telescope

$$\frac{}{():\epsilon}$$

Rules for ...

$$\frac{\delta:\Delta \quad \Delta \vdash A \mathrm{type} \quad a:A[\delta]}{(\delta,a):(\Delta,x:A)}$$

...

$$\frac{\Delta \vdash a:A \quad \delta:\Delta}{a[\delta]:A[\delta]}$$

### Identity telescopes ###

$$\frac{\Delta\ \mathrm{tel} \quad \delta:\Delta \quad \delta^{'}:\Delta}{\delta =_\Delta \delta^{'}\ \mathrm{tel}}$$

...

$$() =_\epsilon () \equiv \epsilon$$

...

$$(\delta,a) =_{\Delta,x:A} (\delta^{'},a^{'}) \equiv \left(\varsigma:\delta =_\Delta \delta^{'}, \alpha:a =_{\Delta.A}^\varsigma a^{'}\right)$$

### Dependent identity types ###

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\ \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\ \mathrm{type}}$$

The [[identity types]] in higher observational type theory is defined as 

$$a =_A a^{'} \equiv a =_{\epsilon.A}^{()} a^{'}$$

Computation rules are defend for pair types:

$$(s =_{A \times B}^\varsigma t) \equiv (\pi_1(s) =_A^\varsigma \pi_1(t)) \times (\pi_2(s) =_B^\varsigma \pi_2(t))$$

Computation rules are defined for function types:

$$(f =_{A \to B}^\varsigma g) \equiv \prod_{a:A} \prod_{b:A} \prod_{q:(a =_A b)} (f(a) =_B^\varsigma g(b))$$

Computation rules are defend for dependent pair types:

$$(s =_{\sum_{x:A} B(x)}^\varsigma t) \equiv \sum_{p:(\pi_1(s) =_A^\varsigma \pi_1(t))} (\pi_2(s) =_{B}^{\varsigma,p} \pi_2(t))$$

Computation rules are defend for dependent pair types:

$$(f =_{\prod_{x:A} B(x)}^\varsigma g) \equiv \prod_{a:A} \prod_{b:A} \prod_{p:(a =_{A}^\varsigma b)} (f(a) =_{B}^{\varsigma,p} g(b))$$

### Dependent Ap ###

...

## With universes ##

We are working in a [[dependent type theory]] with Tarski-style [[universes]].

The [[identity types]] in a universe in higher observational type theory have the following formation rule:

$$\frac{A:\mathcal{U} \quad a:\mathcal{T}_\mathcal{U}(A) \quad b:\mathcal{T}_\mathcal{U}(A)}{\mathrm{id}_A(a, b):\mathcal{U}}$$

We define a general congruence term called ap

$$\frac{x:A \vdash f:B \quad p:\mathrm{id}_A(a, a^{'})}{\mathrm{ap}_{x.f}(p):\mathrm{id}_B(f[a/x], f[a^{'}/x])}$$

and the reflexivity terms:

$$\frac{a:A}{\mathrm{refl}_{a}:\mathrm{id}_A(a, a)}$$

and computation rules for identity functions

$$\mathrm{ap}_{x.x}(p) \equiv p$$

and for constant functions $y$

$$\mathrm{ap}_{x.y}(p) \equiv \mathrm{refl}_{y}$$

Thus, ap is a higher dimensional explicit substitution. There are definitional equalities

$$\mathrm{ap}_{x.f}(\mathrm{refl}_{a}) \equiv \mathrm{refl}_{f[a/x]}$$

$$\mathrm{ap}_{y.g}(\mathrm{ap}_{x.f}(p)) \equiv \mathrm{ap}_{x.g[f/y]}(p)$$

$$\mathrm{ap}_{x.t}(p) \equiv \mathrm{refl}_{t}$$

for constant term $t$. 

### Identity types for universes ###

Let $A \cong_\mathcal{U} B$ be the type of [[one-to-one correspondences]] between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$, and let $\mathrm{id}_\mathcal{U}(A, B)$ be the identity type between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$. Then there are rules

$$\frac{R:A \cong_\mathcal{U} B}{\Delta(R):\mathrm{id}_\mathcal{U}(A, B)} \qquad \frac{P:\mathrm{id}_\mathcal{U}(A, B)}{\nabla(P):A \cong_\mathcal{U} B} \qquad \frac{R:A \cong_\mathcal{U} B}{\nabla(\Delta(R)) \equiv R}$$

### Identity types in universes and singleton contractibility ###

Given a term of a universe $A:\mathcal{U}$

$$\mathrm{id}_{\mathcal{T}_\mathcal{U}(A)} \equiv \pi_1(\nabla(\mathrm{refl}_A))$$

with terms representing **singleton contractibility. 

$$\pi_1(\pi_2(\nabla(\mathrm{refl}_A)):\prod_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

$$\pi_2(\pi_2(\nabla(\mathrm{refl}_A))):\prod_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

### Dependent identity types in universes ###

Given a term of a universe $A:\mathcal{U}$, a judgment $z:\mathcal{T}_\mathcal{U}(A) \vdash B:\mathcal{U}$, terms $x:\mathcal{T}_\mathcal{U}(A)$ and $y:\mathcal{T}_\mathcal{U}(A)$, and an identity $p:\mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(x,y)$, we have

$$\mathrm{ap}_{z.B}(p):\mathrm{id}_\mathcal{U}(B(x),B(y))$$

and 

$$(u,v):\mathcal{T}_\mathcal{U}(B(x)) \times \mathcal{T}_\mathcal{U}(B(y)) \vdash \pi_1(\nabla(\mathrm{ap}_{z.B}(p)))(u,v):\mathcal{U}$$

We could define a dependent identity type as

$$\mathrm{id}_{\mathcal{T}_\mathcal{U}(z.B)}^{p}(u, v) \coloneqq \pi_1(\nabla(\mathrm{ap}_{z.B}(p)))(u, v)$$

There is a rule

$$\frac{A:\mathcal{U} \quad z:\mathcal{T}_\mathcal{U}(A) \vdash B:\mathcal{U} \quad a:\mathcal{T}_\mathcal{U}(A)}{\mathrm{id}_{\mathcal{T}_\mathcal{U}(z.B)}^{\refl_{a}}(u, v) \equiv \mathrm{id}_{\mathcal{T}_\mathcal{U}(B[a/z])}(u, v)}$$

and for constant families $B:\mathcal{U}$

$$\mathrm{id}_{\mathcal{T}_\mathcal{U}(z.B)}^{p}(u, v) \equiv \mathrm{id}_{\mathcal{T}_\mathcal{U}(B)}(u, v)$$

## See also

* [[observational type theory]]

* [[homotopy type theory]]

* [[Martin-Löf type theory]]

* [[cubical type theory]]

## References 

Higher observational type theory was introduced in

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 2* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 3* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-12.pdf), [video](https://www.youtube.com/watch?v=9pDddxB7LbE))

[[!redirects higher observational type theories]]