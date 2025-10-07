
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

If $S$ is an [[(∞,n)-category]] (including the case of [[∞-groupoids]], [[(∞,1)-categories]], ...) or a model thereof (including [[Kan complexes]] or [[quasi-categories]], ...) then 
the _spine_ of $S$ is the maximal list of _composable_ edges ([[morphisms]]) of $S$. 

Similarly, if $S$ is an [[(∞,1)-operad]] or a model thereof (given by a [[dendroidal set]] or [[Segal operad]], etc. ), the spine $Sp(T) \hookrightarrow T \to S$ of a [[tree]] $T$ in $S$ is a collection of composable operations in  the $(\infty,1)$-operad.


## Definition

### In simplicial sets

Let $S : \Delta^{op} \to Set$ be a [[simplicial set]].

+-- {: .num_defn}
###### Definition

The **spine** of an $n$-[[simplex]] $\sigma \in S_n$, also called its **backbone**, is the [[union]] of the edges (1-cells) $0 \to 1$, $1 \to 2$, $\cdots$ , $(n-1) \to n$ between the successive vertices of $\sigma$. 

=--

When $n \gt 2$, an $(n,i)$-[[horn]] in $S$ has the same edges as any of its fillers, so we may speak of the spine of a horn as well. 

### In dendroidal sets

The above notion generalizes to [[dendroidal set]]s

+-- {: .num_defn}
###### Definition


The **spine** of a [[tree]] $T$ is the [[union]] over its [corollas](dendroidal+set#Corolla)

$$
  Sp(T) = \bigcup_{C_{k} \to T} C_k
  \,.
$$

=--

In [Cisinski & Moerdijk 2013](#CisinskiMoerdijk13) this is called the _Segal core_ of $T$.

+-- {: .num_remark}
###### Remark

For a linear tree this reproduces the above definition of spines of simplices.

=--

## Properties

### Characterizations of compositions

+-- {: .num_prop}
###### Proposition

A [[simplicial set]] $X$ is the [[nerve]] of a [[category]] precisely if for all $n \in \mathbb{N}$ all the morphisms induced from the spine inclusion

$$
  X^{Sp[n] \hookrightarrow \Delta[n]} : X_n \to X_1 \times_{X_0} \cdots \times_{X_0} X_1
$$

are [[bijections]]. 

More generally, a [[dendroidal set]] $X$ is the [[dendroidal nerve]] of a [[symmetric operad]] over [[Set]] (a [[symmetric multicategory]]), precisely if for all [[trees]] $T$ the morphisms induced from the spine inclusion
$X^{Sp[T] \hookrightarrow \Delta[n]}$ are bijections.

=--

For simplicial sets, this is a classical statement (Grothendieck / Segal). Its homotopical weakening leads to the notion of [[Segal category]] and [[complete Segal space]]. For dendroidal sets this is [Cisinski & Moerdijk 2013, cor. 2.7](#CisinskiMoerdijk13).

### Closure and lifting properties

In the following, _[[tree]]_ means "finite non-planar rooted tree" as used in the definition of _[[dendroidal set]]_ .

+-- {: .num_prop}
###### Proposition

For any [[tree]] $T$, the spine inclusion $Sp[T] \hookrightarrow \Omega[T]$ is an [[inner anodyne morphism]].
 
=--

This is [Cisinski & Moerdijk 2013, prop. 2.4](#CisinskiMoerdijk13). 

## Related concepts

* [[horn]], [[boundary of a simplex]]

* [[composer]]

## References

On spines of [[n-simplices]]:

* {#Land21} [[Markus Land]], Def. 1.1.37(3) in: *Introduction to Infinity-Categories*, Birkhäuser (2021) &lbrack;[doi:10.1007/978-3-030-61524-6](https://link.springer.com/book/10.1007/978-3-030-61524-6)&rbrack;


On spines in the generality of [[dendroidal sets]]:

* {#CisinskiMoerdijk13} [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], section 1 of: _Dendroidal Segal spaces and infinity-operads_, Journal of Topology **6** 3 (2013) 675-794 &lbrack;[arXiv:1010.4956](http://arxiv.org/abs/1010.4956), [doi:10.1112/jtopol/jtt004](https://doi.org/10.1112/jtopol/jtt004)&rbrack;
 


[[!redirects spines]]

[[!redirects backbone]]
[[!redirects backbones]]

[[!redirects dendroidal spine]]
[[!redirects dendroidal spines]]
