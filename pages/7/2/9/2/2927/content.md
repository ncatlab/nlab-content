+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

## Definition

A **cartesian object** in a [[2-category]] with finite [[2-limit|2-products]] is an object $X$ such that the [[diagonal morphism]] $X \to X \times X$ and the unique map $X \to 1$ have [[right adjoints]].

For example, a cartesian object in [[Cat]] is precisely a category with finite [[products]].

## Properties

Any category with finite products becomes a [[symmetric monoidal category]] by making a choice of products. The symmetric monoidal structure is canonical in the sense that for any other choice of products, there is a canonical isomorphism between the two symmetric monoidal categories. Specifically, there is an invertible strong symmetric monoidal functor whose underlying functor is the identity and whose structure maps are given by the universal property of products.

This fact generalizes to cartesian objects:

+-- {: .num_prop #as_pseudomonoid}
###### Proposition

A cartesian object in a 2-category $C$ with finite 2-products is a symmetric [[pseudomonoid]] in $C$ in a canonical way.

=--

+-- {: .proof}
###### Proof

The idea of the proof is to reduce to the case of Cat using the [[Yoneda lemma for bicategories|2-categorical Yoneda embedding]].

Let $X$ be a cartesian object in $C$, and make a choice of  right adjoints to the diagonal and terminal maps. Because 2-functors preserve adjunctions and the 2-Yoneda embedding $C \to [C^{op}, Cat]$, $A \mapsto C(-,A)$ preserves 2-products, $C(-,X)$ is a cartesian object with a choice of right adjoints in the 2-category of 2-presheaves on $C$. In particular, since 2-products in this 2-category are computed pointwise, $C(Y,X)$ is a cartesian object with a choice of right adjoints in Cat, and hence has the structure of a symmetric pseudomonoid in Cat, for each object $Y$ of $C$. Then, by similar reasoning, $C(-,X)$ is a symmetric pseudomonoid in the 2-presheaf 2-category. Finally, because the 2-Yoneda embedding is locally fully faithful and in particular locally [[conservative functor|reflects isomorphisms]], $X$ is a symmetric pseudomonoid in $C$.

For any other choice of rights adjoints for the cartesian object $X$, there are unique invertible 2-cells between them that commute with the units and counits of the adjunctions. Threading these through the 2-Yoneda embedding as before, the 2-cells define the comparison iso-cells of a strong morphism of symmetric pseudomonoids whose underlying morphism between the carrier objects is the identity.

=--

## References

* [[Jacques Penon]], _Sous-categorie classifiee d’une 2-categorie_ (1974), [[CRAS]]

* [[Aurelio Carboni]], [[Max Kelly]], [[Richard Wood]], _A 2-categorical approach to change of base and geometric morphisms I_ (1991) ([Numdam](http://www.numdam.org/item/?id=CTGDC_1991__32_1_47_0)), Section 5: Cartesian objects in $F$ and various morphisms between them

[[!redirects cartesian objects]]

[[!redirects cocartesian object]]
[[!redirects cocartesian objects]]
