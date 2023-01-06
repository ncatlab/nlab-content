
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In the same way that one could define [[equivalence types]] as types of [[one-to-one correspondences]] and [[function types]] as types of [[anafunctions]], one could define correspondence types as types of [[correspondences]]. 

Correspondences are [[type families]] $x\colon A, y \colon B \vdash R(x, y) \; \mathrm{type}$. From every correspondence, one could derive the [[multivalued partial function]] 
$$x:A, p:\sum_{y:B} R(x, y) \vdash f(x, p):B$$
and for every type family $x:A \vdash P(x)$ and every [[multivalued partial function]] $x:A, p:P(x) \vdash f(x, p):B$, one could define the [[correspondence]] $x:A, y:B \vdash R(x, y)$ as
$$R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$$

## Rules for correspondence types

The rules for correspondence types are as follows:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{Corr}(A, B) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:\mathrm{Corr}(A, B), x:A, y:B \vdash \mathcal{C}_{A, B}(f, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x) \vdash f(x, p):B}{\Gamma \vdash (x, p) \mapsto f(x, p):\mathrm{Corr}(A, B)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x) \vdash f(x, p):B}{\Gamma, x:A, p:P(x) \vdash \alpha(x, p):\mathcal{C}_{A, B}((x, p) \mapsto f(x, p), x, f(x, p))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type}}{\Gamma, f:\mathrm{Corr}(A, B), x:A, p:P(x) \vdash \mathrm{ev}(f, x, p):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type}}{\Gamma, f:\mathrm{Corr}(A, B), x:A, p:P(x) \vdash \beta(f, x, p):\mathcal{F}_{A, B}(f, x, \mathrm{ev}(f, x, p))}$$

## See also

* [[correspondence]]
* [[function type]], [[dependent function type]]
* [[equivalence type]]
* [[partial function type]]

[[!redirects correspondence type]]
[[!redirects correspondence types]]