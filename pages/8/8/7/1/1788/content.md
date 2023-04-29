

## Idea

The notion of *enriched monoidal category* is a compatible combination of the notions of *[[enriched categories]]* and *[[monoidal categories]]*. The main point is that the [[tensor product]]-[[functor]] on the [[underlying]] [[monoidal category]] is properly an [[enriched functor]] with respect to the [[underlying]] [[enriched category]].

## Definition

### The monoidal 2-category of enriched categories

For $V$ a *[[symmetric monoidal category|symmetric monoidal]]* [[cosmos]],  the [[2-category]] [[VCat]] of $V$-[[enriched categories]] becomes a [[monoidal 2-category]] by declaring the [[tensor product]] $\mathbf{C} \otimes \mathbf{D}$ of a [[pair]] $\mathbf{C}$, $\mathbf{D}$ of $V$-[[enriched categories]] to have

* as [[set]] of [[objects]] the [[cartesian product]] of the given sets of objects:
  
  $$
    Obj(\mathbf{C} \otimes \mathbf{D}) 
      \;\coloneqq\;
    Obj(\mathbf{C}) \times Obj(\mathbf{D})
  $$

* as [[hom-objects]] the [[tensor product]] in $V$ between the given [[hom-objects]]:

  $$
    (\mathbf{C} \otimes \mathbf{D})\big((c,d), (c',d')\big)
    \;\coloneqq\;
    \mathbf{C}(c,c') \otimes \mathbf{D}(d,d')
    \,.
  $$

