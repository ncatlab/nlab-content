
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

For $n \in \mathbb{N}$ a [[natural number]], let $F(\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}})$ be the [[free Lie algebra]] on [[generators and relations|generators]] $t_{i j}$ with two indices ranging from 1 to $n$ and distinct.

The _infinitesimal braid relations_ are the following [[generators and relations|relations]] on the underlying [[vector space]] of the [[free construction|free]] [[Lie algebra]] on [[generators and relations|generators]] $\{t_{i j}\}_{i\neq j \in \{1,\cdots, n\}}$ 

\[
  \label{InfinitesimalBriadRelations}
  \left.
 \array{
    R0: \;\; & t_{i j} - t_{j i} & = 0 
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

## Related concepts

* [[braid group]]

* [[Yang-Baxter equation]]

[[!include chord diagrams and weight systems -- table]]


[[!redirects infinitesimal braid relations]]
