
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundational axiom
+-- {: .hide}
[[!include foundational axiom - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], an **axiom of set truncation** is a [[axiom]] or unjustified rule which implies the [[uniqueness of identity proofs]] which states that every type is an [[h-set]]. Adding an axiom of set truncation to a dependent type theory results in a [[set-level type theory]]. 

## Examples

TODO: show that each of the axioms below implies the [[uniqueness of identity proofs]]. 

### Uniqueness of identity proofs

#### For identification types

In [[dependent type theory]], [[uniqueness of identity proofs]] for [[identification types]] is given by the following rule:

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash \mathrm{UIP}_A(a, b, p, q):\mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)}$$

#### For heterogeneous identification types

There is uniqueness of identity proofs for [[heterogeneous identification types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \\
     \Gamma \vdash q:\mathrm{hId}_{B}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{B}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash \mathrm{UIP}_{B}(a, b, p, y, z, q, r):\mathrm{Id}_{\mathrm{hId}_{B}(a, b, p, y, z)}(q, r)}$$

Uniqueness of identity proofs for identification types follows from uniqueness of identity proofs for heterogeneous identification types by taking canonical element $\mathrm{pt}:\mathbb{1}$ of the [[unit type]] $\mathbb{1}$, identification $\mathrm{refl}_{\mathbb{1}}(\mathrm{pt}):\mathrm{Id}_{\mathbb{1}}(\mathrm{pt}, \mathrm{pt})$, and elements $a:A$ and $b:A$. Since the following two types are equivalent: 
$$\mathrm{Id}_{A}(a, b) \simeq \mathrm{hId}_{A}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$$
and because $\mathrm{hId}_{A}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$ is always a [[mere proposition]] by uniqueness of identity proofs for heterogeneous identification types, it follows that $\mathrm{Id}_{A}(a, b)$ is also always a mere proposition. 

Similarly, there is also uniqueness of identity proofs for [[dependent heterogeneous identification types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \\
     \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash \mathrm{UIP}_{x:A.B(x)}(a, b, p, y, z, q, r):\mathrm{Id}_{\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)}(q, r)}$$

Uniqueness of identity proofs for identification types follows from uniqueness of identity proofs for dependent heterogeneous identification types by defining the type $A$ to be the dependent type $C(\mathrm{pt})$ for type family $x:\mathbb{1} \vdash C(x)$ indexed by the [[unit type]] $\mathbb{1}$, and taking the canonical element $\mathrm{pt}:\mathbb{1}$, identification $\mathrm{refl}_{\mathbb{1}}(\mathrm{pt}):\mathrm{Id}_{\mathbb{1}}(\mathrm{pt}, \mathrm{pt})$, and elements $a:C(\mathrm{pt})$ and $b:C(\mathrm{pt})$. Since the two types are equivalent:
$$\mathrm{Id}_{A}(a, b) \equiv \mathrm{Id}_{C(\mathrm{pt})}(a, b) \simeq \mathrm{hId}_{x:\mathbb{1}.C(x)}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$$
and because $\mathrm{hId}_{x:\mathbb{1}.C(x)}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$ is always a [[mere proposition]] by uniqueness of identity proofs for dependent heterogeneous identification types, it follows that $\mathrm{Id}_{C(\mathrm{pt})}(a, b)$ and thus by definition $\mathrm{Id}_{A}(a, b)$ is also always a mere proposition. 

### Axiom K

#### For identification types

In [[dependent type theory]], [[axiom K (type theory)|axiom K]] is given by the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash a:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, a)}{\Gamma\vdash K_A(a, p):\mathrm{Id}_{\mathrm{Id}_A(a, a)}(p, refl_A(a))}$$

#### For heterogeneous identification types

