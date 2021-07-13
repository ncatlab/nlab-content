
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

Diagram chasing is a common technique in [[homological algebra]] for proving properties of and constructing morphisms in [[abelian category|abelian categories]], where one traces elements in various ways around [[commutative diagram|commutative diagrams]].

## Examples

Many basic lemmas in homological algebra, such as the [[five lemma]], the [[3x3 lemma]] and the [[snake lemma]], are typically proven by diagram chases. See for instance the proof at _[[five lemma]]_ or any book on homological algebra.

The [[salamander lemma]] can sometimes be used to give more conceptual proofs.

## Diagram chases in general abelian categories

There are at least five approaches to performing diagram chases in general abelian categories (not assumed to be [[concrete category|concrete]] like [[Ab]] or $R$[[Mod]]):

1. Directly use the universal properties of the objects involved ([[kernel|kernels]], [[cokernel|cokernels]] etc.).
1. Use equivalence classes of [[generalized element|generalized elements]] to mimic naive (element-based) proofs, as detailed at _[[element in an abelian category]]_. These can only be used to show properties of already-given morphisms and not to construct morphisms (for example the [[connecting homomorphism]] of a short exact sequence) by giving their action on elements.
1. Use genuine generalized elements, see _[[element in an abelian category]]_. With these, the naive way of constructing morphisms $A \to B$ (first showing that for every $a \in A$ there exists a certain $b \in B$, then showing that this is independent of any choices made) carries over to the general setting.
1. Interpret constructive element-based proofs written in the fragment of [[regular logic]] using categorical semantics, see _[[internal logic]]_. The naive way of constructing morphisms works because the "axiom of unique choice" is valid in abelian categories (see [Johnstone, Prop. D1.3.12](#Johnstone)).
1. Use the [[Freyd-Mitchell embedding theorem]].



   
## Related concepts

* [[salamander lemma]]
* [[element in an abelian category]]
* [[internal language]]
* [[Freyd-Mitchell embedding theorem]]  
* [[diagram chasing lemmas - contents]]

## References

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ {#Johnstone}

* [[Daniel Murfet]], _Diagram Chasing in Abelian Categories_ (2006) ([pdf](http://therisingsea.org/notes/DiagramChasingInAbelianCategories.pdf))

* {#Bergman} [[George Bergman]], _On diagram-chasing in double complexes_ ([arXiv:1108.0958](http://arxiv.org/abs/1108.0958))
 

[[!redirects diagram chasing lemmas]]

[[!redirects diagram chase]]
[[!redirects diagram chases]]

