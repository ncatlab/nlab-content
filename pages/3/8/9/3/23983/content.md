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

### Inference rules for non-dependent heterogeneous identity types

In the same way that there are [[inference rules]] for non-dependent function types and non-dependent pair types, there are also rules for non-dependent heterogeneous identity types, where the type family $B$ is a constant type family. 

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
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \equiv t(f, a, b, p):C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))}$$

* Propositional computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \equiv_{C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))} t(f, a, b, p) \; \mathrm{true}}$$

* Typal computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{hId}_B}(t, f, a, b, p):\mathrm{Id}_{C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p))}(\mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)), t(f, a, b, p))}$$

Uniqueness rule for non-dependent heterogeneous identity types:

* Judgmental uniqueness rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \quad \Gamma \vdash q:\mathrm{hId}_B(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, y, z, q) \equiv r:C(a, b, p, y, z, q)}$$

* Propositional uniqueness rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \quad \Gamma \vdash q:\mathrm{hId}_B(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, y, z, q) \equiv_{C(a, b, p, y, z, q)} r \; \mathrm{true}}$$

* Typal uniqueness rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{ap}_B(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \quad \Gamma \vdash q:\mathrm{hId}_B(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_B(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \eta_{\mathrm{hId}_B}(t, a, b, p, y, z, q, r):\mathrm{Id}_{C(a, b, p, y, z, q)}(\mathrm{ind}_{\mathrm{hId}_B}(t, a, b, p, y, z, q), r)}$$

Similar to the case for [[identity types]], having the judgmental or propositional uniqueness rules for non-dependent heterogeneous identity types implies that the type theory is an [[extensional type theory]]. The typal uniqueness rules for non-dependent heterogeneous identity types is always provable from the other four inference rules. 

The elimination, typal computation, and typal uniqueness rules for non-dependent heterogeneous identity types state that non-dependent heterogeneous identity types satisfy the **dependent universal property of non-dependent heterogeneous identity types**. If the dependent type theory also has [[dependent sum types]] and [[product types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of non-dependent heterogeneous identity types could be simplified to the following rule:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B, z:B, q:\mathrm{hId}_{B}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p)) \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{up}_{\mathrm{hId}_{B}}(t, f, a, b, p):
\begin{array}{c}
\exists!J:\left(\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p))\right) \\ 
\to \left(\prod_{c:A} \prod_{d:A} \prod_{r:\mathrm{Id}_A(c, d)} \prod_{e:B} \prod_{f:B} \prod_{s:\mathrm{hId}_{B}(c, d, r, e, f)} C(c, d, r, e, f, s)\right) \\
.\mathrm{Id}_{C(a, b, p, f(a), f(b))}(J(t, a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p)), t(f, a, b, p))
\end{array}
}$$

In natural language this states that given types $A$ and $B$, and given a type family $C(a, b, p, y, z, q)$ indexed by elements $a:A$, $b:A$, $p:\mathrm{Id}_A(a, b)$, $y:B$, $z:B$, and $q:\mathrm{hId}_{B}(a, b, p, y, z)$, for all elements $t:\prod_{f:A \to B}$, $a:A$, $b:A$, and $p:\mathrm{Id}_A(a, b)$, there exists a unique function $J$ with domain 
$$\prod_{f:A \to B} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p))$$
and codomain 
$$\prod_{c:A} \prod_{d:A} \prod_{r:\mathrm{Id}_A(c, d)} \prod_{e:B} \prod_{f:B} \prod_{s:\mathrm{hId}_{B}(c, d, r, e, f)} C(c, d, r, e, f, s)$$
such that $J(t, a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p))$ is equal to $t(f, a, b, p)$ in the type $C(a, b, p, f(a), f(b), \mathrm{apd}_{B}(f, a, b, p))$. 

### Inference rules for dependent heterogeneous identity types

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
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, y, z, q):C(a, b, p, y, z, q)}$$

Computation rules for dependent heterogeneous identity types:

