
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The fundamental [[theorem]] of [[rational homotopy theory]] modeled by [[dgc-algebras]].


## Preliminaries

+-- {: .num_defn #NilpotententFiniteRationalHomotopyTypes} 
###### Definition
**(nilpotent and finite rational homotopy types)**

Write

\[
  \label{NilpotentQFiniteHomotopyTypes}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)^{fin_{\mathbb{Q}}}_{\geq 1, nil}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)
\]

for the [[full subcategory]] of the [[classical homotopy category]]  ([[homotopy category]] of the [[classical model structure on simplicial sets]]) on those [[homotopy types]] $X$ which are

* [[connected topological space|connected]]: $\pi_0(X) = \ast$;

* [[nilpotent space|nilpotent]]: the [[fundamental group]] $\pi_1(X)$ is a [[nilpotent group]] and the higher [[homotopy groups]] are [[nilpotent modules]] over it;

* of rational [[finite type]]: the [[rational cohomology]]-[[cohomology group|groups]] are [[finite number|finite]]-[[dimension|dimensional]], $dim_{\mathbb{Q}}\big( H^n(X;,\mathbb{Q}) \big) \lt \infty$, for all $n \in \mathbb{N}$.

and

\[
  \label{NilpotentFiniteRationalHomotopyTypes}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)
\]

for the further [[full subcategory]] on those [[homotopy types]] that are already [[rational spaces|rational]].


Similarly, write

\[
  \label{NilpotentFiniteTypedgcAlgebras}
  Ho
  \big(
     DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)_{fin}^{\geq 1}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)
\]

for the [[full subcategory]] of the [[homotopy category]] of the [[projective model structure on connective dgc-algebras]] on those [[dgc-algebras]] $A$ over the [[rational numbers]] which are

* connected: $H^0(A) \simeq \mathbb{Q}$

* [[finite type]]: the [[cochain cohomology]] [[cohomology group|groups]] are [[finite number|finite]] [[dimension|dimensional]], $dim_{\mathbb{Q}}\big( H^n(A) \big) \lt \infty$, for all $n \in \mathbb{N}$.

=--

