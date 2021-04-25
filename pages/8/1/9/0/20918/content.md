
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

Given any [[ground field]] $\mathbb{F}$ (or in fact just any [[commutative ring|commutative]] [[ground ring]])

1) write $\mathcal{A}^{pb}$ for  the [[linear span]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] the [[2T relations]] and the [[4T relations]] 

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramsModulo2TAnd4T.jpg" width="900">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

regarded as a [[graded vector space]], graded by the number of chords,

and write

\[
  \label{SpaceOfHorizontalWeightSystems}
  \mathcal{W}_{pb} 
    \coloneqq 
  (\mathcal{A}^{pb})^\ast
\]

for its degreewise [[dual vector space]]: the space of _[[horizontal weight systems]]_;


2) write

$$
  \mathcal{A}^{pb} 
    \overset{ 
      \;\;\; p_n \;\;\; 
    }{\longrightarrow}  
  \mathcal{A}^{pb}_n 
    \overset{ 
      \;\;\; i_n \;\;\; 
    }{\hookrightarrow} 
  \mathcal{A}^{pb} 
$$ 

for projection onto and inclusion of the linear subspace spanned by [[horizontal chord diagrams]] with $n$ strands;

3) write

$$
  \underset{\mathbb{N}}{\oplus} \mathbb{N}
  \overset{
    \;\;\;
      \Delta^{(-)}
    \;\;\;
  }{\longrightarrow}
  End( \mathcal{A}^{pb} \big)
$$

for the operation that reads in a [[finite number|finite]] [[tuple]] $k \coloneqq (k_1, \cdots, k_n)$ of [[natural numbers]], with [[sum]] $\left\vert k\right\vert \coloneqq \underset{i}{sum} k_i$, and produces the [[linear map]]

\[
  \label{Delta}
  \mathcal{A}^{pb}
  \overset{
    \; 
    p_n 
    \;
  }{\to}
  \mathcal{A}^{pb}_{n} 
    \overset{
      \;\;\;
      \Delta^k
      \;\;\;
     }{\longrightarrow}
  \mathcal{A}^{pb}_{\left\vert k \right \vert}   
  \overset{ 
    \;
    i_{\left\vert k \right\vert} 
    \;
  }{\hookrightarrow}
  \mathcal{A}^{pb}
\]

