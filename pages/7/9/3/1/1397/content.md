
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The __identity natural transformation__ on a [[functor]] $F: C \to D$ is the [[natural transformation]] $id_F: F \to F$ that maps each [[object]] $x$ of $C$ to the [[identity morphism]] $id_{F(x)}$ in $D$. 

The identity natural transformations are themselves the [[identity morphisms]] for [[vertical composition]] of natural transformations in the [[functor category]] $D^C$ and in the [[2-category]] [[Cat]].

One must be aware that when we say that a natural transformation $\alpha_{A}:F(A) \rightarrow G(A)$ is the identity, it doesn't mean only that $F(A)=G(A)$ for every object $A$ but also that $F(f)=G(f)$ for every morphism $f$ ie. that the two functors $F$ and $G$ are equal.

Not taking care of this can lead to redundant definitions  as for [[permutative categories]]. 

## Related concepts

* [[equality]], [[equivalence]]

* [[identity function]], [[identity morphism]]

* [[identity functor]]

* [[identity type]]

* [[identity of indiscernibles]]


[[!redirects identity natural transformations]]

[[!redirects identity transformation]]
[[!redirects identity transformations]]


