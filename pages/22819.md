
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

Then for every [[object]] $c \in \mathcal{C}$ there is induced a pair of adjoint functors between the [[slice categories]] ([[slice (∞,1)-categories|slice ∞-categories]])

$$
  (L_{/c} \dashv R_{/c}) 
  \;\colon\; 
  \mathcal{D}_{/L(c)}
  \underoverset
    {\underset{\;\;R_{/c}\;\;}{\longrightarrow}}
    {\overset{\;\;L_{/c}\;\;}{\longleftarrow}}
    {\bot}
  \mathcal{C}_{/c}
  \mathrlap{\,,}
$$

where:

* $L_{/c}$ is the evident induced functor (applying $L$ to the entire triangle [[diagrams]] in $\mathcal{C}$ which represent the morphisms in $\mathcal{C}_{/c}$);

* $R_{/c}$ is the [[composition|composite]]

  $$
    R_{/c} 
      \;\colon\; 
    \mathcal{D}_{/{L(c)}} 
      \overset{\;\;R\;\;}{\longrightarrow} 
    \mathcal{C}_{/{(R \circ L(c))}} 
      \overset{\;\;\eta_{c}^*\;\;}{\longrightarrow}
    \mathcal{C}_{/c}
  $$

  of 

  1. the evident functor induced by $R$;

  1. the ([[homotopy pullback|homotopy]]) [[pullback]] along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $c$.

=--

(In the generality of [[(∞,1)-category theory]] this appears as [[Higher Topos Theory|HTT, prop. 5.2.5.1]])

