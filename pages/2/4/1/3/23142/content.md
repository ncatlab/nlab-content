
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

For $\mathcal{C}$ any [[small category]] and $X \,\in\, \mathcal{C}$ an [[object]], the [[category of presheaves]] $PSh\big( \mathcal{C}_{/X}\big)$ on the [[slice category]] $\mathcal{C}_{/X}$ is [[equivalence of categories|equivalent]] to the [[slice category|slice]] $PSh(\mathcal{C})_{/X}$ of the [[category of presheaves]] on $\mathcal{C}$ over the [[image]] of $X$ under the [[Yoneda embedding]].

The former [[presheaf topos]] is manifestly a [[Grothendieck topos]], whence this equivalence shows that also the slice $PSh(\mathcal{C})_{/X}$ is a Grothendieck topos. This is the archetypical special case of the *[[fundamental theorem of topos theory]]* which says that all [[slice category|slices]] of toposes are themselves toposes: *[[slice toposes]]*.

As shown below, this equivalence is canonically an [[adjoint equivalence]], where the [[right adjoint]] $R$ forms the [[hom-set]] in the [[slice category|slice]] over $y(X)$, hence the functor which takes a [[bundle]] (in the broad sense) [[internalization|internal]] to [[presheaves]] to its system of sets $\Gamma_{(-)}(E)$ of [[local sections]]:

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

If instead of presheaves of sets one considers [[simplicial presheaves]] then this adjoint equivalence becomes a [[Quillen adjunction]] with respect to the the [[projective model structure on simplicial presheaves]] and its [[slice model structure]]. This ought to be a [[Quillen equivalence]].

As such this Quillen equivalence models the analogous statement for [[slice (infinity,1)-category|slice $\infty$-categories]] of [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]], which thus also are [[slice (infinity,1)-topos|slice $\infty$-toposes]]. See [there](slice+infinity1-topos#SheavesOnBigSite) for more.


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


### Slices

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

\begin{proposition}
The following anti-parallel functors constitute an [[adjoint equivalence]]
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
Here 

1. the top functor $L$ is the [[cocontinuous functor|colimit-preserving functor]] that makes the top [[commuting diagram|triangle commute]], hence which takes representables over the slice site to the slicing of the underlying representables on the plain site. These two conditions fix the functor completely, by the fact (eq:PresheafAsColimitOfRepresentables) that every presheaf is a colimit of representables.

1. the bottom functor is the [[hom-functor]] of the slice category, which means that it is given by a [[pullback]] of the hom-functor in $PSh(\mathcal{C})$ itself:

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

## References

(...)
