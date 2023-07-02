
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _light-cone gauge quantization_ is one approach to the [[quantization]] of [[sigma models]] whose [[target space]] has a [[lightlike]] [[Killing vector]]. The strategy of this approach is to [[gauge fixing|gauge fix]] the [[metric]] and [[diffeomorphisms]] of the [[worldvolume]] such that also the worldvolume has a [[lightlike]] [[Killing vector field]] and such that this is mapped to the given one on target space.

This typically fixes most of the available gauge freedom, and the strategy is then to apply [[quantization]] to what remains. For more on this general idea see at _[[quantization commutes with reduction]]_.

Often this is considered for [[target space]] being [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ and with $X^+ \coloneqq X^0 - X^1$ denoting one of its canonical lightlike [[coordinates]]. If $\tau$ denotes similarly a lightlike coordinate function on the [[worldvolume]], then the condition of light-cone gauge reads

$$
  X^+ = p^+ \tau
$$

for some proportionality constant $p^+$, the *light cone momentum*.  This is how light cone gauge appears in much of the physics literature.

If in addition, one assumes that the coordinate function $X^+$ on spacetime is periodic, hence that it actually runs along a [[circle]] [[fiber]] (which some authors take to be literally [[lightlike]], while others consider the [[limit of a sequence|limit]] of [[boosts]] of a [[spacelike]] [[circle]] [[fiber]]), then the lightcone momentum $p^+$ becomes quantized in units of the inverse [[radius]] $R$ of this circle

\[
  \label{LightConeMomentumQuantization}
  p^+ \;=\; N/R
  \phantom{AAA}
  N \in \mathbb{Z}
  \,.
\]

The [[quantization]] of a [[sigma model]] in this situation is hence called the _discrete light cone quantization_ or _DLCQ_, for short.

Often it turns out that [[negative number|negative]] values of $N$ in (eq:LightConeMomentumQuantization) can be neglected or integrated out, so that 

$$
  N \in \mathbb{N}
$$

becomes a [[natural number]]-parameter akin to that considered in the [['t Hooft double line construction]] of [[gauge theories]], and then the [[large N limit]] of the discrete light cone quantization becomes of interest.


## Applications

### Quantization of Green-Schwarz super $p$-brane sigma models

Light cone gauge quantization is the only method by which [[Green-Schwarz super p-brane sigma models]] have been quantized, to date. 

### BFSS matrix model

Specifically, applying light-cone gauge quantization to the [[Green-Schwarz sigma model]] for the  [[M2-brane]] on 11d [[Minkowski spacetime]], combined with a certain regularization of the remaining l9ight-cone [[Hamiltonian]] yields the [[BFSS matrix model]].

### BMN matrix model 

Alternatively, applying the light cone gauge quantization of the [[Green-Schwarz sigma-model]] of the [[M2-brane]] not on [[Minkowski spacetime]] but, more generally, on 11d [[pp-wave spacetimes]] (which are [[Penrose limits]] of the [[near horizon geometry]] of the [[black brane|black]] [[M2-branes]]/[[M5-branes]]) yields the [[BMN matrix model]].


## Related concepts

* [[large N limit]]

* [[holographic light front QCD]]

## References

### General

The concept originates with

* [[Paul A. M. Dirac]], §5 "The Front Form", in: *Forms of Relativistic Dynamics*, Rev. Mod. Phys. **21** (1949) 392-399 &lbrack;[doi:10.1103/RevModPhys.21.392](https://doi.org/10.1103/RevModPhys.21.392)&rbrack;

and was rediscovered in

* [[Steven Weinberg]], *Dynamics at Infinite Momentum*, Phys. Rev. **150** (1966) 1313,  Erratum Phys. Rev. 158, 1638 (1967) &lbrack;[doi:10.1103/PhysRev.150.1313](https://doi.org/10.1103/PhysRev.150.1313)&rbrack;

Early review:

* Shau-Jin Chang, Robert G. Root, and Tung-Mow Yan, *Quantum Field Theories in the Infinite-Momentum Frame. I. Quantization of Scalar and Dirac Fields*, Phys. Rev. D **7**,  (1973) 1133 &lbrack;[doi:10.1103/PhysRevD.7.1133](https://doi.org/10.1103/PhysRevD.7.1133)&rbrack;

The notion of lightlike circle compactificaiton ("discrete light cone quantization"):

* [[Hans-Christian Pauli]], [[Stanley J. Brodsky]], *Solving field theory in one space and one time dimension*, Phys. Rev. D **32** (1985) 1993 &lbrack;[doi:10.1103/PhysRevD.32.1993](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.32.1993)&rbrack;


Application to [[QCD]]:

* [[G. Peter Lepage]], [[Stanley J. Brodsky]], *Exclusive processes in perturbative quantum chromodynamics*, Phys. Rev. D **22** (1980) 2157 &lbrack;[doi:10.1103/PhysRevD.22.2157](https://doi.org/10.1103/PhysRevD.22.2157)&rbrack;

* [[Stanley Brodsky]], [[Hans-Christian Pauli]], S. Pinsky, *Quantum Chromodynamics and Other Field Theories on the Light Cone*, Phys. Rept. **301** (1998) 299-486 &lbrack;[arXiv:hep-ph/9705477](https://arxiv.org/abs/hep-ph/9705477), <a href="https://doi.org/10.1016/S0370-1573(97)00089-6">doi:10.1016/S0370-1573(97)00089-6</a>&rbrack;


Review:

* {#Ydri18} [[Badis Ydri]], Section 3.9 of: _Review of M(atrix)-Theory, Type IIB Matrix Model and Matrix String Theory_ ([arXiv:1708.00734](https://arxiv.org/abs/1708.00734)), published as: _Matrix Models of String Theory_, IOP 2018 ([ISBN:978-0-7503-1726-9](https://iopscience.iop.org/book/978-0-7503-1726-9))




All the standard introductory texts on [[string theory]] have sections devoted to light-cone quantization. For instance

* [[Michael Green]], [[John Schwarz]], [[Edward Witten]], section 5.2.1 of: _Superstring theory_, 3 vols. Cambridge Monographs on Mathematical Physics

See also

* Philip D. Mannheim, _Light-front quantization is instant-time quantization_ ([arXiv:1909.03548](https://arxiv.org/abs/1909.03548))

* Philip D. Mannheim, Peter Lowdon, [[Stanley Brodsky]], 
_Comparing light-front quantization with instant-time quantization_ ([arXiv:2005.00109](https://arxiv.org/abs/2005.00109))



[[!include quantization of M2-brane on Minkowski spacetime to BFSS matrix model -- references]]





[[!redirects light cone gauge quantization]]

[[!redirects light-cone gauge]]
[[!redirects light cone gauge]]
[[!redirects lightcone gauge]]

[[!redirects discrete light cone quantization]]
[[!redirects discrete light-cone quantization]]
[[!redirects discrete lightcone quantization]]
[[!redirects discrete light cone quantizations]]
[[!redirects discrete light-cone quantizations]]
[[!redirects discrete lightcone quantizations]]

[[!redirects DLCQ]]

[[!redirects light-front quantization]]

[[!redirects light cone momentum]]
[[!redirects light-cone momentum]]
[[!redirects lightcone momentum]]

[[!redirects light cone longitudal]]
[[!redirects light cone transversal]]
[[!redirects light-cone longitudal]]
[[!redirects light-cone transversal]]
[[!redirects lightcone longitudal]]
[[!redirects lightcone transversal]]
