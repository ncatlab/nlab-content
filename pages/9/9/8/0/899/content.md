#Contens#
* automatic table of contents goes here
{:toc}

## Idea
A **topological group** is an [[internalization|internal]] [[group object]] in the category of [[topological space|topological spaces]].

More explicitly, it is a group equipped with a topology such that the multiplication and inversion maps are continuous.

## Unitary representation on Hilbert spaces

**Definition.** A unitary representation $R$ of a topological group $G$ in the [[Hilbert space]] $\mathcal{H}$ is a continuous homomorphism

$$
   R: G \to \mathcal{U}(\mathcal{H})
$$

where $\mathcal{U}(\mathcal{H})$ is the group of [[unitary operator]]s on $\mathcal{H}$ with respect to the strong topology.

Note that $\mathcal{U}(\mathcal{H})$ is a complete, metrizable topological group in the strong topology, see proposition 3.11 in the book by Schottenloher cited in the references.

In physics, when a classical system is symmetric, i.e. invariant in a proper sense, with respect to the action of a topological group $G$, then an unitary representation of $G$ is often called a **quantization** of $G$.

### Why the strong topology is used

The reason that in the definition of an unitary representation, the strong operator topology on $\mathcal{U}(\mathcal{H})$ is used and not the norm topology, is that only few homomorphisms turn out to be continuous in the norm topology.

Example: let $G$ be a compact [[Lie group]] and $L^2(G)$ be the Hilbert space of square integrable measurable functions with respect to its [[Haar measure]]. The right regular representation of $G$ on $L^2(G)$ is defined as
$$
      R: G \to \mathcal{U}(L^2(G))
$$
$$
         g \mapsto (R_g: f(x) \mapsto f(xg))
$$
and this will generally not be continuous in the norm topology, but is always continuous in the strong topology. 

## References

The following monograph is not particulary about group representations, but some content of this page is based on it:

* Martin Schottenloher: _A mathematical introduction to conformal field theory._ Springer, 2nd edition 2008 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1161.17014&format=complete))

[[!redirects topological groups]]