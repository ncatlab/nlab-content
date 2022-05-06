
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

A _linear chord diagram_ or _arc diagram_ or _rooted chord diagram_  is a trivalent finite [[undirected graph]] with an embedded oriented [[line]] and all [[vertices]] on that line.

Equivalemtly this is just an [[n-tuple]] equipped with a [[partition]] into [[pairs]].

The following shows a generic example of a linear chord diagram:

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/LinearChordDiagramsWithFourVertices.jpg" width="250">
</div>


<center>
<img src="https://ncatlab.org/nlab/files/ALinearChordDiagram.jpg" width="400">
</center>

The graphics on the right shows all linear chord diagrams with precisely four [[vertices]].


Closing up the line of a linear chord diagram to a [[circle]] and remembering the [[ordering]] of vertices only op to [[cyclic permutation]], it becomes a _[[round chord diagram]]_, usually just called a [[chord diagram]]. Conversely, a linear chord diagram is equivalently a round chord diagram with one of its [[vertices]] singled out.

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Applications

### Wick's theorem

The [[combinatorics]] of contractions in [[Wick's theorem]] is governed by linear chord diagrams:

Let $\{Z_i\}$ be a set of [[quantum fields]]/[[random variables]] which are [[free fields]]/[[multivariate normal distribution|multivariate normally distributed]] with 

$$
  \big\langle Z_i Z_j \big\rangle = k_{i j}
  \,.
$$

Then [[Wick's theorem]] says that the [[expectation value]] of the product of $n \in \mathbb{N}$ of these fields/random variables is the [[sum]] over linear chord diagrams with $n$ vertices of the product over the edges $e_i \to e_j$ of the given chord diagram of the factors $k_{i j}$.

For example, for $n = 4$, [[Wick's theorem]] says this:

<center>
<img src="https://ncatlab.org/nlab/files/WickTheoremViaLiearChordDiagrams.jpg" width="600">
</center>



## Related concepts

[[!include chord diagrams and weight systems -- table]]

## References

* Everett Sullivan, _Linear chord diagrams with long chords_ ([arXiv:1611.02771](https://arxiv.org/abs/1611.02771))

[[!redirects linear chord diagrams]]

[[!redirects arc diagram]]
[[!redirects arc diagrams]]

[[!redirects rooted chord diagram]]
[[!redirects rooted chord diagrams]]

[[!redirects rooted chord diagram]]
[[!redirects rooted chord diagrams]]
[[!redirects arc diagram]]
[[!redirects arc diagrams]]


