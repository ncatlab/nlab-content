
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

## Statement

### For horizontal chord diagrams

+-- {: .num_remark #HomologyOfBasedLoopSpaceIsHopfAlgebra}
###### Remark
**([[Hopf algebra]]-[[mathematical structure|structures]])**

Both the [[ordinary homology]] of a [[based loop space]] as well as the [[universal enveloping algebra]] of a [[Lie algebra]] are canonically [[Hopf algebras]], the former via the [[Pontrjagin ring]]-[[mathematical structure|structure]] (see at _[[homology of loop spaces]]_).

=--

+-- {: .num_prop #HomologyOfLoopSpaceOfConfigurationSpaceIsUniversalEnvelopingOfInfinitesimalBraids}
###### Proposition
**([[ordinary homology]] of [[based loop space]] of [[ordered configuration space of points]] is [[universal enveloping algebra]] of [[infinitesimal braid Lie algebra]])**

For $D, n \in \mathbb{N}$ [[natural numbers]] and for any [[ground field]] $\mathbb{F}$ (in fact over every [[commutative ring]]) the [[ordinary homology]] of the [[based loop space]] of the [[ordered configuration space of points]] in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^D$ is [[isomorphism|isomorphic]], as a [[Hopf algebra]] (Remark \ref{HomologyOfBasedLoopSpaceIsHopfAlgebra}),  to the [[universal enveloping algebra]] of the [[infinitesimal braid Lie algebra]]:

$$
  H_\bullet
  \big(
    \Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}(\mathbb{R}^D)
  \big)
  \;\simeq\;
  \mathcal{U}
  \big(
    \mathcal{L}_n(D)
  \big)
  \,.
$$

=--

This is due to [Fadell-Husseini 01, Theorem 2.2](#FadellHusseini01), re-stated as [Cohen-Gitler 01, Theorem 4.1](#CohenGitler01), [Cohen-Gitler 02, Theorem 2.3](#CohenGitler02).

Notice also that:

+-- {: .num_prop #UniversalEnvelopingOfInfinitesimalBraidsIsHorizontalChords}
###### Proposition
**([[universal enveloping of infinitesimal braids is horizontal chord diagrams]])

The [[associative algebra]] 

$$
  \Big(
  \mathcal{A}_n^{pb}
  \;\coloneqq\;
  Span
  \big( 
    \mathcal{D}_n^{pb}
  \big)/(2T, 4T)
  ,
  \circ
  \Big)
$$

of [[horizontal chord diagrams]] on $n$ strands with product given by [[concatenation]] of strands ([this Def.](horizontal+chord+diagram#AlgebraHorizontalChordDiagrams)), [[quotient vector space|modulo]] the [[2T relations]] and [[4T relations]] ([this Def.](horizontal+chord+diagram#2TAnd4TRelations)) is [[isomorphism|isomorphic]] to the [[universal enveloping algebra]] of the [[infinitesimal braid Lie algebra]] (Def. \ref{InfinitesimalBraidLieAlgebra}):

$$
  \big(\mathcal{A}_n^{pb}, \circ\big)
  \;\simeq\;
  \mathcal{U}(\mathcal{L}_n(D))
  \,.
$$

=--
 

The combination of Prop. \ref{HomologyOfLoopSpaceOfConfigurationSpaceIsUniversalEnvelopingOfInfinitesimalBraids} and Prop. \ref{UniversalEnvelopingOfInfinitesimalBraidsIsHorizontalChords} yields:

+-- {: .num_cor #HomologyOfLoopSpaceOfConfigurationSpaceIsAlgebraOfHorizontalChordDiagrams}
###### Corollary

For $D, n \in \mathbb{N}$ and for any [[ground field]] $\mathbb{F}$ (in fact over every [[commutative ring]]) the [[ordinary homology]] of the [[based loop space]] of the [[ordered configuration space of points]] in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^D$ is [[isomorphism|isomorphic]], as a [[Hopf algebra]], to the [[associative algebra]] of [[horizontal chord diagrams]] on $n$ strands with product given by [[concatenation]] of strands ([this Def.](horizontal+chord+diagram#AlgebraHorizontalChordDiagrams)), [[quotient vector space|modulo]] the [[2T relations]] and [[4T relations]] ([this Def.](horizontal+chord+diagram#2TAnd4TRelations)):

$$
  H_\bullet
  \big(
    \Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}(\mathbb{R}^D)
  \big)
  \;\simeq\;
  \big(\mathcal{A}_n^{pb}, \circ\big)
  \,.
$$




=--



### For horizontal weight systems

+-- {: .num_prop}
###### Proposition
**(integral [[horizontal weight systems]] are [[integral cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

Given any [[ground field]] $\mathbb{F}$ (in fact any [[ground ring]], notably the [[integers]]) there is, for each [[natural number]] $n$, a canonical [[isomorphism]] of [[graded abelian groups]] between 

1. the [[weight systems]]

   $$
     \mathcal{W}_n^{pb}
     \;\coloneqq\;
     Hom_{\mathbb{F} Mod}
     \big(
       \underset{
         \mathcal{A}_n^{pb}
       }{
         \underbrace{
           Span
           \big(
             \mathcal{D}_n^{pb}
           \big)
           /(2T,4T)
         } 
       }
       ,
       \mathbb{F}
     \big)
   $$

   on [[horizontal chord diagrams]] of $n$ strands (elements of the set $\mathcal{D}^{pb}$)

1. the [[ordinary cohomology]] of the [[based loop space]] of the [[ordered configuration space of n points]] in [[Euclidean space]]:

$$
  H^\bullet
  \big(
    \Omega 
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    (\mathbb{R}^D)
  \big)
  \;\simeq\;
  (\mathcal{W}_n^{pb})^\bullet
  \;\simeq\;
  Gr^\bullet( \mathcal{V}_{pb} )
  \,.
$$

(the second equivalence on the right is the fact that [[weight systems are associated graded of Vassiliev invariants]], for $D =3$).

=--

This appears stated as [Kohno 02, Theorem 4.1](#Kohno02); it follows immediately by Corollary \ref{HomologyOfLoopSpaceOfConfigurationSpaceIsAlgebraOfHorizontalChordDiagrams} of Prop. \ref{HomologyOfLoopSpaceOfConfigurationSpaceIsUniversalEnvelopingOfInfinitesimalBraids}.



### For round weight systems

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

## Related theorems


[[!include facts about chord diagrams and weight systems -- contents]]


## Related concepts

[[!include chord diagrams and weight systems -- table]]

## References

The statement relating the [[ordinary homology]] of the [[based loop space]] of the [[ordered configuration space of points]] to the [[universal enveloping algebra]] of the [[infinitesimal braid Lie algebra]]:

* {#FadellHusseini01} [[Edward Fadell]], [[Sufian Husseini]], Theorem 2.2 in: _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001) ([MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), [doi:10.1007/978-3-642-56446-8](https://link.springer.com/book/10.1007/978-3-642-56446-8))

* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], Theorem 4.1 of: _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#CohenGitler02} [[Fred Cohen]], [[Samuel Gitler]], Theorem 2.3 of: _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))


The dual statement identifying the [[ordinary cohomology]] of the [[based loop space]] of the [[ordered configuration space of points]] with the space of [[weight systems]] on [[horizontal chord diagrams]]:

* {#Kohno02} [[Toshitake Kohno]], Theorem 4.1 in: _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

See also:

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori and [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))


[[!redirects horizontal weight systems are cohomology of loop space of configuration space]]
