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

Beware that this is not the lowest order [[higher curvature correction]]: there is already one at $\mathcal{O}(\ell^3)$, given by $\ell^3 G_4 \wedge \tfrac{1}{2}p_1(R)$ ([Souères-Tsimpis 17, Section 3.2](#SoueresTsimpis17)). Hence the full correction at $\mathcal{O}(\ell^3)$ should be the further modification of (eq:11dSugraBIAtOrder6) to

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
  \,,
\]




## Related concepts

* [[universal spacetime]]

* [[non-perturbative effect]]

## References

### General

Discussion of quadratic curvature currections includes (see also at _[[Starobinsky model of cosmic inflation]]_)

* [[Luis Alvarez-Gaume]], [[Alex Kehagias]], [[Costas Kounnas]], [[Dieter Luest]], Antonio Riotto, _Aspects of Quadratic Gravity_ ([arXiv:1505.07657](http://arxiv.org/abs/1505.07657))

Discussion of [[causal locality]] in the presence of higher curvature corrections includes

* Xian O. Camanho, Jose D. Edelstein, [[Juan Maldacena]], Alexander Zhiboedov, _Causality Constraints on Corrections to the Graviton Three-Point Coupling_ ([arXiv:](http://arxiv.org/abs/1407.5597))

* Giuseppe D'Appollonio, [[Paolo Di Vecchia]], [[Rodolfo Russo]], [[Gabriele Veneziano]], _Regge behavior saves String Theory from causality violations_ ([arXiv:1502.01254](http://arxiv.org/abs/1502.01254))

Discussion in the context of corrections to [[black hole entropy]] include

* [[Thomas Mohaupt]], _Strings, higher curvature corrections, and black holes_ ([arXiv:hep-th/0512048](http://arxiv.org/abs/hep-th/0512048))

Discussion of higher curvature corrections in [[cosmology]] and [[cosmic inflation]] (for more see at [[Starobinsky model of cosmic inflation]]):

* Gustavo Arciniega, Jose D. Edelstein, Luisa G. Jaime, _Towards purely geometric inflation and late time acceleration_ ([arXiv:1810.08166](https://arxiv.org/abs/1810.08166))

* Gustavo Arciniega, Pablo Bueno, Pablo A. Cano, Jose D. Edelstein, Robie A. Hennigar, Luisa G. Jaimem, _Geometric Inflation_ ([arXiv:1812.11187](https://arxiv.org/abs/1812.11187))

Relation to [[cosmic censorship hypothesis]]:

* Akash K Mishra, Sumanta Chakraborty, _Strong Cosmic Censorship in higher curvature gravity_, Phys. Rev. D 101, 064041 (2020) ([arXiv:1911.09855](https://arxiv.org/abs/1911.09855))


### Higher curvature corrections to 4d supergravity

Discussion of [[higher curvature corrections]] to [[D=4 supergravity]]:

Relation to [[quintessence]]:

* [[Fotis Farakos]], _Quintessence from higher curvature supergravity_ ([arXiv:2003.09366](https://arxiv.org/abs/2003.09366))



### Higher curvature corrections to 11d Supergravity

Discussion of higher curvature corrections to [[11-dimensional supergravity]] includes

* [[Arkady Tseytlin]], _$R^4$ terms in 11 dimensions and conformal anomaly of (2,0) theory_, Nucl. Phys. B584: 233-250, 2000 ([arXiv:hep-th/0005072](https://arxiv.org/abs/hep-th/0005072))

* [[Kasper Peeters]], Pierre Vanhove, Anders Westerberg, _Supersymmetric $R^4$ actions and quantum corrections to superspace torsion constraints_ ([arXiv:hep-th/0010182](https://arxiv.org/abs/hep-th/0010182))

* H. Lu, [[Christopher Pope]], [[Kellogg Stelle]], [[Paul Townsend]], _Supersymmetric Deformations of $G_2$ Manifolds from Higher-Order Corrections to String and M-Theory_, JHEP 0410:019, 2004 ([arXiv:hep-th/0312002](https://arxiv.org/abs/hep-th/0312002))

  (specifically for [[M-theory on G2-manifolds]])

* H. Lu, [[Christopher Pope]], [[Kellogg Stelle]], [[Paul Townsend]], _String and M-theory Deformations of Manifolds with Special Holonomy_, JHEP 0507:075, 2005 ([arXiv:hep-th/0410176](https://arxiv.org/abs/hep-th/0410176))

  (specifically for [[M-theory on G2-manifolds]])

* [[Dimitrios Tsimpis]], _11D supergravity at $\mathcal{O}(\ell^3)$_, JHEP0410:046, 2004 ([arXiv:hep-th/0407271](https://arxiv.org/abs/hep-th/0407271))

* {#Howe04} [[Paul Howe]], _$R^4$ terms in supergravity and M-theory_ ([arXiv:hep-th/0408177](https://arxiv.org/abs/hep-th/0408177))

* {#CGNT04} [[Martin Cederwall]], [[Ulf Gran]], [[Bengt Nilsson]], [[Dimitrios Tsimpis]], _Supersymmetric Corrections to Eleven-Dimensional Supergravity_, JHEP0505:052, 2005 ([arXiv:hep-th/0409107](https://arxiv.org/abs/hep-th/0409107))

* Yoshifumi Hyakutake, Sachiko Ogushi, _$R^4$ Corrections to Eleven Dimensional Supergravity via Supersymmetry_, Phys.Rev. D74 (2006) 025022 ([arXiv:hep-th/0508204](https://arxiv.org/abs/hep-th/0508204))

* Yoshifumi Hyakutake, Sachiko Ogushi, _Higher Derivative Corrections to Eleven Dimensional Supergravity via Local Supersymmetry_, JHEP0602:068, 2006 ([arXiv:hep-th/0601092](https://arxiv.org/abs/hep-th/0601092))

* Anirban Basu, _Constraining gravitational interactions in the M theory effective action_, Classical and Quantum Gravity, Volume 31, Number 16, 2014 ([arXiv:1308.2564](https://arxiv.org/abs/1308.2564))

* {#SoueresTsimpis17} Bertrand Souères, [[Dimitrios Tsimpis]], _The action principle and the supersymmetrisation of Chern-Simons terms in eleven-dimensional supergravity_, Phys. Rev. D 95, 026013 (2017) ([arXiv:1612.02021](https://arxiv.org/abs/1612.02021))

  (discussion of [[I8]] in Section 4)


and from the [[ABJM  model]]:

* Damon J. Binder, Shai M. Chester, Silviu S. Pufu, _Absence of $D^4 R^4$ in M-Theory From ABJM_ ([arXiv:1808.10554](https://arxiv.org/abs/1808.10554))

See also

* [[Mohammad Garousi]], _Minimal gauge invariant couplings at order $\ell^6_p$ in M-theory_ ([arXiv:2102.00639](https://arxiv.org/abs/2102.00639))


Discussion in view of the [[Starobinsky model of cosmic inflation]] is in

* [[Katrin Becker]], [[Melanie Becker]], _Supersymmetry Breaking, M-Theory and Fluxes_, JHEP 0107:038,2001 ([arXiv:hep-th/0107044](https://arxiv.org/abs/hep-th/0107044))

* Kazuho Hiraga, Yoshifumi Hyakutake, _Inflationary Cosmology via Quantum Corrections in M-theory_ ([arXiv:1809.04724](https://arxiv.org/abs/1809.04724))

* Kazuho Hiraga, Yoshifumi Hyakutake, _Scalar Cosmological Perturbations in M-theory with Higher Derivative Corrections_ ([arxiv:1910.12483](https://arxiv.org/abs/1910.12483))


and in view of [[de Sitter spacetime]] vacua:

* Johan Blåbäck, [[Ulf Danielsson]], Giuseppe Dibitetto, Suvendu Giri, _Constructing stable de Sitter in M-theory from higher curvature corrections_ ([arXiv:1902.04053](https://arxiv.org/abs/1902.04053))



[[!include DBI-action higher curvature corrections -- references]]



[[!redirects higher order curvature corrections]]