([Bousfield-Gugenheim 76, 9.2](#BousfieldGugenheim76))

## Statement

+-- {: .num_pro #FundamentalTheoremOfdgAlgebraicRationalHomotopyTheory} 
###### Proposition
**([[fundamental theorem of dg-algebraic rational homotopy theory]])**

The [[derived adjunction]]

$$
  Ho
  \left(
    \big(
      DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
    \big)^{op}_{proj}
  \right)
  \underoverset
    {
      \underset
        {\;\;\; \mathbb{R} exp_{PL} \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\; \mathbb{L} \Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot}
  Ho
  \big(
    SimplicialSets_{Qu}
  \big)
$$

of the [[Quillen adjunction between simplicial sets and connective dgc-algebras]] (whose [[left adjoint]] is the [[PL de Rham complex]]-[[functor]]) has the following properties:

* on connected, nilpotent rationally finite homotopy types $X$ (eq:NilpotentQFiniteHomotopyTypes) the [[derived adjunction unit]] is [[rationalization]]

  $$
    \array{
    Ho
    \big(
       SimplicialSets_{Qu}
    \big)^{fin_{\mathbb{Q}}}_{\geq 1, nil}
    &
      \overset{
      }{\longrightarrow}
    &
    Ho
    \big(
       SimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
    \\
    X
    &\mapsto&
    \mathbb{R}\exp_{PL} \circ \Omega^\bullet_{PLdR}(X)
    }    
  $$

  $$
    X
    \underoverset
      {\eta_X^{der}}
      {rationalization}
      {\longrightarrow}
    \mathbb{R}\exp_{PL} \circ \Omega^\bullet_{PLdR}(X)
  $$

* on the [[full subcategories]] of nilpotent and finite rational homotopy types from Def. \ref{NilpotententFiniteRationalHomotopyTypes} it restricts to an [[equivalence of categories]]:

  $$
    Ho
    \left(
      \big(
        DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
      \big)^{op}_{proj}
    \right)^{\geq 1}_{fin}
    \underoverset
      {
        \underset
          {\;\;\; \mathbb{R} exp_{PL} \;\;\;}
          {\longrightarrow}
      }
      {
        \overset
          {\;\;\; \mathbb{L} \Omega^\bullet_{PLdR}\;\;\;}
          {\longleftarrow}
      }
      {\simeq}
    Ho
    \big(
      SimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
  $$


=--

([Bousfield-Gugenheim 76, Theorems 9.4 & 11.2](#BousfieldGugenheim76))

## Change of scalars
 {#ChangeOfScalars}

Often it is desireable to work with dgc-algebras not over the [[rational numbers]] but over the [[real numbers]], because these relate to [[de Rham complex|de Rham theory]] (e.g.: [[the PL de Rham complex of a smooth manifold is equivalent to the de Rham complex]]). While a [[PL de Rham complex]]-[[Quillen adjunction]] $\Omega^\bullet_{\mathrm{P}\!k\!\mathrm{LdR}} \dashv \exp_{\mathrm{P}\!k\!\mathrm{L}}$ ("piecewise $k$-linear") exists over all [[ground fields]] $k$ of [[characteristic zero]], with induced [[derived adjunction]]

$$
  Ho
  \Big(
    \big(
      DGCAlgebras^{\geq 0}_{k}
    \big)^{op}_{proj}
  \Big)
  \underoverset
    {\underset{\mathbb{R} exp_{\mathrm{P}\!k\!\mathrm{L}}}{\longrightarrow}}
    {\overset{\mathbb{L} \Omega^\bullet_{\mathrm{P}\!k\!\mathrm{LdR}}}{\longleftarrow}}
    {\bot}
  Ho
  \big(
    SimplicialSets_{Qu}
  \big)
  \,,
$$

this does not model $k$-[[localization]] of [[homotopy type|spaces]] unless $k = \mathbb{Q}$. However, it does still relate to [[rationalization]] under [[extension of scalars]], given by the [[derived adjunction]] (via [this Prop.](model+structure+on+dg-algebras#ExtensionOfScalarsQuillenAdjunction))
$$
  Ho
  \Big(
    \big(
      DGCAlgebras^{\geq 0}_{k}
    \big)^{op}_{proj}
  \Big)
  \underoverset
    {
      \underset{
        \mathbb{R}\big( (-)\otimes_{\mathbb{Q}}\mathbb{R} \big)
      }{
        \longrightarrow
      }
    }
    {
      \overset{
        \mathbb{L} res_{\mathbb{Q}}
      }{
      \longleftarrow
      }
    }
    {\bot}
  Ho
  \Big(
    \big(
      DGCAlgebras^{\geq 0}_{\mathbb{Q}}
    \big)^{op}_{proj}
  \Big)
  \,,
$$
in that the following holds:

\begin{proposition}\label{DerivedPLdeRhamFunctorsRelatedByChangeOfScalars}
  For $k$ be a [[field]] of [[characteristic zero]], the following [[diagram]] of [[derived functors]] [[commuting diagram|commutes]] up to [[natural isomorphism]]:

\begin{tikzcd}
    \mathrm{Ho}
    \Big(
      \big(
        \mathrm{dgcAlg}^{\geq 0 }_{\color{blue}\mathbb{Q}}
      \big)^{\mathrm{op}}_{\mathrm{proj}}
    \Big)
    \ar[
      dd,
      "{
        \mathbb{R}
        \big(
          (-) \otimes_{\mathbb{Q}} \mathbb{R}
        \big)
      }"{left}
    ]
    &&
    \;\;
    \mathrm{Ho}
    \big(
      \mathrm{sSets}_{\mathrm{Qu}}
    \big)^{\mathrm{fin}_{\mathbb{Q}}}
    \ar[
      ll,
      "
        \mathbb{L}
        \Omega^\bullet_{\mathrm{P}{\color{blue}\mathbb{Q}}\mathrm{LdR}}
      "{above}
    ]
    \ar[
      dd,-,
      shift right=1pt
    ]
    \ar[
      dd,-,
      shift left=1pt
    ]
    \\
    \\
    \mathrm{Ho}
    \Big(
    \big(   
      \mathrm{dgcAlg}^{\geq 0}_{\color{blue}\mathbb{R}}
    \big)^{\mathrm{op}}_{\mathrm{proj}}
    \Big)
    &&
    \;\;
    \mathrm{Ho}
    \big(
      \mathrm{sSets}_{\mathrm{Qu}}
    \big)^{\mathrm{fin}_{\mathbb{Q}}}
    \ar[
      ll,
      "
        \mathbb{L}
        \Omega^\bullet_{\mathrm{P}{\color{blue}\mathbb{R}}\mathrm{LdR}}
      "{below}
    ]
\end{tikzcd}



\end{proposition} 

This is effectivley the statement of [Bousfield&Gugenheim 1976, Lem. 11.7](#BousfieldGugenheim76).

This state of affairs may be recast as follows ([FSS 2020](#FSS20)):

For any [[field]] $k$ of [[characteristic zero]], abbreviate

$$
  L_k 
  \;\coloneqq\;
  \mathbb{R} exp_{\mathrm{P}k\mathrm{L}}
    \circ
  \mathbb{L} \Omega^\bullet_{\mathrm{P}kLdR}
  \,,
$$

keeping in mind that this is a localization of spaces only if $k = \mathbb{Q}$.

Then for $X, A \in Ho(sSet)^{fin_{\mathbb{Q}}}_{\geq 1, nil}$ a [[pair]] of [[connected homotopy type|connected]] [[nilpotent homotopy type|nilpotent]] [ℚ-finite](finite+type#InRationalHomotopyTheory) [[homotopy types]], define the *$k$-[[Chern-Dold character]]* on the [[non-abelian cohomology|non-abelian]] $A$-cohomology of $X$ to be the [[cohomology operation]] induced by the [[derived adjunction unit]] of the [[PL de Rham complex|PL de Rham adjunction]] ([this Prop.](PL+de+Rham+complex#QuillenAdjunctionBetweenSimplicialSetsAndConnectivedgcAlgebras)):

\[
  \label{ChernDoldCharacter}
  ch^k_A(X)
  \;\colon\;
  H(X;\, A)
  \;\xrightarrow{ 
    \;\;
    H(X;\, \mathbb{D}\eta^{\mathrm{P}k\mathrm{L}_A}) 
    \;\;
  }\;
  H(X;\, L_k A)  
  \,.
\]

Moreover, define *extension of scalars on [[non-abelian cohomology|non-abelian]] [[rational cohomology]]* to be the comoposite

\[
  \label{ExtensionOfScalarsOnChomolology}
  \array{
    H(X;\, L_{\mathbb{Q}}A)
    &\xrightarrow{ (-) \otimes_{{}_{\mathbb{Q}}} k   }&
    H(X;\, L_{k}A)    
    \\
    {}^{\mathllap{
      \widetilde{(-)}
    }}
    \big\downarrow {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{\simeq}}
    \big\uparrow 
    {}^{\mathrlap{
      \widetilde{(-)}
    }}
    \\
    H
    \big(
      \mathbb{D}\Omega^\bullet_{\mathrm{P}\mathbb{Q}\mathrm{LdR}}(X);
      \,
      \mathbb{D}\Omega^\bullet_{\mathrm{P}\mathbb{Q}\mathrm{LdR}}(A)
    \big)
    &
    \xrightarrow{
      \mathbb{D}
      \big(
        (-) \otimes_{{}_{\mathbb{Q}}} k
      \big)
    }
    &
    H
    \big(
      \mathbb{D}\Omega^\bullet_{\mathrm{P}k\mathrm{LdR}}(X);
      \,
      \mathbb{D}\Omega^\bullet_{\mathrm{P}k\mathrm{LdR}}(A)
    \big)    
  }
\]

(where $H(-;\,-) \coloneqq Ho(-,\,-)$ denotes [[hom-sets]] in the respective [[homotopy category of a model category|homotopy category]])

of:

1. the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the [[derived adjunction|derived]] [[PL de Rham complex|PL de Rham adjunction]];

1. the corresponding hom-component of the [[derived functor]] of [[extension of scalars]] ([this Prop.](model+structure+on+dg-algebras#ExtensionOfScalarsQuillenAdjunction)).

(This is essentially the construction of "tensoring a homotopy type with $\mathbb{R}$" that is mentioned in [DGMS 1975, Footnote 5](#DGMS75).)

Then:

\begin{prop}\label{kChernDoldCharacterFactorsThroughRationalChernDoldCharacter}
  The $k$-Chern-Dold character (eq:ChernDoldCharacter)
  factors through the rational Chern-Dold character via the extension-of-scalars-transformation (eq:ExtensionOfScalarsOnChomolology).

$$
  ch^k_A(X)
  \;=\;
  \big(
    (-)\otimes_{{}_{\mathbb{Q}}} k
  \big)
  \,\circ\, 
  ch^{\mathbb{Q}}_A(X)
  \,.
$$
\end{prop}
\begin{proof}
Consider the following [[diagram]] of [[hom-sets]] (shown for $k = \mathbb{R}$, just for definiteness):

<img src="https://ncatlab.org/nlab/files/RationalAndRealCharacterMap20210708.jpg" width="740">

Here:

* the [[commuting diagram|commutativity]] of the bottom part is Prop. \ref{DerivedPLdeRhamFunctorsRelatedByChangeOfScalars};

* the triangle on the left as well as as the outer diagram [[commuting diagram|commute]] by basic properties of [[adjoint functors]] ([this Lemma](geometry+of+physics+--+categories+and+toposes#ReExpressingMiddleFunctorInAdjointTriple));

* the square on the right commutes by definition (eq:ExtensionOfScalarsOnChomolology);

Together this implies that the top rectangle commutes, which is the claim to be shown.
\end{proof}

## Related concepts

* [[fundamental theorem of equivariant dg-algebraic rational homotopy theory]]



## References

The full-blown equivalence first appears in

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

Related discussion over the [[real numbers]]:

* {#DGMS75} [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]], *Real homotopy theory of Kähler manifolds*, 
Inventiones mathematicae volume 29, pages 245–274 (1975) ([doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853))

Review and interpretation in terms of [[non-abelian cohomology|non-abelian]] [[Chern-Dold character]]-theory:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]*



[[!redirects fundamental theorem of dgc-algebraic rational homotopy theory]]

