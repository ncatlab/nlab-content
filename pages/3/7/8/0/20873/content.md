
> For discussion of standard round chord diagrams see at _[[chord diagram]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Knot theory
+-- {: .hide}
[[!include knot theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _horizontal chord diagram_ on $n$ strands is a finite undirected [[graph]] that is obtained from a trivalent graph with $n$ numbered embedded disjoint [[circles]] by cutting the circles open (to give the _strands_), such that the result has all edges not inside the circles (the _chords_) be vertically  ordered (i.e. along the strands) and going between distinct strands.

Here is an example of a horizontal chord diagram on 5 strands:


<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramOnFiveStrandsII.jpg" width="260">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Defintions


### Monoid of horizontal chord diagrams
 {#MonoidOfHorizontalChordDiagrams}

For $n \in \mathbb{N}$ (the *number of strands*), the *monoid of horizontal chord diagrams* is the [[free monoid]] 

\[
  \label{HorizontalChordDiagramsAsFreeMonoidOnChords}
  \mathcal{D}^{pb}_n
  \;\coloneqq\;
  FreeMonoid
  \Big(
    \big\{
      (i j)
      \,\vert\,
      1 \leq i \lt j \leq n
    \big\}
  \Big)
\]

on the [[set]] of pairs of distinct elements of $\{1, \cdots, n\}$, i.e. of pairs of strands, called the *chords* (the traditional superscript $pb$ is for _[[pure braids]]_).

Hence a horizontal chord diagram is equivalently a finite [[list]] of chords

$$
  D 
  \;=\;
  (i_d j_d)
    \cdot 
    \cdots
    \cdot
  (i_2 j_2)
    \cdot
  (i_1 j_1)
$$

and the product of chord diagrams is the concatenation of these list, with the [[empty list]] being the [[neutral element]].

The [[function]] that sends the chord $(i j)$ to that [[permutation]] of $n$ elements (strands) which is given by the [[transposition]] $t_{i j}$ of the $i$th with the $j$th strand extends to a unique [[monoid]] [[homomorphism]] from the monoid of horizontal chord diagrams (eq:HorizontalChordDiagramsAsFreeMonoidOnChords) to the [[symmetric group]] on $n$ elements:

$$
  \array{
    \mathcal{D}^{pn}_n
    &\overset{perm}{\longrightarrow}&
    Sym(n)
    \\
    (i_d j_d)
      \cdot \cdots \cdot
    (i_1 j_1)
    &\mapsto&
    t_{i_d j_d}
      \circ
    \cdots
      \circ
    t_{i_1 j_1}
    \,.
  }
$$



### Closure to round chord diagrams
 {#TraceToRoundChordDiagrams}

Given a [[horizontal chord diagram]] on $n$ strands and given any choice of [[cyclic permutation]] of $n$ elements, the [[trace of horizontal to round chord diagrams]] is the [[round chord diagram]] obtained by gluing the ends of the strands according to the cyclic permutation, and retaining the chords in the evident way.

The following shows an example of the trace operation for [[cyclic permutation]] of strands one step to the left:

<center>
<img src="https://ncatlab.org/nlab/files/TracingHorizontalChordDiagram.jpg" width="600">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

The following are the analogous traces of the four types of horizontal chord diagrams appearing in the [[4T relation]]:

<center>
<img src="https://ncatlab.org/nlab/files/TracingHorizontalChordDiagramsExamplesI.jpg" width="800">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

This defines a [[function]]

$$
  tr \;\colon\; \mathcal{C}^{pb} \longrightarrow \mathcal{C}^c
$$

from the [[set]] of [[horizontal chord diagrams]] to the set of [[round chord diagrams]].

### Algebra of horizontal chord diagrams
 {#AlgebraOfHorizontalChordDiagrams}

+-- {: .num_defn #AlgebraHorizontalChordDiagrams}
###### Definition

For $n \in \mathbb{N}$ and for , the [[linear span]] $Span\big( \mathcal{D}_n^{pb}\big)$ on the set of horizontal chord diagrams on $n$ strands becomes an [[graded algebra|graded]] [[associative algebra]] 

$$
  \big( Span\big( \mathcal{D}_n^{pb}\big), \circ \big)
$$

under [[concatenation]] of strands. 

=--

For example:

<center>
<img src="https://ncatlab.org/nlab/files/AlgebraStrucOnSpanofHorizontalChordDiagrams.jpg" width="500">
</center>


### The 2T- and 4T-relations
 {#The2TAnd4TRelations}

+-- {: .num_defn #2TAnd4TRelations}
###### Definition

On the $R$-[[module]] $R\langle \mathcal{D}^{pb}\rangle$ of [[horizontal chord diagrams]] consider the following [[relations]]:

The [[2T relations]]:

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagram2TRelation.jpg" width="600">
</center>

and the [[4T relations]]:

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagram4TRelation.jpg" width="600">
</center>

=--

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

In terms of the [[commutator]] [[Lie algebra]] of the [above](#AlgebraOfHorizontalChordDiagrams) algebra $\big( R\langle \mathcal{D}^{pb}\rangle, \circ \big)$ of horizontal chord diagrams, these are the [[infinitesimal braid relations]].

One writes

\[
  \label{QuotientModule}
  \mathcal{A}^{{}^{pb}}
  \;\coloneqq\;
  R\langle \mathcal{D}^{pb}\rangle/(2T,4T)
\]

for the [[quotient algebra]] of horizontal chord diagrams by these relations.

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramsModulo2TAnd4T.jpg" width="900">
</center>


### Universal enveloping of infinitesimal braid relations

+-- {: .num_prop #UniversalEnvelopingOfInfinitesimalBraidsIsHorizontalChords}
###### Proposition
**([[universal enveloping algebra]] of [[infinitesimal braid Lie algebra]] is [[horizontal chord diagrams]] [[quotient vector space|modulo]] [[2T relations|2T]]&[[4T relations|4T]])

The [[associative algebra]] (eq:QuotientModule)

$$
  \Big(
  \mathcal{A}_n^{{}^{pb}}
  \;\coloneqq\;
  Span
  \big( 
    \mathcal{D}_n^{pb}
  \big)/(2T, 4T)
  ,
  \circ
  \Big)
$$

of [[horizontal chord diagrams]] on $n$ strands with product given by [[concatenation]] of strands (Def. \ref{AlgebraHorizontalChordDiagrams}) [[quotient vector space|modulo]] the [[2T relations]] and [[4T relations]] (Def. \ref{2TAnd4TRelations}) is [[isomorphism|isomorphic]] to the [[universal enveloping algebra]] of the [[infinitesimal braid Lie algebra]] ([this Def.](infinitesimal+braid+relation#InfinitesimalBraidLieAlgebra)):

$$
  \big(\mathcal{A}_n^{pb}, \circ\big)
  \;\simeq\;
  \mathcal{U}(\mathcal{L}_n(D))
  \,.
$$

=--


### Horizontal weight systems

An $R$-[[linear map]] from the [[quotient module]] (eq:QuotientModule) of [[horizontal chord diagrams]] to $R$

\[
  \label{AHorizontalWeightSystem}
  w
  \;\colon\;
  \mathcal{A}_n^{{}^{pb}}
  \longrightarrow
  R
\]

is called a _[[weight system]]_ on horizontal chord diagrams (of $n$ strands), or maybe a _[[horizontal weight systems]]_.

Hence for $R = k$ a [[field]], the [[vector space]] of all horizontal weight systems is the degreewise [[dual vector space]]

$$
  \mathcal{W}_{pb}
  \;\coloneqq\;
  \big(
    \mathcal{A}^{pb} 
  \big)^\ast
$$

([Bar-Natan 96, p. 3](#BarNatan96))


### Star-algebra structure
 {#StarAlgebraStructure}

Over a [[ground ring]] $R$ that is itself equipped with the [[mathematical structure|structure]] of a [[star-algebra]] $\mathbb{F} \overset{(-)^\ast}{\to} \mathbb{F}$ (such as the [[real numbers]], trivially, or the [[complex numbers]] via [[complex conjugation]]), we have that 
also the [[associative algebra]] (eq:QuotientModule)

$$
  \Big(
  \mathcal{A}_n^{{}^{pb}}
  \;\coloneqq\;
  Span
  \big( 
    \mathcal{D}_n^{pb}
  \big)/(2T, 4T)
  ,
  \circ
  \Big)
$$

of [[horizontal chord diagrams]] on $n$ strands with product given by [[concatenation]] of strands (Def. \ref{AlgebraHorizontalChordDiagrams}) [[quotient vector space|modulo]] the [[2T relations]] and [[4T relations]] (Def. \ref{2TAnd4TRelations}) 

becomes a [[star-algebra]]  with star-operation

$$
  (-)^\ast
  \;:\;
  \mathcal{A}_n^{{}^{pb}}
  \longrightarrow
  \mathcal{A}_n^{{}^{pb}}
$$

given by reversing the [[orientation]] of strands:

<center>
<img src="https://ncatlab.org/nlab/files/StarOperationOnAHorizontalChordDiagram.jpg" width="560">
</center>

Since [[horizontal chord diagrams are the homology of the loop space of configuration space]] and the [[homology of a loop space]] is an [[involutive Hopf algebra]], this is a special case of the general fact that involutive Hopf algebras are star-algebras ([here](star-algebra#InvolutiveHopfAlgebrasAreStarAlgebras)).

With respect to this [[star-algebra]]-[[mathematical structure|structure]] one may ask (setting $R \coloneqq \mathbb{C}$ for definiteness) whether a given [[weight system]] (eq:AHorizontalWeightSystem)

$$
  w
  \;\colon\;
  \mathcal{A}_n^{{}^{pb}}
  \longrightarrow
  \mathcal{C}
$$

is a [[state on a star-algebra]] in that for any $D \in \mathcal{A}_n^{{}^{pb}}$ we have that the value of $w$ on the corresponding [[normal operator]] $D \cdot D^\ast$ is a non-[[negative number|negative]] [[real number]]:

$$
  \Big(
    w \in \mathcal{W}_n^{{}^{pb}}
    \;
    \text{is a state}
  \Big)
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \left(
    \begin{aligned}
      \text{1.}\;\;\;
      &
      w(1) = 1
      \\
      \text{2.}\;\;\;
      &
      \underset{
        \mathclap{
          D \in \mathcal{A}_n^{{}^{pb}}
        }
      }{
        \forall 
      }
      \;\;\;\;
      \Big(
        w(D \cdot D^\ast)
        \;
          \geq 0
        \;
        \in
        \mathbb{R} 
        \subset
        \mathbb{C}
      \Big)
    \end{aligned}
  \right)
  \,.
$$


The [[weight systems]] which are [[states on a star-algebra]] with respect to this star-involution are discussed in [CSS 21](#CSS21).



### Closure to Sullivan chord diagrams
 {#ClosureToSullivanChordDiagrams}

More generally, one obtains [[Sullivan chord diagrams]] with $p$ disjoint embedded circles from [[horizontal chord diagrams]] by closing up strands after acting with a [[permutation]] with $p$ cycles ($p$ [[orbits]])

<center>
<img src="https://ncatlab.org/nlab/files/ClosingHorizontalChordsToSullivanChordsIII.jpg" width="800">
</center>

> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Applications

### Knizhnik-Zamolodchicov connection

[[!include Knizhnik-Zamolodchikov-Kontsevich construction -- definition]]


[[!include chord diagrams as multi-trace observables in BMN matrix model -- example]]



## Related concepts

[[!include chord diagrams and weight systems -- table]]


## References

Original articles

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* [[Adrien Brochier]], _Cyclotomic associators and finite type invariants for tangles in the solid torus_, Algebr. Geom. Topol. 13 (2013) 3365-3409 ([arXiv:1209.0417](https://arxiv.org/abs/1209.0417))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 5.11 of: _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

Discussion of the [[star-algebra]]-structure and associated [[state on a star-algebra|states]] on horizontal chord diagrams:

* {#CSS21} [[David Corfield]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Fundamental weight systems are quantum states]]* ([arXiv:2105.02871](https://arxiv.org/abs/2105.02871))



[[!redirects horizontal chord diagrams]]
