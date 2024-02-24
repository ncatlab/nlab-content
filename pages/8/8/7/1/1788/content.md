

### $D=11$ SuGra from Super-C-Field Flux Bianchi Identity

We show that the [[equations of motion]] of [[D=11 supergravity]] on an $11\vert\mathbf{32}$-dimensional ([[super-torsion]]-free) [[super spacetime]] $X$, with  [[super vielbein]] $(e,\psi)$ ([[graviton]]/[[gravitino]]-[[field (physics)|fields]]) follow from just the requirement that the [[duality-symmetric higher gauge theory|duality-symmetric]] super-[[supergravity C-field|C-field]] [[flux densities]] $(G_4^s, G_7^s) \,\in\, \Omega^4_{dR}(X) \times \Omega^7_{dR}(X) $ 

1. satisfy their [[Bianchi identities]]

   \[
     \label{SuperFluxBianchiIdentity}
     \begin{array}{l}
       \mathrm{d} \, G_4^s \;=\; 0 
       \\
       \mathrm{d} \, G_7^s \;=\; \tfrac{1}{2} G_4^s \, G_4^s
     \end{array}
   \]

1. are on any local super-chart $U \hookrightarrow X$ of the locally supersymmetric form

   \[
     \label{LocalFormOfSuperFluxDensities}
     \begin{array}{l}
       G_4^s 
       \;=\;
       \tfrac{1}{2}
       (G_4)_{a_1 \cdots a_4}
       e^{a_1} \cdots e^{a_4}
       \,-\,
       \big(\overline{\psi}\Gamma_{a_1 a_2} \psi\big)
       e^{a_1} \, e^{a_2}
       \\
       G_7^s 
       \;=\;
       \tfrac{1}{5!}
       (G_7)_{a_1 \cdots a_7}
       e^{a_1} \cdots e^{a_7}
       \,-\,
       \big(\overline{\psi}\Gamma_{a_1 \cdots a_7} \psi\big)
       e^{a_1} \cdots e^{a_7}
       \mathrlap{\,.}
     \end{array}
   \]

Up to some mild (but suggestive) re-arrangement, the computation is essentially that indicated in [CDF91, §III.8](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) (and apparently nowhere else), and the following may be understood as an exposition of this result, which seems to stand out as the only account that is (i) fully first-order and (ii) [[duality-symmetric higher gauge theory|duality-symmetric]] (in that $G_7$ enters the [[equation of motion|EoMs]] as an independent field, whose [[Hodge duality]] to $G_4$ is imposed  *by the [[Bianchi identity]]* for $G_7^s$, remarkably). 

But in restating this we:

1. take care of the proper combinatorial normalization of the fields, which makes the crucial factor of 1/2 appear in (eq:SuperFluxBianchiIdentity);

1. re-define the super-flux densities as in (eq:LocalFormOfSuperFluxDensities), highlighting that it is (only) in this combination that the form of the expected [[Bianchi identity]] (eq:SuperFluxBianchiIdentity) holds even in [[superspace]];

1. disregard the [[gauge potentials]] $C_3$ and $C_6$, whose role in [CDF91, §III.8](D'Auria-Fre+formulation+of+supergravity#CastellaniDAuriaFre) is really just to motivate the form of the [[Bianchi identities]] equivalent to (eq:SuperFluxBianchiIdentity), but whose global nature is more subtle than acknowledged there, while being irrelevant for just the [[equations of motion]].

Instead, the point is that, in consequence of our second item above, one may apply [[flux quantization]] on [[superspace]] and this is then what defines, conversely, the [[gauge potentials]], globally. Moreover, by the fact that the super-flux Bianchi identity already implies the full equations of motion, this flux quantization is compatible with the equations of motion on all of [[super spacetime]].

\begin{definition}\label{SuperSpacetime}
**(super-spacetime)**
\linebreak
  For 

* $D \in \mathbb{N}_{\geq 1}$ a [[natural number]] 

* $\mathbf{N} \in Rep_{\mathbb{R}}\big(Spin(1,D-1)\big)$ a [[real numbers|real]] [[spin representation]] ("[[Majorana spinors]]")

   whose [[spin group|$Spin(1,D)$]]-[[equivariant map|equivariant]] [[bilinear map|bilinear]] pairing we denote

   $$
     \overline{(\text{}-)}(\text{-})
     \;\colon\;
     \mathbf{N} \otimes \mathbf{N}
     \longrightarrow
     \mathbb{R}^{1,D-1}
   $$

by a *[[super-spacetime]]* of super-dimension $D\vert \mathbf{N}$ we here mean:

1. a [[supermanifold]] 

1. which admits an [[open cover]] by [[super-Minkowski spacetime|super-Minkowski]] supermanifolds $\mathbb{R}^{1,D-1\vert \mathbf{N}}$

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

1. and with a [[spin-connection]] $\omega$ (...)

1. such that the [[super-torsion]] vanishes, in that on each chart:

   $$
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
   $$

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
     \overline{\psi}\Gamma^a\psi
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
By [[exterior calculus]] the gravitational [[field strength]] [[tensors]] (Def. \ref{GravitationalFieldStrengths}) satisfy the following [[identities]]:

\[
  \label{GravitationalBianchiIdentities}
  \begin{array}{l}
    \mathrm{d}
    \,
    R^{a}{}_b
    \;=\;
    \omega^a{}_{a'} \, R^{a'}{}_b
    -
    R^{a}{}_{b'}
    \,
    \omega^{b'}{}_{b}
    \\
    \mathrm{d}
    \,
    T^a 
    \;=\;
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
    \;=\;
    \tfrac{1}{4}
    R^{a b} \Gamma_{a b} \psi
  \end{array}
\]

\end{lemma}







