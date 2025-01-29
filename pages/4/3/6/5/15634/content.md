

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


> For disambiguation see at *[[statistics]]*.


\tableofcontents

## Idea

In [[quantum physics]], what is called *particle statistics* refers to the symmetry-properties of [[quantum many-body physics|many-particle]] [[wavefunctions]] under "exchange" of (positions $x_i$ and jointly of all other parameters $p_i$, like [[spin]], of) "indistinguishable" [[particles]].

The term "particle statistics" refers to the fact that the transformation properties of wavefunctions under particle exchange crucially effect the nature of the [[quantum statistical mechanics]] of these particles. 

Or rather, this is the case for the ordinary [[boson|Bose]]/[[fermion|Fermi]]-statistics satisfied by *[[fundamental particles|fundamental]]* particles, namely by [[bosons]] and [[fermions]] respectively (cf. *[[Bose-Einstein condensates]]* as opposed to the *[[Fermi sea]]* due to the *[[Pauli exclusion principle]]*). 

While the richer "para-statistics" and "anyon braid statistics" is often likened to a generalization of Bose/Fermi-statistics, these "exotic statistics" actually arise in practice not as intrinsic symmetries of wavefunctions, but as their "[[Berry phase]]" [[unitary operator|unitary transformations]] under [[quantum adiabatic theorem|adiabatic transport]] along external parameters --- which is conceptually quite different. 

### Boson/Fermion statistics

In the most prominent base case one assumes a single [[quantum state]] represented by a [[wavefunction]] $\Psi\big((x_1, p_1), \cdots (x_N, p_N)\big)$ and asks for its [[group action|transformation]] under a [[permutation]] $\sigma \in$ [[symmetric group|$Sym(N)$]] of its arguments. The particles $(x_i, p_i)$ being indistinguishable means (cf. at *[[quantum symmetry]]*) that the corresponding [[quantum states]] remain [[invariant]], which means that the wavefunction changes at most by multiplication by a [[complex number]] $s(\sigma) \in \mathbb{C}^\times$.

$$
  \Psi\big((x_{\sigma(1)}, p_{\sigma(2)}), \cdots (x_{\sigma(N)}, p_{p(N)})\big)
  \;=\;
  s(\sigma)
  \cdot
  \Psi\big((x_1, p_1), \cdots (x_N, p_N)\big)
  \,.
$$

But the [[symmetric group]] is [[finitely generated group|generated]] by pair exchanges $\sigma_{i j} = (i \leftrightarrow j)$ which all square to the [[neutral element]], $\sigma_{i j} \sigma_{i j} = \mathrm{e}$, whence the same must follow for the phase factor with respect to the complex [[group of units]] $\mathbb{C}^\times$:
$$
  s(\sigma_{i j})^2 \,=\, 1 \,\in\, \mathbb{C}^\times
  \,.
$$

The only two solutions to this [[equation]] are:

* $s(\sigma_{i j}) = +1$ --- in this case the corresponding indistinguishable particles are called *[[bosons]]*,

* $s(\sigma_{i j}) = -1$ --- in this case the corresponding indistinguishable particles are called *[[fermions]]*.

