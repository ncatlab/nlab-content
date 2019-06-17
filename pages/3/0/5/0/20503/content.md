
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _collar neighbourhood theorem_ due to [Brown 62](#Brown62), hence also known as _Brown's collaring theorem_, says that the [[boundary]] of any [[manifold with boundary]] always admits a "collar", namely an [[open neighbourhood]] which is the [[Cartesian product]] of the boundary with a [[half-open interval]].

This theorem is central notably for the definition and behaviour of [[categories of cobordisms]].

## Statement

Let $X$ be a [[topological manifold]] or [[smooth manifold]] [[manifold with boundary|with boundary]] $\partial X$. Then the [[boundary]] [[topological subspace|subspace]] inclusion has an [[open neighbourhood]] which is [[homeomorphism|homeomorphic]] or [[diffeomorphic]], respectively, to a [[collar]], i.e. to the [[product space|Cartesian product]] manifold with boundary $\partial X \times [0,1)$ of $\partial X$ with the [[half-open interval]]:

$$
  \partial X
  \overset{
     (id, 0)
  }{\hookrightarrow}
  (\partial X) \times [0,1)
  \overset{et}{\hookrightarrow}
  X
  \,.
$$

## Related concepts

* [[cobordism]]

## References

Original references are:

* {#Brown62} [[Morton Brown]], _Locally flat imbeddings of topological manifolds_, Annals of Mathematics, Vol. 75 (1962), p. 331-341 ([jstor:1970177](https://www.jstor.org/stable/1970177))

* [[Robert Connelly]], _A new proof of Brown's collaring theorem_, Proceedings of the American Mathematical Society 27 (1971), 180 – 182 ([jstor:2037284](https://www.jstor.org/stable/2037284))

Quick review and sketch of the proof is in

* p. 5 of _Manifolds with boundary_ ([pdf](http://math.ucr.edu/~res/math260s10/manwithbdy.pdf), [[ManifoldsWithBoundary.pdf:file]])

[[!redirects collar]]
[[!redirects collars]]
