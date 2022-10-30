
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] _loop order_ refers to something like the "number of loops" in the [[Feynman diagram]] that contibutes to a given [[scattering amplitude]]. The higher the loop order, the smaller the contribution of this [[Feynman diagram]] to the total [[scattering amplitude]], because loop order translates into prefactors by powers of [[Planck's constant]] $\hbar$ (see [below](#RelationToPowersInPlancksConstant)), which is "small". 

Most predictions of the [[standard model of particle physics]] have very good agreement with [[experiment]] already to very low loop order, first or second; inclusion of third loop order is used to constrain theoretical uncertainties of the result (e.g. in [[Higgs field]] computation, see [ADDHM 15](#ADDHM15)). 
In rare cases higher loop orders are used (for instance in the computation of the [[anomalous magnetic moments]] [AHKN 12](#AHKN12), but this is not a scattering experiment).

This usefulness of low loop order is forturnate because

1. the [[S-matrix]] [[formal power series]] for all [[theory (physics)|theories]] of interest has _vanishing_ [[radius of convergence]] ([Dyson 52](perturbation+theory#Dyson52)), hence is at best an [[asymptotic series]] for which the [[sum]] of more than some low order terms is meaningless;

1. the computational effort increases immensely with loop order.

## Relation to powers in Planck's constant
 {#RelationToPowersInPlancksConstant}

In the computation of [[scattering amplitudes]] for [[field (physics)|fields]]/[[particles]] via [[perturbative quantum field theory]] the [[scattering matrix]] ([[Feynman perturbation series]]) is a [[formal power series]] in (the [[coupling constant]] and) [[Planck's constant]] $\hbar$ whose contributions may be labeled by [[Feynman diagrams]]. Each Feynman diagram $\Gamma$ is a finite labeled [[graph]], and the order in $\hbar$ to which this graph contributes is

$$
  \hbar^{ E(\Gamma) - V(\Gamma) }
$$

where 

1. $V(\Gamma) \in \mathbb{N}$ is the number of [[vertices]] of the graph 

1. $E(\Gamma) \in \mathbb{N}$ is the number of [[edges]] in the graph.

This comes about (see at _[S-matrix -- Feynman diagrams and Renormalization](S-matrix#ExistenceAndRenormalization)_ for details) because the explicit $\hbar$-dependence of the [[S-matrix]] is 

$$
  S\left(\tfrac{g}{\hbar} L_{int} \right)
  = 
  \underset{k \in \mathbb{N}}{\sum} \frac{g^n}{\hbar^n n!} T( \underset{k \, \text{factors}}{\underbrace{L_{int} \cdots L_{int}}} )
$$

and because the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

$$
  T(L_{int} L_{int}) = prod \circ \exp\left( \hbar \int \omega_{F}(x,y) \frac{\delta}{\delta \phi(x)} \frac{\delta}{\delta \phi(y)} \otimes \right) ( L_{int} \otimes L_{int} )
  \,,
$$

where $\omega_F$ denotes the [[Feynman propagator]] and $\phi(x)$ the field observable at point $x$ (where we are notationally suppressing the internal degrees of freedom of the fields for simplicity, writing them as [[scalar fields]], because this is all that affects the counting of the $\hbar$ powers). 

The resulting terms of the S-matrix series are thus labeled by 

1. the number of factors of the [[interaction]] $L_{int}$, these are the [[vertices]] of the corresponding Feynman diagram and hence each contibute with $\hbar^{-1}$ 

1. the number of integrals over the Feynman propagator $\omega_F$, which correspond to the edges of the Feynman diagram, and each contribute with $\hbar^1$.

Now the formula for the [[Euler characteristic of planar graphs]] says that the number of regions in a plane that are encircled by edges, the _faces_ here thought of as the number of "loops", is

$$
  L(\Gamma) =  1 + E(\Gamma) - V(\Gamma)
  \,.
$$

Hence a planar Feynman diagram $\Gamma$ contributes with

$$
  \hbar^{L(\Gamma)-1}
  \,.
$$




## References

* {#AHKN12} Tatsumi Aoyama, Masashi Hayakawa, Toichiro Kinoshita, Makiko Nio, _Tenth-Order QED Contribution to the Electron g-2 and an Improved Value of the Fine Structure Constant_, 10.1103/PhysRevLett.109.111807 ([arXiv:1205.5368](#https://arxiv.org/abs/1205.5368))

* {#ADDHM15} Charalampos Anastasiou, Claude Duhr, Falko Dulat, Franz Herzog, Bernhard Mistlberger, _Higgs boson gluon-fusion production in N3LO QCD_, Phys. Rev. Lett. 114, 212001 (2015) ([arXiv:1503.06056](https://arxiv.org/abs/1503.06056))


[[!redirects 1-loop]]
[[!redirects 2-loop]]
[[!redirects 3-loop]]
