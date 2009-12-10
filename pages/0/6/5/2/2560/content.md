
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

### In simplicial sets

Let $S : \Delta^{op} \to Set$ be a [[simplicial set]].

The **spine** of an $n$-[[simplex]] $\sigma \in S_n$, also called its **backbone**, consists of the edges $0 \to 1$, $1 \to 2$, $\cdots$ , $(n-1) \to n$ between the successive vertices of $\sigma$. 

When $n \gt 2$, an $(n,i)$-[[horn]] in $S$ has the same edges as any of its fillers, so we may speak of the spine of a $horn$ as well. 

### In dendroidal sets

The above notion generalizes to [[dendroidal set]]s: the spine of a [[tree]] $T$ is the union over its corollas

$$
  Sp(T) = \cup_{C_{k} \to T} C_k
  \,.
$$

For a linear tree this reproduces the above definition.


## Interpretation in terms of higher categories

If $S$ is a [[Kan complex]] or [[quasi-category]], then 
the spine of $\sigma$ is the maximal list of _composable_ edges ([[k-morphism|1-morphism]]s) of $\sigma$. 

Similarly, if $S$ is a fibrant [[dendroidal set]] or [[(∞,1)-operad]], the spine $Sp(T) \hookrightarrow T \to S$ of a tree $T$ in $S$ is a collection of composable operations in  the $(\infty,1)$-operad.

[[!redirects backbone]]