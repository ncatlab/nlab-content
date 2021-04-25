
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Knot theory
+-- {: .hide}
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

## Idea
 {#Idea}

In [[knot theory]], a large class of [[weight systems]] arises from reading a ([[horizontal chord diagram|horizontal]]) [[chord diagram]] as a [[string diagram]] in the evident way, and then labeling it by the structure morphisms of a [[metric Lie algebra|metric]] [[Lie algebra object]] equipped with a [[metric Lie representation|metric]] [[Lie algebra representation]] [[internalization|internal to]] a suitable [[tensor category]]. 

<center>
<img src="https://ncatlab.org/nlab/files/LieAlgebraWeightSystemAssignment.jpg" width="600">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

This does yield weight systems, because, using that [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]], the required [[STU-relations]] translate into the structural equations satisfied by [[Lie modules]] ([[Jacobi identity]] and Lie action property); see [Roberts & Willerton 06, Theorem 3.1](#RobertsWillerton06), following [Vaintrob 94](#Vaintrob94), [Vogel 11](#Vogel11) following [Bar-Natan 95, 2.4](#BarNatan95), [Bar-Natan 96](#BarNatan96) following [Kontsevich 94](#Kontsevich94).

The [[weight systems]] arising this way are called _Lie algebra weight systems_.

## Properties

### Ubiquity

#### On round chord diagrams

Examples of [[weight systems]] on (ordinary, round) [[chord diagrams]] which are _not_ Lie algebra weight systems are rare. Originally it was conjectured that none exist ([Bar-Natan 95, Conjecture 1](#BarNatan95), [Bar-Natan & Stoimenow 97, Conjecture 2.4](#BarNatanStoimenow97)).  

Eventually, a (counter-)example of a weight system which at least does not arise from any [[finite dimensional vector space|finite-dimensional]] [[super Lie algebra]] was given in [Vogel 11](#Vogel11).

#### On horizontal chord diagrams

For [[horizontal chord diagrams]] we have: 

* _[[all horizontal weight systems are partitioned Lie algebra weight systems]]_ ([Bar-Natan 96](#BarNatan96))

* the [[fundamental representation|fundamental]] [[general linear Lie algebra|$\mathfrak{gl}(n)$]]-weight system coincides with the [[Cayley distance kernel]] at [[inverse temperature]] $\beta = \ln(n)$ ([CSS21](#CSS21))

### Stringy weight systems span classical Lie algebra weight systems

[[stringy weight systems span classical Lie algebra weight systems]]

### Relation to Adams operations

On the [[vector space]] $\mathcal{A}$ of [[Jacobi diagrams]] [[quotient vector space|modulo]] [[STU-relations]] ([[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] [[chord diagrams]] [[quotient vector space|modulo]] [[4T relations]])  there is a system of [[linear maps]] (for $q \in \mathbb{Z}$, $q \neq 0$)

$$
  \psi^q
  \;\colon\;
  \mathcal{A}
  \longrightarrow
  \mathcal{A}
$$

which respect the [[coalgebra]] [[mathematical structure|structure]] and satisfy

$$
  \psi^{q_2} \circ \psi^q_1
  \;=\;
  \psi^{q_1 \cdot q_2}
$$

and as such are (dually) analogous to the [[Adams operations]] on [[topological K-theory]].

([Bar-Natan 95, Def. 3.11 & Theorem 7](#BarNatan95))

In fact, when evaluated in [[Lie algebra weight systems]] $w_{\mathbf{N}}$ and under the identification (see [here](equivariant+K-theory#RelationToRepresentationTheory)) of the [[representation ring]] of a [[compact Lie group]] $G$ with the $G$-[[equivariant K-theory]] of the point, these Adams operations on [[Jacobi diagrams]] correspond to the [[Adams operations]] on [[equivariant K-theory]]:


$$
  w_{\mathbf{N}}(\psi^q D)
  \;=\;
  w_{\psi^q \mathbf{N}}(D)
  \,.
$$

([Bar-Natan 95, Exc. 6.24](#BarNatan95)
)

For more see at _[[Adams operation on Jacobi diagrams]]_.


### As expectation values of single trace observables
 {#AsExpectationValuesOfSingleTraceOperators}

We discuss how [[Lie algebra weight systems]] on round [[chord diagrams]] arise in [[quantum field theory]] and [[statistical mechanics]] as [[expectation values]] of suitable [[single trace observables]] subject to [[Wick's theorem]].

So consider

* $\mathfrak{g}$ be a [[metric Lie algebra]], with metric denoted $k$, 

* $(\mathfrak{g}\otimes C \overset{\rho}{\to} C) \in \mathfrak{g}Mod$ be a [[finite-dimensional vector space|finite-dimensional]] [[Lie algebra representation]] of $\mathfrag{g}$.

For comparison with traditional literature, choose 

1. a [[linear basis]] $\{v^a\}$ of $C$

1. a [[linear basis]] $\{t^i\}$ of $\mathfrak{g}$

In terms of these linear bases, the representation is given by a sequence $\rho^i$ of [[square matrices]] $\big((\rho^i)^a{}_b\big)$ such that 

$$
  (\rho^i)^a{}_b v^b
  \;\coloneqq\;
  \rho(t^i, v^a) 
$$

with the [[Einstein summation convention]] understood here and in the following.

We write $k = (k_{i j})$ for the components of the Lie algebra metric in this basis, and write

$$
  \rho_i \;\coloneqq\; k_{i j} \rho^j
$$


With all this understood, a [[field (physics)|field]]/[[random variable]] with values in $\mathfrak{g}$ is

$$
  Z \;=\; Z_i \cdot \rho^i \;\;
$$

for [[scalar field]] components $Z_i$.


Now assume that the $Z_i$ are [[free fields]]/[[random variables]] with [[Gaussian distribution]], hence such that

$$
  \langle Z_i \rangle \;=\; 0
$$

$$
  \langle Z_i Z_j \rangle \;=\; k_{i k}
$$

and such that [[Wick's theorem]] applies to higher [[moments]]:

$$
  \langle Z_{i_1} Z_{i_2} Z_{i_3} Z_{i_4} \rangle 
  \;=\; 
  k_{i_1 i_2} k_{i_3 i_4}
  +
  k_{i_1 i_3} k_{i_2 i_4}
  +
  k_{i_1 i_4} k_{i_2 i_3}
$$

etc.

Consider the [[expectation values]] of [[single trace observables]]:

$$
  \Big\langle 
    tr
    \big(
      \underset{
        \mathclap{
          n\, factors
        }
      }{
      \underbrace{
        Z Z \cdots Z
      }
      }
    \big)
  \Big\rangle
  \;\coloneqq\;
  \big\langle
    Z_{i_1}
    Z_{i_2}
    \cdots
    Z_{i_n}
  \big\rangle
  \cdot
  tr
  \big(
    \rho^{i_1} 
    \cdot
    \rho^{i_2} 
    \cdots
    \rho^{i_n} 
  \big)
$$

Using [[Wick's theorem]], they are given by

$$
  \begin{aligned}
    \Big\langle 
      tr
      \big(
        Z Z Z Z
      \big)
    \Big\rangle
    & 
    =
  \big\langle
    Z_{i_1}
    Z_{i_2}
    Z_{i_3}
    Z_{i_4}
  \big\rangle
  \cdot
  tr
  \big(
    \rho^{i_1} 
    \cdot
    \rho^{i_2} 
    \cdot
    \rho^{i_3} 
    \cdot
    \rho^{i_4} 
  \big)
  \\
  & =
  \phantom{+\;}
  k_{i_1 i_2} \, k_{i_3 i_4}
  \cdot
  tr
  \big(
    \rho^{i_1} 
    \cdot
    \rho^{i_2} 
    \cdot
    \rho^{i_3} 
    \cdot
    \rho^{i_4} 
  \big)
  \\
  & 
  \phantom{=\;}
  + 
  k_{i_1 i_3} \, k_{i_2 i_4}
  \cdot
  tr
  \big(
    \rho^{i_1} 
    \cdot
    \rho^{i_2} 
    \cdot
    \rho^{i_3} 
    \cdot
    \rho^{i_4} 
  \big)  
  \\
  & 
  \phantom{=\;}
  + 
  k_{i_1 i_4} \, k_{i_2 i_3}
  \cdot
  tr
  \big(
    \rho^{i_1} 
    \cdot
    \rho^{i_2} 
    \cdot
    \rho^{i_3} 
    \cdot
    \rho^{i_4} 
  \big)  
  \\
  & =
  2
  \cdot
  tr
  \big(
    \rho_i 
    \cdot
    \rho^i 
    \cdot
    \rho_j
    \cdot
    \rho^j
  \big)
  \\
  &
  \phantom{=\;}
  +
  tr
  \big(
    \rho_{i} 
    \cdot
    \rho_j
    \cdot
    \rho^i 
    \cdot
    \rho^j
  \big)
  \end{aligned}
$$

etc.  

{#TracedWickTheorem} Here [[Wick's theorem]] in the first lines is given by a sum over [[linear chord diagrams]], and the [[trace]] then serves to close these to [[round chord diagrams]]:

<center>
<img src="https://ncatlab.org/nlab/files/SingleTraceOprtrAsWeightSystemOnChordDiagram.jpg" width="830">
</center>

> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


The values of the traces in the last line are
the values of the [[Lie algebra weight system]] $w_C$ on the [[chord diagram]] which reflects the Wick-contractions modulo cyclic permutation.

Essentially this observation (specifically for [[SYK-model]]-like systems and without mentioning of [[weight systems]]) appears in [GGJJV 18, Section 2.2](#GGJJV18), [Jia-Verbaarschot 18, Section 4](#JiaVerbaarschot18), [BNS 18, Section 2.1](#BNS18), [BINT 18, Section 2](#BINT18), [Narovlansky 19, Slides 5-21](#Narovlansky19).


[[!include chord diagrams as multi-trace observables in BMN matrix model -- example]]


## Related concepts

* [[metric Lie algebra]]

* [['t Hooft double line notation]]

[[!include chord diagrams and weight systems -- table]]



## References

### General

Lie algebra weight systems motivated from [[Yang-Mills theory]] [[Feynman amplitudes]]:

* [[Predrag Cvitanović]], _Group theory for Feynman diagrams in non-Abelian gauge theories_, Phys. Rev. D14 (1976) 1536-1553 ([doi:10.1103/PhysRevD.14.1536](https://doi.org/10.1103/PhysRevD.14.1536), [spire:108133](http://inspirehep.net/record/108133), [[CvitanovicWeights76.pdf:file]])

The concept of round Lie algebra weight systems for [[Chern-Simons theory]] with [[Wilson lines]] originates around

* {#Kontsevich94} [[Maxim Kontsevich]], _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

* {#BarNatan95} [[Dror Bar-Natan]], Section 2.4 of: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

and for [[horizontal weight systems]] in

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

reviewed in 

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, Section 2.2 of: _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))

Discussion of [[fundamental representation|fundamental]] $\mathfrak{gl}(n)$-weight systems in terms of [[Cayley distance kernels]] on the [[symmetric group]]:

* {#CSS21} *[[schreiber:Weight systems that are quantum states]]*

### Via string diagrams

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

* Alexander Schrijver, _On Lie algebra weight systems for 3-graphs_ ([arXiv:1412.6923](https://arxiv.org/abs/1412.6923))


### For $\mathfrak{sl}(2)$

For the [[special linear Lie algebra]] $\mathfrak{sl}(2)$

* [[Sergei Chmutov]], [[Alexander Varchenko]], _Remarks on the Vassiliev knot invariants coming from $\mathfrak{sl}(2)$_, Topology 36 (1), 153-178, 1997

* E. Kulakova, S. Lando, T. Mukhutdinova, G. Rybnikov, _On a weight system conjecturally related to $\mathfrak{sl}_2$_, European Journal of Combinatorics Volume 41, October 2014, Pages 266-277 ([arXiv:1307.4933](https://arxiv.org/abs/1307.4933))


### For $\mathfrak{gl}(1\vert1)$

For the [[super Lie algebra]] $\mathfrak{gl}(1\vert1)$:

* {#FFKV97} [[José Figueroa-O’Farrill]], [[Takashi Kimura]], [[Arkady Vaintrob]], _The universal Vassiliev invariant for the Lie superalgebra $\mathfrak{gl}(1\vert1)$_, Commun. Math. Phys. 185 (1997) 93-127 ([arXiv:q-alg/9602014](https://arxiv.org/abs/q-alg/9602014))


### Further discussion

Relation of the [[colored Jones polynomial]] to [[Lie algebra weight systems]] on [[chord diagrams]]:

* [[Dror Bar-Natan]], [[Stavros Garoufalidis]], _On the Melvin–Morton–Rozansky conjecture_, Invent math (1996) 125: 103 ([doi:10.1007/s002220050070](https://doi.org/10.1007/s002220050070), [[BarNatanGaroufaldis96.pdf:file]])

On the [[logical equivalence]] between the [[four-colour theorem]] and a statement about transition from the [[small N limit]] to the [[large N limit]] for [[Lie algebra weight systems]] on [[Jacobi diagrams]] via the [['t Hooft double line construction]]:

* [[Dror Bar-Natan]], _Lie Algebras and the Four Color Theorem_, Combinatorica 17-1(1997) 43–52  ([arXiv:q-alg/9606016](https://arxiv.org/abs/q-alg/9606016), [doi:10.1007/BF01196130](https://doi.org/10.1007/BF01196130))


[[!include weight systems on chord diagrams in physics]]



[[!redirects Lie algebra weight systems]]

