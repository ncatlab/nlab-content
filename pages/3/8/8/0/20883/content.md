
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

In [[knot theory]], a large class of [[weight systems]] arises from reading a ([[horizontal chord diagram|horizontal]]) [[chord diagram]] as a [[string diagram]] in the evident way, and then labelling it by the structure morphisms of a [[metric Lie algebra|metric]] [[Lie algebra object]] equipped with a [[Lie algebra representation]] [[internalization|internal to]] a suitable [[tensor category]]. 

<center>
<img src="https://ncatlab.org/nlab/files/LieAlgebraWeightSystemAssignment.jpg" width="600">
</center>

This does yield weight systems, because, using that [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]], the required [[STU-relations]] translate into the structural equations satisfied by [[Lie modules]] ([[Jacobi identity]] and Lie action property); see [Roberts & Willerton 06, Theorem 3.1](#RobertsWillerton06), following [Vaintrob 94](#Vaintrob94), [Vogel 11](#Vogel11) following [Bar-Natan 95, 2.4](#BarNatan95), [Bar-Natan 96](#BarNatan96) following [Kontsevich 94](#Kontsevich94).

The [[weight systems]] arising this way are called _Lie algebra weight systems_.

## Properties

### Ubiquity

#### On round chord diagrams

Examples of [[weight systems]] on (ordinary, round) [[chord diagrams]] which are _not_ Lie algebra weight systems are rare. Originally it was conjectured that none exist ([Bar-Natan 95, Conjecture 1](#BarNatan95), [Bar-Natan & Stoimenow 97, Conjecture 2.4](#BarNatanStoimenow97)).  

Eventually, a (counter-)example of a weight system which at least does not arise from any [[finite dimensional vector space|finite-dimensional]] [[super Lie algebra]] was given in [Vogel 11](#Vogel11).

#### On horizontal chord diagrams

However, for [[horizontal chord diagrams]] the situation is clear-cut: [[all horizontal weight systems are Lie algebra weight systems]]. We state this as Prop. \ref{AllHorizontalWeightSystemsAreslNWeightSystems} below, but first to recall the ingredients:

For $\mathfrak{g}$ a [[metric Lie algebra]], write  

1)  $\mathfrak{g}Mod_{/\sim}$ for its [[set]] of [[isomorphism classes]] of [[finite dimensional vector space|finite dimensional]] [[Lie algebra representations]] ([[Lie modules]])

2) $\mathfrak{g}Mod_{/\sim} \overset{ w_{(-)} }{\longrightarrow} \mathcal{W}_{pb}$ for the [[function]] that sends a Lie module $C$ to the corresponding [[Lie algebra weight system]] $w_C$ on [[horizontal chord diagrams]];

3)

\[
  \label{LinearExtensionOfMapAssigningLieWeightSystemsToModules}
   Span\big(\mathfrak{g}Mod_{/\sim}\big) 
     \overset{ w_{(-)} }{\longrightarrow} 
  \mathcal{W}_{pb}
\] 

for the linear extension of this function to the [[linear span]] of [[isomorphism classes]] of [[Lie modules]].


+-- {: .num_prop #AllHorizontalWeightSystemsAreslNWeightSystems}
###### Proposition
([[all horizontal weight systems are Lie algebra weight systems]])

For $N \geq 2$ consider the [[special linear Lie algebra]] $\mathfrak{sl}(N)$, canonically regarded as a [[metric Lie algebra]] via its  [[Killing form]]. 

Then the space $\mathcal{W}_{pb} \coloneqq (\mathcal{A}^{pb})^\ast$ of [[weight systems]] on [[horizontal chord diagrams]] is [[linear span|spanned]] by $\mathfrak{sl}(N)$-[[Lie algebra weight systems]], in that the linear extension (eq:LinearExtensionOfMapAssigningLieWeightSystemsToModules) of the function assigning $\mathfrak{sl}(N)$-[[Lie algebra weight systems]] is an [[epimorphism]]:

$$
  Span
  \big(
    \mathfrak{sl}(N) Mod_{/\sim}
  \big)
  \underoverset{\color{blue}epi}{ \;\;\; w_{(-) \;\;\;} }{\longrightarrow}
  \mathcal{W}_{pb}
  \,.
$$

=--

This is due to [Bar-Natan 96, Corollary 2.6](#BarNatan96).

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
    Z^{i_1} 
    \cdot
    Z^{i_2} 
    \cdots
    Z^{i_n} 
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
    Z^{i_1} 
    \cdot
    Z^{i_2} 
    \cdot
    Z^{i_3} 
    \cdot
    Z^{i_4} 
  \big)
  \\
  & =
  2
  \cdot
  tr
  \big(
    Z_i 
    \cdot
    Z^i 
    \cdot
    Z_j
    \cdot
    Z^j
  \big)
  +
  tr
  \big(
    Z_{i} 
    \cdot
    Z_j
    \cdot
    Z^i 
    \cdot
    Z^j
  \big)
  \end{aligned}
$$

etc.  The values of the traces in the last line are
the values of the [[Lie algebra weight system]] $w_C$ on the [[chord diagram]] which reflects the Wick-contractions modulo cyclic permutation.

## Related concepts

* [[metric Lie algebra]]

## References

### General

The concept for ordinary [[weight systems]] originates around

* {#Kontsevich94} [[Maxim Kontsevich]], _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

* {#BarNatan95} [[Dror Bar-Natan]], Section 2.4 of: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

and for [[horizontal weight systems]] in

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

reviewed in 

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, Section 2.2 of: _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))


From the construction given in [Bar-Natan 95, Section 2.4](#BarNatan95) the interpretation in terms of [[string diagrams]] for [[Lie algebra objects]] in [[tensor categories]] is evident, but standard textbooks in [[knot theory]]/[[combinatorics]] do not pick this up:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Chapter 6 of: _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], Section 14 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

The interpretation of Lie algebra weight systems as [[string diagram]]-calculus and generalization to [[Lie algebra objects]] (motivated by generalization at least to [[super Lie algebras]]) is made more explicit in

* {#Vaintrob94} [[Arkady Vaintrob]], _Vassiliev knot invariants and Lie S-algebras_, Mathematical Research Letters1, 579–595 (1994) ([pdf](https://pdfs.semanticscholar.org/bdc3/ac1d8da476245e2408e481a70b115b3e9aab.pdf))

* {#Vogel11} [[Pierre Vogel]], _Algebraic structures on modules of diagrams_, Journal of Pure and Applied Algebra, Volume 215, Issue 6, June 2011, Pages 1292-1339 ([doi:10.1016/j.jpaa.2010.08.013](https://doi.org/10.1016/j.jpaa.2010.08.013), [pdf](https://webusers.imj-prg.fr/~pierre.vogel/diagrams.pdf))


and fully explicit in

* {#RobertsWillerton06} [[Justin Roberts]], [[Simon Willerton]], Section 3 of: _On the Rozansky-Witten weight systems_, Algebr. Geom. Topol. 10 (2010) 1455-1519 ([arXiv:math/0602653](https://arxiv.org/abs/math/0602653))

For complex-valued weight systems see also

* Alexander Schrijver, _On Lie algebra weight systems for 3-graphs_ ([arXiv:1412.6923](https://arxiv.org/abs/1412.6923))


### For $\mathfrak{sl}(2)$

For the [[special linear Lie algebra]] $\mathfrak{sl}(2)$

* [[Sergei Chmutov]], [[Alexander Varchenko]], _Remarks on the Vassiliev knot invariants coming from $\mathfrak{sl}(2)$_, Topology 36 (1), 153-178, 1997

### For $\mathfrak{gl}(1\vert1)$

For the [[super Lie algebra]] $\mathfrak{gl}(1\vert1)$:

* {#FFKV97} [[José Figueroa-O’Farrill]], [[Takashi Kimura]], [[Arkady Vaintrob]], _The universal Vassiliev invariant for the Lie superalgebra $\mathfrak{gl}(1\vert1)$_, Commun. Math. Phys. 185 (1997) 93-127 ([arXiv:q-alg/9602014](https://arxiv.org/abs/q-alg/9602014))

[[!redirects Lie algebra weight systems]]

