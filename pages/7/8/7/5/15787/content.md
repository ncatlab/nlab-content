
#Contents#
* table of contents
{:toc}

## Idea

Given a [[Dirichlet character]]

$$
  \chi \;\colon\; (\mathbb{Z}/N\mathbb{Z})^\times \longrightarrow \mathbb{C}^\times
$$

it is called _even_ if $\chi(-1) = 1$ and _odd_ if $\chi(-1) = -1$.

The _[[theta function]]_ associated with $\chi$ is the function on $\mathbb{R}_+$ defined by

$$
  \theta_\chi(\tau)
  \coloneqq
  \left\{
    \array{
      \underset{n \in \mathbb{Z}}{\sum} \chi(n) \exp(-\pi n^2 t/N) & if\; \chi\; even
      \\
      \underset{n \in \mathbb{Z}}{\sum} n \chi(n) \exp(-\pi n^2 t/N) & if\; \chi\; odd
    }
  \right.
$$

where $N$ is the [[conductor]] of $\chi$.

## Properties

### Relation to Jacobi theta function

For trivial $\chi$ the Dirichlet theta reproduces the [[Jacobi theta function]].

### Mellin transform and relation to Dirichlet L-function

The [[Mellin transform]] of this is the completed [[Dirichlet L-function]] associated with $\chi$ (e.g. [Continuations, p. 8](#Continuations))


## Related concepts

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]


## References

* section 3 of _Continuations and functional equations_ ([pdf](http://people.reed.edu/~jerry/361/lectures/feqn.pdf))