{#BoseFermiAsRepTheory} In [[representation theory|representation theoretic]] words: The [[wavefunctions]] of ordinarily indistinguishable particles must, by definition, [[linear span|span]] **1-[[dimension of a vector space|dimensional]] [[linear representations]] [[representation theory of the symmetric group|of the symmetric group]]** and there are exactly two such, up to [[isomorphism]]:

1. the [[trivial representation]] ([[bosons]]),

1. the [[alternating representation]] ([[fermions]]).


### Para-statistics

More generally, one may ask that the [[symmetric group]] of particle exchanges does not necessarily leave the [[quantum state]] [[invariant]], but [[transformation group|transforms]] it [[group homomorphism|homomorphically]] within a [[linear subspace]] of the [[Hilbert space]] of all states. 

This means to ask for *any* [[linear representation]] [[representation theory of the symmetric group|of the symmetric group]] (not necessarily 1-dimensional as for bosons and fermions [above](#BoseFermiAsRepTheory)).

In this case $s(\sigma)$ is not just a [[complex number]] but a ([[unitary operator|unitary]]) [[linear operator]], and there are many more possibilities for its values.

This generalization of particle statistics is referred to as *[[parastatistics]]*.


### Anyon braid statistics

Still more generally, one may consider the case that the behaviour of the wavefunction depends not just on the [[permutation]] of the particle labels, but also on the "*way*" in which the permutation is accomplished.

Concretely, envisioning the $N$ "particles" to be confined to an effectively 2-[[dimension of a manifold|dimensional]] [[surface]] $\Sigma^2$, and envisioning that the "ways" to permute them are [[isotopy]]-[[equivalence classes|classes]] of [[group of motions|motions]] of $N$ pairwise distinct points in the surface (hence of [[paths]] in the [[configuration space of points]]), then the [[group]] of such exchanges is not just the [[symmetric group]] but the [[braid group]] $Br_N(\Sigma^2)$ which ([[epimorphism|surjects]] onto the [[symmetric group]]) or the [[pure braid group]] $PBr_N(\Sigma^2)$ (which is the [[kernel]] of that surjection):

$$
  1 
  \to
  PBr_N(\Sigma^2)
  \hookrightarrow
  Br_N(\Sigma^2)
  \twoheadrightarrow
  Sym_N
  \to
  1
  \,.
$$

In this situation one may hence ask that the [[quantum states]] of these $N$ "particles" form a [[linear representation]] of the [[braid group]]. 

In this case one speaks of *[[braid statistics]]*.

Even if the [[braid representation]] is 1-dimensional, this is more general than Bose/Fermi-statistics: The (unitary) phase assigned to the motion of a pair of such "particles" past each other may be *any* [[complex number]] of unit [[absolute value]]. For this reason the "particles" satisfying 1-dimensional braid statistics have been called *[[anyons|any-ons]]*.


More in detail, for such 1-dimensional braid representations one speaks of *abelian anyons*, while for higher dimensional braid [[irreps]] one speaks of *non-abelian anyons*.





## Related entries

* [[boson]], [[fermion]] 

* [[spin-statistics theorem]]

* [[braid group statistics]], [[anyon]]

* [[parastatistics]]


## References

### General

See also:

* Wikipedia: *[Particle statistics](https://en.wikipedia.org/wiki/Particle_statistics)*


### Via AQFT

Discussion via [[algebraic quantum field theory]] and in view of [[causal locality]] and [[DHR superselection theory]]:

* [[Sergio Doplicher]], [[Rudolf Haag]], [[John E. Roberts]]: *Local observables and particle statistics I*, Commun.Math. Phys. **23** (1971) 199–230 &lbrack;[doi:10.1007/BF01877742](https://doi.org/10.1007/BF01877742), [euclid:cmp/1103857630](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-23/issue-3/Local-observables-and-particle-statistics-I/cmp/1103857630.full)&rbrack;

* [[Sergio Doplicher]], [[Rudolf Haag]], [[John E. Roberts]]: *Local observables and particle statistics I*, Commun.Math. Phys. **35** (1974) 49–85 &lbrack;[doi:10.1007/BF01646454](https://doi.org/10.1007/BF01646454)&rbrack;

Review and further discussion:

* [[Sergio Doplicher]]: *The statistics of particles in local quantum theories*, in: *International Symposium on Mathematical Problems in Theoretical Physics*, Lecture Notes in Physics **39** (1975) 264-273 &lbrack;[doi:10.1007/BFb0013339](https://doi.org/10.1007/BFb0013339), [inSpire:105411](https://inspirehep.net/literature/105411),  [pdf](https://inspirehep.net/files/a1303bb4c674e0b8271e22aa7b77729d)&rbrack;

* [[Hans Halvorson]]: *Statistics, permutation symmetry, and identical particles*, Section 11.4 in: *Algebraic Quantum Field Theory*, in *Philosophy of Physics*, Handbook of the Philosophy of Science (2007) 731-864 &lbrack;[doi:10.1016/B978-044451560-5/50011-7](https://doi.org/10.1016/B978-044451560-5/50011-7), [arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)&rbrack;



category: physics 