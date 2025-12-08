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
    [\vec F] = ch^{\mathcal{A}}([\chi])
    &\leftarrow\!\!\!\vert&
    [\chi]
  \end{array}
$

\linebreak

There is either none of infinitely many admissible $\mathcal{A}$

$\Rightarrow$ is a *hypothesis* about the correct model for given physics

**Examples**

[[Dirac charge quantization]] of EM-field: $\mathcal{A} \equiv B \mathrm{U}(1)^2$

[Hypothesis K](/nlab/show/D-brane+charge+quantization+in+K-theory) on the [[RR-field]]

[Hypothesis h](/schreiber/show/Renormalization+of+Wilson+Loops) on [[Maxwell-Chern-Simons field]]: $\mathcal{A} \equiv S^2 $

[[Hypothesis H]] on [[C-field]]: $\mathcal{A} \equiv S^4$

\linebreak

Finally, the full completed higher gauge field 

is not just the flux densities $\vec F$, a charge $\chi$

and an *[[equality]]* $[\vec F] = ch[\chi]$, but involves

a [[gauge transformation]]/[[homotopy]] $\widehat{A}$ exhibiting this equality 

which out the "be" the [[gauge potentials]].

The globally completed phase space is, schematically:

$
  PhsSpc
  \;\coloneqq\;
  \left\{
  \begin{array}{ll}
    \text{gauge potentials} & \vec F \in \Omega^1_{dR}(X^d;\mathfrak{a})
    \\
    \text{local charges} & \chi \in Map(X^d, \mathcal{A})
    \\
    \text{gauge potentials} & \widehat{A} \colon \vec F \Rightarrow \chi
  \end{array}
  \right\}
$

In reality this is the [smooth ∞-groupoid](/nlab/show/smooth+infinity-groupoid) 

which as such is the [[homotopy pullback]] 

of the character map from total flux to flux densities.

Essentially. In the following we will only need 

the *[[shape modality|shape]]* of the space space, 

which turns out to be given by a concrete formula.


\linebreak

