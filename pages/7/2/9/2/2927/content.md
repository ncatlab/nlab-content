<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

## Definition

A **cartesian object** in a [[2-category]] with finite [[2-limit|2-products]] is an object $X$ such that the [[diagonal morphism]] $X \to X \times X$ and the unique map $X \to 1$ have [[right adjoints]].

For example, a cartesian object in [[Cat]] is precisely a category with finite [[products]].

## Properties

By making a choice of products, any category with finite products is automatically a [[symmetric monoidal category]] in a canonical way. This fact generalizes to:

+-- {: .num_prop #as_pseudomonoid}
###### Proposition

A cartesian object in a 2-category $C$ with finite 2-products is a symmetric [[pseudomonoid]] in $C$ in a canonical way.

=--

+-- {: .proof}
###### Proof

The idea of the proof is to reduce to the case of Cat using the [[Yoneda lemma for bicategories|2-categorical Yoneda embedding]]. Let $X$ be a cartesian object in $C$. Because 2-functors preserve adjunctions and the 2-Yoneda embedding $C \to [C^{op}, Cat]$, $A \mapsto C(-,A)$ preserves 2-products, $C(-,X)$ is a cartesian object in the 2-category of 2-presheaves on $C$. In particular, since 2-products in this 2-category are computed pointwise, $C(Y,X)$ is a cartesian object in Cat, and hence is canonically a symmetric pseudomonoid in Cat, for each object $Y$ of $C$. Then, by similar reasoning, $C(-,X)$ is a symmetric pseudomonoid in the 2-presheaf 2-category. Finally, because the 2-Yoneda embedding is locally fully faithful and hence locally [[conservative functor|reflects isomorphisms]], $X$ is a symmetric pseudomonoid in $C$.

=--

## References

* Carboni, Kelly, Wood, _A 2-categorical approach to change of base and geometric morphisms I_ (1991) ([Numdam](http://www.numdam.org/item/?id=CTGDC_1991__32_1_47_0)), Section 5: Cartesian objects in $F$ and various morphisms between them

[[!redirects cartesian objects]]

