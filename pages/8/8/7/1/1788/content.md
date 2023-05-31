
\begin{proposition}
  The category of [[sSet]]-[[enriched groupoids]] is [[cartesian closed category|cartesian closed]].
\end{proposition}
\begin{proof}
The ambient category of [[sSet-enriched categories]] is cartesian closed (as any [[category of enriched categories|category of $\mathcal{V}$-categories]] for [[cartesian closed category|cartesian closed]] [[complete category|complete]] [[cosmos]] $\mathcal{V}$), given by forming [[enriched product categories]] and [[enriched functor categories]].

Therefore we just need to check that for $\mathbf{D},\,\mathbf{C} \,\in\, sSet\text{-}Grpd$ also the $sSet$-[[enriched product category]] $\mathbf{C} \times \mathbf{D}$ and the $sSet$-[[enriched functor category]] $[\mathbf{D},\,\mathbf{C}]$ are in fact [[enriched groupoids]]. 

For the product this is immediate, the [[inverse morphism|inversion]]-operation is given factorwise.

To see the statement for the [[internal hom]], write $\mathbf{I}_S$ for the [[sSet-enriched category]] with set objects $\{0,1\}$ and [[hom objects]] given by:

* $\mathbf{I}_{S}(0,0) \,\coloneqq\, \ast$

* $\mathbf{I}_{S}(1,1) \,\coloneqq\, \ast$

* $\mathbf{I}_{S}(1,0) \,\coloneqq\, \varnothing$

* $\mathbf{I}_{S}(0,1) \,\coloneqq\, S$

(whence there is no non-trivial [[composition]] to be defined).

Now for $n \in \mathbb{N}$ the $sSet$-[[enriched functors]]

$$
  \mathbf{I}_{\Delta[n]} 
    \longrightarrow 
  [\mathbf{D},\,\mathbf{C}]
$$

are in [[bijection]] with the $(n+1)$-morphisms in $[\mathbf{D},\,\mathbf{C}]$, and we need to exhibit an inversion operation on these.

But by the [[cartesian closed monoidal category|cartesian closure]] of [[VCat|sSet Cat]] these are also in natural bijection to enriched functors of the form
$$
  \mathbf{D}
  \times
  \mathbf{I}_{\Delta[n]}
  \longrightarrow
  \mathbf{C}
$$
which are manifestly a simplicial diagram of [[natural transformations]] between the restrictions $\mathbf{D} \times \{0\} \to \mathbf{C}$ and $\mathbf{D} \times \{1\} \to \mathbf{C}$. The corresponding system of inverse natural transformations corresponds to the inverse $n+1$-morphism that we are after.
\end{proof}

