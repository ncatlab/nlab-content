

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]], _differential renormalization_ ([Freedman-Johnson-Latorre 92](#FreedmanJohnsonLatorre92)) is a method of _[[renormalization|("re"-)normalization]]_ which makes choices for defining [[time-ordered products]]/[[Feynman amplitudes]] at coincident interaction [[vertices]].

Differential normalization follows directly ([Prange 97](#Prange97)) from [[Epstein-Glaser renormalization]] in the guise of [[extensions of distributions]] of [[time-ordered products]]/[[Feynman amplitude]] to coinciding interaction points 
([this prop.](renormalization#RenormalizationIsInductivelyExtensionToDiagonal)):

In the proof of that construction ([this prop](renormalization#SpaceOfPointExtensions)) over [[Minkowski spacetime]] $\mathbb{R}^{p,1}$, a choice of [[renormalization|("re"-)normalization]] is embodied at each order $k \in \mathbb{N}$ (number of [[vertices]] in [[Feynman diagrams]]) by a choice of projection operator

$$
  p_{\rho_k}
   \;\colon\;
  \mathcal{D}(\mathbb{R}^{(p+1)(k-1)})
    \longrightarrow
  \mathcal{D}_{\rho_k}(\mathbb{R}^{(p+1)(k-1)})
$$

([this equation](renormalization#eq:ForExtensionOfDistributionsProjectionMaps)) from all test functions to those that vanish to order $\rho_k$ at the origin. (This projction is often denoted "$W$", see [this remark](renormalization#WExtensions)).

Restricted to the image of this projector the relevant [[time-ordered product]] $T_k$ has a _unique_ [[extension of distributions]] to the origin, and this defines the [[renormalization|("re"-)normalization]].

This defines a new [[distribution]] $T_{k,R}$ by

$$
  \left\langle T_{k,R}, b \right\rangle
  \;\coloneqq\;
  \left\langle T_k, p_{\rho_k}(b)\right\rangle
  \,.
$$

Differential renormalization focuses on manipulating theses expressions $T_{k,R}$ ([Prange 97, section 1.1](#Prange97)).




## References

The concept is due to

* {#FreedmanJohnsonLatorre92} D. Z. Freedman, K. Johnson, J. I. Latorre, _Differential regularization and renormalization: a new method of calculation in quantum field theory_, Nucl. Phys. B 371 (1992) 353-414

* J. I. Latorre, X. Vilasis-Cardona, _Systematic Differential Renormalization to All Orders_, Ann. Phys. (N.Y.) 231 (1994) 149

Discussion in [[causal perturbation theory]]/relation to [[Epstein-Glaser renormalization]] is due to 

* {#Prange97} Dirk Prange, _Epstein-Glaser renormalization and differential renormalization_, J. Phys. A 32, 2225 (1999) ([arXiv:hep-th/9710225](http://xxx.lanl.gov/abs/hep-th/9710225))

* [[Jose Gracia-Bondia]], _Differential renormalization and Epstein-Glaser renormalization_, Mod. Phys. Lett. A, 16, 281 (2001).  ([spire](http://inspirehep.net/record/557491/))

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _Causal perturbation theory in terms of retarded products, and a proof of the Action Ward Identity_, Reviews in Mathematical Physics, Volume 16, Issue 10, November 2004 ([arXiv:hep-th/0403213](https://arxiv.org/abs/hep-th/0403213))

* [[Michael Dütsch]], [[Klaus Fredenhagen]], Kai Johannes Keller, [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy. 55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))

* [[José Gracia-Bondía]], Heidy Gutiérrez, Joseph C. Várilly, _Improved Epstein-Glaser renormalization in $x$-space versus differential renormalization_, Nuclear Physics B 886 (2014), 824-869 ([arXiv:1403.1785](https://arxiv.org/abs/1403.1785))

Discussion of application to [[anomalous magnetic moment]] and [[supergravity]]:

* F. del Aguila, A. Culatti, R. Munoz-Tapia, M. Perez-Victoria, _Supergravity corrections to $(g-2)_l$ in differential renormalization_, Nuclear Physics  B  504  (1997)  532-550 ([arXiv:hep-ph/9702342](https://arxiv.org/abs/hep-ph/9702342))