* Judgmental computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \equiv t(f, a, b, p):C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}$$

* Propositional computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \equiv_{C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))} t(f, a, b, p) \; \mathrm{true}}$$

* Typal computational rules
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{hId}_{x:A.B(x)}}(t, f, a, b, p):\mathrm{Id}_{C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}(\mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)), t(f, a, b, p))}$$

Uniqueness rule for dependent heterogeneous identity types:

* Judgmental uniqueness rules

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, y, z, q) \equiv r:C(a, b, p, y, z, q)}$$

* Propositional uniqueness rules

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, y, z, q) \equiv_{C(a, b, p, y, z, q)} r \; \mathrm{true}}$$

* Typal uniqueness rules

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash r:C(a, b, p, y, z, q)
    \end{array}
  }{\Gamma \vdash \eta_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, y, z, q, r):\mathrm{Id}_{C(a, b, p, y, z, q)}(\mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t, a, b, p, y, z, q), r)}$$

Similar to the case for [[identity types]] and non-dependent heterogeneous identity types, having the judgmental or propositional uniqueness rules for dependent heterogeneous identity types implies that the type theory is an [[extensional type theory]]. The typal uniqueness rules for dependent heterogeneous identity types is always provable from the other four inference rules. 

The elimination, typal computation, and typal uniqueness rules for dependent heterogeneous identity types state that dependent heterogeneous identity types satisfy the **dependent universal property of dependent heterogeneous identity types**. If the dependent type theory also has [[dependent sum types]] and [[product types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of dependent heterogeneous identity types could be simplified to the following rule:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, p:\mathrm{Id}_A(a, b), y:B(a), z:B(b), q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \vdash C(a, b, p, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)) \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)
    \end{array}
  }{\Gamma \vdash \mathrm{up}_{\mathrm{hId}_{x:A.B(x)}}(t, f, a, b, p):
\begin{array}{c}
\exists!J:\left(\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))\right) \\ 
\to \left(\prod_{c:A} \prod_{d:A} \prod_{r:\mathrm{Id}_A(c, d)} \prod_{e:B(c)} \prod_{f:B(c)} \prod_{s:\mathrm{hId}_{x:A.B(x)}(c, d, r, e, f)} C(c, d, r, e, f, s)\right) \\
.\mathrm{Id}_{C(a, b, p, f(a), f(b))}(J(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p)), t(f, a, b, p))
\end{array}
}$$

In natural language this states that given a type $A$, a type family $B(x)$ indexed by elements $x:A$, and given a type family $C(a, b, p, y, z, q)$ indexed by elements $a:A$, $b:A$, $p:\mathrm{Id}_A(a, b)$, $y:B(a)$, $z:B(b)$, and $q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$, for all elements $t:\prod_{f:\prod_{x:A} B(x)}$, $a:A$, $b:A$, and $p:\mathrm{Id}_A(a, b)$, there exists a unique function $J$ with domain 
$$\prod_{f:\prod_{x:A} B(x)} \prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))$$
and codomain 
$$\prod_{c:A} \prod_{d:A} \prod_{r:\mathrm{Id}_A(c, d)} \prod_{e:B(c)} \prod_{f:B(c)} \prod_{s:\mathrm{hId}_{x:A.B(x)}(c, d, r, e, f)} C(c, d, r, e, f, s)$$
such that $J(t, a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))$ is equal to $t(f, a, b, p)$ in the type $C(a, b, p, f(a), f(b), \mathrm{apd}_{x:A.B(x)}(f, a, b, p))$. 

## Properties

### One-to-one correspondence structure

Heterogeneous identity types are [[one-to-one correspondences]]: given elements $a:A$, $b:A$, and $p:\mathrm{Id}_A(a, b)$, 

* for all elements $y:B(a)$, there exists a unique element $z:B(b)$ such that $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$

$$\prod_{y:B(a)} \exists!z:B(b).\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$$

* for all elements $z:B(b)$, there exists a unique element $y:B(a)$ such that $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$

