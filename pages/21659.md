


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

We define
$$Spin^h(n) = (Spin(n) \times Sp(1))/(\mathbf{Z}/2),$$
in complete analogy to 
$$Spin^c(n) = (Spin(n) \times U(1))/(\mathbf{Z}/2),$$
and
$$Spin(n) = (Spin(n) \times O(1))/(\mathbf{Z}/2).$$

We have a canonical double covering, which is a homomorphism of Lie groups:
$$Spin^h(n) \to SO(n)\times SO(3).$$
It induces canonical homomorphisms of Lie groups
$$Spin^h(n) \to SO(n)$$
and
$$Spin^h(n) \to SO(3).$$

A __spin$^h$-structure__ on a [[principal bundle]] $P\to B SO(n)$
is a lift through the canonical map $B Spin^h(n) \to B SO(n)$.

Thus, in concrete terms, a spin$^h$-structure on $P$ is a principal $SO(3)$-bundle $E$ together with a principal $Spin^h(n)$-bundle $Q$ and a double covering
map $Q\to P\times E$ equivariant with respect to the homomorphism $Spin^h(n) \to SO(n)\times SO(3)$.

The canonical inclusions
$$Spin(n)\to Spin^c(n)\to Spin^h(n)$$
allow promotions of [[spin-structures]] to [[spin^c-structures]] to [[spin^h-structures]].

## Obstructions to existence

The homotopy fiber of $B Spin^h(n) \to B SO(n)$ is not an [[Eilenberg-MacLane space]],
so we cannot expect a single cohomological class to control the existence of spin$^h$-structures.

The first obstruction is the vanishing of the fifth [[integral Stiefel-Whitney class]].

## References

The original definition is due to

* [[Christian Bär]], _Elliptic symbols_.  Mathematische Nachrichten, 201(1), 7–35.

A survey is given in

* Michael Albanese, Aleksandar Milivojevic, _Spin^h and further generalisations of spin_.  [arXiv:2008.04934](https://arxiv.org/abs/2008.04934)