A paracyclic (synonym: $\mathbf{Z}$-cyclic) 
object in a category $C$ is a simplicial object $F_\bullet$ together with
a sequence of isomorphisms $t_n : F_n \rightarrow F_n$, $n\geq 1$, such that
$$\array{
\partial_i t_n = t_{n-1} \partial_{i-1},\,\, i \gt 0, &
\sigma_i t_n = t_{n+1} \sigma_{i-1},\,\, i \gt0, \\
\partial_0 t_n = \partial_n, & \sigma_0 t_n = t_{n+1}^2 \sigma_n,
}$$
where $\partial_i$ are boundaries, $\sigma_i$ are degeneracies. If $t_n^{n+1} = \mathrm{id}:F_n\to F_n$ then paracyclic object is [[cyclic object|cyclic]].