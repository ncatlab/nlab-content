
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Preliminaries

Write

\[
  \label{PolynomialDifferentialFormsOnSimplices}
  \Omega^\bullet_{polydR}
  (\Delta^\bullet)
  \;\colon\;
  \Delta^\op
  \longrightarrow
  dgcAlgebras^{\geq 0}_{\mathbb{R}}
\]

for the [[simplicial object]] in [[dgc-algebras]] given by [[polynomial differential forms on simplices]] over the [[real numbers]] (see also at [[fundamental theorem of dgc-algebraic homotopy theory]] -- [change of scalars](fundamental+theorem+of+dg-algebraic+rational+homotopy+theory#ChangeOfScalars)).


+-- {: .num_defn #PLdeRhamComplex} 
###### Definition
**([[PL de Rham complex]])**

The for $S \in $ [[sSet]] a [[simplicial set]], its PL de Rham complex is the
[[hom-object]] of [[simplicial objects]] from $S$ to $\Omega^\bullet_{polyDR}$ (eq:PolynomialDifferentialFormsOnSimplices), hence is the following [[end]] in [[dgcAlgebras]], here over the [[real numbers]]:

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

for the [[simplicial object]] in [[dgc-algebras]] (over the [[real numbers]]) given by smooth [[differential forms on simplices]].

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


## Statement


+-- {: .num_prop #PLdeRhamComplex} 
###### Proposition
**(PL de Rham complex of smooth manifold is equivalent to de Rham complex)**

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


* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))

[[!redirects the PL de Rham complex of a smooth manifold is equivalent to the de Rham complex]]

