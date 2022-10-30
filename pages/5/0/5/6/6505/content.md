
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

# The moment map
* table of contents
{: toc}

## Idea

A _moment map_ is a dual incarnation of a [[Hamiltonian action]] of a [[Lie group]] (or [[Lie algebra]]) on a [[symplectic manifold]].

An [[action]] of a [[Lie group]] $G$ on a [[symplectic manifold]] $X$ by ([[Hamiltonian symplectomorphisms|Hamiltonian]]) [[symplectomorphisms]] corresponds [[infinitesimal space|infinitesimally]] to a Lie algebra [[homomorphism]] from the [[Lie algebra]] $\mathfrak{g}$ to the [[Hamiltonian vector fields]] on $X$. If this lifts to a coherent choice of [[Hamiltonians]], hence to a Lie algebra homomorphism $\mathfrak{g} \to (C^\infty(X), \{-,-\})$ to the [[Poisson bracket]], then, by [[dual vector space|dualization]], this is equivalently a Poisson homomorphism 

$$
  \mu : X \to \mathfrak{g}^*
  \,.
$$

This is called the _moment map_ or _momentum map_ of the Hamiltonian action.

The name derives from the special and historically first case of [[angular momentum]] in the [[rigid body dynamics|dynamics of rigid bodies]], see _[Examples - Angular momentum](#AngularMomentum)_ below.


## Definition

The [Preliminaries](#Preliminaries) below review some basics of [[Hamiltonian vector fields]]. The definition of the moment map itself is below in _[Hamiltonian action and the moment map](#HamiltonianActionAndTheMomentMap)_.

### Preliminaries
 {#Preliminaries}

This section briefly reviews the notion of [[Hamiltonian vector fields]] on a [[symplectic manifold]]

The basic setup is the following: Let $(M,\omega)$ be a [[symplectic manifold]] with a [[Hamiltonian action]] of a [[Lie group]] $G$. In particular that means that there is an [[action]] $\nu\colon G \times M \to M$ via [[symplectomorphism]]s (diffeomorphisms $\nu_g$ such that $\nu_g^*(\omega) = \omega$). A vector field $X$ is [[symplectic vector field|symplectic]] if the corresponding flow preserves (again by pullbacks) $\omega$. The symplectic vector fields form a Lie subalgebra $\chi(M,\omega)$ of the Lie algebra of all smooth vector fields $\chi(M)$ on $M$ with respect to the Lie bracket. 

By the [[Cartan homotopy formula]] and closedness $d \omega = 0$

$$
\mathcal{L}_X \omega = d \iota_X \omega
$$

where $\mathcal{L}_X$ denotes the [[Lie derivative]]. Therefore a vector field $X$ is symplectic iff $\iota(X)\omega = d H$ for some function $H\in C^\infty(M)$, usually called Hamiltonian (function) for $X$. Here $X$ is determined by $H$ up to a locally constant function. Such $X = X_H$ is called the __Hamiltonian vector field__ corresponding to $H$.  The Poisson structure on $M$ is the bracket $\{,\}$ on functions may be given by 

$$
\{ f, g\} := [X_f,X_g]
$$

where there is a Lie bracket of vector fields on the right hand side.

There is an exact sequence

$$
0 \to \mathbf{R}\to C^\infty(M)\to \chi(M,\omega)
$$

and $H^1(M, \mathbf{R})$ measures how far is the right-most map from the identity. Thus there is a possible difference between the set of symplectic vector fields and of Hamiltonian vector fields only if the manifold is not simply connected. 

### Hamiltonian action and moment map
 {#HamiltonianActionAndTheMomentMap}

__Hamiltonian action__ above means that the action induced at the level of Lie algebra is by Hamiltonian vector fields with specified [[Hamiltonian]]. That means that the infinitesimal action from $\mathfrak{g}\to \chi(M,\omega)$ lifts to a linear map

$$
\mathfrak{g}\to C^\infty(M); \,\,\,\,\,A\mapsto \mu_A
$$ 

One usually dualizes that map. The __moment map__

$$\mu: M\to \mathfrak{g}^*$$

is determined by the formula 

$$
\langle \mu(z),A\rangle = \mu_A(z),\,\,\,\,\,\,\forall z\in M.
$$

## Examples

### Angular moment
 {#AngularMomentum}

(...)


## Related concepts

The moment map is a crucial ingredient in the construction of Marsden--Weinstein [[symplectic quotients]].




## References

Lecture notes and surveys include

* [[Joel W. Robbin]], _The moment map_, an exposition, [pdf](http://www.math.wisc.edu/~robbin/moment.pdf)

* [[Nicole Berline]], [[Michèle Vergne]], _Hamiltonian manifolds and moment maps_ ([pdf](http://www.math.polytechnique.fr/~berline/cours-Fudan.pdf))

Original articles include

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Geometric asymptotics_, AMS (1977) ([online](http://www.ams.org/online_bks/surv14))

* [[Michael Atiyah]], _Convexity and commuting Hamiltonians_, Bull. London
Math. Soc. __14__ (1982), 1-15.

* [[Michael Atiyah]], [[R. Bott]], _The moment map and equivariant cohomology_, Topology __23__, 1, 1-28 (1984)

Further developments are in

* M. Spera, _On a generalized uncertainty principle, [[coherent state]]s and the moment map_, J. of Geometry and Physics __12__ (1993) 165-182, [MR94m:58097](http://www.ams.org/mathscinet-getitem?mr=1237511), <a href="http://dx.doi.org/10.1016/0393-0440(93)90032-A">doi</a>


* Ctirad Klim&#269;&#237;k, [[Pavol Ševera]], _[[T-duality]] and the moment map_, IHES/P/96/70, [hep-th/9610198](http://arxiv.org/abs/hep-th/9610198); _Poisson-Lie T-duality: open strings and D-branes_, CERN-TH/95-339. Phys.Lett. B376 (1996) 82-89, [hep-th/9512124](http://arxiv.org/abs/hep-th/9512124)

* A. Cannas da Silva, [[Alan Weinstein]], _Geometric models for noncommutative algebras_, Berkeley Math. Lec. Notes Series, AMS 1999, ([pdf](http://math.berkeley.edu/%7Ealanw/Models.pdf))

* Friedrich Knop, _Automorphisms of multiplicity free Hamiltonian manifolds_, [arxiv/1002.4256](http://arxiv.org/abs/1002.4256)

* W. Crawley-Boevey, _Geometry of the moment map for representations of
quivers_, Compositio Math. __126__ (2001), no. 3, 257-293.


See also

* wikipedia, _[moment map](http://en.wikipedia.org/wiki/Moment_map)_


[[!redirects moment map]]
[[!redirects moment maps]]
