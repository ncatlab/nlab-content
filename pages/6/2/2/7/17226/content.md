

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[generalized homology theory]] [[Brown representability theorem|represented]] by a [[Thom spectrum]]. The dual concept of [[cobordism cohomology theory]].

## Examples

[[!include flavours of cobordism cohomology theories -- table]]

## Geometric model

See Section 2 in Atiyah \cite{Atiyah}.
Atiyah's geometric model for bordism homology groups
defines them as equivalence classes of maps of manifolds.

We concentrate on the oriented case, corresponding to the [[Thom spectrum]]
$\mathrm{M} \mathrm{SO}$.

Specifically, the $k$-dimensional oriented bordism group $\mathrm{M} \mathrm{SO}_k(X)$ of a smooth manifold $X$
(more generally, a [[paracompact Hausdorff topological space]],
even more generally, an arbitrary [[topological space]] provided
we use [[numerable open covers]] for trivializations)
is defined as the quotient of the [[commutative monoid]] $C_k(X)$ by
the equivalence relation $\sim$ of bordism, defined below.

Elements of $C_k(X)$ are smooth (or continuous) maps $F\colon M\to X$,
where $M$ is a [[compact]] $k$-dimensional
[[oriented]] [[smooth manifold]] (without boundary).

Two such maps $F$ and $F'$ are equivalent
if there is a smooth (or continuous) map $G\colon N\to X$,
where $N$ is a [[compact]] $(k+1)$-dimensional
[[oriented]] [[smooth manifold]] with boundary
$$\partial N = M\sqcup M'$$
such that $G|_M=F$ and $G|_{M'}=F'$.

One can also defined [[twisted homology groups]] in the same manner.
Twists are [[principal bundles]] $\alpha$ over $X$ with [[structure group]] $\mathbf{Z}/2$.
Elements of $C_k(X,\alpha)$
are maps $F\colon (M,\tau)\to (X,\alpha)$,
where $M$ is a [[compact]] $k$-dimensional [[smooth manifold]]
equipped with a principal $\mathbf{Z}/2$-bundle $\tau$,
and the map $F$ is a morphism of such [[principal bundles]].
Likewise, $F\sim F'$ if there is a map $G\colon (N,\sigma)\to(X,\alpha)$
with the same properties as above.



## Related concepts

* [[bordism]]

* [[ordinary homology]]

* [[equivariant bordism homology theory]]

* [[stable homotopy homology theory]]

## References

The original article introducing cobordism as a [[Whitehead-generalized cohomology theory]]:

\bibitem{Atiyah}
[[Michael Atiyah]], _Bordism and Cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 57, Issue 2, April 1961, pp. 200 - 208 ([doi:10.1017/S0305004100035064](https://doi.org/10.1017/S0305004100035064), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahb.pdf))

Surveys:

* [[Peter Landweber]], _A survey of bordism and cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 100, Issue 2 September 1986 , pp. 207-223 ([doi:10.1017/S0305004100066032](https://doi.org/10.1017/S0305004100066032))

* Max Hopkins, _The Extraordinary Bordism Homology_, 2016  ([pdf](http://cseweb.ucsd.edu/~nmhopkin/papers/Bordism.pdf), [[HopkinsBordism.pdf:file]])

For more, see the references at _[[cobordism cohomology theory]]_.

[[!redirects bordism homology theories]]
