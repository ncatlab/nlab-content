
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

## Ingredients

Given any [[ground field]] (or in fact just any [[commutative ring|commutative]] [[ground ring]]) we write:

1) $\mathcal{A}^{pb}$ for  the [[linear span]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] the [[2T relations]] and the [[4T relations]] 

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramsModulo2TAnd4T.jpg" width="900">
</center>

regarded as a [[graded vector space]], graded by the number of chords;

2) $\mathcal{W}_{pb} \coloneqq (\mathcal{A}^{pb})^\ast$ for the degreewise [[dual vector space]] of _[[horizontal weight systems]]_.

Moreover, for $\mathfrak{g}$ a [[metric Lie algebra]], write  

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

## Statement

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


+-- {: .num_remark}
###### Remark

For [[weight systems]] on _[[round chord diagrams]]_ the analogous statement is _not true_: There are round weight systems that do not even arise from any (finite-dimensional) metric [[super Lie algebra]] ([Vogel 11](#Vogel11))

=--


## References

The theorem for horizontal weight systems is due to

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

The counter-example for round weight systems is due to 

* {#Vogel11} [[Pierre Vogel]], _Algebraic structures on modules of diagrams_, Journal of Pure and Applied Algebra, Volume 215, Issue 6, June 2011, Pages 1292-1339 ([doi:10.1016/j.jpaa.2010.08.013](https://doi.org/10.1016/j.jpaa.2010.08.013), [pdf](https://webusers.imj-prg.fr/~pierre.vogel/diagrams.pdf))





