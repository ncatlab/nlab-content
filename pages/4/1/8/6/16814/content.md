
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

The [[equivalences of categories]] that arise from fixed points of adjunctions this way are often known as [[dualities]]. Examples include _[[Pontrjagin duality]]_, _[[Gelfand duality]]_, _[[Stone duality]]_, and the _[[Isbell duality]]_ between [[commutative rings]] and [[affine schemes]] (see [Porst-Tholen 91](#PorstTholen91)).

## Definition


+-- {: .num_prop #FixedPointEquivalenceOfAnAdjunction}
###### Proposition
**(fixed point equivalence of an adjunction)**

Let

$$
  \mathcal{D}
    \underoverset
      {\underset{ R }{\longrightarrow}}
      {\overset{ L }{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  \mathcal{C}
$$

be a pair of [[adjoint functors]]. Say that 

1. an [[object]] $c \in \mathcal{C}$ is a _fixed point of the adjunction_ if its  [[adjunction unit]] is an [[isomorphism]]

   $$
     c \underoverset{\simeq}{\eta_c}{\longrightarrow} R L (c)
   $$

   and write 

   $$
     \mathcal{C}_{fix} \hookrightarrow \mathcal{C}
   $$

   for the [[full subcategory]] on these fixed objects;


1. an [[object]] $d \in \mathcal{D}$ is a _fixed point of the adjunction_ if its  [[adjunction counit]] is an [[isomorphism]]

   $$
    L R(d) \underoverset{\simeq}{\epsilon_d}{\longrightarrow} d
   $$

   and write 

   $$
     \mathcal{D}_{fix} \hookrightarrow \mathcal{D}
   $$

   for the [[full subcategory]] on these fixed objects.


Then the [[adjunction]] ([[corestriction|co]]-)[[restriction|restrics]] to an [[adjoint equivalence]] on these [[full subcategories]] of [[fixed points]]:

$$
  \mathcal{D}_{fix}
    \underoverset
      {\underset{ R }{\longrightarrow}}
      {\overset{ L }{\longleftarrow}}
      {\phantom{A}\phantom{{}_{\bot}}\simeq_{\bot}\phantom{A}}
  \mathcal{C}_{fix}
$$


=--


+-- {: .proof}
###### Proof

It is sufficient to see that the functors ([[corestriction|co-]])[[restriction|restrict]] as claimed, for then the restricted adjunction unit/counit are [[isomorphisms]] by definition, and hence exhibit an [[adjoint equivalence]].

Hence we need to show that 

1. for $c \in \mathcal{C}_{fix} \hookrightarrow \mathcal{C}$ we have that $\epsilon_{L(c)}$ is an [[isomorphism]];

1. for $d \in \mathcal{D}_{fix} \hookrightarrow \mathcal{D}$ we have that $\eta_{R(d)}$ is an [[isomorphism]].

For the first case we claim that $L(\eta_{c})$ provides an [[inverse morphism|inverse]]: by the [[triangle identity]] (eq:TriangleIdentities) it is a [[right inverse]], but by assumption it is itself an [[invertible morphism]], which implies that $\epsilon_{L(c)}$ is an isomorphism.

The second claim is [[formal duality|formally dual]].

=--


## Properties

* If the adjunction is [[idempotent adjunction|idempotent]], then the fixed objects in $\mathcal{C}$ are precisely those of the form $G d$, and dually the fixed objects in $\mathcal{D}$ are those of the form $F c$.  Indeed, this is essentially the definition of an idempotent adjunction.

## Examples
 {#Examples}

### Gelfand duality
 {#GelfandDuality}

[[Gelfand duality]] is (a further restriction of) the fixed point equivalence of the adjunction between [[compactly generated topological spaces|compactly generated]] [[Hausdorff spaces]] and [[topological algebras]] over the [[complex numbers]], given by using the [[complex numbers]] as [[dualizing object]] ([Porst-Tholen 91, section 4-c](#PorstTholen91)).

## Related concepts

* [[nucleus of a profunctor]]

## References

* {#PorstTholen91} [[Hans-E. Porst]], [[Walter Tholen]], _Concrete Dualities_ in H. Herrlich, [[Hans-E. Porst]] (eds.) _Category Theory at Work_, Heldermann Verlag 1991 ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf))


[[!redirects fixed points of an equivalence]]

[[!redirects center of an adjunction]]
[[!redirects centers of adjunctions]]

[[!redirects fixed point equivalence of an adjunction]]
[[!redirects fixed point equivalences of adjunctions]]
