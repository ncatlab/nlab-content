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

In [[dependent type theory]], given a [[type]] $A$, a [[type family]] $x:A \vdash B(x)$, [[terms]] $a_0:A$, $a_1:A$, and an [[identification]] $p:a_0 =_A a_1$, a **dependent heterogeneous identity type** between two elements $b_0: B(a_0)$ and $b_1:B(a_1)$ is a type whose elements witness that $b_0$ and $b_1$ are "equal" over or modulo the identification $p$. 

There is also a **non-dependent heterogeneous identity type** where we allow the type family to be a constant type family $B$. Non-dependent heterogeneous identity types are not the same as normal [[identity types]] because they still depend on the terms $a_0:A$ and $a_1:$A and the identification $p:a_0 =_A a_1$, as evidenced by the introduction rules for non-dependent heterogeneous identity types, which is [[function application to identifications]] rather than [[reflexivity]]. 

### Note on terminology

There are many different names used for this particular dependent type, as well as many different names used for the terms of this dependent type. These include the following:

| name of type | name of terms |
|--------------|---------------|
| heterogeneous identity type | heterogeneous identities |
| heterogeneous path type | heterogeneous paths |
| heterogeneous identification type | heterogeneous identifications |
| heterogeneous equality type | heterogeneous equalities |

These four names have different reasons behind the use of the name: 

* The name "heterogeneous identity type" comes from the fact that the dependent identity type is the canonical [[one-to-one correspondence]] $x:B(a), y:B(b) \vdash \mathrm{Id}_B^p(x, y)$ of the [[transport]] [[equivalence in type theory|equivalence]] $\mathrm{tr}_B^p:B(a) \simeq B(b)$ on a type family $x:A \vdash B(x)$ and an identification $p:a =_A b$, which is the dependent/heterogeneous version of the identity type for the identity equivalence $\mathrm{id}_A:A \simeq A$

* The name "heterogeneous path type" comes from either the fact that every term in the heterogeneous identity type is represented by a [[dependent function]] from the [[interval type]], the dependent version of the path type. 

## Definitions

Heterogeneous identity types, like function types and pair types, come in dependent and non-dependent flavors. This is because the usual natural deduction rules for dependent heterogeneous identity types require a type $A$ and a type family $x:A \vdash B(x)$; the non-dependent version is for a constant family $B$, which is just a type $B$; the dependent function $f:\prod_{x:A} B(x)$ in the rules for the dependent heterogeneous identity type becomes the non-dependent function $f:A \to B$ in the non-dependent heterogeneous identity types. 

The introduction rules for dependent and non-dependent heterogeneous identity types result in the [[dependent function application to identifications]] and non-dependent [[function application to identifications]] respectively, in the same way that the introduction rules for [[identity types]] result in reflexivity. 

Finally, as with every other type in [[dependent type theory]], the [[computation rules]] of both dependent and non-dependent heterogeneous identity types use [[judgmental equality]], [[propositional equality]], or [[typal equality]]. 

### Rules for non-dependent heterogeneous identity types

In the same way that there are rules for non-dependent function types and non-dependent pair types, there are also rules for non-dependent heterogeneous identity types, where the type family $B$ is a constant type family. 

Formation rule for non-dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B
    \end{array}
  }{\Gamma \vdash \mathrm{hId}_B(a, b, p, y, z) \; \mathrm{type}}$$ 

Introduction rule for non-dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ap}_B(f, a, b, p):\mathrm{hId}_B(a, b, p, f(a), f(b))}$$ 

Elimination rule for non-dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \quad \Gamma \vdash q:\mathrm{hId}_B(a, b, p, y, z)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, y, z, q):C(a, b, p, y, z, q)}$$

Computation rules for non-dependent heterogeneous identity types:

* Judgmental computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \equiv t:C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))}$$

* Propositional computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \equiv_{C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))} t \; \mathrm{true}}$$

* Typal computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{hId}_B}(t, f, a, b, p):\mathrm{Id}_{C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))}(\mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)), t)}$$

### Rules for dependent heterogeneous identity types

