
#Contents#
* table of contents
{:toc}

## Fixing conventions and prefactors

$$
  \array{
  a = & 0 & 1 & 2 & 3 & 4 & 5
  \\
  \mu = & 0 & 1 & 2 & 3
  \\
  i = &  & 1 & 2 & 3
  }
$$

\linebreak

$$
  \begin{aligned}
    F
    & = \;
    \tfrac{1}{2} F_{\mu \nu} \, d x^\mu \wedge d x^\nu
    \\
    = d A
    & = \;
    \partial_{\mu} A_\mu \, dx^\mu \wedge dx^\nu
  \end{aligned}
$$

\linebreak

$$
  F_{\mu \nu}
  \;=\;
  \partial_\mu A_\nu - \partial_\nu A_\mu
$$

\linebreak

\[
  \label{FaradayInTermsOfEAndB}
  \begin{aligned}
    F
    \;=\;
    E_i \, d x^i \wedge d x^0
    \;+\;
    \tfrac{1}{2} B^i \epsilon_{i j k} \, d x^j \wedge d x^k
  \end{aligned}
\]

\linebreak


\[
  \label{FF}
  \begin{aligned}
    F \wedge F
    & =
    E_{l}  \tfrac{1}{2} B^i \epsilon_{i j k}
    d x^l \wedge d x^0 \wedge d x^j \wedge d x^{k}
    \\
    & =
    \tfrac{1}{2} E_l B^i \epsilon_{i j k} \epsilon^{j k l}
    \,
    \mathrm{dvol}
    \\
    & =
    E_i B^i \, \mathrm{dvol}
  \end{aligned}
\]

\linebreak


$$
  \begin{aligned}
    \star_{{}_4} F
    & =
    \tfrac{1}{2}
      (\star_{{}_4}F)_{\mu_1 \mu_2}
      \,
      d x^{\mu_1} \wedge d x^{\mu_2}
    \\
    & =
    \tfrac{1}{2}
    \epsilon_{\mu_1 \mu_2 \mu_3 \mu_4}
      F^{\mu_3 \mu_4}
      d x^{\mu_1} \wedge d x^{\mu_2}
  \end{aligned}
$$

\linebreak

$$
  \begin{aligned}
    (\star_{{}_4} F)^{\mu_1 \mu_2}
    & = \;
    \epsilon^{\mu_1 \mu_2 \mu_3 \mu_4}  F_{\mu_3 \mu_4}
    \\
  \end{aligned}
$$

\linebreak


$$
  \begin{aligned}
    F \wedge \star_{{}_4} F
    & = \;
    \tfrac{1}{2} F_{\mu_1 \mu_2}
    \tfrac{1}{2} F^{\kappa_1 \kappa_2}
    \epsilon_{\mu_3 \mu_4 \kappa_1 \kappa_2}
     d x^{\mu_1}
     \wedge
     d x^{\mu_2}
     \wedge
     d x^{\mu_3}
     \wedge
     d x^{\mu_4}
     \\
    & = \;
    \tfrac{1}{4}
    F_{\mu_1 \mu_2}
    F^{\kappa_1 \kappa_2}
    \epsilon_{\mu_3 \mu_4 \kappa_1 \kappa_2}
    \epsilon^{\mu_1 \mu_2 \mu_3 \mu_4}
    \,
    \mathrm{dvol}
    \\
    & = \;
    F_{\mu_1 \mu_2}
    F^{\mu_1 \mu_2}
    \,
    \mathrm{dvol}
  \end{aligned}
$$

\linebreak

## The super-exceptional correction term

\[
  \label{SECorrectionTerm}
  L_{\mathrm{corr}}
  \;:=\;
  f^\ast
  \Big(
    \big(\iota_{v_5} e_{a_1 a_2} (\wedge e^{a_1} \wedge e^{a_2})\big)
    \wedge
    \big(
      e_{a_1 a_2} \wedge e^{a_2 a_3} \wedge e_{a_3}{}^{a_1}
    \big)
  \Big)
  \wedge d x^5
\]

where 

$$
  H 
  \;:=\;
  f^\ast( e_{a_1 a_2} \wedge e^{a_1} \wedge e^{a_2}  )
  \;=\;
  F \wedge d x^5 - (\star_{{}_4} F) \wedge d x^4
$$

so that

$$
  \star_{{}_6} H \;=\; H
$$

\linebreak

## For constant field strengths

Consider constant field strength (eq:FaradayInTermsOfEAndB)

\[
  \label{ConstantFieldStrength}
  F
  \;=\;
  E_i \, d x^i \wedge d x^0
  \;+\;
  \tfrac{1}{2} B^i \epsilon_{i j k} \, d x^j \wedge d x^k
  \,,
  \phantom{AAA}
  d E_i = 0
  \,,\;\;
  d B^i = 0
\]

\linebreak

One choice of vector potential for this is

$$
  A 
  \;:=\;
  E_i x^i \, d x^0
  +
  \tfrac{1}{2}
  B^i x^j \epsilon_{i j k} d x^k
  \,.
$$

\linebreak

$$
  A_a 
  \;=\;
  E_i x^i \delta^0_a
  +
  \tfrac{1}{2}
  B^i x^j \epsilon_{i j a} 
