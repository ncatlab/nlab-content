+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The **[[topos]] of trees** is the category of [[presheaves]] over the [[ordinal]] of [[natural numbers]], $\omega$. More properly, this is the category of trees of  _height_ bounded by $\omega$, in that every path from the root has length $\omega$ or less (when considered as ordinals). These trees can, however, be arbitrarily branching at every level.

An object is then a family of sets $X_i$ for each $i \in \omega$ with restriction functions $X_i \leftarrow X_{i+1}$. We can visualize this as a (potentially infinite) tree (really, forest) where an element of any $X_i$ is a node of the tree, and the restriction functions map each node to its parent node.

## Related pages

* [[synthetic guarded domain theory]]
* [[guarded recursion]]
* [[bridge type]]