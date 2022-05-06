
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

### Round weight systems

+-- {: .num_defn #LinearSpanOfChordDiagramsModulo4T}
###### Definition
**([[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] [[4T-relations|4T]])**

Let $k$ be a [[field]] (or just a [[commutative ring]]). Write 

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

\linebreak

### Horizontal weight systems


+-- {: .num_defn #LinearSpanOfHorizontalChordDiagramsModulo2TAnd4T}
###### Definition
**([[linear span]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] [[2T relation|2T]]/[[4T-relations|4T]])**

Let $k$ be a [[field]] (or just a [[commutative ring]]). Write 

1. $\mathcal{D}^{pb}$ for the [[set]] of [[horizontal chord diagrams]],

1. $k\langle \mathcal{D}^{pb}\rangle$ for its $k$-[[linear span]],

1. $\mathcal{A}^{pb} \;\coloneqq\; k\langle \mathcal{D}^c\rangle/(2T,4T)$ for the [[quotient vector space]] by the [[2T relations]] and [[horizontal 4T-relations]].

=--

(The superscript "${}^{pb}$"in Def. \ref{LinearSpanOfHorizontalChordDiagramsModulo2TAnd4T} is for _[[pure braids]]_, alluding to the fact that [[horizontal weight systems are associated graded of Vassiliev braid invaraints]].)

+-- {: .num_defn #HorizontalWeightSystems}
###### Definition
**([[horizontal weight system]])**

A _$k$-valued horizontal weight system_ is a [[linear function]] on the [[linear span]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] [[2T relation|2T]]&[[4T-relations]] (Def. \ref{LinearSpanOfHorizontalChordDiagramsModulo2TAnd4T})

$$
  w 
  \;\colon\;
  \mathcal{A}^{pb} \longrightarrow k
  \,,
$$

hence the $k$-[[vector space]] of horizontal weight systems is the [[dual vector space]]

\[
  \mathcal{W}_{pb}
  \;\coloneqq\;
  (\mathcal{A}^{pb})^\ast
\]

=--




## Constructions of weight systems

### Lie algebra weight systems
 {#LieAlgebraWeightSystems}

A large class of [[weight systems]] arises from reading a ([[horizontal chord diagram|horizontal]]) [[chord diagram]] as a [[string diagram]] in the evident way, and then labelling it by the structure morphisms of a [[Lie algebra object]] equipped with a [[Lie algebra representation]] [[internalization|internal to]] a suitable [[tensor category]]. This does yield weight systems because the required relations translate exactly to the structural equations satisfied by [[Lie modules]] ([[Jacobi identity]] and Lie action property).

The weight systems arising this way are called _[[Lie algebra weight systems]]_. See there for more.

Examples of [[weight systems]] which are _not_ [[Lie algebra weight systems]] are rare. Originally it was conjectured that none exist ([Bar-Natan 95, Conjecture 1](#BarNatan95), [Bar-Natan & Stoimenow 97, Conjecture 2.4](Lie+algebra+weight+system#BarNatanStoimenow97)). 

Eventually, a (counter-)example of a weight system which at least does not arise from any [[finite dimensional vector space|finite-dimensional]] [[super Lie algebra]] was given in [Vogel 11](Lie+algebra+weight+system#Vogel11).

### Stringy weight systems

[[stringy weight systems]]

### Rozansky-Witten weight systems

[[Rozansky-Witten weight systems]]

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
     \mathcal{W}_{pb}
     \;\coloneqq\;
     Hom_{\mathbb{Z} Mod}
     \big(
       \underset{
         \mathcal{A}^{pb}
       }{
         \underbrace{
           \mathbb{Z}
           \langle 
             \mathcal{D}^{pb}
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
    \underset{n \in \mathbb{N}}{\sqcup}
    \Omega 
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    (\mathbb{R}^3)
  \big)
  \;\simeq\;
  (\mathcal{W}_{pb})^\bullet
  \;\simeq\;
  Gr^\bullet( \mathcal{V}_{pb})
  \,.
$$

(the second equivalence on the right is the fact that [[weight systems are associated graded of Vassiliev invariants]]).

=--

This is stated as [Kohno 02, Theorem 4.1](#Kohno02)


#### For round chord diagrams

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

### As cohomology of the knot graph complex

[[cohomology of knot graph complex is weight systems on chord diagrams]]

### All horizontal weight systems are partitioned Lie algebra weight systems

* [[all horizontal weight systems are partitioned Lie algebra weight systems]]

## Related concepts

[[!include chord diagrams and weight systems -- table]]


* [[Kontsevich integral]]

## References

### General

Original articles:

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 4 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* {#JacksonMoffat19} [[David Jackson]], [[Iain Moffat]], Section 11.7 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

### Lie algebra weight systems

Discussion of [[Lie algebra weight systems]]

From the construction given in [Bar-Natan 95, Section 2.4](#BarNatan95) the interpretation of [[Lie algebra weight systems]] in terms of [[string diagrams]] for [[Lie algebra objects]] in [[tensor categories]] is evident, but standard textbooks in [[knot theory]]/[[combinatorics]] do not pick this up:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Chapter 6 of: _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], Section 14 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

The interpretation of Lie algebra weight systems as [[string diagram]]-calculus and generalization to [[Lie algebra objects]] (motivated by generalization at least to [[super Lie algebras]]) is made more explicit in

* {#Vaintrob94} [[Arkady Vaintrob]], _Vassiliev knot invariants and Lie S-algebras_, Mathematical Research Letters1, 579–595 (1994) ([pdf](https://pdfs.semanticscholar.org/bdc3/ac1d8da476245e2408e481a70b115b3e9aab.pdf))

* {#Vogel11} [[Pierre Vogel]], _Algebraic structures on modules of diagrams_, Journal of Pure and Applied Algebra, Volume 215, Issue 6, June 2011, Pages 1292-1339 ([doi:10.1016/j.jpaa.2010.08.013](https://doi.org/10.1016/j.jpaa.2010.08.013), [pdf](https://webusers.imj-prg.fr/~pierre.vogel/diagrams.pdf))

and fully explicit in

* {#RobertsWillerton06} [[Justin Roberts]], [[Simon Willerton]], Section 3 of: _On the Rozansky-Witten weight systems_, Algebr. Geom. Topol. 10 (2010) 1455-1519 ([arXiv:math/0602653](https://arxiv.org/abs/math/0602653))


See also 

* [[Vladimir Hinich]], [[Arkady Vaintrob]], _Cyclic operads and algebra of chord diagrams_, Sel. math., New ser. (2002) 8: 237 ([arXiv:math/0005197](https://arxiv.org/abs/math/0005197))

* E. Kulakova, S. Lando, T. Mukhutdinova, G. Rybnikov, _On a weight system conjecturally related to $\mathfrak{sl}_2$_, European Journal of Combinatorics Volume 41, October 2014, Pages 266-277 ([arXiv:1307.4933](https://arxiv.org/abs/1307.4933))

* Alexander Schrijver, _On Lie algebra weight systems for 3-graphs_ ([arXiv:1412.6923](https://arxiv.org/abs/1412.6923))


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

[[!include weight systems on chord diagrams in physics]]


[[!redirects weight systems]]

[[!redirects framed weight system]]
[[!redirects framed weight systems]]

[[!redirects unframed weight system]]
[[!redirects unframed weight systems]]

[[!redirects un-framed weight system]]
[[!redirects un-framed weight systems]]

[[!redirects horizontal weight system]]
[[!redirects horizontal weight systems]]


