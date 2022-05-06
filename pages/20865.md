
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

In [[knot theory]] a _framed weight system_ is an assignment of [[numbers]] to [[chord diagrams]] that is [[invariant]] under the [[4T-relation]]. 

If the assignment is in addition invariant under the [[1T-relation]], then it is called an _unframed weight system_, or just _weight system_, for short.

Similarly, in [[braid group]]-theory, a _horizontal weight system_ is an assignment of [[numbers]] to [[horizontal chord diagrams]] that is invariant under the horizontal [[2T relation]] and horizontal [[4T relation]].
 
## Definition

### Weight systems (circular)

+-- {: .num_defn #LinearSpanOfChordDiagramsModulo4T}
###### Definition
**([[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] [[4T-relations|4T]])**

Let $k$ be a [[field]] of [[characteristic zero]]. Write 

1. $\mathcal{D}^c$ for the [[set]] of [[chord diagrams]],

1. $k\langle \mathcal{D}^c\rangle$ for its $k$-[[linear span]],

1. $\mathcal{A}^c \;\coloneqq\; k\langle \mathcal{D}^c\rangle/4T$ for the [[quotient vector space]] by the [[4T-relations]].

=--

+-- {: .num_defn #FramedWeightSystems}
###### Definition
**([[framed weight system]])**

A _$k$-valued framed weight system_ is a [[linear function]] on the [[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] [[4T-relations]] (Def. \ref{LinearSpanOfChordDiagramsModulo4T})

$$
  w 
  \;\colon\;
  \mathcal{A}^c \longrightarrow k
  \,,
$$

hence the $k$-[[vector space]] of framed weight systems is the [[dual vector space]]

\[
  \mathcal{W}
  \;\coloneqq\;
  (\mathcal{A}^c)^\ast
\]

=--

([Bar-Natan 95, Def. 1.6](#BarNatan95), see [Chmutov-Duzhin-Mostovoy 11, Def. 4.1.1](#ChmutovDuzhinMostovoy11), [Jackson-Moffat 19, Section 11.7](#JacksonMoffat19))


+-- {: .num_remark}
###### Remark

Since [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]], framed weight systems equivalently form the [[dual vector space]]

\[
  \label{SpaceOfWeightSystemsAsLinearDual}
  \begin{aligned}
    \label{FramedWeightSystemsAsDualOfChordAndJacobiDiagrams}
    \overset{
       \mathclap{
         \color{blue}
         {
         {framed}
         \atop
         {{weight}\atop{systems}}
         }
       }
    }{
      \mathcal{W} 
    }
    & 
    \;\coloneqq\;
    \big(
       \overset
       {
         \color{blue}
         {
           {
             {chord}
             \atop
             {diagrams}
           }
           \atop
           { 
             {modulo}\,{4T}
           }
         }
       }
       {
         \mathcal{A}^c
       }
    \big)^\ast
    \\
    & 
    \;\simeq\;
    \big(
      \underset{
        \color{blue}
        {
          {
            {Jacobi}
            \atop
            {diagrams}
          }
          \atop
          {
            {modulo}\,{STU}
          }
        }
      }{
        \mathcal{A}^t
      }
    \big)^\ast
  \end{aligned}
\]

of the [[quotient vector space]] $\mathcal{A}^t \coloneqq k\langle \mathcal{D}^t \rangle/STU$ of the [[linear span]] of [[Jacobi diagrams]] by the [[STU-relation]].

=--

### Horizontal weight systems

(...)

## Properties

### As the associated graded space of Vassiliev invariants



+-- {: .num_prop #WeightSystemsAreAssociatedGradedOfVassilievInvariants}
###### Proposition
**([[weight systems are associated graded of Vassiliev invariants]])**

For [[ground field]] $k = \mathbb{R}, \mathbb{C}$ the [[real numbers]] or [[complex numbers]], there is for each [[natural number]] $n \in \mathbb{N}$ a canonical [[linear isomorphism]]

$$
  \mathcal{V}_n/\mathcal{V}_{n-1}
  \underoverset{\simeq}{\phantom{AAAA}}{\longrightarrow}
  \big( 
    \mathcal{A}_n^u
  \big)^\ast
$$

from 

1. the [[quotient vector space]] of order-$n$ [[Vassiliev invariants]] of [[knots]] by those of order $n-1$ 

1. to the space of [[unframed weight systems]] of order $n$.

In other words, in [[characteristic zero]], the [[graded vector space]] of [[unframed weight systems]] is the [[associated graded vector space]] of the [[filtered vector space]] of [[Vassiliev invariants]].

=--

([Bar-Natan 95, Theorem 1](#BarNatan95), following [Kontsevich 93](#Kontsevich93))


### As cohomology of loop spaces of configuration spaces
 {#AsCohomologyOfLoopSpacesOfConfigurationSpaces}


[[weight systems are cohomology of loop space of configuration space]]:

#### For horizontal chord diagrams

+-- {: .num_prop}
###### Proposition
**(integral [[horizontal weight systems]] are [[integral cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground ring]] $R = \mathbb{Z}$ the [[integers]], there is, for each [[natural number]] $n$, a canonical [[isomorphism]] of [[graded abelian groups]] between 

1. the integral [[weight systems]]

   $$
     \mathcal{W}^{pb}_n  
     \;\coloneqq\;
     Hom_{\mathbb{Z} Mod}
     \big(
       \underset{
         \mathcal{A}^{pb}_n
       }{
         \underbrace{
           \mathbb{Z}
           \langle 
             \mathcal{D}^{pb}_n 
           \rangle
           /(2T,4T)
         } 
       }
       ,
       \mathbb{Z}
     \big)
   $$

   on [[horizontal chord diagrams]] of $n$ strands (elements of the set $\mathcal{D}^{pb}$)

1. the [[integral cohomology]] of the [[based loop space]] of the [[ordered configuration space of n points]] in 3d [[Euclidean space]]:

$$
  H \mathbb{Z}^\bullet
  \big(
    \Omega 
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    (\mathbb{R}^3)
  \big)
  \;\simeq\;
  (\mathcal{W}^{pb}_n)^\bullet
  \;\simeq\;
  Gr^\bullet( \mathcal{V}^{pb}_n )
  \,.
$$

(the second equivalence on the right is the fact that [[weight systems are associated graded of Vassiliev invariants]]).

=--

This is stated as [Kohno 02, Theorem 4.1](#Kohno02)


#### For chord diagrams (circular)

+-- {: .num_prop}
###### Proposition
**([[weight systems]] are inside [[real cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground field]] $k = \mathbb{R}$ the [[real numbers]], 
there is a canonical [[injection]] of the [[real vector space]] $\mathcal{W}$ of [[framed weight systems]] ([here](weight+system#eq:SpaceOfWeightSystemsAsLinearDual)) into the [[real cohomology]] of the [[based loop spaces]] of the ordered [[configuration spaces of points]] in 3-[[dimension|dimensional]] [[Euclidean space]]:

$$
  \mathcal{W}
  \;\overset{\;\;\;\;}{\hookrightarrow}\;
  H\mathbb{R}^\bullet
  \Big(
    \underset{n \in \mathbb{N}}{\sqcup}
    \Omega 
    \underset{{}^{\{1,\cdots,n\}}}{Conf}
    \big(
      \mathbb{R}^3 
    \big)
  \Big)
$$

=--

This is stated as [Kohno 02, Theorem 4.2](#Kohno02)

\linebreak

Combining the above two propositions

1. [[weight systems are associated graded of Vassiliev invariants]],

1. [[weight systems are cohomology of loop space of configuration space]]

we get this situation:


<img src="https://ncatlab.org/nlab/files/VassilievInvInCohOfLoopSpacesOfConfigSpaces.jpg" width="600">


### Weight systems from Lie algebras

(...)

## Related concepts

[[!include chord diagrams and weight systems -- table]]


* [[Kontsevich integral]]

## References

### General

Textbook accounts

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 4 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* {#JacksonMoffat19} [[David Jackson]], [[Iain Moffat]], Section 11.7 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

### From Lie algebras

* E. Kulakova, S. Lando, T. Mukhutdinova, G. Rybnikov, _On a weight system conjecturally related to $\mathfrak{sl}_2$_, European Journal of Combinatorics Volume 41, October 2014, Pages 266-277 ([arXiv:1307.4933](https://arxiv.org/abs/1307.4933))


### As the associated graded space of Vassiliev invariants

On spaces of [[weight systems]] as the [[associated graded spaces]] of [[Vassiliev invariants]]:

* {#Kontsevich93} [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf))

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))


### As cohomology of loop spaces of configuration spaces

On [[weight systems]] as the [[real cohomology]] of [[based loop spaces]] of ordered [[configuration spaces of points]]:

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori and [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))


* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* [[Fred Cohen]], [[Samuel Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))

[[!redirects weight systems]]

[[!redirects framed weight system]]
[[!redirects framed weight systems]]

[[!redirects unframed weight system]]
[[!redirects unframed weight systems]]

[[!redirects un-framed weight system]]
[[!redirects un-framed weight systems]]

[[!redirects horizontal weight system]]
[[!redirects horizontal weight systems]]


