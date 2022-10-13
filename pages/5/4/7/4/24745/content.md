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

## Definition

In a [[dependent type theory]] with [[function types]], [[dependent sum types]], and [[identity types]], the **type of fibers** of a function $f:A \to B$ over a term $b:B$ is defined to be the type
$$\mathrm{fiber}_{A, B}(f, b) \coloneqq \sum_{a : A} (f(a) = b)$$
hence the [[dependent sum]] over $A$ of the [[identity type]] on $B$ with $f(a)$ and $b$ [[substitution|substituted]]. 

### Rules for fiber types

If the dependent type theory does not have [[dependent sum types]], it is still possible to define fiber types by adding the formation, introduction, elimination, computation, and uniqueness rules for fiber types

Formation rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B, x:A \vdash f(x) =_B y \; \mathrm{type}}{\Gamma, f:A \to B, y:B \vdash \mathrm{fiber}_{A, B}(f, y) \; \mathrm{type}}$$

Introduction rules for fiber types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B, x:A \vdash b(x):f(x) =_B y \quad \Gamma \vdash a:A \quad \Gamma, f:A \to B, y:B \vdash p:f[a/x] =_B y}{\Gamma, f:A \to B, y:B \vdash (a, b):\mathrm{fiber}_{A, B}(f, y)}$$

Elimination rules for fiber types:
$$\frac{\Gamma, f:A \to B, y:B \vdash z:\mathrm{fiber}_{A, B}(f, y)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma, f:A \to B, y:B \vdash z:\mathrm{fiber}_{A, B}(f, y)}{\Gamma, f:A \to B, y:B \vdash \pi_2(z):f(\pi_1(z)) =_B y}$$

Computation rules for fiber types:
$$\frac{\Gamma, f:A \to B, y:B, x:A \vdash b(x):f(x) =_B b \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\mathrm{fiber}_{A, B} 1}:\pi_1(a, b) =_A a} \qquad \frac{\Gamma, f:A \to B, y:B, x:A \vdash b(x):f(x) =_B y \quad \Gamma \vdash a:A}{\Gamma, f:A \to B, y:B \vdash \beta_{\mathrm{fiber}_{A, B} 2}:\pi_2(a, b) =_{f(\pi_1(a, b)) =_B y} b}$$

Uniqueness rules for fiber types:
$$\frac{\Gamma, f:A \to B, y:B \vdash z:\mathrm{fiber}_{A, B}(f, y)}{\Gamma, f:A \to B, y:B \vdash \eta_{\mathrm{fiber}_{A, B}}:z =_{\mathrm{fiber}_{A, B}(f, y)} (\pi_1(z), \pi_2(z))}$$

## See also

* [[equivalence of types]]
* [[fiber]]
* [[homotopy fiber]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*,
The Univalent Foundations Program, Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

For the corresponding [[Coq]] code  see

* [[Vladimir Voevodsky]], _[Foundations/Generalities/uuo.v](https://github.com/vladimirias/Foundations/blob/master/Generalities/uu0.v)_

[[!redirects fiber type]]
[[!redirects fiber types]]

[[!redirects homotopy fiber type]]
[[!redirects homotopy fiber types]]

[[!redirects type of fibers]]
[[!redirects types of fibers]]

[[!redirects type of homotopy fibers]]
[[!redirects types of homotopy fibers]]