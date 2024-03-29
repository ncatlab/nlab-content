
> This entry is about the concept in [[physics]]. For the concept in [[algebra]] see at _[[free field]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
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

A [[field (physics)|field]] [[theory (physics)|theory]] in [[physics]] is called a _free field theory_ if it describes standard [[dynamics]] of fields without any [[interaction]]. Otherwise it is called an _[[interacting field theory]]_.

There is some freedom in formalizing precisely what this means. At the very least the [[equations of motion]] of a free field theory should be [[linear differential equations]]. In [[relativistic field theory]] over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] one typically requires that the [[linear differential equation]] [[equation of motion|of motion]] is, after [[gauge fixing]], in fact the [[wave equation]] or [[Klein-Gordon equation]].


## Definition

### In covariant phase space geometry/multisymplectic geometry

We describe free field theory in the language of [[covariant phase spaces]] of [[local Lagrangians]] and their [[multisymplectic geometry]].

Let $\Sigma = (\mathbb{R}^{d-1;1}, \eta)$ be [[Minkowski spacetime]].
Write the canonical [[coordinates]] as

$$
  \sigma^i \;\colon\; \Sigma \longrightarrow \mathbb{R}
  \,.
$$

Let $(X,g)$ be a [[vector space]] $X$ equipped with a [[bilinear form]] $g$ that makes it a [[Riemannian manifold]]. Write its canonical coordinates as

$$
  \phi^a \;\colon\; X \longrightarrow \mathbb{R}
  \,.
$$

Let then $X \times \Sigma \to \Sigma$ be the [[field bundle]].
Its first [[jet bundle]] then has canonical coordinates

$$
  \{ \sigma^i \}, \{\phi^a\}, \{\phi^a_{,i}\} \;\colon\; j_\infty^1(\Sigma \times X) \longrightarrow X
  \,.
$$

