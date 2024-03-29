
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

For $(X,\omega)$ a ([[pre-symplectic form|pre]]-)[[symplectic manifold]] such that $\omega$ is an [[integral form]], a **prequantum line bundle** is any [[line bundle]] $P \to X$ with [[connection on a bundle|connection]] $\nabla$ on $X$ such that 

$$
  \omega = F_\nabla
$$

is the [[curvature]] 2-form of $\nabla$.

=--

+-- {: .num_remark}
###### Remark

Choosing a prequantum line bundle is the first step in the [[geometric quantization]] of $(X, \omega)$.

=--

+-- {: .num_remark}
###### Remark


In [[cohomology]], a choice of prequantum line bundle corresponds to a lift from [[curvature]] 2-forms to [[ordinary differential cohomology]] $H^2(X)_{diff}$ through the [[curvature]] projection

$$
  H^2(X)_{diff} \stackrel{F}{\to} \Omega^2_{int}(X)
  \,.
$$

=--

The above definition has an immediate generalization to [[n-plectic geometry]].

+-- {: .num_defn}
###### Definition

For $(X,\omega)$ an [[n-plectic manifold]] such that $\omega$ is an [[integral form]], a **prequantum circle n- bundle** is any [[circle n-bundle with connection]] $(P \to X, \nabla)$  such that 

$$
  \omega = F_\nabla
$$

is the [[curvature]] $(n+1)$-form of $\nabla$.

=--


+-- {: .num_remark}
###### Remark


In [[cohomology]], a choice of prequantum circle $n$-bundle corresponds to a lift from [[curvature]] $(n+1)$-forms to [[ordinary differential cohomology]] $H^{n+1}(X)_{diff}$ through the [[curvature]] projection

$$
  H^{n+1}(X)_{diff} \stackrel{F}{\to} \Omega^{n+1}_{int}(X)
  \,.
$$

=--

## Related concepts

* [[prequantized Lagrangian correspondence]]

* [[prequantum circle n-bundle]]

* [[local prequantum field theory]]

* [[fiber bundles in physics]]

* [[circle bundle]], [[circle n-bundle with connection]]



[[!include extended prequantum field theory - table]]


* [[geometric quantization]], [[higher geometric quantization]]



## References

Lecture notes with more details are in the section _[Lagrangians and Action functionals](geometry+of+physics#LagrangiansAndActionFunctionals)_ of 

* _[[geometry of physics]]_


Discussion of prequantized (and [[polarization|polarized]]) symplectic manifolds in the context of [[cobordism rings]] and [[Thom spectra]] is in

* {#Morava99} [[Jack Morava]], _Cobordism of symplectic manifolds and asymptotic expansions_, talk at the conference in honor of S.P. Novikov's 60th birthday ([arXiv:9908070](http://arxiv.org/abs/math/9908070))

[[!redirects prequantum line bundles]]

[[!redirects prequantum circle bundle]]
[[!redirects prequantum circle bundles]]

[[!redirects prequantum bundle]]
[[!redirects prequantum bundles]]

[[!redirects pre-quantum line bundle]]
[[!redirects pre-quantum line bundles]]

[[!redirects pre-quantum circle bundle]]
[[!redirects pre-quantum circle bundles]]

[[!redirects pre-quantum bundle]]
[[!redirects pre-quantum bundles]]

[[!redirects prequantization]]
[[!redirects prequantizations]]

[[!redirects pre-quantization]]
[[!redirects pre-quantizations]]

[[!redirects prequantum connection]]
[[!redirects prequantum connections]]
