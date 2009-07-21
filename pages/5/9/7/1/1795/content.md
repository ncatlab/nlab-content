#Idea#

The notion of _essential image_ is the generalization of the notion of [[image]] from a [[category theory|1-categorical]] to a [[higher category theory|higher categorical context]].

Given that there are different definitions of the ordinary notion of [[image]], there are different higher versions of these, which may or may not still be equivalent.


#Definitions#

## in $Cat$ ##

(A concrete realization of)
the __essential image__ of a [[functor]] $F: A\to B$ between [[category|categories]] or $n$-[[n-category|categories]] is the smallest [[replete subcategory]] of the target $n$-category $B$ containing the __image__ of $F$, which is in turn the smallest [[subcategory]] which contains all the $n$-cells which are strictly the images of $n$-cells in $A$.  Note that the property of belonging to the image is [[evil]]; of two [[equivalence|equivalent]] objects, one may belong while the other does not.  Passing to the essential image precisely removes this evil.

Note that:

* the *image* may contain some morphisms or cells which are not the images of any cell in $A$, namely the [[composite|compositions]] of $B$-composable chains of such image cells, whose preimage cells do not form any $A$-composable chain;
* the *essential image* in addition contains precisely all equivalent $k$-cells to the $k$-cells of the image for all $0 \leq k \leq n$.

## in $(\infty,1)$-categories ##

One of the definitions of the [[image]] of a morphism $f : c \to d$ is in terms of universal [[subobject]]s -- i.e. universal [[monomorphism]]s -- through which  $f$ factors.

This definition can be generalized to the context of [[(infinity,1)-category|(infinity,1)-categories]] [[presentable (infinity,1)-category|presented]] by a [[model category]].

+-- {: .un_defn}
###### Definition (homotopy image)

Let $C$ be an $S$ [[enriched model category]] satisfying some assumptions... . 

* A morphism $f : c \to d$ in $C$ is called a **homotopy monomorphism**  if the universal morphism $Id \times Id : c  \to c \times^h_d c$ into its [[homotopy pullback]]  along itself is an [[isomorphism]] in the [[homotopy category]].

* The **homotopy image** of $f$ is a factorization of $f$ into a cofibration $c \to f(c)$ followed by a homotopy monomorphism $f(c) \to d$ 

  * such that for any other such factorization $c \to e \to d$ there exists a unique morphism $f(c) \to e$ in the [[homotopy category]] making the obvious triangles commute.


=--

This is definition 2.36 in 

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

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