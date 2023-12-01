
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In ([[higher gauge theory|higher]]) [[gauge theory]], the total (generalized) electric/magnetic [[fluxes]] through given [[surfaces]] (or higher [[submanifolds]]) should be [[observables]] and hence have [[Poisson brackets]] in the [[classical field theory]] To the extent that these induce non-trivial operator [[commutators]] in the corresponding [[quantum field theory]], this means that the corresponding kinds of fluxes would be subject to the [[Heisenberg uncertainty principle]].

A subtlety here is that the usual [[phase space]]-methods for [[Lagrangian field theories]] directly provide these brackets only for the [[differential forms]] which are the [[flux densities]]. These however, provide only a [[rational homotopy theory|rational]] image of the fluxes, which in general may furthermore have [[torsion subgroup|torsion]]-[[cohomology group|cohomology]]-components.

In plain [[electromagnetism]], the [[canonical momentum]] of the [[gauge potential]] $A$ is proportional (by constants to be ignored in the following) to the electric flux density $\star F$ (where $F$ is the [[Faraday tensor]] [[flux density]] and $\star$ is the [[Hodge star operator]] on the given [[spacetime]] [[pseudo-Riemannian manifold]]), which however means that the the Poisson bracket of the magnetic flux density $F \equiv \mathrm{d}_{dR} A$ with the electric flux density is a total derivative (cf. eg. [Blaschke & Gieres 2021 (5.5)](Yang-Mills+theory#BlaschkeGieres21)), so that the bracket of the integrated fluxes $\Phi_E$ and $\Phi_B$ through given [[orientable manifold|orientable]] [[closed manifold|closed]] surfaces $S_E$ and $S_B$, respectively, actually vanishes (cf. [FMS07b (3.6)](#FreedMooreSegal07b)):

$$
  \big\{
    \Phi_E
    ,\,
    \Phi_B
  \big\}
  \;\equiv\;
  \Big\{
  \textstyle{\int}_{S_B} \star F 
  ,\,
  \textstyle{\int}_{S_E} F
  \Big\}
  \;=\;
  0
  \,.
$$

The thrust of [FMS 07a](#FreedMooreSegal07a), [07b](#FreedMooreSegal07b) is the claim that this bracket becomes non-vanishing if torsion-components of the fluxes (through their enhancement to [[ordinary differential cohomology]]) are retained, but it seems that this is ultimately by definition ([FMS07a, Def. 1.29](#FreedMooreSegal07a); [FMS07b (3.28)](#FreedMooreSegal07b)) more than by derivation from first principles.

On the other hand, for [[non-abelian group|non-abelian]] [[gauge group]], a careful analysis of the (somewhat subtle) Poisson brackets reveals ([Cattaneo & Perez 2017](#CattaneoPerez17)) that the electric fluxes -- understood as flux densities integrated against [[Lie algebra]] valued functions $\alpha$ -- have a non-trivial bracket among *themselves*:

$$
 \big\{
   \Phi^\alpha_E
   ,\,
   \Phi^{\alpha'}_E
 \big\}
 \;\propto\;
 \Phi_E^{[\alpha, \alpha']}
$$

(where $[-,-]$ is the pointwise [[Lie bracket]]). This result has found a lot of attention (only) in the context of [[first-order formulations of gravity]].

## Details
 {#Details}

> under construction

For 3+1 dimensional [[Yang-Mills theory]] with a [[semisimple Lie algebra|semisimple]] gauge Lie algebra $\mathfrak{g}$ (such as [[su(n)|$\mathfrak{su}(n)$]] or [[so(n)|$\mathfrak{so}(n)$]]) we discuss ([below](#ThePoissonBracketOfIntegratedFluxes)) the [[Poisson bracket]] of integrals (against [[Lie algebra]]-valued functions) of [[flux densities]] ([[curvature 2-forms]]) over [[oriented manifold|oriented]] [[closed manifold|closed]] [[surfaces]], following [Cattaneo & Perez 2017](#CattaneoPerez17). 

The bracket of electric fluxes among themselves is equation (7) [Cattaneo & Perez 2017](#CattaneoPerez17), and to warm-up we spell out the relevant computation in detail. Then we similarly compute the bracket between electric and magnetic fluxes, showing that it vanishes identically.

The computations are standard and straightforward, but since, as usual, the results depend crucially on delicate signs, we go into full detail.


### Lie theoretic preliminaries

Our [[ground field]] is the [[real numbers]]. 

Consider a [[Lie algebra]] $\mathfrak{g}$ with [[Lie bracket]]

\[
  \label{LieBracket}
  [-,-] 
    \,\colon\, 
  \mathfrak{g} \otimes \mathfrak{g}
  \longrightarrow
  \mathbb{R}
  \,.
\]

We aim to mostly write intrinsic expressions, but it is still useful to have the component expression at hand. For that purpose we choose once and for all any [[linear basis]] of the [[underlying]] [[vector space]] of the Lie algebra

$$
  \mathfrak{g}
  \;\simeq_{{}_\mathbb{R}}\;
  \mathbb{R}
  \big\langle 
    t_1, \cdots, t_{{}_{dim(\mathfrak{g})}}
  \big\rangle
$$

in terms of which the Lie bracket (eq:LieBracket) is given by the structure constants $\{f^i{}_{j k}\}$ defined by the following equation (using [[Einstein summation convention]], throughout):

$$
  [t_j, t_k]
  \;=\;
  f^i{}_{j k} \, t_i
  \,.
$$

The following discussion is all about [[Lie algebra-valued differential form|$\mathfrak{g}$-valued differential forms]], notably 1-forms

\[
  \label{GaugePotential}
  A \;\equiv\; A^i t_i 
  \;\in\;
  \Omega^1_{dR} \otimes \mathfrak{g}
  \,,
\]

which are going to represent the [[gauge potential]].

In writing (Lie- or Poisson-)brackets of such form, we always mean to (1.) take the [[wedge product]] of the bare [[differential forms]] *in the given order* and (2.) apply the bracket to the [[coefficients]], eg.:

\[
  \label{BracketOfGaugePotentialWithItself}
  [ A , A ]
  \;\equiv\;
  A^j \wedge A^k [t_i, t_j]
  \;=\;
  f^i{}_{j k} A^j \wedge A^k t_i
  \,.
\]


The [[Jacobi identity]] of $\mathfrak{g}$ says that $[t_i,-]$ is a [[derivation]] of the Lie bracket:

\[
  \label{JacobiIdentity}
  \big[t_i, [t_j, t_k] \big]
  \;=\;
  \big[ [t_i, t_j], t_k] \big]
  \,+\,
  \big[ t_j, [t_i, t_k] \big]
  \;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;
  f^\bullet{}_{i l} f^{l}{}_{j k}
  \;=\;
  f^\bullet{}_{l k}  f^l{}_{i j}
  \,+\,
  f^\bullet{}_{ j l } f^l{}_{ i k } 
  \,.
\]

For any $X \in \Omega^n_{dR} \otimes \mathfrak{g}$ this means for instance, with (eq:BracketOfGaugePotentialWithItself), that

$$
  \begin{array}{l}
  \big[A, [A, X]\big]^i
  \\
  \;=\;
  \big[ [A,A], X \big]^i
  -
  \big[A, [A, X]\big]^i
  \end{array}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  \big[A, [A, X]\big]
  \;=\;
  \tfrac{1}{2}
  \big[ [A,A], X \big]
$$

[[covariant derivative]]:

$$
  (\mathrm{d}_{A} X)^i
  \;\equiv\;
  \mathrm{d} X^i + [A, X]^i
  \;=\;
  \mathrm{d} X^i + f^i_{j k} A^j X^k
$$

[[curvature]]:

$$
  \begin{array}{l}
    \mathrm{d}_A \mathrm{d}_A X
    \\
     \;=\;
     \mathrm{d}_A \big(
       \mathrm{d}X + [A,X]
     \big)
     \\
     \;=\;
     [A, \mathrm{d}X]
     +
     \mathrm{d}[A,X] 
     +
     \big[ A, [A, X] \big]
     \\
     \;=\;
     [A, \mathrm{d}X]
     +
     [\mathrm{d} A,X] 
     -
     [A, \mathrm{d} X] 
     +
     \tfrac{1}{2}\big[ [A, A],  X \big]
     \\
     \;=\;
     \big[
       \underset{
         \equiv \, F_A
       }{
         \underbrace{
           \mathrm{d} A + \tfrac{1}{2}[A, A]
         }   
       }
       ,\,
       X
     \big]
  \end{array}
$$

[[Bianchi identity]]:

$$
  \begin{array}{l}
    \mathrm{d}_A \mathrm{d}_A \mathrm{d}_A X
    \\
    \;=\;
    \mathrm{d}_A \big[ F_A ,\, X \big]
    \\
    \;=\;
    \big[ \mathrm{d}_A F_A ,\, X \big]
    +
    \big[ F_A ,\, \mathrm{d}_A X \big]
    \\
    \;=\;
    \big[ \mathrm{d}_A F_A ,\, X \big]
    +
    \mathrm{d}_A \mathrm{d}_A \mathrm{d}_A X
   \end{array}
   \;\;\;\;\;\;\;
   \Rightarrow
   \;\;\;\;\;\;\;
   \mathrm{d}_A F_A \,=\, 0
$$

[[invariant polynomial]]:

$$
  \langle -,-\rangle
  \;\colon\;
  \mathfrak{g} \otimes \mathfrak{g}
  \to
  \mathbb{R}
$$

$$
  k_{i j}
  \;\equiv\;
  \langle t_i, t_j\rangle
$$

invariance

$$
  \big\langle
    [t, -]
    ,\,
    -
  \big\rangle
  +
  \big\langle
    -
    ,\,
    [t,-]
  \big\rangle
  \;=\;
  0
$$

The induced trilinear pairing

$$
  \langle -,-,- \rangle
  \;\coloneqq\;
  \big\langle -,[-,-] \big\rangle
$$

is also $\mathfrak{g}$-invariant, in that

$$
  \begin{array}{l}
    \big\langle
      [t,-], -,-
    \big\rangle
    +
    \big\langle
      -, [t,-], -
    \big\rangle
    +
    \big\langle
      -, -, [t,-]
    \big\rangle
    \\
    \;\equiv\;
    \big\langle
      [t,-], [-,-]
    \big\rangle
    +
    \Big\langle
      -, \big[[t,-], -\big]
    \Big\rangle
    +
    \Big\langle
      -, \big[-, [t,-]\big]
    \Big\rangle
    \\
    \;=\;
    \big\langle
      [t,-], [-,-]
    \big\rangle
    +
    \Big\langle
      -, \big[ t, [-, -] \big]
    \Big\rangle
    \\
    \;=\;
    0
    \,,
  \end{array}
$$

where we used first the Jacobi identity and then the invariant of the bilinear pairing.

Moreover, for a [[semisimple Lie algebra]]
the trilinear pairing is also skew-symmetric and hence in particular invariant under cyclic permutation of its arguments.

$$
  \big\langle
    t_i, t_j k
  \big\rangle
  \;=\;
  \big\langle
    t_k, t_i j
  \big\rangle
$$



### The Poisson bracket of canonical variables

[[Poisson bracket]]:

$$
  \big\{ E^i, A^j \big\}
  \;\equiv\;
  k^{ i j }
$$


$$
  \begin{array}{l}
    \Big\{
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \big(
        \mathrm{d}_A \beta
      \big)
    \Big\}
    \\
    \;\equiv\;
    \Big\{
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \big(
        \mathrm{d}\beta
        + [A, \beta]
      \big)
    \Big\}
    \\
    \;=\;
    \big(\mathrm{d}_A \alpha_i\big)
    \Big[
      \big\{
        E^i
        ,\,
        A
      \big\}
      ,\,
      \beta
    \Big]
    \\
    \;=\;
    \big(\mathrm{d}_A \alpha_i\big)
    \big[
      t^i
      ,\,
      \beta
    \big]
    \\
    \;=\;
    \Big[
      \big(\mathrm{d}_A \alpha\big)
      ,\,
      \beta
    \Big]
  \end{array}
$$

notably:

$$
  \begin{array}{l}
    \Big\{
      \underset{x}{\textstyle{\int}}
      \big(\mathrm{d}_A \alpha_i(x)\big) \wedge E^i(x)
      ,\,
      \mathrm{d} A(x')
    \Big\}
    \\
    \;=\;
    \underset{x}{\textstyle{\int}}
    \big( \mathrm{d}_A \alpha(x) \big)
    \wedge
    \mathrm{d}_{x'} \delta(x,x')
    \\
    \;=\;
    -
    \underset{x}{\textstyle{\int}}
    \big( \mathrm{d}_A \alpha(x) \big)
    \wedge
    \mathrm{d}_{x} \delta(x,x')
    \\
    \;=\;
    -
    \underset{x}{\textstyle{\int}}
    \Big(
      \mathrm{d}
      \big( \mathrm{d}_A \alpha(x) \big)
    \Big)
    \delta(x,x')
    \\
    \;=\;
    -
    \mathrm{d} \big( \mathrm{d}_A \alpha(x') \big)
  \end{array}
$$

and hence

$$
  \begin{array}{l}
    \Big\{
      \underset{x}{\textstyle{\int}}
      \big(\mathrm{d}_A \alpha_i(x)\big) \wedge E^i(x)
      ,\,
      F_A(x')
    \Big\}
    \\
    \;=\;
    -
    d_A \big(\mathrm{d}_A \alpha\big)(x')
  \end{array}
$$


### The Poisson bracket of integrated fluxes
 {#ThePoissonBracketOfIntegratedFluxes}

Poisson bracket of electric with electric fluxes

$$
  \begin{array}{l}
  \Big\{
    \big( \mathrm{d}_A \alpha_i \big) E^i
    ,\,
    \big( \mathrm{d}_A \beta_j \big) E^j
  \Big\}
  \\
  \;=\;
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  -
  \Big[
    \big(\mathrm{d}_A \beta\big)
    ,\,
    \alpha
  \Big]_i
  E^i
  \\
  \;=\;
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  +
  \Big[
    \alpha
    ,\,
    \big(\mathrm{d}_A \beta\big)
  \Big]_i
  E^i
  \\
  \;=\;
  \big(
    \mathrm{d}_A
    [\alpha,\beta]_i
  \big)
  E^i
  \end{array}
$$

Poisson bracket of electric with magnetic flux:

$$
  \begin{array}{l}
  \Big\{
    \textstyle{\int}
    \big( \mathrm{d}_A \alpha_i \big) 
    \wedge 
    E^i
    ,\,
    \textstyle{\int}
    \big( \mathrm{d}_A \beta_j \big) 
    \wedge
    F_A^j    
  \Big\}
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle
    \big[
      \mathrm{d}_A \alpha
      ,\,
      \beta_j
    \big]
    ,\,
    F_A^j
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle
    \big(
      \mathrm{d}_A \beta
    \big)
    ,\,
    \mathrm{d}_A
    \big(
      \mathrm{d}_A \alpha
    \big)
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \big\langle
    \mathrm{d}_A \alpha
    ,\,
    \beta
    ,\,
    F_A
  \big\rangle
  +
  \textstyle{\int}
  \big\langle
    \mathrm{d}_A \beta
    ,\,
    F_A
    ,\,
    \alpha
  \big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle  
    \mathrm{d}_A \alpha
    ,\,
    \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \mathrm{d}_A  \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \beta
    ,\,
    \underset{= 0}{
      \underbrace{
        \mathrm{d}_A F_A
      }
    }
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle  
    \mathrm{d} \alpha
    ,\,
    \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \mathrm{d}\beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \beta
    ,\,
    \mathrm{d} F_A
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \mathrm{d}
  \big\langle
    \alpha
    ,\,
    \beta
    ,\,
    F_A
  \big\rangle
  \\
  \;=\;
  0
  \end{array}
$$


## Related concepts

* **[[flux]]**
 
  * [[flux tube]]

  * [[flux quantization]]

  * [[flux compactification]]


## References


In [[electromagnetism]], with focus on torsion components that are argued to not generally commute:

* {#FreedMooreSegal07a} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *The Uncertainty of Fluxes*, Commun. Math. Phys. **271**  (2007) 247-274 &lbrack;[arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3)&rbrack;

* {#FreedMooreSegal07b} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *Heisenberg Groups and Noncommutative Fluxes*,  Annals Phys. **322** (2007) 236-285 &lbrack;[arXiv:hep-th/0605200](http://arxiv.org/abs/hep-th/0605200), [doi:10.1016/j.aop.2006.07.014](https://doi.org/10.1016/j.aop.2006.07.014)&rbrack;


In [[SU(2)]]-[[gauge theory]] (highlighted for the case of the [[first-order formulation of gravity]] but applying verbatim also to [[Yang-Mills theory]], cf. [there](Yang-Mills+theory#ReferencesPhaseSpaceAndCanonicalQuantization)):

* {#CattaneoPerez17} [[Alberto S. Cattaneo]], Alejandro Perez, *A note on the Poisson bracket of 2d smeared fluxes*, Class. Quant. Grav. **34** (2017) 107001 &lbrack;[arXiv:1611.08394](https://arxiv.org/abs/1611.08394), [doi:10.1088/1361-6382/aa69b4](https://doi.org/10.1088/1361-6382/aa69b4)&rbrack;


See also:

* Mikhail A. Savrov, *Commutator of Electric Charge and Magnetic Flux* &lbrack;[arXiv:2003.02225](https://arxiv.org/abs/2003.02225)&rbrack;


