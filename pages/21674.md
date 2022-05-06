
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

The concept of the _PL de Rham complex_ ([Bousfield-Gugenheim 76](#BousfieldGugenheim76), [Sullivan 77](#Sullivan77)) is a variant of that of the [[de Rham complex]] for [[smooth manifolds]] which applies to general [[topological spaces]] and [[simplicial sets]].

The terminology "PL" for "piecewise linear" seems to have been tacitly introduced in [Bousfield-Gugenheim 76](#BousfieldGugenheim76). Beware that despite this commonly adopted terminology (e.g. [Griffith-Morgan 13](#GriffithMorgan13)), the PL de Rham complex consist of piecewise _[[polynomial differential forms|polynomial]]_ [[differential forms]], but polynomial with respect to a piecewise linear structure on the domain space/complex. 

In analogy to the [[de Rham theorem]] for [[smooth manifolds]], the fundamental theorem of  dg-algebraic rational homotopy theory shows that the PL de Rham complex computes the [[rational cohomology]] (or [[real cohomology]], [[complex cohomology]]) of the given [[topological space]]/[[simplicial sets]].

Applied to a topological space that happens to carry the structure of a [[smooth manifold]], the PL de Rham complex is connected by a [[zig-zag]] of [[quasi-isomorphisms]] to the smooth [[de Rham complex]], hence both are [[isomorphism|isomorphic]] in the [[homotopy category]] of the [[model structure on connective dgc-algebras]].

## Definition


Let $k \in \{\mathbb{Q}, \mathbb{R}, \mathbb{C}\}$.

Write

\[
  \label{PolynomialDifferentialFormsOnSimplices}
  \Omega^\bullet_{polydR}
  (\Delta^\bullet)
  \;\colon\;
  \Delta^\op
  \longrightarrow
  dgcAlgebras^{\geq 0}_{k}
\]

for the [[simplicial object]] in [[dgc-algebras]] given by [[polynomial differential forms on simplices]].


+-- {: .num_defn #PLdeRhamComplex} 
###### Definition
**([[PL de Rham complex]])**

The for $S \in $ [[sSet]] a [[simplicial set]], its PL de Rham complex is the
[[hom-object]] of [[simplicial objects]] from $S$ to $\Omega^\bullet_{polyDR}$ (eq:PolynomialDifferentialFormsOnSimplices), hence is the following [[end]] in [[dgcAlgebras]]:

\[
  \label{PLdERhamComplexOfSimplicialSet}
  \Omega^\bullet_{PLdR}(S)
  \;\coloneqq\;
  sSet
  \big(
    S,\,
    \Omega^\bullet_{polydR}(\Delta^\bullet)
  \big)
  \;\coloneqq\;
  \underset{
     [n] \in \Delta^{op}
  }{\int}
  \underset{
    S_n
  }{\oplus}
  \Omega^\bullet_{polydR}
  \big(
    \Delta^n
  \big)
  \,.
\]

=--

([Bousfield-Gugenheim 76, Sec. 2, p. 7](#BousfieldGugenheim76))

For $X \in $ [[Top]] a [[topological space]] its _PL de Rham complex_ is the PL de Rham complex as in (eq:PLdERhamComplexOfSimplicialSet) of its [[singular simplicial complex]]:

$$
  \Omega^\bullet_{PLdR}(X)
  \;\coloneqq\;
  \Omega^\bullet_{PLdR}
  \big(
    Sing(X)
  \big)
  \,.
$$

The [[cochain cohomology]] of the PL de Rham complex is _PL de Rham cohomology_

\[
  \label{PLdeRhamCohomology}
  H^\bullet_{PLdR}(-)
  \;\coloneqq\;
  H \Omega^\bullet_{PLdR}(-)
  \,.
\]


## Properties

### Relation to simplicial sets

+-- {: .num_prop} 
###### Proposition
**([[Quillen adjunction between simplicial sets and connective dgc-algebras]])**

The [[PL de Rham complex]]-construction (Def. \ref{PLdeRhamComplex}) is the [[left adjoint]] in a [[Quillen adjunction]] between


* the [[opposite model structure|opposite]] of the [[projective model structure on connective dgc-algebras]]

* the [[classical model structure on simplicial sets]]

$$
  \big(
    DiffGradedCommAlgebras^{\geq 0}_{k}
  \big)^{op}_{proj}
  \underoverset
    {
      \underset
        {\;\;\; exp \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\;\Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot_{\mathrlap{Qu}}}
  SimplicialSets_{Qu}
$$

=--

+-- {: .proof}
###### Proof

That the [[PL de Rham complex]] [[functor]] preserves [[cofibrations]], hence sends injections of simplicial sets to surjections of dgc-algebras, is immediate from its construction.

That its [[right adjoint]] preserves fibrations, hence sends cofibrations of dgc-algebras to [[Kan fibrations]], is the statement of [Bousfield-Gugenheim 76, Lemma 8.2](#BousfieldGugenheim76).

=--


### Relation to rational cohomology
  {#RelationToRationalCohomology}

+-- {: .num_prop #PLdeRhamTheorem} 
###### Proposition
**([[PL de Rham theorem]])**

Let $k$ be a [[field]] of [[characteristic zero]] (such as the [[rational numbers]], [[real numbers]] or [[complex numbers]]). 

Then the evident operation of [[integration of differential forms]] over [[simplices]] induces a [[quasi-isomorphism]] between the [[PL de Rham complex]] with coefficients in $k$ (Def. \ref{PLdeRhamComplex}}) and [[cochain complex]] for [[singular cohomology]] with [[coefficients]] in $k$

$$
  \Omega^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  C^\bullet(X; k)
$$

and hence an [[isomorphism]] from [[PL de Rham cohomology]] (eq:PLdeRhamCohomology) to [[ordinary cohomology]] with [[coefficients]] in $k$ (such as [[rational cohomology]], [[real cohomology]], [[complex cohomology]]):

$$
  H^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  H^\bullet(X; k)
$$

(for $X$ any [[topological space]]).

=--

([Bousfield-Gugenheim 76, Theorem 2.2](#BousfieldGugenheim76))


### Relation to smooth de Rham complex
 {#RelationToSmoothdeRhamComplex}

Write

\[
  \label{SmoothDifferentialFormsOnSimplices}
  \Omega^\bullet_{dR}
  (-)
  \;\colon\;
  \Delta^\op
  \longrightarrow
  dgcAlgebras^{\geq 0}_{\mathbb{R}}
\]

for the [[simplicial object]] in [[dgc-algebras]] given by smooth [[differential forms on simplices]].

+-- {: .num_defn #PSdeRhamComplex} 
###### Definition
**(PS de Rham complex)**

The for $S \in $ [[sSet]] a [[simplicial set]], its _PS de Rham complex_ ("piecewise smooth") is the [[hom-object]] of [[simplicial objects]] from $S$ to $\Omega^\bullet_{dR}(\Delta^\bullet)$ (eq:SmoothDifferentialFormsOnSimplices), hence is the following [[end]] in [[dgcAlgebras]]:

\[
  \label{PSdERhamComplexOfSimplicialSet}
  \Omega^\bullet_{PSdR}(S)
  \;\coloneqq\;
  sSet
  \big(
    S,\,
    \Omega^\bullet_{dR}(\Delta^\bullet)
  \big)
  \;\coloneqq\;
  \underset{
     [n] \in \Delta^{op}
  }{\int}
  \underset{
    S_n
  }{\oplus}
  \Omega^\bullet_{dR}
  \big(
    \Delta^n
  \big)
  \,.
\]

=--

This receives an evident inclusion from the PL de Rham complex (eq:PSdERhamComplexOfSimplicialSet):

\[
  \label{InclusionOfPolynomialFormsIntoSmoothFormsOnSimplices}
  \Omega_{PLdR}^\bullet(-)
  \overset{
    \phantom{AA} i_{poly} \phantom{AA}
  }{\hookrightarrow}
  \Omega_{PSdR}^\bullet(-)
\]


For $X$ a [[smooth manifold]], and $S(X)$ the [[simplicial complex]] given by any smooth [[triangulation]], notice that:

* there is a [[homeomorphism]] of [[topological spaces]]

  $$
    S(X) \overset{p}{\longrightarrow} X
  $$

  which restricts to a [[diffeomorphism]] onto its image in the [[interior]] of any [[simplex]]

* there is a [[weak homotopy equivalence]] of [[simplicial sets]]

  $$
    S(X) 
      \overset{ \phantom{AA} i \phantom{AA} }{\hookrightarrow}
    Sing(X)
    =
    Sing\big( \left\vert S(X)\right\vert \big)
  $$

  into the [[singular simplicial set]] of $X$ (this being the [[adjunction unit]] of the $\left\vert - \right\vert \dashv Sing$ [[Quillen equivalence]] between the [[classical model structure on simplicial sets]] and the [[classical model structure on topological spaces]], and in fact equivalently the derived adjunction unit, since $\left\vert -\right\vert$ preserves all weak equivalences, and $Sing$ those between CW-complexes, by [[Ken Brown's lemma]]).



+-- {: .num_defn #PLdeRhamComplex} 
###### Definition
**([[PL de Rham complex of smooth manifold is equivalent to de Rham complex]])**

Let $X$ be a [[smooth manifold]].

We have the following [[zig-zag]] of [[dgc-algebra]] [[quasi-isomorphisms]] between the [[PL de Rham complex]] of (the [[topological space]] underlying) $X$ and the smooth [[de Rham complex]] of $X$:

$$
  \array{
    &&
    \Omega^\bullet_{PLdR}
    \big(
      S(X)
    \big)    
    &&
    &&
    \Omega^\bullet_{dR}(X)
    \\
    &
      {}^{
        \mathllap{
          i^\ast
        }
      }
      \nearrow
    & &
      \searrow^{
        \mathrlap{
          i_{poly}
        }
      }
    & & 
      {}^{
        \mathllap{
          p^\ast
        }
      }
      \swarrow
    \\
    \mathllap{
      \Omega^\bullet_{PLdR}(X)
      \;=\;
    }
    \Omega^\bullet_{PLdR}
    \big(
      Sing(X)
    \big)
    && && 
    \Omega^\bullet_{PSdR}
    \big(
      S(X)
    \big)
  }
$$

Here $S(X)$ is the [[simplicial complex]] corresponding to any smooth [[triangulation]] of $X$.

=--

+-- {: .proof}
###### Proof

For the two morphisms on the right this is [Griffith-Morgan 13, Cor. 9.9](#GriffithMorgan13).

For the morphism on the left this follows since $S(X) \hookrightarrow Sing(X)$ is a [[weak homotopy equivalence]] and since $\Omega^\bullet_{PLdR}$, being a [[left Quillen functor]] preserves weak equivalences between [[cofibrant objects]] (where every simplicial set being cofibrant), by [[Ken Brown's lemma]].


=--



## References

* {#Sullivan77} [[Dennis Sullivan]], _Infinitesimal computations in topology_, Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 ([numdam:PMIHES_1977__47__269_0](http://www.numdam.org/item/PMIHES_1977__47__269_0/))

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))

[[!redirects PL de Rham complexes]]

[[!redirects PL de Rham cohomology]]
