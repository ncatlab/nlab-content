
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

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

* An [[object]] is given by a triple of data $t \coloneqq (n,t_+,t_-)$, which is a [[partition]] of the [[poset]] $\{i \;|\; 1\leq i\leq n\}$ for some [[natural number]] $n \geq 0$ into two [[subset]] parts $t_+$ and $t_-$. (The corresponding diagram as above has nodes $t_0, \ldots, t_n$, and the arrow between $t_{i-1}$ and $t_i$ points forward to $t_i$ if $i \in t_+$, and backward if $i \in t_-$.) 

* A [[morphism]] is a [[monotone map]] preserving the partitions.

We will call $\mathbf{T}$ the __zigzag category__, or the __category of zigzag types__.

Also, notice that we have cleverly hidden the [[empty set]] among the objects.  We pat ourselves on the backs for doing this. (Here the zigzag type consists of a single node.) 


## Applications

Such zig-zag [[diagram]]s serve to model morphisms in an [[(∞,1)-category]] in terms of a presentation by a [[category with weak equivalences]]. See [[simplicial localization of a homotopical category]].


[[!redirects zigzag category]]
[[!redirects zigzag categories]]
[[!redirects zig-zag category]]
[[!redirects zig-zag categories]]
[[!redirects category of zigzag types]]
[[!redirects categories of zigzag types]]
[[!redirects category of zig-zag types]]
[[!redirects categories of zig-zag types]]
[[!redirects zigzag type]]
[[!redirects zigzag types]]
