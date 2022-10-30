
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

### Basic definition
 {#BasicDefinition}

The step of [[prequantization]] is about refining data in ([[differential cohomology|differential]]) real [[cohomology]] to ([[differential cohomology|differential]]) [[integral cohomology]]. Often this is understood in terms of the canonical inclusion

$$
  \mathbb{Z} \hookrightarrow \mathbb{R}
$$

of the [[integers]] as an addiditve [[subgroup]] of the [[real numbers]]. But since strictly speaking what appears in [[physics]] is the [[real line]] on which a [[unit]] is chosen as part of the identification of mathematical formalism with physical reality, one should really consider _all_ possible additive group homomorphisms $\mathbb{Z}\to \mathbb{R}$. These are parameterized by 

$$
  h \in (\mathbb{R}- \{0\}) \hookrightarrow \mathbb{R}
$$

$$
  (-)\cdot h \;\colon\; \mathbb{Z} \longrightarrow \mathbb{R}
$$

and this "physical [[unit]]" $h$ is what is called _Planck's constant_. 

In particular the induced [[circle group]] is identified as the [[quotient]] of $\mathbb{R}$ by $h \mathbb{Z}$, in this sense

$$
  U(1) \simeq \mathbb{R}/h \mathbb{Z}
$$

and under this identification its [[quotient]] map is expressed in terms of the [[exponential function]] $\exp \colon z \mapsto  \sum_{k = 0}^\infty \frac{z^k}{k!} \in \mathbb{C}$ as

$$
  \exp(\tfrac{i}{\hbar} (-)) \;\colon\; \mathbb{R} \longrightarrow U(1)
  \,,
$$

where

$$
  \hbar \coloneqq h/2\pi
  \,.
$$

This is the source of the ubiquity of the expression  $\exp(\tfrac{i}{\hbar} (-))$ in [[quantum physics]], say in the [[path integral]], where the exponentiated [[action functional]] appears as $\exp(\tfrac{i}{\hbar} S)$.


### In relation to the symplectic form

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


## As a physical constant 

Planck's constant $h$ is a quantum of action. It may be illustrated in the case of the [[electromagnetic field]] by the fact that each of its [[quanta]] -- a [[photon]] -- carries an [[energy]] $E$ that is fixed by the frequency (cycles per second) $\nu$ according to the relation $E = h\nu$. Thus, the energy emitted by a laser beam of fixed frequency $\nu$ is an integer multiple $n h \nu$ of a packet of energy $h\nu$, where $n$ is the number of photons emitted. 

As a fundamental physical constant, $h$ has dimension $(mass)(length)^2(time)^{-1}$. In meter-kilogram-second (MKS) units, its value is 

$$h \sim 6.62606957 \cdot 10^{-34} m^2 kg / s$$ 

with an uncertainty of up to 29 in the last two digits. 

The reduced Planck constant $\hbar = h/2\pi$ is the proportionality constant that relates energy (of a photon) to angular frequency $\omega$ (radians per second as opposed to cycles per second), so that $E = \hbar \omega$. 


## Related concepts

* [[theory (physics)]]


## References

* {#Donaldson00} [[Simon Donaldson]], _Planck's constant in complex and almost-complex geometry_, XIIIth International Congress on Mathematical Physics (London,
2000), 63&#8211;72, Int. Press, Boston, MA, 2001
 

* Wikipedia, _[Planck's constant](https://en.wikipedia.org/wiki/Planck_constant)_

[[!redirects Planck constant]]
