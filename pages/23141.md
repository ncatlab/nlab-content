


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In broad generality, the relation between (non-[[equivariant stable homotopy theory|stable]]) [[global equivariant homotopy theory]] and $G$-[[equivariant homotopy theory]] for any fixed admissible [[equivariance group]] $G$ may be organized and formalized as follows: 

The [[slice (infinity,1)-topos|slice]] of [[global equivariant homotopy theory]] (Def. \ref{GlobalAndGEquivariantHomotopyTheory}) over the archetypical $G$-[[orbi-singularity]] $\prec\!\! G$ (Def. \ref{CategoryOfOrbiSingularities}) is [[cohesive (infinity,1)-topos|cohesive]] over $G$-[[equivariant homotopy theory]]. In particular: 

1. $G$-equivariant homotopy theory [[full sub-(infinity,1)-category|faithfully embeds]] into the $\prec\!\! G$-slice of the global theory in two different ways, one of them interpreted as the inclusion of [[G-spaces]] $X$ as [[global quotient orbifold|global]] [[orbispaces]] $X \!\sslash\! G$, 

1. these inclusions have a compatible pair of [[reflective sub-(infinity,1)-category|reflections]], one of which forms the [[spaces of sections]] $FixLoc \,\coloneqq\, \Gamma_{{}_{\prec G}}$ over the $G$-singularity $\prec\!\! G$:

\begin{tikzcd}
  \phantom{AAAAAAA}
  \overset{
    \mathclap{
    \raisebox{8pt}{
      \tiny
      \color{blue}
      \begin{tabular}{c}
        global equivariant
        \\
        homotopy theory sliced
        \\
        over $G$-orbi-singularity
        \\   
        \phantom{A}
      \end{tabular}
    }\;\;\;\;
    }
  }{
    \;\;(\mathrm{Glo} \mathrm{Grpd}_\infty)_{/\prec G}\;\;
  }
      \ar[
        rr,
        "{ \mathrm{FixLoc}    }"{description}
      ]
      \ar[
        rr,
        shift left=40pt,
        "{  }"{description, pos=.35},
        "\mathclap{\times}"{description, pos=0}
      ]
      &&
     \overset{
       \mathclap{
       \;\;
       \raisebox{3pt}{
         \tiny
         \color{blue}
         \begin{tabular}{c}
            $G$-equivariant
            \\
            homotopy theory
            \\
            \phantom{A}
         \end{tabular}
       }
       }
     }{
       \;\; G \mathrm{Grpd}_\infty \;\;
      }
     \phantom{AAAAAAA}
      \ar[
        ll,
        hook',
        shift right=20pt,
        "{ \mathrm{OrbSp} }"{description}
      ]
      \ar[
        ll,
        hook',
        shift right=-20pt,
        "{  }"{description, pos=.35}
      ]
      \ar[
        ll,
        phantom,
        shift right=10pt,
        "{\scalebox{.5}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=30pt,
        "{\scalebox{.5}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-10pt,
        "{\scalebox{.5}{$\bot$}}"
      ]
\end{tikzcd}


This observation is due to [Rezk 2014](#Rezk14). Below we amplify how this is a formal consequence (as in [Rezk 14, Sec. 7.1-7.2](#Rezk14))
of the evident [[reflective sub-(infinity,1)-category|reflection]] (Prop. \ref{GOrbitsAreReflectiveInSliceOverGOrbiSingularity}) of the $G$-[[orbit category]] inside the $\prec\!\! G$-[[slice (infinity,1)-category|slice]] of the "[[global orbit category]]" (see Rem. \ref{TerminologySingularities} below), which immediately implies (Prop. \ref{SliceOfGlobalHOverGOrbiSingularityIsCohesiveOverGH}) the cohesive relation, by [[(infinity,1)-Kan extension|$\infty$-Kan extension]].


## Preliminaries

\begin{remark}
**equivariance groups)**
\linebreak
Throughout we consider [[discrete group|discrete]] [[equivariance groups]], not necessarily [[finite group|finite]] (though [[subgroups]] of interest will be finite, as in [[proper equivariant homotopy theory]]). Much of the following also works for equivariance groups which are [[compact Lie groups]], but some definitions become a tad more laborious to state and the relation to [[smooth infinity-groupoids|smooth cohesion]] gets messed up.
\end{remark}

