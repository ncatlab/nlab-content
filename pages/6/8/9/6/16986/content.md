+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

_Under construction_

#Contents#
* table of contents
{:toc}

## Idea

The _octonionic Hopf fibration_ is the [[fibration]]


$$
  \array{
     S^7 &\hookrightarrow& S^15
     \\
     && \downarrow^{\mathrlap{p_{\mathbb{O}}}}
     \\
     && S^8
  }
$$

of the [[15-sphere]] over the [[8-sphere]] with [[fiber]] the [[7-sphere]]. This may be derived by the [[Hopf construction]] on the [[7-sphere]] $S^7$ with its [[Moufang loop]] structure.

Alternatively, we may construct a fibration by first decomposing $\mathbb{O}^2$ into the octonionic lines, 

$l_m \coloneqq \{(x, m x)|x \in \mathbb{O}\}$ and $l_{\infty} := \{(0, y)|y \in \mathbb{O}\}$. 

In this way the fibration $\mathbb{O}^2 \setminus (0, 0) \to S^8 = \{m \in \mathbb{O}\} \union \{\infty\}$ is obtained, with fibers $\mathbb{O} \setminus 0$, and the intersection with the [[unit sphere]] $S^{15} \subset \mathbb{O}^2$ provides the octonionic Hopf fibration (see [OPPV 12, p. 7](#OrneaPartonPiccinniVuletescu12)).

This second construction yields the standard parameterization of the octonionic Hopf fibration via $(x,y) \mapsto x y^{-1}$ (in one chart) and $(x,y ) \mapsto x^{-1} y$ (in the other), while the Hopf construction gives $(x,y) \mapsto x y$. The latter yields the generator $-1$ of $\pi_{15}(S^8) \cong \mathbb{Z}$, while the former yields $+1$. 

## Properties
 
### $G_2$- and $Spin(9)$-equivariance

The [[automorphism group]] [[G2]] of the [[octonions]], as a [[normed algebra]], manifestly acts on the octonionic Hopf fibration, such that the latter is [[equivariant function|equivariant]].

(see also [Cook-Crabb 93](#CookCrabb93))


But the octonionic Hopf fibration is [[equivariant function|equivariant]] even with respect to the [[Spin(9)]]-[[action]], the one on $S^8 = S(\mathbb{R}^9)$ induced from the canonical action of $Spin(9)$ on $\mathbb{R}^9$, and on $S^{15} = S(\mathbb{R}^{16})$ induced from the canonical inclusion $Spin(9) \hookrightarrow Spin(16)$.

([Gluck-Warner-Ziller 86, Prop. 7.1](#GluckWarnerZiller86))

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

### Subfibrations

*  The complex and quaternionic Hopf fibrations are not subfibrations of the octonionic one ([Parton &amp; Piccinni 18, p. 4](#PartonPiccinni18)).

* The octonionic Hopf fibration does not admit any $S^1$ [[subfibration]] ([Parton &amp; Piccinni 18, p. 13](#PartonPiccinni18)).


## Related concepts

* [[real Hopf fibration]], [[complex Hopf fibration]], [[quaternionic Hopf fibration]]

* [[octonionic projective space]]

## References

* {#GluckWarnerZiller86} [[Herman Gluck]], [[Frank Warner]], [[Wolfgang Ziller]], _The geometry of the Hopf fibrations_, L'Enseignement Math&eacute;matique, t.32 (1986), p. 173-198

* {#OrneaPartonPiccinniVuletescu12} Liviu Ornea, Maurizio Parton, [[Paolo Piccinni]], Victor Vuletescu, _Spin(9) geometry of the octonionic Hopf fibration_, Transformation Groups (2013) 18: 845 ([arXiv:1208.0899](http://arxiv.org/abs/1208.0899), [doi:10.1007/s00031-013-9233-x]( https://doi.org/10.1007/s00031-013-9233-x))

* {#PartonPiccinni18} Maurizio Parton, [[Paolo Piccinni]], _The Role of Spin(9) in Octonionic Geometry_, ([arXiv:1810.06288](https://arxiv.org/abs/1810.06288)).

* {#Miyaoka93} [[Reiko Miyaoka]], _The linear isotropy group of $G_2/SO(4)$, the Hopf fibering and isoparametric hypersurfaces_, Osaka J. Math. Volume 30, Number 2 (1993), 179-202. ([Euclid](http://projecteuclid.org/euclid.ojm/1200784357))

Discussion in [[parameterized homotopy theory]] is in

* {#CookCrabb93} A. L. Cook, M.C. Crabb, _Fiberwise Hopf structures on sphere bundles_, J. London Math. Soc. (2) 48 (1993) 365-384 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/crabbcook.pdf))

* {#Iriye95} [[Kouyemon Iriye]], _Equivariant Hopf structures on a sphere_, J. Math. Kyoto Univ. Volume 35, Number 3 (1995), 403-412 ([Euclid](http://projecteuclid.org/euclid.kjm/1250518704))

