+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] the term _gravitino_ refers to the [[supersymmetry|superpartner]] of the [[graviton]], a [[Rarita-Schwinger field]] of [[spin]] $3/2$ that appears in [[supergravity]].

In [[supergravity]] a [[field history]] is a [[connection on a bundle|connection]] on [[super spacetime]] locally given by a  [[super Lie algebra|super]] [[Lie algebra-valued differential form]]

$$
  (E, \Omega, \Psi) \,\colon\, T X \longrightarrow \mathfrak{iso}\big(\mathbb{R}^{1,10\vert \mathbf{32}}\big)
$$

on [[spacetime]] with values in the [[super Poincaré Lie algebra]]. Its components $\Psi$ in the [[spin representation]] 
$\mathbf{32} \subset
\mathfrak{iso}\big(\mathbb{R}^{1,10\vert \mathbf{32}}\big)
$
is the **gravitino** field.

The name derives from the fact that the other two components are identified in [[gravity]] with the [[graviton]] field.


## Examples

### Gravitino in 11d Supergravity
 {#GravitinoIn11dSugra}

The [[Rarita-Schwinger equation|Rarita-Scwinger]]-like [[equation of motion]] for the [[gravitino]] in [[D=11 N=1 supergravity]] is (on any [[chart]])

\[
  \label{GravitinoEquationIn11dSugra}
  \Gamma^{a \, b_1 b_2}
  \,
  \rho_{b_1 b_2}
  \;=\;
  0
\]

(due to [Cremmer, Julia & Scherk 1978, p. 411](D=11+N=1+supergravity#CremmerJuliaScherk78), cf. [Castellani, D'Auria & Fré 1991, §III.8](D=11+N=1+supergravity#CastellaniDAuriaFré91), [p. 910](https://ncatlab.org/nlab/files/CastellaniDAuriaFre-ChIII8.pdf#page=24)),

where

* $\rho_{b_1 b_2}$ are the bosonic [[frame field]] components of the gravitino [[field strength]]:

  $$
    \mathrm{d}\, \Psi
    -
    \!\tfrac{1}{4}
    \omega^{a b}
    \Gamma_{a b}
    \psi
    \;=\;
    \rho_{b_1 b_2}
    E^{b_1} E^{b_2}
    +
    (\cdots)
    \Psi E
    \,,
  $$ 

  So for each value of the indices $b_i \in \{0, 1, \cdots, 10\}$ this is a [[smooth function]] from the chart to the [[real vector space]] [[underlying]] the [[irrep|irreducible]] [[real numbers|real]] [[representation]] $\mathbf{32}$ of [[pin group|$Pin^+(1,10)$]],

* $\Gamma^{a_1 \cdots a_p} \,\coloneqq\, \tfrac{1}{p!} \underset{\sigma \in Sym(p)}{\sum} sgn(\sigma) \Gamma^{a_{\sigma(1)}} \cdots \Gamma^{a_{\sigma(p)}}$ is the skew-symmetrized product of $p$ [[Clifford algebra]] [[linear basis|basis]] elements in the [[irrep|irreducible]] real [[representation]] $\mathbf{32}$ of [[pin group|$Pin^+(1,10)$]], 

  here acting pointwise on the component spinors of $\rho$,

* the [[Einstein summation convention]] implies summation over repeated indices.

\begin{prop}
**(implications of 11d gravitino equation)**

We have the following implications of the gravitino equation   $\Gamma^{a b_1 b_2} \rho_{b_1 b_2} \;=\; 0$
(eq:GravitinoEquationIn11dSugra) in [[D=11 supergravity]]:

\[
  \label{FirstImplicationOf11dGravitinoEquation}
  \Gamma^{b_1 b_2} \, \rho_{b_1 b_2} \;=\; 0
\]

\[
  \label{SecondImplicationOf11dGravitinoEquation}
  \Gamma^{b_1} \, \rho_{b_1 b_2} \;=\; 0
\]

\[
  \label{ThirdImplicationOf11dGravitinoEquation}
  \Gamma^{a a'} \, \rho_{a' b} \;=\; - \rho^a{}_b
\]

\[
  \label{FourthImplicationOf11dGravitinoEquation}
  \Gamma_{\!c_1 c_2}{}^{ b_1 b_2 } \rho_{b_1 b_2}
  \;=\;
  -
  2\rho_{c_1 c_2}
  \,.
\]

\end{prop}

\begin{proof}
Equation (eq:FirstImplicationOf11dGravitinoEquation) follows immediately by Clifford contraction:
$$
  \Gamma_{\!a} \Gamma^{a b_1 b_2} \,\rho_{b_1 b_2}
  \;=\;
  9 \, \Gamma^{b_1 b_2} \,\rho_{b_1 b_2}
$$

Equation (eq:SecondImplicationOf11dGravitinoEquation) follows by the contraction
$$
  \begin{array}{l}
    \Gamma_{\!c a} \Gamma^{a b_1 b_2} \, \rho_{b_1 b_2}
    \;=\;
    18 \, \Gamma^{b} \rho_{ c b }
    \;+\;
    8 \, \Gamma^{c b_1 b_2} \rho_{b_1 b_2}
  \end{array}
$$
and using that the second summand vanishes by assumption (eq:GravitinoEquationIn11dSugra).

For equation (eq:ThirdImplicationOf11dGravitinoEquation) we compute as follows:
$$
  \begin{array}{l}
    \Gamma^{a a'}\rho_{a' b}
    \\
    \;=\;
    \tfrac{1}{2}
    \big(
      \Gamma^a \Gamma^{a'} \rho_{a' b}
      -
      \Gamma^{a'} \Gamma^a \rho_{a' b}
    \big)
    \\
    \;=\;
    -
    \tfrac{1}{2}
    \Gamma^{a'} \Gamma^a \rho_{a' b}
    \\
    \;=\;
    \tfrac{1}{2}
    \Gamma^a \Gamma^{a'} \rho_{a' b}
    -
    \eta^{a a'} \rho_{a' b}
    \\
    \;=\;
    -\rho^a{}_b
    \,,
  \end{array}
$$
where in the second and fourth step we used (eq:SecondImplicationOf11dGravitinoEquation).

For (eq:FourthImplicationOf11dGravitinoEquation) we consider this contraction:

$$
  \begin{array}{l}
  \Gamma_{c_1 c_2 a}
  \Gamma^{a b_2 b_3}
  \rho_{b_2 b_3}
  \\
  \;=\;
  16 \Gamma_{c_1}{}^{b} \rho_{c_2 b}
  -
  16 \Gamma_{c_2}{}^{b} \rho_{c_1 b}
  -
  18 \rho_{c_1 c_2}
  +
  7
  \Gamma_{c_1 c_2}{}^{ b_1 b_2 } \rho_{b_1 b_2}
  \\
  \;=\;
  16 \rho_{c_1 c_2}
  -
  16 \rho_{c_2 c_1}
  -
  18 \rho_{c_1 c_2}
  +
  7
  \Gamma_{c_1 c_2}{}^{ b_1 b_2 } \rho_{b_1 b_2}
  \\
  \;=\;
  14 \rho_{c_1 c_2}
  +
  7
  \Gamma_{c_1 c_2}{}^{ b_1 b_2 } \rho_{b_1 b_2}
  \,,
  \end{array}
$$
where in the second step we used (eq:ThirdImplicationOf11dGravitinoEquation).
\end{proof}

## Related concepts

* [[gravitino condensation]]


## References

### General

See also

* Wikipedia, _[Gravitino](https://en.wikipedia.org/wiki/Gravitino)_

[[!include classification of long-range forces -- references]]


### As a dark matter candidate
 {#AsDarkMatterCandidate}

#### General

Discussion of the gravitino as a [[dark matter]] candidate:

* {#EllisOlive10} [[John Ellis]], [[Keith Olive]], _Supersymmetric Dark Matter Candidates_ ([arXiv:1001.3651](http://arxiv.org/abs/1001.3651))

#### Via $E_{10}$
 {#ViaE10AsDarkMatterCandidate}

{#NicolaiMeissner} A proposal for super-heavy [[gravitinos]] as [[dark matter]], by embedding [[D=4 N=8 supergravity]] into [[E10]]-[[U-duality]]-invariant [[M-theory]] (see [there](E10#StandardModelPhenomenology) for the corresponding [[standard model of particle physics|standard model]] [[phenomenology]]):

* {#MeissnerNicolai18a} [[Krzysztof A. Meissner]], [[Hermann Nicolai]]: *Standard Model Fermions and Infinite-Dimensional R-Symmetries*, Phys. Rev. Lett. **121** 091601 (2018) &lbrack;[arXiv:1804.09606](https://arxiv.org/abs/1804.09606), [doi:10.1103/PhysRevLett.121.091601](https://doi.org/10.1103/PhysRevLett.121.091601)&rbrack;

* {#MeissnerNicolai18b} [[Krzysztof A. Meissner]], [[Hermann Nicolai]], _Planck Mass Charged Gravitino Dark Matter_, Phys. Rev. D 100, 035001 (2019) ([arXiv:1809.01441](https://arxiv.org/abs/1809.01441))

following the proposal towards the end of

* {#GellMann83} [[Murray Gell-Mann]], introductory talk at _[Shelter Island II](https://en.wikipedia.org/wiki/Shelter_Island_Conference)_ (1983) ([[Gell-Mann_ShelterIslandII_1983.pdf:file]]) 

  in: _Shelter Island II: Proceedings of the 1983 Shelter Island Conference on Quantum Field Theory and the Fundamental Problems of Physics_. MIT Press (1985) 301-343 \[ISBN:0-262-10031-2\]

Further discussion:

* [[Krzysztof A. Meissner]], [[Hermann Nicolai]], _Supermassive gravitinos and giant primordial black holes_ ([arXiv:2007.11889](https://arxiv.org/abs/2007.11889))

* [[Krzysztof A. Meissner]], [[Hermann Nicolai]], *Evidence for a stable supermassive gravitino with charge $2/3$?* &lbrack;[arXiv:2303.09131](https://arxiv.org/abs/2303.09131)&rbrack;

* Adrianna Kruk, Michał Lesiuk, [[Krzysztof A. Meissner]], [[Hermann Nicolai]]: *Signatures of supermassive charged gravitinos in liquid scintillator detectors* &lbrack;[arXiv:2407.04883](https://arxiv.org/abs/2407.04883)&rbrack;





[[!redirects gravitinos]]
