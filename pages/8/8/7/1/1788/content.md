**Prop.** Let $\mathbb{T}$ be of presheaf type. Then $Set[\mathbb{T}]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]$.

Proof. By assumption $Set[\mathbb{T}]\simeq [\mathcal{C}, Set]$. Since $[\mathcal{C},Set]\simeq [\hat{\mathcal{C}}, Set]$ (by Elephant, p.10) we can assume that $\mathcal{C}$ is Cauchy complete.

We have:

* $Ind\text{-}\mathcal{C}\simeq Flat(\mathcal{C}^{op}, Set)$ (by Elephant, p.723, or Caramello, p.198)

* $(Ind\text{-}\mathcal{C})_{fp}\simeq \mathcal{C}$ (by Elephant 4.2.2.(iii), p.724)

* $\mathbb{T}\text{-}Mod(Set)\simeq Flat(\mathcal{C}^{op}, Set)$ (from Diaconescu’s theorem).

Whence $(Ind\text{-}\mathcal{C})_{fp}\simeq (\mathbb{T}\text{-}Mod (Set))_{fp} =\mathbb{T}\text{-}Mod_{fp}(Set)\simeq \mathcal{C}$ and, accordingly, $[\mathcal{C},Set]]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]$. $\qed$
