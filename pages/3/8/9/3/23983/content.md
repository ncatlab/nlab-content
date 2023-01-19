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

### Note on terminology

There are many different names used for this particular dependent type, as well as many different names used for the terms of this dependent type. These include the following:

| name of type | name of terms |
|--------------|---------------|
| heterogeneous identity type | heterogeneous identities |
| heterogeneous path type | heterogeneous paths |
| heterogeneous identification type | heterogeneous identifications |
| heterogeneous equality type | heterogeneous equalities |

These four names have different reasons behind the use of the name: 

* The name "dependent/heterogeneous identity type" comes from the fact that the dependent identity type is the canonical [[one-to-one correspondence]] $x:B(a), y:B(b) \vdash \mathrm{Id}_B^p(x, y)$ of the [[transport]] [[equivalence in type theory|equivalence]] $\mathrm{tr}_B^p:B(a) \simeq B(b)$ on a type family $x:A \vdash B(x)$ and an identification $p:a =_A b$, which is the dependent/heterogeneous version of the identity type for the identity equivalence $\mathrm{id}_A:A \simeq A$

* The name "dependent/heterogeneous path type" comes from either the fact that every term in the heterogeneous identity type is represented by a [[dependent function]] from the [[interval type]], the dependent version of the path type. 

## Definitions

As with every other type in [[dependent type theory]], there are three notions of heterogeneous identity types: **judgmentally strict heterogeneous identity types**, **propositionally strict heterogeneous identity types**, and **weak heterogeneous identity types**, depending on whether the [[conversion rules]] use [[judgmental equality]], [[propositional equality]], or [[typal equality]]. 

### Natural deduction rules for heterogeneous identity types

The formation, introduction, and elimination rules for the different heterogeneous identity types are the same:

Formation rule for heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, y:B(a), z:B(b) \vdash y =_B^{p} z \; \mathrm{type}}$$ 

Introduction rule for heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x) \vdash \mathrm{apd}_B^{p}(w):w(a) =_B^{p} w(b)}$$ 

Elimination rule for heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash J_B^p(t, y, z, q):C(y, z, q)}$$

The computation rules for heterogeneous identity types are different depending on the notion of [[equality]] used in the computation rules:

Computation rules for judgmentally strict heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, x:A, w:B(x) \vdash J(t, w(a), w(b), \mathrm{apd}_B^{p}(w)) \equiv t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}$$

Computation rules for propositionally strict heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, x:A, w:B(x) \vdash J(t, w(a), w(b), \mathrm{apd}_B^{p}(w)) \equiv_{C(w(a), w(b), \mathrm{apd}_B^{p}(w))} t \; \mathrm{true}}$$

Computation rules for weak heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, y:B(a), z:B(b), q:y =_B^p z \vdash C(y, z, q) \; \mathrm{type} \quad \Gamma, x:A, w:B(x) \vdash t:C(w(a), w(b), \mathrm{apd}_B^{p}(w))}{\Gamma, x:A, w:B(x) \vdash \beta_{=_B^p}(w):J(t, w(a), w(b), \mathrm{apd}_B^{p}(w)) =_{C(w(a), w(b), \mathrm{apd}_B^{p}(w))} t}$$

The same is true of the optional uniqueness rules for heterogeneous identity types:

Optional uniqueness rules for judgmentally strict heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x), q:w(a) =_B^{p} w(b) \vdash q \equiv \mathrm{apd}_B^{p}(w):w(a) =_B^{p} w(b)}$$

Optional uniqueness rules for propositionally strict heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x), q:w(a) =_B^{p} w(b) \vdash q \equiv_{w(a) =_B^{p} w(b)} \mathrm{apd}_B^{p}(w) \; \mathrm{true}}$$

Optional uniqueness rules for weak heterogeneous identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, x:A, w:B(x), q:w(a) =_B^{p} w(b) \vdash K_B^p(x, w, q):q =_{w(a) =_B^{p} w(b)} \mathrm{apd}_B^{p}(w)}$$

### As weak transport along an identity

Another way to define the heterogeneous identity type is by using [[weak transport]] along the identity $p$:

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

In [[higher observational type theory]], the heterogeneous identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$.  The resulting heterogeneous identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of heterogeneous identity types.  The [[type formation|formation rule]] is then

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\; \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\; \mathrm{type}}$$

... needs to be finished

#### Heterogeneous identity types in universes

Given a term of a universe $A:\mathcal{U}$, a judgment $z:\mathcal{T}_\mathcal{U}(A) \vdash B:\mathcal{U}$, terms $x:\mathcal{T}_\mathcal{U}(A)$ and $y:\mathcal{T}_\mathcal{U}(A)$, and an identity $p:\mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(x,y)$, we have

