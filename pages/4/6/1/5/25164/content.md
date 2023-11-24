
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

In dependent type theory, the **embedding type** between two types $A$ and $B$ is the type of [[embeddings]], the type of functions $f:A \to B$ such that 

$$A \hookrightarrow B \coloneqq \sum_{f:A \to B} \mathrm{isEmbedding}(f)$$

where the type $\mathrm{isEmbedding}(f)$ could be defined as

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{x:A} \prod_{y:A} \prod_{q:f(x) =_B f(y)} \exists! p:x =_A y.ap_f(x, y, p) =_{f(x) =_B f(y)} q$$

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{y:B} \prod_{x:A} \prod_{z:f(x) =_B y} \exists! x:A.f(x) =_B y$$

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{y:B} \mathrm{isProp}\left(\sum_{x:A}f(x) =_B y\right)$$

### Rules for embedding types

#### As functions whose applications to identities have contractible fibers

Let us assume the [[dependent type theory]] has [[identity types]], [[dependent identity types]] and [[uniqueness quantifiers]], but does not have [[function types]] or [[dependent function types]] (as in some versions of [[predicative mathematics]]). Then the [[natural deduction]] rules for embedding types is given by:

Formation rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, x:A, y:A, q:f(x) =_B f(y) \vdash u(x, y, q):\exists! p:x =_A y.ap_f(x, y, p) =_{f(x) =_B f(y)} q}{\Gamma \vdash \mathrm{embed}(f, u):A \simeq B}$$

Elimination rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B, x:A \vdash \mathrm{ev}(f, x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B, x:A, y:A, q:f(x) =_B f(y) \vdash \mathrm{uniqact}(f, x, y, q):\exists! p:x =_A y.ap_f(x, y, p) =_{f(x) =_B f(y)} q}$$

Computation rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, x:A, y:A, q:f(x) =_B f(y) \vdash u(x, y, q):\exists! p:x =_A y.ap_f(x, y, p) =_{f(x) =_B f(y)} q}{\Gamma, x:A \vdash \beta_{A \simeq B}^{\mathrm{ev}}(x):\mathrm{ev}(\mathrm{embed}(f, u), x) =_B f(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, x:A, y:A, q:f(x) =_B f(y) \vdash u(x, y, q):\exists! p:x =_A y.ap_f(x, y, p) =_{f(x) =_B f(y)} q}{\Gamma, x:A, y:A, q:f(x) =_B f(y) \vdash \beta_{A \simeq B}^{\mathrm{uniq}}(x, y, q):\mathrm{uniqact}(\mathrm{embed}(f, u), x, y, q) =_{\exists! p:x =_A y.(-) =_{f(x) =_B f(y)} q}^{\beta_{A \simeq B}^{\mathrm{ev}}(x)} u(x, y, q)}$$

Uniqueness rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B \vdash \eta_{A \simeq B}(f):\mathrm{embed}(\mathrm{ev}(f), \mathrm{uniqact}(f)) =_{A \simeq B} f}$$

#### As functions with propositional fibers

Let us assume the [[dependent type theory]] has [[identity types]], [[dependent identity types]], and [[uniqueness quantifiers]]. Then the [[natural deduction]] rules for embedding types is given by:

Formation rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B, x:A, z:f(x) =_B y \vdash p(y, x, z):\exists!x:A.f(x) =_B y}{\Gamma \vdash \mathrm{embed}(f, p):A \simeq B}$$

Elimination rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B, x:A \vdash \mathrm{ev}(f, x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B, y:B, x:A, z:f(x) =_B y \vdash \mathrm{atmostone}(f, y, x, z):\exists!x:A.f(x) =_B y}$$

Computation rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B, x:A, z:f(x) =_B y \vdash p(y, x, z):\exists!x:A.f(x) =_B y}{\Gamma, x:A \vdash \beta_{A \simeq B}^{\mathrm{ev}}(x):\mathrm{ev}(\mathrm{embed}(f, p), x) =_B f(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B, x:A, z:f(x) =_B y \vdash p(y, z):\exists!x:A.f(x) =_B y}{\Gamma, y:B, x:A, z:f(x) =_B y \vdash \beta_{A \simeq B}^{\mathrm{atmostone}}(y, x, z):\mathrm{atmostone}(\mathrm{embed}(f, p), y, x, z) =_{\exists!x:A.(-) =_B y}^{\beta_{A \simeq B}^{\mathrm{ev}}(x)} p(y, x, z)}$$

Uniqueness rules for embedding types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \simeq B \vdash \eta_{A \simeq B}(f):\mathrm{embed}(\mathrm{ev}(f), \mathrm{atmostone}(f)) =_{A \simeq B} f}$$


## See also

* [[embedding of types]]

* [[injection set]]

* [[object of monomorphisms]]

* [[function type]], [[equivalence type]]

[[!redirects embedding type]]
[[!redirects embedding types]]

[[!redirects type of embeddings]]
[[!redirects types of embeddings]]