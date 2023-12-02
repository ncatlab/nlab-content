
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

In plain [[electromagnetism]], the [[canonical momentum]] of the [[gauge potential]] $A$ is proportional (by constants to be ignored in the following) to the electric flux density $\star F$ (where $F$ is the [[Faraday tensor]] [[flux density]] and $\star$ is the [[Hodge star operator]] on the given [[spacetime]] [[pseudo-Riemannian manifold]]), which however means that the the Poisson bracket of the magnetic flux density $F \equiv \mathrm{d}_{dR} A$ with the electric flux density is a total derivative (cf. eg. [Blaschke & Gieres 2021 (5.5)](Yang-Mills+theory#BlaschkeGieres21)), so that the bracket of the integrated fluxes $\Phi_E$ and $\Phi_B$ through given [[orientable manifold|orientable]] [[closed manifold|closed]] surfaces $S_E$ and $S_B$, respectively, actually vanishes (cf. [FMS07b (3.6)](#FreedMooreSegal07b) and Prop. \ref{PoissonBracketBetweenElectricAndMagneticFluxes} below):

\[
  \label{CommutingAbelianFluxes}
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
\]

The thrust of [FMS 07a](#FreedMooreSegal07a), [07b](#FreedMooreSegal07b) is the claim that this bracket becomes non-vanishing if torsion-components of the fluxes (through their enhancement to [[ordinary differential cohomology]]) are retained, but it seems that this is ultimately by definition ([FMS07a, Def. 1.29](#FreedMooreSegal07a); [FMS07b (3.28)](#FreedMooreSegal07b)) more than by derivation from first principles.

On the other hand, for [[non-abelian group|non-abelian]] [[gauge group]], a careful analysis of the (somewhat subtle) Poisson brackets reveals ([Cattaneo & Perez 2017](#CattaneoPerez17)) that the electric fluxes -- understood as flux densities integrated against [[Lie algebra]] valued functions $\alpha$ -- have a non-trivial bracket among *themselves* (Prop. \ref{PoissonBracketBetweenElectricFluxes}):

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

Consider a [[metric Lie algebra]] $\mathfrak{g}$ -- such as [[line Lie algebra|$\mathfrak{u}(1)$]] or  [[su(n)|$\mathfrak{su}(n)$]], [[so(n)|$\mathfrak{so}(n)$]] via their [[Killing forms]], or any [[direct sum]] of these. 

For 3+1 dimensional [[Yang-Mills theory]] with [[gauge group|gauge]] Lie algebra $\mathfrak{g}$, we discuss ([below](#ThePoissonBracketOfIntegratedFluxes)) the [[Poisson bracket]] of integrals (against [[Lie algebra]]-valued functions) of [[flux densities]] ([[curvature 2-forms]]) over [[oriented manifold|oriented]] [[closed manifold|closed]] [[surfaces]], following [Cattaneo & Perez 2017](#CattaneoPerez17) (where this is discussed for the special case $\mathfrak{g} =$ [[su(2)|$\mathfrak{su}(2)$]], cf. Ex. \ref{TheLieAlgebrasu2}). 

The Poisson bracket of electric fluxes among themselves is equation (7) in [CP17](#CattaneoPerez17), and to warm-up we spell out the relevant computation in detail (Prop. \ref{PoissonBracketBetweenElectricFluxes} below, which also provides a rigorous proof of the abelian case (eq:CommutingAbelianFluxes)). 
Then we similarly compute the bracket between electric and magnetic fluxes (Prop. \ref{PoissonBracketBetweenElectricAndMagneticFluxes} below, which seems not to discussed elsewhere in the literature).

The computations are standard and straightforward, but since, as usual, the results depend crucially on delicate signs, we go into full detail.

\linebreak

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

The following discussion is all about [[Lie algebra-valued differential form|$\mathfrak{g}$-valued differential forms]], being elements of the [[tensor product]] $\Omega^\bullet_{dR} \otimes \mathfrak{g}$ of the [[de Rham algebra]] on a given [[smooth manifold]] with the given [[Lie algebra]].

The primary example are $\mathfrak{g}$-valued 1-forms

\[
  \label{GaugePotential}
  A 
    \;\equiv\; 
  A^i \otimes t_i 
  \;\in\;
  \Omega^1_{dR} \otimes \mathfrak{g}
  \,,
\]

which are going to represent the (local) [[gauge potential]] of $\mathfrak{g}$-[[Yang-Mills theory]].

In writing (Lie- or Poisson-)brackets of such [[Lie algebra-valued differential form|$\mathfrak{g}$-valued differential forms]], we mean to (1.) take the [[wedge product]] of the bare [[differential forms]] *in the given order* and (2.) apply the bracket to the [[coefficients]], 

\[
  \label{LieBracketOnLieAlgebraValuedDifferentialForms}
  \omega, \gamma \in \Omega^\bullet_{dR} \otimes \mathfrak{g}
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  [ \omega , \gamma ]
  \,\coloneqq\,
  \omega^i \wedge \gamma^j 
  \otimes
  [t_i, t_j]
  \,.
\]

This bracket makes [[Lie algebra-valued differential forms|$\mathfrak{g}$-valued forms]] into a [[super Lie algebra]]:

\[
  \label{GradedSkewSymemtryOfLieBracketOnLieAlgValuedForms}
  \begin{array}{l}
    \omega \,\in\, \Omega_{dR}^p \otimes \mathfrak{g}
    \\
    \omega' \,\in\, \Omega_{dR}^{p'} \otimes \mathfrak{g}
  \end{array}
  \;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;
  \big[ \omega , \omega' \big]
  \;=\;
  -(-1)^{p p'}
  \big[ \omega' , \omega \big]
  \,.
\]

For example, the Lie bracket of the [[gauge potential]] 1-form  (eq:GaugePotential) with itself is:

\[
  \label{BracketOfGaugePotentialWithItself}
  [ A , A ]
  \;\equiv\;
  A^j \wedge A^k \otimes [t_i, t_j]
  \;=\;
  f^i{}_{j k} 
  \, 
  A^j \wedge A^k \otimes t_i
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

\[
  \label{AAX}
  \big[A, [A, X]\big]
  \;=\;
  \big[ [A,A], X \big]
  -
  \big[A, [A, X]\big]
  \;\;\;\;
  \text{and hence}
  \;\;\;\;
  \big[A, [A, X]\big]
  \;=\;
  \tfrac{1}{2}
  \big[ [A,A], X \big]
  \,.
\]

Given a [[gauge potential]] $A$ as above (eq:GaugePotential), the *[[covariant derivative]]* is the sum of the [[de Rham differential]] with the operation $[A,-]$ (eq:LieBracketOnLieAlgebraValuedDifferentialForms):

\[
  \label{CovariantDerivative}
  \mathrm{d}_{A} X
  \;\equiv\;
  \mathrm{d} X + [A, X]
  \;=\;
  \mathrm{d} X^\bullet + f^\bullet{}_{j k} A^j \wedge X^k
  \,.
\]

Since the [[de Rham differential]] $\mathrm{d}$ is a degree=1 [[graded derivation]] on the [[de Rham algebra]] $\Omega^\bullet_{dR}$, the [[Jacobi identity]] (eq:JacobiIdentity) implies that the [[covariant derivative]] (eq:CovariantDerivative) is a degree=1 [[graded derivation]] on the [[Lie bracket]] (eq:LieBracketOnLieAlgebraValuedDifferentialForms) of [[Lie algebra-valued differential forms]]:

\[
  \label{CovariantDerivativeIsDerivationOfLieBracket}
  \begin{array}{l}
    \omega \,\in\, \Omega^p_{dR} \otimes \mathfrak{g}
    \\
    \gamma \,\in\, \Omega^\bullet_{dR} \otimes \mathfrak{g}
  \end{array}
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  \mathrm{d}_A [ \omega, \gamma ]
  \;=\;
  \big[
    \mathrm{d}_A \omega
    ,\,
    \gamma
  \big]
  +
  (-1)^{p}
  \big[
    \omega 
    ,\,
    \mathrm{d}_A \gamma
  \big]
  \,.
\]

Another key point is that applying the [[covariant derivative]] (eq:CovariantDerivative) twice is equal to applying the Lie bracket $[F_A, -]$ with the [[curvature 2-form]]

\[
  F_A 
  \;\equiv\;
  \mathrm{d}A + \tfrac{1}{2}[A, A]
  \,,
\]

representing the [[magnetic charge|magnetic]] [[flux density]] carried by the [[gauge field]] $A$, because:

\[
  \label{CurvatureFromCovariantDerivativeSquared}
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
     \,,
  \end{array}
\]

where in the third step we used (eq:AAX).

Similarly, from applying the covariant derivative three times follows the [[Bianchi identity]], $\mathrm{d}_A F_A = 0$:

\[
  \label{BianchiIdentity}
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
   \;\;\;\;\;\;\;\;\;
   \Rightarrow
   \;\;\;\;\;\;\;\;\;
   \mathrm{d}_A F_A \,=\, 0
   \,.
\]


\linebreak

Our assumption that $\mathfrak{g}$ is a [[metric Lie algebra]] means that it is equipped with an binary [[invariant polynomial]], namely a [[bilinear map]]

$$
  \langle -,-\rangle
  \;\colon\;
  \mathfrak{g} \otimes \mathfrak{g}
  \to
  \mathbb{R}
  \,,
  \;\;\;\;\;\;
  k_{i j}
  \;\equiv\;
  \langle t_i, t_j\rangle
$$

which is symmetric

\[
  \label{SymmetryOfInvariantPolynomial}
  \langle t_i, t_j\rangle
  \;=\;
  \langle t_j, t_i\rangle
\]

and [[adjoint action|ad-]][[invariant]], in that

\[
  \label{AdInvarianceOfInvariantPolynomial}
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
  \,.
\]

For example:

\[
  \label{AdInvarianceOfPairingOnLieAlgValuedForms}
  X, Y 
   \,\in\,
  \Omega^0 \otimes \mathfrak{g}
  \;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;
  \langle
    [A, X] ,\, Y 
  \rangle
  +
  \langle
    X ,\, [A , Y ]
  \rangle
  \;=\;
  0
  \,.
\]

The induced trilinear pairing

\[
  \label{TrilinearPairing}
  \langle -,-,- \rangle
  \;\coloneqq\;
  \big\langle -,[-,-] \big\rangle
  \;\colon\;
  \mathfrak{g} \otimes \mathfrak{g} \otimes \mathfrak{g}
  \to
  \mathbb{R}
  \,,
  \;\;\;\;\;\;\;
  f_{i j k}
  \;\equiv\;
  \langle t_i, t_j, t_k\rangle
  \;=\;
  k_{i i'} f^{i'}{}_{j k}
\]

is also ad-invariant:

\[
  \label{AdInvarianceOfTrilinearPairing}
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
      -, \big[ {[t,-]}, -\big]
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
\]

(where we used first the Jacobi identity (eq:JacobiIdentity) and then the invariance (eq:AdInvarianceOfInvariantPolynomial) of the bilinear pairing) 

and is invariant under [[cyclic permutation]] of its arguments:

\[
  \label{CyclicInvarianceOfTrilinearPairing}
  \begin{array}{l}
    \langle 
      t_i, t_j , t_k 
    \rangle  
    \\
    \;\equiv\;
    \phantom{-\;}
    \big\langle 
      t_i, [t_j , t_k] 
    \big\rangle  
    \\
    \;=\;
    -
    \big\langle 
       [t_j ,  t_i ],  t_k
    \big\rangle  
    \\
    \;=\;
    \phantom{-\;}
    \big\langle 
       [t_i,  t_j ],  t_k
    \big\rangle  
    \\
    \;=\;
    \phantom{-\;}
    \big\langle 
      t_k, [t_i,  t_j ]
    \big\rangle  
    \\
    \;\equiv\;
    \phantom{-\;}
    \langle 
      t_k, t_i, t_j
    \rangle  
    \,,
  \end{array}
\]

(where we used ad-invariance (eq:AdInvarianceOfInvariantPolynomial), and symmetry (eq:SymmetryOfInvariantPolynomial) of the pairing and skew-symmetry of the Lie bracket).

\linebreak

\begin{example}
\label{TheLieAlgebrasu2}
In the case 
$\mathfrak{g} = $ [[su(2)|$\mathfrak{su}(2)$]] equipped with its [[Killing form]] and with linear basis taken to be the [[Pauli matrices]], we have:

* $f_{i j k} = \epsilon_{i j k}$ the [[Levi-Civita symbol]],

* $k_{i j} = \delta_{i j}$ the [[Kronecker delta]].

This is the case considered in [Cattaneo & Perez 2017](#CattaneoPerez17).
\end{example}

\linebreak


### The phase space of Yang-Mills theory
 {#ThePoissonBracketOfCanonicalVariables}

We consider now such [[Lie algebra-valued differential forms]] on a given [[smooth manifold|smooth 3-manifold]] $X$, thought of as a chosen [[Cauchy surface]] in a 3+1-dimensional [[Minkowski spacetime]].

On the space of $\mathfrak{g}$-valued 1-forms $A$ \eqref{GaugePotential} and 2-forms $E$, which on any [[coordinate chart]] $\mathbb{R}^3 \hookrightarrow X$ we may expand as 

$$
  A 
  \,=\,
  A_a^i \, \mathrm{d}x^a \otimes t_u
  \,,
  \;\;\;\;
  E \,=\,
  E_{a b}^i \, 
  \mathrm{d} x^a \wedge \mathrm{d} x^b \otimes t_u
  \,,
$$

we declare the [[distribution|distributional]] [[Poisson bracket]]:

\[
  \label{ThePoissonBracketOnCanonicalCoordinates}
  \begin{array}{l}
    \big\{ E^i_{a b}(x), E^j_{c d}(x') \big\}
    \;=\; 0
    \\
    \big\{ A^j_a(x), A^j_b(x') \big\}
    \;=\; 0
    \\
    \big\{ E^i_{a b}(x), A^j_c(x') \big\}
    \;\equiv\;
    k^{ i j } \epsilon_{a b c} \delta(x,x')
  \end{array}
\]

together with the [[first class constraint]] that the [[covariant derivative]] (eq:CovariantDerivative) of $E$ vanishes:

\[
  \label{GaussLawConstraint}
  \mathrm{d}_A E \;\approx\; 0
  \,.
\]

This is the [[phase space]] of [[Yang-Mills theory]] (see the references [there](Yang-Mills+theory#ReferencesPhaseSpaceAndCanonicalQuantization)), with:

* the [[canonical coordinate]] being the [[gauge potential]] $A$,

* its [[canonical momentum]] being the [[electric field]] [[flux density]] $E$,

* the [[constrained mechanics|constraint]] (eq:GaussLawConstraint) expressing the [[Gauss law]].

\linebreak

On this phase space, we are concerned with [[observables]] expressing electromagnetic flux through [[closed manifold|closed]] [[oriented manifold|oriented]] [[surface]] [[submanifolds]]

$$
  S \hookrightarrow X
  \,.
$$ 

Taken at face value, these observables are the surface [[integration of differential forms|integrals]] of the [[flux densities]] over $S$:

\[
  \label{NaiveFluxObservables}
  \begin{array}{c}
  \Phi_E^\alpha
  \;\overset{?}{\equiv}\;
  \int_S \langle \alpha,  E \rangle 
  \,,
  \\
  \Phi_B^\beta
  \;\overset{?}{\equiv}\;
  \int_S \langle \alpha, F_A \rangle
  \,,
  \end{array}
  \;\;\;\;\;\;\;\;
  \text{for}
  \;\;
  \alpha, \beta 
    \;\in\; 
  \Omega^0(S) \otimes \mathfrak{g}
  \,.
\]

However, these expression need to be corrected to become actual observables, since as give they do not have associated a smooth [[Hamiltonian vector field]]. This is the point explained in [Cattaneo & Perez 2017](#CattaneoPerez17): Instead, one needs to consider 3-dimensional "smearing" of the canonical observables in Prop. \ref{TheProperFluxObservables} below. 

Using the orientation of $S$ we consider any one-sided [[tubular neighbourhood]] $\hat S$ of $S$ inside $X$, extending to the "exterior" of $S$ (a non-compact [[submanifold]] [[manifold with boundary|with boundary]] $S$), 

> ([CP17](#CattaneoPerez17) speak of extending to the "interior" and seem to imagine that $S$ is actually the boundary of a compact sub-manifold -- which however is generally not what one wants to assume in discussion of fluxes: Typical choices of $S$ coincide with actual ([[asymptotic boundary|asymptotic]]) boundaries of the ambient spacetime, such as around the singular locus of a [[magnetic monopole]] that has been removed from spacetime. Our choice of extending to a neighbourhood of $S$ towards the exterior, instead of the interior, works just as well and allows $S$ to actually sit on a boundary of spacetime.)

and extending the coefficient functions to this neighbourhood with [[compact support]]  (i.e. such that they vanish some finite distance from $S$):

\begin{proposition}
\label{TheProperFluxObservables}
**([CP17 (6)](#CattaneoPerez17))**
Well-defined flux-observables equivalent to 
the na&iuml;ve observables (eq:NaiveFluxObservables)
are of this form:
\[
  \label{TheFluxObservables}
  \begin{array}{l}
  \Phi_E^\alpha
  \;\equiv\;
  \int_{\widehat S} 
  \big\langle
    \mathrm{d}_A \alpha
    ,\,
    E
  \big\rangle
  \,,
  \\
  \Phi_B^\beta
  \;\equiv\;
  \int_{\widehat S}
  \big\langle
    \mathrm{d}_A \alpha
    ,\,
    F_A
  \big\rangle
  \,,
  \end{array}
  \;\;\;\;
  \text{for}
  \;\;
  \alpha, \beta
    \;\in\; 
  \Omega^0\big(\widehat S \big)_{cpt}
    \otimes \mathfrak{g}
  \,.
\]
\end{proposition}
\begin{proof}
  To check that these are indeed equivalent to the na&iuml;ve observables, in that the difference is proportional to the left hand side of the [[Gauss law]] (eq:GaussLawConstraint), so that they coincide on the locus where the Gauss law holds:
$$
  \begin{array}{l}
  \int_{\widehat{S}} 
    \big\langle
      \mathrm{d}_A \alpha
      ,\,
      E
    \big\rangle
    \\
    \;\approx\;
    \int_{\widehat{S}} 
    \Big(
    \big\langle
      \mathrm{d}_A \alpha
      ,\,
      E
    \big\rangle
    +
    \underset{
      \approx 0
    }{
    \underbrace{
    \big\langle
      \alpha
      ,\,
      \mathrm{d}_A E
    \big\rangle
    }
    }
    \Big)
    \\
    \;=\;
    \int_{\widehat{S}} 
    \Big(
    \big\langle
      \mathrm{d} \alpha
      ,\,
      E
    \big\rangle
    \,+\,
    \big\langle
      \alpha
      ,\,
      \mathrm{d} E
    \big\rangle
    \Big)
    \\
    \;=\;
    \int_{\widehat{S}} 
    \mathrm{d}
    \big\langle
      \alpha
      ,\,
      E
    \big\rangle
    \\
    \;=\;
    \int_{S} 
    \big\langle
      \alpha
      ,\,
      E
    \big\rangle    
    \mathrlap{\,,}
  \end{array}
$$
where we used:

1. the Gauss law

1. (eq:AdInvarianceOfPairingOnLieAlgValuedForms)

1. derivation property of $\mathrm{d}$

1. [[Stokes theorem|Stokes]]

\end{proof}

\linebreak

In the computation [below](#ThePoissonBracketOfIntegratedFluxes), of the Poisson brackets of these flux observables, we repeatedly need the following identities, which also serve as good examples for how to compute with the Poisson brackets (eq:ThePoissonBracketOnCanonicalCoordinates):

\begin{example}
A key consequence of the corrected flux observables (eq:TheFluxObservables), is a non-trivial Poisson bracket between electric field observables and plain smearing functions:
\[
  \label{PoissonBracketBetweenElectricFieldAndSmearingFunction}
  \begin{array}{l}
    \Big\{
      \textstyle{\int}
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \mathrm{d}_A \beta
    \Big\}
    \\
    \;\equiv\;
    \Big\{
      \textstyle{\int}
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \mathrm{d}\beta
      + [A, \beta]
    \Big\}
    \\
    \;=\;
    \textstyle{\int}
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
    \,.
  \end{array}
\]
\end{example}
This is the relation needed for the computation of the bracket among electric fluxes in Prop. \ref{PoissonBracketBetweenElectricFluxes} below.

\begin{example}
\label{BracketOfElectricFluxWithMagneticFluxDensity}
The Poisson bracket of an electric flux observable with a magnetic flux density results in the *covariant derivative* of the electric smearing function:
\[
  \label{TheBracketOfElectricFluxWithMagneticFluxDensity}
  \begin{array}{l}
    \Big\{
      \textstyle{\int}
      \big(\mathrm{d}_A \alpha_i\big) \wedge E^i
      ,\,
      F_A(x')
    \Big\}
    \;=\;
    d_A \big(\mathrm{d}_A \alpha\big)(x')
  \end{array}
\]
\end{example}
This is the main relation needed in the computation of the bracket between electric and magnetic fluxes, in Prop. \ref{PoissonBracketBetweenElectricAndMagneticFluxes} below.
\begin{proof}
For the first summand in $F_A \,\equiv\, \mathrm{d}A + \tfrac{1}{2}[A, A]$ we have simply:
$$
  \begin{array}{l}
    \Big\{
      \textstyle{\int}
      \big(\mathrm{d}_A \alpha_i \big) \wedge E^i
      ,\,
      \mathrm{d} A(x')
    \Big\}
    \\
    \;=\;
    \mathrm{d}
      \Big\{
      \textstyle{\int}
      \big(\mathrm{d}_A \alpha_i \big) \wedge E^i
      ,\,
       A(x')
    \Big\}
    \\
    \;=\;
    \mathrm{d}
    \big(\mathrm{d}_A \alpha(x') \big)    
    \,.
  \end{array}
$$
For the second summand, considering any $\omega \in \Omega^1_{dR} \otimes \mathfrak{g}$, we have:

$$
  \begin{array}{l}
    \Big\{
      \textstyle{\int}
       \omega_i E^i
       ,\,
       \tfrac{1}{2} [A, A]
    \Big\}
    \\
    \;=\;
    \tfrac{1}{2} 
    \Big[
      \big\{
        \textstyle{\int}
        \omega_i E^i
        ,\,
        A
      \big\}
      ,\,
      A
    \Big]
    +
    \tfrac{1}{2} 
    \Big[
      A
      ,\,
      \big\{
        \textstyle{\int}
        \omega_i E^i
        ,\,
        A
      \big\}
    \Big]   
    \\
    \;=\;
    \big[
      A
      ,\,
      \omega
    \big]
    \,.
  \end{array}
$$

Together this yields the claim.

It may be instructive to state the last computation with more components made explicit:

> (combinatorial prefactors currently not shown properly, but they don't affect the sign, of course)

$$
  \begin{array}{l}
    \Big\{
      \textstyle{\int}
      \omega^i
      E_i
      ,\,
      \tfrac{1}{2}[A, A]
    \Big\}
    \\
    \;=\;
    \textstyle{\int}
    \omega_{i a}
    \epsilon^{a b c}
    \tfrac{1}{2} 
    \big\{
      E^i_{b c}
      ,\,
      A^j_{b'} 
      A^k_{c'} 
    \big\}
    [t_j, t_k]
    \mathrm{d} x^{b'} 
      \wedge 
    \mathrm{d} x^{c'}
    \\
    \;=\;
    \textstyle{\int}
    \tfrac{1}{2}
    \omega^i_a
    \epsilon^{a b c}
    \big(
      k^{i j} 
      \epsilon_{b c b'}
      A^k_{c'} 
      +
      A^j_{b'} 
      k^{i k} \epsilon_{b c c'}
    \big)
    [t_j, t_k]
    \mathrm{d} x^{b'} 
      \wedge 
    \mathrm{d} x^{c'}
    \\
    \;=\;
    \tfrac{1}{2}
    \big(
      A^k_{c'} 
      \omega^j_{b'}
      +
      A^j_{b'} 
      \omega^k_{c'}
    \big)
    [t_j, t_k]
    \mathrm{d} x^{b'} 
      \wedge 
    \mathrm{d} x^{c'}
    \\
    \;=\;
    A^j_{b'} 
    \omega^k_{c'}
    [t_j, t_k]
    \mathrm{d} x^{b'} 
      \wedge 
    \mathrm{d} x^{c'}
    \\
    \;=\;
    [A, \omega]
    \,.
  \end{array}
$$
\end{proof}


\linebreak


### The Poisson bracket of integrated fluxes
 {#ThePoissonBracketOfIntegratedFluxes}

We may now compute the [[Poisson bracket]] (eq:ThePoissonBracketOnCanonicalCoordinates) of the electromagnetic [[flux]] [[observables]] from Prop. \ref{TheProperFluxObservables}.

\begin{proposition}
\label{PoissonBracketBetweenElectricFluxes}
**([CP17 (7)](#CattaneoPerez17))**
\linebreak
 The Poisson bracket (eq:ThePoissonBracketOnCanonicalCoordinates) of electric flux observables (eq:TheFluxObservables) among each other is the Lie bracket on their smearing functions:
$$
  \Big\{
    \Phi_E^{\alpha}
    ,\,
    \Phi_E^{\beta}
  \Big\}
  \;=\;
  \Phi_E^{ [\alpha,\beta] }
  \,.
$$
\end{proposition}
\begin{proof}
We compute as follows:
\[
  \label{PoissonBracketElectricElectricFluxes}
  \begin{array}{l}
  \Big\{
    \textstyle{\int}
    \big( \mathrm{d}_A \alpha_i \big) E^i
    ,\,
    \textstyle{\int}
    \big( \mathrm{d}_A \beta_j \big) E^j
  \Big\}
  \\
  \;=\;
  \textstyle{\int}
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  -
  \textstyle{\int}
  \Big[
    \big(\mathrm{d}_A \beta\big)
    ,\,
    \alpha
  \Big]_i
  E^i
  \\
  \;=\;
  \textstyle{\int}
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  +
  \textstyle{\int}
  \Big[
    \alpha
    ,\,
    \big(\mathrm{d}_A \beta\big)
  \Big]_i
  E^i
  \\
  \;=\;
  \textstyle{\int}
  \big(
    \mathrm{d}_A
    [\alpha,\beta]_i
  \big)
  E^i
  \mathrlap{\,,}
  \end{array}
\]
where we used, in order of appearance:

1. (eq:PoissonBracketBetweenElectricFieldAndSmearingFunction)

1. (eq:GradedSkewSymemtryOfLieBracketOnLieAlgValuedForms)

1. (eq:CovariantDerivativeIsDerivationOfLieBracket).

\end{proof}

\begin{proposition}
\label{PoissonBracketBetweenElectricAndMagneticFluxes}
 The Poisson bracket (eq:ThePoissonBracketOnCanonicalCoordinates) of an electric flux observable with a magnetic flux observable (eq:TheFluxObservables) is the magnetic flux observable smeared by the Lie bracket of the given smearing functions:
$$
  \Big\{
    \Phi_E^\alpha
    ,\,
    \Phi_B^\beta
  \Big\}
  \;=\;
  \Phi_B^{[\alpha, \beta]}
  \,.
$$
\end{proposition}
\begin{proof}
We compute as follows:
\[
  \label{PoissonBracketElectricMagneticFluxes}
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
    \alpha
    ,\,
    \mathrm{d}_A  \beta
    ,\,
    F_A
  \big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \big\langle
    \mathrm{d}_A [\alpha, \beta]
    ,\,
    F_A
  \big\rangle
  \,.
  \end{array}
\]
Here we used, in order of appearance:

1. (eq:PoissonBracketBetweenElectricFieldAndSmearingFunction) and (eq:TheBracketOfElectricFluxWithMagneticFluxDensity);

1. (eq:CyclicInvarianceOfTrilinearPairing) and (eq:CurvatureFromCovariantDerivativeSquared)

1. (eq:CyclicInvarianceOfTrilinearPairing)

1. (eq:CovariantDerivativeIsDerivationOfLieBracket).

\end{proof}

\linebreak


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


