
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Let $\mathcal{C}$ be any [[small category]].

### Over a representable
 {#IdeaOverARepresentable}

For $X \,\in\, \mathcal{C}$ an [[object]], the [[category of presheaves]] $PSh\big( \mathcal{C}_{/X}\big)$ on the [[slice category]] $\mathcal{C}_{/X}$ is [[equivalence of categories|equivalent]] to the [[slice category|slice]] $PSh(\mathcal{C})_{/X}$ of the [[category of presheaves]] on $\mathcal{C}$ over the [[image]] of $X$ under the [[Yoneda embedding]].

The former [[presheaf topos]] is manifestly a [[Grothendieck topos]], whence this equivalence shows that also the slice $PSh(\mathcal{C})_{/X}$ is a Grothendieck topos. This is the archetypical special case of the *[[fundamental theorem of topos theory]]* which says that all [[slice category|slices]] of toposes are themselves toposes: *[[slice toposes]]*.

As shown in Prop. \ref{TheAdjointEquivalenceInOrdinaryCategoryTheory} below, this equivalence is canonically an [[adjoint equivalence]], where the [[right adjoint]] $R$ forms the [[hom-set]] in the [[slice category|slice]] over $y(X)$, hence is the functor which takes a [[bundle]] (in the broad sense) [[internalization|internal]] to [[presheaves]] to its system of sets $\Gamma_{(-)}(E)$ of [[local sections]]:

$$
  \array{
    PSh(\mathcal{C})_{/X}
    &
    \xrightarrow{\;\;\;\; \sim \;\;\;\;}
    &
    PSh
    \big(
      \mathcal{C}_{/X}
    \big)
    \\
    \left(
    \array{
      E
      \\
      \downarrow
      \\
      X
    }
    \right)
    &\mapsto&
    \big(
      (U \to X)
      \,\mapsto\,
      \Gamma_U(E)
    \big)
    \,.
  }
$$

If instead of presheaves of sets one considers [[simplicial presheaves]] then this adjoint equivalence becomes a [[Quillen equivalence]] with respect to the the [[projective model structure on simplicial presheaves]] and its [[slice model structure]] (Prop. \ref{SimplicialLocalSectionsIsRightQuillen} below).

As such this Quillen equivalence [[Ho(CombModCat)|models]] the analogous statement (Prop. \ref{EquivalenceOfInfinityCategories} below) for [[slice (infinity,1)-category|slice $\infty$-categories]] of [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]], which thus also are [[slice (infinity,1)-topos|slice $\infty$-toposes]]. This is the archetypical case of the *[[fundamental theorem of (infinity,1)-topos theory|fundamental theorem of $\infty$-topos theory]]*, see [there](slice+infinity1-topos#SheavesOnBigSite) for more.

### Over any presheaf
 {#IdeaOverAnyPresheaf}

More generally, the analogous statement remains true when $X \,\in\, PSh(\mathcal{C})$ is any [[presheaf]] (not necessarily a [[representable functor|representable]] in the [[image]] of the [[Yoneda embedding]]). In this more general case the equivalence reads just as before

$$
  \array{
    PSh(\mathcal{C})_{/X}
    &
    \xrightarrow{\;\;\;\; \sim \;\;\;\;}
    &
    PSh
    \big(
      \mathcal{C}_{/X}
    \big)
    \,,
  }
$$


only that now the [[site]] appearing on the right must be understood as a [[full subcategory]] of the [[slice category]] of the full [[category of presheaves]], on those objects whose [[domain]] is a [[representable functor|representable]]:

$$
  \mathcal{C}_{/X}
  \;\xhookrightarrow{\;\;}\;
  PSh(\mathcal{C})_{/X}
  \,.
$$

This may equivalently be understood as the [[Grothendieck construction]] on the functor $X$.

\linebreak

## Preliminaries

### Presheaves

Let $\mathcal{C}$ be a [[small category]], we write

$$
  PSh(\mathcal{C})
  \,\coloneqq\,
  Func(\mathcal{C}^{op} ,\, Set)
$$

for its [[category of presheaves]] and

\[
  \label{PlainYonedaEmbedding}
  y_{\mathcal{C}} 
    \,\colon\, 
  \mathcal{C} 
    \xrightarrow{\;\;\;} 
  PSh(\mathcal{C}) 
\]

for the [[Yoneda embedding]].

Recall (from [there](presheaf#PresheavesAreColimitsOfRepresentables)) that every [[presheaf]] $F \,\in\, PSh(\mathcal{C})$ is a [[colimit]] of [[representables]] $y_{\mathcal{C}}(c)$ indexed by the [[comma category]] of morphisms $y_{\mathcal{C}}(c) \to F$. We will denote this "[[co-Yoneda lemma]]" by

\[
  \label{PresheafAsColimitOfRepresentables}
  F
  \;\;
  \simeq
  \;\;
  \underset
    {\underset{ y_{\mathcal{C}}(c) \to F }{\longrightarrow}}
    {
      lim
    }
    \;
    y_{\mathcal{C}}(c)
  \,.
\]


### Slice categories

For $\mathcal{D}$ any [[category]] and $B \in \mathcal{D}$, the [[hom-object]] in the [[slice category]] is given by the following [[fiber product]] (e.g, [here](over-infinity1-category#HamSpacesInASlice)):

\[
  \label{HomInSliceCategoryAsFiberProduct}
  \mathcal{D}_{/B}
  \big(
    (U,p_U)
    \,\,
    (U',p_{U'})
  \big)
  \;\;
  \simeq
  \;\;
  \mathcal{D}(U, U') 
  \underset{
    \mathcal{D}(U, B)
  }{\times}
  \{p_{U}\}
  \,.
\]

### Slices of presheaf categories

For any $X \,\in\, \mathcal{C}$ we denote the generic [[object]] of the [[slice category]] $\mathcal{C}_{/X}$ by

$$
  c_X
  \,=\,
  \left(
  \array{
    c
    \\
    \downarrow^{\mathrlap{c_X}}
    \\
    X
  }
  \;\;
  \right)
  \;\;
  \in
  \;
  \mathcal{C}_{/X}
  \,.
$$


Notice that the [[slice category]] $\mathcal{C}_{/X}$ has its own [[Yoneda embedding]]

$$
  y_{\mathcal{C}_{/X}}
  \;\colon\;
  \mathcal{C}_{/X}
  \xrightarrow{\;\;\;\;}
  PSh
  \big(
    \mathcal{C}_{/X}
  \big)
$$

but that it is also the [[source]] of the slicing of the plain  Yoneda embedding (eq:PlainYonedaEmbedding), which is still a [[fully faithful functor]]:

\[
  \label{SlicedYonedaEmbedding}
  \array{
    (y_{\mathcal{C}})_{/X}
    &\colon&
    \mathcal{C}_{/X}
    &\xhookrightarrow{\phantom{-----}}&
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \\
    &&
    c_X
    &\mapsto&  
    \left(
    \array{
      y_{\mathcal{C}}(c)
      \\
      \downarrow^{\mathrlap{ y_{\mathcal{C}}(c_X) }}
      \\
      y_{\mathcal{C}}(X)
    }
    \;\;\;\;\;
    \right)
  }
\]




## Statement

### In plain category theory

We discuss the statement in plain [[category theory]].

#### Over a representable
 {#DetailsInPlainCategoryTheoryOverARepresentable}

\begin{proposition}\label{TheAdjointEquivalenceInOrdinaryCategoryTheory}
For $X \,\in\, \mathcal{C} \xhookrightarrow{\;y\;} PSh(\mathcal{C})$.
the following anti-parallel functors constitute an [[adjoint equivalence]]
\begin{tikzcd}
    &
    \mathcal{C}_{/X}
    \ar[
      dl, 
      hook',
      "{ (y_{\mathcal{C}})_{/X} }"{above, xshift=-8pt}
    ]
    \ar[
      dr, 
      hook,
      "{ y_{(\mathcal{C}_{/X})} }"{above, xshift=4pt}
    ]
    \\
    \mathrm{PSh}
    (
      \mathcal{C}
    )_{/y(X)}
    \ar[
      rr,
      shift right=7pt,
      "{ 
        R 
        \,\coloneqq\,
        \mathrm{PSh}(\mathcal{C})_{/y(X)}
        \big(
          (y_{\mathcal{C}})_{/X}(-)
          ,\,
          -  
        \big)
      }"{below}
    ]
    &&
    \mathrm{PSh}
    \big(
      \mathcal{C}_{/X}
    \big)
    \ar[
      ll,
      shift right=7pt,
      "{L}"{above}
    ]
    \ar[
      ll,
      phantom,
      "\scalebox{.6}{$\bot$}"
    ]
\end{tikzcd}
\end{proposition}
Here:

1. the top functor $L$ is the [[cocontinuous functor|colimit-preserving functor]] that makes the top [[commuting diagram|triangle commute]], hence which takes representables over the slice site to the slicing of the underlying representables on the plain site. These two conditions fix the functor completely, by the fact (eq:PresheafAsColimitOfRepresentables) that every presheaf is a colimit of representables.

1. the bottom functor is the [[hom-functor]] of the slice category, which means (eq:HomInSliceCategoryAsFiberProduct) that it is given by a [[pullback]] of the hom-functor in $PSh(\mathcal{C})$ itself:

   \[
     \label{SliceHomOfPresheavesAsFiberOfPlainHom}
     PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
     \big(
       (y_{\mathcal{C}})_{/X}(U \xrightarrow{\phi} X)
       ,\,
       (E \xrightarrow{p} y_{\mathcal{C}}(X) )
     \big)
     \;=\;
     PSh(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        E
     \big)
     \underset
       {
         PSh(\mathcal{C})
         \big(
            y_{\mathcal{C}}(U)
            ,\,
            y_{\mathcal{C}}(X)
         \big)          
       }
       {\times}
       \big\{
          y_{\mathcal{C}}(\phi)
       \big\}
   \]


\begin{tikzcd}[column sep=20pt]
     \mathrm{PSh}(\mathcal{C})_{/y_{\mathcal{C}}(X)}
     \big(
       (y_{\mathcal{C}})_{/X}(U \xrightarrow{\phi} X)
       ,\,
       (E \xrightarrow{p} y_{\mathcal{C}}(X) )
     \big)
     \ar[
       rr
     ]
     \ar[d]
     \ar[
        drr,
        phantom,
        "\mbox{\tiny\textrm(pb)}"
     ]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        E
     \big)
     \ar[
       d,
       "{  
         \mathrm{PSh}(\mathcal{C})
         \big(
           y_{\mathcal{C}}(U)
           ,\,
           p
         \big)
       }"
     ]
     \\
     \big\{
        y_{\mathcal{C}}(\phi)
     \big\}
     \ar[rr]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        y_{\mathcal{C}}(X)
     \big)              
\end{tikzcd}

\begin{proof}
First to see that the functors are [[adjoint functor|adjoint]], we check the required [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) by observing the following sequence of [[natural bijections]]:

$$
  \begin{aligned}
  PSh(\mathcal{C}_{/X})
  \big(
    A ,\, R(B)
  \big)  
  &
  \;=\;
  PSh(\mathcal{C}_{/X})
  \Big(
    A
    ,\,
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    (
      (y_{\mathcal{C}})_{/X}(-)
      ,\,
      B
    )
  \Big)
  \\
  & \;\simeq\;
  PSh
  \big(
    \mathcal{C}_{/X}
  \big)
  \Big(
    \underset
      {\underset{c_X \to A}{\longrightarrow}}
      {\mathrm{lim}}
    y_{(\mathcal{C}_{/X})}(c_{X})
    ,\,
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    (
      (y_{\mathcal{C}})_{/X}(-)
      ,\,
      B
    )
  \Big)
  \\
  & \;\simeq\;
  \underset{
    \underset{c_X \to A}{\longleftarrow}
  }{\mathrm{lim}}
  PSh(\mathcal{C}_{/X})
  \Big(
    y_{(\mathcal{C}_{/X})}(c_{X})
    ,\,
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    (
      (y_{\mathcal{C}})_{/X}(-)
      ,\,
      B
    )
  \Big)
  \\
  &
  \;
  \simeq
  \;
  \underset{
    \underset{c_X \to A}{\longleftarrow}
  }{\mathrm{lim}}
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \big(
      (y_{\mathcal{C}})_{/X}(c_X)
      ,\,
      B
    \big)
  \\
  &
  \;
  \simeq
  \;
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \Big(
      \underset{
        \underset{c_X \to A}{\longrightarrow}
      }{\mathrm{lim}}
      (y_{\mathcal{C}})_{/X}(c_X)
      ,\,
      B
    \Big)
  \\
  & \;=\;
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \big(
      L(A)
      ,\,
      B
    \big)
  \end{aligned}
$$
Here:

* the first step is the above definition of the right adjoint,

* the second step is (eq:PresheafAsColimitOfRepresentables), 

* the third is that any [[hom-functor]] sends [[colimits]] in its first argument into [[limits]] ([[hom-functor preserves limits|here]]),

* the fourth step is the [[Yoneda lemma]] over the slice site,

* the fifth step takes the limit back into the hom-functor, but now that of the other category,

* the sixth step is the above definition of the would-be left adjoint, using again (eq:PresheafAsColimitOfRepresentables).

Now to see that these two functors are weak inverses of each other. 

In one direction we have the following sequence of [[natural bijections]] for $A \,\in\, PSh\big( \mathcal{C}_{/X}\big)$:

$$
  \begin{aligned}
    R \circ L (A)
    & 
    \;\simeq\;
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \big(
      (y_{\mathcal{C}})_{/X}(-)
      ,\,
      L(A)
    \big)
    \\
    & \;\simeq\;
    PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \Big(
      (y_{\mathcal{C}})_{/X}(-)
      ,\,
      \underset{\underset{c_X \to A}{\longrightarrow}}{\lim}
      (y_{\mathcal{C}})_{/X}(c_X)
    \Big)
    \\
    & \;\simeq\;
    \underset{\underset{c_X \to A}{\longrightarrow}}{\lim}
    y_{(\mathcal{C}_{/X})}(c_X)
    \\
    & \;\simeq\;
    A
  \end{aligned}
$$

Here:

* the first two steps just unwind again the above definitions of the functors;

* the third step follows by the [[Yoneda lemma]] over $\mathcal{C}$, to which applies by observing that that:

  1. colimits in slices are reflected a colimits in the underlying category (by [this Prop](over+category#ColimitInSliceAreReflectedByColimitsInPlainCategory)),

  1. [[colimits of presheaves are computed objectwise]],

  1. the slice hom is a pullback of the plain hom (eq:SliceHomOfPresheavesAsFiberOfPlainHom),

  1. colimits in a topos such as $PSh(\mathcal{C})$ are [[pullback-stable colimit|pullback-stable]];

* the last step re-assembles the argument, by (eq:PresheafAsColimitOfRepresentables).

In the other direction we have the following sequence of natural bijections, for $B \,\in\, PSh(\mathcal{C})_{/y_{\mathcal{C}}(X)}$:

$$
  \begin{aligned}
    L \circ R(B)
    & \;\simeq\;
    L
    \Big(
      \underset{
        \underset
        {
          y_{(\mathcal{C}_{/X})}(c_X) \to R(B)
        }
        {\longrightarrow}
      }
      {\lim}
      y_{(\mathcal{C}_{/X})}(c_X)
    \Big)
    \\
    & \;\simeq\;
    \underset{
      \underset
      {
        y_{(\mathcal{C}_{/X})}(c_X) \to R(B)
      }
      {\longrightarrow}
    }
    {\lim}
    (y_{\mathcal{C}})_{/X}(c_X)
    \\
    & \;\simeq\;
    \underset{
      \underset
      {
        L\big( y_{(\mathcal{C}_{/X})}(c_X) \big) \to B
      }
      {\longrightarrow}
    }
    {\lim}
    (y_{\mathcal{C}})_{/X}(c_X)
    \\
    & \;\simeq\;
    \underset{
      \underset
      {
        (y_{\mathcal{C}})_{/X}(c_X) \to B
      }
      {\longrightarrow}
    }
    {\lim}
    (y_{\mathcal{C}})_{/X}(c_X)
    \\
    & \;\simeq\;
    B
  \end{aligned}
$$

Here:

* the first step is the [[co-Yoneda lemma]] (eq:PresheafAsColimitOfRepresentables) for $R(B)$,

* the second step unwinds the definition of $L$ from above,

* the third step uses the [[adjoint functor|adjunction]] $L \dashv R$ established above on the indexing category of the colimit;

* the fourth step applies again the definition of $L$ from above,

* the last step is again the [[co-Yoneda lemma]] (eq:PresheafAsColimitOfRepresentables), now for $B$ itself.

\end{proof}


#### Over any presheaf
 {#DetailsInPlainCategoryTheoryOverAnyPresheaf}

\begin{proposition}\label{StatementInPlainCategoryTheoryOverAnyPresheaf}
  For $X \,\in\, PSh(\mathcal{C})$ any presheaf, we have an [[equivalence of categories]]

$$
  PSh(\mathcal{C})_{/X}
  \;\simeq\;
  PSh
  \big(
    \mathcal{C}_{/X}
  \big)
  \,.
$$
\end{proposition}
\begin{proof}
Using that

1. every presheaf is a [[colimit]] of [[representables]] (the "[[co-Yoneda lemma]]");

1. colimits in slice categories are computed in the underlying categories (see [there](over+category#LimitsAndColimits))

$$
  \left(
  \array{
    U
    \\
    \big\downarrow
    \mathrlap{{}^{p_{U}}}
    \\
    X
  }
  \;\;\;
  \right)
  \;=\;
  \Big(
     U, 
     \,
     p_U
  \Big)
  \;\simeq\;
  \Big(
  \underset{
    \underset{i \in \mathcal{I}}{\longrightarrow}
  }{\lim}
  \,
  c_U(i)
  ,\,
  (p_{c_U(i)})_{i \in \mathcal{I}}
  \big)
  \;\simeq\;
  \underset{
    \underset{i \in \mathcal{I}}{\longrightarrow}
  }{\lim}
  \big(
    c_U(i)
    ,\, 
    p_{c_U(i)}
  \big)
$$
we have an evident functor
$$
  \array{
    PSh(\mathcal{C})_{/X}
    &\longrightarrow&
    PSh
    \big(
      \mathcal{C}_{/X}
    \big)
    \\
    (U,p_U)
    &\overset{\phantom{----}}{\mapsto}&
    \underset{\underset{
      i \in \mathcal{I}
    }{\longrightarrow}}{\lim}
    \big(
      c_U(i)
      ,\, 
      p_{c_U(i)}
    \big)
  }
$$
which is clearly [[essentially surjective functor|essentially surjective]]. That it is also [[fully faithful functor|fully faithful]] is established by the following sequence of [[natural equivalences]]:

$$
  \begin{array}{l}
  PSh(\mathcal{C})_{/X}
  \Big(
    \big(
      U, 
      \,
      p_U
    \big)
    \,,
    \big(
      U
      ,\,
      p_{U'}
    \big)
  \Big)
  \\
  \;\simeq\;
  PSh(\mathcal{C})
  \big(
    U
    \,,
    U'
  \big)
  \underset{
  PSh(\mathcal{C})
  \big(
    U
    \,,
    X
  \big)
  }{\times}
  \{p_U\}
  \\
  \;\simeq\;
  \underset{
    \underset{i \in \mathcal{I}}{\longleftarrow}
  }{\lim}
  \,
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    U'
  \big)
  \underset{
  \underset{
    \underset{i \in \mathcal{I}}{\longleftarrow}
  }{\lim}
  \,
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    X
  \big)
  }{\times}
  \Big\{
    \big(
      p_{c_U(i)}
    \big)_{i \in \mathcal{I}}
  \Big\}
  \\
  \;\simeq\;
  \underset{
    \underset{i \in \mathcal{I}}{\longleftarrow}
  }{\lim}
  \,
  \bigg(
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    U'
  \big)
  \underset{
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    X
  \big)
  }{\times}
  \big\{
    p_{c_U(i)}
  \big\}
  \bigg)
  \\
  \;\simeq\;
  \underset{
    \underset{i \in \mathcal{I}}{\longleftarrow}
  }{\lim}
  \,
  \bigg(
  \underset{
    \underset{i' \in \mathcal{I}'}{\longrightarrow}
  }{\lim}
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    c_{U'}(i')
  \big)
  \underset{
  PSh(\mathcal{C})
  \big(
    c_U(i)
    \,,
    X
  \big)
  }{\times}
  \big\{
    p_{c_U(i)}
  \big\}
  \bigg)
  \\
  \;\simeq\;
  \underset{
    \underset{i \in \mathcal{I}}{\longleftarrow}
  }{\lim}
  \,
  \underset{
    \underset{i' \in \mathcal{I}'}{\longrightarrow}
  }{\lim}
  \,
  \bigg(
  PSh(\mathcal{C}_{/X})
  \Big(
    \big(
      c_U(i)
      ,\, 
      p_{c_U(i)}
    \big)
    \,,
    \big(
      c_{U'}(i')
      ,\, 
      p_{c_{U'}(i')}
    \big)
  \Big)
  \bigg)
  \\
  \;\simeq\;
  PSh(\mathcal{C}_{/X})
  \Big(
    \underset{
      \underset{i \in \mathcal{I}}{\longrightarrow}
    }{\lim}
    \big(
      c_U(i)
      ,\, 
      p_{c_U(i)}
    \big)
    \,,
    \underset{
      \underset{i' \in \mathcal{I}'}{\longrightarrow}
    }{\lim}
    \big(
      c_{U'}(i')
      ,\, 
      p_{c_{U'}(i')}
    \big)
  \Big)
  \bigg)
  \\
  \;\simeq\;
  PSh(\mathcal{C}_{/X})
  \Big(
    \big(
      U
      ,\,
      p_U
    \big)
    \,,
    \big(
      U'
      ,\,
      p_{U'}
    \big)
  \Big)
  \bigg)
  \mathrlap{\,.}
  \end{array}
$$

Here 

* the first step is the definition (eq:HomInSliceCategoryAsFiberProduct) of the slice hom;

* the second step is the expression of $U$ as a colimit of representables ([[co-Yoneda lemma]]), together with the fact that any [[hom-functor preserves limits|hom functor sends colimits in the first argument to limits]];

* the third step is the the [[fiber product]] commutes with this limit (since [[limits commute with limits]]);

* the fourth step is the expression of $U'$ as a colimit of representables ([[co-Yoneda lemma]]), together with the [[Yoneda lemma]] and the fact that colimits of presheaves are computed objectwise ([here](category+of+presheaves#LimitsOfPresheavesAreComputedObjectwise));

* the fifth step is [[universal colimits]] in the ambient [[topos]] (of [[Sets]]);

* the sixths step recognizes that the slice hom (eq:HomInSliceCategoryAsFiberProduct) defining $\mathcal{C}_{/X}$ has appeared and moves the colimits back inside by the reverse of the previous arguments, now over the slice side.

\end{proof}

\linebreak

### In enriched category theory

For $\mathcal{V}$ any [[Bénabou cosmos]] for [[enriched category theory]], the statement and proof of Prop. \ref{TheAdjointEquivalenceInOrdinaryCategoryTheory} holds and applies verbatim also in $\mathcal{V}$-[[enriched category theory]] for [[enriched presheaves]] and [[enriched slice categories]] 
(with the [[colimit]]-of-[[representable functor|representables]]-expression for [[enriched presheaves]] now being the corresponding [[coend]], as discussed at *[[co-Yoneda lemma]]*).

\begin{example}\label{ForSimplicialPresheaves}
**(for [[simplicial presheaves]])**
\linebreak
With [[Bénabou cosmos]] $\mathcal{V} \,=\,$ [[sSet]] being the category of [[simplicial sets]] with its [[cartesian monoidal category]]-structure (see at *[[products of simplicial sets]]*), the [[enriched presheaves]] are [[simplicial presheaves]] over [[simplicial sites]] $\mathcal{C}$.  With [[categories of simplicial presheaves]] denoted $sPSh(-)$, Prop. \ref{TheAdjointEquivalenceInOrdinaryCategoryTheory} reads:

\begin{tikzcd}
    \mathrm{sPSh}(\mathcal{C})_{/y_{\mathcal{C}}(X)}
    \ar[
      rrr,
      "{ 
        \mathrm{PSh}(\mathcal{C})_{/y(X)}
        \big(
          (y_{\mathcal{C}})_{/X}(-)
          ,\,
          -  
        \big)
      }"{above},
      "{ \sim }"{below}
    ]
    &&&
    \mathrm{sPSh}
    \big(
      \mathcal{C}_{/X}
    \big)
\end{tikzcd}
\end{example}

### In simplicial model category theory
 {#InSimplicialModelCategoryTheory}

For 

* $\mathcal{C}$ an [[sSet-enriched category]], 

* $X \,\in\, \mathcal{C}$ an object,

* $\mathcal{C}_{/X}$ the [[sSet]]-[[enriched slice category]]

write:


* $sPSh\big(\mathcal{C}_{/X}\big)_{proj}$ for the projective [[model structure on sSet-enriched presheaves]] (relative to the [[classical model structure on simplicial sets]] $sSet_{Qu}$) on the [[enriched slice category]],
  
  notice that this is an [[classical model structure on simplicial sets|$sSet_{Qu}$]]-[[enriched model category]], hence a [[simplicial model category]];

* $\big(sPSh(\mathcal{C})_{/y_{\mathcal{C}(X)}}\big)_{proj}$ for the [[slice model structure]] over the [[representable functor|representable]] $y_{\mathcal{C}}(X)$ of the projective [[model structure on sSet-enriched presheaves]] on $\mathcal{C}$ itself.


\begin{proposition}\label{SimplicialLocalSectionsIsRightQuillen}
  Relative to these projective (slice) model structures, the comparison functor from Exp. \ref{ForSimplicialPresheaves} is a [[right Quillen functor]], hence the [[right adjoint]] in a [[simplicial Quillen adjunction]], which is a [[Quillen equivalence]]:

\begin{tikzcd}
   \big(
    \mathrm{sPSh}(\mathcal{C})_{/y_{\mathcal{C}}(X)}
  \big)_{\mathrm{proj}}
    \ar[
      rrr,
      shift right=8pt,
      "{ 
        \mathrm{PSh}(\mathcal{C})_{/y(X)}
        \big(
          (y_{\mathcal{C}})_{/X}(-)
          ,\,
          -  
        \big)
      }"{below}
    ]
    &&&
    \mathrm{sPSh}
    \big(
      \mathcal{C}_{/X}
    \big)_{\mathrm{proj}}
    \ar[
       lll,
       shift right=8pt
    ]
    \ar[
      lll,
      phantom,
      "{ \scalebox{.6}{$\simeq_{\mathrlap{\mathrm{Qu}}}$} }"
    ]
\end{tikzcd}

\end{proposition}
\begin{proof}
Observe that:

1. Since representables are [[cofibrant objects|cofibrant]] (evidently so in the projective model structure, since [[acyclic Kan fibrations]]  [are surjective](acyclic+Kan+fibration#AcyclicKanFibrationsAreSurjective)), the unsliced simplicial hom out of a representable is a right Quillen functor by the [pullback-power axiom](enriched+model+category#PullbackPowerAxiom) in the $sSet_{Qu}$-[[enriched model category]] $sSh(\mathcal{C})$. 

1. The [[base change]]-functor by [[pullback]] is a right Quillen functor on [[slice model categories]] of $sSet_{Qu}$  (by [this Prop.](slice+model+structure#LeftBaseChangeQuillenAdjunction)). 

Together this implies that their composite (eq:SliceHomOfPresheavesAsFiberOfPlainHom) is a [[right Quillen functor]].

By [[Ken Brown's lemma]] ([here](factorization+lemma#KenBrownLemma)) it follows that the right adjoint preserves weak equivalences between [[fibrant objects]]. We claim that it also *reflects* weak equivalences between fibrant objects, in that a morphism between fibrant objects on the left is a weak equivalence if and only if its image under the right adjoint functor is a weak equivalences. 
Since the functor is also an [[equivalence of categories]], by Prop. \ref{TheAdjointEquivalenceInOrdinaryCategoryTheory}, this immediately implies that the [[derived adjunction]] is an [[equivalence of categories|equivalence]] of [[homotopy category of a model category|homotopy categories]], and hence that we have a [[Quillen adjunction]].

To see this remaining claim that the right adjoint reflects weak equivalences between fibrant objects, consider a morphism $f \,\in\, sPsh(\mathcal{C})_{/y_{\mathcal{C}}(X)}$ between fibrations such that for all $U \xrightarrow{\phi} X$ in $\mathcal{C}_{/X}$ the [[base change]] (eq:SliceHomOfPresheavesAsFiberOfPlainHom) of its values on $U \,\in\, \mathcal{C}$ is a weak equivalence:

\begin{tikzcd}[column sep=20pt]
   &[30pt]
   \mathllap{
      \mathrm{W}
      \,\ni\,
   }
   \big(y_{\mathcal{C}}(\phi)\big)^\ast
   \Big(
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        f
     \big)   
   \Big)
     \ar[
       rr
     ]
     \ar[d]
     \ar[
        drr,
        phantom,
        "\mbox{\tiny\textrm(pb)}"
     ]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        f
     \big)
     \ar[
       d
     ]
     \\
     &
     \big\{
        y_{\mathcal{C}}(\phi)
     \big\}
     \ar[rr]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        y_{\mathcal{C}}(X)
     \big)              
\end{tikzcd}

Here the right vertical morphisms are [[Kan fibrations]] by the fact that $sPSh(\mathcal{C})\big( y_{\mathcal{C}}(U),\, - \big)$ is a [[right Quillen functor]] as in the first item above.
Therefore -- since this holds for all $\phi$, by assumption -- [this Prop.](slice+model+structure#SimplicialWeakEquivalencesInSliceDetectedFiberwise) implies that 
$ 
  f(U)
  \,\simeq\,    
  \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        f
     \big)
$
is a weak equivalence.  And since this holds for all $U \,\in\, \mathcal{C}$, this means that $f$ is a weak equivalence in the slice of the projective model structure.
\end{proof}


### In $\infty$-category theory
 {#InInfinityCategoryTheory}

#### Over a representable
 {#DetailsInInfinityCategoryTheoryOverARepresentable}

Since [[simplicial localization]] at the [[Quillen equivalences]] [[Ho(CombModCat)|identifies]]  the [[homotopy theory]] ([[(infinity,1)-category|$\infty$-category]]) of [[combinatorial model categories]] (such as [[model categories of simplicial presheaves]] and their [[slice model structures]]) with that of [[presentable (infinity,1)-categories|presentable $\infty$-categories]], Prop. \ref{SimplicialLocalSectionsIsRightQuillen} immediately [[Ho(CombModCat)|implies]]:

\begin{prop}\label{EquivalenceOfInfinityCategories}
  For $\mathbf{C}$ a [[small (infinity,1)-category|small $\infty$-category]] and $X \,\in\, \mathbf{S}$ an [[object]], the operation of forming systems of [[local sections]] of [[bundles]] of [[(infinity,1)-presheaves|$\infty$-presheaves]] over $y(X)$ is an [[equivalence of (infinity,1)-categories|equivalence of $\infty$-categories]]:


\begin{tikzcd}
    \mathrm{PSh}_\infty(\mathbf{C})_{/y_{\mathbf{C}}(X)}
    \ar[
      rrr,
      "{ 
        \mathrm{PSh}_\infty(\mathbf{C})_{/y_{\mathbf{C}}(X)}
        \big(
          (y_{\mathbf{C}})_{/X}(-)
          ,\,
          (-)
        \big)
     }"
    ]
    &&&
    \mathrm{PSh}_\infty
    \big(
      \mathbf{C}_{/X}
    \big)
\end{tikzcd}

from the [[slice (infinity,1)-category|slice $\infty$-category]] of the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-category of $\infty$-presheaves]] over $\mathbf{C}$ to the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-category of $\infty$-presheaves]] over the [[slice (infinity,1)-category|slice $\infty$-category]] of $\mathbf{C}$.
\end{prop}

An alternative proof of this statement in terms of [[quasi-categories]] is in [Lurie 2009, Prop. 5.1.6.12](#Lurie09). (See also [here](slice+infinity1-topos#SheavesOnBigSite) at *[[slice (infinity,1)-topos|slice $\infty$-topos]]*.)

\begin{example}\label{CohesionOfGlobalOverGEquivariantHomotopyTheory}
**([[cohesion of global- over G-equivariant homotopy theory]])**
\linebreak

In the case that $\mathbf{C} \,=\, Snglrt \,\coloneqq\, Grpd^{fin}_{1,\geq 1}$ is the [[global orbit category]] (a [[(2,1)-category]]) the equivalence of Prop. \ref{EquivalenceOfInfinityCategories} extracts the system of [[fixed loci]] of an object in [[global equivariant homotopy theory]] sliced over the archetypical $G$-[[orbi-singularity]], for some [[equivariance group]] $G$.
Together with the [[adjoint quadruple]] that is induced (see [here](adjoint+quadruple#ViaKanExtensionOfAdjointPairs)) via [[(infinity,1)-Kan extension|$\infty$-Kan extension]] from the [[reflective sub-(infinity,1)-category|reflection]] onto the $G$-[[orbit category]],  this implies the [[cohesion of global- over G-equivariant homotopy theory]]. See there for more.
\end{example}

### Over any presheaf
 {#DetailsInInfinityCategoryTheoryOverAnyPresheaf}

A [[model category]]-theory argument for the statement over any [[1-truncated]] simplicial presheaf is in ([Hollander 2008](#Hollander08)).

But the proof of Prop. \ref{StatementInPlainCategoryTheoryOverAnyPresheaf} above uses only general abstyract properties (such as the interplay of the hom-functor with (co-)limits) which also hold in [[(infinity,1)-category theory|$\infty$-category theory]].

\linebreak


## References

Textbook accounts for the statement in plain [[category theory]]:

* {#SGA41}[[Michael Artin]], [[Alexander Grothendieck]], [[Jean-Louis Verdier]], Ex. 1 Prop. 5.11, p. [27](http://www.cmls.polytechnique.fr/perso/laszlo/sga4/SGA4-1/sga41.pdf#page=27) in:  _Théorie des Topos et Cohomologie Etale des Schémas_ ([[SGA4]]) Tome 1: *Théorie des Topos* Springer **LNM** **269** (1972) ([doi:10.1007/BFb0081551](https://link.springer.com/book/10.1007/BFb0081551), [pdf](http://www.cmls.polytechnique.fr/perso/laszlo/sga4/SGA4-1/sga41.pdf))


* {#KS06} [[Masaki Kashiwara]], [[Pierre Schapira]], Lemma 1.4.12 in: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften __332__, Springer 2006 ([doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf))

Discussion in [[(infinity,1)-category theory|$\infty$-category theory]]:

via [[model categories]]:

* {#Hollander08} [[Sharon Hollander]], Thm. 6.1(a) in : *Diagrams indexed by Grothendieck constructions*, Homology Homotopy Appl. 10(3): 193-221 (2008) ([doi:10.4310/HHA.2008.v10.n3.a10](https://dx.doi.org/10.4310/HHA.2008.v10.n3.a10),  [euclid:1251832473](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-10/issue-3/Diagrams-indexed-by-Grothendieck-constructions/hha/1251832473.full))

and via [[quasi-categories]]:

* {#Lurie09} [[Jacob Lurie]], Prop. 5.1.6.12 in: *[[Higher Topos Theory]]*, Annals of Mathematics Studies 170, Princeton University Press, 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


