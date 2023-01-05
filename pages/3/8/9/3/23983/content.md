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

In [[dependent type theory]], given a [[type]] $A$, a [[type family]] $x:A \vdash B(x)$, [[terms]] $a_0:A$, $a_1:A$, and an [[identification]] $p:a_0 =_A a_1$, a **dependent identity type** or a **heterogeneous identity type** between two elements $b_0: B(a_0)$ and $b_1:B(a_1)$ is a type whose elements witness that $b_0$ and $b_1$ are "equal" over or modulo the identification $p$.  There are different ways to define this precisely, depending partly on the particular type theory used.

The terms of a dependent identity types are **dependent identifications** or **heterogeneous identifications**.

## Definitions

### Natural deduction rules for dependent identity types

Formation rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, y:B(a), z:B(b) \vdash y =_B^{p} z \; \mathrm{type}}$$ 

Introduction rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x) \vdash \mathrm{apd}_B^{p}(w):w(a) =_B^{p} w(b)}$$ 

Elimination rule for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash J_B^p(t, y, z, q):C(y, z, q)}$$

Computation rules for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, x:A, w:B(x) \vdash \beta_{=_B^p}(w):J(t, w(a), w(b), \mathrm{apd}_B^{p}(w)) =_{C(w(a), w(b), \mathrm{apd}_B^{p}(w))} t}$$

Optional uniqueness rules for dependent identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x), q:w(a) =_B^{p} w(b) \vdash K_B^p(x, w, q):q =_{w(a) =_B^{p} w(b)} \mathrm{apd}_B^{p}(w)}$$

### As a one-to-one correspondence

One could also define dependent identity types as [[one-to-one correspondences]] between types $B(a)$ and $B(b)$ for type $A$, elements $a:A$ and $b:A$, identity $p:a =_A b$, and type family $x:A \vdash B(x)$. The [[transport]] functions and dependent [[action on identities]] automatically come with the rules for dependent identity types, which are:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:B(a), y:B(b) \vdash x =_{B}^{p} y \; \mathrm{type}}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:A, w:B(x) \vdash \mathrm{apd}_B(a, b, p, w):w(a) =_{B}^{p} w(b)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, y:B(b) \vdash \mathrm{tr}_B^r(a, b, p, y):B(a)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:B(a) \vdash \mathrm{tr}_B^l(a, b, p, x):B(b)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:A, w:B(x), u:w(a) =_{B}^{p} w(b) \vdash r(a, b, p, x, w, u):\mathrm{tr}_B^r(a, b, p, w(b)) =_{B(a)} w(a)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:A, w:B(x), u:w(a) =_{B}^{p} w(b) \vdash l(a, b, p, x, w, u):\mathrm{tr}_B^l(a, b, p, w(a)) =_{B(b)} w(b)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, y:B(b) \vdash r_\tau(a, b, p, y):\mathrm{tr}_B^r(a, b, p, y) =_B^{p} y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:B(a) \vdash l_\tau(a, b, p, y):x =_B^{p} \mathrm{tr}_B^l(a, b, p, x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, y:B(b), x:B(a), u:x =_B^{p} y \vdash r_\eta(a, b, p, y, x, u):r_\tau(a, b, p, y) =_{(-) =_B^{p} y}^{r(a, b, p, x, w, u)} u}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b, x:B(a), y:B(b), u:x =_B^{p} y \vdash l_\eta(a, b, p, x, y, u):l_\tau(a, b, p, x) =_{x =_B^{p}(-)}^{l(a, b, p, x, w, u))} u}$$

By the rules for [[dependent product types]] and [[dependent sum types]] one could derive that

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, a:A, b:A, p:a =_A b \vdash \eta(a, b, p):\left(\prod_{y:B(b)} \mathrm{isContr}\left(\sum_{x:B(a)} x =_{B}^{p} y\right)\right) \times \left(\prod_{x:B(a)} \mathrm{isContr}\left(\sum_{y:B(b)} x =_{B}^{p} y\right)\right)}$$

which is precisely the condition that $(-) =_{B}^{p} (-)$ is a [[one-to-one correspondence]] for all types $A$ elements $a:A$ and $b:A$, identities $p:a =_A b$, and type families $x:A \vdash B(x)$. 

### As transport along an identity

Another way to define the dependent identity type is by using [[transport]] along the identification $p$:

$$
  (a =_B^p b) 
  \;\coloneqq\; 
  \big(
    \mathrm{tr}_B^p(a) 
    =_{B(b)} 
    b
  \big)
  \,.
$$ 

### Definition in higher observational type theory 

In [[higher observational type theory]], the dependent identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$.  The resulting dependent identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of dependent identity types.  The [[type formation|formation rule]] is then

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\; \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\; \mathrm{type}}$$

... needs to be finished

#### Dependent identity types in universes

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

## Categorical semantics

needs to be written

## See also

[[!include notions of type]]

## References

* [[Mike Shulman]], *Towards Third-Generation HOTT -- Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], *Towards Third-Generation HOTT -- Part 2* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]

[[!redirects dependent path]]
[[!redirects dependent paths]]
[[!redirects heterogeneous path]]
[[!redirects heterogeneous paths]]

[[!redirects dependent identity]]
[[!redirects dependent identities]]
[[!redirects heterogeneous identity]]
[[!redirects heterogeneous identities]]

[[!redirects dependent identification]]
[[!redirects dependent identifications]]
[[!redirects heterogeneous identification]]
[[!redirects heterogeneous identifications]]