
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For various constructions in [[stable homotopy theory]] -- such as notably that of the [[symmetric monoidal smash product of spectra]] -- it is useful to use a model
for objects in the [[stable (∞,1)-category of spectra]]
and the [[stable homotopy category]] more refined than that given by [[sequential spectra]]. The notion of _coordinate-free spectrum_ is such
a refinement.

Where a [[sequential spectrum]] is a collection of [[pointed topological space]] indexed by  the [[natural numbers]] $\mathbb{N}$, a coordinate free spectrum is a collection of [[topological space]]s index by all finite dimensional subspaces of a real inner product [[vector space]] $U$ isomorphic to $\mathbb{R}^\infty$.

Notice that also spectra realized as [[excisive functors]] are coordinate-free in an evident sense, as these are indexed on all [[finite homotopy types]].

In the broader context of [[equivariant stable homotopy theory]] a coordinate-free spectrum may be thought of as the special case of a  [[G-spectrum]] over a [[G-universe]] for the special case of the trivial group $G = 1$.


## Definition

Let $U$ be a real inner product [[vector space]] isomorphic to the [[direct sum]]
$\mathbb{R}^\infty$ of countably many copies of the [[real line]] $\mathbb{R}$.

For $V \subset U$ a finite-dimensional subspace, write $S^V$ for its
[[one-point compactification]] (an $n$-dimensional [[sphere]] if $V$ is $n$-dimensional)
and for $X$ any [[pointed object|based]] [[topological space]] 
write $\Omega^V X := Maps(S^V,X)$ for the [[topological space]] of basepoint-preserving
continuous maps.

For $V \subset W$ an inclusion of finite dimensional subspaces $V,W \subset U$
write $W-V$ for the [[orthogonal complement]] of $V$ in $W$.

+-- {: .num_defn}
###### Definition

A **coordinate-free spectrum** $E$ modeled on the "universe" $U$ is

* for each finite-dimensional subspace $V \subset U$ a [[pointed object|pointed]]
[[topological space]] $E_V$;

* for each inclusion $V \subset W$ of finite dimensional subspaces $V,W \subset U$
a [[homeomorphism]] of pointed [[topological space]]s
  
  $$
    \tilde \sigma_{V,W} : E_V \stackrel{\simeq}{\to} \Omega^{W-V} E_W
    \,.
  $$

* If we drop the requirement that the maps $\tilde \sigma_{V,W}$ be homeomorphisms, we obtain the notion of a **prespectrum**.

=--

+-- {: .num_remark}
###### Remark

The definition of coordinate free spectrum directly generalizes to that of genuine [[G-spectrum]] modeled on a [[G-universe]], leading from [[stable homotopy theory]] to [[equivariant stable homotopy theory]].

=--

## Related concepts

* [[excisive functor]]

* [[functor with smash product]]
  
## References 

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May|P. May]], section 1 of _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ (1995)  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#Kochmann96} [[Stanley Kochmann]], section 3.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996
[[!redirects coordinate-free spectra]]
