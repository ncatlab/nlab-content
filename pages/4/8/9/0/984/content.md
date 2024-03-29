
#Contents#
* table of contents
{:toc}

## Idea

The concept of _cyclic object_ is the generalization of that of _[[cyclic sets]]_ where [[Set]] may be replaced with any other [[category]].

Cyclic objects are used in the description of the cyclic structure on [[Hochschild homology]]/[[Hochschild cohomology]] and hence for the discussion of [[cyclic homology]]/[[cyclic cohomology]].

## Definition

Let $\Lambda$ denote the [[cyclic category]] of [[Alain Connes]].  A __cyclic object__  in a [[category]] $C$ is a $C$-valued [[presheaf]] on $\Lambda$.  ([[formal duality|Dually]], a *cocyclic object* is a [[copresheaf]] on the cyclic category.)

Equivalently, this is a [[simplicial object]] $F_\bullet$ together with a sequence of isomorphisms $t_n : F_n \rightarrow F_n$, $n\geq 1$, such that
$$\array{
\partial_i t_n = t_{n-1} \partial_{i-1},\,\, i \gt 0, &
\sigma_i t_n = t_{n+1} \sigma_{i-1},\,\, i \gt0, \\
\partial_0 t_n = \partial_n, & \sigma_0 t_n = t_{n+1}^2 \sigma_n,\\
t^n_{n+1} = \mathrm{id}
}$$
where $\partial_i$ are boundaries, $\sigma_i$ are degeneracies.

## Related concepts

* [[cyclic space]]

* [[cyclic set]]

* [[cyclotomic space]], [[cyclotomic spectrum]]

## References

See the references at *[[cyclic category]]* and at *[[cyclic set]]* and *[[cyclic space]]*.




[[!redirects cyclic objects]]

[[!redirects cocyclic object]]
[[!redirects cocyclic objects]]
