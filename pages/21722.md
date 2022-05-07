
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
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

The fundamental [[theorem]] of [[equivariant rational homotopy theory]] modeled by [[equivariant dgc-algebras]].

## Preliminaries

Let $G$ be a [[finite group]].


Write

* $\big(G dgcAlgebras^{\geq 0}_{k} \big)^{op}_{proj}$ for the [[opposite model structure|opposite]] of the [[projective model structure on equivariant connective dgc-algebras]];

* $G SimplicialSets_{Qu}$ for the [[model structure on equivariant simplicial sets]], namely the global projective [[model structure on functors]] from the [[opposite category|opposite]] of the [[orbit category]] to the [[classical model structure on simplicial sets]]).


+-- {: .num_defn #NilpotententFiniteRationalHomotopyTypes} 
###### Definition
**(simply connected and finite equivariant rational homotopy types)**

Write

\[
  \label{NilpotentQFiniteHomotopyTypes}
  Ho
  \big(
     G SimplicialSets_{Qu}
  \big)^{fin_{\mathbb{Q}}}_{\geq 2}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
    G SimplicialSets_{Qu}
  \big)
\]

for the [[full subcategory]] of the [[homotopy category of a model category|homotopy category]] of the [[model structure on equivariant simplicial sets]] on those [[equivariant homotopy types]] $X$ which over each $G/H \in G Orbits$ are

* [[connected topological space|connected]]: $\pi_0(X^H) = \ast$

* [[simply connected topological space|simply connected]]: $\pi_1(X^H) = 1$ is the [[trivial group]];

* rationally [[of finite type]]: $dim_{\mathbb{Q}}\big( H^n(X^H;,\mathbb{Q}) \big) \lt \infty$ for all $n \in \mathbb{N}$.

and

\[
  \label{NilpotentFiniteRationalHomotopyTypes}
  Ho
  \big(
     G SimplicialSets_{Qu}
  \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 2}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)
\]

for the futher [[full subcategory]] on those [[equivariant homotopy types]] that are already [[rational spaces|rational]].


Similarly, write

\[
  \label{NilpotentFiniteTypedgcAlgebras}
  Ho
  \big(
     G dgcAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)_{fin}^{\geq 1}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     G dgcAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)
\]

for the [[full subcategory]] of the [[homotopy category of a model category|homotopy category]] of the [[projective model structure on equivariant connective dgc-algebras]] on those [[equivariant dgc-algebras]] $A$ which for each $G/H \in G Orbits$ are

* connected: $H^0(A^H) \simeq \mathbb{Q}$

* simply connected: $H^1(A^H) \simeq 0$

* [[finite type]]: $dim_{\mathbb{Q}}\big( H^n(A^H) \big) \lt \infty$ for all $n \in \mathbb{N}$.

=--

([Scull 08, p. 12, 14](#Scull08))

## Statement

+-- {: .num_prop #FundamentalTheoremOfdgAlgebraicRationalHomotopyTheory} 
###### Proposition
**([[fundamental theorem of equivariant dg-algebraic rational homotopy theory]])**

The [[derived adjunction]]

$$
  Ho
  \left(
    \big(
      G dgcAlgebras^{\geq 0}_{k}
    \big)^{op}_{proj}
  \right)
  \underoverset
    {
      \underset
        {\;\;\; \mathbb{R} exp \;\;\;}
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
    G SimplicialSets_{Qu}
  \big)
$$

of the [[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]] (whose [[left adjoint]] is the [[equivariant PL de Rham complex]]-[[functor]]) has the following properties:

* on connected, simply connected, rationally finite equivariant homotopy types $X$ (eq:NilpotentQFiniteHomotopyTypes) the [[derived adjunction unit]] is [[equivariant rationalization]]

  $$
    \array{
    Ho
    \big(
       G SimplicialSets_{Qu}
    \big)^{fin_{\mathbb{Q}}}_{\geq 1, nil}
    &
      \overset{
      }{\longrightarrow}
    &
    Ho
    \big(
       G SimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
    \\
    X
    &\mapsto&
    \mathbb{R}\exp \circ \Omega^\bullet_{PLdR}(X)
    }    
  $$

  $$
    X
    \underoverset
      {\eta_X^{der}}
      {rationalization}
      {\longrightarrow}
    \mathbb{R}\exp \circ \Omega^\bullet_{PLdR}(X)
  $$

* on the [[full subcategories]] of connected, simply connected, and finite rational homotopy types from Def. \ref{NilpotententFiniteRationalHomotopyTypes} it restricts to an [[equivalence of categories]]:

  $$
    Ho
    \left(
      \big(
        G dgcAlgebras^{\geq 0}_{k}
      \big)^{op}_{proj}
    \right)^{\geq 1}_{fin}
    \underoverset
      {
        \underset
          {\;\;\; \mathbb{R} exp \;\;\;}
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
      G SimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
  $$


=--

([Scull 08, Theorem 5.5](#Scull08))




## Related concepts

* [[fundamental theorem of dg-algebraic rational homotopy theory]]


## References

* [[Marek Golasiński]], _Equivariant rational homotopy theory as a closed model category_, Journal of Pure and Applied Algebra Volume 133, Issue 3, 30 December 1998, Pages 271-287 (<a href="https://doi.org/10.1016/S0022-4049(97)00127-8">doi:10.1016/S0022-4049(97)00127-8</a>)

  (for Hamiltonian groups)


* {#Scull08} [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))


[[!redirects fundamental theorem of equivariant dg-algebraic rational homotopy theory]]

