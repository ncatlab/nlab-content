

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### In classical gravity

In an [[action functional]] on a space of [[pseudo-Riemannian manifolds]] -- such as the [[Einstein-Hilbert action]] functional for [[gravity]] -- a **cosmological constant** is a term proportional to the [[volume]] 

$$
  S_{cc} :  (X,g) \mapsto \lambda \int_X dvol_g
  \,,
$$

where $\lambda \in \mathbb{R}$ is the _cosmological constant_ .

For instance pure Einstein-Hilbert gravity with cosmological constant (and no other fields) is given by the functional

$$
  S_{EH} + S_{cos} :  (X,g) \mapsto \int_X R\, dvol + \lambda \int_X d vol_g
  \,,
$$

Generically it happens that one considers action functionals where $\lambda$ is in fact not a constant, but a function of other fields $\phi$ on $X$. 

$$
  S : (X,g,\phi) \mapsto \int_X \lambda(\phi) dvol_g
  \,.
$$

In this context those solutions to the [[Euler-Lagrange equation]]s are of interest in which $\lambda(\phi)$ happens to be exactly or approximately constant. Many such models of not-really-constant-but-effectively-constant terms proportional to the volume are being proposed and considered in attempts to explain observed or speculated dynamics of the cosmos.

See in particular at _[[FRW model]]_ for the role of the cosmological constant in homogeneous and isotropic models as in the [[standard model of cosmology]]. In that context the cosmological constant is also called the _dark energy_ (density), which makes up about 70% of the energy density of the [[observable universe]] (the rest being [[dark matter]]) and a comparatively little bit of [[baryon|baryonic]] [[matter]].


### In perturbative quantum gravity
 {#InPerturbativeQuantumGravity}

In [[perturbative quantum field theory]] [[QFT on curved spacetime]] the cosmological constant receives contributions from the [[vacuum expectation value]] of the [[stress-energy tensor]] of the any [[matter]] [[field (physics)|fields]]. There is [[renormalization]]-freedom in this contribution  ([Wald 78](#Wald78), [Dappiaggi-Fredenhagen-Pinamonti 08](#DappiaggiFredenhagenPinamonti08), [Dappiagi-Hack-Moeller-Pinamonti 10](#DappiagiHackMollerPinamonti10)). 

This means that apart from the freedom of choosing a classical comsological constant in the [[Einstein-Hilbert action]] as above, its [perturbative quantization](A+first+idea+of+quantum+field+theory#InteractingQuantumFields) ([[perturbative quantum gravity]]) introduces [[renormalization]] freedom to the value of the cosmological constant.

The folklore discussion of the "cosmological constant problem" (see the references [below](#CCProblemReferences)) tends not to take this freedom in the theory into account.

### Observation

<img src="http://ncatlab.org/nlab/files/DarkEnergyConcordance.gif" width="500">

(e.g. [Einasto 09, fig 17](#Einasto09))


## Related concepts

* [[FRW model]]

* [[cosmology]]

* [[energy]]

  * [[matter]], [[radiation]], **cosmological constant**

## References


### In pAQFT
 {#ReferencedInpAQFT}

Discussion of the cosmological constant in the rigorous formulation of [[perturbative AQFT]] [[AQFT on curved spacetimes|on curved spacetimes]] includes the following.

The freedom of [[renormalization]] of the [[vacuum expectation value]] of any [[stress-energy tensor]], hence of the cosmological constant, was discussed in

* {#Wald78} [[Robert Wald]], _Trace anomaly of a conformally invariant quantum field in curved spacetime_, Phys. Rev. D 17, 1477 1978 ([doi:10.1103/PhysRevD.17.1477](https://doi.org/10.1103/PhysRevD.17.1477))

Notice that ([Wald 78](#Wald78)) is based on 

* {#Wald77} [[Robert Wald]], _The back reaction effect in particle creation in curved spacetime_, Commun. Math. Phys. (1977) 54: 1. ([doi:10.1007/BF01609833](https://doi.org/10.1007/BF01609833))

which claimed _no_ freedom of renormalization, but [Wald 78](#Wald78) explains that this was due to a mistake inherited from a citation.

Realization of renormalization of stress-energy/cosmological constant in concrete [[FRW models]] is discussed in

* {#DappiaggiFredenhagenPinamonti08} [[Claudio Dappiaggi]], [[Klaus Fredenhagen]], [[Nicola Pinamonti]], _Stable cosmological models driven by a free quantum scalar field_, Phys. Rev. D77:104015, 2008 ([arXiv:0801.2850](https://arxiv.org/abs/0801.2850))

* {#DappiagiHackMollerPinamonti10} [[Claudio Dappiaggi]], Thomas-Paul Hack, Jan Möller, [[Nicola Pinamonti]], _Dark Energy from Quantum Matter_ ([arXiv:1007.5009](https://arxiv.org/abs/1007.5009))


### The "cosmological constant problem"
 {#CCProblemReferences}

Discussion of the experimentally observed tiny cosmological constant and the folklore theoretical problem with that includes the following

* Subir Sarkar, _New results in cosmology_ ([arXiv:hep-ph/0201140](https://arxiv.org/abs/hep-ph/0201140))

* Stefanus Nobbenhuis, _The cosmological constant problem -- an inspiration for new physics_ PhD thesis (2006) ([web](http://igitur-archive.library.uu.nl/dissertations/2006-0615-200938/) [pdf](http://igitur-archive.library.uu.nl/dissertations/2006-0615-200938/c1.pdf))

* Joan Sola, _Cosmological constant and vacuum energy: old and new ideas_, J.Phys.Conf.Ser. 453 (2013) 012015 ([arXiv:1306.1527](https://arxiv.org/abs/1306.1527))
 
* {#Einasto09} Jaan Einasto, _Dark matter_ ([arXiv:0901.0632](https://arxiv.org/abs/0901.0632)) 2009


### In string theory

Discussion from the point of view of [[perturbative string theory]], where the cosmological constant is fixed by the choice of [[perturbative string theory vacuum]] includes

* {#Witten00} [[Edward Witten]], _The Cosmological Constant From The Viewpoint Of String Theory_ ([arXiv:hep-ph/0002297](https://arxiv.org/abs/hep-ph/0002297))

See also

* [[Edward Witten]], _Strong coupling and the cosmological constant_, Mod.Phys.Lett.A10:2153-2156,1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

for discussion in terms of the [[M-theory]]/[[type IIA string theory|type IIA]] relation [[KK-compactification|KK-compactified]] to a 4d/3d scenrio, where the 3d physics is weakly coupled and the 4d physics strongly coupled. (Recall the [[super 2-brane in 4d]].)  

This discussion was later supplemented by 

* [[Edward Witten]], section 3 of _Some Comments On String Dynamics_ ([arXiv:hep-th/9507121](http://arxiv.org/abs/hep-th/9507121))


But a) there might be a large space of [[perturbative string theory vacua]]  and b) the [[de Sitter spacetime|de Sitter vacua]] that seem to correspond to observation tend to exist (only) as metastable vacua:

* {#KachruKalloshLindeTrivedi03} [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip Trivedi]], _de Sitter Vacua in String Theory_, Phys.Rev.D68:046005, 2003 ([arXiv:hep-th/0301240](https://arxiv.org/abs/hep-th/0301240))

This observation led to the discussion of the "[[landscape of string theory vacua]]".

For review see

* {#Kallosh05} [[Renata Kallosh]], section 3 of _de Sitter vacua and the landscape of string theory_, J. Phys. Conf. Ser. 24 (2005) 87-110 ([spire](http://inspirehep.net/record/701033/))


[[!redirects dark energy]]

