
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The notion of _homotopy image_ generalizes the notion of [[image]] of a morphism in a [[category]] to that of a morphism in a [[presentable (infinity,1)-category]] or [[model category]].

## Definition 

### In a model category

One of the definitions of the [[image]] of a morphism $f : c \to d$ is in terms of universal [[subobject]]s -- i.e. universal [[monomorphism]]s -- through which  $f$ factors.

This definition can be generalized to the context of [[(infinity,1)-category|(infinity,1)-categories]] [[presentable (infinity,1)-category|presented]] by a [[model category]].

+-- {: .num_defn}
###### Definition (homotopy image)

Let $C$ be an $S$ [[enriched model category]] satisfying some assumptions... . 

* A morphism $f : c \to d$ in $C$ is called a **homotopy monomorphism**  if the universal morphism $Id \times Id : c  \to c \times^h_d c$ into its [[homotopy pullback]]  along itself is an [[isomorphism]] in the [[homotopy category]].

* The **homotopy image** of $f$ is a factorization of $f$ into a cofibration $c \to f(c)$ followed by a homotopy monomorphism $f(c) \to d$ 

  * such that for any other such factorization $c \to e \to d$ there exists a unique morphism $f(c) \to e$ in the [[homotopy category]] making the obvious triangles commute.


=--

### In an $(\infty,1)$-topos

The above definition of _homotopy monomorphism_ [[presentable (infinity,1)-category|presents]] precisely the notion of _[[monomorphism in an (∞,1)-category]]_ : a [[(-1)-truncated]] morphism.
Because ([[Higher Topos Theory|HTT, lemma 5.5.6.15]]) a morphism is [[(-1)-truncated]] precisely if its [[diagonal]] is [[(-2)-truncated]], hence is an [[equivalence in an (∞,1)-category|equivalence]]. 

Therefore in an [[(∞,1)-topos]] the homtopy image of a morphism is a presentation for the [[n-connected/n-truncated factorization system|(-1)-connected/(-1)-truncated factorization]] of the morphism.

See _[[∞-image]]_.


## Related concepts

* [[image]], [[coimage]]

## References

A definition for model categories is def. 2.36 in 

* [[Clark Barwick]], _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

For the definition in $(\infty,1)$-topos theory see the references at [[n-connected/n-truncated factorization system]].