$$\prod_{z:B(b)} \exists!y:B(a).\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$$

### Transport

Since the uniqueness quantifier is defined as 

$$\exists!x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

uniqueness quantifiers have a [[center of contraction]]. For the uniqueness quantifers defined above, the centers of contraction are [[transport]]:

$$\overrightarrow{\mathrm{transport}}_{x:A.B(x)}:\prod_{a:A} \prod_{b:A} \mathrm{Id}_A(a, b) \to (B(a) \to B(b))$$ 
$$\overrightarrow{\mathrm{lift}}_{x:A.B(x)}:\prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} \prod_{y:B(a)} \mathrm{hId}_{x:A.B(x)}(a, b, p, y, \overrightarrow{\mathrm{transport}}_{x:A.B(x)}(a, b, p, y))$$

Similarly, 

$$\overleftarrow{\mathrm{transport}}_{x:A.B(x)}:\prod_{a:A} \prod_{b:A} \mathrm{Id}_A(a, b) \to (B(b) \to B(a))$$ 
$$\overleftarrow{\mathrm{lift}}_{x:A.B(x)}:\prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} \prod_{z:B(b)} \mathrm{hId}_{x:A.B(x)}(a, b, p, \overleftarrow{\mathrm{transport}}_{x:A.B(x)}(a, b, p, z), z)$$

One could then show that there exist equivalences

$$\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \simeq \mathrm{Id}_{B(b)}(\overrightarrow{\mathrm{transport}}_{x:A.B(x)}(a, b, p, y), z)$$

and 

$$\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \simeq \mathrm{Id}_{B(a)}(y, \overleftarrow{\mathrm{transport}}_{x:A.B(x)}(a, b, p, z))$$

for all $a:A$, $b:A$, $p:\mathrm{Id}_A(a, b)$, $y:B(a)$, and $z:B(b)$. For constant families $B$, $\overrightarrow{\mathrm{transport}}_{B}(a, b, p, y) \coloneqq y$ and $\overleftarrow{\mathrm{transport}}_{B}(a, b, p, z) \coloneqq z$, so the above two equivalences simplify down to

$$\mathrm{hId}_{B}(a, b, p, y, z) \simeq \mathrm{Id}_{B}(y, z)$$

for non-dependent heterogeneous identity types. 

### Extensionality principles

Heterogeneous identity types are used in many extensionality principles. 

* The extensionality principle for [[function types]] states that there is an equivalence 

$$\mathrm{ext}_{\to}:\prod_{f:A \to B} \prod_{g:A \to B} \mathrm{Id}_{A \to B}(f, g) \simeq \prod_{a:A} \prod_{b:B} \prod_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}_{B}(a, b, p, f(a), g(b))$$

* The extensionality principle for [[dependent product types]] states that there is an equivalence

$$\mathrm{ext}_\Pi:\prod_{f:\prod_{x:A} B(x)} \prod_{g:\prod_{x:A} B(x)} \mathrm{Id}_{\prod_{x:A} B(x)}(f, g) \simeq \prod_{a:A} \prod_{b:B} \prod_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), g(b))$$

* The extensionality principle for [[product types]] states that there is an equivalence

$$\mathrm{ext}_{\times}:\prod_{s:A \times B} \prod_{t:A \times B} \mathrm{Id}_{A \times B}(s, t) \simeq \sum_{p:\mathrm{Id}_A(\pi_1(s), \pi_1(t))} \mathrm{hId}_{B}(\pi_1(s), \pi_1(t), p, \pi_2(s), \pi_2(t))$$

* The extensionality principle for [[dependent sum types]] states that there is an equivalence

$$\mathrm{ext}_\Sigma:\prod_{s:\sum_{x:A} B(x)} \prod_{t:\sum_{x:A} B(x)} \mathrm{Id}_{\sum_{x:A} B(x)}(s, t) \simeq \sum_{p:\mathrm{Id}_A(\pi_1(s), \pi_1(t))} \mathrm{hId}_{x:A.B(x)}(\pi_1(s), \pi_1(t), p, \pi_2(s), \pi_2(t))$$

