In geometry, a **flag** is a chain of incidence relations, as for example between distinct linear subspaces 

$$V_0 \subseteq V_1 \subseteq \ldots \subseteq V_n$$ 

of a fixed vector space $V$, or between isotropic subspaces, etc. 

## Flags of posets

Generally speaking, if $P$ is a [[poset]], a flag is a chain 

$$x_0 \lt x_1 \lt \ldots \lt x_n$$ 

and the set of elements $\{x_0, x_1, \ldots, x_n\}$ can be thought of as an $n$-simplex of a simplicial complex whose vertices are the poset elements. Hence we have a functor 

$$Flag: Pos \to SimpComplex$$ 

In the other direction, there is an underlying functor 

$$U: SimpComplex \to Pos$$ 

which sends a [[simplicial complex]] $(V, \Sigma)$ to $\Sigma$ (regarded as a poset ordered by inclusion). The composite 

$$Flag \circ U: SimpComplex \to SimpComplex$$ 

is called the [[subdivision]] functor, or, more exactly, the [[barycenter|barycentric subdivision]] functor.
