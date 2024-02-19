
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] the [[scattering amplitudes]] in the [[S-matrix]] are expressed as [[formal power series]] in (the [[coupling constant]] and) in [[Planck's constant]] $\hbar$. This formal power series may be expressed as a formal sum of contributions labeled by [[Feynman diagrams]]. The _loop order_ refers to something like the "number of loops" of [[edges]] in the [[Feynman diagram]] that contibutes to a given [[scattering amplitude]]. It turns out that the loop order corresponds to the order in $\hbar$ that is contributed by this diagram (see [below](#RelationToPowersInPlancksConstant)). 

Therefore contributions of graphs at zero without loops (these are [[trees]], and hence these contributions are referred to as being at "tree level") correspond to the limit of [[classical field theory]] with $\hbar \to 0$. Indeed tree level Feynman diagrams yield [[perturbation theory|perturbative]] solutions of the [[classical field theory|classical]] [[equations of motion]] (see [Helling](#Helling)).

Most predictions of the [[standard model of particle physics]] have very good agreement with [[experiment]] already to very low loop order, first or second; inclusion of third loop order is used (at least in [[QCD]]) to constrain theoretical uncertainties of the result (see [Cacciari 05, slide 5](#Cacciari05), e.g. in [[Higgs field]] computation, see [ADDHM 15](#ADDHM15)). 
In rare cases higher loop orders are used (for instance in the computation of the [[anomalous magnetic moments]] [AHKN 12](#AHKN12), but this is not a scattering experiment).

This usefulness of low loop order is fortunate because

1. the [[S-matrix]] [[formal power series]] for all [[theory (physics)|theories]] of interest has _vanishing_ [[radius of convergence]] ([Dyson 52](perturbation+theory#Dyson52)), hence is at best an [[asymptotic series]] for which the [[sum]] of more than some low order terms is meaningless;

1. the computational effort increases immensely with loop order.

## Relation to powers in Planck's constant
 {#RelationToPowersInPlancksConstant}

The following is taken from _[[geometry of physics -- A first idea of quantum field theory]]_. See there for more background.

+-- {: .num_prop #FeynmanDiagramLoopOrder}
###### Proposition
**([[loop order]] and [[tree level]] of [[Feynman perturbation series]])**

The [[effective action]] ([this def.](A+first+idea+of+quantum+field+theory#InPerturbationTheoryActionEffective)) contains no negative powers of [[Planck's constant]] $\hbar$, hence is indeed
a [[formal power series]] also in $\hbar$:

$$
  S_{eff}(g,j)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
  \,.
$$

and in particular

$$
  \left\langle
    S_{eff}(g,j)
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g, j] ]
  \,.
$$

Moreover, the contribution to the effective action in the [[classical limit]] $\hbar \to 0$
is precisely that of [[Feynman amplitudes]] of those [[finite multigraphs]] ([this prop.](A+first+idea+of+quantum+field+theory#FeynmanPerturbationSeriesAwayFromCoincidingPoints)) which are [[trees]] ([this def.](A+first+idea+of+quantum+field+theory#GraphPlanar)); thus called the _[[tree level]]_-contribution:

$$
  S_{eff}(g,j)\vert_{\hbar = 0}
  \;=\;
  i \hbar
  \underset{\Gamma \in \mathcal{G}_{conn} \cap \mathcal{G}_{tree}}{\sum}
  \Gamma\left( (g S_{int} + j A)_{i = 1}^{\nu(\Gamma)} \right)
  \,.
$$

Finally, a [[finite multigraph]] $\Gamma$ ([this def.](A+first+idea+of+quantum+field+theory#Graphs)) which is [[planar graph|planar]] and [[connected graph|connected]] contributes to the effective action precisely at order

$$
  \hbar^{L(\Gamma)}
  \,,
$$

where $L(\Gamma) \in \mathbb{N}$ is the number of _[[faces]]_ of $\Gamma$, here called the _number of loops_ of the diagram;
here usually called the _[[loop order]]_ of $\Gamma$.

(Beware the terminology clash with [[graph theory]], see the discussion of [[tadpoles]] [here](A+first+idea+of+quantum+field+theory#Tadpoles))

=--

+-- {: .proof}
###### Proof


By [this def.](A+first+idea+of+quantum+field+theory#LagrangianFieldTheoryPerturbativeScattering) the explicit $\hbar$-dependence of the [[S-matrix]] is

$$
  \mathcal{S}
  \left(
    S_{int}
  \right)
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
    \frac{1}{k!}
    \frac{1}{(i \hbar)^k}
    T( \underset{k \, \text{factors}}{\underbrace{S_{int}, \cdots,  S_{int}}} )
$$

and by [this prop.](A+first+idea+of+quantum+field+theory#TimeOrderedProductAwayFromDiagonal) the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

$$
  T(S_{int}, S_{int})
  \;=\;
  prod \circ
  \exp\left(
    \hbar
    \left\langle
      \Delta_F,
      \frac{\delta}{\delta \mathbf{\Phi}}
        \otimes
      \frac{\delta}{\delta \mathbf{\Phi}}
    \right\rangle
  \right)
 ( S_{int} \otimes S_{int} )
  \,,
$$

By the [[Feynman rules]] ([this prop.](A+first+idea+of+quantum+field+theory#FeynmanPerturbationSeriesAwayFromCoincidingPoints)) this means that

1. each [[vertex]] of a Feynman diagram contributes a power $\hbar^{-1}$ to its Feynman amplitude;

1. each [[edge]] of a Feynman diagram contributes a power $\hbar^{+1}$ to its Feynman amplitude.

If we write

$$
  E(\Gamma), V(\Gamma) \;\in\; \mathbb{N}
$$

for the total number of [[vertices]] and [[edges]], respectively, in $\Gamma$, this means that a Feynman amplitude
corresponding to some $\Gamma \in \mathcal{G}$ contributes precisely at order

$$
  \label{GeneralFeynmanDiagramhbarContribution}
  \hbar^{E(\Gamma) - V(\Gamma)}
  \,.
$$

So far this holds for arbitrary $\Gamma$. If however $\Gamma$ is [[connected graph|connected]] and [[planar graph|planar]], then _[[Euler's formula]]_ asserts that

$$
  \label{ConnectedPlanarGraphEulerCharacteristic}
  E(\Gamma) - V(\Gamma)
  \;=\;
  L(\Gamma) - 1
  \,.
$$

Hence $\hbar^{L(\Gamma)- 1}$ is the order of $\hbar$ at which $\Gamma$ contributes to the [[scattering matrix]] expressed as the [[Feynman perturbation series]].

But the [[effective action]], by definition ([this equation](A+first+idea+of+quantum+field+theory#eq:ExpansionEffectiveAction)), has the same contributions
of Feynman amplitudes, but multiplied by another power of $\hbar^1$, hence it contributes at order

$$
  \hbar^{E(\Gamma) - V(\Gamma) + 1} = \hbar^{L(\Gamma)}
  \,.
$$

This proves the second claim on [[loop order]].

The first claim, due to the extra factor of $\hbar$ in the definition of the effective action, is equivalent to saying
that the Feynman amplitude of every [[connected graph|connected]] [[finite multigraph]]
contributes powers in $\hbar$ of order $\geq -1$ and contributes at order $\hbar^{-1}$ precisely if the graph is a tree.

Observe that a [[connected graph|connected]] [[finite multigraph]] $\Gamma$ with $\nu \in \mathbb{N}$ vertices (necessarily $\nu \geq 1$) has at least $\nu-1$ edges and precisely $\nu - 1$ edges if it is a tree.

To see this, consecutively remove edges from $\Gamma$ as long as possible while retaining connectivity. When this process stops, the result must be a connected tree $\Gamma'$, hence a [[connected graph|connected]] [[planar graph]] with $L(\Gamma') = 0$. Therefore [[Euler's formula]] (eq:ConnectedPlanarGraphEulerCharacteristic) implies that that $E(\Gamma') = V(\Gamma') -1$.

This means that the connected multigraph $\Gamma$ in general has a Feynman amplitude of order

$$
  \hbar^{E(\Gamma) - V(\Gamma)}
  =
  \hbar^{ \overset{\geq 0}{\overbrace{E(\Gamma) - E(\Gamma')}} + \overset{= -1}{\overbrace{E(\Gamma') - V(\Gamma)}}  }
$$

and precisely if it is a tree its Feynman amplitude is of order $\hbar^{-1}$.

=--


## Related concepts

* [[radiative correction]]


## References

General discussion includes

* {#BrodskyHoyer10} Stanley J. Brodsky, Paul Hoyer, _The $\hbar$-Expansion in Quantum Field Theory_, Phys.Rev.D83:045026, 2011 ([arXiv:1009.2313](https://arxiv.org/abs/1009.2313))

Discussion of tree level Feynman diagrams as perturbative solutions in [[classical field theory]] is in 

* {#Helling} Robert Helling, _Solving classical field equations_ ([pdf](http://homepages.physik.uni-muenchen.de/~helling/classical_fields.pdf))


Discussion of loop orders of relevance in comparison to [[experiment]] cited above includes for instance the following

* {#Cacciari05} Matteo Cacciari, _(Theoretical) review of heavy quark production_, BNL 14/12/2005 ([pdf](https://www.phenix.bnl.gov/WWW/publish/xiewei/RBRC_Workshop_Dec/heavyworkshop/cacciari.pdf))

* {#AHKN12} Tatsumi Aoyama, Masashi Hayakawa, Toichiro Kinoshita, Makiko Nio, _Tenth-Order QED Contribution to the Electron g-2 and an Improved Value of the Fine Structure Constant_, 10.1103/PhysRevLett.109.111807 ([arXiv:1205.5368](#https://arxiv.org/abs/1205.5368))

* {#ADDHM15} Charalampos Anastasiou, Claude Duhr, Falko Dulat, Franz Herzog, Bernhard Mistlberger, _Higgs boson gluon-fusion production in N3LO QCD_, Phys. Rev. Lett. 114, 212001 (2015) ([arXiv:1503.06056](https://arxiv.org/abs/1503.06056))


[[!redirects loop orders]]

[[!redirects tree level]]
[[!redirects tree levels]]

[[!redirects tree-level]]
[[!redirects tree-levels]]

[[!redirects 1-loop]]
[[!redirects 2-loop]]
[[!redirects 3-loop]]
[[!redirects 4-loop]]

[[!redirects one-loop]]
[[!redirects two-loop]]
[[!redirects three-loop]]
[[!redirects four-loop]]