## Categorical semantics

needs to be written

## In higher observational type theory 

In [[higher observational type theory]], the dependent heterogeneous identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$. The resulting dependent heterogeneous identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of dependent heterogeneous identity types.  The [[type formation|formation rule]] is then

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\; \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\; \mathrm{type}}$$

... needs to be finished

### Heterogeneous identity types in universes

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
[[!redirects non-dependent heterogeneous identity type]]
[[!redirects non-dependent heterogeneous identity types]]

[[!redirects weak dependent identity type]]
[[!redirects weak dependent identity types]]
[[!redirects weak heterogeneous identity type]]
[[!redirects weak heterogeneous identity types]]
[[!redirects weak dependent heterogeneous identity type]]
[[!redirects weak dependent heterogeneous identity types]]
[[!redirects weak non-dependent heterogeneous identity type]]
[[!redirects weak non-dependent heterogeneous identity types]]

[[!redirects strict dependent identity type]]
[[!redirects strict dependent identity types]]
[[!redirects strict heterogeneous identity type]]
[[!redirects strict heterogeneous identity types]]
[[!redirects strict dependent heterogeneous identity type]]
[[!redirects strict dependent heterogeneous identity types]]
[[!redirects strict non-dependent heterogeneous identity type]]
[[!redirects strict non-dependent heterogeneous identity types]]

[[!redirects judgmentally strict dependent identity type]]
[[!redirects judgmentally strict dependent identity types]]
[[!redirects judgmentally strict heterogeneous identity type]]
[[!redirects judgmentally strict heterogeneous identity types]]
[[!redirects judgmentally strict dependent heterogeneous identity type]]
[[!redirects judgmentally strict dependent heterogeneous identity types]]
[[!redirects judgmentally strict non-dependent heterogeneous identity type]]
[[!redirects judgmentally strict non-dependent heterogeneous identity types]]

[[!redirects propositionally strict dependent identity type]]
[[!redirects propositionally strict dependent identity types]]
[[!redirects propositionally strict heterogeneous identity type]]
[[!redirects propositionally strict heterogeneous identity types]]
[[!redirects propositionally strict dependent heterogeneous identity type]]
[[!redirects propositionally strict dependent heterogeneous identity types]]
[[!redirects propositionally strict non-dependent heterogeneous identity type]]
[[!redirects propositionally strict non-dependent heterogeneous identity types]]

[[!redirects dependent path type]]
[[!redirects dependent path types]]
[[!redirects heterogeneous path type]]
[[!redirects heterogeneous path types]]
[[!redirects dependent heterogeneous path type]]
[[!redirects dependent heterogeneous path types]]
[[!redirects non-dependent heterogeneous path type]]
[[!redirects non-dependent heterogeneous path types]]

[[!redirects weak dependent path type]]
[[!redirects weak dependent path types]]
[[!redirects weak heterogeneous path type]]
[[!redirects weak heterogeneous path types]]
[[!redirects weak dependent heterogeneous path type]]
[[!redirects weak dependent heterogeneous path types]]
[[!redirects weak non-dependent heterogeneous path type]]
[[!redirects weak non-dependent heterogeneous path types]]

[[!redirects strict dependent path type]]
[[!redirects strict dependent path types]]
[[!redirects strict heterogeneous path type]]
[[!redirects strict heterogeneous path types]]
[[!redirects strict dependent heterogeneous path type]]
[[!redirects strict dependent heterogeneous path types]]
[[!redirects strict non-dependent heterogeneous path type]]
[[!redirects strict non-dependent heterogeneous path types]]

