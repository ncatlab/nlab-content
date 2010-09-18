
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _zigzag category_ is the [[category]] whose objects are [[diagram]]s that look like

$$
  \{
    t_0 \leftarrow t_1 \leftarrow t_2 \rightarrow t_3 \leftarrow t_4 
    \cdots
  \}
  \,.
$$


## Definition

Let $\mathbf{T}$ be the [[category]] defined as follows:

* [[Objects]] are defined by triples of data $t \coloneqq (n,t_+,t_-)$, which are [[partition]]s of the sets $\{i\}_{1\leq i\leq n}$ for $n\geq 0$ into two disjoint subsets $t_+$ and $t_-$.

* [[Morphisms]] are [[monotone maps]] preserving the partitions.  

We will call $\mathbf{T}$ the __zigzag category__, or the __category of zigzag types__.

Also, notice that we have cleverly hidden the [[empty set]] among the objects.  We pat ourselves on the backs for doing this.


## Applications

Such zig-zag [[diagram]]s serve to model morphisms in an [[(∞,1)-category]] in terms of a presentation by a [[category with weak equivalences]]. See [[simplicial localization of a homotopical category]].

[[!redirects zigzag categories]]
[[!redirects zig-zag category]]
[[!redirects zig-zag categories]]