\begin{definition}\label{CategoryOfOrbiSingularities}
**(canonical orbi-singularities)**
  We write 
  \[
    \label{TheCategoryOfOrbiSingularities}
    \array{
    Snglrt
    &\coloneqq&
    Grpd^{fin}_{1, \geq 1}
    &\xhookrightarrow{\;}&
    Grp_\infty
    \\
    \prec\!\!G 
      &\mapsto&  
    B G
    }
  \]
  for the [[full sub-(infinity,1)-category|full sub-$\infty$-category]]  of all [[infinity-groupoids|$\infty$-groupoids]] on those that are

1. [[n-connected object of an (infinity,1)-topos|0-connected]]

1. [[n-truncated object of an (infinity,1)-category|1-truncated]]

1. [[pi-finite homotopy type|$\pi$-finite]],

hence, [[equivalence of (infinity,1)-categories|equivalently]]:

the full sub-[[(2,1)-category]] of [[Grpd]] on the [[delooping groupoids]] $\mathbf{B}G \,\simeq\, B G$ of [[finite groups]] $G$, with [[functors]] as [[1-morphisms]] and [[natural transformations]] (necessarily [[natural isomorphisms]]) as [[2-morphisms]].
\end{definition}
\begin{remark}\label{TerminologySingularities}
**(terminology: singularities vs. "global orbits")**
\linebreak
  The $(2,1)$-category in Def. \ref{CategoryOfOrbiSingularities}
is sometimes called the *[[global orbit category]]*, though other times that name refers to its non-full subcategory on the [[faithful functors]]. But *neither* of these two actually is a "category of orbits" -- instead, orbit categories are full subcategories of their slices, by Prop. \ref{GOrbitsAreReflectiveInSliceOverGOrbiSingularity} below. On the other hand, application of [[global equivariant homotopy theory]] to [[orbifolds]] identifies the category in Def. \ref{CategoryOfOrbiSingularities} with the category of archetypical local models for [[orbi-singularities]]. Therefore the choice of notation in Def. \ref{CategoryOfOrbiSingularities}.
\end{remark}

\begin{definition}\label{GlobalAndGEquivariantHomotopyTheory}
**(global- and $G$-equivariant homotopy theory)**
\linebreak
For $\mathbf{H}$ an [[(infinity,1)-topos|$\infty$]] write

\[
  \label{GlobalEquivariantInfinityTopos}
  Glo \mathbf{H}
  \;\coloneqq\;
  Sh_\infty( Singlrt ,\, \mathbf{H} )
\]

for the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-topos of $\infty$-presheaves]] on $Snglrt$ (Def. \ref{CategoryOfOrbiSingularities}), to be called the *[[global equivariant homotopy theory]]* over $\mathbf{H}$.

Moreover, for $G \,\in\, Grp(FinSet)$, write

\[
  \label{GEquivariantInfinityTopos}
  G{}\mathbf{H}
  \;\coloneqq\;
  Sh_\infty( G{}Orbt ,\, \mathbf{H} )
\]

for the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-topos of $\infty$-presheaves]] on the $G$-[[orbit category]] $G{}Orbt$ (Def. \ref{}), to be called the $G$-*[[equivariant homotopy theory]]* over $\mathbf{H}$.
\end{definition}

## Statement

