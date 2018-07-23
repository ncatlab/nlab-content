
+-- {: .num_prop #FixedPointEquivalenceOfAnAdjunction}
###### Proposition
**([[fixed point equivalence of an adjunction]])**

Let

$$
  \mathcal{D}
    \underoverset
      {\underset{ R }{\longrightarrow}}
      {\overset{ L }{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  \mathcal{C}
$$

be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Say that 

1. an [[object]] $c \in \mathcal{C}$ is a _[[fixed point of an adjunction|fixed point of the adjunction]]_ if its  [[adjunction unit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) is an [[isomorphism]] (Def. \ref{Isomorphism})

   $$
     c \underoverset{\simeq}{\eta_c}{\longrightarrow} R L (c)
   $$

   and write 

   $$
     \mathcal{C}_{fix} \hookrightarrow \mathcal{C}
   $$

   for the [[full subcategory]] on these fixed objects (Example \ref{FullSubcategoryOnClassOfObjects})


1. an [[object]] $d \in \mathcal{D}$ is a _[[fixed point of an adjunction|fixed point of the adjunction]]_ if its  [[adjunction counit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) is an [[isomorphism]] (Def. \ref{Isomorphism})

   $$
    L R(d) \underoverset{\simeq}{\epsilon_d}{\longrightarrow}
   $$

   and write 

   $$
     \mathcal{D}_{fix} \hookrightarrow \mathcal{D}
   $$

   for the [[full subcategory]] on these fixed objects (Example \ref{FullSubcategoryOnClassOfObjects})


Then the [[adjunction]] ([[corestriction|co]]-)[[restriction|restrics]] to an [[adjoint equivalence]] (Def. \ref{AdjointEquivalenceOfCategories}) on these [[full subcategories]] of [[fixed points]] sprign 

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

1. for $c \in \mathcal{C}_{fix} \hookrightarrow \mathcal{C}$ we have that $\eta_{R(d)}$ is an [[isomorphism]];

1. for $d \in \mathcal{D}_{fix} \hookrightarrow \mathcal{D}$ we have that $\epsilon_{L(c)}$ is an [[isomorphism]].

For the first case we claim that $R(\eta_{d})$ provides an [[inverse morphism|inverse]]: by the [[triangle identity]] (eq:TriangleIdentities) it is a [[right inverse]], but by assumption it is itself an [[invertible morphism]], this implies that $\eta_{R(d)}$ is an isomorphism.

The second claim is [[formal duality|formally dual]].

=--
