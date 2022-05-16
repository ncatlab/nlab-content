

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The underlying higher [[quiver]] or higher [[directed pseudograph]] of an [[(n,r)-category|$(n, r)$-category]]. 

## Definition 

For finite $r$, $(n,r)$-quivers are defined inductively as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, an **$(n,0)$-quiver** is an [[∞-groupoid]] that is [[n-truncated]]: an [[n-groupoid]]. 

For $0 \leq r \lt \infty$, an **$(n+1,r+1)$-quiver** is an (n+1)-groupoid $G$ such that for every object $A$ and $B$,  called a **vertex**, in $G$, there is a $(n,r)$-quiver of **edges** $Edge(A, B)$ between $A$ and $B$. 

where $\infty + 1 = \infty$
=--

For the case $r = \infty$, $(n, \infty)$-quivers are [[coinductive definition|defined coinductively]] as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, an **$(n,\infty)$-quiver** is an [[n-groupoid]] $G$ such that for every object $A$ and $B$, called a **vertex**, in $G$, there is a $(n,\infty)$-quiver of **edges** $Edge(A, B)$ between $A$ and $B$. 
=--

## See also 

* [[quiver]]

* [[pseudograph]]

* [[(n,r)-category]]

* [[coinduction]]