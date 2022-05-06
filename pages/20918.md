
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

All [[weight systems]] on [[horizontal chord diagrams]] may be realized as [[linear combinations]] of [[Lie algebra weight systems]] applied not necessarily to the given [[horizontal chord diagram]] itself, but to the result of regarding each of its strands as resolved by some [[finite number]] of strands.

We state this precisely as Prop. \ref{AllHorizontalWeightSystemsAreslNWeightSystems} below (due to [Bar-Natan 96](#BarNatan96)). First we introduce all the definitions that enter the statement:

## Ingredients
 {#Ingredients}

Given any [[ground field]] (or in fact just any [[commutative ring|commutative]] [[ground ring]])

1) write $\mathcal{A}^{pb}$ for  the [[linear span]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] the [[2T relations]] and the [[4T relations]] 

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramsModulo2TAnd4T.jpg" width="900">
</center>

regarded as a [[graded vector space]], graded by the number of chords;

2) $\mathcal{A}^{pb} \overset{ p_n }{\to}  \mathcal{A}^{pb}_n \overset{ i_n }{\hookrightarrow} \mathcal{A}^{pb} $ for projection onto and inclusion of the linear subspace spanned by [[horizontal chord diagrams]] with $n$ strands;

3) write

\[
  \label{SpaceOfHorizontalWeightSystems}
  \mathcal{W}_{pb} 
    \coloneqq 
  (\mathcal{A}^{pb})^\ast
\]

for the degreewise [[dual vector space]], called the space of _[[horizontal weight systems]]_.

\linebreak

Moreover, for $\mathfrak{g}$ a [[metric Lie algebra]]:

1) write 

$$
  \mathfrak{g}Mod_{/\sim}
$$ 

for its [[set]] of [[isomorphism classes]] of [[finite dimensional vector space|finite dimensional]] [[Lie algebra representations]] ([[Lie modules]])

2) write

\[
  \label{AssignLieAlgebraWeightSystem}
  \mathfrak{g}Mod_{/\sim} 
    \overset{ w_{(-)} }{\longrightarrow} 
  \mathcal{W}_{pb}
\]

for the [[function]] that sends a [[Lie module]] $C$ over $\mathfrak{g}$ to the corresponding [[Lie algebra weight system]] $w_C$ on [[horizontal chord diagrams]];

3) write

$$
  \underset{\mathbb{N}}{\sqcup} \mathbb{N}
  \overset{
    \;\;\Delta\;\;
  }{\longrightarrow}
  End( \mathcal{A}^{pb} \big)
$$

for the operation that reads in a [[finite number|finite]] [[tuple]] $k \coloneqq (k_1, \cdots, k_n)$ of [[natural numbers]] and produces the map

\[
  \label{Delta}
  \mathcal{A}^{pb}
  \overset{p_n}{\to}
  \mathcal{A}^{pb}_{n} 
    \overset{
      \;\;\;
      \Delta^k
      \;\;\;
     }{\longrightarrow}
  \mathcal{A}^{pb}_{\left\vert k \right \vert}   
    \overset{ i_n }{\hookrightarrow}
  \mathcal{A}^{pb}
\]

which takes a [[horizontal chord diagram]] with $n$ strands to the [[linear combination]] of chord diagrams obtained by replacing its $i$-th strand by $k_i$ strands for all $i$ and then reconnecting its chords in all possible ways.

([Bar-Natan 96, Def. 2.2](#BarNatan96))


4) The  [[composition]] of the partitioning function (eq:Delta) with the assignment (eq:AssignLieAlgebraWeightSystem) of [[Lie algebra weight systems]] yields a [[function]]

\[
  \label{MapAssigningPartitionedLieWeightSystemsToModules}
  \mathfrak{g}Mod_{/\sim} 
    \times 
  \underset{\mathbb{N}}{\sqcup} \mathbb{N}
    \overset{ 
      \;\;
      w_{(-)} \circ \Delta 
      \;\;
    }{
      \longrightarrow
    } 
  \mathcal{W}_{pb}
\] 

Write also

\[
  \label{LinearExtensionOfMapAssigningPartitionedLieWeightSystemsToModules}
    Span
    \big(
      \mathfrak{g}Mod_{/\sim} 
        \times 
      \underset{\mathbb{N}}{\sqcup} \mathbb{N} \big) 
      \overset{ 
        w_{(-)} \circ \Delta 
      }{
        \longrightarrow
      } 
  \mathcal{W}_{pb}
\] 

for its linear extension to the [[linear span]] of [[pairs]] consisting of an [[isomorphism classes]] of [[Lie modules]] and a [[finite set|finite]] [[tuple]] of [[natural numbers]].


## Statement

+-- {: .num_prop #AllHorizontalWeightSystemsAreslNWeightSystems}
###### Proposition
([[all horizontal weight systems are partitioned Lie algebra weight systems]])

For $N \geq 2$ consider the [[special linear Lie algebra]] $\mathfrak{sl}(N)$, canonically regarded as a [[metric Lie algebra]] via its  [[Killing form]]. 

Then the space $\mathcal{W}_{pb} \coloneqq (\mathcal{A}^{pb})^\ast$ (eq:SpaceOfHorizontalWeightSystems) of [[weight systems]] on [[horizontal chord diagrams]] is [[linear span|spanned]] by partitioned $\mathfrak{sl}(N)$-[[Lie algebra weight systems]], 
in that the linear extension (eq:LinearExtensionOfMapAssigningPartitionedLieWeightSystemsToModules) of the function (eq:MapAssigningPartitionedLieWeightSystemsToModules) assigning $\mathfrak{sl}(N)$-[[Lie algebra weight systems]] composed with partitioning (eq:Delta) is an [[epimorphism]]:

$$
  Span
  \Big(
    \underset{
      \mathclap{
      \color{blue}
      {Lie\,data}
      }
    }{
      \underbrace{
        \mathfrak{sl}(N) Mod_{/\sim}
      }
    }
    \;
      \times
    \;
    \underset{
      \mathclap{
      \color{blue}
      partitioning
      }
    }{
      \underbrace{
        \underset{\mathbb{N}}{\sqcup} \mathbb{N}
      }
    }
  \Big)
  \underoverset{\color{blue}epi}{ 
     \;\;\; w_{(-)} \circ \Delta \;\;\; 
  }{\longrightarrow}
  \mathcal{W}_{pb}
  \,.
$$

=--


## References

The theorem is due to

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))


[[!redirects all horizontal weight systems are Lie algebra weight systems]]