$$

\linebreak


Take

$$
  f^\ast(e_{a_1 a_2})
  \;\coloneqq\;
  d (A_{[a_1}) \delta^{5}_{a_2]} 
  +
  d(
    (\star_{{}_4} F)_{a_1 a_2}
    x^4
  )
$$

Then the super-exceptional correction term \eqref{SECorrectionTerm} is:


$$
  \begin{aligned}
  &
  - F_{\mu_1 \mu_2} dx^{\mu_1} \wedge dx^{\mu_2}
  \wedge
  f^\ast
  \big(
    e_{a_1 a_2}\wedge e^{a_2 a_3}\wedge e_{a_3}{}^{a_1}
  \big)
  \wedge dx^5
  \\
  & = 
  6
  \, 
  F_{\mu_1 \mu_2} dx^{\mu_1} \wedge dx^{\mu_2}
  \wedge 
  (\partial_{\mu_3} A_{\nu_1}) \, d x^{\mu_3}
  \wedge
  (\partial_{\mu_4} A_{\nu_2}) \, d x^{\mu_4}
  \wedge
  (\star_{{}_4} F)^{\nu_1 \nu_2} \, d x^4
  \,
  \wedge dx^5
  \\
  & =
  6
  \,
  \epsilon^{\mu_1 \mu_2 \mu_3 \mu_4}
  F_{\mu_1 \mu_2}  
  (\partial_{\mu_3} A_{\nu_1})
  (\partial_{\mu_4} A_{\nu_2})
  F_{\nu_3 \nu_4}
  \epsilon^{\nu_1 \nu_2 \nu_3 \nu_4}
  \;
  \mathrm{dvol}_6
  \\
  & =
  12
  \,
  \epsilon^{\mu_1 \mu_2 \mu_3 \mu_4}
  F_{\mu_1 \mu_2}
  (\partial_{\mu_3} A_{j'})
  (\partial_{\mu_4} A_{k'})
  F_{0 i'}
  \epsilon^{i' j' k'}
  \,
  \mathrm{dvol}_6
  \\
  & =
  24
  \,
  \big(
  \epsilon^{i j k}
  F_{0 i}
  (\partial_{j} A_{j'})
  (\partial_{k} A_{k'})
  F_{0 i'}
  \epsilon^{i' j' k'}
  +
  \epsilon^{i j k}
  F_{i j}
  \underset{
    = 0
  }{
  \underbrace{
  (\partial_{0} A_{j'})
  }
  }
  (\partial_{k} A_{k'})
  F_{0 i'}
  \epsilon^{i' j' k'}
  \big)
  \,
  \mathrm{dvol}_6
  \\
  & =
  24
  \,
  \epsilon^{ijk}
  \,
  E_i
  \,
  \epsilon_{j j' j'' } B^{j''}
  \,
  \epsilon_{k k' k''} B^{k''}
  \,
  E_{i'}
  \,
  \epsilon^{i' j' k'}
  \,
  \mathrm{dvol}_6
  \\
  & =
  24
  \,
  \big(
  \delta^i_{j''}\delta^{k}_{j'}
  \,
  E_i
  \,
  B^{j''}
  \,
  \epsilon_{k k' k''} B^{k''}
  \,
  E_{i'}
  \,
  \epsilon^{i' j' k'}
  -
  \delta^i_{j'}\delta^{k}_{j''}
  \,
  E_i
  \,
  B^{j''}
  \,
  \epsilon_{k k' k''} B^{k''}
  \,
  E_{i'}
  \,
  \epsilon^{i' j' k'}
  \big)
  \,
  \mathrm{dvol}_6
  \\
  & =
  24
  \,
  \big(
  E_i
  \,
  B^{i}
  \,
  \epsilon_{k k' k''} B^{k''}
  \,
  E_{i'}
  \,
  \epsilon^{i' k k'}
  -
  \,
  E_i
  \,
  B^{k}
  \,
  \epsilon_{k k' k''} B^{k''}
  \,
  E_{i'}
  \,
  \epsilon^{i' i k'}
  \big)
  \\
  & =
  24
  \,
  \big(
  E_i
  \,
  B^i
  \,
  2 \delta^{i'}_{k''}
  \,
  B^{k''}
  \,
  E_{i'}
  \,
  -
  \,
  \underset{
    = 0
  }{
  \underbrace{
  ( \delta^i_k \delta^{i'}_{k''}
  - \delta^i_{k''} \delta^{i'}_{k})
  \,
  E_i
  \,
  B^{k}
  \,
  B^{k''}
  \,
  E_{i'}
  \,
  \big)
  }
  }
  \\
  & =
  48
  \,
  (E\cdot B)^2
  \,
  \mathrm{dvol}_6
  \\
  & =
  48
  \,
  (( F \wedge F )/\mathrm{dvol}_4)^2
  \,
  \mathrm{dvol}_6
  \end{aligned}
$$

In the last line we used (eq:FF).

\linebreak

This proves that, at least in the special case of 
constant field-strength, the super-exceptional correction term
is proportional to the first DBI-correction term.

\linebreak

