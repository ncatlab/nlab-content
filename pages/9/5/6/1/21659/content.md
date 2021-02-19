


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

With [[Sp(1)]] denoting the [[quaternion unitary group]], 
we define the [[Spin^h group|Spin$^h$ group]]
$$Spin^h(n) = (Spin(n) \times Sp(1))/(\mathbf{Z}/2),$$
in complete analogy to the [[Spin^c group|Spin$^c$ group]]
$$Spin^c(n) = (Spin(n) \times U(1))/(\mathbf{Z}/2),$$
and the [[Spin group]]
$$Spin(n) = (Spin(n) \times O(1))/(\mathbf{Z}/2).$$

We have a canonical [[double covering]], which is a [[homomorphism]] of [[Lie groups]]:
$$Spin^h(n) \to SO(n)\times SO(3).$$
It induces canonical homomorphisms of Lie groups
$$Spin^h(n) \to SO(n)$$
and
$$Spin^h(n) \to SO(3).$$

A __spin$^h$-structure__ on a [[principal bundle]] $P\to B SO(n)$
is a [[lift]] through the canonical map $B Spin^h(n) \to B SO(n)$.

Thus, in concrete terms, a spin$^h$-structure on $P$ is a principal $SO(3)$-bundle $E$ together with a principal $Spin^h(n)$-bundle $Q$ and a double covering
map $Q\to P\times E$ equivariant with respect to the homomorphism $Spin^h(n) \to SO(n)\times SO(3)$.

The canonical inclusions
$$Spin(n)\to Spin^c(n)\to Spin^h(n)$$
allow promotions of [[spin-structures]] to [[spin^c-structures]] to [[spin^h-structures]]. The converse is not true: just as $\mathbb{CP}^2$ is a spin$^c$ manifold with no spin structure, the _Wu manifold_ $SU(3)/SO(3)$ is a spin$^h$ manifold with no spin$^c$ structure ([MathOverflow discussion](https://mathoverflow.net/questions/304471/spin-h-structures)).

## Obstructions to existence

The homotopy fiber of $B Spin^h(n) \to B SO(n)$ is not an [[Eilenberg-MacLane space]],
so we cannot expect a single cohomological class to control the existence of spin$^h$-structures.

The first obstruction is the vanishing of the fifth [[integral Stiefel-Whitney class]].

## In physics

[Freed-Hopkins](#FH16) use spin$^h$ [[invertible field theory|invertible field theories]] to model and classify [[SPT order|SPT phases]] in Altland-Zirnbauer class C.

[Wang-Wen-Witten](#WWW19) study an anomaly in 4d $SU(2)$ gauge theory that can appear when the theory is placed in spin$^h$ manifolds.

## References

The original definition is due to

* [[Christian Bär]], _Elliptic symbols_.  Mathematische Nachrichten, 201(1), 7–35.

A survey is given in

* Michael Albanese, Aleksandar Milivojevic, _Spin^h and further generalisations of spin_.  [arXiv:2008.04934](https://arxiv.org/abs/2008.04934)

Applications in physics:

* {#FH16} [[Dan Freed]] and [[Mike Hopkins]], _Reflection positivity and invertible topological phases_ ([arXiv:1604.06527](https://arxiv.org/abs/1604.06527)).

* {#WWW19} [[Juven Wang]], [[Xiao-Gang Wen]], and [[Edward Witten]], _A New SU(2) Anomaly_, Journal of Mathematical Physics 60, 052301 (2019) ([arXiv:1810.00844](https://arxiv.org/abs/1810.00844)).


[[!redirects spin^h structures]]

[[!redirects spin^h-structure]]
[[!redirects spin^h-structures]]

[[!redirects Spin^h structure]]
[[!redirects Spin^h structures]]

[[!redirects Spin^h-structure]]
[[!redirects Spin^h-structures]]

[[!redirects spin^h]]
[[!redirects Spin^h]]

[[!redirects spin^h group]]
[[!redirects Spin^h group]]

[[!redirects spin^h groups]]
[[!redirects Spin^h groups]]

[[!redirects spin^h-group]]
[[!redirects Spin^h-group]]

[[!redirects spin^h-groups]]
[[!redirects Spin^h-groups]]






