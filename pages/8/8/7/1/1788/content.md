> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***



**Complete Topological Quantization of Higher Gauge Fields**
\linebreak
[ncatlab.org/schreiber/show/ICMS25](https://ncatlab.org/schreiber/show/ICMS25)

Plan:

1. [Completion of Higher Gauge Theories](#Part1)

2. [Their Complete Topological Quantization](#Part2)

3. [Application to Topological Quantum Materials](#Part3)


Motivation: 

* Global completion of [[11D supergravity]] ("[[M-theory]]"),

* and of its [[M5-brane]] [[probe brane|probes]] ("[[Theory X]]"),

* relatedly of [[FQH system|FQH]] [[anyons]] ("[[topological quantum]]").

\linebreak

{#Part1} **Part 1 -- Completion of Higher Gauge Theories**

Recall [[Maxwell's equations]] in [[vacuum]]:

$
  \mathrm{d} F_2 = 0
  ,\;
  \mathrm{d} \star_{1,3} F_2 = 0
  \mathrlap{\,.}
$

Suprprisingly good idea to rewrite this in

[[pre-metric electromagnetism|pre-metric or duality symmetric form]]

$
  \left.
  \begin{aligned}
  \mathrm{d} F_2 & = 0
  \\
  \mathrm{d} G_2 &= 0
  \end{aligned}
  \right\}\,,
  \;\;\;\;\;
  G_2 = \star_{1,3} F_2
$

In this vein, say that

**[higher Maxwell-type equations](/nlab/show/Gauss law#InHigherGaugeTheory)** 

on higher [[flux densities]]

$
  \vec F 
  \;\coloneqq\;
  \Big(
    F^{(i)} \in Omega^{deg_i}_{dR}(X^{1,d})
  \Big)_{i \in I}
$

are equations of the form

$
  \mathrm{d} \vec F
  \;=\;
  \vec P\big( \vec F  \big)
  \,,\;\;\;\;
  \star_{1,d} \vec F = \vec \mu\big( \vec F \big)
$

for

* $\vec P$ an $I$-tuple of graded-symemtric [[polynomials]],

* $\vec \mu$ an $I$-tuple of [[linear maps]]


**Examples**

[[RR-field]] in [[type IIA 10D supergravity]]:

$
 \mathrm{d} F_{2\bullet} = 0
 \Big\}
 \,,\;\;\;\;
 \star_{1,9} F_{2\bullet} = F_{10-2\bullet}
 ,.
$

[[self-dual higher gauge field]]:

$
  \mathrm{d} H_{2k+1} = 0
  \Big\}
  \,,\;\;\;\;\;
  \star_{1,4k+1} H_{2k+1} = H_{2k+1}
$

[[Maxwell-Chern-Simons field]] in minimal [[5D supergravity]]

$
  \left.
  \begin{aligned}
    \mathrm{d} F_2 & = 0
    \\
    \mathrm{d} F_3 & = \tfrac{1}{2} F_2 \wedge F_2
  \end{aligned}
  \right\}
  \,,\;\;\;\;
  F_3 = \star_{1,4} F_2
$

[[C-field]] in [[11D supergravity]]:

$
  \left.
  \begin{aligned}
    \mathrm{d} G_4 & = 0
    \\
    \mathrm{d} G_7 & = \tfrac{1}{2} G_4 \wedge G_3
  \end{aligned}
  \right\}
  \,,\;\;\;\;
  G_7 = \star_{1,10} G_4
$


\linebreak

now assume a [[globally hyperbolic spacetime]]

$
  X^{1,d} \simeq \mathbb{R}^{1,0} \times X^d
$

with [[Cauchy surface]]

$
  X^d \xhookrightarow{ \iota_t } \mathbb{R}^{1,0} \times X^d
$

and consider the time-local solution space

$
  LocSol_t
  \;\coloneqq\;
  \begin{array}{l}
    \text{ temporal germs of solutions }
    \\
    \text{ of the above EoMs around }\; \{t\} \times X^d 
  \end{array}
$

\linebreak

**Proposition.**

$
  LocSol_t
  \xrightarrow[\sim]{\phantom{--}\iota_t^\ast\phantom{--}}
  \Big\{
    \vec B
    \coloneqq
    \big(
      B^{(i)} \in \Omega^{deg_i}_{dR}(X^d)
    \big)_{i \in I}
    \;\Big\vert\;
    \mathrm{d}\vec B = \vec P(\vec B)
  \Big\}
$

so

* dual flux densities become [[canonical momenta]]

* Hodge duality relation disappears (absorbed in the iso)

* remaining differential relation is [higher Gauss law](/nlab/show/Gauss+law#InHigherGaugeTheory)

\linebreak

**Proposition:** Moreover:

$
  \Big\{
    \vec B
    \;\Big\vert\;
    \mathrm{d}\vec B = \vec P(\vec B)
  \Big\}
  \;\;
  \simeq
  \;\;
  \Omega^1_{dR}\big(X^d; \mathfrak{a}\big)_{cl}
$

for **characteristic $L_\infty$-algebra** $\mathfrak{a}$

connected [$L_\infty$-algebras](/nlab/show/L-infinity-algebra) of [[finite type]] are

$
  \begin{array}{ccc}
    L_\infty Alg^{ft}_{conn}
    &\xhookrightarrow{\phantom{--}}&
    dgcAlg^{op}
    \\
    \left(
      \mathfrak{g}
      ,\;
      \begin{array}{l}
        [-], [-,-], 
        \\
        [-,-,-], \cdots
      \end{array}
    \right)
    &\mapsto&
    \left(
    \wedge^\bullet \mathfrak{g}^{\vee}
    ,\,
    \mathrm{d}_{\vert \wedge^1 \mathfrak{g}^{\vee}}
    =
    \begin{array}{l}
      [-]^\ast + [-,-]^\ast +
      \\
      [-,-,-]^\ast + \cdots
    \end{array}
    \right)
  \end{array}
$

where $\mathfrak{g}$ is 

* an $\mathbb{N}$-[[graded vector space]]

* degreewise of finite dimension.

and [closed $L_\infty$-valued forms](/nlab/show/infinity-Lie+algebroid-valued+differential+form) are

$
  \Omega^1_{dR}\big(X; \mathfrak{g}\big)_{cl}
  \;\coloneqq\;
  Hom_{dgAlg}\Big(
    CE(\mathfrak{g})
    ,
    \Omega^\bullet_{dR}(X)
  \Big)
$

\linebreak

**Definition/Proposition**

For $\mathcal{A}$ a [[connected topological space]]

with abelian [[fundamental groups]] (for simplicity)

and $dim_{\mathbb{R}}\big(H^\bullet(\mathcal{A},\mathbb{R}) \lt \infty$

then its real [[Whitehead L∞-algebra]] $\mathfrak{l}\mathcal{A}$ is 

$
  (\mathfrak{l}\mathcal{A})_\bullet
  \coloneqq
  \pi_\bullet(\Omega \mathcal{A}) \otimes_{\mathbb{Z}} \mathbb{R}
$

with brackets uniquely determined by the condition that

$
  H^\bullet\big(
    CE(\mathfrak{l}\mathcal{A})
  \big)
  \;\simeq\;
  H^\bullet\big(
   \mathcal{A}; \mathbb{R}
  \big)
$

\linebreak

**Examples**

[[electromagnetism]]: $\mathfrak{a} = \mathfrak{l}(B \mathrm{U}(1)^2)$

[[self-dual higher gauge field]]: $\mathfrak{a} = \mathfrak{l} B^{2k} \mathbb{Z}$

[[RR-field]]: $\mathfrak{a} = \mathfrak{l}(B \mathrm{U})$

[[Maxwell-Chern-Simons field]]: $\mathfrak{a} = \mathfrak{l}S^2$

[[C-field]]: $\mathfrak{a} = \mathfrak{l}S^4$

\linebreak

**Definition/Proposition.**

The *total flux* of a [[flux density]] $\vect F$

is its image in [[non-abelian de Rham cohomology]]

$
 H^1_{dR}\big(
   X;\, \mathfrak{a}
 \big)
 \;\simeq\;
 \Omega^1_{dR}\big(X; \mathfrak{a}\big)_{cl}\big/ \text{concordance}
$

\linebreak

**Definition/Proposition.**

Denoting by

* $L^{\mathbb{Q}}\mathcal{A}$ the [[rationalization]] of $\mathcal{A}$,

* $L^{\mathbb{R}}\mathcal{A}$ its [[extension of scalars]] to the reals

* $\eta^{\mathbb{R}} \colon \mathcal{A} \longrightarrow L^{\mathbb{R}} \mathcal{A}$ the comparison mao,

the *nonabelian character map* is

$
  \begin{array}{ccc}
    \begin{array}{c}
    \text{charge in}
    \\
    \text{nonabelian cohomology}
    \end{array}
    &character&
    \begin{array}{c}
    \text{total flux in}
    \\
    \text{nonabelian dR-cohomology}
    \end{array}
    \\
    H^1(X;\,\Omega \mathcal{A})
    &\xrightarrow{\phantom{--} ch^{\mathcal{A}} \phantom{--}}&
    H^1_{dR}\big(X;\,\mathfrak{a}\big)
    \\
    = && \simeq
    \\
    \pi_0\, Map\big(X, \mathcal{A}\big)
    &\xrightarrow{\phantom{--} \eta^{\mathbb{R}} \phantom{--}}&
    \pi_0\, Map\big(X, L^{\mathbb{R}}\mathcal{A}\big)
  \end{array}
$

\linebreak

**Flux quantization** of a higher gauge theory is

choice of $\mathcal{A}$ with $\mathfrak{l}\mathcal{A}\simeq \mathfrak{a}$

Promotion of flux densities to pairs $(\vec F, \chi)$ for 

$\chi$ a charge whose character is the total flux of $\vec F$:

$
  \begin{array}{ccccc}
    \Omega^1_{dR}\big(
      X^d; \mathfrak{a}
    \big)_{cl}
    &\xrightarrow{ [-] }&
    H^1_{dR}\big(
     X^d;\,
     \mathfrak{a}
    \big)
    &\xleftarrow{ ch^{\mathcal{A}} }&
    H^1(X^d; \Omega \mathcal{A})
    \\
    \vec F
    &\mapsto&
    [\vec F] = ch^{\mathcal{A}}(\chi)
    &\leftarrow\!\!\!\vert&
    \chi
  \end{array}
$

\linebreak

There is either none of infinitely many admissible $\mathcal{A}$

$\Rightarrow$ is a *hypothesis* about the correct model for given physics

**Examples**

[[Dirac charge quantization]] of EM-field: 
$\mathcal{A} \equiv B \mathrm{U}(1)^2$

Hyothesis h on 5D MCS-field:
$\mathcal{A} \equiv S^2 $


[[Hypothesis H]] on [[C-field]]:
$\mathcal{A} \equiv S^4 $



(...)
















\linebreak

{#Part2} **Part 2 -- Their Complete Topological Quantization**

(...)

\linebreak

{#Part3} **Part 3 -- Application to Topological Quantum Materials**

(...)







