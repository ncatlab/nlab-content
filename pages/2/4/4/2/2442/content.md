
<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#

* autoamtic table of contents goes here
{:toc}

#Idea#

An ordinary  smooth [[vector bundle]] on a [[manifold]] $X$ may be identified with its [[sheaf]] of [[section]]s, which is a locally free sheaf of modules over its [[structure sheaf]] and all such localyy free module sheaves arise this way.

The definition of vector bundles in terms of sheaves of sections therefore immediately generalizes to every [[ringed space]] and in particular to [[supermanifold]]s.

#Definition#

A **super vector bundle** over a [[supermanifold]] $X$ is a locally free [[sheaf]] on the [[category of open subsets]] of $|X|$ of modules for the [[structure sheaf]] $O_X$.


#Examples#

## super tangent bundle ##

The [[tangent bundle]] of an ordinary [[manifold]] has the sheaf of sections given by the [[derivation]]s of the [[structure sheaf]]. The same definition works here:

the **super tangent bundle** $T X$ of a [[supermanifold]] $X$ is given by the sheaf $U \mapsto Der O_X(U)$.

so a super tangent vector is a global section of this sheaf of derivations. 

**Example** on the  [[supermanifold]] $\mathbb{R}^{1|1}$ with its canonical coordinates

$$
  t \in C^\infty(\mathbb{R}^{1|1})^{ev}
$$

$$
  \theta \in C^\infty(\mathbb{R}^{1|1})^{odd}
$$

there is the odd vector field

$$
  D := \partial_\theta + \theta \cdots \partial_{t}
$$

whose super Lie bracket with itself vanishes

$$
  [D, D] = 0
  \,.
$$

**Claim** This odd vector field $D$ is left invariant with respect to the [[supergroup|super Heisenberg group]] structure on $\mathbb{R}^{1|1}$.

This means that $Lie(\mathbb{R^{1|1}})$ is free on one odd generator.