Formation rule for dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b)
    \end{array}
  }{\Gamma \vdash \mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \; \mathrm{type}}$$ 

Introduction rule for dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{apd}_{x:A.B(x)}(f, a, b, p):\mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), f(b))}$$ 

Elimination rule for dependent heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, y, z, q):C(a, b, p, y, z, q)}$$

Computation rules for dependent heterogeneous identity types:

* Judgmental computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \equiv t:C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}$$

* Propositional computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \equiv_{C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))} t \; \mathrm{true}}$$

* Typal computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{hId}_{x:A.B(x)}}(t, f, a, b, p):\mathrm{Id}_{C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}(\mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)), t)}$$

### As weak transport along an identity

Another way to define the dependent heterogeneous identity type is by using [[weak transport]] along the identity $p$:

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

In [[higher observational type theory]], the dependent heterogeneous identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$. The resulting dependent heterogeneous identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of dependent heterogeneous identity types.  The [[type formation|formation rule]] is then

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
[[!redirects dependent heterogeneous identity type]]
[[!redirects dependent heterogeneous identity types]]

[[!redirects weak dependent identity type]]
[[!redirects weak dependent identity types]]
[[!redirects weak heterogeneous identity type]]
[[!redirects weak heterogeneous identity types]]
[[!redirects weak dependent heterogeneous identity type]]
[[!redirects weak dependent heterogeneous identity types]]

[[!redirects strict dependent identity type]]
[[!redirects strict dependent identity types]]
[[!redirects strict heterogeneous identity type]]
[[!redirects strict heterogeneous identity types]]
[[!redirects strict dependent heterogeneous identity type]]
[[!redirects strict dependent heterogeneous identity types]]

[[!redirects judgmentally strict dependent identity type]]
[[!redirects judgmentally strict dependent identity types]]
[[!redirects judgmentally strict heterogeneous identity type]]
[[!redirects judgmentally strict heterogeneous identity types]]
[[!redirects judgmentally strict dependent heterogeneous identity type]]
[[!redirects judgmentally strict dependent heterogeneous identity types]]

[[!redirects propositionally strict dependent identity type]]
[[!redirects propositionally strict dependent identity types]]
[[!redirects propositionally strict heterogeneous identity type]]
[[!redirects propositionally strict heterogeneous identity types]]
[[!redirects propositionally strict dependent heterogeneous identity type]]
[[!redirects propositionally strict dependent heterogeneous identity types]]

[[!redirects dependent path type]]
[[!redirects dependent path types]]
[[!redirects heterogeneous path type]]
[[!redirects heterogeneous path types]]
[[!redirects dependent heterogeneous path type]]
[[!redirects dependent heterogeneous path types]]

[[!redirects weak dependent path type]]
[[!redirects weak dependent path types]]
[[!redirects weak heterogeneous path type]]
[[!redirects weak heterogeneous path types]]
[[!redirects weak dependent heterogeneous path type]]
[[!redirects weak dependent heterogeneous path types]]

[[!redirects strict dependent path type]]
[[!redirects strict dependent path types]]
[[!redirects strict heterogeneous path type]]
[[!redirects strict heterogeneous path types]]
[[!redirects strict dependent heterogeneous path type]]
[[!redirects strict dependent heterogeneous path types]]

[[!redirects judgmentally strict dependent path type]]
[[!redirects judgmentally strict dependent path types]]
[[!redirects judgmentally strict heterogeneous path type]]
[[!redirects judgmentally strict heterogeneous path types]]
[[!redirects judgmentally strict dependent heterogeneous path type]]
[[!redirects judgmentally strict dependent heterogeneous path types]]

[[!redirects propositionally strict dependent path type]]
[[!redirects propositionally strict dependent path types]]
[[!redirects propositionally strict heterogeneous path type]]
[[!redirects propositionally strict heterogeneous path types]]
[[!redirects propositionally strict dependent heterogeneous path type]]
[[!redirects propositionally strict dependent heterogeneous path types]]

[[!redirects dependent identification type]]
[[!redirects dependent identification types]]
[[!redirects heterogeneous identification type]]
[[!redirects heterogeneous identification types]]
[[!redirects dependent heterogeneous identification type]]
[[!redirects dependent heterogeneous identification types]]

