
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

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{y:B} (\exists x:A.f(x) =_B y) \to (\exists! x:A.f(x) =_B y)$$

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{y:B} \mathrm{isProp}\left(\sum_{x:A}f(x) =_B y\right)$$

## The subtype proposition

Given types $A$ and $B$, the [[subtype]] [[mere proposition]] is defined as the [[bracket type]] of the embedding type:

$$A \subseteq B \coloneqq [A \hookrightarrow B]$$

## See also

* [[embedding]]

* [[subtype]]

* [[injection set]]

* [[object of monomorphisms]]

* [[function type]], [[equivalence type]]

[[!redirects embedding type]]
[[!redirects embedding types]]

[[!redirects type of embeddings]]
[[!redirects types of embeddings]]