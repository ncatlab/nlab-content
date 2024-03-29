
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

Notice here that since $\Omega^k$ denotes the holomorphic forms, this is the [[kernel]] of the [[Dolbeault operator]] $\bar \partial$ and hence the [[de Rham differential]] $\mathbf{d} = \partial + \bar \partial$ restricts to the holomorphic component $\partial$ as above.

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

* [[Hodge-filtered differential cohomology]]

## References

* {#Voisin02} [[Claire Voisin]], section 8.2 of _[[Hodge theory and Complex algebraic geometry]] I,II_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3


* {#Beilinson85} [[Alexander Beilinson]], _Higher regulators and values of L-functions_, J. Soviet Math. 30 (1985), 2036-2070 (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88)) ([doi](http://dx.doi.org/10.1007/BF02105861))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], section 2.5 of: *Deligne-Beilinson cohomology*, in: [[Michael Rapoport]], [[Norbert Schappacher]], [[Peter Schneider]] (eds.), _[[Beilinson's Conjectures on Special Values of L-Functions]]_, Perspectives in Mathematics **4**, Academic Press, Inc. (1988) &lbrack;ISBN:978-0-12-581120-0, [[EsnaultViehweg-DeligneBeilinsonCohomology.pdf:file]]&rbrack;

On holomorphic de Rham cohomology of [[Stein manifolds]] (where it coincides with ordinary [[de Rham cohomology]], see [there](Stein+manifold#HolomorphicDeRhamCoincidesWithDeRhamOnSteinMfds)):

* [[Jean-Pierre Serre]]: *Quelques problemes globaux relatifs aux varietes de Stein*,  Colloque sur les fonctions de plusieurs variables (1953) &lbrack;[doi:10.1007/978-3-642-39816-2_23](https://doi.org/10.1007/978-3-642-39816-2_23)&rbrack;

* {#Serre54} [[Jean-Pierre Serre]]: §2.1 in: *Cohomologie et fonctions de variables complexes*, Séminaire Bourbaki 2 71 (1954) &lbrack;[numdam:SB_1951-1954__2__213_0](http://www.numdam.org/item/SB_1951-1954__2__213_0)&rbrack;



[[!redirects holomorphic de Rham complexes]]

[[!redirects holomorphic de Rham cohomology]]