There is an axiom K for [[heterogeneous identification types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \\
     \Gamma \vdash q:\mathrm{hId}_{B}(a, b, p, f(a), f(b))
    \end{array}
}{\Gamma \vdash K_{B}(f, a, b, p, q):\mathrm{Id}_{\mathrm{hId}_{B}(a, b, p, f(a), f(b))}(q, \mathrm{ap}_{B}(f, a, b, p))}$$

Axiom K for identification types follows from axiom K for heterogeneous identification types by taking canonical element $\mathrm{pt}:\mathbb{1}$ of the [[unit type]] $\mathbb{1}$, identification $\mathrm{refl}_{\mathbb{1}}(\mathrm{pt}):\mathrm{Id}_{\mathbb{1}}(\mathrm{pt}, \mathrm{pt})$, and elements $a:A$ and $b:A$. Since the following two types are equivalent: 
$$\mathrm{Id}_{A}(a, b) \simeq \mathrm{hId}_{A}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$$
and because $\mathrm{hId}_{A}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, a)$ is always a [[contractible type]] with [[center of contraction]] $\mathrm{ap}_{A}(f, \mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}))$ for element $a:A$, and function $f:\mathbb{1} \to A$, by axiom K for heterogeneous identification types, it follows that $\mathrm{Id}_{A}(a, a)$ is also always a contractible type, with center of contraction $\mathrm{refl}_A(a)$. 

Similarly, there is also an axiom K for [[dependent heterogeneous identification types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \\
     \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), f(b))
    \end{array}
}{\Gamma \vdash K_{x:A.B(x)}(f, a, b, p, q):\mathrm{Id}_{\mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), f(b))}(q, \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}$$

Axiom K for identification types follows from axiom K for dependent heterogeneous identification types by defining the type $A$ to be the dependent type $C(\mathrm{pt})$ for type family $x:\mathbb{1} \vdash C(x)$ indexed by the [[unit type]] $\mathbb{1}$, and taking the canonical element $\mathrm{pt}:\mathbb{1}$, identification $\mathrm{refl}_{\mathbb{1}}(\mathrm{pt}):\mathrm{Id}_{\mathbb{1}}(\mathrm{pt}, \mathrm{pt})$, and elements $a:C(\mathrm{pt})$ and $b:C(\mathrm{pt})$. Since the two types are equivalent:
$$\mathrm{Id}_{A}(a, b) \equiv \mathrm{Id}_{C(\mathrm{pt})}(a, b) \simeq \mathrm{hId}_{x:\mathbb{1}.C(x)}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$$
and because $\mathrm{hId}_{x:\mathbb{1}.C(x)}(\mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}), a, b)$ is always a [[contractible type]] with [[center of contraction]] $\mathrm{apd}_{x:\mathbb{1}.C(x)}(f, \mathrm{pt}, \mathrm{pt}, \mathrm{refl}_{\mathbb{1}}(\mathrm{pt}))$ for element $a:A$, and dependent function $f:\prod_{x:\mathbb{1}} C(x)$, by axiom K for heterogeneous identification types, it follows that $\mathrm{Id}_{C(\mathrm{pt}}(a, a)$ and thus by definition $\mathrm{Id}_{A}(a, a)$ is also always a contractible type, with center of contraction $\mathrm{refl}_A(a)$. 

### Boundary separation

In [[cubical type theory]], [[boundary separation]] is given by the following rule:

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash r:I \quad \Gamma, (r =_I 0) \vee (r =_I 1) \; \mathrm{true} \vdash a \equiv b:A}{\Gamma \vdash a \equiv b:A}$$

### Equality reflection

In [[dependent type theory]], [[equality reflection]] is given by the following rule:

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b)}{\Gamma \vdash a \equiv b:A}$$

### Strong pattern matching

...

### $S^1$-localization

In [[dependent type theory]], the [[axiom of S1-localization|axiom of $S^1$-localization]] is given by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \mathrm{circlocal}_{A}:\mathrm{isEquiv}(\mathrm{const}_{A, S^1})}$$

## See also

* [[h-set]]
* [[set-level type theory]]

[[!redirects axioms of set truncation]]