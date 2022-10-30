
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While a (left or right) [[adjoint]] to a [[functor]] may be understood as the best approximation (from one side or the other) of a possibly non-existent [[inverse]], any pair of [[adjoint functors]] restricts to an [[equivalence of categories]] on [[subcategories]]. These subcategories are sometimes known as the _center_ of the adjunction, their objects are sometimes known as the _fixed points_ of the adjunction.

The [[equivalences of categories]] that arise from fixed points of adjunctions this way are often known as [[dualities]]. Examples include _[[Pontrjagin duality]]_, _[[Gelfand duality]]_, _[[Stone duality]]_, and the _[[Isbell duality]]_ between [[commutative rings]] and [[affine schemes]].

## Definition

If $F \colon \mathcal{D} \longrightarrow \mathcal{C}$ is [[left adjoint]] to $G  \colon \mathcal{C} \longrightarrow \mathcal{D}$, then we take the [[fixed points of the endofunctor]] $F G$ to be those [[objects]] of $\mathcal{C}$ on which the [[counit of an adjunction|counit]] $\epsilon$ is an [[isomorphism]], and take the fixed points of $G F$ to be those objects of $\mathcal{D}$ on which the [[unit of an adjunction|unit]] $\eta$ is an isomorphism. The [[triangle identities]] then imply that $F$ and $G$ induce an [[equivalence of categories]] between the [[full subcategories]] of fixed points of $F G$ and the fixed points of $G F$. 

## Properties

* If the adjunction is [[idempotent adjunction|idempotent]], then the fixed objects in $\mathcal{C}$ are precisely those of the form $G d$, and dually the fixed objects in $\mathcal{D}$ are those of the form $F c$.  Indeed, this is essentially the definition of an idempotent adjunction.

## Examples
 {#Examples}

### Gelfand duality
 {#GelfandDuality}

[[Gelfand duality]] is the fixed point equivalence of an adjunction between [[compactly generated topological spaces|compactly generated]] [[Hausdorff spaces]] and [[topological algebras]] over the [[complex numbers]], given by using the [[complex numbers]] as [[dualizing object]] ([Porst-Tholen 91, section 4-c](#PorstTholen91)).

## Related concepts

* [[nucleus of a profunctor]]

## References

* {#PorstTholen91} [[Hans-E. Porst]], [[Walter Tholen]], _Concrete Dualities_ in H. Herrlich, [[Hans-E. Porst]] (eds.) _Category Theory at Work_, Heldermann Verlag 1991 ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf))


[[!redirects fixed points of an equivalence]]

[[!redirects center of an adjunction]]
[[!redirects centers of adjunctions]]

[[!redirects fixed point equivalence of an adjunction]]
[[!redirects fixed point equivalences of adjunctions]]