[[!redirects weak dependent identification type]]
[[!redirects weak dependent identification types]]
[[!redirects weak heterogeneous identification type]]
[[!redirects weak heterogeneous identification types]]
[[!redirects weak dependent heterogeneous identification type]]
[[!redirects weak dependent heterogeneous identification types]]

[[!redirects strict dependent identification type]]
[[!redirects strict dependent identification types]]
[[!redirects strict heterogeneous identification type]]
[[!redirects strict heterogeneous identification types]]
[[!redirects strict dependent heterogeneous identification type]]
[[!redirects strict dependent heterogeneous identification types]]

[[!redirects judgmentally strict dependent identification type]]
[[!redirects judgmentally strict dependent identification types]]
[[!redirects judgmentally strict heterogeneous identification type]]
[[!redirects judgmentally strict heterogeneous identification types]]
[[!redirects judgmentally strict dependent heterogeneous identification type]]
[[!redirects judgmentally strict dependent heterogeneous identification types]]

[[!redirects propositionally strict dependent identification type]]
[[!redirects propositionally strict dependent identification types]]
[[!redirects propositionally strict heterogeneous identification type]]
[[!redirects propositionally strict heterogeneous identification types]]
[[!redirects propositionally strict dependent heterogeneous identification type]]
[[!redirects propositionally strict dependent heterogeneous identification types]]

[[!redirects dependent equality type]]
[[!redirects dependent equality types]]
[[!redirects heterogeneous equality type]]
[[!redirects heterogeneous equality types]]
[[!redirects dependent heterogeneous equality type]]
[[!redirects dependent heterogeneous equality types]]

[[!redirects weak dependent equality type]]
[[!redirects weak dependent equality types]]
[[!redirects weak heterogeneous equality type]]
[[!redirects weak heterogeneous equality types]]
[[!redirects weak dependent heterogeneous equality type]]
[[!redirects weak dependent heterogeneous equality types]]

[[!redirects strict dependent equality type]]
[[!redirects strict dependent equality types]]
[[!redirects strict heterogeneous equality type]]
[[!redirects strict heterogeneous equality types]]
[[!redirects strict dependent heterogeneous equality type]]
[[!redirects strict dependent heterogeneous equality types]]

[[!redirects judgmentally strict dependent equality type]]
[[!redirects judgmentally strict dependent equality types]]
[[!redirects judgmentally strict heterogeneous equality type]]
[[!redirects judgmentally strict heterogeneous paequalityth types]]
[[!redirects judgmentally strict dependent heterogeneous equality type]]
[[!redirects judgmentally strict dependent heterogeneous paequalityth types]]

[[!redirects propositionally strict dependent equality type]]
[[!redirects propositionally strict dependent equality types]]
[[!redirects propositionally strict heterogeneous equality type]]
[[!redirects propositionally strict heterogeneous equality types]]
[[!redirects propositionally strict dependent heterogeneous equality type]]
[[!redirects propositionally strict dependent heterogeneous equality types]]

[[!redirects dependent path]]
[[!redirects dependent paths]]
[[!redirects heterogeneous path]]
[[!redirects heterogeneous paths]]
[[!redirects dependent heterogeneous path]]
[[!redirects dependent heterogeneous paths]]

[[!redirects dependent identity]]
[[!redirects dependent identities]]
[[!redirects heterogeneous identity]]
[[!redirects heterogeneous identities]]
[[!redirects dependent heterogeneous identity]]
[[!redirects dependent heterogeneous identities]]

[[!redirects dependent identification]]
[[!redirects dependent identifications]]
[[!redirects heterogeneous identification]]
[[!redirects heterogeneous identifications]]
[[!redirects dependent heterogeneous identification]]
[[!redirects dependent heterogeneous identifications]]

[[!redirects dependent equality]]
[[!redirects dependent equalities]]
[[!redirects heterogeneous equality]]
[[!redirects heterogeneous equalities]]
[[!redirects dependent heterogeneous equality]]
[[!redirects dependent heterogeneous equalities]]