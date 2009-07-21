
# Idea #

The notion of _homotopy image_ generalizes the notion of [[image]] of a morphism in a [[category]] to that of a morphism in a [[presentable (infinity,1)-category]] or [[model category]].

# Definition #

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

