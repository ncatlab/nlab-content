
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called the _$\beta$-$\gamma$ system_ is a 2-dimensional [[quantum field theory]] defined on [[Riemann surfaces]] $X$ whose [[field (physics)|fields]] are pairs consisting of a $(0,0)$-form and a $(1,0)$-form and whose [[equations of motion]] demand these fields to be [[holomorphic differential forms]]. 

The name results from the traditional symbols for these fields, which are 

$$
  (\gamma,\beta) \in \Omega^{0,\bullet}(X) \oplus \Omega^{1, \bullet}(X)
  \,. 
$$


## Definition

We state the definition of the $\beta$-$\gamma$-system as a [[free field theory]] (see there) in [[BV-BRST formalism]], following ([Gwilliam, section 6.1](#Gwilliam)).

We first give the standard variant of the theory, the

* [Abelian massless theory](#AbelianMasslessTheory). 

Then we consider the

* [Abelian massive theory](#AbelianMassiveTheory)

* [Holomorphic Chern-Simons theory](#HolomorphicChernSimonsTheory)


### Abelian massless theory
 {#AbelianMasslessTheory}

Let $X$ be a [[Riemann surface]]. 

**[[kinematics]]**

* the [[field bundle]] $E \to X$ is

  $$
    E \coloneqq \wedge^{0,\bullet}\Gamma(T X) \oplus \wedge^{1,\bullet} \Gamma(T X)
  $$

* hence the ([[abelian sheaf|abelian]]) [[sheaf]] of [[local sections]] is

  $$
    \mathcal{E} = \Omega_X^{0,\bullet} \oplus \Omega_X^{1, \bullet}
    \,,
  $$

  we write

  $\mathcal{E}_c \hookrightarrow \Gamma_X(E)$

  for the sections of [[compact support]]

* the local pairing

  $$
    \langle -,-\rangle_{loc} \colon E \otimes E \to Dens_X
  $$

  with values in the [[density bundle]] is given by [[wedge product]] followed by projection on the $(1,1)$-forms

  $$
    \langle \gamma_1 + \beta_1, \gamma_2, \beta_2\rangle_{loc}
    \coloneqq
    (\gamma_1 \wedge \beta_2 + \gamma_2 \wedge \beta_1)_{|(1,1)}
  $$

* hence the global pairing
  
  $$
    \langle -,-\rangle \colon \mathcal{E}_c \otimes \mathcal{E}_c \to \mathbb{C}
  $$

  is given by

  $$
    \langle \gamma_1 + \beta_1, \gamma_2, \beta_2\rangle_{loc}
    \coloneqq
    \int_{X}\left(\gamma_1 \wedge \beta_2 + \gamma_2 \wedge \beta_1\right)
  $$

**[[dynamics]]**

* the [[differential operator]]

  $$
    Q \colon \mathcal{E} \to \mathcal{E}
  $$

  is the [[Dolbeault differential]] $\bar \partial$

* hence the [[elliptic complex]] of fields is

  $$
    (\mathcal{E}, Q) = (\Omega_X^{0,\bullet}\oplus \Omega_X^{1,\bullet}, \bar \partial)
  $$

  is the [[Dolbeault complex]];

* and hence the [[action functional]] 

  $$
    S \colon \mathcal{E}_c \to \mathcal{C}
  $$

  is

  $$
    \begin{aligned}
      (\gamma + \beta) & \mapsto  
     \frac{1}{2}\int_X \langle \gamma+ \beta, \; \bar \partial (\gamma + \beta)\rangle 
     \\
     & =  \int_X \beta \wedge \bar \partial \gamma
    \end{aligned}
  $$

### Abelian massive theory
 {#AbelianMassiveTheory}

(...)

### Holomorphic Chern-Simons theory
 {#HolomorphicChernSimonsTheory}

...[[holomorphic Chern-Simons theory]]...

## Properties

### Euler-Lagrange equations of motion

The [[equations of motion]] are

$$
  \bar \partial \gamma = 0
  \;\;,
  \;\;
  \bar \partial\beta = 0
  \,.
$$

## Relation with $\sigma$-models

Consider a [[sigma-model]] $X\hookrightarrow \mathbb{R}^{1,1}$ to the [[target space]] $\mathbb{R}^{1,1}$

$$ S[q,\gamma] = \int_X \partial q \wedge \bar{\partial}\gamma, $$

which has an abelian right-moving Kac-Moody symmetry $q\mapsto q+\lambda$ with $\partial\lambda=0$. We can can consider a theory where this symmetry is promoted to a [[gauge symmetry]], i.e.

$$ S_{\mathrm{gauged}}[q,\gamma] = \int_X \partial_\beta q \wedge \bar{\partial}\gamma, $$

where $\partial_\beta q := \partial q + \beta$ where $\beta\in\Omega^{1,\bullet}(X)$ is the [[connection]].
If we choose the gauge with $q=0$, we obtain the $\beta$-$\gamma$ system with action

$$ S_{\beta\gamma}[\beta,\gamma] = \int_X \beta \wedge \bar{\partial}\gamma. $$

Thus, a $\beta$-$\gamma$ system can be interpreted as a chiral (or Kac-Moody) quotient along a null killing vector of a [[sigma-model]] with target space $\mathbb{R}^{1,1}$ ([LinRoc20](#LinRoc20)).

## Related concepts

* [[pure spinor formalism]]

## References

### General

* [[Nikita Nekrasov]], _Lectures on curved beta-gamma systems, pure spinors, and anomalies_, ([hep-th/0511008](https://arxiv.org/abs/hep-th/0511008))

* [[Anton Zeitlin]], _Beta-gamma systems and the deformations of the BRST operator_, J.Phys. A42:355401 (2009) ([doi](https://doi.org/10.1088/1751-8113/42/35/355401) [arXiv/0904.2234](https://arxiv.org/abs/0904.2234))

Discussion in the context of [[BV-quantization]] and [[factorization algebras]] is in chapter 6 of

* [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([pdf](https://people.math.umass.edu/~gwilliam/thesis.pdf)) 
 {#Gwilliam}

A construction of [[chiral differential operator]]s via quantization of $\beta\gamma$ system in [[BV formalism]] with an intermediate step using factorization algebras:

* [[Vassily Gorbounov]], [[Owen Gwilliam]], Brian Williams, _Chiral differential operators via Batalin-Vilkovisky quantization_, [pdf](http://people.mpim-bonn.mpg.de/gwilliam/cdo.pdf)

* {#LinRoc20} [[Ulf Lindstrom]], [[Martin Rocek]], _$\beta$-$\gamma$-systems interacting with sigma-models_, ([arXiv:2004.06544](https://arxiv.org/abs/2004.06544v3))


### As a fractional level or logarithmic CFT

On the beta-gamma system as the [[su(2)|$\mathfrak{su}(2)$]] [[WZW model]] at fractional [[level (Chern-Simons theory)|level]] $-1/2$:

* {#LesageMathieuRasmussenSaleur02} F. Lesage, P. Mathieu, J. Rasmussen, H. Saleur, *The $\mathfrak{su}(2)_{-1/2}$ WZW model and the beta-gamma system*, Nucl. Phys. B **647** (2002) 363-403  $[$[arXiv:hep-th/0207201](https://arxiv.org/abs/hep-th/0207201), <a href="https://doi.org/10.1016/S0550-3213(02)00905-7">doi:10.1016/S0550-3213(02)00905-7</a>a$]$

and its lift to a [[logarithmic CFT]]:

* {#LesageMathieuRasmussenSaleur04} F. Lesage, P. Mathieu, J. Rasmussen, H. Saleur, *Logarithmic lift of the $\mathfrak{su}(2)_{-1/2}$ model*, Nuclear Physics B **686** 3 (2004) 313-346 &lbrack;[doi:10.1016/j.nuclphysb.2004.02.039](https://doi.org/10.1016/j.nuclphysb.2004.02.039)&rbrack;





