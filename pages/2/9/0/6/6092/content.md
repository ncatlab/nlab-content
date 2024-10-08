
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Goldman bracket_ of a [[compact space|compact]] [[closed manifold|closed]] [[surface]] $\Sigma$ is a [[Lie algebra]] structure on the [[free abelian group]] generated from the [[isotopy]] classes of based loops in $\Sigma$.

Equivalently, the Goldman bracket on $\Sigma$ is a structure on the 0th [[homology]] $H_0(L \Sigma)$ of the [[free loop space]] of $\Sigma$. It is in fact just the lowest degree of the [[string topology]] operations on $\Sigma$. See there for more details.

## Definition

Let $\Sigma$ be a compact closed and [[orientation|oriented]] surface ([[manifold]] of [[dimension]] 2). For $\gamma : S^1 \to \Sigma$ a [[continuous function]] from the based [[circle]], write $[\gamma]$ for the corresponding [[isotopy]] class. 

For $[\gamma_1]$ and $[\gamma_2]$ two such classes, one can always find differentiable representatives $\gamma_1$ and $\gamma_2$ that intersect - if they intersect at some point $p$ - [[transversal map|transversally]]. Write $\gamma_1 \ast_p \gamma_2$ for the curve obtained by starting at the intersection point $p$, traversing along $\gamma_1$ back to that point and then along $\gamma_2$. 

The **Goldman bracket** on the free abelian group on classes $[\gamma]$ is defined by

$$
  \left\{
    [\gamma_1], [\gamma_2]
  \right\}
  :=
  \sum_{p \in \gamma_1 \cap \gamma_2}
  sgn(p) [\gamma_1 \ast_p \gamma_2]
  \,,
$$

where $sgn(p)$ is +1 if $T_p \gamma_1, T_p \gamma_2$ is an oriented [[basis]] of the [[tangent space]] $T_p \Sigma$, and -1 otherwise.


## References

The original definition is due to

* [[William M. Goldman]], _Invariant functions on Lie groups and Hamiltonian flows of surface group representations_, Invent. Math. __85__ (1986), no. 85, 263--302 [doi](https://doi.org/10.1007/BF01389091)

The relation to [[string topology]] is due to

* [[Moira Chas]], [[Dennis Sullivan]], _String topology_, Ann. Math. [math.GT/9911159](http://arxiv.org/abs/math/9911159)
