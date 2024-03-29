
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[higher gauge theory]] analog of [[electromagnetism]], including in degree 2 the [[B-field]], in degree 3 the [[supergravity C-field|C-field]], and so on.

## Definition

Over a [[spacetime]] $X$, a field configuration of order $n$ $U(1)$-gauge theory is a [[circle n-bundle with connection]] $\hat F : X \to \mathbf{B}^n U(1)_{conn}$.

The [[action functional]] of the bare theory is given by

$$
  \exp(i S(-)) 
  : 
  \hat F \mapsto \exp(i \int_X   F\wedge \ast F)
  \,,
$$

where $F \in \Omega^{n+1}_{cl}(X)$ is the [[field strength]]/[[curvature]] of $\hat F$, and where $\ast$ denotes the [[Hodge star operator]].

The presence of background [[electric charge]] on $X$ is modeled by a fixed [[circle n-bundle with connection|circle (d-n-1)-bundle with connection]]

$$
  \hat j_{el} : X \to \mathbf{B}^{d-n-1} U(1)_{conn}
  \,,
$$

where $d$ is the [[dimension]] of $X$, and adding to the action the [[higher electric background charge coupling]] term

$$
  \exp(i S_{el}(-)) 
  : 
  \hat F 
    \mapsto 
  \exp(i \int_X \hat F \cup \hat j)
  \,,
$$

given by the [[Beilinson-Deligne cup product]] of the higher electromagnetic field with the background electric current, followed by [[fiber integration in ordinary differential cohomology]].

The presence of background [[magnetic charge]], on the other hand, is modeled by changing the configurations from circle $n$-bundles with connection to _twisted_ circle $n$-bundles with connection (...)

## Examples

* [[electromagnetic field]]

* [[B2-field]]

* [[C3-field]]

* [[B6-field]]

* [[C6-field]]

## Related concepts

* [[self-dual higher gauge theory]]




## References

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_

* [[Dan Freed]], [[Greg Moore]], [[Graeme Segal]], _The uncertainty of fluxes_ 	Commun.Math.Phys.271:247-274 (2007) ([arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198))

* [[Dan Freed]], [[Greg Moore]], [[Graeme Segal]], _Heisenberg Groups and Noncommutative Fluxes_ 	AnnalsPhys.322:236-285 (2007) ([arXiv:hep-th/0605200](http://arxiv.org/abs/hep-th/0605200))

[[!redirects higher U(1)-gauge field]]
[[!redirects higher U(1)-gauge fields]]