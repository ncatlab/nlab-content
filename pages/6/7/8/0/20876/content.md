
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #InfinitesimalBraidLieAlgebra}
###### Definition
**([[infinitesimal braid Lie algebra]])**

For $D,n \in \mathbb{N}$ [[natural numbers]], let $F(\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}})$ be the [[free Lie algebra]] (over a given [[ground field]]) on [[generators and relations|generators]] $t_{i j}$ in degree $D-2$ with two indices ranging from 1 to $n$ and distinct.

The _infinitesimal braid relations_ are the following [[generators and relations|relations]] on the underlying [[vector space]] of the [[free construction|free]] [[Lie algebra]] on [[generators and relations|generators]] $\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}}$ 

\[
  \label{InfinitesimalBriadRelations}
  \left.
 \array{
    R0: \;\; & t_{i j} - (-1)^D t_{j i} & = 0 
    \\
    R1: \;\; & [t_{i j}, t_{k l}] & =  0  
    \\
    R2: \;\; & [t_{i k} + t_{j k}, t_{i j}] & = 0 
  }
  \;\;
  \right\}
  \phantom{AAA}
  {
  \text{for all pairwise distinct}
  \atop
  \text{tuples of indices}
  }
\]

This defines a quotient [[Lie algebra]] often denoted 

$$
  \mathcal{L}_n(D)
  \;\coloneqq\;
  F(\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}})
  /(R0, R1, R2)
 \,.
$$

=--

This is originally due to [Kohno 87 (1.1.4)](#Kohno87), it
appears also in [Kohno 88](#Kohno88), [Bar-Natan 96, Fact 3](#BarNatan96), [Fadell-Husseini 01](#FadellHusseini01), [Cohen-Gitler 01, Section 3](#CohenGitler01), [Cohen-Gitler 02, p. 2](#CohenGitler02).

## Properties

### Relation to horizontal chord diagrams

If $F(\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}})/R0$ is identified with the [[commutator]] Lie algebra of [[horizontal chord diagrams]] on $n$ strands under [[concatenation]] of diagrams along strands, as in 

<center>
<img src="https://ncatlab.org/nlab/files/AlgebraStrucOnSpanofHorizontalChordDiagrams.jpg" width="500">
</center>

then the remaining infinitesimal braid relations (eq:InfinitesimalBriadRelations) are equivalently the following:

R1 is the the [[2T relation]]:

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagram2TRelation.jpg" width="600">
</center>

R2 is the [[4T relation]]:

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagram4TRelation.jpg" width="600">
</center>

> graphics taken from [Sati-Schreiber 19b]()

Hence:

+-- {: .num_prop #UniversalEnvelopingOfInfinitesimalBraidsIsHorizontalChords}
###### Proposition
**([[universal enveloping algebra]] of [[infinitesimal braid Lie algebra]] is [[horizontal chord diagrams]] [[quotient vector space|modulo]] [[2T relations|2T]]&[[4T relations|4T]])

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
 

## Related concepts

* [[braid group]]

* [[Yang-Baxter equation]]

* [[weight systems are cohomology of loop space of configuration space]]

[[!include chord diagrams and weight systems -- table]]

## References

* {#Kohno87} [[Toshitake Kohno]], (1.1.4) in: _Monodromy representations of braid groups and Yang-Baxter equations_, Annales de l'Institut Fourier, Volume 37 (1987) no. 4, p. 139-160 ([doi:10.5802/aif.1114](https://doi.org/10.5802/aif.1114))



* {#Kohno88} [[Toshitake Kohno]], _Linear representations of braid groups and classical  Yang-Baxter equations_, in: [[Joan S. Birman]], Anatoly Libgober (eds.) _Braids_ Cont. Math. 78 (1988), 339-363 ([doi:10.1090/conm/078](http://dx.doi.org/10.1090/conm/078))

* {#BarNatan96} [[Dror Bar-Natan]], Fact 3 in: _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

* {#FadellHusseini01} [[Edward Fadell]], [[Sufian Husseini]], Theorem 2.2 in: _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 

* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], Section 3 in: _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#CohenGitler02} [[Fred Cohen]], [[Samuel Gitler]], p. 2 of: _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))

[[!redirects infinitesimal braid relations]]

[[!redirects infinitesimal braid Lie algebra]]
[[!redirects infinitesimal braid Lie algebras]]

[[!redirects universal enveloping of infinitesimal braids is horizontal chord diagrams]]
