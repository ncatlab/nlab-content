
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

...

### Axiom K

In [[dependent type theory]], [[axiom K (type theory)|axiom K]] is given by the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash a:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, a)}{\Gamma\vdash K_A(a, p):\mathrm{Id}_{\mathrm{Id}_A(a, a)}(p, refl_A(a))}$$

There are also axiom K for [[heterogeneous identity types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash f:A \to B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \\
     \Gamma \vdash q:\mathrm{hId}_{B}(a, b, p, f(a), f(b))
    \end{array}
}{\Gamma \vdash K_{B}(f, a, b, p, q):\mathrm{Id}_{\mathrm{hId}_{B}(a, b, p, f(a), f(b))}(q, \mathrm{ap}_{B}(f, a, b, p))}$$

and for [[dependent heterogeneous identity types]]:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \\
     \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), f(b))
    \end{array}
}{\Gamma \vdash K_{x:A.B(x)}(f, a, b, p, q):\mathrm{Id}_{\mathrm{hId}_{x:A.B(x)}(a, b, p, f(a), f(b))}(q, \mathrm{apd}_{x:A.B(x)}(f, a, b, p))}$$

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

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \epsilon_A(f):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \eta_A(f):\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(\epsilon_A(f)), f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash y:\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(x), f)}{\Gamma \vdash c_{\epsilon_A}(f, x, y):\mathrm{Id}_{A}(\epsilon_A(f), x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash y:\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(x), f)}{\Gamma \vdash c_{\eta_A}(f, x, y):\mathrm{hId}_{z:A.\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(z), f)}(\epsilon_A(f), x, c_{\epsilon_A}(f, x, y), \eta_A(f), y)}$$

## See also

* [[h-set]]
* [[set-level type theory]]

[[!redirects axioms of set truncation]]