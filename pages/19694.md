
# The Divergence Theorem
* table of contents
{: toc}

## Idea

The _Divergence Theorem_ is a generalization of the classical _Ostrogradsky--Gauss Theorem_ to arbitrary dimensions.  As such, it is also a generalization of the (second) [[Fundamental Theorem of Calculus]] and a special case of the [[Stokes Theorem]].  The value of picking out this particular case is its formulation using [[vector fields]] in any number of dimensions.


## Statement

Let $n$ be a [[natural number]], and let $S$ be a [[continuously differentiable map|continuously differentiable]] simple [[closed manifold|closed]] [[hypersurface]] in $\mathbb{R}^n$, in other words the image of a continuously differentiable [[immersion]] of the $(n-1)$-[[sphere]].  By the [[Jordan–Brouwer separation theorem]], $S$ is the boundary of some [[bounded subspace|bounded]] [[open subset|open]] region $U$ in $\mathbb{R}^n$.

Let $F$ be a continuously differentiable [[vector field]] defined on a neighbourhood of $cl(U)$ (so defined on both $U$ and $S$).  We can integrate $F$ outwards across $S$ by taking the dot product $F \cdot \mathbf{n}$, where $\mathbf{n}$ is the unit normal vector field on $S$ (perpendicular to $S$ and pointing outwards, that is away from $U$) since $S$ is continuously differentiable, and integrating this with respect to hypersurface area on $S$.  Equivalently, form an exterior differential [[pseudoform]] of rank $n - 1$ by taking the dot product of $F$ with the [[Hodge dual]] of the identity vector-valued $1$-form $\mathrm{d}\mathbf{x}$ and integrate that outwards across $S$.  We can also form the [[divergence]] of $F$, a scalar field, by differentiating each component of $F$ with respect to the corresponding coordinate and adding these, and then integrate this with respect to volume on $U$; equivalently, form an exterior differential pseudoform of rank $n$ by multiplying the divergence of $F$ by the [[volume pseudoform]].

The Divergence Theorem states that these two integrals are equal:
$$ \int_S F \cdot \mathbf{n} = \int_U div F ,$$
or
$$ \int_S F \cdot *\mathrm{d}\mathbf{x} = \int_U div F \vol .$$
This is a special case of the generalized [[Stokes Theorem]], since $div F \vol$ is the [[exterior differential]] of $F \cdot *\mathrm{d}\mathbf{x}$.


[[!redirects divergence theorem]]
[[!redirects divergence theorems]]
[[!redirects Divergence Theorem]]

[[!redirects Ostrogradsky theorem]]
[[!redirects Ostrogradsky Theorem]]
[[!redirects Ostrogradsky's theorem]]
[[!redirects Ostrogradsky's Theorem]]
[[!redirects Ostrogradsky’s theorem]]
[[!redirects Ostrogradsky’s Theorem]]
[[!redirects Ostrogradsky\'s theorem]]
[[!redirects Ostrogradsky\'s Theorem]]
[[!redirects Остроградский theorem]]
[[!redirects Остроградский Theorem]]
[[!redirects Остроградский's theorem]]
[[!redirects Остроградский's Theorem]]
[[!redirects Остроградский’s theorem]]
[[!redirects Остроградский’s Theorem]]
[[!redirects Остроградский\'s theorem]]
[[!redirects Остроградский\'s Theorem]]

[[!redirects Gauss theorem]]
[[!redirects Gauss Theorem]]
[[!redirects Gauss's theorem]]
[[!redirects Gauss's Theorem]]
[[!redirects Gauss’s theorem]]
[[!redirects Gauss’s Theorem]]
[[!redirects Gauss\'s theorem]]
[[!redirects Gauss\'s Theorem]]
[[!redirects Gauß theorem]]
[[!redirects Gauß Theorem]]
[[!redirects Gauß's theorem]]
[[!redirects Gauß's Theorem]]
[[!redirects Gauß’s theorem]]
[[!redirects Gauß’s Theorem]]
[[!redirects Gauß\'s theorem]]
[[!redirects Gauß\'s Theorem]]

[[!redirects Ostrogradsky-Gauss theorem]]
[[!redirects Ostrogradsky-Gauss Theorem]]
[[!redirects Ostrogradsky–Gauss theorem]]
[[!redirects Ostrogradsky–Gauss Theorem]]
[[!redirects Ostrogradsky--Gauss theorem]]
[[!redirects Ostrogradsky--Gauss Theorem]]
