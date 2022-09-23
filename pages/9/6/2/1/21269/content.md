[[!redirects tangles]]

#Contents#
* table of contents
{:toc}


## Idea

An *ordinary tangle* is 1-manifold with boundary that is embedded in the 2-cube (or 3-cube), such that the tangle's boundary is embedded in two chosen opposing sides of the cube. Thus, one may think of a tangle as a [[knot]] that was cut at several points and the resulting strands were pulled apart at their endpoints to opposite sides of the cube. 

The notion generalizes to that of *$m$-tangles in dimension $n$*, which are $m$-manifolds with corners embedded in the $n$-cube that, such that their corners are appropriately embedded in the $n$-cube's boundary. 

## Definition of ordinary tangles

Tangles form a [[category]]. Its objects are finite [[subsets]] of $\mathbf{R}^2$. Morphisms $A\to B$ are embeddings of unions of finitely many closed intervals and circles into $[0,1]\times\mathbf{R}^2$ such that the restriction of the embedding to the endpoints yields a bijection to $A\sqcup B$. Morphisms are composed by gluing two copies of $[0,1]$ together and rescaling.

As usual, this suffers from being associative only up to an ambient isotopy. Thus, one can either take ambient isotopy classes of such embeddings, obtaining a [[1-category]] of tangles, or instead turn tangles into an [[(∞,1)-category]],
in which case morphisms $A\to B$ will encode the whole [[homotopy type]] of the space of embeddings described above.

## Higher-dimensional variants

Higher-dimensional tangles, i.e. $m$-manifold with corners embedded in the $n$-cube, were considered for instance in [Baez and Dolan 95](#BaezDolan95). A "tame" definition of tangles that admit *finite* [[stratified space|stratifications]] by their critical point types was given in [Dorn and Douglas 22](#DornDouglas22).

## Related concepts

* [[generalized tangle hypothesis]]
* [[manifold diagram|manifold diagrams]]

## References

* {#BaezDolan95} [[John Baez]] and [[James Dolan]], _Higher-dimensional Algebra and Topological Quantum Field Theory_ 1995 ([arXiv](http://arxiv.org/abs/q-alg/9503002))

* {#DornDouglas22} Christoph Dorn and Christopher Douglas, _Manifold diagrams and tame tangles_, 2022 ([pdfs](https://cxdorn.github.io/manifold-diagram-paper/))

