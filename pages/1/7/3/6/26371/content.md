
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

The analogue in [[dependent type theory]] of the concept of [[injection]] in [[set theory]], [[embedding of topological spaces]] in [[topology]], and [[embedding]] in [[category theory]]. 

This is similar to [[equivalence of types]], which are the analogues in dependent type theory of the concept of [[bijection]] in [[set theory]], [[homeomorphism]] in [[topology]], and [[isomorphism]] in [[category theory]]. 

## Definition

Given types $A$ and $B$, a function $f:A \to B$ is an **embedding** if one of the following equivalent conditions holds of $f$:

* for all $x:A$ and $y:A$, [[function application to identifications|application]] of the function $f$ to identifications between $x$ and $y$ is an equivalence of types;

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\mathrm{ap}_f(x, y))$$

* for all $y:B$, the fiber of $f$ at $y$ is a [[mere proposition]]

$$\mathrm{isEmbedding}(f) \coloneqq \prod_{y:B} \mathrm{isProp}\left(\sum_{x:A}f(x) =_B y\right)$$

## Properties

### Relation to subtypes

Given a [[type of propositions]] $\mathrm{Prop}$ and a [[material subtype]] $P:A \to \mathrm{Prop}$, the corresponding [[structural subtype]] of $A$ is defined by 
$$\sum_{x:A} x \in P$$
and the embedding is given by the first projection function 
$$\pi_1:\left(\sum_{x:A} x \in P\right) \to A$$
with the witness that $\pi_1$ is an embedding given by the fact that the membership relation $x \in P$ is a proposition for all elements $x:A$ and material subtypes $P:A \to \mathrm{Prop}$. 

## Related concepts

* [[embedding type]]

* [[injection]], [[embedding of topological spaces]], [[embedding of smooth manifolds]], [[embedding]]

* [[equivalence of types]]

* [[subtype]], [[predicate]]

## References

For embeddings in [[dependent type theory]], see section 11.4 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects embedding of types]]
[[!redirects embeddings of types]]

[[!redirects embedding in type theory]]
[[!redirects embeddings in type theory]]