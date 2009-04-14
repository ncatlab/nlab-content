{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


In 1966, [J. Wolfgang Smith](http://www.ams.org/mathscinet/search/author.html?mrauthid=541554) studied the following extension of the notion of a smooth manifold.

+-- {: mynumdef #SmithSp}
###### Definition
A _differentiable structure_ on an arbitrary topological space $X$ is a family, $\mathcal{F}$, of real-valued functions on $X$ satisfying a certain closure condition.

To express the closure condition, we need an auxiliary notion.
A _plot_ of $(X, \mathcal{F})$ is a continuous map $\phi : U \to X$ with domain an open subset of some Euclidean space with the property that $f \circ \phi \in C^\infty(U)$ for all $f \in \mathcal{F}$.

The closure condition is that if a continuous map $f: X \to \mathbb{R}$ has the property that whenever $\phi: U \to X$ is a plot for $(X, \mathcal{F})$ then $f \circ \phi \in C^\infty(U)$ then $f \in \mathcal{F}$.
=--


## References

* [The de Rham theorem for general spaces.](http://www.ams.org/mathscinet-getitem?mr=202154) 1966