


## 11d-SuGra from Super C-Field Flux Quantization
 {#11DSugraFromSuperCFieldFluxQuantization}

We discuss (Thm. \ref{11dSuGraEOMFromSuperFluxIdentity} below, following [[schreiber:Super-Flux Quantization of 11d Supergravity|GSS24]]) how the [[equations of motion]] of [[D=11 supergravity]] --- on an $11\vert\mathbf{32}$-dimensional [[super-torsion]]-free [[super spacetime]] $X$ with  [[super vielbein]] $(e,\psi)$ (the [[graviton]]/[[gravitino]]-[[field (physics)|fields]]) --- follow from just the requirement that the [[duality-symmetric higher gauge theory|duality-symmetric]] [[differential form on a supermanifold|super-]][[supergravity C-field|C-field]] [[flux densities]] $(G_4^s, G_7^s) \,\in\, \Omega^4_{dR}(X) \times \Omega^7_{dR}(X)$:

1. satisfy their [[Bianchi identities]]

   \[
     \label{SuperFluxBianchiIdentity}
     \begin{array}{l}
       \mathrm{d} \, G_4^s \;=\; 0 
       \\
       \mathrm{d} \, G_7^s \;=\; \tfrac{1}{2} G_4^s \, G_4^s
     \end{array}
   \]

1. are on any super-[[chart]] $U \hookrightarrow X$ of the locally supersymmetric form

   \[
     \label{LocalFormOfSuperFluxDensities}
     \begin{array}{l}
       G_4^s 
       \;=\;
       \tfrac{1}{4!}
       (G_4)_{a_1 \cdots a_4}
       e^{a_1} \cdots e^{a_4}
       \,-\,
       \tfrac{1}{2}
       \big(\overline{\psi}\Gamma_{a_1 a_2} \psi\big)
       e^{a_1} \, e^{a_2}
       \\
       G_7^s 
       \;=\;
       \tfrac{1}{7!}
       (G_7)_{a_1 \cdots a_7}
       e^{a_1} \cdots e^{a_7}
       \,-\,
       \tfrac{1}{5!}
       \big(\overline{\psi}\Gamma_{a_1 \cdots a_5} \psi\big)
       e^{a_1} \cdots e^{a_5}
       \mathrlap{\,.}
     \end{array}
   \]

Up to some mild (but suggestive, see below) re-arrangement, the computation is essentially that indicated in [CDF91, §III.8.5](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) (and apparently nowhere else), and the following may be understood as an exposition of this result, which seems to stand out as the only account that is (i) fully [[first-order formulation of gravity|first-order]] and (ii) [[duality-symmetric higher gauge theory|duality-symmetric]] (in that $G_7$ enters the [[equation of motion|EoMs]] as an independent field, whose [[Hodge duality]] to $G_4$ is imposed  *by the [[Bianchi identity]]* for $G_7^s$, remarkably). 

Notice that the discussion in [CDF91, §III.8](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) amplifies the [[superspace]]-[rheonomy principle](D'Auria-Fre+formulation+of+supergravity#Rheonomy) as a constraint that makes the Bianchi identities on (in our paraphrase) a [[supergravity Lie 6-algebra]]-[[L-infinity algebra valued differential form|valued]] higher vielbein be equivalent to the [[equations of motion]] of [[D=11 SuGra]].
But we may observe that the only rheonomic *constraint* necessary is that (eq:LocalFormOfSuperFluxDensities) on the [[supergravity C-field|C-field]] [[flux density]] --- and this is the one not strictly given by rules in [CDF91, p. 874](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre), cf. around [CDF91, (III.8.41)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) ---; while the remaining rheonomy condition on the [[gravitino]] [[field strength]] $\rho$ is *implied* (Lem. \ref{SuperBianchiIdentityOnG4InComponents} below), and the [all-important](torsion+constraints+in+supergravity#Examples11dSuGra) [[torsion constraints in supergravity|torsion constraint]] (eq:TorsionConstraint) (which is also outside the rules of rheonomy constraints, cf. [CDF91, (III.8.33)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre)) is naturally regarded as part of the definition of a [[super-spacetime]] in the first place (Def. \ref{SuperSpacetime} below). 


In thus recasting the formulation of the theorem somewhat, we also:

1. re-define the super-flux densities as above (eq:LocalFormOfSuperFluxDensities), highlighting that it is (only) in this combination that the algebraic form of the expected [[Bianchi identity]] (eq:SuperFluxBianchiIdentity) extends to [[superspace]];

1. disregard the [[gauge potentials]] $C_3$ and $C_6$, whose role in [CDF91, §III.8.2-4](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) is really just to motivate the form of the [[Bianchi identities]] equivalent to (eq:SuperFluxBianchiIdentity), but whose global nature is more subtle than acknowledged there, while being irrelevant for just the [[equations of motion]].

Indeed, the point is that, in consequence of our second item above, the following formulation shows that one may apply [[flux quantization]] of the [[supergravity C-field]] on [[superspace]] in formally the same way as bosonically (for instance in [[Cohomotopy]] as per *[[schreiber:Hypothesis H]]*, or in any other [[nonabelian cohomology theory]] whose [[classifying space]] has the $\mathbb{Q}$-[[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] [[rational n-sphere|of the]] [[4-sphere]]), and in fact that the ability to do so *implies* the [[equations of motion|EoMs]] of [[D=11 supergravity|11d SuGra]].
Any such choice of [[flux quantization]] is then what defines, conversely, the [[gauge potentials]], globally. Moreover, by the fact brought out here, that the super-flux Bianchi identity already implies the full equations of motion, this flux quantization is thereby seen to be compatible with the equations of motion on all of [[super spacetime]].

\linebreak

For the present formulation, we find it suggestive to regard the [all-important](torsion+constraints+in+supergravity#Examples11dSuGra) [[torsion constraints in supergravity|torsion constraint]] (eq:TorsionConstraint) as part of the definition of the super-gravity field itself (since it ties the auxiliary [[spin-connection]] to the [[super-vielbein]] field which embodies the actual super-metric structure):

\begin{definition}\label{SuperSpacetime}
**(super-spacetime)**
\linebreak
For 

* $D \in \mathbb{N}_{\geq 1}$ a [[natural number]] 

* $\mathbf{N} \in Rep_{\mathbb{R}}\big(Spin(1,D-1)\big)$ a [[real numbers|real]] [[spin representation]] ("[[Majorana spinors]]") of $\mathbb{R}$-[[dimension of a vector space|dimension]] $N$

   whose [[spin group|$Spin(1,D)$]]-[[equivariant map|equivariant]] [[bilinear map|bilinear]] pairing we denote

   $$
     \overline{(\text{-})}(\text{-})
     \;\colon\;
     \mathbf{N} \otimes \mathbf{N}
     \longrightarrow
     \mathbb{R}^{1,D-1}
     \,,
   $$

by a *[[super-spacetime]]* of super-dimension $D\vert \mathbf{N}$ we here mean:

1. a [[supermanifold]] 

1. which admits an [[open cover]] by [[super-Minkowski spacetime|super-Minkowski]] supermanifolds $\mathbb{R}^{1,D-1\vert \mathbf{N}}$,

1. equipped with a [[super Cartan geometry|super]] [[Cartan connection]] with respect to the canonical subgroup inclusion $Spin(1,D-1) \hookrightarrow Iso(\mathbb{R}^{1,D-1\vert\mathbf{N}})$ of the [[spin group]] into the [[super Poincaré group]], namely:

   1. equipped with a [[super-vielbein]] $(e, \psi)$, hence on each super-chart $U \hookrightarrow X$ 

      $$
        \big(
          (e^a)_{a=0}^{D=1}
          ,\,
          (\psi^\alpha)_{\alpha=1}^N
        \big)
        \;\in\;
        \Omega^1_{dR}\big(
          U
          ;\,
          \mathbb{R}^{1,D-1\vert \mathbf{N}}
        \big)
      $$ 

      such that at every point $x \in \overset{\rightsquigarrow}{X}$ the induced map on [[tangent spaces]] is an [[isomorphism]]

      $$
        (e,\psi)_x \;\colon\;
        T_x X
        \overset{\sim}{\longrightarrow}
        \mathbb{R}^{1,10\vert \mathbf{N}}
        \,.
      $$

   1. and with a [[spin-connection]] $\omega$ (...),

1. such that the [[super-torsion]] vanishes, in that on each chart:

   \[
     \label{TorsionConstraint}
     \mathrm{d} \, e^a 
     -
     \omega^a{}_b \, e^b 
     \;=\;
     \big(
       \overline{\psi}
       \,\Gamma^a\,
       \psi
     \big)
     \,,
   \]

   where $\Gamma^{(-)} \,\colon\, \mathbb{R}^{1,D-1} \longrightarrow End_{\mathbb{R}}(\mathbf{N})$ is a [[representation]] of [[pin group|$Pin^+(1,10)$]], hence

   $$
     \Gamma_{a} \Gamma_b
     + 
     \Gamma_{b} \Gamma_a
     \;=\;
     + 2\, diag(-, +, +, \cdots, +)_{a b}
     \,.
   $$
 
\end{definition}

\begin{definition}\label{GravitationalFieldStrengths}
**(the gravitational [[field strength]])**
\linebreak
Given a [[super-spacetime]] (Def. \ref{SuperSpacetime}), we say that (super chart-wise):

1. its *[[super-torsion]]* is:

   $$
    T^a 
      \;\coloneqq\;
     \mathrm{d}\, e^a
     \,-\,
     \omega^a{}_b \, e^b
     \,-\,
     \big(
       \overline{\psi}\Gamma^a\psi
     \big)
   $$

1. its *[[gravitino]] [[field strength]]* is

   $$
     \rho
     \;\coloneqq\;
     \mathrm{d}\, \psi
     +
     \tfrac{1}{4} \omega_{a b}\Gamma^{a b}\psi
     \,,
   $$

1. its *[[curvature]]* is

   $$
     R^{a}{}_b
     \;\coloneqq\;
     \mathrm{d}\, \omega^{a}{}_b
     \,-\,
     \omega^a{}_c \, \omega^c{}_b
     \,.
   $$

\end{definition}

\begin{lemma}
**(super-gravitational Bianchi identities)**
\linebreak
By [[exterior calculus]] the gravitational [[field strength]] [[tensors]] (Def. \ref{GravitationalFieldStrengths}) satisfy the following [[identities]]:

\[
  \label{GravitationalBianchiIdentities}
  \begin{array}{ccl}
    \mathrm{d}
    \,
    R^{a}{}_b
    &=&
    \omega^a{}_{a'} \, R^{a'}{}_b
    -
    R^{a}{}_{b'}
    \,
    \omega^{b'}{}_{b}
    \\
    \mathrm{d}
    \,
    T^a 
    &=&
    - R^{a}{}_b \ e^b
    +
    2
    \big(
      \overline{\psi}
      \,\Gamma^a\,
      \rho
    \big)
    \\
    \mathrm{d}
    \,
    \rho
    &=&
    \tfrac{1}{4}
    R^{a b} \Gamma_{a b} \psi
  \end{array}
\]

\end{lemma}

\begin{remark}
**(role of the gravitational Bianchi identities)**
\linebreak
  Notice that the equations (eq:GravitationalBianchiIdentities) are not conditions but identities satisfied by any [[super-spacetime]] (in the sense of Def. \ref{SuperSpacetime}, hence even such that $T^a = 0$.) But conversely this means that when *constructing* a super-spacetime (say subject to further contraints, such as [[Bianchi identities]] for [[flux densities]]), the equations (eq:GravitationalBianchiIdentities) are a *necessary condition* to be satisfied by any *candidate* [[super-vielbein]]-field, and as such they may play the role of [[equations of motion]] for the [[supergravity|super-gravitational]] [[field (physics)|field]], as we will see.
\end{remark}

\linebreak

Write now $\mathbf{32} \in Rep_{\mathbb{R}}\big(Spin(1,10)\big)$ for the unique non-trivial [[irreducible representation|irreducible]] [[real spin representation|real $Spin(1,10)$-representation]].

\begin{theorem}
\label{11dSuGraEOMFromSuperFluxIdentity}
**(11d SuGra EoM from super-flux Bianchi identity)**
Given 

1. ([[supergravity|super-gravity]] [[field (physics)|field]]:) an $11\vert\mathbf{32}$-dimensional [[super-spacetime]] $X$ (Def. \ref{SuperSpacetime}), 

1. ([[differential form on a supermanifold|super-]][[supergravity C-field|C-field]] [[flux densities]]:)  $(G^s_4,\, G^s_7)$ as in (eq:LocalFormOfSuperFluxDensities)

then the super-flux [[Bianchi identity]]  (eq:SuperFluxBianchiIdentity) (the super-[higher Maxwell equation](higher+gauge+field#HigherGaugeTheoryOfMaxwellType) for the [[supergravity C-field|C-field]])

\[
  \begin{array}{l}
    \mathrm{d} \, G_4^s \;=\; 0 
    \\
    \mathrm{d} \, G_7^s \;=\; \tfrac{1}{2} G_4^s \, G_4^s
  \end{array}
\]

is equivalent to the joint solution by $\big(e, \psi, \omega, G_4^s,\, G_7^s\big)$ of the [[equations of motion]] of [[D=11 supergravity]].
\end{theorem}
This is, in some paraphrase, the result of [CDF91, §III.8.5](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre), We indicate the **proof** broken up in the following Lemmas \ref{SuperBianchiIdentityOnG4InComponents}, \ref{SuperBianchiIdentityOnG7InComponents}, and 
\ref{SuperCFieldBianchiImpliesSuGraEoM}.

In all of the following lemmas one expands the Bianchi identoties in their super-vielbein form components.

\begin{remark}
**(Normalization conventions)**
\linebreak
Our choice of prefactors and normalization follows [CDF91](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre)
except for the following changes:

* our Clifford generators absorb a factor of [[imaginary unit|$\mathrm{i}$]]: $\;\;\;\Gamma_a \;=\; \mathrm{i}\, \Gamma_a^{^{DF}} $

* our gravitinos absorb a factor of $\sqrt{2}$: $\;\;\;\psi \;=\; \sqrt{2}\psi^{^{DF}}$

* our 4-flux density absorbs a combinatorial factor of $1/2$: $\;\;\;G_4 = \tfrac{1}{2} R^{\Box}$

* our 7-flux density absorbs a combinatoiral factor of $1/5!$: $\;\;\;G_7 = \tfrac{1}{5!} R^{\otimes}$

Here:

* The  first rescaling reflects that $\Gamma^{{}^{\mathrm{DF}}}$ is not actually a Majorana representation of $\mathrm{Pin}^+(1,10)$, but $\mathrm{i}\Gamma^{{}^{\mathrm{DF}}}$ is. 

  This rescaling removes all occurrences of imaginary units in the Bianchi identities, as it should be for algebra over the real numbers with real fermion representations.

* The second rescaling has the effect that $\mathrm{d} e^a = \big(\overline{\psi} \Gamma^a \psi\big) + \cdots$ instead of $\mathrm{d}\, e^a = \tfrac{1}{2} \big(\overline{\psi} \Gamma^a \psi\big) + \cdots$.


\end{remark}

\begin{lemma}
\label{SuperBianchiIdentityOnG4InComponents}
  The [[Bianchi identity]] for $G^s_4$ (eq:SuperFluxBianchiIdentity) is equivalent to 

1. the closure of the ordinary 4-flux density $G_4$ 

1. the following dependence of $\rho$ on $G_4$

shown in any super-chart:

\[
  \label{BianchiIdentityForG4sInComponents}
  \begin{array}{l}
    \mathrm{d}\, G^s_4 \;=\; 0
    \\
    \;\Leftrightarrow\;
    \left\{
    \begin{array}{l}
      \big(
        \nabla_{a} (G_4)_{a_1 \cdots a_4}
      \big)
      e^{a} \, e^{a_1} \cdots e^{a_4}
      \;=\;
      0
      \\
      \rho
      \;=\;
      \rho_{a b} \, e^{a} \, e^b
      \,+\,
      \Big(
      -\tfrac{1}{6}
      \,
      \tfrac{1}{3!}
      (G_4)_{a b_1 b_2 b_3}
      \,\Gamma^{a b_1 b_2 b_3}\,
      \,
      +
      \tfrac{1}{12}
      \,
      \tfrac{1}{4!}
      (G_4)_{b_1 \cdots b_4}
      \,\Gamma^{a b_1 \cdots b_4}\,
      \Big)
      \psi
      \, 
      e^a
      \\
      \Big(
        \tfrac{1}{4!}
        \psi^\alpha
        \nabla_\alpha
        (G_4)_{a_1 \cdots a_4}
        \;+\;
        \big(
          \overline{\psi}
          \Gamma_{a_1 a_2}
          \rho_{a_3 a_4} 
        \big)
      \Big)
      e^{a_1} \cdots e^{a_4}
      \;=\;
      0
      \,.
    \end{array}
    \right.
  \end{array}
\]
\end{lemma}
This is essentially [CDF91, (III.8.44-49 & 60b)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre).
\begin{proof}
  The general expansion of $\rho$ in the super-vielbein basis is of the form 
  $$
    \rho
    \;:=\;
    \rho_{a b}
    \,
    e^a\, e^b
    +
    H_a \psi \, e^a
    +
    \underset{ = 0 }{
      \underbrace{
      \overline{\psi}
        \,\kappa\,
      \psi
      }
    }
    \,,
  $$
  where the last term is taken to vanish.l (...).



Therefore, the Bianchi identity has the following components, 
\[
  \label{ComponentsOfBianchiForGs4}
    \begin{array}{l}
      \mathrm{d}
      \Big(
      \,
      \tfrac{1}{4!}
      (G_4)_{a_1 \cdots a_4}
      \,
      e^{a_1} \cdots e^{a_4}
      -
      \tfrac{1}{2}
        \big(
          \overline{\psi}
          \Gamma_{a_1 a_2}
        \psi
        \big)
        \,
        e^{a_1}\, e^{a_2}
      \Big)
      \;=\;
      0
      \\
      \;\Leftrightarrow\;
      \left\{
      \begin{array}{l}
        \big(
          \nabla_{a}
          (G_4)_{a_1 \cdots a_4}
        \big)
        e^{a}\, e^{a_1} \cdots e^{a_4}
        \;=\;
        0
        \\
        \Big(
          \tfrac{1}{4!}
          \psi^\alpha
          \big(
            \nabla_\alpha
            (G_4)_{a_1 \cdots a_4}
          \big)
          \;+\;
          \big(
            \overline{\psi}
            \Gamma_{a_1 a_2}
            \rho_{a_3 a_4}
          \big)
        \Big)
        e^{a_1} \cdots e^{a_4}
        \;=\;
        0
        \\
        \tfrac{1}{3!}
        (G_4)_{a b_1 b_2 b_3}
        \big(
          \overline{\psi}
          \,\Gamma^a\,
          \psi
        \big)
        \,
        e^{b_1 b_2 b_3}
        +
        \big(
        \overline{\psi}
        \,\Gamma_{a_1 a_2}\,
        H_b
        \psi
        \big)
        e^{a_1} \, e^{a_2} \, e^b
        \;=\;
        0
        \,,
      \end{array}
      \right.
    \end{array}
\]
where we used that the quartic spinorial component vanishes identically, due to a [[Fierz identity]] ([here](Majorana+spinor#eq:QuarticFierzIdentitiesOn32)):
  $$
    -
    \tfrac{1}{2}
    \big(
      \overline{\psi}
      \Gamma_{a_1 a_2}
      \psi
    \big)
    \big(
      \overline{\psi}
      \Gamma^{a_1}
      \psi
    \big)
    e^{a_2}
    \;=\;
    0
    \,.
  $$
 
To solve the second line in (eq:ComponentsOfBianchiForGs4) for $H_a$ (this is [CDF91 (III.8.43-49)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre)) we 
expand $H_a$ in the Clifford algebra (according to [this Prop.](Majorana+spinor#ExpandingEndomorphismOf32InCliffordElements)), 
observing that for $\Gamma_{a_1 a_2} H_{a_3}$ to be a linear combination of the $\Gamma_a$ the matrix $H_a$ needs to have a $\Gamma_{a_1}$-summand or a $\Gamma_{a_1 a_2 a_3}$-summand. The former does not admit a Spin-equivariant linear combination with coefficients $(G_4)_{a_1 \cdots a_4}$, hence it must be the latter. But then we may also need a component $\Gamma_{a_1 \cdots a_5}$ in order to absorb the skew-symmetric product in $\Gamma_{a_1 a_2} H_a$. Hence $H_a$ must be of this form:

\[
    \label{AnsatzForHa}
    H_a 
    \;=\;
    \mathrm{const}_1
    \,
    \tfrac{1}{3!}
    (G_4)_{a b_1 b_2 b_3}
    \Gamma^{b_1 b_2 b_3}
    +
    \mathrm{const}_2
    \,
    \tfrac{1}{4!}
    (G_4)^{b_1 \cdots b_4}
    \Gamma_{a b_1 \cdots b_4}
    \,.
\]
  With this, we compute:
  \[
    \label{PairingTheHaTermInRho}
    \begin{array}{ll}
      \big(
      \overline{\psi}
      \Gamma_{a_1 a_2} H_{a_3}
      \psi
      \big)
      e^{a_1} \, e^{a_2} \, e^{a_3}
      &
      =\;
      \mathrm{const}_1
      \,
      \tfrac{1}{3!}
      (G_4)_{a_3 b_1 b_2 b_3}
      \,
     \big(
     \overline{\psi}
     \Gamma_{a_1 a_2}
     \Gamma^{b_1 b_2 b_3}
     \psi
     \big)
     e^{a_1} \, e^{a_2} \, e^{a_3}
     \\
     &
     \;\;\;+\,
     \mathrm{const}_2
     \,
     \tfrac{1}{4!}
     \,
     (G_4)^{b_1 \cdots b_4}
     \,
     \big(
     \overline{\psi}
     \Gamma_{a_1 a_2}
     \Gamma_{a_3 b_1 \cdots b_4}
     \psi
     \big)
     e^{a_1} \, e^{a_2} \, e^{a_3}
     \\
     &
     \;=\;
      1
      \,
      \mathrm{const}_1
      \,
      \tfrac{1}{3!}
      \,
      (G_4)_{a_3 b_1 b_2 b_3}
      \big(
       \overline{\psi}
       \,\Gamma_{a_1 a_2}{}^{b_1 b_ 2 b_3}\,
       \psi
      \big)
      e^{a_1} \, e^{a_2} \, e^{a_3}
      \\
      &
      \;\;\;+\,
      6
      \,
      \mathrm{const}_1
      \,
      \tfrac{1}{3!}
      \,
      (G_4)_{b_3 a_1 a_2 a_3}
       \big(
       \overline{\psi}
       \,\Gamma^{b_3}\,
       \psi
       \big)
     e^{a_1} \, e^{a_2} \, e^{a_3}
     \\
     &
     \;\;\;+\,
     8
     \,
     \mathrm{const}_2
     \,
     \tfrac{1}{4!}
     \,
     (G_4)^{b_1 \cdots b_3 a_3}
     \,
     \big(
     \overline{\psi}
     \Gamma^{a_1 a_2}{}_{b_1 \cdots b_3}
     \psi
     \big)
     e^{a_1} \, e^{a_2} \, e^{a_3}
     \,.
    \end{array}
  \]
  Here the multiplicities of the nonvanishing Clifford-contractions arise via [this Lemma](Majorana+spinor#ProductOfLinearCliffordGenerators):
  $$
    \begin{array}{l}
      1 \;=\; 0! \Big( {2 \atop 0} \Big) \Big( {3 \atop 0} \Big)
      \\
      6 \;=\; 2! \Big( {2 \atop 2} \Big) \Big( {3 \atop 2} \Big)
      \\
      8 \;=\; 1! \Big( {2 \atop 1} \Big) \Big( {4 \atop 1} \Big)
    \,,
    \end{array}
  $$
  and all remaining contractions vanish inside the spinor pairing by [this lemma](Majorana+spinor#VanishingQuadraticFormsOn32).

  Now using (eq:PairingTheHaTermInRho) in (eq:ComponentsOfBianchiForGs4) yields:
  $$
    \begin{array}{l}
    \mathrm{const}_1 = -1/6
    \,,
    \\
    \mathrm{const}_2 
      = 
    -
    4!/3!
    \,
    \mathrm{const}_1 / 8
      =
    + 1/12 
    \,,
    \end{array}
  $$ 
  as claimed.
\end{proof}



\begin{lemma}\label{SuperBianchiIdentityOnG7InComponents}
  Given the [[Bianchi identity]] for $G^s_4$ (eq:BianchiIdentityForG4sInComponents), then 
 the [[Bianchi identity]] for $G^s_7$ (eq:SuperFluxBianchiIdentity) is equivalent to 

1. the Bianchi identity for the ordinary flux density $G_7$ 

1. its [[Hodge duality]] to $G_4$

1. another condition on the gravitino field strength

\[
  \label{BianchiIdentityForG7sInComponents}
  \begin{array}{l}
    \mathrm{d}
    \,
    G^s_7
    \;=\;
    \tfrac{1}{2}
    G^s_4 \, G^s_4
    \\
    \;\Leftrightarrow\;
    \left\{
    \begin{array}{l}
      \big(
        \nabla_{a_1} 
        \tfrac{1}{7!} (G_7)_{a_2 \cdots a_8}
      \big)
      e^{a_1} \cdots e^{a_8}
     \;=\;
     \tfrac{1}{2}
      \big(
        \tfrac{1}{4!}
        (G_4)_{a_1 \cdots a_4}
        \,
        \tfrac{1}{4!}
        (G_4)_{a_5 \cdots a_8}
      \big)
      e^{a_1} \cdots e^{a_8}
      \\
      (G_7)_{a_1 \cdots a_7}
      \;=\;
      \tfrac{1}{4!}
      \epsilon_{a_1 \cdots a_b b_1 \cdots b_4}
      (G_4)^{b_1 \cdots b_4}
      \\
      \Big(
        \tfrac{1}{7!}
        \psi^\alpha
        \nabla_\alpha
        (G_7)_{a_1 \cdots a_7}
        \psi^\alpha
        \;+\;
        \frac{2}{5!}
        \big(
          \overline{\psi}
          \Gamma_{a_1 \cdots a_5} 
          \rho_{a_6 a_7}
        \big)
      \Big)
      e^{a_1} \cdots e^{a_7}
      \;=\;
      0
    \end{array}
    \right.
  \end{array}
\]
\end{lemma}
This is essentially [CDF91, (III.8.50-53)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre).
\begin{proof}
The components of the Bianchi identity are
$$
  \begin{array}{l}
  \mathrm{d}
  \,
  G_4^s \;=\; 0
  \\
  \Rightarrow
  \left\{
  \begin{array}{l}
  \mathrm{d}
  \Big(
    \tfrac{1}{7!}
    (G_7)_{a_1 \cdots a_7}
    \, 
    e^{a_1} \cdots e^{a_7}
    -
    \tfrac{1}{5!}
    \big(
    \overline{\psi}
    \Gamma_{a_1 \cdots a_5}
    \psi
    \big)
    e^{a_1} \cdots e^{a_5}
  \Big)
  \\
  \;=\;
  \tfrac{1}{2}
  \Big(
    \tfrac{1}{4!}
    (G_4)_{a_1 \cdots a_4}
    e^{a_1}
    \cdots
    e^{a_4}
    -
    \tfrac{1}{2}
    \big(
      \overline{\psi}
      \Gamma_{a_1 a_2}
      \psi
    \big)
  \Big)
  \Big(
    \tfrac{1}{4!}
    (G_4)_{a_1 \cdots a_4}
    e^{a_1}
    \cdots
    e^{a_4}
    -
    \tfrac{1}{2}
    \big(
      \overline{\psi}
      \Gamma_{a_1 a_2}
      \psi
    \big)
  \Big)
  \\
  \;\Leftrightarrow\;
  \left\{
  \begin{array}{l}
  \Big(
    \nabla_{a_1}
    \tfrac{1}{7!}
    (G_7)_{a_2 \cdots a_8}  
    \;=\;
    \;\tfrac{1}{2}\;
    \tfrac{1}{4!}
    (G_4)_{a_1 \cdots a_4}
    \,
    \tfrac{1}{4!}
    (G_4)_{a_5 \cdots a_8}
  \Big)
  e^{a_1} \cdots e^{a_8}
  \\
  \Big(
    \tfrac{1}{7!}
    \psi^\alpha
    \nabla_\alpha
    (G_7)_{a_1 \cdots a_7}
    +
    \frac{2}{5!}
    \big(
      \overline{\psi}
      \Gamma_{a_1 \cdots a_5} 
      \rho_{a_6 a_7}
    \big)
  \Big)
  e^{a_1} \cdots e^{a_7}
  \;=\;
  0
  \\
  \left.
  \begin{array}{l}
    \tfrac{1}{6!}
    (G_7)_{a_1 \cdots a_6 b}
    \big(
      \overline{\psi}
      \,\Gamma^b\,
      \psi
    \big)
    e^{a_1}
    \cdots
    e^{a_6}
    \\
    \;\;\;+\,
    \tfrac{2}{12}
    \,
    \tfrac{1}{5!}
    \,
    \tfrac{1}{4!}
    \,
      (G_4)^{b_1 \cdots b_4}
    \big(
      \overline{\psi}
      \,
      \Gamma_{a_1 \cdots a_5}
      \,
      \Gamma_{a b_1 \cdots b_4}\,
      \psi
    \big)
    e^a
    \,
    e^{a_1} \cdots e^{a_5}
    \\
    \;\;-\;
    \tfrac{2}{6}
    \tfrac{1}{5!}
    \tfrac{1}{3!}
    (G_4)_{a b_1 b_2 b_3}
    \big(
      \overline{\psi}
      \,\Gamma_{a_1 \cdots a_5}\,
      \Gamma^{b_1 b_2 b_3}
      \psi
    \big)
    e^{a}
    \,
    e^{a_1} \cdots e^{a_5}
    \\
    \;\;\;-\,
    \Big(
    \tfrac{1}{2}
    \big(
      \overline{\psi}
       \Gamma_{a_1 a_2}
      \psi
    \big)
    e^{a_1} \, e^{a_2}
    \Big)
    \tfrac{1}{4!}
    (G_4)_{b_1 \cdots b_4}
    \,
    e^{b_1} \cdots e^{b_4}
    \;\;=\;\; 0
    \,,
  \end{array}
  \right\}
  \Leftrightarrow
  (G_7)_{a_1 \cdots a_6 b}
  \;=\;
  \tfrac{1}{4!}
  \epsilon_{a_1 \cdots a_6 b
  b_1 \cdots b_4}
  (G_4)^{b_1 \cdots b_4}
  \end{array}
  \right.
  \end{array}
  \right.
  \end{array}
$$
where:

**(i)** in the quadratic spinorial component we inserted the expression for $\rho$ from (eq:BianchiIdentityForG4sInComponents), then contracted $\Gamma$-factors using again [this Lemma](Majorana+spinor#ProductOfLinearCliffordGenerators),
and finally observed that of the three spinorial quadratic forms (see [there](Majorana+spinor#eq:TheThreeQuadraticFormsOn32))
the coefficients of $\big(\overline{\psi}\Gamma_{a_1 a_2} \psi\big)$ and of $\big(\overline{\psi}\Gamma_{a_1 \cdots a_6} \psi\big)$ vanish identically, by a remarkable cancellation of combinatorial prefactors:

* $\underset{= 0 }{\underbrace{\bigg(- \frac{2}{12} \frac{1}{5!} \frac{1}{4!} 4!
 \Big(
   { 5 \atop 4 }
 \Big)
 \Big(
   { 4 \atop 4 }
 \Big)
 \;+\;
 \frac{2}{6}
 \frac{1}{5!}
 \frac{1}{3!}
 3!
 \Big(
   { 5 \atop 3 }
 \Big)
 \Big(
   { 3 \atop 3 }
 \Big)
 \;-\;
 \frac{1}{2}
 \frac{1}{4!}
 \bigg)
 }
 }
 \;
 (G_4)_{a_2 \cdots a_5}
 \big(
 \overline{\psi}
 \,\Gamma_{a a_1}\,
 \psi
 \big)
 e^{a}
 \,
 e^{a_1} \cdots e^{a_6}
 \;\;\;
$
(<a href="https://www.wolframalpha.com/input?i=-+%282%2F12%29+*+%281%2F5%21%29+*+%281%2F4%21%29+*+4%21+%285+choose+4%29+*+%284+choose+4%29+%2B+%282%2F6%29+*+%281%2F5%21%29+*+%281%2F3%21%29+*+3%21+*+%285+choose+3%29+*+%283+choose+3%29+-+%281%2F2%29*+++%281%2F4%21%29">check</a>)

* $\underset{
    = 0
  }{   
  \underbrace{
    \bigg(
    \frac{2}{12}
    \frac{1}{5!}
    \frac{1}{4!}
    2
    \Big(
      { 5 \atop 2 }
    \Big)
    \Big(
      { 4 \atop 2 }
    \Big)
    \;-\;
    \frac{2}{6}
    \frac{1}{5!}
    \frac{1}{3!}
    3!
    \Big(
      { 5 \atop 1 }
    \Big)
    \Big(
      { 3 \atop 1 }
    \Big)    
    \bigg)
  }
  }
  \;
    (G_4)_{a_1 a_2 b_1 b_2}
    \big(
      \overline{\psi}
      \,\Gamma_{a_3 \cdots a_6}{}^{b_1 b_2}\,
      \psi
    \big)
    e^{a_1} \cdots e^{a_6}
  \;\;\;
$
(<a href="https://www.wolframalpha.com/input?i=%282%2F12%29+*+%281%2F5%21%29+*+%281%2F4%21%29+*+2%21+*+%285+choose+2%29+*+%284+choose+2%29++-++%282%2F6%29+*+%281%2F5%21%29+*+%281+%2F+3%21%29+*+5+*+3">check</a>)

**(ii)** the quartic spinorial component holds identitically, due to the [[Fierz identity]] [here](Majorana+spinor#eq:QuarticFierzIdentitiesOn32):
$$
  -\tfrac{1}{4!}
  \big(
    \overline{\psi}
    \,\Gamma_{a_1 \cdots a_5}\,
    \psi
  \big)
  \big(
    \overline{\psi}
    \Gamma^{a_1}
  \big)
  e^{a_2} \cdots e^{a_5}
  \;=\;
  \tfrac{1}{8}
  \Big(
  \big(
    \overline{\psi}
    \,\Gamma_{a_1 a_2}\,
    \psi
  \big)
  e^{a_1} e^{a_2}
  \Big)
  \Big(
  \big(
    \overline{\psi}
    \,\Gamma_{a_1 a_2}\,
    \psi
  \big)
  e^{a_1} e^{a_2}
  \Big)
  \,.
$$

Therefore the only spinorial component of the Bianchi identity which is not automatically satisfied is (with $\Gamma_{0 1 2 \cdots} = \epsilon_{0 1 2 \cdots}$, see [there](Majorana+spinor#eq:CliffordVolumeFormIn11d)) the vanishing of
$$
  \tfrac{1}{6!}
  \Big(
  (G_7)_{a_1 \cdots a_6 b}
  -
  \tfrac{1}{4!}
  (G_4)^{b_1 \cdots b_4}
  \epsilon_{b_1 \cdots b_4 a_1 \cdots a_6 b}
  \Big)
  \big(
    \overline{\psi}
    \,\Gamma^b\,
    \psi
  \big)
  \,,
$$
which is  manifestly the claimed [[Hodge duality]] relation.
\end{proof}
 
\begin{lemma}\label{SuperCFieldBianchiImpliesSuGraEoM}
  Given the Bianchi identities for $G_4^s$ (eq:BianchiIdentityForG4sInComponents) and $G_7^s$ (eq:BianchiIdentityForG7sInComponents), the supergravity fields satisfy their [[Einstein equations]] with these source terms:
$$
  \begin{array}{l}
    \mathrm{d}\, G_4^s \;=\;0
    \,,
     \;\;\;
    \mathrm{d}\, G_7^s \;=\; \tfrac{1}{2} G_4^s \, G_4^2
    \\
    \;\Rightarrow\;
    \left\{
    \begin{array}{l}
      R^{a m}_{b m}
      -
      \tfrac{1}{2}
      \delta^a_b\, 
      R^{m n}_{m n}
      \;=\;
      const\, 
      (G_4)^a{c_1 \cdots c_3}
      (G_4)_{b c_1 \cdots c_3}
      +
      const\,
      \delta^a_b
      \,
      (G_4)^{c_1 \cdots c_4}
      (G_4)_{c_1 \cdots c_4}
      \;\;\;\;
      ({\color{darkblue}\text{Einstein equation}})
      \\
      \Gamma^{b a_1 a_2}
      \rho_{a_1 a_2}
      \;=\;
      0
      \;\;\;\;
      ({\color{darkblue}\text{Rarita-Schwinger equation}})
    \end{array}
    \right.
  \end{array}
$$
\end{lemma}
This is indicated in [CDF91, (III.8.54-60)](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre).
It follows by solving the super-gravitational Bianchi identities \eqref{GravitationalBianchiIdentities}, using from the previous lemmas only the form of the gravitino field strength (eq:BianchiIdentityForG4sInComponents).

In conlcusion, the above lemmas give Thm. \ref{11dSuGraEOMFromSuperFluxIdentity}.

