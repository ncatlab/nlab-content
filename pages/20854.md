
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The microscopic geometry of transversal [[Dp-D(p+2)-brane intersections]] and [[Dp-D(p+4)-brane intersections]] look like warped [[non-commutative geometry|non-commutative]] [[metric cones]] on [[fuzzy spheres]] (namely on the spheres around the lower dimensional [[D-branes]] inside the higher dimensional D-branes). These have hence been called _fuzzy funnels_.

<center>
<img src="https://ncatlab.org/nlab/files/D6D8FuzzyFunnel.jpg" width="600">
</center>

> graphics grabbed from [Fazzi 17, Fig. 3.14](#Fazzi17), taken in turn from 
[Gaiotto-Tomassiello 14, Figure 5](#GaiottoTomassiello14)

<center>
<img src="https://ncatlab.org/nlab/files/D3D5FuzzyFunnel.jpg" width="600">
</center>

> graphics grabbed from [Fazzi 17](#Fazzi17)

[[!include Dp-D(p+2)-brane intersections in fuzzy funnels -- section]]

## Properties

### Single trace observables as $\mathfrak{su}(2)$-weight systems on chord diagrams
  {#SingleTraceObservablesAsWeightSystemsOnChordDiagrams}

We discuss how the [[single trace observables]] on the [[fuzzy 2-sphere]]-sections  of [[Dp-D(p+2) brane intersection]] [[fuzzy funnels]] are given by [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] (following [Ramgoolam-Spence-Thomas 04](#RamgoolamSpenceThomas04), [McNamara-Papageorgakis 05](#McNamaraPapageorgakis05), see [McNamara 06, Section 4](#McNamara06) for review).

For more see at _[[weight systems on chord diagrams in physics]]_.


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WeightSystemsAsShapeObservabesOnFuzzySphere.jpg" width="400">
</div>


\linebreak


While in the commutative [[large N limit]], all powers of the [[radius]] function on the [[fuzzy 2-sphere]] are equal

$$
  \underset{N\to \infty}{\lim}
  \int_{S^2_N} R^{2 k}
  \;=\;  
  4 \pi 
  \,;
$$

for [[finite number|finite]] $N$ there is an ordering ambiguity: In fact, the number of functions on the [[fuzzy 2-sphere]] at [[finite number|finite]] $N$ that all go to the same function $R^{2k}$ in the [[large N limit]] grows rapidly with $k$.

At $k = 1$ there is the single radius observable (eq:RadiusOfFuzzy2Sphere)

$$
  \int_{S^2_N} R^2 
  \;=\; 
  \int_{S^2_N}
  \underset{i}{\sum} X_i \cdot X_i
  \;=\;
  4 \pi \tfrac{ N }{ \sqrt{N^2 -1} }
$$

At $k = 2$ there are, under the integral (eq:FuzzyS2Integration), two radius observables:

1. $ \int_{S^2_N} \underset{i,j}{\sum} X_i X_i X_j X_j$

1. $\int_{S^2_N} \underset{i,j}{\sum} X_i X_j X_j X_i$

(Here we are using that under the integral/trace, a [[cyclic permutation]] of the factors in the integrand does not change the result).

Similarly for higher $k$, where the number of possible orderings increases rapidly. The [[combinatorics]] that appears here is familiar in [[knot theory]]:

Every ordering of operators, up to cyclic permutation, in the [[single trace observable]] $Tr(R^2)^n$ is encoded in a [[chord diagram]] and the value of the corresponding [[single trace observable]] is the value of the [[su(2)]]-[[Lie algebra weight system]] on this chord diagram.



## Related concepts

* [[Nahm's equation]]

* [[fuzzy sphere]]

* [[noncommutative torus]]



\linebreak

[[!include brane bound states -- table]]

## References

### General

* Rajsekhar Bhattacharyya, Robert de Mello Koch, _Fluctuating Fuzzy Funnels_, JHEP 0510 (2005) 036 ([arXiv:hep-th/0508131](https://arxiv.org/abs/hep-th/0508131))


### For D1-D3-brane intersections

On [[D1-D3 brane intersections]] as fuzzy funnels on [[fuzzy 2-spheres]]:

* [[Neil Constable]], [[Robert Myers]], Oyvind Tafjord, _The Noncommutative Bion Core_, Phys. Rev. D61 (2000) 106009 ([arXiv:hep-th/9911136](https://arxiv.org/abs/hep-th/9911136))

* [[Robert Myers]], Section 4 of: _Nonabelian D-branes and Noncommutative Geometry_, J. Math. Phys. 42: 2781-2797, 2001 ([arXiv:hep-th/0106178](https://arxiv.org/abs/hep-th/0106178))

* [[Neil Constable]], [[Neil Lambert]], _Calibrations, Monopoles and Fuzzy Funnels_, Phys. Rev. D66 (2002) 065016 ([arXiv:hep-th/0206243](https://arxiv.org/abs/hep-th/0206243))


### For D3-D5 brane intersections

On [[D3-D5 brane intersections]] as fuzzy funnels on [[fuzzy 2-spheres]]:

* [[Davide Gaiotto]], [[Edward Witten]], Section 3.4.3 of: _Supersymmetric Boundary Conditions in N=4 Super Yang-Mills Theory_, J Stat Phys (2009) 135: 789 ([arXiv:0804.2902](https://arxiv.org/abs/0804.2902))

* {#Fazzi17} [[Marco Fazzi]], Section 3.2.3 of: _Higher-dimensional field theories from type II supergravity_ ([arxiv:1712.04447](https://arxiv.org/abs/1712.04447))

### For D6-D8 brane intersections

On [[D6-D8 brane intersections]] as fuzzy funnels on [[fuzzy 2-spheres]]:

* {#GaiottoTomassiello14} [[Davide Gaiotto]], [[Alessandro Tomasiello]], _Holography for $(1,0)$ theories in six dimensions_, JHEP 12 (2014) 003 ([arXiv:1404.0711](https://arxiv.org/abs/1404.0711))

* [Fazzi 17, p. 41-46](#Fazzi17)

### For D1-D5-brane intersections

On [[D1-D5 brane intersections]] as fuzzy funnels on [[fuzzy 4-spheres]]:

* [[Neil Constable]], [[Robert Myers]], Oyvind Tafjord, _Non-abelian Brane Intersections_, JHEP 0106:023, 2001 ([arXiv:hep-th/0102080](https://arxiv.org/abs/hep-th/0102080))


### For D1-D7-brane intersections

On [[D1-D7 brane intersections]] as fuzzy funnels on [[fuzzy 6-spheres]]:

* [[Paul Cook]], Robert de Mello Koch, Jeff Murugan, _Non-Abelian BIonic Brane Intersections_,  Phys. Rev. D68:126007, 2003 ([arXiv:hep-th/0306250](https://arxiv.org/abs/hep-th/0306250))


### Single trace observables as weight systems on chord duagrams

Relation of [[single trace observables]] on [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] computing [[radii]] averages of [[fuzzy spheres]]:

* {#RamgoolamSpenceThomas04} [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* {#McNamaraPapageorgakis05} [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* {#McNamara06} [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])


[[!redirects fuzzy funnels]]