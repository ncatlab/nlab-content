The __essential image__ of a [[functor]] $F: A\to B$ between [[category|categories]] or $n$-[[n-category|categories]] is the smallest [[replete subcategory]] of the target $n$-category $B$ containing the __image__ of $F$, which is in turn the smallest [[subcategory]] which contains all the $n$-cells which are strictly the images of $n$-cells in $A$.  Note that the property of belonging to the image is [[evil]]; of two [[equivalence|equivalent]] objects, one may belong while the other does not.  Passing to the essential image precisely removes this evil.


Note that:

* the *image* may contain some morphisms or cells which are not the images of any cell in $A$, namely the [[composite|compositions]] of $B$-composable chains of such image cells, whose preimage cells do not form any $A$-composable chain;
* the *essential image* in addition contains precisely all equivalent $k$-cells to the $k$-cells of the image for all $0 \leq k \leq n$.

+-- {: .query}

[[Urs Schreiber]]: one way to get good "non-evil" definitions is to never mention components, but just abstract arrow theory

over at [[image]] there is a definition in terms of equalizers: the image of a morphism $f : c \to d$ in a category is the limit $lim( d \stackrel{\to}{\to} d \sqcup_c d )$. This kind of definition will work in every context in which a notion of (weak) pushout and (weak) pullback exists. Has anyone thought about this? In particular I'd be interested in the notion of image for morphisms of $\infty$-groupoids.

I have a concrete question motivating this: what can one say about the essential image of the product of all [[Chern class]]es

$$
  \mathbf{B} U \stackrel{\prod_k c_k}{\to}
  \prod_k \mathbf{B}^{2 k -1} U(1)
$$

?

=--