which takes a [[horizontal chord diagram]] with $n$ strands to the [[linear combination]] of chord diagrams obtained by replacing its $i$-th strand by $k_i$ strands for all $i$ and then summing over all ways of re-attaching chords, with any vertex previously on some strand $i$ now to be put on one of the $k_i$ strands ([Bar-Natan 96, Def. 2.2](#BarNatan96)).

For example:

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramPartitioning.jpg" width="600">
</center>

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordDiagramPartitioningGenericII.jpg" width="700">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak

Moreover, for $\mathfrak{g}$ a [[metric Lie algebra]]

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
  \underset{n \in \mathbb{N}}{\oplus}
  Hom_{\mathbb{F}}
  \big(
    \mathcal{A}^{pb}_n
    ,
    End(C^{\otimes n})
  \big)
\]

for the [[function]] that sends a [[Lie module]] $C$ over $\mathfrak{g}$ to the corresponding [[endomorphism ring]]-valued [[Lie algebra weight system]] $w_C$ on [[horizontal chord diagrams]].

Finally, for 

1. $C \in \mathfrak{g} Mod$ a [[Lie algebra representation]] of $\mathfrak{g}$, 

1. $n \in \mathbb{N}$ a [[natural number]],

1. $\sigma \in Sym(n)$ a [[permutation]] of $n$ elements

write

\[
  \label{PermutationTraceOperation}
  tr_\sigma 
    \;\colon\;
  End
  \big( 
    C^{\otimes n}
  \big)
  \longrightarrow 
  \mathbb{F}
\]


for the [[composition|composite]] operation of 

1. [[composition|composing]] an [[endomorphism]] on the $n$-fold [[tensor product of vector spaces|tensor power]] of $C$ by the [[braiding]] according to the [[permutation]] $\sigma$;

1. forming the [[trace]] of the resulting endomorphism of $C^{\otimes n}$.

Then the  [[composition]] of 

1. the partitioning function (eq:Delta);

1. the assignment (eq:AssignLieAlgebraWeightSystem) of [[Lie algebra weight systems]];

1. the permuted [[trace]] operation (eq:PermutationTraceOperation)

yields a [[function]] from [[triples]] consisting of a [[Lie module]], a [[tuple]] of [[natural numbers]] and a [[permutation]] to [[horizontal weight systems]]:

\[
  \label{MapAssigningPartitionedLieWeightSystemsToModules}
  \array{
    \big(
      \mathfrak{g}Mod_{/\sim} 
    \big)
      \;\times\; 
    \big(
      \underset{\mathbb{N}}{\oplus} \mathbb{N}
    \big)
      \;
      \underset{
        \mathbb{N}
      }{\times}
      \;
    \big(
      \underset{n \in \mathbb{N}}{\sqcup} Sym(n)
    \big)
    &
      \overset{ 
        \;\;
        tr_{(-)} \circ w_{(-)} \circ \Delta 
        \;\;
      }{
        \longrightarrow
      } 
    &
    \mathcal{W}_{pb}
    \\
    (C, \; k = (k_1, \cdots, k_n), \; \sigma)
    &\mapsto&
    \left(
      D 
        \;\mapsto\;
      tr_\sigma 
        \circ 
      w_C
        \circ 
      \Delta^k (D)
    \right)
  }
\] 

Finally, write also

\[
  \label{LinearExtensionOfMapAssigningPartitionedLieWeightSystemsToModules}
    Span
    \big(
      \mathfrak{g}Mod_{/\sim} 
        \;\times\; 
      \underset{\mathbb{N}}{\oplus} \mathbb{N} 
        \;\underset{\mathbb{N}}{\times}\;
      \underset{n \in \mathbb{N}}{\mathbb{N}} Sym(n)
   \big)
      \overset{ 
        tr_{(-)} \circ w_{(-)} \circ \Delta^{(-)} (-)
      }{
        \longrightarrow
      } 
  \mathcal{W}_{pb}
\] 

for the linear extension of this function (eq:MapAssigningPartitionedLieWeightSystemsToModules) to the [[linear span]] of its [[domain]] [[set]].

\linebreak

## Statement

+-- {: .num_prop #AllHorizontalWeightSystemsAreslNWeightSystems}
###### Proposition
([[all horizontal weight systems are partitioned Lie algebra weight systems]])

For $N \geq 2$ consider the [[special linear Lie algebra]] $\mathfrak{sl}(N)$, canonically regarded as a [[metric Lie algebra]] via its  [[Killing form]]. 

Then the space $\mathcal{W}_{pb} \coloneqq (\mathcal{A}^{pb})^\ast$ (eq:SpaceOfHorizontalWeightSystems) of [[weight systems]] on [[horizontal chord diagrams]] is [[linear span|spanned]] by partitioned $\mathfrak{sl}(N)$-[[Lie algebra weight systems]], 
in that the linear extension (eq:LinearExtensionOfMapAssigningPartitionedLieWeightSystemsToModules) of the function (eq:MapAssigningPartitionedLieWeightSystemsToModules) assigning $\mathfrak{sl}(N)$-[[Lie algebra weight systems]] composed with partitioning (eq:Delta) is an [[epimorphism]]:

$$
  \array{
  Span
  \Big(
    \big(
    \underset{
      \mathclap{
      \color{blue}
      {Lie\;modules}
      }
    }{
      \underbrace{
        \mathclap{\phantom{\vert \atop \vert}}
        \mathfrak{sl}(N) \, Mod_{/\sim}
      }
    }
    \big)
    \;
      \times
    \;
    \big(
    \underset{
      \mathclap{
      \color{blue}
      tuples\;of\;numbers
      }
    }{
      \underbrace{
        \mathclap{ \phantom{\vert \atop \vert }  }
        \underset{\mathbb{N}}{\oplus} \mathbb{N}
      }
    }
    \big)
    \;
    \underset{\mathbb{N}}{\times}
    \;
    \big(
      \underset{
        \color{blue}
        permutations
      }{
        \underbrace{
          \underset{n \in \mathbb{N}}{\sqcup}
          Sym(n)
        }
      }
    \big)
  \Big) 
  &
  \underoverset{\color{blue}epimorphism}{ 
     \;\;\; 
     tr_{(-)}
      \circ
     w_{(-)} 
      \circ 
     \Delta^{(-)}
     (-)
     \;\;\; 
  }{\longrightarrow}
  &
  \overset{
    \mathclap{
      {\color{blue} horizontal\;weight\;systems}
      \atop
      {\phantom{a}}
    }
  }{
    \mathcal{W}_{pb}
  }
  \\
    (
      C, \;\; k = (k_1, \cdots, k_n), \;\; \sigma
    )
    &\mapsto&
    \left(
      \;\;\;\;\;\;
      \array{
        \overset{
          \mathclap{
            \color{blue}
            {
              {horizontal}
                \atop
              {
                {chord}
                \atop
                {diagram}
              }
            }
            \atop
            {\phantom{a}}
          }
        }{
          D
        } 
          \mapsto
        & 
        \phantom{=\;} 
        \overset{
          \mathclap{
            \color{blue} \sigma\text{-}trace
          }
        }{
          \overbrace{
            tr_\sigma 
          }
        }
          \circ 
        \underset{
          \mathclap{
            {\color{blue}RT\;invariant}
          }
        }{
          \underbrace{
            W_{{}_{C^{\otimes k_1}, \cdots , C^{\otimes k_n} }}(D)
          }
        }
        \;\;\;\;\;\;\;\;\;
        \\
        & 
        = 
        tr_\sigma 
          \circ 
        \underset{
           \mathclap{
             {\color{blue} End\text{-}valued\;Lie\;algebra\;weight\;system}
           }
        }{
          \underbrace{
            w_C
          }
       }
          \circ
        \overset{
          \mathclap{
            {\color{blue} partitioning}
          }
        }{ 
          \overbrace{
            \Delta^k 
          }
        }
        (D)
      }
    \right)
  }
  \,.
$$

=--

This is the statement of [Bar-Natan 96, Corollary 2.6](#BarNatan96).

{#Example} For example:

<center>
<img src="https://ncatlab.org/nlab/files/PartitionedLieAlgebraWeightSystem.jpg" width="840">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak

## Applications

[[!include chord diagrams as multi-trace observables in BMN matrix model -- example]]


## Related theorems

[[!include facts about chord diagrams and weight systems -- contents]]


## References

The theorem and its proof is due to:

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))


[[!redirects all horizontal weight systems are Lie algebra weight systems]]



