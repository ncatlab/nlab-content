
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## In geometric quantization
 {#InGeometricQuantization}

In the context of [[geometric quantization]] Planck's constant appears as the inverse scale of the [[symplectic form]]. 

For instance in the simple case that [[phase space]] is $T^* \mathbb{R} \simeq \mathbb{R}^2$ with standard coordinates $\{p,q\}$, then the normalization of the symplectic form $\sim d p \wedge dq$ actually needed in physics is

$$
  \omega = \frac{1}{\hbar} d p \wedge d q
  \,.
$$

This is because after [[geometric quantization]] of this form the [[observables]] will obey

$$
  [\hat q, \hat p] = i (\omega_{p,q})^{-1}
$$

and this is supposed to be

$$
  \cdots = i \hbar
  \,.
$$

Accordingly, it follows that if $(E, \nabla)$ is a [[prequantum line bundle]] for $\omega$, then its $k$-fold [[tensor product]] with itself, for $k \in \mathbb{N}$, is a line bundle $(E^{\otimes k}, \nabla_k)$ with [[curvature]] $k \omega$. By the above this corresponds to rescaling

$$
  \hbar \to \hbar / k
  \,.
$$

This implies in particular

1. a global rescaling of the [[periods]] of the symplectic form may be absorbed in a rescaling of Planck's constant, see at _[[geometric quantization of non-integral forms]]_;

1. for $(E, \nabla)$ a given [[prequantum line bundle]] the limit of the tensor powers $(E^{\otimes k}, \nabla_k)$ as $k$ tends to [[infinity]] roughly corresponds to taking a [[classical limit]]. See also ([Donaldson 00](#Donaldson00)).



### Examples

#### Chern-Simons theory

In [[Chern-Simons theory]] Planck's constant corresponds to the inverse _level_ of the theory, hence the inverse of the [[characteristic class]] that defines the theory, regarded as an element in $\mathbb{Z}$.

Similarly for [[schreiber:infinity-Chern-Simons theory]]. 
For instance ordinary [[spin group]] Chern-Simons theory may be taken to have as the fundamental value $\hbar = 2$, because the [[first Pontryagin class]] that defines the theory is divisible by 2, the [[prequantum circle n-bundle|prequantum 3-bundle]] that defines the theory of the [[moduli stack]] of $Spin$-[[principal connections]] is 

$$
  \tfrac{1}{2}\hat \mathbf{p}_1 : \mathbf{B}Spin_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

Similarly for 7-dimensional [[String 2-group]] [[schreiber:infinity-Chern-Simons theory]] the fundamental value is $\hbar = 6$, with the extended Lagrangian being

$$
  \tfrac{1}{6}\hat \mathbf{p}_2 : \mathbf{B}String_{conn} \to \mathbf{B}^7 U(1)_{conn}
  \,.
$$

See at _[[higher geometric quantization]]_ for more on this.

## Related concepts

* [[theory (physics)]]

## References

* [[Simon Donaldson]], _Planck's constant in complex and almost-complex geometry_, XIIIth International Congress on Mathematical Physics (London,
2000), 63&#8211;72, Int. Press, Boston, MA, 2001
 {#Donaldson00}

[[!redirects Planck constant]]
