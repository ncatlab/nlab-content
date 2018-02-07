

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A central result in the construction of [[perturbative quantum field theories]] via the method of [[causal perturbation theory]] is called the _main theorem of perturbative renormalization theory_. This says that given a suitable [[free field theory|free field]] [[vacuum]] to be [[perturbation theory|perturbed]] ([this def.](S-matrix#VacuumFree)), then any two _[[renormalization schemes]]_ for [[perturbative quantum field theory]] around this free field theory, hence any two solutions $\mathcal{S}$, $\mathcal{S}'$ to the [[induction|inductive]] construction of the [[perturbative S-matrix]] scheme as a [[function]] 

$$
  \mathcal{S}
   \;\colon\; 
  LocObs(E)[ [\hbar , g ] ]\langle g , j\rangle
    \longrightarrow
  PolyObs(E)_{mc}((\hbar))[ [ g, j] ]
$$

from [[local observables]] $g S_{int} + j A$, regarded as [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functionals]], to [[scattering amplitude]] [[Wick algebra]] elements $S\mathcal{S}(\mathbf{L}_{int})$, are related by a unique _perturbative_ transformation 

$$
  \mathcal{Z}
    \;\colon\;
  LocObs(E)[ [\hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  LocObs(E)[ [\hbar, g, j] ]\langle g, j\rangle
$$

of the space of [[local observable|local]] [[interaction]] [[action functionals]] via [[precomposition]]

$$
  \mathcal{S}' 
    \;=\; 
  \mathcal{S} \circ \mathcal{Z}
  \,.
$$


The collection of these operations $\mathcal{Z}$ forms a [[group]], called the _[[Stückelberg-Petermann renormalization group]]_. Hence the space of [[renormalization schemes]] is a [[torsor]] over this group.

The precise nature of this group depends on which set of _[[renormalization conditions]]_ one imposes. The larger this set, the smaller the corresponding [[renormalization group]] ([Dütsch 18, remark 3.102](#Duetsch18)).

Beware the terminology: Contrary to common practice, the construction of a single $\mathcal{S}$ is more properly called a choice of _normalization_ rather a "re"-normalization (e. g. [Scharf 95, section 4.3](causal+perturbation+theoryscatt#Scharf95)), but the "main theorem" above says that the elements in the [[Stückelberg-Petermann renormalization group]] are precisely that: _re_-normalizations, passing from one choice of normalization to another.

## Details


See at _[[renormalization]]_ _[this theorem](renormalization#PerturbativeRenormalizationMainTheorem)_.


## References

The theorem is originally due to 

* G. Popineau, [[Raymond Stora]], _A Pedagogical Remark on the Main Theorem of Perturbative Renormalization Theory, Nucl. Phys. B 912 (2016), 70–78, preprint:
LAPP–TH, Lyon (1982)

In various variants it has been (re-)proved in the following articles:

* G. Pinter, section 6 of _The Action Principle in Epstein Glaser Renormalization and Renormalization of the S-Matrix in $\phi^4$-Theory_, Annalen Phys. 10 (2001) 333-363 ([arXiv:hep-th/9911063](https://arxiv.org/abs/hep-th/9911063))

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], section 4.1 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* [[Michael Dütsch]], [[Klaus Fredenhagen]], section 4.2 of _Causal perturbation theory in terms of retarded products, and a proof of the Action Ward Identity_,  Rev. Math. Phys. 16, 1291 (2004) ([arXiv:hep-th/0403213](https://arxiv.org/abs/hep-th/0403213))

* [[Stefan Hollands]], theorem 2 in _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

Review is in 

* {#Rejzner16} [[Katarzyna Rejzner]], section 6.3 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

* [[Michael Dütsch]], section 3.5.2 of _[[From classical field theory
to perturbative quantum field theory]]_, 2018


[[!redirects main theorem of perturbative renormalization theory]]
