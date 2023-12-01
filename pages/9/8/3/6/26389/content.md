
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
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

In ([[higher gauge theory|higher]]) [[gauge theory]], the total (generalized) electric/magnetic [[fluxes]] through given [[surfaces]] (or higher [[submanifolds]]) should be [[observables]] and hence have [[Poisson brackets]] in the [[classical field theory]] To the extent that these induce non-trivial operator [[commutators]] in the corresponding [[quantum field theory]], this means that the corresponding kinds of fluxes would be subject to the [[Heisenberg uncertainty principle]].

A subtlety here is that the usual [[phase space]]-methods for [[Lagrangian field theories]] directly provide these brackets only for the [[differential forms]] which are the [[flux densities]]. These however, provide only a [[rational homotopy theory|rational]] image of the fluxes, which in general may furthermore have [[torsion subgroup|torsion]]-[[cohomology group|cohomology]]-components.

In plain [[electromagnetism]], the [[canonical momentum]] of the [[gauge potential]] $A$ is proportional (by constants to be ignored in the following) to the electric flux density $\star F$ (where $F$ is the [[Faraday tensor]] [[flux density]] and $\star$ is the [[Hodge star operator]] on the given [[spacetime]] [[pseudo-Riemannian manifold]]), which however means that the the Poisson bracket of the magnetic flux density $F \equiv \mathrm{d}_{dR} A$ with the electric flux density is a total derivative (cf. eg. [Blaschke & Gieres 2021 (5.5)](Yang-Mills+theory#BlaschkeGieres21)), so that the bracket of the integrated fluxes $\Phi_E$ and $\Phi_B$ through given [[orientable manifold|orientable]] [[closed manifold|closed]] surfaces $S_E$ and $S_B$, respectively, actually vanishes (cf. [FMS07b (3.6)](#FreedMooreSegal07b)):

$$
  \big\{
    \Phi_E
    ,\,
    \Phi_B
  \big\}
  \;\equiv\;
  \Big\{
  \textstyle{\int}_{S_B} \star F 
  ,\,
  \textstyle{\int}_{S_E} F
  \Big\}
  \;=\;
  0
  \,.
$$

The thrust of [FMS 07a](#FreedMooreSegal07a), [07b](#FreedMooreSegal07b) is the claim that this bracket becomes non-vanishing if torsion-components of the fluxes (through their enhancement to [[ordinary differential cohomology]]) are retained, but it seems that this is ultimately by definition ([FMS07a, Def. 1.29](#FreedMooreSegal07a); [FMS07b (3.28)](#FreedMooreSegal07b)) more than by derivation from first principles.

On the other hand, for [[non-abelian group|non-abelian]] [[gauge group]], a careful analysis of the (somewhat subtle) Poisson brackets reveals ([Cattaneo & Perez 2017](#CattaneoPerez17)) that the electric fluxes -- understood as flux densities integrated against [[Lie algebra]] valued functions $\alpha$ -- have a non-trivial bracket among *themselves*:

$$
 \big\{
   \Phi^\alpha_E
   ,\,
   \Phi^{\alpha'}_E
 \big\}
 \;\propto\;
 \Phi_E^{[\alpha, \alpha']}
$$

(where $[-,-]$ is the pointwise [[Lie bracket]]). This result has found a lot of attention (only) in the context of [[first-order formulations of gravity]].


## Related concepts

* **[[flux]]**
 
  * [[flux tube]]

  * [[flux quantization]]

  * [[flux compactification]]


## References


In [[electromagnetism]], with focus on torsion components that are argued to not generally commute:

* {#FreedMooreSegal07a} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *The Uncertainty of Fluxes*, Commun. Math. Phys. **271**  (2007) 247-274 &lbrack;[arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3)&rbrack;

* {#FreedMooreSegal07b} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *Heisenberg Groups and Noncommutative Fluxes*,  Annals Phys. **322** (2007) 236-285 &lbrack;[arXiv:hep-th/0605200](http://arxiv.org/abs/hep-th/0605200), [doi:10.1016/j.aop.2006.07.014](https://doi.org/10.1016/j.aop.2006.07.014)&rbrack;


In [[SU(2)]]-[[gauge theory]] (highlighted for the case of the [[first-order formulation of gravity]] but applying verbatim also to [[Yang-Mills theory]], cf. [there](Yang-Mills+theory#ReferencesPhaseSpaceAndCanonicalQuantization)):

* {#CattaneoPerez17} [[Alberto S. Cattaneo]], Alejandro Perez, *A note on the Poisson bracket of 2d smeared fluxes*, Class. Quant. Grav. **34** (2017) 107001 &lbrack;[arXiv:1611.08394](https://arxiv.org/abs/1611.08394), [doi:10.1088/1361-6382/aa69b4](https://doi.org/10.1088/1361-6382/aa69b4)&rbrack;


See also:

* Mikhail A. Savrov, *Commutator of Electric Charge and Magnetic Flux* &lbrack;[arXiv:2003.02225](https://arxiv.org/abs/2003.02225)&rbrack;


