


[[BO(n)|$B O(n)$]]



### Gravitino in 11d Supergravity

The [[Rarita-Schwinger equation|Rarita-Scwinger]]-like [[equation of motion]] for the [[gravitino]] in [[D=11 N=1 supergravity]] is (on any [[chart]])

\[
  \label{GravitinoEquationIn11dSugra}
  \Gamma^{a \, b_1 b_2}
  \,
  \rho_{b_1 b_2}
  \;=\;
  0
\]

(due to [Cremmer, Julia & Scherk 1978, p. 411](D=11+N=1+supergravity#CremmerJuliaScherk78), cf. [Castellani, D'Auria & Fré 1991, §III.8](D=11+N=1+supergravity#CastellaniDAuriaFré91), [p. 910](https://ncatlab.org/nlab/files/CastellaniDAuriaFre-ChIII8.pdf#page=24))

where

* $\rho_{b_1 b_2} \coloneqq \nabla_{[b_1} \psi_{b_2]}$ are the components of the [[field strength]] of the gravitino with respect to the [[frame field]] ([[vielbein]], which encodes the bosonic field of [[gravity]] in [[first-order formulation of gravity|first-order formulation]]): 

  for each value of the indices $b_i \in \{0, 1, \cdots, 10\}$ this is a [[smooth function]] from the chart to the [[real vector space]] [[underlying]] the [[irrep|irreducible]] [[real numbers|real]] [[representation]] $\mathbf{32}$ of [[pin group|$Pin^+(1,10)$]],

* $\Gamma^{a_1 a_2 a_3} \,\coloneqq\, \tfrac{1}{3!} \underset{\sigma \in Sym(3)}{\sum} sgn(\sigma) \Gamma^{a_{\sigma(1)}} \Gamma^{a_{\sigma(2)}} \Gamma^{a_{\sigma(3)}}$ is the skew-symmetrized product of three [[Clifford algebra]] [[linear basis|basis]] elements in the [[irrep|irreducible]] real [[representation]] $\mathbf{32}$ of [[pin group|$Pin^+(1,10)$]], acting pointwise on the component spinors of $\rho$,

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


***



## Idea

The *Stieltjes integral* can refer to two different [[integral|integrals]]: the [[Riemann-Stieltjes integral]] or the [[Lebesgue-Stieltjes integral]].

$$
\big( (x+2) \big)
$$

and

$$
  \int_{c' \in \mathcal{C}} 
  V\big(
    \mathcal{C}(c',c)
    ,\, F(c')
  \big) 
    \;\simeq\; 
  F(c)
  \,.
$$

## Related concepts

* [[integral]]
* [[Riemann integration]]
* [[Lebesgue integration]]

[[!redirects Stieltjes integrals]]