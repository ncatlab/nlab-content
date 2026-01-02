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

## Idea

The **[[topos]] of trees** is the category of [[presheaves]] over the [[ordinal]] of [[natural numbers]], $\omega$. The [[internal language]] of this category is used as a convenient setting for working with [[coinductive|coinductively defined]] sets. The intuition is that many coinductive definitions can be formally constructed as $\omega^{op}$ [[limits]] and an object of the topos of trees can be thought of as a presentation of an object as a limit. This technique has become common in [[programming language semantics]], where it is known as "step-indexing" or [[guarded domain theory]].

## Presheaves as Trees

By "tree" here we mean trees of  _height_ bounded by $\omega$, in that every path from the root has length $\omega$ or less (when considered as ordinals). These trees can, however, be arbitrarily branching at every level.

An object is then a family of sets $X_i$ for each $i \in \omega$ with restriction functions $X_i \leftarrow X_{i+1}$. We can visualize this as a (potentially infinite) tree (really, forest) where an element of any $X_i$ is a node of the tree, and the restriction functions map each node to its parent node.


## As Sheaves

The topos of trees is equivalent to a [[sheaf category]] on the ordinal $\omega + 1$, where the sheaf condition is that the set $X_\omega$ with its restriction functions $X_\omega \to X_i$ is a limit of the $\omega^op$ diagram given by the restriction to a presheaf on $\omega$. Sheafification of a presheaf on $\omega+1$ then replaces $X_\omega$ with a limit. This is equivalently defined as the sheaves on the [[topological space]] given by the [[Alexandroff topology]] on the poset $\omega^{op}$.

## Related pages

* [[synthetic guarded domain theory]]
* [[guarded recursion]]
* [[bridge type]]