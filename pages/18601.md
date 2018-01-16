
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

In [[perturbative quantum field theory]] the [[scattering amplitudes]] in the [[S-matrix]] are expressed as [[formal power series]] in (the [[coupling constant]] and) in [[Planck's constant]] $\hbar$. This formal power series may be expressed as a formal sum of contributions labeled by [[Feynman diagrams]]. The _loop order_ refers to something like the "number of loops" of [[edges]] in the [[Feynman diagram]] that contibutes to a given [[scattering amplitude]]. It turns out that the loop order corresponds to the order in $\hbar$ that is contributed by this diagram (see [below](#RelationToPowersInPlancksConstant)). 

Therefore contributions of graphs at zero without loops (these are [[trees]], and hence these contributions are referred to as being at "tree level") correspond to the limit of [[classical field theory]] with $\hbar \to 0$. Indeed tree level Feynman diagrams yield [[perturbation theory|perturbative]] solutions of the [[classical field theory|classical]] [[equations of motion]] (see [Helling](#Helling)).

Most predictions of the [[standard model of particle physics]] have very good agreement with [[experiment]] already to very low loop order, first or second; inclusion of third loop order is used (at least in [[QCD]]) to constrain theoretical uncertainties of the result (see [Cacciari 05, slide 5](#Cacciari05), e.g. in [[Higgs field]] computation, see [ADDHM 15](#ADDHM15)). 
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

This comes about (see at _[S-matrix -- Feynman diagrams](S-matrix#FeynmanDiagrams)_ for details) because 

1. the explicit $\hbar$-dependence of the [[S-matrix]] is 

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

1. the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

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

where $\Delta_F$ denotes the [[Feynman propagator]] and $\mathbf{\Phi}^a(x)$ the [[field observable]] at point $x$.

The resulting terms of the S-matrix series are thus labeled by 

1. the number of factors of the [[interaction]] [[action functional]] $S_{int}$, these are the [[vertices]] of the corresponding Feynman diagram and hence each contribute with $\hbar^{-1}$;

1. the number of integrals over the Feynman propagator $\Delta_F$, which correspond to the [[edges]] of the Feynman diagram, and each contribute with $\hbar^1$.

In summary this means that a Feynman diagram $\Gamma$ contributes at order

$$
  \hbar^{E(\Gamma) - V(\Gamma)}
  \,.
$$

Now if the Feynman diagram happens to be a [[planar graph]], then the formula for the [[Euler characteristic of planar graphs]] says that  the number of regions in the plane that are encircled by edges, the _[[faces]]_, here thought of as the number of "loops" and denoted $L(\Gamma)$, is

$$
  L(\Gamma) \;=\;  1 + E(\Gamma) - V(\Gamma)
  \,.
$$

Hence a planar Feynman diagram $\Gamma$ contributes to the [[Feynman perturbation series]] at order

$$
  \hbar^{L(\Gamma)-1}
  \,.
$$

So far this is the discussion for internal edges. An actual scattering matrix element is of the form

$$
  \langle 
    \mathbf{\Psi}_{out} 
    \vert 
    \mathcal{S}\left( S_{int}\right)
  \vert \mathbf{\Psi}_{in} \rangle
  \,,
$$

where 

$$
  \vert \mathbf{\psi}_{in}\rangle 
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{in}}}} 
  \mathbf{\Phi}^\dagger(k_1)   
     \cdots 
   \mathbf{\Phi}^\dagger(k_{n_{in}}) 
  \vert vac \rangle
$$

is a state of $n_{in}$ free field quanta and similarly

$$
  \vert \mathbf{\Psi}_{out}\rangle 
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{out}}}} 
  \mathbf{\Phi}^\dagger(k_1) \cdots \mathbf{\Phi}^\dagger(k_{n_{out}}) 
  \vert vac \rangle
$$

is a state of $n_{out}$ field quanta. The normalization of these states, in view of the [[Peierls-Poisson bracket]] [[commutator]] $[\mathbf{\Phi}(k), \mathbf{\Phi}(q)] \propto \hbar$, yields the given powers of $\hbar$.

This means that an actual [[scattering amplitude]] given by a [[Feynman diagram]] $\Gamma$ with $E_{ext}(\Gamma)$ external vertices contributes at order

$$
  \hbar^{L(\Gamma) - 1 + E_{ext}(\Gamma)/2 }
  \,.
$$

(For the analogous discussion of the dependence on the actual [[quantum observables]] on $\hbar$ given by [[Bogoliubov's formula]], see [there](Bogoliubov's+formula#PowersInPlancksConstant).)


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

[[!redirects 1-loop]]
[[!redirects 2-loop]]
[[!redirects 3-loop]]

[[!redirects tree level]]
[[!redirects tree levels]]

[[!redirects tree-level]]
[[!redirects tree-levels]]