[[!redirects judgmentally strict dependent path type]]
[[!redirects judgmentally strict dependent path types]]
[[!redirects judgmentally strict heterogeneous path type]]
[[!redirects judgmentally strict heterogeneous path types]]
[[!redirects judgmentally strict dependent heterogeneous path type]]
[[!redirects judgmentally strict dependent heterogeneous path types]]
[[!redirects judgmentally strict non-dependent heterogeneous path type]]
[[!redirects judgmentally strict non-dependent heterogeneous path types]]

[[!redirects propositionally strict dependent path type]]
[[!redirects propositionally strict dependent path types]]
[[!redirects propositionally strict heterogeneous path type]]
[[!redirects propositionally strict heterogeneous path types]]
[[!redirects propositionally strict dependent heterogeneous path type]]
[[!redirects propositionally strict dependent heterogeneous path types]]
[[!redirects propositionally strict non-dependent heterogeneous path type]]
[[!redirects propositionally strict non-dependent heterogeneous path types]]

[[!redirects dependent identification type]]
[[!redirects dependent identification types]]
[[!redirects heterogeneous identification type]]
[[!redirects heterogeneous identification types]]
[[!redirects dependent heterogeneous identification type]]
[[!redirects dependent heterogeneous identification types]]
[[!redirects non-dependent heterogeneous identification type]]
[[!redirects non-dependent heterogeneous identification types]]

[[!redirects weak dependent identification type]]
[[!redirects weak dependent identification types]]
[[!redirects weak heterogeneous identification type]]
[[!redirects weak heterogeneous identification types]]
[[!redirects weak dependent heterogeneous identification type]]
[[!redirects weak dependent heterogeneous identification types]]
[[!redirects weak non-dependent heterogeneous identification type]]
[[!redirects weak non-dependent heterogeneous identification types]]

[[!redirects strict dependent identification type]]
[[!redirects strict dependent identification types]]
[[!redirects strict heterogeneous identification type]]
[[!redirects strict heterogeneous identification types]]
[[!redirects strict dependent heterogeneous identification type]]
[[!redirects strict dependent heterogeneous identification types]]
[[!redirects strict non-dependent heterogeneous identification type]]
[[!redirects strict non-dependent heterogeneous identification types]]

[[!redirects judgmentally strict dependent identification type]]
[[!redirects judgmentally strict dependent identification types]]
[[!redirects judgmentally strict heterogeneous identification type]]
[[!redirects judgmentally strict heterogeneous identification types]]
[[!redirects judgmentally strict dependent heterogeneous identification type]]
[[!redirects judgmentally strict dependent heterogeneous identification types]]
[[!redirects judgmentally strict non-dependent heterogeneous identification type]]
[[!redirects judgmentally strict non-dependent heterogeneous identification types]]

[[!redirects propositionally strict dependent identification type]]
[[!redirects propositionally strict dependent identification types]]
[[!redirects propositionally strict heterogeneous identification type]]
[[!redirects propositionally strict heterogeneous identification types]]
[[!redirects propositionally strict dependent heterogeneous identification type]]
[[!redirects propositionally strict dependent heterogeneous identification types]]
[[!redirects propositionally strict non-dependent heterogeneous identification type]]
[[!redirects propositionally strict non-dependent heterogeneous identification types]]

[[!redirects dependent equality type]]
[[!redirects dependent equality types]]
[[!redirects heterogeneous equality type]]
[[!redirects heterogeneous equality types]]
[[!redirects dependent heterogeneous equality type]]
[[!redirects dependent heterogeneous equality types]]
[[!redirects non-dependent heterogeneous equality type]]
[[!redirects non-dependent heterogeneous equality types]]

[[!redirects weak dependent equality type]]
[[!redirects weak dependent equality types]]
[[!redirects weak heterogeneous equality type]]
[[!redirects weak heterogeneous equality types]]
[[!redirects weak dependent heterogeneous equality type]]
[[!redirects weak dependent heterogeneous equality types]]
[[!redirects weak non-dependent heterogeneous equality type]]
[[!redirects weak non-dependent heterogeneous equality types]]