$$\mathrm{ap}_{z.B}(p):\mathrm{id}_\mathcal{U}(B(x),B(y))$$

and 

$$(u,v):\mathcal{T}_\mathcal{U}(B(x)) \times \mathcal{T}_\mathcal{U}(B(y)) \vdash \pi_1(\nabla(\mathrm{ap}_{z.B}(p)))(u,v):\mathcal{U}$$

We could define a heterogeneous identity type as

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

[[!redirects dependent identity type]]
[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]

[[!redirects weak dependent identity type]]
[[!redirects weak dependent identity types]]
[[!redirects weak heterogeneous identity type]]
[[!redirects weak heterogeneous identity types]]

[[!redirects strict dependent identity type]]
[[!redirects strict dependent identity types]]
[[!redirects strict heterogeneous identity type]]
[[!redirects strict heterogeneous identity types]]

[[!redirects judgmentally strict dependent identity type]]
[[!redirects judgmentally strict dependent identity types]]
[[!redirects judgmentally strict heterogeneous identity type]]
[[!redirects judgmentally strict heterogeneous identity types]]

[[!redirects propositionally strict dependent identity type]]
[[!redirects propositionally strict dependent identity types]]
[[!redirects propositionally strict heterogeneous identity type]]
[[!redirects propositionally strict heterogeneous identity types]]

[[!redirects dependent path type]]
[[!redirects dependent path types]]
[[!redirects heterogeneous path type]]
[[!redirects heterogeneous path types]]

[[!redirects weak dependent path type]]
[[!redirects weak dependent path types]]
[[!redirects weak heterogeneous path type]]
[[!redirects weak heterogeneous path types]]

[[!redirects strict dependent path type]]
[[!redirects strict dependent path types]]
[[!redirects strict heterogeneous path type]]
[[!redirects strict heterogeneous path types]]

[[!redirects judgmentally strict dependent path type]]
[[!redirects judgmentally strict dependent path types]]
[[!redirects judgmentally strict heterogeneous path type]]
[[!redirects judgmentally strict heterogeneous path types]]

[[!redirects propositionally strict dependent path type]]
[[!redirects propositionally strict dependent path types]]
[[!redirects propositionally strict heterogeneous path type]]
[[!redirects propositionally strict heterogeneous path types]]

[[!redirects dependent identification type]]
[[!redirects dependent identification types]]
[[!redirects heterogeneous identification type]]
[[!redirects heterogeneous identification types]]

[[!redirects weak dependent identification type]]
[[!redirects weak dependent identification types]]
[[!redirects weak heterogeneous identification type]]
[[!redirects weak heterogeneous identification types]]

[[!redirects strict dependent identification type]]
[[!redirects strict dependent identification types]]
[[!redirects strict heterogeneous identification type]]
[[!redirects strict heterogeneous identification types]]

[[!redirects judgmentally strict dependent identification type]]
[[!redirects judgmentally strict dependent identification types]]
[[!redirects judgmentally strict heterogeneous identification type]]
[[!redirects judgmentally strict heterogeneous identification types]]

[[!redirects propositionally strict dependent identification type]]
[[!redirects propositionally strict dependent identification types]]
[[!redirects propositionally strict heterogeneous identification type]]
[[!redirects propositionally strict heterogeneous identification types]]

[[!redirects dependent equality type]]
[[!redirects dependent equality types]]
[[!redirects heterogeneous equality type]]
[[!redirects heterogeneous equality types]]

[[!redirects weak dependent equality type]]
[[!redirects weak dependent equality types]]
[[!redirects weak heterogeneous equality type]]
[[!redirects weak heterogeneous equality types]]

[[!redirects strict dependent equality type]]
[[!redirects strict dependent equality types]]
[[!redirects strict heterogeneous equality type]]
[[!redirects strict heterogeneous equality types]]

[[!redirects judgmentally strict dependent equality type]]
[[!redirects judgmentally strict dependent equality types]]
[[!redirects judgmentally strict heterogeneous equality type]]
[[!redirects judgmentally strict heterogeneous paequalityth types]]

[[!redirects propositionally strict dependent equality type]]
[[!redirects propositionally strict dependent equality types]]
[[!redirects propositionally strict heterogeneous equality type]]
[[!redirects propositionally strict heterogeneous equality types]]

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

[[!redirects dependent equality]]
[[!redirects dependent equalities]]
[[!redirects heterogeneous equality]]
[[!redirects heterogeneous equalities]]