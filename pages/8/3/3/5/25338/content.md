## Definition

A __necklace__ is a gluing of [[simplicial sets]]
$$\Delta^{n_1}\vee \Delta^{n_2}\vee\cdots\vee \Delta^{n_k}.$$

Here the final vertex of $\Delta^{n_i}$ is identified with the initial vertex of $\Delta^{n_{i+1}}$.

## Applications

Necklaces provide a way to extract a [[simplicial category]] from a [[simplicial set]] (not necessarily fibrant) in the [[Joyal model structure]].

Given such a [[simplicial set]] $X$, construct a [[simplicial category]] by taking its objects to be vertices of $X$, and for a pair of object $x$, $y$ take as the [[simplicial set]] of morphisms $x\to y$ the simplicial set whose $k$-simplices are necklaces of length $k$ in $X$ as described above, with the initial vertex of $\Delta^{n_1}$ mapping to $x$ and the final vertex of $\Delta^{n_k}$ mapping to $y$.

Dugger and Spivak prove that the resulting [[simplicial category]] is weakly equivalent to the other [[simplicial categories]] that one can extract from $X$, e.g., the left adjoint of the [[homotopy coherent nerve]].

## Related concepts

* [[homotopy coherent nerve]]

* [[simplicial category]], [[quasicategory]]

## References

* [[Daniel Dugger]], [[David I. Spivak]], _Rigidification of quasi-categories_, [arXiv:0910.0814](https://arxiv.org/abs/0910.0814).

* [[Daniel Dugger]], [[David I. Spivak]], _Mapping spaces in Quasi-categories_, [arXiv:0911.0469](https://arxiv.org/abs/0911.0469).

A similar idea is developed for [[complete Segal spaces]] in

* Shaul Barkan, Jan Steinebrunner, _Segalification and the Boardmann-Vogt tensor product_, [arXiv:2301.08650](https://arxiv.org/abs/2301.08650).