{#Part2} **Part 2 -- Their Complete Topological Quantization**

[[observables]] are the [[smooth functions]] on [[phase space]]

$
  O \,\colon\,
  PhsSpc
  \longrightarrow
  \mathbb{C}
$

the *topological observables* are the *locally constant* functions

$
  O \,\colon\,
  PhsSpc
  \longrightarrow
  \flat \mathbb{C}
$

(where $\flat \mathcal{C}$ is the discrete set [[underlying]] $\mathcal{C}$)

\linebreak

**Proposition**

The topological observables 

$
  PhsSpc \xrightarrow{\phantom{--}} \flat \mathbb{C}
$

are naturally equivalent to the maps

$
  \pi_0 \, Map(X^d, \mathcal{A}) 
    \xrightarrow{\phantom{--}}
  \mathcal{C}
$

out of the [[connected components]] of the [[mapping space]] 

from the [[Cauchy surface]] into the [[classifying space]],

\linebreak

"Topologically, fields are only seen through their charges."


\linebreak

Moreover, realistic observables are 

supported on finitely many components, hence:

$
  TopObs 
  \;\coloneqq\;
  \mathbb{C}\big[
    \pi_0 \, Map(X^d, \mathcal{A})
  \big]
  \,\simeq\,
  H_0\big(
    Map(X^d, \mathcal{A})
    ;\,
    \mathbb{C}
  \big)
$

\linebreak

More specifically, we look at **field [[solitons]]**, 

whose charge [vanishes at infinity](/nlab/show/vanishing+at+infinity)

To formalize this, consider a [[pointed topological space]]

$ 
 \big( X^d_{dom}, \infty \big)
 \in
 Top^\ast
$

with basepoint thought of as a [[point at infinity]]:

$
 X^d \,\simeq\, X^d_{dom} \setminus \{\infty\}
$

Also think of $\mathcal{A}$ as pointed by 0-charge

$$
  \big(\mathcal{A}, 0\big) \in Top^\ast
  \,.
$$

Then a pointed map $\chi \in Map^\ast\big(X^d_{dom}, \mathcal{A}\big)$ 

*literally* takes the value $0$ at $\infty$

$
 \begin{array}{ccc}
    X^d_{dom} &\xrightarrow{\phantom{--} \chi \phantom{--}}&
    \mathcal{A}
    \\
    \uparrow
    &&
    \uparrow
    \\
    \{\infty\} &\xrightarrow{\phantom{----}}& \{0\}
 \end{array}
$

\linebreak

So the *solitonic topological observabes* are

$
  TopObs
  \,\coloneqq\,
  \mathbb{C}\Big[
    Map^\ast\big(X^d_{dom}, \mathcal{A}\big)
  \Big]
$

\linebreak

Question: What is the quantum operator product $\star$ on $TopObs$?

[Feynman 1948](/nlab/show/path integral#QuantumCommutatorsAreTimeOrderedOrdinaryProducts):
the time-ordered ordinary product 

e.g. for field operators $\phi$ and their [[canonical momenta]]:

$$
  \begin{array}{rcr}
    \big\langle
    \pi(t, \vec x)
    \star
    \phi(t, \vec y)
    \big\rangle
    &=&
    \underset{\underset{\epsilon \to_+ 0}{\longrightarrow}}{\lim}
    \big\langle
      \pi(t + \epsilon, \vec x)
      \cdot
      \phi(t, \vec y)
    \big\rangle
    \\
    -
    \big\langle
    \pi(t, \vec x)
    \star
    \phi(t, \vec y)
    \big\rangle
    &&
    -
    \underset{\underset{\epsilon \to_+ 0}{\longrightarrow}}{\lim}
    \big\langle
      \pi(t + \epsilon, \vec x)
      \cdot
      \phi(t, \vec y)
    \big\rangle
  \end{array}
$$

\linebreak

The analogue is still true for [[light front quantization]]

with respect to ordering in the light-front parameter 
$X^+ \coloneqq X^0 + x^1$.

So consider light-fron quantization on spacetime 

$
  \begin{aligned}
    X^{1,d}
    &\simeq\,
    \mathbb{R}^{1,1} \times X^{d-1}
    \\
    X^d
    & \simeq
    \mathbb{R}^1 \times X^{d-1}
    \\
    X^d_{dom} 
    & =
    \mathbb{R}^1_{\cup \{\infty\}} \wedge X^{d-1}_{dom}
  \end{aligned}
$

For topological observables which are necessarily $x^0$-independent

their light-front ordering is their $x^1$-ordering.

This is given by the *[[Pontrjagin product]]*/[fundamental](/nlab/show/fundamental+group)[[group algebra]] on

$
  \begin{aligned}
  TopObs
  & =
  H_0\Big(
    Map^\ast\big(
      \mathbb{R}^1_{\cup \{\infty\}}
      \wedge
      X^d_{dom}
    \big)
  \Big)
  \\
  & \simeq
  H_0\Big(
    \Omega
    Map^\ast\big(
      X^d_{dom}
    \big)
  \Big)  
  \\
  & \simeq
  \mathbb{C}\Big[
    \pi_1
    \,
    Map^\ast\big(
      X^d_{dom}
    \big)
  \Big]
  \end{aligned}
$

induced under pushforward in homology from

$
  \begin{array}{ccc}
    \Omega M \times \Omega M
    &\xrightarrow{\phantom{--} \star \phantom{--}}&
    \Omega M
    \\
    \big( \ell_2, \ell_1 \big)
    &\mapsto&
    \ell_2 \star \ell_1 
    &
    \colon\;
    s \,\mapsto\,
    \begin{array}{lcl}
      \ell_1(s) & \vert & s \leq \tfrac{1}{2}
      \\
      \ell_2(s) & \vert & s \geq \tfrac{1}{2}
    \end{array}
  \end{array}
$















(...)

\linebreak

{#Part3} **Part 3 -- Application to Topological Quantum Materials**

(...)







