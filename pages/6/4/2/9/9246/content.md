
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Effective field theory and renormalization
+--{: .hide}
[[!include renormalization - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]], for a suitable [[free field theory]] to perturb around, given an  [[interaction]] [[Lagrangian density]] then the [[renormalization]] of the corresponding [[Lagrangian field theory]] is in each order $\omega \in \mathbb{Z}$ a choice from an [[affine space]] of renormalization parameters. A _renormalization scheme_ is a way to pick for all interaction Lagrangians at once an origin in these affine spaces, making them [[finite dimensional vector spaces]] relative to this choice.

This means that, given a [[free field theory]] $\mathbf{L}_{kin}$, then a renormalization scheme makes the construction of the [[perturbative S-matrix]] become a [[function]]

$$
  S 
    \;\colon\; 
  LocObs(E)[ [\hbar] ] 
    \longrightarrow 
  PolyObs(E,\mathbf{L}_{kin})_{mc}
$$

which assigns to each [[local observable]] $\mathbf{L}_{int} \in LocObs(E)$, regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[Lagrangian density]], the corresponding perturbative [[scattering matrix]] $S(\mathbf{L}_{int}) \in PolyObs(E,\mathbf{L}_{kin})$ (in the form of an element of the [[Wick algebra]] $(PolyObs(E,\mathbf{L})_{mc}, \star_{H})$) satisfying some conditions (notably [[causal additivity]]).

Concretely, in [[causal perturbation theory]] [[renormalization]] is understood as the choice of [[extension of distributions]] of the [[Feynman amplitudes]] (which are [[products of distributions]], along [[edges]] of [[Feynman diagrams]], of [[Feynman propagators]] with the [[interaction]] [[Lagrangian densities]]) to the [[diagonal]] where the interaction points coincide. For translation-invariant theories this amounts, locally, to [[extension of distributions]] from the [[complement]] $\mathbb{R}^n \setminus \{0\}$ of the origin in some (high-dimensional) [[Cartesian space]] to the full space. For given [[scaling degree of a distribution]] $\omega$, the space of such extensions is an [[affine space]] modeled on the [[finite dimensional vector space]] of [[point-supported distributions]] at the origin of degree $\leq \omega$. 

A choice of such extensions for all distributions at once is naturally fixed by a choice of [[projection]] from the space of all [[bump functions]] on $\mathbb{R}^n$ to the subspace of those all whose [[partial derivatives]] to order $\omega$ vanish at the origin ([Brunetti-Fredenhagen 00, p. 24-25](#BrunettiFredenhagen00), following [Epstein-Glaser 73, p. 27-28 (236-237)](#EpsteinGlaser73)).  

Such a choice hence amounts to a _renormalization scheme_.

The [[main theorem of perturbative renormalization]] states that any two choices of renormalization schemes differ by a unique re-definition of the [[interaction]] [[Lagrangian density]] by an element in the [[Stückelberg-Petermann renormalization group]].


## References

Discussion in [[relativistic field theory]] via [[causal perturbation theory]] is due to 

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], section 5 of _[[The role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 5.2 of _Microlocal analysis and interacting quantum field theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

Review is in 

* [[Frédéric Paugam]], section 20.6 of _Towards the mathematics of quantum field theory_, Springer 2014 ([pdf](https://webusers.imj-prg.fr/~frederic.paugam/documents/enseignement/master-mathematical-physics.pdf))

Discussion in [[Euclidean field theory]] is in

* [[Kevin Costello]], def. 1.4.1, def. 8.0.2 _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))



Further discussion of dependence of quantities on choice of renormalization scheme includes

* _Renormalization scheme dependence_, lecture notes ([pdf](http://bolvan.ph.utexas.edu/~vadim/classes/2012f/ms.pdf))

* Matin Mojaza, Stanley J. Brodsky, Xing-Gang Wu, _A Systematic All-Orders Method to Eliminate Renormalization-Scale and Scheme Ambiguities in PQCD_ ([arXiv:1212.0049](http://arxiv.org/abs/1212.0049))

[[!redirects renormalization schemes]]