### The adjoint pair between sites
 {#TheAdjunctionOfSites}

\begin{lemma}\label{TruncatedObjectsInSliceOverGOrbiSingularity}
**(0-truncated objects reflective in slice over $G$-orbi-singularity)**
\linebreak
  For $G \,\in\, Grp(FinSet)$, the 
  [[full sub-(infinity,1)-category|full sub-$\infty$-category]]
  of the [[slice (infinity,1)-category|slice]] of $Snglrt$ (Def. \ref{CategoryOfOrbiSingularities}) over $\prec\!\! G$ (eq:TheCategoryOfOrbiSingularities) on the [[n-truncated object in an (infinity,1)-category|0-truncated objects]] 

1. consists precisely of the [[faithful functors]] $B H \xrightarrow{\;\; B i_H \;\;} B G$ between [[delooping groupoids]], 

   hence those which are [[delooping groupoid|deloopings]] of [[subgroup]]-inclusions $H \xhookrightarrow{\;\; i_H \;\;} G$;

1. is [[reflective sub-(infinity,1)-category|reflective]], with reflector being the [[image]]-factorization of [[group homomorphisms]]:

\[
  \label{TheAbstractAdjunctionOfSites}
      Sngrlt_{/\prec G}
      \underoverset
        {\underset{}{\hookleftarrow}}
        {\overset{\tau_0}{\longrightarrow}}
        {\;\;\;\;\bot\;\;\;\;}
      \big(
        Snglrt_{/\prec G}
      \big)_{\tau_0}
      \;\simeq\;
      \left\{
      \array{
        \prec\!\!H
        && \longrightarrow &&
        \prec\!\!K
        \\
        & 
        {}_{\mathllap{\prec i_H}}\searrow
        &&
        \swarrow_{\mathrlap{\prec i_K}}
        \\
        && \prec\!\!G
      }
     \right\}
\]

\end{lemma}
\begin{proof}
  That 0-truncated morphisms between 1-groupoids are equivalently the [[faithful functors]] is [this Prop.](n-truncated+object+of+an+infinity1-category#TruncatedMorphismsBetweenGroupoids). With this in hand, it is immediate to check the [hom-equivalence](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences) (here just a [[natural bijection]] of [[hom-sets]]) which characterizes the adjunction.
\end{proof}

\begin{lemma}\label{GOrbitsAs0TruncatedObjectsInSliceOverGOrbiSingularity}
**($G$-orbits as 0-truncated objects in slice over $G$-orbi-singularity)**
\linebreak
  For $G \,\in\, Grp(FinSet)$
  there is an [[equivalence of (infinity,1)-categories|equivalence of $\infty$-categories]] (here in fact: an [[equivalence of categories]])
  between 

1. the [[n-truncated object in an (infinity,1)-category|0-truncated objects]] in the [[slice (infinity,1)-category|slice]] of $Snglrt$ (Def. \ref{CategoryOfOrbiSingularities}) over $\prec\!\! G$ (eq:TheCategoryOfOrbiSingularities),

1. the $G$-[[orbit category]] (the [[full subcategory]] of [[G-sets]] on the [[transitive actions]], hence the [[coset space|coset sets]] $G/H$):

$$
  \array{
    (Sngrtl_{/\prec G})_{\tau_0}
    &
    \xleftrightarrow{\;\; \sim \;\;}
    &
    G{}Orbt
    \\
    \left(
    \array{
      \prec\!\!H
      \\ 
      \downarrow^{\mathrlap{\prec i_H}}
      \\
      \prec\!\!G
    }
    \;\;
    \right)
    &\mapsto&
    G/H
  }
  \,.
$$
\end{lemma}
\begin{proof}
  It is straightforward, to check this directly. But it also follows abstractly by [this Prop.](Borel+model+structure#RelationToSliceOverSimplicialClassifyingSpace) about the general relation between slicing over $B G$ and [[infinity-action|$\infty$-actions]] of $G$: 

The functor which assigns to $B H \xrightarrow{\;\; B i_H\;\;} B G$ its [[homotopy fiber]] is a [[fully faithful functor]] into the [[G-sets]] among all $G$-[[infinity-action|$\infty$-actions]] (by the [[n-truncated object in an (infinity,1)-category|0-truncation condition]]). But the [[homotopy fiber]] of $B i_H$ is the [[coset space|coset set]] (by [this Example](...)):
$$
  \array{
    \big(
      Snglrt_{/\prec G}
    \big)_{\tau_0}
    &\simeq&
    \big(
      (Grp_{1,\geq 1})_{/B G}
    \big)_{\tau_0}
    &
    \xhookrightarrow{\;\; hofib(-) \;\;}
    &
    G Set
    \\
    \left(
      \array{
        \prec\!\!H 
        \\
        \downarrow^{\mathrlap{ \prec i_H }}
        \\
        \prec\!\!G
      }
      \;\;
    \right)
    &\mapsto&
    \left(
      \array{
        B H 
        \\
        \downarrow^{\mathrlap{ B i_H }}
        \\
        B G
      }
      \;\;\;
    \right)
    &\mapsto&
    G/H
    \mathrlap{\,.}
  }
$$
\end{proof}

\begin{lemma}
\label{ReflectorPreservesFiniteProductsOnFreeCoproductCompletion}
  The [[free coproduct completions]] of the $(2,1)$-categories (eq:TheAbstractAdjunctionOfSites) have [[finite products]] and the unique coproduct-preserving extension of $\tau0_0$ to these preserves finite products.
\end{lemma}
\begin{proof}
 The category on the right is equivalently the $G$-[[orbit category]] (by Lem. \ref{GOrbitsAs0TruncatedObjectsInSliceOverGOrbiSingularity}) whose [[free coproduct completion]] is (using here our assumption that $G$ is a [[discrete group]]) the category of all [[G-set|$G$-sets]] (as in  [this remark](orbit+category#GActionsAndGOrbits)). 

Similarly, the free coproduct completion of the category on the left is readily seen to be that of all 1-truncated in $\infty Grpd_{/B G}$. Hence the coproduct-preserving extension of $\tau_0$ to these is just the 0-truncation functor in this slice [[(infinity,1)-topos|$\infty$-topos]] and as such preserves finite products (by [this Prop.](n-truncated+object+of+an+infinity1-category#nTruncationInToposPreservesFiniteProducts), see [this Exp.](adjoint+quadruple#nTruncationsOfFullSubcategoriesOfInfinityToposes)).
\end{proof}

In conclusion:

\begin{proposition}\label{GOrbitsAreReflectiveInSliceOverGOrbiSingularity}
**($G$-orbits are reflective in slice over $G$-orbi-singularity)**
\linebreak
For $G \,\in\, Grp(FinSet)$ the $G$-[[orbit category]] is canonically a [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of 
the [[slice (infinity,1)-category|slice]] of $Snglrt$ (Def. \ref{CategoryOfOrbiSingularities}) over $\prec\!\! G$ (eq:TheCategoryOfOrbiSingularities) whose reflector $\tau_0$ preserves finite products when extended to the [[free coproduct completions]], where all finite products exist:

\begin{tikzcd}[row sep=0pt]
  \mathrm{Sngrlt}_{/\prec G}
  \ar[
    rr,
    shift left=7pt,
    "\tau_0"{above},
    "{ \mathclap{\widehat{\times}} }"{description, pos=0}
  ]
  &&
  G \mathrm{Orbt}
  \ar[
    ll,
    hook',
    shift left=7pt,
    "{ i }"{below}
  ]
  \ar[
    ll,
    phantom,
    "{ \scalebox{.5}{$\bot$} }"
  ]
  \\
  \left(
  \!\!
  \begin{array}{c}
    \prec\!\! H
    \\
    \downarrow^{\mathrlap{\scalebox{.7}{$\prec\! i_H$}}}
    \\  
    \prec\!\! G
  \end{array}
  \right)
  \ar[
    rr,
    phantom,
    "{ \mapsto }"{description, rotate=180}
  ]
  &&
  G/H
\end{tikzcd}
\end{proposition}
\begin{proof}
  By the immediate combination of
  Lem. \ref{TruncatedObjectsInSliceOverGOrbiSingularity}
  with
  Lem. \ref{GOrbitsAs0TruncatedObjectsInSliceOverGOrbiSingularity}
  and 
  Lem. \ref{ReflectorPreservesFiniteProductsOnFreeCoproductCompletion}.
\end{proof}



### The adjoint quadruple between homotopy theories
 {#TheCohesionOfHomotopyTheories}

\begin{prop}\label{SliceOfGlobalHOverGOrbiSingularityIsCohesiveOverGH}
**(slice of $Glo(\mathbf{H})$ over $\prec\!\!G$ is cohesive over $G\mathbf{H}$)**
\linebreak
For $\mathbf{H}$ any [[(infinity,1)-topos|$\infty$-topos]] and $G \,\in\, Grp(FinSet)$, the [[slice (infinity,1)-category|slice]] of the [[global equivariant homotopy theory]] $Glo(\mathbf{H})$ (eq:GlobalEquivariantInfinityTopos) over the $G$-orbi-singularity $\prec\!\!G$ (eq:TheCategoryOfOrbiSingularities) is [[cohesive (infinity,1)-topos|cohesive]] [[base (infinity,1)-topos|over]] the $G$-[[equivariant homotopy theory]] $G\mathbf{H}$ (eq:GEquivariantInfinityTopos) in that there exists an [[adjoint quadruple]] of [[(infinity,1)-functors|$\infty$-functors]] of the form
\begin{tikzcd}
  (\mathrm{Glo} \mathbf{H})_{/\prec G}
      \ar[
        rr,
        "{ \tau_\ast \,\simeq\, i^\ast    }"{description}
      ]
      \ar[
        rr,
        shift left=40pt,
        "{ \tau_! }"{description, pos=.39},
        "\mathclap{\times}"{description, pos=0}
      ]
      &&
     G \mathbf{H}
      \ar[
        ll,
        hook',
        shift right=20pt,
        "{ \tau^\ast \,\simeq\, i_! }"{description}
      ]
      \ar[
        ll,
        hook',
        shift right=-20pt,
        "{ i_\ast }"{description, pos=.39}
      ]
      \ar[
        ll,
        phantom,
        shift right=10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=30pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}
where those going to the left are [[fully faithful (infinity,1)-functors|fully faithful]] and the top one [[preserved limit|preserves]] [[finite product|finite]] [[homotopy products]].
\end{prop}
\begin{proof}\label{ProofOfTheCohesiveAdjointQuadruple}
The general fact that [[slice of presheaves is presheaves on slice|$\infty$-slices of $\infty$-presheaves are $\infty$-presheaves on the $\infty$-slice]] (by  [this Prop.](slice+of+presheaves+is+presheaves+on+slice#EquivalenceOfInfinityCategories) or [this Prop.](slice+infinity1-topos#SheavesOnBigSite)) means in the present case that the operation of extracting systems of [[fixed loci]] is an [[equivalence of (infinity,1)-categories]] as follows:
  $$
    (Glo \mathbf{H})_{/\prec G}
    \;\coloneqq\;
    PSh_\infty
    \big(
      Sngrlt
      ,\,
      \mathbf{H}
    \big)_{/\prec G}
    \;\;
    \simeq
    \;\;
    PSh_\infty
    \big(
      Sngrlt_{/\prec G}  
      ,\,
      \mathbf{H}
    \big)
    \,.
  $$
  With this, the statement follows -- via [this Prop.](adjoint+quadruple#KanExtensionOfFiniteProductPreservingReflectionIsCohesiveAdjointQuadruple) --
by  [[(infinity,1)-Kan extension|$\infty$-Kan extension]]
 of the adjoint pair from Prop. \ref{GOrbitsAreReflectiveInSliceOverGOrbiSingularity}.
\end{proof}


## References

The observation is due to:

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014  ([pdf](http://www.math.uiuc.edu/~rezk/global-cohesion.pdf), [[Rezk14.pdf:file]])

where further properties of this cohesive situation are proven, revolving around further characterization of the full inclusion of $G$-[[orbispaces]].

Some of the above notation (e.g. for "$\prec\!\! G$") follows:

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

which expands on application of the above singular cohesion -- in the special case $G = 1$ but combined with [[smooth infinity-groupoid|smooth cohesion]] --  to differential-geometric [[orbifolds]]  and [[orbifold cohomology]].

Diagrams and discussion as presented above are taken from:

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Equivariant principal infinity-bundles|Equivariant principal $\infty$-bundles]]*



