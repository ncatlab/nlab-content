
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

### Axiom K

In [[dependent type theory]], [[axiom K (type theory)|axiom K]] is given by the following rule:

$$
\frac{\Gamma\vdash A\; type \quad \Gamma\vdash a : A \quad  \quad \Gamma \vdash p : a =_A a}{\Gamma\vdash K : p =_{a =_A a} refl_A(a)}
$$

### Boundary separation

In [[cubical type theory]], [[boundary separation]] is given by the following rule:

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash r:I \quad \Gamma, (r =_I 0) \vee (r =_I 1) \; \mathrm{true} \vdash a \equiv b:A}{\Gamma \vdash a \equiv b:A}$$

### Equality reflection

In [[dependent type theory]], [[equality reflection]] is given by the following rule:

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b}{\Gamma \vdash a \equiv b:A}$$

### Strong pattern matching

...

### $S^1$-localization

In [[dependent type theory]], the [[axiom of S1-localization|axiom of $S^1$-localization]] is given by the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \mathrm{circlocal}(f):\mathrm{isContr}\left(\sum_{x:A} \mathrm{const}_{A, S^1}(x) =_{S^1 \to A} f\right)}$$

## See also

* [[h-set]]
* [[set-level type theory]]

[[!redirects axioms of set truncation]]