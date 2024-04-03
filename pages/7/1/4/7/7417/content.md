
#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of [[symplectic vector space]] from [[symplectic geometry]] to [[n-plectic geometry]].

## Definition

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, an **[[n-plectic vector space]]**
is a [[vector space]] $V$ (over the [[real numbers]]) equipped with an $(n+1)$-linear skew function

$$
  \omega : \wedge^{n+1} V \to \mathbb{R}
$$

such that regarded as a function

$$
  V \to \wedge^n V^*
$$

is has trivial [[kernel]].

=--

The concept of [[Lagrangian subspace]] also generalizes accordingly.


Let $(V,\Omega)$ be an $n$-plectic vector space, and $W\subset V$ a subspace. Let $1\leq l \leq n-1$. We define the $l$-orthogonal subspace of $W$ as

$$
W^{\perp,l} = \{ v\in V \vert \forall w_1,\cdots,w_l \in W  ,  \imath_{v\wedge w_1\wedge \cdots w_l}\Omega =0\}
$$

Then we say $W$ is $l$**-isotropic**, $l$**-coisotropic**, and $l$**-lagrangian** if $W\subset W^{\perp,l}$, $W^{\perp,l} \subset W$, and $W=W^{\perp,l}$, respectively.

See Section 3 of [de Leon et al. 2003](#dL03) for more.


## Related concepts

* [[n-plectic manifold]]

* [[Heisenberg Lie n-algebra]]

## References

* {#dL03} Manuel de León, David Martín de Diego,
Aitor Santamaría-Merino. *Tulczyjew’s triples and lagrangian submanifolds in classical field theories* (2003). ([arXiv:math-ph/0302026](https://arxiv.org/abs/math-ph/0302026)).

[[!redirects n-plectic vector spaces]]

