

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

In [[dependent type theories]] with more than one layer of type, function extension types are types which behave like [[function types]] except the [[domain]] is the outer layer  (or equivalent) of type rather than the normal layer of type. 

## Definition

### In dependent type theory with second layer for propositions

In [[dependent type theory]] with a second layer of propositions $\phi \; \mathrm{prop}$, the [[inference rules]] for extension types are given as follows:

Formation rules for extension types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A}{\Gamma \vdash \{A \vert \overline{\phi \to u}\}}$$

Introduction rules for extension types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A \quad \Gamma \vdash v:A \quad \overline{\Gamma, \phi \vdash u \equiv v:A}}{\Gamma \vdash \mathrm{inS}(v):\{A \vert \overline{\phi \to u}\}}$$

Elimination rules for extension types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A \quad \Gamma \vdash v:\{A \vert \overline{\phi \to u}\}}{\Gamma \vdash \mathrm{outS}(v):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A \quad \Gamma \vdash v:\{A \vert \overline{\phi \to u}\}}{\overline{\Gamma, \phi \vdash \mathrm{outS}(v) \equiv u:A}}$$

Computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A \quad \Gamma \vdash v:A}{\Gamma \vdash \mathrm{outS}(\mathrm{inS}(v)) \equiv v:A}$$

Uniqueness rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash \phi \; \mathrm{prop} \quad \Gamma, \phi \vdash u:A \quad \Gamma \vdash v:\{A \vert \overline{\phi \to u}\}}{\Gamma \vdash \mathrm{inS}(\mathrm{outS}(v)) \equiv v:\{A \vert \overline{\phi \to u}\}}$$

### In type theory with shapes

In [[type theory with shapes]], there are three different layers - there are the cube layer and the tope layer, which is [[logic over type theory]] where the cubes are the types and the topes are the propositions in the logic over type theory, and finally there is the type layer, which is a [[dependent type theory]]. 

Shapes are formed in the usual set-builder notation in [[set theory]]: given a cube $I$ and a predicate tope $t:I \vdash \phi$, one could construct the shape $\{t:I \vert \phi\}$. A cofibration in two-level type theory is an inclusion of shapes, which means shapes $\{t:I \vert \phi\}$ and $\{t:I \vert \psi\}$ with a predicate $t:I \vert \phi \vdash \psi$. 

Formation rules for dependent extension types
$$\frac{\{t:I \vert \phi\} \; \mathrm{shape} \quad \{t:I \vert \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \quad \Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi \vert \Phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A}{\Xi \vert \Phi \vert \Gamma \vdash \langle \{t:I \vert \psi\} \to A \vert_a^\phi \rangle \; \mathrm{type}}$$

## Related concepts

* [[dependent extension type]]
* [[function type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* [[Jonathan Sterling]], [[Robert Harper]], *Logical Relations as Types: Proof-Relevant Parametricity for Program Modules*, Journal of the ACM, Volume 68, Issue 6, December 2021, Article No.: 41, pp 1-47. ([doi:10.1145/3474834](https://doi.org/10.1145/3474834), [arXiv:2010.08599](https://arxiv.org/abs/2010.08599))

* [[Daniel Gratzer]], [[Jonathan Sterling]], [[Carlo Angiuli]], [[Thierry Coquand]], [[Lars Birkedal]], *Controlling unfolding in type theory* ([arXiv:2210.05420](https://arxiv.org/abs/2210.05420))

* [[Tesla Zhang]], *Three non-cubical applications of extension types* ([arXiv:2311.05658](https://arxiv.org/abs/2311.05658))

For extension types in [[cubical type theory]], see section 3.5 of:

* [[Carlo Angiuli]], *Computational Semantics of Cartesian Cubical Type Theory*, Ph.D. Thesis, <https://www.cs.cmu.edu/~cangiuli/thesis/thesis.pdf>

[[!redirects extension type]]
[[!redirects extension types]]