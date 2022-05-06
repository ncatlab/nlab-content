
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[spin group]] in [[dimension]] 9.

## Properties

### Relation to octonionic Hopf fibration

The [[octonionic Hopf fibration]] is [[equivariant function|equivariant]] with respect to the [[Spin(9)]]-[[action]], the one on $S^8 = S(\mathbb{R}^9)$ induced from the canonical action of $Spin(9)$ on $\mathbb{R}^9$, and on $S^{15} = S(\mathbb{R}^{16})$ induced from the canonical inclusion $Spin(9) \hookrightarrow Spin(16)$.

This equivariance is made fully manifest by realizing the octonionic Hopf fibration as a map of [[coset spaces]] as follows ([Ornea-Parton-Piccinni-Vuletescu 12, p. 7](#OrneaPartonPiccinniVuletescu12)):


$$
  \array{
    S^7 
      &\overset{fib(h_{\mathbb{O}})}{\longrightarrow}& 
    S^{15}
      &\overset{h_{\mathbb{O}}}{\longrightarrow}& 
    S^8
    \\
     = && = && =
    \\
    \frac{Spin(8)}{Spin(7)}
    &\longrightarrow&
    \frac{Spin(9)}{Spin(7)}
    &\longrightarrow&
    \frac{Spin(9)}{Spin(8)}  
  }
$$

### Relation to standard model gauge group

The exact [[gauge group]] of the [[standard model of particle physics]] (see [there](standard+model+of+particle+physics#GaugeGroup)) is [[isomorphism|isomorphic]] to the [[subgroup]] of the [[Jordan algebra]] [[automorphism group]] of the [[octonions|octonionic]] [[Albert algebra]] that "[[stabilizer subgroup|stabilizes]] a 4d sub-[[Minkowski spacetime]]" (see [there](Albert+algebra#StabilizerOf4dMinkowskiInsideOctonionicAlbertAlgebra) for details).

   More concretely, it is identified with the [[subgroup]] of [[Spin(9)]] which respects a splitting $\mathbb{H} \oplus \mathbb{H} \simeq_{\mathbb{R}} \mathbb{C} \oplus \mathbb{C}^3$ ([Krasnov 19](#Krasnov19), see also at [SO(10)-GUT](GUT#TheGUTKnownAsSO10))



## Related concepts

[[!include low dimensional rotation groups -- table]]

\linebreak

## References

* Thomas Friedrich, _Weak Spin(9)-Structures on 16-dimensional Riemannian Manifolds_, ([arXiv:math/9912112](https://arxiv.org/abs/math/9912112))

* Maurizio Parton, Paolo Piccinni, _Spin(9) and almost complex structures on 16-dimensional manifolds_, ([arXiv:1105.5318](https://arxiv.org/abs/1105.5318))

* {#OrneaPartonPiccinniVuletescu12} Liviu Ornea, Maurizio Parton, Paolo Piccinni, Victor Vuletescu, _Spin(9) geometry of the octonionic Hopf fibration_, ([arXiv:1208.0899](http://arxiv.org/abs/1208.0899), [doi:10.1007/s00031-013-9233-x]( https://doi.org/10.1007/s00031-013-9233-x))

* Maurizio Parton, Paolo Piccinni, _The Role of Spin(9) in Octonionic Geometry_, ([arXiv:1810.06288](https://arxiv.org/abs/1810.06288))

* {#Krasnov19} [[Kirill Krasnov]], _$SO(9)$ characterisation of the Standard Model gauge group_ ([arXiv:1912.11282](https://arxiv.org/abs/1912.11282))

[[!redirects Spin9]]

[[!redirects SO(9)]]
[[!redirects SO9]]
