
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A **ringed site** is a [[site]] $S_X$ equipped with a [[sheaf]] $O_X$ of [[ring]]s.

A morphism $(f^{-1}, f^\sharp):(S_X, O_X) \to (S_Y, O_Y)$ of ringed sites is a pair $(f^{-1},f^\sharp)$ where $f^{-1}:S_Y\to S_X$ is a functor representing a morphism $f:S_X\to S_Y$ of sites and $f^\sharp:O_Y\to f_* O_X$ is a morphism of sheaves of rings over $Y$ (also called a $f$-[[comorphism]]). 

## Examples

* The archetypical and motivating class of examples is: $X$ a [[topological space]], $S_X = Op(X)$ the [[category of open subsets]] of $X$ with its standard [[Grothendieck topology]] and $O_X := C(-,\mathbb{R})$ the sheaf of continuous functions with values in (say) the real numbers.

* A [[supermanifold]] is a ringed site where $X$ is the underlying [[manifold]], $S_X = Op(X)$ the [[category of open subsets]] $U$ of $X$ such that for each contractible $U$ $O_X(U) \simeq C^\infty(U) \otimes_{\mathbb{R}} \Lambda^\bullet V$ for $V$ a fixed finite dimensional vector space, $\Lambda^\bullet V$ its exterior algebra and the isomorphism being one of $\mathbb{Z}_2$-grading rings.

* The full generalization of the notion of a ringed site is that of a [[structured (∞,1)-topos]].


## Related concepts

* [[ringed space]], [[locally ringed space]]

*  **ringed site**, [[locally ringed site]]

*  [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* [[structured (∞,1)-topos]]

## References

* _Ringed sites_ ([web](http://stacks.math.columbia.edu/tag/04KQ)); _Locally ringed topoi_ ([web](http://stacks.math.columbia.edu/tag/04ER)); [[Aise Johan de Jong]],  _[[The Stacks Project]]_
{#deJong}


[[!redirects ringed sites]]
[[!redirects locally ringed site]]
[[!redirects locally ringed sites]]