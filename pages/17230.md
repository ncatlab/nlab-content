

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

In [[perturbative quantum field theory]] the _Schwinger-Dyson equation_ ([Dyson 49](#Dyson49), [Schwinger 51](#Schinger51)) equates, [[on-shell]], the [[time-ordered product]] of the [[functional derivative]] of the [[action functional]] $S$ for a [[free field theory]] and another [[observable]] $A$ with the [[time ordered product|time ordering]] of the corresponding [[functional derivative]] of just $A$ itself, times $i \hbar$ ([[imaginary unit]] times [[Planck's constant]]):

$$
 \label{EquationSchwingerDyson}
  \mathcal{T}
  \left(
    \underset{\Sigma}{\int}
      \frac{\delta S}{\delta \mathbf{\Phi}^a(x)}
      \cdot
      A^a(x)
      \, dvol_\Sigma(x)
  \right)
  \;=\;
  i \hbar
  \mathcal{T}
  \left(
    \underset{\Sigma}{\int}
    \frac{\delta A^a(x)}{\delta \mathbf{\Phi}^a(x)}
    \,
    dvol_\Sigma(x)     
  \right)  
  \phantom{AAA}
  \text{on-shell}
  \,.
$$

(e.q. [Henneaux-Teitelboim 92, (15.25)](#HenneauxTeitelboim92), [Rejzner 16, remark 7.7](#Rejzner16)).

This may be understood as a special case of the quantum-correction of the [[BV-differential]] by the [[BV-operator]] in [[pQFT]], which is hence also called the _[[Schwinger-Dyson operator]]_; see [there](BV-operator#SchwingerDysonEquation).

Often (eq:EquationSchwingerDyson) is displayed before spacetime-smearing of observables in terms of [[operator products]] of [[operator-valued distributions]] 

$$
  A^a(x) 
    \;\coloneqq\;
  \delta(x-x_0) \delta^a_{a_0} 
  \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
$$

which makes the [[distribution|distributional]] [[Schwinger-Dyson equation]] read

$$
  \begin{aligned}
  & T
  \left(
    \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
      \cdot 
    \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \right)
  \\
  & 
  \underset{\text{on-shell}}{=}
  i \hbar
  \underset{k}{\sum}
  T
  \left(
    \mathbf{\Phi}^{a_1}(x_1)
      \cdots
    \mathbf{\Phi}^{a_{k-1}}(x_{k-1})
      \cdot
    \delta(x_0 - x_k) \delta^{a_0}_{a_k}
      \cdot
    \mathbf{\Phi}^{a_{k+1}}(x_{k+1})
      \cdots
    \mathbf{\Phi}^{a_n}(x_m)
  \right)
  \end{aligned}
$$

(e.q. [Dermisek 09](#Dermisek09))

In particular this means that if $(x_0,a_0) \neq (x_k, a_k)$ for all $k \in \{1,\cdots ,n\}$ then

$$
  T
  \left(
    \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
      \cdot 
    \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \right)
  \;=\;
  0
  \phantom{AAA}
  \text{on-shell}
$$

Since (by the [[principle of extremal action]]) the equation 

$$
  \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
  \;=\;
  0
$$ 


is  the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] (for the [[classical field theory]]) "at $x_0$", this may be interpreted as saying that the classical equations of motion for fields at $x_0$ still hold for [[time-ordered product|time-ordered]] [[quantum theory|quantum]] [[expectation values]], as long as all other observables are evaluated away from $x_0$; while if observables do coincide at $x_0$ then there is a correction (governed by the [[BV-operator]] of the theory, see [this prop.](BV-operator#DysonSchwinger)).

## Details

For details and proof see at _[[BV-operator]]_ [this prop.](BV-operator#DysonSchwinger), following [Rejzner 16, remark 7.7](#Rejzner16), following [Henneaux-Teitelboim 92, section 15.5.3](#HenneauxTeitelboim92)

## Related concepts

* [[path integral]]

* [[Feynman diagram]]

## References

The equation is originally due to 

* {#Dyson49} [[Freeman Dyson]], _The S Matrix in Quantum Electrodynamics_, Phys. Rev. 75: 1736 (1949) ([doi:10.1103/PhysRev.75.1736](https://doi.org/10.1103/PhysRev.75.1736))

* {#Schinger51} [[Julian Schwinger]], _On Green's functions of quantized fields I + II_, PNAS. 37: 452–459 (1951) ([doi:10.1073/pnas.37.7.452](https://doi.org/10.1073%2Fpnas.37.7.452))


The traditional informal account in terms of [[path integral]]-heuristics is reviewed for instance in

* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], section 15.1.4, 15.5.1, 15.5.3 of _[[Quantization of Gauge Systems]]_, Princeton University Press 1992. 

* {#Dermisek09} [[Radovan Dermisek]], _Schwinger-Dyson equations_, 2009  ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-II-4-4p.pdf))

A rigorous derivation in terms of [[BV-formalism]] in [[causal perturbation theory]]/[[pAQFT]] is provided in

* {#Rejzner16} [[Katarzyna Rejzner]], remark 7.7 _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

For discussion in the context of the [[master Ward identity]], see

* {#DuetschFredenhagen02} [[Michael Dütsch]], [[Klaus Fredenhagen]], _The Master Ward Identity and Generalized Schwinger-Dyson Equation in Classical Field Theory_, Commun.Math.Phys. 243 (2003) 275-314 ([arXiv:hep-th/0211242](https://arxiv.org/abs/hep-th/0211242))

See also

* Wikipedia, _[Schwinger-Dyson equation](https://en.wikipedia.org/wiki/Schwinger%E2%80%93Dyson_equation)_


Discussion of [[round chord diagrams]] organizing Dyson-Schwinger equations:

* Nicolas Marie, [[Karen Yeats]], *A chord diagram expansion coming from some Dyson-Schwinger equations*, Communications in Number Theory and Physics, 7(2):251291, 2013 ([arXiv:1210.5457](https://arxiv.org/abs/1210.5457))

* Markus Hihn, [[Karen Yeats]], *Generalized chord diagram expansions of Dyson-Schwinger equations*, Ann. Inst. Henri Poincar Comb. Phys. Interact. 6 no 4:573-605 ([arXiv:1602.02550](https://arxiv.org/abs/1602.02550))

Review in:

* Ali Assem Mahmoud, Section 3 of: *On the Enumerative Structures in Quantum Field Theory* ([arXiv:2008.11661](https://arxiv.org/abs/2008.11661))


[[!redirects Schwinger-Dyson equations]]

[[!redirects Dyson-Schwinger equation]]
[[!redirects Dyson-Schwinger equations]]

