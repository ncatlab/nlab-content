
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

On a [[complex analytic space]] $\Sigma$, the _holomorphic de Rham complex_ is the restriction of the [[de Rham complex]] to [[holomorphic differential forms]] $\Omega^p$

$$
  \Omega^\bullet_\Sigma
  \coloneqq
  \left(
  \mathcal{O}_\Sigma \stackrel{\partial}{\longrightarrow} \Omega^1_\Sigma \stackrel{\partial}{\longrightarrow} \Omega^2_\Sigma \longrightarrow \cdots 
  \right)
  \,.
$$

Notice here that since $\Omega^k$ denotes the holomorphic forms, this is the [[kernel]] of the [[Dolbeault operator]] $\par \partial$ and hence the [[de Rham differential]] $\mathbf{d} = \partial + \bar \partial$ restricts to the holomorphic component $\partial$ as above.

Often considered is a version of this with singularities ("logarithmic de Rham complex") where one consideres instead meromorphic differential forms which are holomorphic in the bulk with logarithmic singularities towards compactification boundaries of $X$.

## Properties

### Relation to complex cohomology
 {#RelationToComplexCohomology}

For $\Sigma$ a [[complex manifold]] then the [[ordinary cohomology]] of $\Sigma$
with [[coefficients]] in the [[complex numbers]] is [[natural isomorphism|naturally isomorphic]] to the [[hypercohomology|hyper]]-[[abelian sheaf cohomology]] with coefficients in the holomorphic de Rham complex:

$$
  H^k(\Sigma,\mathbb{C})
  \simeq
  H^k(\Sigma, \Omega_\Sigma^\bullet)
$$

(e.g. [Voisin 02, theorem 8.1](#Voisin02)).

### Filtering and Relation to Hodge filtation

The holomorphic de Rham complex is naturally [[filtered object|filtered]] by degree with the $p$th filtering stage being

$$
  F^p \Omega^\bullet_X
  \coloneqq
  (0 \to \cdots \to \Omega^p_X \stackrel{\partial}{\longrightarrow}
   \Omega^{p+1} \stackrel{\partial}{\longrightarrow} \cdots)
  \,.
$$

Notice that here $\Omega^p$ is still regarded as sitting in degree $-p$, one just replaces by 0 in the holomorphic de Rham complex the groups of differential forms of degree less than $p$.

With this, the _[[Hodge filtration]]_ on $H^\bullet(X,\mathbb{C})$ is defined to be the [[filtration]] with $p$th stage the [[image]] of the [[hypercohomology|hyper]]-[[abelian sheaf cohomology]] with coefficients in the $p$th filtering stage of the holomorphic de Rham complex inside that with coefficients the full de Rham complex:

$$
  F^p H^k(X,\mathbb{C})
  \coloneqq
  im
  \left(
    H^k(X, F^p \Omega^\bullet_X)
    \to 
    H^k(X, \Omega^\bullet_X)
  \right)
$$

(e.g. [Voisin 02, def. 8.2](#Voisin02)).

If $X$ happens to be a [[Kähler manifold]] then the [[Frölicher spectral sequence]]  shows that this coincides with the more traditional definition via [[harmonic differential forms]] (e.g. [Voisin 02, remark 8.29](#Voisin02)).


## Related concepts

* [[differential form with logarithmic singularities]]

* [[Dolbeault cohomology]]

* [[Hodge filtration]]

* [[Hodge cohomology]]

## References

* {#Voisin02} [[Claire Voisin]], section 8.2 of _[[Hodge theory and Complex algebraic geometry]] I,II_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3


* {#Beilinson85} [[Alexander Beilinson]], _Higher regulators and values of L-functions_, J. Soviet Math. 30 (1985), 2036-2070 (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], section 2.5 of _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

