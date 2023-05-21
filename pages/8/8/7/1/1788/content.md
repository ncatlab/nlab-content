
\begin{example}
With respect to any [[bifunctor]] $\otimes \,\colon\, \mathcal{C} \times \mathcal{C} \to \mathcal{C}$, the pushout-product with with an [[identity morphism]] is an identity morphim:
$$
  f \widehat{\otimes} id
  \;\simeq\;
  id
  \;\;\;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;\;\;
  id \,\widehat{\otimes}\, g
  \;\simeq\;
  id
  \,.
$$
This is because the defining pushout-diagram, say in the first case, now  looks like this:
\begin{tikzcd}
  X \otimes Y
  \ar[r, "{ \mathrm{id} }"{description}]
  \ar[d, "{ f \otimes \mathrm{id} }"{description}]
  \ar[dr, phantom, "{\scalebox{.6}{(po)}}"]
  &
  X \otimes Y
  \ar[d, "{ f \otimes \mathrm{id} }"{description}]
  \ar[
    ddr, 
    bend left=15, 
    "{ f \otimes \mathrm{id} }"{description}
  ]
  \\
  X' \otimes Y
  \ar[r, "{ \mathrm{id} }"{description}]
  \ar[drr, bend right=15, "{ \mathrm{id} }"{description}]
  &
  X' \otimes Y
  \ar[dr, dashed, "{ \mathrm{id} }"{description}]
  \\  
  & & X' \otimes Y
\end{tikzcd}
because the top morphism is an identity morphism by assumption, so that also its pushout is given by an identity, as shown.

The analogous argument applies in the other variable.
\end{example}


