
### Slicing of adjoint functors
 {#OnSlices}

+-- {: .num_prop #SliceAdjoints}
###### Proposition

Let

$$
  (L \dashv R) 
  \;\colon\; 
   \mathcal{D} 
   \underoverset
    {\underset{\;\;\;R\;\;\;}{\longrightarrow}}
    {\overset{\;\;\;L\;\;\;}{\longleftarrow}}
    {\bot}
  \mathcal{C}
$$

be a pair of [[adjoint functors]] ([[adjoint (∞,1)-functors|adjoint ∞-functors]]), where the [[category]] ([[(∞,1)-category|∞-category]]) $\mathcal{C}$ has all [[pullbacks]] ([[homotopy pullbacks]]). 

Then for every [[object]] $X \in \mathcal{C}$ there is induced a pair of adjoint functors between the [[slice categories]] ([[slice (∞,1)-categories|slice ∞-categories]])

$$
  (L/X \dashv R/X) 
  \;\colon\; 
  \mathcal{D}/(L X) 
  \underoverset
    {\underset{\;\;R/X\;\;}{\longrightarrow}}
    {\overset{\;\;L/X\;\;}{\longleftarrow}}
    {\bot}
  \mathcal{C}/X
  \mathrlap{\,,}
$$

where:

* $L/X$ is the evident induced functor;

* $R/X$ is the [[composition|composite]]

  $$
    R/X   
    \;\colon\; 
    \mathcal{D}/{L X} 
      \overset{\;\;R\;\;}{\longrightarrow} 
    \mathcal{C}/{(R L X)} 
      \overset{\;\;\eta_{X}^*\;\;}{\longrightarrow}
    \mathcal{C}/X
  $$

  of the evident functor induced by $R$ with the (homotopy) pullback along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $X$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.2.5.1]].
