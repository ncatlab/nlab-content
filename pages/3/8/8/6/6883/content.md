
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

By the general mechanism of [[schreiber:∞-Chern-Simons theory]], every [[invariant polynomial]] of total degree 2 induces a 1-dimensional Chern-Simons-like theory.

## Examples

### For the first Chern class

By the general mechanism of [[schreiber:∞-Chern-Simons theory]] there is a Chern-Simons action functional associated to the first [[Chern class]], or rather to the corresponding [[invariant polynomial]], which is simply the [[trace]] map on the [[unitary Lie algebra]]

$$
  tr : \mathfrak{u}(n) \to \mathbb{R}
  \,.
$$

This yields an [[action functional]] for a 1-dimensional [[QFT]] as follows:

The [[configuration space]] over a 1-dimensional $\Sigma$ is the [[groupoid of Lie algebra valued 1-forms]] $\Omega^1(\Sigma, \mathfrak{u})$. After identifying $\Sigma \subset \mathbb{R}$ this may be identified with the space of $\mathfrak{u}(n)$-valued functions.

The action functional is simply the [[trace]] operation

$$
  S_{CS}(\phi) = \int_\Sigma tr(\phi)
  \,.
$$

Degenerate as this situation is, it can be useful to regard the [[trace]] as a Chern-Simons action functional. 

* Arguments for a role in large $N$ gauge theory are in ([Nair 06](#Nair)). 

* The _[[spectral action]]_  is of this form.

### For a group character, on a coadjoint orbit

For $G$ a suitable [[Lie group]] (compact, semi-simple and simply connected) the [[Wilson loops]] of $G$-[[principal connections]] are equivalently the [[partition functions]] of a 1-dimensional Chern-Simons theory.

This appears famously in the formulation of [[Chern-Simons theory]] [with Wilson lines](Chern-Simons+theory#WithWilsonLineObservables). More detailes are at _[[orbit method]]_.

### For a symplectic Lie 0-algebroid

A [[symplectic manifold]] regarded as a [[symplectic Lie n-algebroid]] with $n = 0$ induces a 1d Chern-Simons theory whose [[Chern-Simons form]] is a Liouville form of the symplectic form. 

This case is discussed in ...

## Related concepts

* [[higher dimensional Chern-Simons theory]]

  * **D=1 Chern-Simons theory**

  * [[D=2 Chern-Simons theory]]

  * [[D=3 Chern-Simons theory]]

  * [[D=4 Chern-Simons theory]]

  * [[D=5 Chern-Simons theory]]

  * [[D=6 Chern-Simons theory]]

  * [[D=7 Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

## References

### For the first Chern class

A discussion of 1d CS theory in the context of large $N$-gauge theory is in 

* V.P. Nair, _The Matrix Chern-Simons One-form as a Universal Chern-Simons Theory_ 	Nucl.Phys.B750:289-320,2006 ([arXiv:hep-th/0605007](http://arxiv.org/abs/hep-th/0605007))
  {#Nair}

An exposition of this theory formulated via an [[extended Lagrangian]] in [[higher geometric quantization]] is in section 1 of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_

Further discussion is in section 5.7 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

### For a symplectic Lie 0-algebroid

A 1d Chern-Simons theory with target a [[cotangent bundle]] is discussed in 

* [[Ryan Grady]], [[Owen Gwilliam]], _One-dimensional Chern-Simons theory and the $\hat{A}$ genus_ ([arXiv:1110.3533](http://arxiv.org/abs/1110.3533))
  {#GradyGwilliam}

[[!redirects D=1 Chern-Simons theories]]
[[!redirects 1d Chern-Simons theory]]
[[!redirects 1d Chern-Simons theories]]
[[!redirects 1-dimensional Chern-Simons theory]]
[[!redirects 1-dimensional Chern-Simons theories]]