+-- {: .num_defn #FreeFieldLocalLagrangian}
###### Definition


The [[local Lagrangian]] for [[free field theory]] with this [[field bundle]] is

$$
  L  
   \coloneqq
  \left(
     \frac{1}{2} g^{i j} \eta_{a b} \phi^a_{,i} \phi^a_{,j}
  \right)
  \wedge
  \mathbf{d}\sigma^1 \wedge \cdots \wedge \mathbf{d}\sigma^d
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The [[canonical momentum]]-densities  for the free field local Lagrangian of def. \ref{FreeFieldLocalLagrangian} are

$$
  \begin{aligned}
    p_a^i \wedge \mathbf{d}\sigma^1 \wedge \cdots \wedge \mathbf{d}\sigma^d
      & \coloneqq 
    \frac{\partial}{\partial u^a_i} L
    \\
      & =
    \left(
       g^{i j} \eta_{a b} \phi^a_{,j}
    \right)
    \wedge
    \mathbf{d}\sigma^1 \wedge \cdots \wedge \mathbf{d}\sigma^d    
  \end{aligned}
$$

=--

+-- {: .num_remark}
###### Remark

So the boundary term $\theta$ in [[variational calculus]], 
(see [this remark](covariant+phase+space#CanonicalThetaDensityInLocalCoordinates) at _[[covariant phase space]]_ ) is

$$
  \begin{aligned}
    \mathbf{d}u^a 
     \wedge
    \iota_{\partial_i}
    \left(
      \frac{\partial}{\partial \phi^a_{,i}}L 
    \right)
     & =  
    p^i_a \wedge (\iota_{\partial_{\sigma^i}} vol) \wedge \mathbf{d}u^a
    \\
    & =  p^i_a \wedge dq_i^a
    \,,
  \end{aligned}
$$

where in the last line we adopted the notation of [this remark](#multisymplectic+geometry#CanonicalFormInGoodCoordinates) at _[[multisymplectic geometry]]_.

This shows that the canonical [[multisymplectic form]]
is the "covariant symplectic potential current density" 
which is induced by the free field Lagrangian.

=--



### In BV-formalism

#### Kinematics and dynamics

In the formalization of [[perturbation theory]] via [[BV-quantization]] as in ([Costello-Gwilliam](#CostelloGwilliam)), a free field theory is given by a [[BV-complex]] that arises from the following data.

The following appears for instance as ([Gwilliam 2.6.2](#Gwilliam)).

+-- {: .num_defn #FreeFieldTheory}
###### Definition

A **free field theory** ([[local quantum field theory|local]], [[Lagrangian]]) is the following data

**[[kinematics]]**:

* A [[smooth manifold]] $X$ ("[[spacetime]]"/"[[worldvolume]]");

* a $\mathbb{Z}$-[[graded object|graded]] [[complex numbers|complex]] [[vector bundle]] $E \to X$ (the "[[field bundle]]" containing also in general [[antifields]] and [[ghosts]]);

* equipped with a [[bundle]] [[homomorphism]] (the "[[antibracket]] [[density]]")

  $$
    \langle -,-\rangle_{loc} \;\colon\; E \times E \to Dens_X
  $$

  from the fiberwise [[tensor product]] of $E$ with itself to the compex [[density bundle]] which is fiberwise

  * non-degenerate

  * anti-symmetric

  * of degree -1

(See also at _[[Verdier duality]]_.)

Write $\mathcal{E}_c \coloneqq \Gamma_{cp}(E)$ for the space of [[sections]] of the [[field bundle]] of [[compact support]]. Write

$$
  \langle -,-\rangle
  \;\colon\;
  \mathcal{E}_c
  \otimes
  \mathcal{E}_c
  \to 
  \mathbb{C}
$$

for the induced pairing on sections

$$
  \langle \phi, \psi\rangle
  =
  \int_{x \in X} \langle \phi(x), \psi(x)\rangle_{loc}
  \,.
$$

The paring being non-degenerate means that we have an [[isomorphism]] $E \stackrel{\simeq}{\to} E^* \otimes Dens_X$ and we write

$$
  E^! \coloneqq E^* \otimes Dens_X
  \,.
$$

**[[dynamics]]**

* A [[differential operator]] on sections of the [[field bundle]] 

  $$
    Q \;\colon\; \mathcal{E} \to \mathcal{E}
  $$
 
  of degree 1 such that

  1. $(\mathcal{E}, Q)$ is an [[elliptic complex]];

  1. $Q$ is [[self-adjoint operator|self-adjoint]] with respect to $\langle -,-\rangle$ in that for all [[field (physics)|fields]] $\phi,\psi \in \mathcal{E}_c$ of homogeneous degree we have $\langle \phi , Q \psi\rangle = (-1)^{{\vert \phi\vert}} \langle Q \phi, \psi\rangle$.

=--

+-- {: .num_remark}
###### Remark

From this data we obtain:

* The [[action functional]] $S \colon \mathcal{E}_c \to \mathbb{C}$ of this corresponding free field theory is

  $$
    S \;\colon\; \phi \mapsto \int_X \langle \phi, Q \phi\rangle
    \,.
  $$

* The [[classical BV-complex]] is the [[symmetric algebra]] $Sym  \mathcal{E}^!_c$ of [[compact support|compactly suppported]] [[sections]] of $E^!$ equipped with the induced action of the differential $Q$ and the pairing 

  $$ 
    \{\alpha,\beta\} \coloneqq  \int_{x \in X} \langle \alpha(x), \beta(x)\rangle
    \,.
  $$

  See below at _[The classical observables](#TheClassicalObservables)_ for more.

* The [[quantum BV-complex]] 

  $$
    Obs^q \coloneqq (Sym \mathcal{E}^!_c[ [\hbar] ], Q + \hbar \Delta)
  $$

  is the deformation of the above to the [[symmetric algebra]] tensored with the [[formal power series]] in $\hbar$ ("[[Planck's constant]]") $Sym(\mathcal{E}^!)[ [\hbar] ]$  and differential $Q + \hbar \Delta$ with [[BV-Laplacian]] defined to vanish on $Sym^{\leq 1}$, given by 

  $$
    \Delta (\alpha \cdot \beta) \coloneqq \{\alpha,\beta\}
  $$

  for $\alpha,\beta \in \mathcal{E}^!$ and extended by the formula

  $$
    \Delta(a \cdot b)
    \coloneqq
    (\Delta a) \cdot b
    + 
    (-1)^{deg(a)}
    a \cdot (\Delta b)
    + 
    \{a,b\}  
    \,.
  $$

  See below at _[The quantum observables](#TheQuantumObservables)_ for more.

A closed element $\mathcal{O} \in Obs^q$ is an [[observable]] and its formal [[path integral]] [[expectation value]] $\langle \mathcal{O}\rangle$ is its image in the [[cochain cohomology]] $H^\bullet Obs^q$. Via the [[homological perturbation lemma]] this may be computed in [[perturbation theory]] (order by order in $\hbar$) in terms of [[Feynman diagrams]].

In a non-free field theory the differential would have an additional perturbation of the complex  by an [[interaction]] term $I$ to 

$$
  Q + \{I,-\} + \hbar \Delta
  \,.
$$

=--

[[!include action (physics) - table]]

#### The classical observables
 {#TheClassicalObservables}


For $(E, Q, \langle-, -\rangle_{loc})$ a free field theory, def. \ref{FreeFieldTheory}, write 

$$
  E^! \coloneqq E^\ast \otimes Dens_X
$$

and accordingly write $\overline{\mathcal{E}^!}$ for its [[distribution|distributional]] [[sections]]. This is the distributional dual to the smooth sections $\mathcal{E}$ of $E$.

+-- {: .num_defn #ClassicalObservables}
###### Definition

The complex of **global classical observables** of the free field theory $(E,Q, \langle-,- \rangle_{loc})$ is the [[classical BV-complex]]

$$
  Obs^{cl} \coloneqq (Sym \mathcal{E}^!_c, Q)
$$

given by the [[symmetric algebra]] of dual sections and quipped with the dual of the differential (which we denote by the same letter) defined on generators and then extended as a graded [[derivation]] to the full [[symmetric algebra]].

The [[factorization algebra]] of local classical observables is the [[cosheaf]] of these observables which assigns to $U \subset X$ the complex

$$
  Obs^{cl} \colon U \mapsto (Sym \mathcal{E}^!_c(U), Q)
  \,.
$$

=--

in ([Gwilliam](#Gwilliam)), this is def. 5.3.6.



#### The quantum observables
 {#TheQuantumObservables}

There is a canonical [[BV-quantization]] of the [above classical observable](#TheClassicalObservables) of a free field theory
given by defining the [[BV Laplacian]] as follows.

+-- {: .num_defn #TheStandardBVLaplacian}
###### Definition

For $(E, Q, \langle -,-\rangle_{loc})$ a free field theory, def. \ref{FreeFieldTheory}, the **standard [[BV Laplacian]]** 

$$
  \Delta 
  \colon
  Sym \mathcal{E}^!_c \to Sym \mathcal{E}^!_c
$$

is given on generators $a,b \in Sym^1 \mathcal{E}^!_c$ of homogeneous degree by

$$
  \Delta(a \cdot b) \coloneqq \{a,b\}
$$

and then extended to arbitrary elements by the formula

$$
  \Delta(a \cdot b)
  \coloneqq
  (\Delta a) \cdot b
  + 
  (-1)^{deg(a)}
  a \cdot (\Delta b)
  + 
  \{a,b\}  
$$

=--

In ([Gwilliam](#Gwilliam)) this is construction 2.4.9 (also construction 3.1.6, and section 5.3.3).

+-- {: .num_defn #QuantumObservables}
###### Definition

For $(E, Q, \langle -,-\rangle_{loc})$ a free field theory, def. \ref{FreeFieldTheory} its complex of **[[quantum observables]]** is then the corresponding [[quantum BV-complex]] deformation of the classical BV-complex, def. \ref{ClassicalObservables}, given by the standard 
BV-Laplacian of def.\ref{TheStandardBVLaplacian}

$$
  Obs^{q} \colon U \mapsto
  \left(
    Sym(\mathcal{E}^!_c(U))[ [ \hbar ] ], Q + \hbar \Delta
  \right)
  \,.
$$

=--

In ([Gwilliam](#Gwilliam)) this is def. 5.3.9.

## Properties

### Characterization of the quantum observables

We characterize the [[cochain complex]] $Obs^q$ of [[quantum observables]] of def. \ref{QuantumObservables} by an equivalent but small complex built from just the [[cochain cohomology]] of the [[elliptic complex]] of [[field (physics)|fields]] $(\mathcal{E}, Q)$.


+-- {: .num_defn #TheQuantumBVComplexOnTheCohomologyOfTheFieldComplex}
###### Definition

For $(E, Q, \langle -,-\rangle_{loc})$ a free field theory, def. \ref{FreeFieldTheory}, the global pairing constitutes a dg-[[symplectic vector space]] $(\mathcal{E}, Q, \langle -,-\rangle)$, which descends to the [[cochain cohomology]] to a graded symplectic vector space $(H^\bullet(\mathcal{E}, \langle -,-\rangle)$;
hence by def. \ref{TheStandardBVLaplacian} there is a standard [[BV-Laplacian]] $\Delta_{H^\bullet\mathcal{E}}$. Write

$$
  \mathcal{BVQ}(H^\bullet \mathcal{E})
  \coloneqq
  ( Sym (H^\bullet(\mathcal{E}))^*, \Delta_{H^\bullet \mathcal{E}} )
$$

for the corresponding [[quantum BV-complex]].

=--

This is part of ([Gwilliam, prop. 2.4.10, prop. 5.5.1](#Gwilliam)),

> Handle the following with care for the moment.

+-- {: .num_prop}
###### Proposition

For a free field theory $(E,Q,\langle-,- \rangle_{loc})$, def. \ref{FreeFieldTheory}, the complex of quantum observables $Obs^q$, def. \ref{QuantumObservables} is [[quasi-isomorphism|quasi-isomorphic]] to
the BV-quantization of the cohomology of the field complex, given by def. \ref{TheQuantumBVComplexOnTheCohomologyOfTheFieldComplex}

$$
  Obs^q
  \simeq
  \mathcal{BVQ}(H^\bullet(\mathcal{E}))
  \,.
$$

=--

This is ([Gwilliam, prop. 5.5.1](#Gwilliam)).

The proof is supposedly along the lines of ([Gwilliam, section 2.5](#Gwilliam)), applying the [[homological perturbation lemma]].

+-- {: .num_prop}
###### Proposition

The bracket $\{-,-\}$ on the complex of quantum observables $Obs^q$ of def. \ref{QuantumObservables} descends to a bracket on [[cochain cohomology]], making $(H^\bullet (Obs^q), \{-,-\})$ into a graded [[symplectic vector space]].

=--

+-- {: .proof}
###### Proof

Let $a,b \in Obs^q$ be closed elements of homogeneous degree. Then by the compatibly of $\Delta$ with $\{-,-\}$ also $\{a,b\}$ is closed:

$$
  \Delta \{a,b\}
  = 
  \{\Delta a, b\} \pm \{a , \Delta b\} = 0
  \,.
$$

Let in addition $c \in Obs^q$ be any element. Then

$$
  \begin{aligned}
    \{a, b + \Delta c\}
    &= 
    \{a,b\} + \{a, \Delta c\}
    \\ 
    & = \{a,b\} + \Delta (a \cdot (\Delta b)) - (\Delta a)\cdot b   -a \cdot (\Delta^2 b)
    \\
    & = \{a,b\} + \Delta (a \cdot (\Delta b))
  \end{aligned}
$$

and hence the cohomology class of $\{a,b\}$ is independent of the representative cocycle $b$, and similarly for $a$.

=--

## Examples
 {#Examples}

### 0-Dimensional free field theory
 {#0DimensionalFreeFieldTheory}

A degenerate but instructive class of examples to compare to is the case where $X = *$ is the 0-dimensional connected manifold: the point. (See ([Gwilliam 2.3.1](#Gwilliam))).

In this case 

$$
  E = V \oplus V^*[-1]
$$ 

is the [[direct sum]] of a vector space and its formal dual shifted in degree. The pairing is the canonical pairing between a vector space and its dual.

If $\{x^i \colon V \to \mathbb{R}\}_i$ is a [[basis]] for functional on $V$ and $\{\xi_i\}$ is the corresponding basis of functions on $V^*[-1]$, then the [[antibracket]] in this case is 

$$
  \{
    X^i, x^j
  \}
  = 0
  \;\;\;
  \{\xi_i, \xi_j\} = 0
  \;\;\;
  \{x^i, \x_j\} = \delta^i_j
  \,.
$$

The [[BV-Laplacian]] in this basis is

$$
  \Delta = \sum_{i = 1}^n \frac{\partial}{\partial x^i} \frac{\partial}{\partial \xi_i}
  \,.
$$

The [[action functional]] is a [[Gaussian distribution]] over $V$ defined by a matrix $A = (a_{i j})$. The corresponding differential is

$$
  Q = \sum_{i,j =1}^n x^i a_{i j} \frac{\partial}{\partial \xi_i}
  \,.
$$

Hence for a field of the form

$$
  \phi = \sum_{i = 1}^n \phi^i \xi_i
$$

we have the [[action functional]]

$$
  \begin{aligned}
    \exp(S(\phi))
    & =
    \exp(-\langle \phi , Q \phi\rangle)
    \\
    & = \exp( - \phi^i a_{k j} \phi^j \langle \xi_i, x^k   \rangle )
    \\
    & = \exp(- \phi^i a_{i j} \phi^j )
  \end{aligned}
$$

### Locally free field theories

Some [[sigma-model]] quantum field theories have the property that they are free _locally_ on their [[target spaces]]. Under good conditions then [[quantization]] of free field theory locally yields a [[sheaf]] of [[quantum observables]] on [[target space]] from which the full quantization of the field theory may be reconstructed.

A famous example of this is the [[topological twist|topologically twisted]][[2d (2,0)-superconformal QFT]] (see there for more, and see ([Gwilliam, section 6](#{#Gwilliam}) for the description in terms of [[factorization algebras]]).



## Related concepts

* [[Wick algebra]]

* [[Gaussian probability distribution]], [[Gaussian integral]]

* [[Wick's lemma]]

* [[gauge theory]]


## References

Discussion of free field theories and their [[quantization]] on [[globally hyperbolic Lorentzian manifolds]] is in 

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))

Discussion on Euclidean manifolds and in terms of [[BV-formalism]] is in


* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html), [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf))
 

* {#Gwilliam} [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([[GwilliamThesis.pdf:file]])

* [[Owen Gwilliam]], [[Rune Haugseng]], _Linear Batalin-Vilkovisky quantization as a functor of ∞-categories_ ([arXiv:1608.01290](https://arxiv.org/abs/1608.01290))
 

[[!redirects free field theories]]

[[!redirects free field]]
[[!redirects free fields]]


[[!redirects free quantum field theory]]
[[!redirects free quantum field theories]]


[[!redirects free quantum field]]
[[!redirects free quantum fields]]

