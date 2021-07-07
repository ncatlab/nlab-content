
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

* [[nilpotent space|nilpotent]]: the [[fundamental group]] $\pi_1(X)$ is a [[nilpotent group]];

* rational [[finite type]]: the [[rational cohomology]]-[[cohomology group|groups]] are [[finite number|finite]]-[[dimension|dimensional]], $dim_{\mathbb{Q}}\big( H^n(X;,\mathbb{Q}) \big) \lt \infty$, for all $n \in \mathbb{N}$.

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

\begin{proposition}
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

## Related concepts

* [[fundamental theorem of equivariant dg-algebraic rational homotopy theory]]



## References

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))


[[!redirects fundamental theorem of dgc-algebraic rational homotopy theory]]

