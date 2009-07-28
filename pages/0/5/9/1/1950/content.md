
This entry describes special methods for the construction of  fibrant replacements in the standard [[model structure on simplicial sets]].

# Ex-functor #


For $\Delta[k]$ the simplicial $k$-[[simplex]] let $sd \Delta[k]$ be its _barycentric subdivision_: this is the simplicial set that is the [[nerve]] of the [[poset]] of non-degenerate sub-simplicies in $\Delta[k]$.

For instance

$$
  sd \Delta^1 = \{0 \to (0,1) \leftarrow 1\}
$$

This defines a functor $Ex : SSet \to SSet$ by setting

$$
  (Ex X)_n = Hom_{SSet}(sd \Delta[k], X)
$$

and a natural map

$$
  X \to Ex X
  \,.
$$

Define the simplicial set $Ex^\infty X$ to be the [[colimit]] over

$$
  X \to Ex X \to Ex Ex X \to \cdots
  \,.
$$

Then

* $Ex^\infty X$ is a [[Kan complex]];

* $X \to Ex^\infty X$ is a natural weak equivalence.

## References ##

For instance section 3 of 

* Jardine, _Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))