[[!redirects strict dependent equality type]]
[[!redirects strict dependent equality types]]
[[!redirects strict heterogeneous equality type]]
[[!redirects strict heterogeneous equality types]]
[[!redirects strict dependent heterogeneous equality type]]
[[!redirects strict dependent heterogeneous equality types]]
[[!redirects strict non-dependent heterogeneous equality type]]
[[!redirects strict non-dependent heterogeneous equality types]]

[[!redirects judgmentally strict dependent equality type]]
[[!redirects judgmentally strict dependent equality types]]
[[!redirects judgmentally strict heterogeneous equality type]]
[[!redirects judgmentally strict heterogeneous paequalityth types]]
[[!redirects judgmentally strict dependent heterogeneous equality type]]
[[!redirects judgmentally strict dependent heterogeneous paequalityth types]]
[[!redirects judgmentally strict non-dependent heterogeneous equality type]]
[[!redirects judgmentally strict non-dependent heterogeneous paequalityth types]]

[[!redirects propositionally strict dependent equality type]]
[[!redirects propositionally strict dependent equality types]]
[[!redirects propositionally strict heterogeneous equality type]]
[[!redirects propositionally strict heterogeneous equality types]]
[[!redirects propositionally strict dependent heterogeneous equality type]]
[[!redirects propositionally strict dependent heterogeneous equality types]]
[[!redirects propositionally strict non-dependent heterogeneous equality type]]
[[!redirects propositionally strict non-dependent heterogeneous equality types]]

[[!redirects dependent path]]
[[!redirects dependent paths]]
[[!redirects heterogeneous path]]
[[!redirects heterogeneous paths]]
[[!redirects dependent heterogeneous path]]
[[!redirects dependent heterogeneous paths]]
[[!redirects non-dependent heterogeneous path]]
[[!redirects non-dependent heterogeneous paths]]

[[!redirects dependent identity]]
[[!redirects dependent identities]]
[[!redirects heterogeneous identity]]
[[!redirects heterogeneous identities]]
[[!redirects dependent heterogeneous identity]]
[[!redirects dependent heterogeneous identities]]
[[!redirects non-dependent heterogeneous identity]]
[[!redirects non-dependent heterogeneous identities]]

[[!redirects dependent identification]]
[[!redirects dependent identifications]]
[[!redirects heterogeneous identification]]
[[!redirects heterogeneous identifications]]
[[!redirects dependent heterogeneous identification]]
[[!redirects dependent heterogeneous identifications]]
[[!redirects non-dependent heterogeneous identification]]
[[!redirects non-dependent heterogeneous identifications]]

[[!redirects dependent equality]]
[[!redirects dependent equalities]]
[[!redirects heterogeneous equality]]
[[!redirects heterogeneous equalities]]
[[!redirects dependent heterogeneous equality]]
[[!redirects dependent heterogeneous equalities]]
[[!redirects non-dependent heterogeneous equality]]
[[!redirects non-dependent heterogeneous equalities]]

[[!redirects dependent universal property of dependent identity types]]
[[!redirects dependent universal property of dependent identification types]]
[[!redirects dependent universal property of dependent equality types]]
[[!redirects dependent universal property of dependent path types]]

[[!redirects dependent universal property of heterogeneous identity types]]
[[!redirects dependent universal property of heterogeneous identification types]]
[[!redirects dependent universal property of heterogeneous equality types]]
[[!redirects dependent universal property of heterogeneous path types]]

[[!redirects dependent universal property of dependent heterogeneous identity types]]
[[!redirects dependent universal property of dependent heterogeneous identification types]]
[[!redirects dependent universal property of dependent heterogeneous equality types]]
[[!redirects dependent universal property of dependent heterogeneous path types]]

[[!redirects dependent universal property of non-dependent heterogeneous identity types]]
[[!redirects dependent universal property of non-dependent heterogeneous identification types]]
[[!redirects dependent universal property of non-dependent heterogeneous equality types]]
[[!redirects dependent universal property of non-dependent heterogeneous path types]]