Given a (directed) [[graph]] $D$, that is, a collection of vertices and of labeled arrows between them, the **free groupoid** $G(D)$ **on**$D$ is the [[category]] -- in fact the [[groupoid]] -- that has the vertices of $D$ as [[object]]s, and whose [[morphism]]s are constructed recursively by formal composition (i.e., juxtaposition) from identity maps, the arrows of $D$ and formal [[inverse]]s for the arrows of $D$. The only relations between morphisms of $G(D)$ are the necessary ones defining the [[identity]] of each object, the [[inverse]] of each arrow in $D$ and the associativity of composition. 
This is clearly a groupoid, which comes with an evident morphism $D \to G(D)$ of directed graphs. 

The above sketched construction could be made more precise, but what really matters is the [[universal property]] it enjoyes: the free groupoid $G(D)$ is the universal ([[initial object|initial]]) [[groupoid]] mapping out of $D$. By varying $D$, the free groupoid yields a [[functor]] $G$ from [[directed graph]]s to [[groupoid]]s, [[left adjoint]] to the forgetful functor. 

This last conceptual characterization is best taken as the definition. Similarly, it is possible to construct the left adjoint to the forgetful functor from groupoids to categories, that is the **free groupoid over a category**.

#Related notions#

A [[quiver]] category is the free [[category]] on a [[graph]].