[[!redirects higher curvature corrections]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In the context of [[gravity]] ([[general relativity]]), _higher curvature corrections_ are modifications of the [[Einstein-Hilbert action]] that include not just the linear appearance of the [[scalar curvature]] $R$ but higher scalar powers of the [[Riemann curvature tensor]].

When viewing Einstein-Hilbert [[gravity]] as an [[effective field theory]] valid at low [[energy]]/long [[wavelengths]], then higher curvature corrections are precisely the terms that may appear at higher energy in pure gravity. Notably the effective field theories induced by [[string theory]] come with infinite towers of higher curvature corrections.

In the context of [[cosmology]], higher curvature corrections are a candidate for the [[inflaton field]], see at _[[Starobinsky model of cosmic inflation]]_.

A [[spacetime]] that extremizes the [[Einstein-Hilbert action]] for given [[cosmological constant]] and _arbitrary_ higher curvature correction is called a _[[universal spacetime]]_.

## Examples

### For 11d Supergravity

A systematic analysis of the possible [[supersymmetry|supersymmetric]] [[higher curvature corrections]] of [[D=11 supergravity]] makes the [[I8]]-[[characteristic class|characteristic 8-form]] 

\[
  I_8(R)
  \;\coloneqq\;
  \tfrac{1}{48}
  \Big(
    p_2(R) \;-\; \big( \tfrac{1}{2} p_1(R)\big)^2
  \Big)
  \;\; 
  \in
  \Omega^8
\]

(a [[differential form]] built from the [[Riemann curvature]], expressing a polynomial in the first and second [[Pontryagin classes]], see at _[[I8]]_) appear as the higher curvature correction at order $\ell^6$, where $\ell$ is the [[Planck length]] in 11d ([Souères-Tsimpis 17, Section 4](#SoueresTsimpis17)).

At this order, the [[equation of motion]] for the [[supergravity C-field]] [[flux]] $G_4$ and its dual $G_7$ is ([Souères-Tsimpis 17, (4.3)](#SoueresTsimpis17))

\[
  \label{11dSugraBIAtOrder6}
  d G_7(\ell)
  \;=\;
  -\tfrac{1}{2}
  G_4(\ell) \wedge G_4(\ell)
  + 
  \ell^6 I_8(R)
  \,,
\]

where the flux forms themselves appear in their higher order corrected form as [[power series]] in the [[Planck length]]

$$
  G_4(\ell)
  \;=\;
  G_4 + \ell^6 G_4^{(1)} + \cdots
$$

$$
  G_7(\ell)
  \;=\;
  G_7 + \ell^6 G_7^{(1)} + \cdots
$$

([Souères-Tsimpis 17, (4.4)](#SoueresTsimpis17))

Beware that this is not the lowest order [[higher curvature correction]]: there is already one at $\mathcal{O}(\ell^3)$, given by $\ell^3 G_4 \wedge \tfrac{1}{2}p_1(R)$ ([Souères-Tsimpis 17, Section 3.2](#SoueresTsimpis17)). Hence the full correction at $\mathcal{O}(\ell^3)$ should be the further modification of (eq:11dSugraBIAtOrder6) to (cf. [Tsimpis 2004, p. 8](#Tsimpis04)):

\[
  \label{11dSugraBIAtOrder6}
  d G_7(\ell)
  \;=\;
  -\tfrac{1}{2}
  G_4(\ell) \wedge 
  \big( 
    G_4(\ell)
    -
    \tfrac{1}{2} p_1(R)
  \big)
  + 
  \ell^6 I_8(R)
  \,.
\]




## Related concepts

* [[universal spacetime]]

* [[non-perturbative effect]]


## References

### General

Discussion of quadratic curvature currections includes (see also at _[[Starobinsky model of cosmic inflation]]_):

* [[Luis Alvarez-Gaume]], [[Alex Kehagias]], [[Costas Kounnas]], [[Dieter Luest]], Antonio Riotto, _Aspects of Quadratic Gravity_ ([arXiv:1505.07657](http://arxiv.org/abs/1505.07657))

Discussion of [[causal locality]] in the presence of higher curvature corrections includes

* Xian O. Camanho, Jose D. Edelstein, [[Juan Maldacena]], Alexander Zhiboedov, _Causality Constraints on Corrections to the Graviton Three-Point Coupling_ ([arXiv:](http://arxiv.org/abs/1407.5597))

* Giuseppe D'Appollonio, [[Paolo Di Vecchia]], [[Rodolfo Russo]], [[Gabriele Veneziano]], _Regge behavior saves String Theory from causality violations_ ([arXiv:1502.01254](http://arxiv.org/abs/1502.01254))

Discussion in the context of corrections to [[black hole entropy]]:

* [[Thomas Mohaupt]], _Strings, higher curvature corrections, and black holes_ ([arXiv:hep-th/0512048](http://arxiv.org/abs/hep-th/0512048))

Discussion of [[renormalization]] for gravity with higher curvature corrections:

* Nobuyoshi Ohta, *One-loop divergences in higher-derivative gravity*, in *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2210.02583](https://arxiv.org/abs/2210.02583)&rbrack;


Discussion of higher curvature corrections in [[cosmology]] and [[cosmic inflation]] (for more see at [[Starobinsky model of cosmic inflation]]):

* Gustavo Arciniega, Jose D. Edelstein, Luisa G. Jaime, _Towards purely geometric inflation and late time acceleration_ ([arXiv:1810.08166](https://arxiv.org/abs/1810.08166))

* Gustavo Arciniega, Pablo Bueno, Pablo A. Cano, Jose D. Edelstein, Robie A. Hennigar, Luisa G. Jaimem, _Geometric Inflation_ ([arXiv:1812.11187](https://arxiv.org/abs/1812.11187))

Relation to [[cosmic censorship hypothesis]]:

* Akash K Mishra, Sumanta Chakraborty, _Strong Cosmic Censorship in higher curvature gravity_, Phys. Rev. D 101, 064041 (2020) ([arXiv:1911.09855](https://arxiv.org/abs/1911.09855))

See also:

* Jesse Daas, Cristobal Laporte, Frank Saueressig, Tim van Dijk: *Rethinking the Effective Field Theory formulation of Gravity* &lbrack;[arXiv:2405.12685](https://arxiv.org/abs/2405.12685)&rbrack;


For [[supergravity]]:

* Mehmet Ozkan, Yi Pang, [[Ergin Sezgin]], *Higher Derivative Supergravities in Diverse Dimensions* &lbrack;[arXiv:2401.08945](https://arxiv.org/abs/2401.08945)&rbrack;


### For $D=4$ supergravity

Discussion of [[higher curvature corrections]] to [[D=4 supergravity]]:

Relation to [[quintessence]]:

* [[Fotis Farakos]], _Quintessence from higher curvature supergravity_ ([arXiv:2003.09366](https://arxiv.org/abs/2003.09366))

On [[small N corrections]] in [[ABJM theory]] and [[higher curvature corrections]] in the [[AdS/CFT duality|AdS/CFT dual]] [[D=4 supergravity]]:

* [[Nikolay Bobev]], Anthony M. Charles, [[Kiril Hristov]], Valentin Reys, *The Unreasonable Effectiveness of Higher-Derivative Supergravity in $AdS_4$ Holography*, Phys. Rev. Lett. **125** 131601 (2020) \[<a href="https://doi.org/10.1103/PhysRevLett.125.131601">doi:10.1103/PhysRevLett.125.131601</a>, [arXiv:2006.09390](https://arxiv.org/abs/2006.09390)\]

* [[Nikolay Bobev]], Anthony M. Charles, [[Dongmin Gang]], [[Kiril Hristov]], Valentin Reys, *Higher-Derivative Supergravity, Wrapped M5-branes, and Theories of Class $\mathcal{R}$*,  J. High Energ. Phys. **2021** 58 (2021) \[<a href="https://doi.org/10.1007/JHEP04(2021)058">doi:10.1007/JHEP04(2021)058</a>, [arXiv:2011.05971](https://arxiv.org/abs/2011.05971)\]

* [[Kiril Hristov]], *ABJM at finite $N$ via 4d supergravity*,  J. High Energ. Phys. **2022** 190 (2022) \[<a href="https://doi.org/10.1007/JHEP10(2022)190">doi:10.1007/JHEP10(2022)190</a>, [arXiv:2204.02992](https://arxiv.org/abs/2204.02992)\]


### For $D=5$ supergravity

Discussion for [[D=5 supergravity]]:

Analysis via computer algebra:

* Gregory Gold, Saurish Khandelwal, Gabriele Tartaglino-Mazzucchelli, *Supergravity Component Reduction with Computer Algebra* &lbrack;[arXiv:2406.19687](https://arxiv.org/abs/2406.19687)&rbrack;



### For $D=10$ heterotic supergravity

On higher curvature corrections to [[heterotic supergravity]]:

* Eric Lescano, Carmen Núñez, Jesús A. Rodríguez, *Supersymmetry, T-duality and Heterotic $\alpha'$-corrections* ([arXiv:2104.09545](https://arxiv.org/abs/2104.09545))

* Hao-Yuan Chang, [[Ergin Sezgin]], Yoshiaki Tanii, *Dimensional reduction of higher derivative heterotic supergravity* ([arXiv:2110.13163](https://arxiv.org/abs/2110.13163))



[[!include higher curvature corrections to D=11 supergravity -- references]]



[[!include DBI-action higher curvature corrections -- references]]



[[!redirects higher order curvature corrections]]