

\linebreak


electron density (number of electrons per surface area) in Landau level

$$
  d
  \;=\;
  \frac{
    e B 
  }{
    h
  }
$$

Hence with $n$ the given charge densite, the magnetic field value at which the $i$th Landau level is exactly filled,
$$
  n = i d
$$
is
$$
  B_i
  \;=\;
  \frac{
    n h
  }{e}
  \tfrac{1}{i}
$$


\linebreak

### Abelian Chern-Simons as EFT for FQH

The following is a streamlined digest of the traditional argument and Ansatz &lbrack;[Zee 1995](#Zee95), [Wen 1995](#Wen95), [Witten 2016 pp 30](#Witten16), [Tong 2016 §5](#Tong16)&rbrack; for [[abelian Chern-Simons theory]] at [[level (Chern-Simons theory)|level]] $k \in \mathbb{N}$ as an [[effective field theory]] for [[fractional quantum Hall systems]] at filling fraction $\nu = 1/k$.


\linebreak


**Preliminaries.**
Our [[spacetime]] $\Sigma$ has dimension $1 + 2$, to be thought of as the [[worldvolume]] of the conducting sheet that hosts the [[fractional quantum Hall system]].

On this spacetime, the electric [[current density]] is a [[differential 2-form]] $J$.

Note that the corresponding electric current [[vector field]] $\vec J$ is characterized by its [[tensor contraction|contraction]] into the given [[volume form]] $dvol$ being equal to the density 2-form

$$
  J \;=\; dvol\big(\, \vec J, \cdots \big)
  \,,
$$

and that the conservation law for $\vec J$, hence the vanishing of its [[divergence]] is equivalent to the density 2-form being [[closed differential form]]:

\[
  \label{CurrentConservationLaw}
  div \vec J \;=\; 0
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \mathrm{d} J \;=\; 0
  \,.
\]

We write $A$ for the [[vector potential]] 1-form on $\Sigma$ which encodes the [[background field|background]] [[electromagnetic field]], and $F \,=\, \mathrm{d}A$ for its [[field strength]], the [[Faraday tensor]]. Since we regard this as a fixed [[background field]], we do not (need to) consider the Maxwell [[Lagrangian density]] $L_{YM} \,\coloneqq\, F \wedge \star F$.

But we do (need to) consider the interaction term between the electromagnetic field and the electric current density, which is 

\[
  \label{ElectricInteractionTerm}
  L_{int} \,\coloneqq\, A \wedge J
  \,.
\]

Here we assume that $A$ is globally defined, in fact we shall assume that $\Sigma$ has vanishing [[de Rham cohomology]] in degree=2,

\[
  \label{AssumingdeRham2CohomologyVanishes}
  H^2_{dR}(\Sigma) \;=\; 0
  \,.
\]

This means we are focused on the local nature of fields, not on their global properties, as (for better or worse) usual for [[Lagrangian field theory]].
 
\linebreak

**The auxiliary gauge potential.**
With the assumption (eq:AssumingdeRham2CohomologyVanishes) also the conserved current density (eq:CurrentConservationLaw) admits a [[coboundary]], a [[differential 1-form]] to be denoted $a$:

$$
  J \,=\, \mathrm{d}a
  \,.
$$

The central Ansatz of the approach is to *think of this 1-form as an effective dynamical gauge field for the FQH dynamics*.

\linebreak

**The Lagrangian density.** This in turn suggests that the effective [[Lagrangian density]] should be the sum of

1. the interaction term (eq:ElectricInteractionTerm) already mentioned, which thus specializes to

   $$
     L_{int} \;=\; A \wedge J \;=\; A \wedge \mathrm{d}a
     \,,
   $$

1. a further interaction term for $a$, now regarded as a gauge potential, to its own current density $j$, to be thought of as the current of FQH [[quasi-particles]] (or quasi-holes)

   $$
     L_{quas} \;=\; a \wedge j
   $$

1. a dynamical term for $a$ itself, where the only sensible choice is the [[Chern-Simons theory|Chern-Simons form]] at [[level (Chern-Simons theory)|level]] $k$

   $$
     L_{CS} \;=\; k \tfrac{1}{2} a \wedge \mathrm{d}a
     \,.
   $$

In total, the traditional Ansatz for the effective Lagrangian density for "single layer" FQH systems at filling fraction $1/k$ is hence:

\[
  \label{TheEffectiveLagrangianDensity}
  L 
  \,\coloneqq\,
  k \tfrac{1}{2}\, a\wedge \mathrm{d}a
  \,-\,
  A \wedge 
  \underset{J}{
    \underbrace{
      \mathrm{d}a
    }
  }
  \,+\,
  a \wedge j
  \,.
\]

&lbrack;[Wen 1995 (2.11)](#Wen95)&rbrack;

\linebreak

**The equation of motion.**
The [[Euler-Lagrange equation]] [[equation of motion|of motion]] for the effective gauge field $a$ induced by (eq:TheEffectiveLagrangianDensity) is simply

\[
  \label{EquationOfMotion}
  \frac{\delta L}{\delta A}
  \;=\;
  0
  \;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;
  J
    \,=\,
  \tfrac{1}{k}\Big(
    F - j
  \Big)
  \,.
\]

> (This means in particular that if, on topologically non-trivial $\Sigma$, one wants to subject the effective gauge field $a$ to [[Dirac charge quantization]] then the ordinary electromagnetic field must be assumed to carry magnetic charge being a multiple of $k$.)

\linebreak

**Recovering the Hall conductivity.**
The first plausibility check on the effective model is to observe that its equation of motion (eq:EquationOfMotion) implies the correct Hall conductivity relation for a [[fractional quantum Hall system]] at filling fraction $1/k$:

Namely assuming that the electric field is oriented in the $y$-direction, so that the [[Faraday tensor]] is of the form (cf [there](Maxwell's+equations#InTermsOfFaradayTensor)):

$$
  F 
  \;=\;
  E_y \mathrm{d}t \wedge \mathrm{d}y
  +
  B \mathrm{d}x\wedge \mathrm{d}y
$$

and assuming that the quasi-particles are stationary, so that 

$$
  j 
    \;\propto\; 
  dvol(\partial_0) \propto \mathrm{d}x \wedge \mathrm{d}y
$$

the temporal component of the equation of motion (eq:EquationOfMotion) becomes

$$
  J_x \;=\; \tfrac{1}{k} E_y
$$

which is the correct form of the *Hall field* $E_y$ for given longitudinal current $J_X$ at filling fraction $1/k$.

> (Following [Zee 1995 (4.5)](#Zee95), later authors &lbrack;[Witten 2016 §2.3](#Witten16), [Tong 2016 p 161](#Tong16)&rbrack; deduce this in a more roundabout way, by first inserting the equation of motion back into the Lagrangian density and then varying that with respect to $A$. It seems that this unnecessary step is brought about by first tacitly renaming "$J$" to "$f$" and then forgetting that this was just a renaming.)

\linebreak

**Recovering the fractional quasi-particles.**
Second, the spatial component of the equation of motion (eq:EquationOfMotion) says that (1.) the magnetic flux quanta and (2.) the quasi-particles contribute their $k$th fraction to the total charge density:

$$
  J_0 \;=\; \tfrac{1}{k}(B - j_0)
  \,.
$$

Here 

* statement (1) reflects exactly the composite fermion model, where at $k$th filling fraction each electron is bound to $k$ quanta of magnetic flux 

* statement (2) is the desired property of quasi-holes to have $k$th fractional charge.


\linebreak

This largely concludes the traditional justification for the effective abelian Chern-Simons theory (eq:TheEffectiveLagrangianDensity).


\linebreak



## Loop space of the 2-sphere

* [[Frederick R. Cohen]], J. Wu: *On Braid Groups, Free Groups, and the Loop Space of the 2-Sphere*, in: *Categorical Decomposition Techniques in Algebraic Topology*, in *Progress in Mathematics* **215**,  Birkhäuser (2003) 93-105  \[<a href="https://doi.org/10.1007/978-3-0348-7863-0_6">doi:10.1007/978-3-0348-7863-0_6</a>\]
