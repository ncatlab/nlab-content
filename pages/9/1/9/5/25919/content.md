
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

\tableofcontents

## Definition 

In [[graph theory]], an **adjacency matrix** for a [[finite set|finite]] [[multigraph]] or [[pseudograph]] with $n$ [[vertices]] is an $n$ by $n$ [[matrix]] of [[natural numbers]] which encodes the number of [[edges]] between each vertex: entry $a_{i, j}$ in the matrix is the number of edges between vertex $v_i$ and $v_j$. 

## Properties

Let $G$ be a finite multigraph, and let $A$ be the associated adjacency matrix. Then the matrix power $A^n$ encodes the number of $n$-step [[walks]] between each vertex: entry $b_{i, j}$ in $A^n$ is the number of $n$-step walks between vertex $v_i \in G$ and $v_j \in G$. 

## Related concepts

* [[matrix]]

## References

* Wikipedia, [Adjacency matrix](https://en.wikipedia.org/wiki/Adjacency_matrix)