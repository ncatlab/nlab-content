
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

For $\mathcal{C}$ any [[small category]] and $X \,\in\, \mathcal{X}$ an [[object]], the [[category of presheaves]] $PSh\big( \mathcal{C}_{/X}\big)$ on the [[slice category]] $\mathcal{C}_{/X}$ is [[equivalence of categories|equivalent]] to the [[slice category|slice]] $PSh(\mathcal{C})_{/X}$ of the [[category of presheaves]] on $\mathcal{C}$ over the [[image]] of $X$ under the [[Yoneda embedding]].

The former [[presheaf topos]] is manifestly a [[Grothendieck topos]], whence this equivalence shows that also the slice $PSh(\mathcal{C})_{/X}$ is a Grothendieck topos. This is the archetypical special case of the *[[fundamental theorem of topos theory]]* which says that all [[slice category|slices]] of toposes are themselves toposes: *[[slice toposes]]*.

As shown below, this equivalence is canonically an [[adjoint equivalence]], where the [[right adjoint]] $R$ forms the [[hom-set]] in the [[slice category|slice]] over $y(X)$, hence the functor which takes a [[bundle]] (in the broad sense) [[internalization|internal]] to [[presheaves]] to its system of sets $\Gamma_{(-)}(E)$ of [[local sections]]:

$$
  \array{
    PSh(\mathcal{C})_{/X}
    &
    \underoverset
      {\underset{ 
        R
      }{\longrightarrow}}
      {}
      {\;\;\;\; \simeq \;\;\;\;}
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


Let $\mathcal{C}$ be a [[small category]] and $X \,\in\, \mathcal{C}$ any [[object]]. Write

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

Recall (from [there](presheaf#PresheavesAreColimitsOfRepresentables)) that every [[presheaf]] $F \,\in\, PSh(\mathcal{C})$ is a [[colimit]] of [[representables]] $y_{\mathcal{C}}(c)$ indexed by the [[comma category]] of morphisms $y_{\mathcal{C}}(c) \to F$. We will denote this by

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


For any $X \,\in\, \mathcal{X}$ we denote the generic [[object]] of the [[slice category]] $\mathcal{C}_{/X}$ by

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

but that it is also the [[source]] of the slicing of the plain  Yoneda embedding (eq:PlainYonedaEmbedding):

$$
  \array{
    (y_{\mathcal{C}})_{/X}
    &\colon&
    \mathcal{C}_{/X}
    &\xrightarrow{\phantom{-----}}&
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
$$

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
      "{ y_{(\mathcal{C}_{/X})} }"{above, xshift=3pt}
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
      shift right=7pt
    ]
    \ar[
      ll,
      phantom,
      "\scalebox{.6}{$\bot$}"
    ]
\end{tikzcd}
\end{proposition}
Here the top functor is the [[cocontinuous functor|colimit-preserving functor]] that makes the top [[commuting diagram|diagram commute]], hence which takes representables over the slice site to the slicing of the underlying representables on the plain site. These two conditions fix the functor completely, by the fact (eq:PresheafAsColimitOfRepresentables) that every presheaf is a colimit of representables.
\begin{proof}

First to see that the functors are [[adjoint functor|adjoint]], we check the required [hom-isomorphism](adjoint functor#InTermsOfHomIsomorphism):

(...)

\end{proof}

## References

(...)
