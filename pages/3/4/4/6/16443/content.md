
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Tractor bundles are certain [[associated bundles]] considered in
[[conformal geometry]] and more generally in [[parabolic geometry]].

Even more generally, given a [[subgroup]] inclusion $H \hookrightarrow G$ of [[Lie groups]] and given a linear [[representation]] of $G$ on some [[vector space]] $V$, with [[restricted representation]] by $H$, then the operation of forming [[associated bundles]] 

$$
  P \mapsto P \underset{H}{\times} V
$$ 

to $H$-[[principal bundles]] $P$ constitutes a construction of [[natural vector bundles]] on the category of $(H\to G)$-[[Cartan geometries]]. For the case that $H \hookrightarrow G$ is a [[parabolic subgroup]], hence for the case of [[parabolic geometry]], and the case that $P \to X$ is the $H$-[[frame bundle]] of an $(H \to G)$ [[Cartan geometry]] on a manifold $X$, then these [[associated bundles]] $P \underset{H}{\times} V \to X$ are called _tractor bundles_ (e.g [&#268;ap-Sou&#269;ek 07, p. 11](#CapSoucek07)), often denoted 

$$
  V X \to X
  \,.
$$

These tractor bundles carry special [[connection on a bundle|connections]] and as such are called _tractor connections_ ([&#268;ap-Gover 02](#CapGover02)).

Some $G$-representations are special and hence some tractor bundles are singled out (e.g. [&#268;ap-Slov&#225;k 09, 1.5.7](#CapSlovak09)):

* For the case that $V = \mathfrak{g}$ is the [[Lie algebra]] of $G$ equipped with its [[adjoint action]], then

  $$
    \mathcal{A}X \coloneqq P \underset{H}{\times} \mathfrak{g}
  $$

  is called the _adjoint tractor bundle_. A key point is that for [[parabolic geometries]] the Lie algebra structure is retained by this bundle in that $\mathcal{A}X$ is a bundle of [[Lie algebras]], hence its [[space of sections]] $\Gamma(\mathcal{A}X)$ carries a [[Lie bracket]] $\{-,-\}$ which makes each [[fiber]] [[isomorphism|isomorphic]] to $\mathfrak{g}$ not just as a vector space, but as [[Lie algebra]]. In particular therefore for any representation $V$ then the sections of the associated tractor bundle $V X$ carry an [[action]] by sections of $\mathcal{A}X$.

* By the axioms on [[Cartan geometries]] (see also at [[Cartan connection]]) the tractor bundle corresponding to the [[quotient]] $\mathfrak{g}/\mathfrak{h}$ is [[isomorphism|isomorphic]] to the [[tangent bundle]] $T X$. 

* The inclusion $\mathfrak{p}\hookrightarrow \mathfrak{g}$ of the [[Lie algebra]] of the [[parabolic subgroup]] induces a tractor subbundle $P \underset{H}{\times} \mathfrak{p} \hookrightarrow P \underset{H}{\times}\mathfrak{g}$ denoted

  $$
    \mathcal{A}^0 X \hookrightarrow \mathcal{A}X
  $$

  (e.g [&#268;ap-Sou&#269;ek 07, p. 5](#CapSoucek07)). The corresponding [[quotient]] is again the [[tangent bundle]]

  $$
    \mathcal{A}X/\mathcal{A}^0 X = P\underset{H}{\times} \mathfrak{g}/\mathfrak{p} \simeq T X
  $$

  (e.g [&#268;ap-Sou&#269;ek 07, p. 12](#CapSoucek07)). 

* Dually, the tractor bundle associated to $(\mathfrak{g}/\mathfrak{p})^\ast \simeq \mathfrak{p}_+$ is $\mathcal{A}^1 X $ which is [[isomorphism|isomorphic]] to the [[cotangent bundle]] $T^\ast X$.

  $$
    \mathcal{A}^1 X \simeq T^\ast X
    \,.
  $$

* From this one gets that [[differential forms]] with values in the tractor bundle of $V$ are equivalently sections of the tractor bundle given by the [[tensor product]] representation $\wedge^k \mathfrak{p}_+ \otimes V$

  $$
    \Omega^k(X, V X) \simeq \Gamma( P \underset{H}{\times} \wedge^k \mathfrak{p}_+ \otimes V )
    \,.
  $$

* The [[differential]] in the [[Lie algebra homology]] of $\mathfrak{p}_+$ with [[coefficients]] in $V$ is a [[natural transformation]]

  $$
    \wedge^{k+1} \mathfrak{p}_+ \otimes V \longrightarrow \wedge^{k} \mathfrak{p}_+ \otimes V
  $$

  (often called the _Kostant codifferential_ $\partial^\ast$ is this parabolic context) and hence gives homomorphisms of natural bundles

  $$
    \partial^\ast_k \colon \Lambda^{k+1} T^\ast X \otimes_X V X \longrightarrow \Lambda^{k} T^\ast X \otimes_X V X
  $$

  This yields a [[complex]] of bundles whose [[chain homology]] is fiberwise the [[Lie algebra homology]], hence $ker(\partial^\ast)/im(\partial^\ast)$ is the bundle associated to the [[Lie algebra homology]] group of $\mathfrak{p}_+$ regarded as an $H$-representation:

  $$
    ker(\partial^\ast_{k-1})/im(\partial^\ast_k)
    \simeq
    P \underset{H}{\times} H_k(\mathfrak{p}_+, V)
  $$

  (e.g [&#268;ap-Sou&#269;ek 07, p. 17](#CapSoucek07))
  
  For homogeneous Cartan geometries $X = G/H$ this gives a geometric construction  of [[BGG resolutions]] of representations, for general Cartan geometries it gives a curved generalization of that.

## Related concepts

* [[Fefferman-Graham ambient construction]]

## References

* {#CapGover02} [[Andreas Čap]], A. Rod Gover, _Tractor calculi for parabolic geometries_, Trans. Amer. Math. Soc. 354 (2002), 1511&#8211;1548.

* {#CapSoucek07} [[Andreas Čap]], [[Vladimír Souček]], _Curved Casimir operators and the BGG machinery_, SIGMA __3__, 2007, 111 ([arxiv:0708.3180](http://arxiv.org/abs/0708.3180) [doi](http://dx.doi.org/10.3842/SIGMA.2007.111))

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]],  _Parabolic Geometries I -- Background and General Theory_, AMS 2009

* Sean Curry, A. Rod Gover, _An introduction to conformal geometry and tractor calculus, with a view to applications in general relativity_, 2014 ([arXiv:1412.7559](http://arxiv.org/abs/1412.7559))

* Wikipedia, _[Tractor bundle](http://en.wikipedia.org/wiki/Tractor_bundle)_


[[!redirects tractor bundles]]