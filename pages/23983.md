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

In [[dependent type theory]], given a [[type]] $A$, a [[type family]] $x:A \vdash B(x)$, [[terms]] $a_0:A$, $a_1:A$, and an [[identification]] $p:a_0 =_A a_1$, a **dependent identity type**, **dependent path type**, a **heterogeneous identity type**, or a **heterogeneous path type** between two elements $b_0: B(a_0)$ and $b_1:B(a_1)$ is a type whose elements witness that $b_0$ and $b_1$ are "equal" over or modulo the identification $p$.  There are different ways to define this precisely, depending partly on the particular type theory used.

## Definition in Martin-Löf type theory

One way to define the dependent identity type in Martin-Lof type theory is using [[transport]] along the identification $p$:

$$(a =_B^p b) \coloneqq (\mathrm{tr}_B^p(a) =_{B(b)} b)$$ 

There are also other possibilities...

## Definition in higher observational type theory 

In [[higher observational type theory]], the dependent identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$.  The resulting dependent identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of dependent identity types.  The [[type formation|formation rule]] is then

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\; \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\; \mathrm{type}}$$

... needs to be finished

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

## Definition in cubical type theory

The path types found in [[cubical type theory]] are dependent identity types. They are defined by the following rules:

* Formation

$$\frac{\Gamma, i:I \vdash A \; \mathrm{type} \quad \Gamma \vdash a:[0/i]A \quad \Gamma \vdash b:[1/i]A}{\Gamma \vdash \mathrm{path}_{i.A}(a,b) \; \mathrm{type}}$$

* Introduction

$$\frac{\Gamma, i:I \vdash a:A}{\Gamma \vdash \lambda i.a:\mathrm{path}_{i.A}([0/i]a,[1/i]a)}$$

* Elimination

$$\frac{\Gamma \vdash p:\mathrm{path}_{i.A}(a,b) \quad \Gamma \vdash r:I}{\Gamma \vdash p(r):[r/i]A [\partial(r) \to [r \equiv 0 \to a \vert r \equiv 1 \to b]]}$$

* Computation

$$\frac{.}{\Gamma \vdash (\lambda i.a)(r) \equiv [r/i]a:[r/i]A}$$

* Uniqueness (optional)

$$\frac{.}{\Gamma \vdash p \equiv \lambda i.p(i) : \mathrm{path}_{i.A}(a,b)}$$

## Categorical semantics

needs to be written

## See also

[[!include notions of type]]

## References

For dependent identity types in [[higher observational type theory]]:

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], Towards a Third-Generation HOTT Part 2 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

For dependent identity types in [[cubical type theory]]:

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]

[[!redirects dependent path types]]
[[!redirects dependent path types]]
[[!redirects heterogeneous path type]]
[[!redirects heterogeneous path types]]