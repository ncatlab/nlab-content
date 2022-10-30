
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

In [[perturbative quantum field theory]] formalized as [[causal perturbation theory]]/[[perturbative AQFT]] the _retarded products_ ([Glaser-Lehmann-Zimmermann 57](#GlaserLehmannZimmermann57)) is a system of [[operator-valued distributions]] which are the [[coefficients]] in the [[formal power series]] expression for the [[quantum observables on interacting fields]]. 

If the quantum observables are obtained via [[Bogoliubov's formula]] from the [[S-matrix]] induced by [[time-ordered products]], then the retarded products may be expressed in terms of the [[time-ordered products]]. But the retarded producst may also be [[axiom|axiomatized]] directly ([D&#252;tsch-Fredenhagen 04](#DuetschFredenhagen04)),
see ([Collini 16, section 2.2](#Collini16)).


## Definition


Let $\Sigma$ be a [[spacetime]] of [[dimension]] $p + 1$ and let $E \overset{fb}{\longrightarrow} \Sigma$ be a [[field bundle]]. Let $\mathbf{L}_{free}\in \Omega^{p+1,0}_\Sigma(E)$ be a [[local Lagrangian density]] for a [[free field theory]] with [[field (physics)|fields]] of type $E$. Let $\mathcal{W}$ be the corresponding [[Wick algebra]] of [[quantum observables]] of the free field, with 

$$
  \mathcal{F}_{loc} \overset{:(-):}{\longrightarrow} \mathcal{W}
$$

the corresponding quantization map from [[local observables]] ("[[normal ordering]]").

Let then 

$$
  S
  \;\colon\;
  \mathcal{F}_{loc}\langle g,j\rangle 
    \longrightarrow 
  \mathcal{W}[ [ g/\hbar ] ][ [ j/\hbar ] ]
$$ 

be a  [[perturbative S-matrix]]. Moreover let

$$
  g_{sw} \mathbf{L}_{int} \in \mathcal{F}_{loc}\langle g\rangle
$$ 

be an [[adiabatic switching|adiabatically switched]]
[[interaction]] [[Lagrangian density]], so that the full Lagrangian density is

$$
  \mathbf{L} = \mathbf{L}_{free} + g \mathbf{L}_{int}
  \,.
$$


For $A \in \mathcal{F}_{loc}$ a [[local observable]] and $j \in C^\infty_{cp}(\Sigm)$, write

$$
  Z_L(\epsilon j A)
  \; \coloneqq \;
  S(g_{sw}\mathbf{L}_{int}) S( g_{sw}\mathbf{L}_{int} + j A )
$$

for the [[generating function]] induced by the perturvbative [[S-matrix]].


+-- {: .num_defn #RetardedProductFromPerturbativeSMatrix}
###### Definition
**([[retarded products]] induced from perturbative S-matrix)

It follows from the "perturbation" axiom on the [[S-matrix]] (see there) that there is a system of [[continuous linear functionals]]

$$
  R
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g\rangle\right)^{\otimes^k}
    \otimes
  (\mathcal{F}_{loc})^{\otimes^l}
    \longrightarrow
  \mathcal{W}[ [ g/\hbar] ] [ [ j/\hbar] ]
$$

for all $k,l \in \mathbb{N}$ such that the [[generating function]] induced by the [[S-matrix]] is expressed as

$$
  Z_{g_{sw} L}(j_{sw} A)
  =
  \underset{k,l \in \mathbb{N}}{\sum} \frac{1}{k! l!}
  R(
    \underset{k \,\text{arguments}}{\underbrace{ g_{sw} L \cdots g_{sw} L } },
    \underset{l \; \text{arguments}}{\underbrace{ j_{sw} A \cdots j_{sw} A }}
  )
  \,.
$$

Similarly there is

$$
  R
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g \rangle\right)^{\otimes^k}
    \otimes
  \left(\mathcal{F}_{loc}\langle j \rangle\right)
    \longrightarrow
  \mathcal{W}[ [ g ] ] [ [ \hbar ] ]
$$

such that

$$
  \widehat{A}(h)
  =
  \underset{k \in \mathbb{N}}{\sum} \frac{1}{k!}
  r( \underset{k \,\text{arguments}}{\underbrace{g_{sw}L_{int} \cdots g_{sw}L_{int}}}, h A )
  \,.
$$

These are called the (generating) _retarded products_ ([Glaser-Lehmann-Zimmermann 57](#GlaserLehmannZimmermann57), [Epstein-Glaser 73, section 8.1](#EpsteinGlaser73)).

=--

The actual retarded products are, via _[[Bogoliubov's formula]]_, the [[derivatives]] of these generating retarded products with respect to the [[source field]].

## Related concepts

[[!include products in pQFT -- table]]


## References

The concept goes back to

* {#GlaserLehmannZimmermann57} [[Vladimir Glaser]], H. Lehmann, W. Zimmermann, _Field operators and retarded functions_, Il Nuovo Cimento 6, 1122-1128 (1957) ([doi:10.1007/bf02747395](http://dx.doi.org/10.1007/bf02747395))

* O. Steinmann, _Perturbation Expansions in Axiomatic Field Theory_, Lecture Notes in Physics, vol. 11, Springer, Berlin and Heidelberg, 1971.

Discussion of retarded products as derived from [[time-ordered products]] in [[causal perturbation theory]] is due to

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], section 8.1 of _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

Direct axiomatization of retarded products is due to

* {#DuetschFredenhagen04} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Causal perturbation theory in terms of retarded products, and a proof of the Action Ward Identity_, Rev. Math. Phys. 16, 1291 (2004) ([arXiv:hep-th/0403213](https://arxiv.org/abs/hep-th/0403213))

reviewed for instance in

* {#Collini16} [[Giovanni Collini]], section 2.2 of _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

[[!redirects retarded products]]
