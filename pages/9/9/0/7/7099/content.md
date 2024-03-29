+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[action functional]] for [[higher U(1)-gauge theory]] in the presence of background [[electric charge]] contains a charge-coupling term which is of [[schreiber:infinity-Chern-Simons theory]]-type.

## Definition

Let $X$ be a [[smooth manifold]] of [[dimension]] $d$ and let $n \in \mathbb{N}$. Then a [[higher U(1)-gauge field|degree n U(1)-gauge field]] on $X$ is a [[circle n-bundle with connection]] $\hat F : X \to \mathbf{B}^n U(1)_{conn}$. 

### For smooth currents

A background [[electric current]] for this is a circle $(d-n-1)$-bundle with connection $\hat j_{el} : X \to \mathbf{B}^{d-n-1} U(1)_{conn}$.

The coupling [[action functional]] is

$$
  \exp(i S_{el}(-)) : \hat F \mapsto \exp(i \int_X \hat F \cup \hat j)
$$

given by the [[higher holonomy]]/[[fiber integration in ordinary differential cohomology]] of the [[Beilinson-Deligne cup product]] of the gauge field with the higher electric background.

### For $\delta$-distributed charges

The object $\hat j_{el}$ above models the [[electric current]] of a smooth density of charged electric [[brane|(n-1)-branes]]. If we think of the current form $j_{el}$ as being a [[delta distribution]] on the [[worldvolume]] $\Sigma \to X$ of a single charged  [[brane|(n-1)-branes]], then (one may thing of this via [[Poincare duality]]) the electric charge coupld action functional becomes the [[higher holonomy]] of the [[higher U(1)-gauge field]] over $\Sigma$

$$
  \exp(i S_{el}(-)) : \hat F \mapsto hol_\Sigma(\hat F)
  \,.
$$

If, moreover, we restrict attention to gauge field configurations whose underlying [[circle n-bundle]] is trivial, which are given by globally defined [[differential form|n-forms]] $A$ (with $d A = F$), then this is

$$
  \cdots = \exp(i \int_\Sigma A)
  \,.
$$

In the form of this simple special case the higher electric background charge coupling is often presented in [[physics]] texts.

## References

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_


