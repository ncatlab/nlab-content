
# Super tangent bundles
* table of contents
{: toc}

## Idea

The [[tangent bundle]] of an ordinary [[manifold]] is a [[vector bundle]] whose [[sheaf of sections]] is given by the [[derivation]]s of the [[structure sheaf]]. The same idea applies to a [[supermanifold]] to produce a [[super vector bundle]].


## Definition

The **super tangent bundle** $T X$ of a [[supermanifold]] $X$ is given by the sheaf $U \mapsto Der O_X(U)$.

So a __super tangent vector__ is a [[global section]] of this sheaf of derivations. 


## Example

On the  [[supermanifold]] $\mathbb{R}^{1|1}$ with its canonical coordinates

$$
  t \in C^\infty(\mathbb{R}^{1|1})^{ev}
$$

$$
  \theta \in C^\infty(\mathbb{R}^{1|1})^{odd}
$$

there is the odd vector field

$$
  D \coloneqq \partial_\theta + \theta \cdot \partial_{t}
$$

whose super Lie bracket with itself vanishes

$$
  [D, D] = 0
  \,.
$$
=--

+-- {: .un_thm}
###### Claim
This odd vector field $D$ is left invariant with respect to the [[supergroup|super translation group]] structure on $\mathbb{R}^{1|1}$.
=--

This means that $Lie(\mathbb{R}^{1|1})$ is free on one odd generator.


[[!redirects super tangent bundle]]
[[!redirects super tangent bundles]]
[[!redirects super tangent bundle of a supermanifold]]
[[!redirects super tangent bundles of supermanifolds]]
[[!redirects super tangent bundle is supermanifold]]

[[!redirects super tangent vector]]
[[!redirects super tangent vectors]]