* [[composition]] obtained by the given composition operations, after using the symmetric [[braiding]] in $V$ to align factors:

  $$
    \array{
      (\mathbf{C} \otimes \mathbf{D})
        \big((c',d'), (c'', d'')\big)
      \otimes
      (\mathbf{C} \otimes \mathbf{D})
        \big((c,d), (c',d')\big)
      &\overset
         {\circ_{\mathbf{C} \otimes \mathbf{D}}}{
        \longrightarrow
        }
       &
      (\mathbf{C} \otimes \mathbf{D})
        \big((c,d), (c'',d'')\big)
      \\
      \mathbf{C}(c',c'') 
        \otimes 
      \mathbf{D}(d',d'')
        \otimes
      \mathbf{C}(c,c') 
        \otimes 
      \mathbf{D}(d,d')
      &\overset{\sim}{\to}&
      \mathbf{C}(c',c'') 
        \otimes 
      \mathbf{C}(c,c') 
        \otimes
      \mathbf{D}(d',d'')
        \otimes 
      \mathbf{D}(d,d')
      &\overset{
        \circ_{\mathbf{C}} \otimes \circ_{\mathbf{D}}
      }{\longrightarrow}&
      \mathbf{C}(c,c'') \otimes \mathbf{D}(d,d'')
    }
  $$

### Enriched monoidal categories

An $V$-enriched monoidal category $\mathbf{C}$ is a [[pseudomonoid]] [[internalization|internal]] to the above monoidal 2-category $V Cat$.

This means mainly that

* $\mathbf{C}$ is a $V$-[[enriched category]]

* whose [[underlying]] category $C$ is equipped with [[monoidal category]]-[[structure]], hence with a [[tensor product]]-[[functor]]

  $$
    \otimes \,\colon\, C \times C \longrightarrow C
  $$

* which is compatibly lifted for each [[pair]] of [[pairs]] of [[objects]] of $C$ to a [[morphisms]] on [[hom-objects]] in $V$:

  $$  
    \otimes_{\mathbf{C}}\big( (c,d),\, (c',c') \big)
    \,\colon\,
    \mathbf{C}(c,c') \otimes \mathbf{C}(d,d')
    \longrightarrow
    \mathbf{C}(c \otimes_C d ,\, c' \otimes_C d')
  $$ 

in a compatible way.


## References

* [[Michael Ching]], *Bar constructions for topological operads and the Goodwillie derivatives of the identity*, Geom. Topol. **9** (2005) 833-934 &lbrack;[arXiv:math/0501429](https://arxiv.org/abs/math/0501429), [doi:10.2140/gt.2005.9.833](http://dx.doi.org/10.2140/gt.2005.9.833)&rbrack;



* [[Rune Haugseng]], [MO:a/315075](https://mathoverflow.net/a/315075/381)

Regarded as [[pseudo-monoids]] in the  

\begin{example}
\label{BorelModelStructureOnSimplicialGroupActions}


It follows that for $\mathcal{X} \,\in\, sSet\text{-}Grpd$ a [[simplicial groupoid]] with any set $\pi_0(\mathcal{X})$ of [[connected components]], the projective model structure of simplicial functors over it is the [product model structure](model+category#ProductModelStructure) of the [[Borel model structures]] of [[simplicial group actions]], one for each connected component:
\end{example}


$$
  \begin{array}{l}
   Hom\big(
    (p_X)^\ast
    \mathscr{V}_\ast
    ,\,
    \mathscr{W}_{X}
  \big)
  \\
  \;\simeq\;
   Hom\big(
    \mathbb{1}_{X}
    \otimes
    \mathscr{V}_{\ast}
    ,\,
    \mathscr{W}_X
  \big)
  \end{array}
$$



$$
  \array{ 
    \mathcal{X}_i
    \times
    \mathcal{Y}
    &
    \overset{\; pr_{\mathcal{X}_i} \;}{\longrightarrow}
    &
    \mathcal{X}_i
    \\
    \mathllap{{q}^{\mathcal{X}_i} \times id_{\mathcal{Y}}}
    \Big\downarrow
    && 
    \Big\downarrow
    \mathrlap{{}^{ q^{\mathcal{X}_i} }}
    \\
    \underset{\underset{j \in I}{\longrightarrow}}{lim}
    \mathcal{X}_j 
       \times 
    \mathcal{Y}
    &
    \underset
      {pr_{\underset{\longrightarrow}{lim}\mathcal{X}}}  
      {\longrightarrow}
    &
    \underset{\underset{j \in I}{\longrightarrow}}{lim} \mathcal{X}_j
  }
$$


$$
  \begin{array}{ll}
  \Big(
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \mathscr{V}(i)_{\mathcal{X}_i}
  \Big)
  \boxtimes 
  \mathscr{W}_{\mathcal{Y}}
  \\
  \;\simeq\;
  \left(
  \big(
    \underset{\longrightarrow}{\lim}
    q^{\mathcal{X}}_!\mathscr{V}
  \big)_{\underset{\longrightarrow}{\lim}\mathcal{X}}
  \right)
  \boxtimes
  \mathscr{W}_{\mathcal{Y}}
  &
  \text{colimit in Groth. constr.}
  \\
  \;\simeq\;
  \Big(
    \big(
    (pr_{\underset{\longrightarrow}{lim}\mathcal{X}})^\ast
    (
      \underset{\longrightarrow}{\lim}
      q^{\mathcal{X}}_!\mathscr{V}
    )
    \big)
    \,\otimes\,
    \big(
    (pr_{\mathcal{Y}})^\ast
    \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{def. of external tensor}
  \\
  \;\simeq\;
  \Big(
    \big(
      \underset{\longrightarrow}{\lim}
      (pr_{\underset{\longrightarrow}{lim}\mathcal{X}})^\ast
      q^{\mathcal{X}}_!
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{pullback preserves colimits}
  \\
  \;\simeq\;
  \Big(
    \big(
      \underset{\longrightarrow}{\lim}
      (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{Beck-Chevalley}
  \\
  \;\simeq\;
  \bigg(
    \underset{\longrightarrow}{\lim}
    \Big(
    \big(
      (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
    \Big)
  \bigg)_{
    \underset{\longrightarrow}{\lim}
    \big(
    \mathcal{X}
    \times
    \mathcal{Y}
    \big)
  }
  &
  \text{products preserve colimits}
  \\
  \;\simeq\;
  \bigg(
    \underset{\longrightarrow}{\lim}
    (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
    \Big(
    \big(
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
    \Big)
  \bigg)_{
    \underset{\longrightarrow}{\lim}
    \big(
    \mathcal{X}
    \times
    \mathcal{Y}
    \big)
  }
  &
  \text{projection formula}
  \\
  \;\simeq\;
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \bigg(
  \Big(
    \big(
      (pr_{\mathcal{X}_i})^\ast \mathscr{V}(i)
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
  \Big)_{ 
    \underset{\longrightarrow}{lim} 
    (
    \mathcal{X}
    \times
    \mathcal{Y}
    )
  } 
  \bigg)
  &
  \text{colimit in Groth. constr.}
  \\
  \;\simeq\;
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \Big(
    \mathscr{V}(i)_{\mathcal{X}_i}
    \,\boxtimes\,
    \mathscr{W}_{\mathcal{Y}}
  \Big)
  &
  \text{def of external tensor}
  \end{array}
$$



