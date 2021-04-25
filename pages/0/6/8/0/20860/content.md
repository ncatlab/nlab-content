
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


## Ingredients

Consider 

1. the [[set]] $\mathcal{D}^c$ of [[chord diagrams]];

1. the [[set]] $\mathcal{D}^t$ of [[Jacobi diagrams]];


Write

\[
  \label{InjectionOfChordDiagramsIntoJacobiDiagrams}
  \mathcal{D}^c 
    \overset{i}{\hookrightarrow} 
  \mathcal{D}^t
\]

for the canonical [[injection]], regarding [[chord diagrams]] as [[Jacobi diagrams]] without internal [[vertices]], hence with all [[vertices]] on the circle.

For $R \in $ [[CRing]] a [[commutative ring]], write

1. $R\langle \mathcal{D}^c \rangle$ for the $R$-[[linear span]] of [[chord diagrams]];

1. $R\langle \mathcal{D}^t \rangle$ for the $R$[[linear span]] of [[Jacobi diagrams]]


and finally

\[
  \label{QuotientSpaces}
  \mathcal{A}^c 
    \;\coloneqq\;
  R\langle \mathcal{D}^c \rangle/4T 
  \,,
  \phantom{AAAA}
  \mathcal{A}^t 
    \;\coloneqq\;
  R\langle \mathcal{D}^t\rangle/STU
\]

for the respective [[quotient spaces]] by the [[4T relations]] 

<center>
<img src="https://ncatlab.org/nlab/files/4TRelationsForRoundChordDiagrams.jpg" width="320">
</center>


and by the [[STU relations]]

<center>
<img src="https://ncatlab.org/nlab/files/STU-relation.jpg" width="500">
</center>

respectively.

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Statement
 {#Statement}

The linear extension of the canonical inclusion $\mathbb{D}^c \overset{i}{\hookrightarrow} \mathbb{D}^t$ (eq:InjectionOfChordDiagramsIntoJacobiDiagrams) descends to the quotients (eq:QuotientSpaces) and yields a [[linear isomorphism]]:

$$
  \mathcal{A}^c
  \underoverset{\simeq}{i}{\longrightarrow}
  \mathcal{A}^t
$$

<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagModulo4TAreJAcobiDiagModuloSTU.jpg" width="840">
</center>

This is due to [Bar-Natan 95, Theorem 6](#BarNatan95). See also [Chmutov-Duzhin-Mostovoy 11, 5.3](#ChmutovDuzhinMostovoy11)

> graphics from [Sati-Schreiber 19]()


The key step of the **proof** is to observe that the [[STU-relations]] imply the [[4T-relations]] as follows:

<center>
<img src="https://ncatlab.org/nlab/files/STURelationImplies4TRelation.jpg" width="350">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Application

### Relation to weight systems

The immediate consequence is that the space of [[framed weight systems]] $\mathcal{W}$, which by definition is the [[dual vector space]] to the [[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] the [[4T-relations]], is equiuvalently also the [[dual vector space]] to the [[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] the [[4T-relations]]:

$$
  \begin{aligned}
    \mathcal{W}
    & \coloneqq
    (\mathcal{A}^c)^\ast
    \\
    & \simeq 
    (\mathcal{A}^t)^\ast
  \end{aligned}
$$


## Related theorems

[[!include facts about chord diagrams and weight systems -- contents]]


## Related concepts

* [[Lie algebra weight system]]

## References

The result is due to 

* {#BarNatan95} [[Dror Bar-Natan]], Theorem 6 in: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Lecture notes

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 5.3 of  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))


[[!redirects chord diagrams modulo 4T are Chern-Simons diagrams modulo STU]]

