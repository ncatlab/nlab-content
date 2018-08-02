## Quantization
 {#Quantization}


In this chapter we discuss the following topics:

* _[Motivation from Lie theory](#MotivationFromLieTheory)_

* _[Geometric quantization](#GeometricQuantization)_

* _[Moyal star products](#StarProducts)_

* _[Moyal star product as deformation quantization](#MoyalStarProductAsDeformationQuantization)_

* _[Moyal star product via geometric quantization](#MoyalStarProductViaGeometricQuantization)_

* _[Example: Wick algebra of normal ordered product on Kähler vector space](#WickAlgebraOfNormalOrderedProductsOnKählerVectorspace)_

* _[Star-product on regular polynomial observables in field theory](#RegularPolynomialFieldTheoryStarProduct)_



$\,$


In the previous chapters we had found the [[Peierls-Poisson bracket]] (theorem \ref{PPeierlsBracket}) on the [[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) of a [[gauge fixing|gauge fixed]] (def. \ref{GaugeFixingLagrangianDensity}) [[free field theory|free]] [[Lagrangian field theory]] (def. \ref{FreeFieldTheory}). 

This [[Poisson bracket]] (def. \ref{SuperPoissonAlgebra} below) is a  [[Lie bracket]] and hence reflects [[infinitesimal symmetries]] acting on the [[covariant phase space]]. Just as with the [[infinitesimal symmetries of the Lagrangian]] and the [[BRST-complex|BRST]]-[[reduced phase space|reduced]] [[field bundle]] (example \ref{LocalOffShellBRSTComplex}), we may hard-wire these [[Hamiltonian]] symmetries into the very geometry of the phase space by forming their [[homotopy quotient]] given by the corresponding [[Lie algebroid]] (def. \ref{LInfinityAlgebroid}): here this is called the _[[Poisson Lie algebroid]]_. Its [[Lie integration]] to a  finite (instead of infinitesimal) structure is called the _[[symplectic groupoid]]_. This is the original [[covariant phase space]], but with its [[Hamiltonian flows]] hard-wired into its [[higher differential geometry]] ([[schreiber:master thesis Bongers|Bongers 14, section 4]]).

Where smooth functions on the plain covariant phase space form the [[commutative algebra|commutative]] [[algebra of observables]] under their pointwise product (def. \ref{Observable}), the smooth functions on this [[symplectic groupoid]]-refinement of the phase space are multiplied by the _[[groupoid convolution product]]_ and as such become a [[noncommutative algebra|non-commutative]] [[algebra of quantum observables]]. This passage from the commutative to the non-commutative algebra of observables is called _[[quantization]]_, here specifically _[[geometric quantization of symplectic groupoids]]_ ([Hawkins 04](geometric+quantization+of+symplectic+groupoids#EH), [[schreiber:master thesis Nuiten|Nuiten 13]]).

Instead of discussing this in generality, we here focus right away on the simple special case relevant for the [[quantization]] of [[gauge fixing|gauge fixed]] [[free field theories|free]] [[Lagrangian field theories]] in the [next chapter](#FreeQuantumFields). 

After an informal motivation of [[geometric quantization]] from [[Lie theory]] [below](#MotivationFromLieTheory) (for a self-contained introduction see [[schreiber:master thesis Bongers|Bongers 14]]), we first showcase [[geometric quantization]] by discussing how the archetypical example of [[quantum mechanics]] in the [[Schrödinger representation]] arises from the _[[polarization|polarized]]_ action of the [[Poisson bracket]] [[Lie algebra]]   (example \ref{GeometricRepresentationSchroedingerRepresentation} below). With the concept of [[polarization]] thus motivated, we use this to find the polarized [[groupoid convolution algebra]] of the [[symplectic groupoid]] of a free theory (prop. \ref{PolarizedSymplecticGroupoidConvolutionProductOfSymplecticVectorSpaceIsMoyalStarProduct} below). 

The result is the  "[[Moyal star product|Moyal]]-[[star product]]" (def. \ref{StarPoduct} below).  This is the [[exponentiation]] of the [[integral kernel]] of the [[Poisson bracket]] plus possibly a symmetric shift (prop. \ref{SymmetricContribution} below); it turns out to be (example \ref{MoyalStarProductIsFormalDeformationQuantization} below) a _[[formal deformation quantization]]_ of the original commutative pointwise product (def. \ref{FormalDeformationQuantization} below). 

Below we spell out the (elementary) proofs of these statements for the case of [[phase spaces]] which are [[finite dimensional vector spaces]]. But these proofs manifestly depend only on elementary algebraic properties of [[polynomials]] and hence go through in more general contexts as long as these basic algebraic properties are retained. 

In the context of [[free field theory|free]] [[Lagrangian field theory]] the analogue of the [[formal power series algebras]] on a linear [[phase space]] is, a priori, the algebra of [[polynomial observables]] (def. \ref{PolynomialObservables}). These are effectively [[polynomials]] in the [[field observables]] $\mathbf{\Phi}^a(x)$ (def. \ref{PointEvaluationObservables}) whose [[coefficients]], however, are [[distributions]] [[distribution of several variables|of several variables]]. By [[microlocal analysis]], such polynomial distributions do satisfy the usual algebraic properties of ordinary polynomials _if_ potential [[UV-divergences]] (remark \ref{UltravioletDivergencesFromPaleyWiener}) encoded in their [[wave front set]] (def. \ref{WaveFrontSet}) vanish, according to _[[Hörmander's criterion]]_ (prop. \ref{HoermanderCriterionForProductOfDistributions}).

This criterion is always met on the subspace of _[[regular polynomial observables]]_ and hence every [[propagator]] induces a [[star product]] on these (prop. \ref{PropagatorStarProduct} below). In particular thus the [[star product]] of the [[causal propagator]] of a [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]] is a [[formal deformation quantization]] of its algebra of [[regular polynomial observables]] (cor. \ref{FreeGaugeFixedLagrangianFieldTheoryQuantizationOfRegularObservables} below). In order to extend this to [[local observables]] one may appeal to a certain quantization freedom (prop. \ref{SymmetricContribution} below) and shift the [[causal propagator]] by a symmetric contribution, such that it becomes the [[Wightman propagator]]; this is the topic of the following chapters (remark \ref{TowardsQuantizationExtendingBeyondRegularPolynomialObservables} at the end below).

In conclusion, for [[free field theory|free]] [[gauge fixing|gauge fixed]] [[Lagrangian field theory]] the product in the [[algebra of quantum observables]] is given by [[exponential|exponentiating]] [[propagators]]. It is the [[combinatorics]] of these exponentiated propagator expressions that yields the hallmark structures of [[perturbative quantum field theory]], namely the combinatorics of [[Wick's lemma]] for the [[Wick algebra]] of free fields, and the combinatorics of [[Feynman diagrams]] for the [[time-ordered products]]. This is the topic of the following chapters _[Free quantum fields](#FreeQuantumFields)_ and _[Scattering](#Scattering)_.  Here we conclude just with discussing the finite-dimensional toy version of the [[normal-ordered product]] in the [[Wick algebra]] (example \ref{WickAlgebraOfASingleMode} below).



$\,$

**motivation from Lie theory**
 {#MotivationFromLieTheory}


Quantization of course was and is motivated by experiment, hence by observation of the [[observable universe]]: it just so happens that [[quantum mechanics]] and [[quantum field theory]] correctly account for experimental observations where [[classical mechanics]] and [[classical field theory]] gives no answer or incorrect answers. A historically important example is the phenomenon called the "[[ultraviolet catastrophe]]", a [[paradox]] predicted by classical [[statistical mechanics]] which is _not_ observed in nature, and which is corrected by [[quantum mechanics]].

But one may also ask, independently of experimental input, if there are good formal mathematical reasons and motivations to pass from [[classical mechanics]] to [[quantum mechanics]]. Could one have been led to [[quantum mechanics]] by just pondering the mathematical formalism of [[classical mechanics]]? 

The following spells out an argument to this effect. It will work for readers with a background in modern [[mathematics]], notably in [[Lie theory]], and with an understanding of the formalization of classical/prequantum mechanics in terms of [[symplectic geometry]]. 

So to briefly recall, a system of [[classical mechanics]]/[[prequantum field theory|prequantum mechanics]] is a [[phase space]], formalized as a [[symplectic manifold]] $(X, \omega)$. A symplectic manifold is in particular a [[Poisson manifold]], which means that the [[algebra of functions]] on [[phase space]] $X$, hence the algebra of _classical [[observables]]_, is canonically equipped with a compatible [[Lie bracket]]: the _[[Poisson bracket]]_. This Lie bracket is what controls [[dynamics]] in [[classical mechanics]]. For instance if $H \in C^\infty(X)$ is the function on [[phase space]] which is interpreted as assigning to each configuration of the system its [[energy]] -- the [[Hamiltonian]] function -- then the [[Poisson bracket]] with $H$ yields the [[infinitesimal object|infinitesimal]] time evolution of the system: the [[differential equation]] famous as [[Hamilton's equations]].

Something to take notice of here is the _[[infinitesimal space|infinitesimal]]_ nature of the [[Poisson bracket]]. Generally, whenever one has a [[Lie algebra]] $\mathfrak{g}$, then it is to be regarded as the [[infinitesimal object|infinitesimal]] approximation to a globally defined object, the corresponding [[Lie group]] (or generally [[smooth group]]) $G$. One also says that $G$ is a _[[Lie integration]]_ of $\mathfrak{g}$ and that $\mathfrak{g}$ is the [[Lie differentiation]] of $G$.

Therefore a natural question to ask is: _Since the observables in [[classical mechanics]] form a [[Lie algebra]] under [[Poisson bracket]], what then is the corresponding [[Lie group]]?_

The answer to this is of course "well known" in the literature, in the sense that there are relevant monographs which state the answer. But, maybe surprisingly, the answer to this question is not (at time of this writing) a widely advertized fact that has found its way into the basic educational textbooks. The answer is that this [[Lie group]] which integrates the [[Poisson bracket]] is the "[[quantomorphism group]]", an object that seamlessly leads to the [[quantum mechanics]] of the system.

Before we spell this out in more detail, we need a brief technical aside: of course [[Lie integration]] is not quite unique. There may be different global [[Lie group]] objects with the same [[Lie algebra]]. 

The simplest example of this is already one of central importance for the issue of quantization, namely, the Lie integration of the abelian [[line Lie algebra]] $\mathbb{R}$. This has essentially two different [[Lie groups]] associated with it: the [[simply connected topological space|simply connected]] [[translation group]], which is just $\mathbb{R}$ itself again, equipped with its canonical additive [[abelian group]] structure, and the [[discrete space|discrete]] [[quotient]] of this by the group of [[integers]], which is the [[circle group]]

$$
  U(1) = \mathbb{R}/\mathbb{Z}
  \,.
$$

Notice that it is the discrete and hence "quantized" nature of the [[integers]] that makes the [[real line]] become a [[circle]] here. This is not entirely a coincidence of terminology, but can be traced back to the heart of what is "quantized" about [[quantum mechanics]].

Namely, one finds that the [[Poisson bracket]] [[Lie algebra]] $\mathfrak{poiss}(X,\omega)$ of the classical [[observables]] on [[phase space]] is (for $X$ a [[connected topological space|connected]] [[manifold]]) a [[Lie algebra extension]] of the Lie algebra $\mathfrak{ham}(X)$ of [[Hamiltonian vector fields]] on $X$ by the [[line Lie algebra]]:

$$
  \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X)
  \,.
$$

This means that under [[Lie integration]] the [[Poisson bracket]] turns into an [[central extension]] of the group of [[Hamiltonian symplectomorphisms]] of $(X,\omega)$. And either it is the fairly trivial non-compact extension by $\mathbb{R}$, or it is the interesting [[central extension]] by the [[circle group]] $U(1)$. For this non-trivial [[Lie integration]] to exist, $(X,\omega)$ needs to satisfy a quantization condition which says that it admits a [[prequantum line bundle]]. If so, then this $U(1)$-[[central extension]] of the group $Ham(X,\omega)$ of [[Hamiltonian symplectomorphisms]] exists and is called... the _[[quantomorphism group]]_ $QuantMorph(X,\omega)$:

$$
  U(1) \longrightarrow QuantMorph(X,\omega) \longrightarrow Ham(X,\omega)
  \,.
$$

While important, for some reason this group is not very well known, which is striking because it contains a small [[subgroup]] which is famous in [[quantum mechanics]]: the _[[Heisenberg group]]_.

More precisely, whenever $(X,\omega)$ itself has a [[Hamiltonian action|compatible]] [[group]] structure, notably if $(X,\omega)$ is just a [[symplectic vector space]] (regarded as a group under addition of vectors), then we may ask for the [[subgroup]] of the [[quantomorphism group]] which covers the (left) [[action]] of [[phase space]] $(X,\omega)$ on itself. This is the corresponding [[Heisenberg group]] $Heis(X,\omega)$, which in turn is a $U(1)$-[[central extension]] of the group $X$ itself:

$$
  U(1) \longrightarrow Heis(X,\omega) \longrightarrow X
  \,.
$$

At this point it is worth pausing for a second to note how the hallmark of [[quantum mechanics]] has appeared as if out of nowhere simply by applying [[Lie integration]] to the [[Lie algebra|Lie algebraic]] structures in [[classical mechanics]]:

if we think of [[Lie integration|Lie integrating]] $\mathbb{R}$ to the interesting [[circle group]] $U(1)$ instead of to the uninteresting [[translation group]] $\mathbb{R}$, then the name of its canonical [[basis]] element $1 \in \mathbb{R}$ is canonically "$i$", the imaginary unit. Therefore one often writes the above [[central extension]] instead as follows:

$$
  i \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X,\omega)
$$

in order to amplify this. But now consider the simple special case where $(X,\omega) = (\mathbb{R}^2, d p \wedge d q)$ is the 2-dimensional [[symplectic vector space]] which is for instance the [[phase space]] of the [[particle]] propagating on the line. Then a canonical set of generators for the corresponding [[Poisson bracket]] [[Lie algebra]] consists of the linear functions $p$ and $q$ of classical mechanics textbook fame, together with the _constant_ function. Under the above Lie theoretic identification, this constant function is the canonical basis element of $i \mathbb{R}$, hence purely Lie theoretically it is to be called "$i$".

With this notation then the [[Poisson bracket]], written in the form that makes its [[Lie integration]] manifest, indeed reads

$$
  [q,p] = i
  \,.
$$

Since the choice of [[basis]] element of $i \mathbb{R}$ is arbitrary, we may rescale here the $i$ by any non-vanishing [[real number]] without changing this statement. If we write "$\hbar$" for this element, then the [[Poisson bracket]] instead reads

$$
  [q,p] = i \hbar
  \,.
$$


This is of course the hallmark equation for [[quantum physics]], if we interpret $\hbar$ here indeed as [[Planck's constant]]. We see it arises here merely by considering the non-trivial (the interesting, the non-simply connected) [[Lie integration]] of the [[Poisson bracket]]. 

This is only the beginning of the story of quantization, naturally understood and indeed "derived" from applying [[Lie theory]] to [[classical mechanics]]. From here the story continues. It is called the story of _[[geometric quantization]]_. We close this motivation section here by some brief outlook.

The [[quantomorphism group]] which is the non-trivial [[Lie integration]] of the [[Poisson bracket]] is naturally constructed as follows: given the [[symplectic form]] $\omega$, it is natural to ask if it is the [[curvature]] 2-form of a $U(1)$-[[principal connection]] $\nabla$ on [[complex line bundle]] $L$ over $X$ (this is directly analogous to [[Dirac charge quantization]] when instead of a [[symplectic form]] on [[phase space]] we consider the  the [[field strength]] 2-form of [[electromagnetism]] on [[spacetime]]). If so, such a connection $(L, \nabla)$ is called a _[[prequantum line bundle]]_ of the [[phase space]] $(X,\omega)$. The [[quantomorphism group]] is simply the [[automorphism group]] of the [[prequantum line bundle]], covering [[diffeomorphisms]] of the phase space (the [[Hamiltonian symplectomorphisms]] mentioned above).

As such, the [[quantomorphism group]] naturally [[action|acts]] on the [[space of sections]] of $L$. Such a [[section]] is like a [[wavefunction]], except that it depends on all of [[phase space]], instead of just on the "[[canonical coordinates]]". For purely abstract mathematical reasons (which we won't discuss here, but see at _[[motivic quantization]]_ for more) it is indeed natural to choose a "[[polarization]]" of [[phase space]] into [[canonical coordinates]] and [[canonical momenta]] and consider only those [[sections]] of the [[prequantum line bundle]] which depend only on the former. These are the actual _[[wavefunctions]]_ of [[quantum mechanics]], hence the _[[quantum states]]_. And the [[subgroup]] of the [[quantomorphism group]] which preserves these polarized sections is the group of exponentiated [[quantum observables]]. For instance in the simple case mentioned before where $(X,\omega)$ is the 2-dimensional [[symplectic vector space]], this is the [[Heisenberg group]] with its famous action by multiplication and differentiation operators on the space of complex-valued functions on the real line.


$\,$


**[[geometric quantization]]**
  {#GeometricQuantization}

We had seen that every [[Lagrangian field theory]] induces a [[presymplectic current]] $\Omega_{BFV}$ (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) on the [[jet bundle]] of its [[field bundle]] in terms of which there is a concept of [[Hamiltonian differential forms]] and [[Hamiltonian vector fields]] on the jet bundle (def. \ref{HamiltonianForms}). The concept of [[quantization]] is induced by this _local [[phase space]]_-structure. 

In order to disentangle the core concept of [[quantization]] from the technicalities involved in fully fledged [[field theory]], we now first discuss the [[finite number|finite]] [[dimension|dimensional]] situation.


+-- {: .num_example #GeometricRepresentationSchroedingerRepresentation}
###### Example
**([[Schrödinger representation]] via [[geometric quantization]])**

Consider the [[Cartesian space]] $\mathbb{R}^2$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) with canonical [[coordinate functions]] denoted $\{q,p\}$ and to be called the _[[canonical coordinate]]_ $q$ and its [[canonical momentum]] $p$ (as in example \ref{CanonicalMomentum})
and equipped with the [[left invariant differential form|constant]] [[differential 2-form]] given in in (eq:CanonicalMomentumPresymplecticCurrent) by

$$
  \label{R2SymplecticForm}
  \omega = d p \wedge d q
  \,.
$$

This is [[closed differential form|closed]] in that $d \omega = 0$, and invertible in that the contraction of [[tangent vector fields]] into it (def. \ref{ContractionOfFormsWithVectorFields}) is an [[isomorphism]] to [[differential 1-forms]], and as such it is a _[[symplectic form]]_.

A choice of [[presymplectic potential]] for this [[symplectic form]] is

$$
  \label{CanonicalSymplecticPotentialOnR2}
  \theta \;\coloneqq\; - q \, d p
$$

in that $d \theta = \omega$. (Other choices are possible, notably $\theta = p \, d q$).


For 

$$
  A 
    \;\colon\;
  \mathbb{R}^2 
    \longrightarrow 
  \mathbb{C}
$$

a [[smooth function]] (an [[observable]]), we say that a _[[Hamiltonian vector field]]_ for it (as in def. \ref{HamiltonianForms}) is a [[tangent vector field]] $v_A$ (example \ref{TangentVectorFields}) whose contraction (def. \ref{ContractionOfFormsWithVectorFields}) into the [[symplectic form]] (eq:R2SymplecticForm) is the [[de Rham differential]] of $A$:

$$
  \label{HamiltonianVectorFieldOnR2}
  \iota_{v_A} \omega = d A
  \,.
$$

Consider the [[foliation]] of this phase space by constant-$q$-slices

$$
  \label{ConstantqSlicesOnR2}
  \Lambda_q \subset \mathbb{R}^2
  \,.
$$

These are also called the _[[leaves]]_ of a _[[real polarization]]_ of the [[phase space]].

(Other choices of [[polarization]] are possible, notably the constant $p$-slices.)

We says that a smooth function 

$$
 \psi \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{C}
$$

is _[[polarization|polarized]]_ if its [[covariant derivative]] with [[connection on a bundle]] $i \theta$ along the [[leaves]] vanishes; which for the choice of polarization in (eq:ConstantqSlicesOnR2) means that

$$
  \nabla_{\partial_p} \psi = 0
  \phantom{AAA}
  \Leftrightarrow
   \phantom{AAA}
  \iota_{\partial_p} \left(  d \psi + i \theta \psi \right)
  = 
  0
  \,,
$$

which in turn, for the choice of [[presymplectic potential]] in (eq:CanonicalSymplecticPotentialOnR2), means that

$$
  \frac{\partial}{\partial p} \psi - i q \psi = 0
  \,.
$$

The solutions to this [[differential equation]] are of the form

$$
  \label{PolarizedFunctionsForBasicExampleOnR2}
  \Psi(q,p) = \psi(q) \, \exp(+ i p q)
$$

for $\psi \colon \mathbb{R} \to \mathbb{C}$ any [[smooth function]], now called a _[[wave function]]_.

This establishes a [[linear isomorphism]] between  polarized smooth functions and [[wave functions]].


By (eq:HamiltonianVectorFieldOnR2) we have the [[Hamiltonian vector fields]]

$$
  v_q = \partial_p
  \phantom{AAAA}
  v_p = -\partial_q  
  \,.
$$

The corresponding _[[Poisson bracket]]_ is

$$
  \label{R2PoissonBracket}
  \begin{aligned}
    \{q,p\}
    & \coloneqq 
    \iota_{v_p} \iota_{v_q}  \omega
    \\
    & = 
    -\iota_{\partial_q} \iota_{\partial_p} d p \wedge d q
    =
    \\
    & = 
    - 1
  \end{aligned}  
$$

The action of the corresponding [[quantum operator (in geometric quantization)|quantum operators]] $\hat q$ and $\hat p$ on the polarized functions (eq:PolarizedFunctionsForBasicExampleOnR2) is as follows

$$
  \begin{aligned}
    \hat q \Psi(q,p)
      & =
      - i \nabla_{\partial_p}\Psi(q,p) + q \Psi(q,p)
      \\
      & = -i
      \underset{ = 0 }{
        \underbrace{
          \left(
            \underset{
              = i q \Psi(q,p)
            }{
              \underbrace{
                \frac{\partial}{\partial p}
                \left( 
                  \psi(q) e^{i q p}
                \right)
              }
            }
            - i q \Psi(q,p)
        \right)
       }
      }
      +
      q \Psi(q,p)
      \\
      & = \left( q \psi(q) \right) e^{i q p}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \hat p \Psi(q,p)
    & =  
    i \nabla_{\partial_q} \Psi(q,p) + p \Psi(q,p)
    \\
    & = i \frac{\partial}{\partial q} (\psi(q)e^{i q p}) + p \Psi(q,p)
    \\
    & =
    \left(
      i \frac{\partial}{\partial q}\psi(q)
    \right) e^{i q p}
    +
    \underset{ = 0}{
      \underbrace{
        \underset{ 
           = - p \Psi(q,p) 
        }{
          \underbrace{
            \psi(q) 
            \left( 
              i \frac{\partial}{\partial q} e^{i q p}
            \right)
          }
        }
        +
        p \Psi(q,p)
     }  
   }
   \\
   & = 
   \left( 
     i \frac{\partial}{\partial q}\psi(q)
   \right) e^{i p q}
  \end{aligned}   
  \,.
$$

Hence under the identification (eq:PolarizedFunctionsForBasicExampleOnR2) we have

$$
  \hat q \psi = q \psi
  \phantom{AAAA}
  \hat p \psi = i \frac{\partial}{\partial q} \psi
  \,.
$$

This is called the [[Schrödinger representation]] of the [[canonical commutation relation]] (eq:R2PoissonBracket).

=--


$\,$


**[[Moyal star products]]**
  {#StarProducts}

Let $V$ be a [[finite dimensional vector space]] and let $\pi \in V \otimes V$ be an element of the [[tensor product]] (not necessarily skew symmetric at the moment).

We may canonically regard $V$ as a [[smooth manifold]], in which case $\pi$ is canonically regarded as a constant rank-2 [[tensor]]. As such it has a canonical [[action]] by forming [[derivatives]] on the tensor product of the space of [[smooth functions]]:

$$
  \pi
  \;\colon\;
  C^\infty(V) \otimes C^\infty(V)
  \longrightarrow
  C^\infty(V) \otimes C^\infty(V)
  \,.
$$

If $\{\partial_i\}$ is a [[linear basis]] for $V$, identified, as before, with a basis for $\Gamma(T V)$, then in this basis this operation reads

$$
  \pi(f \otimes g)
  \;=\;
  \pi^{i j}
  (\partial_i f) \otimes (\partial_j g)
  \,,
$$

where $\partial_i f \coloneqq \frac{\partial f}{\partial x^i}$ denotes the [[partial derivative]] of the [[smooth function]] $f$ along the $i$th [[coordinate]], and where we use the [[Einstein summation convention]].

For emphasis we write

$$
  \array{
    C^\infty(V) \otimes C^\infty(V)
      &\overset{prod}{\longrightarrow}&
    C^\infty(V)
    \\
    f \otimes g &\mapsto& f \cdot g
  }
$$

for the pointwise product of smooth functions.


+-- {: .num_defn #StarPoduct}
###### Definition
**([[star product]] induced by constant rank-2 [[tensor]])**

Given $(V,\pi)$ as above, then the _[[star product]]_ induced by $\pi$ on the [[formal power series algebra]] $C^\infty(V) [ [\hbar] ]$ in a formal variable $\hbar$ ("[[Planck's constant]]") with [[coefficients]] in the [[smooth functions]] on $V$ is the linear map

$$
  (-) \star_\pi (-)
  \;\colon\;
  C^\infty(V)[ [ \hbar ] ] \otimes C^\infty(V)[ [ \hbar ] ]
    \longrightarrow
  C^\infty(V)[ [\hbar] ]
$$

given by

$$
  (-) \star_\pi (-)
  \;\coloneqq\;
  prod
    \circ \exp\left(
       \hbar \pi^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)
$$

Hence

$$
  f \star_\pi g
  \;\coloneqq\;
  1
  +
  \hbar \pi^{i j}
  \frac{\partial f}{\partial x^i} \cdot \frac{\partial g}{\partial x^j}
  +
  \hbar^2
  \tfrac{ 1 }{2}
  \pi^{i j}
  \pi^{k l}
  \frac{\partial^2 f}{\partial x^{i} \partial x^{k}}
    \cdot
  \frac{\partial^2 g}{\partial x^{j} \partial x^{l}}
  +
  \cdots
  \,.
$$

=--


+-- {: .num_example }
###### Example
**([[star product]] degenerating to pointwise product)**

If $\pi = 0$ in def. \ref{StarPoduct}, then the star product $\star_0 = \cdot$ is the plain pointwise product of functions.

=--


+-- {: .num_exaple #MoyalStarProduct}
###### Example
**([[Moyal star product]])**

If the tensor $\pi$ in def. \ref{StarPoduct} is skew-symmetric, it may be regarded as a constant [[Poisson tensor]] on the smooth manifold $V$. In this case $\star_{\tfrac{1}{2}\pi}$ is called a _[[Moyal star product]]_ and the star-product algebra $C^\infty(V)[ [\hbar] ], \star_\pi)$ is called the _[[Moyal deformation quantization]]_ of the [[Poisson manifold]] $(V,\pi)$.

=--



+-- {: .num_prop #AssociativeAndUnitalStarProduct}
###### Proposition
**([[star product]] is [[associativity|associative]] and [[unitality|unital]])**

Given $(V,\pi)$ as above, then the star product
$(-) \star_\pi (-)$ from def. \ref{StarPoduct}
is [[associativity|associative]] and [[unitality|unital]]
with unit the [[constant function]] $1 \in C^\infty(V) \hookrightarrow C^\infty(V)[ [ \hbar ] ]$.

Hence the [[vector space]] $C^\infty(V)$ equipped with the star product $\pi$ is a [[unital algebra|unital]] [[associative algebra]].

=--


+-- {: .proof}
###### Proof

Observe that the [[product rule]] of [[differentiation]] says that

$$
  \partial_i \circ prod
    =
   prod \circ ( \partial_i \otimes id \;+\; id \otimes \partial_i  )
  \,.
$$

Using this we compute as follows:

$$
  \begin{aligned}
  & (f \star_\pi  g) \star_\pi h
  \\
  & =
  prod \circ
  \exp( \pi^{i j} \partial_i \otimes \partial_j )  \circ
  \left(
    \left( prod \circ \exp( \pi^{k l} \partial_k \otimes \partial_l ) \right) \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  \exp( \pi^{i j} \partial_i \otimes \partial_j ) \circ
  (prod \otimes id)
  \circ
  \left(
    \exp( \pi^{k l} \partial_k \otimes \partial_l )  \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \pi^{i j}  ( \partial_i \otimes id \otimes \partial_j +id \otimes \partial_i \otimes \partial_j   )
  \circ
  \exp( \pi^{k l} \partial_k \otimes \partial_l )  \otimes id
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \pi^{i j}   \partial_i \otimes id \otimes \partial_j   )
  \circ
  \exp( \pi^{i j}  id \otimes \partial_i \otimes \partial_j )
  \circ
  \exp( \pi^{k l} \partial_k \otimes \partial_l \otimes id )
  (f \otimes g \otimes g)
  \\
  & =
  prod_3
  \circ
  \exp( \pi^{i j} ( \partial_i \otimes \partial_j \otimes id  +  \partial_i \otimes id \otimes \partial_j + id \otimes \partial_i \otimes \partial_j)   )
  \end{aligned}
$$

In the last line we used that the ordinary pointwise product of functions is associative, and wrote $prod_3 \colon C^\infty(V) \otimes C^\infty(V) \otimes C^\infty(V) \to C^\infty(V)$ for the unique pointwise product of three functions.

The last expression above is manifestly independent of the choice of order of the arguments in the triple star product, and hence it is clear that an analogous computation yields

$$
  \cdots = f \star_\pi (g \star_\pi h)
  \,.
$$

=--

+-- {: .num_prop #SymmetricContribution}
###### Proposition
**(shift by symmetric contribution is [[isomorphism]] of [[star products]])**

Let $V$ be a vector space, $\pi \in V \otimes V$ a rank-2 [[tensor]] and $\alpha \in Sym(V \otimes V)$ a _symmetric_ rank-2 tensor.

Then the [[linear map]]

$$
  \array{
    C^\infty(V)
     &\overset{\exp\left(\tfrac{1}{2}\alpha \right)}{\longrightarrow}&
    C^\infty(V)
    \\
    f 
      &\mapsto& 
    \exp\left( \tfrac{1}{2}\hbar \alpha^{i j} \partial_i \partial_j \right) f
  }
$$

constitutes an [[isomorphism]] of star product algebras (prop. \ref{AssociativeAndUnitalStarProduct}) of the form

$$
  \exp\left(\hbar\tfrac{1}{2}\hbar\alpha \right)
   \;\colon\;
  (C^\infty(V)[ [\hbar] ], \star_{\pi})
    \overset{\simeq}{\longrightarrow}
  (C^\infty(V))[ [\hbar] ], \star_{\pi + \alpha})
  \,,
$$

hence identifying the star product induced from $\pi$ with that induced from $\pi + \alpha$.

In particular every star product algebra $(C^\infty(V)[ [\hbar] ],\star_\pi)$ is isomorphic to a Moyal star product algebra $\star_{\tfrac{1}{2}\pi}$ (example \ref{MoyalStarProduct}) with $\tfrac{1}{2}\pi_{skew}^{i j} = \tfrac{1}{2}(\pi^{i j} - \pi^{j i})$ the skew-symmetric part of $\pi$, this isomorphism being exhibited by the symmetric part $2\alpha^{i j} = \tfrac{1}{2}(\pi^{i j} + \pi^{j i})$.

=--


+-- {: .proof}
###### Proof

We need to show that

$$
  \array{
    C^\infty(V)[ [\hbar] ] \otimes  C^\infty(V)[ [\hbar] ]
    &
     \overset{ 
       \exp\left( \tfrac{1}{2}\hbar \alpha \right)    
       \otimes
       \exp\left( \tfrac{1}{2}\hbar \alpha \right)    
     }{\longrightarrow}&
    C^\infty(V)[ [\hbar] ] \otimes  C^\infty(V)[ [\hbar] ]
     \\
     {}^{\mathllap{\star_{\pi}}}\downarrow 
       && 
    \downarrow^{\mathrlap{\star_{\pi + \alpha}}}
    \\
    C^\infty(V)[ [\hbar] ]
      &\underset{\exp\left( \tfrac{1}{2} \alpha \right) }{\longrightarrow}&
    C^\infty(V)[ [\hbar] ]
  }
$$

hence that 

$$
  prod \circ
  \exp( \hbar(\pi + \alpha) )
  \circ
  \left(
    \exp\left( \tfrac{1}{2}\alpha\right)
    \otimes
    \exp\left( \tfrac{1}{2}\alpha \right)
  \right)
  \;=\;
  \exp\left( \tfrac{1}{2}\alpha \right)
  \circ
   prod \circ \exp( \pi )
  \,.
$$


To this end, observe that the [[product rule]] of [[differentiation]] applied twice in a row implies that

$$
  \partial_i \partial_j \circ prod
  \;=\;
  prod \circ
  \left(
     (\partial_i \partial_j)  \otimes id
     +
     id \otimes (\partial_i \partial_j)
     +
     \partial_i \otimes \partial_j
     +
     \partial_j \otimes \partial_i
  \right)
  \,.
$$

Using this we compute

$$
  \begin{aligned}
    & 
    \exp\left( \hbar\tfrac{1}{2}\alpha^{i j} \partial_i \partial_j \right)
    \circ
    prod
    \circ
    \exp( \hbar \pi^{i j} \partial_{i} \otimes \partial_j )
    \\
    & =
    prod
      \circ
      \exp\left( 
        \hbar \tfrac{1}{2}\alpha^{i j}
        \left(
           (\partial_i \partial_j) \otimes id
           +
           id \otimes (\partial_i \partial_j)
           +
           \partial_i \otimes \partial_j
           +
           \partial_j \otimes \partial_i
        \right)
      \right)
      \circ
    \exp( \hbar \pi^{i j} \partial_{k} \otimes \partial_l )
    \\
    &
    =
    prod
    \circ
    \exp\left(
       \hbar (\pi^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
    \right)
    \circ
    \exp\left(
      \hbar \tfrac{1}{2} \alpha^{i j} (\partial_i \partial_j) \otimes id
      \hbar \tfrac{1}{2} \alpha^{i j} id \otimes (\partial_i \partial_j)
    \right)
    \\
    & =
    prod
    \circ
    \exp\left(
       \hbar (\pi^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
    \right)
    \circ
    \left(
      \exp\left( \tfrac{1}{2} \hbar \alpha \right)
        \otimes
      \exp\left( \tfrac{1}{2} \hbar \alpha \right)
    \right)
  \end{aligned}
$$

=--


$\,$

**[[Moyal star product]] as [[deformation quantization]]**
 {#MoyalStarProductAsDeformationQuantization}

+-- {: .num_defn #SuperPoissonAlgebra}
###### Definition
**(super-[[Poisson algebra]])**

A super-[[Poisson algebra]] is

1. a [[supercommutative algebra]] $\mathcal{A}$ (here: over the [[real numbers]])

1. a [[bilinear function]]

   $$
     \{-,-\}
     \;\colon\;
     \mathcal{A} \otimes \mathcal{A} 
     \longrightarrow
     A
   $$

   to be called the _[[Poisson bracket]]_

such that

1. $\{-,-\}$ is a [[super Lie algebra|super Lie bracket]] on $\mathcal{A}$, hence it 

   1. is graded skew-symmetric;

   1. satisfies the super-[[Jacobi identity]];

1. for each $A \in \mathcal{A}$ of homogeneous degree, the operation 

   $$
     \left\{ A, -\right\} 
     \;\colon\;
     \mathcal{A}
       \longrightarrow
     \mathcal{A}
   $$

   is a graded [[derivation]] on $\mathcal{A}$ of the same degree as $A$.

=--

+-- {: .num_defn #FormalDeformationQuantization}
###### Definition
**([[formal deformation quantization]])**

Let $(\mathcal{A},\{-,-\})$ be a super-[[Poisson algebra]] (def. \ref{SuperPoissonAlgebra}). Then a _[[formal deformation quantization]]_ of $(A,\{-,-\})$ is 

* the [[structure]] of an [[associative algebra]] on the [[formal power series algebra]] over $\mathcal{A}$ in a [[variable]] to be called $\hbar$, hence an [[associativity|associative]] and [[unitality|unital]] product

  $$
    \mathcal{A}[ [\hbar] ]
    \otimes
    \mathcal{A}[ [\hbar] ]
    \longrightarrow
    \mathcal{A}[ [\hbar] ]
  $$

such that for all $f,g \in \mathcal{A}$ of homogeneous degree we have

1. $f \star g \, mod \hbar = f g$

1. $f \star g - (-1)^{deg(f) deg(g)} g \star f \, \mod \hbar^2 = \hbar \{f,g\}$

meaning that 

1. to zeroth order in $\hbar$ the [[star product]] coincides with the given commutative product on $\mathcal{A}$, 

1. to first order in $\hbar$ the [[graded commutator]] of the [[star product]] coincides with the given [[Poisson bracket]] on $\mathcal{A}$.

=--

+-- {: .num_example #MoyalStarProductIsFormalDeformationQuantization}
###### Example
**([[Moyal star product]] is [[formal deformation quantization]])**

Let $(V,\pi)$ be a _[[Poisson manifold|Poisson vector space]]_, hence a [[vector space]] $V$, equipped with a skew-symmetric [[tensor]] $\pi \in V \wedge V$.

Then with $V$ regarded as a [[smooth manifold]], the [[algebra of functions|algebra of]] [[smooth functions]] $C^\infty(X)$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) becomes a [[Poisson algebra]] (def. \ref{SuperPoissonAlgebra}) with [[Poisson bracket]] given by

$$
  \{f,g\}
  \;\coloneqq\;
  \pi^{i j} \frac{\partial f}{\partial x^i} \frac{\partial g}{\partial x^j}
  \,.
$$

Moreover, for every symmetric tensor $\alpha \in V \otimes V$, the [[Moyal star product]] associated with $\tfrac{1}{2}\pi + \alpha$

$$
  \array{
    C^\infty(V)[ [\hbar] ] \otimes C^\infty(V)[ [\hbar] ]
      &\overset{\star_{\tfrac{1}{2}\pi + \alpha}}{\longrightarrow}&
    C^\infty(V)[ [\hbar] ]
    \\
    (f,g)
      &\mapsto&
    ((-)\cdot (-)) \circ \exp\left( (\tfrac{1}{2}\pi^{i j} + \alpha^{i j}) \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}  \right\}
  }
  (f,g)
$$

is a [[formal deformation quantization]] (def. \ref{FormalDeformationQuantization}) of this [[Poisson algebra]]-structure.

=--


$\,$


**[[Moyal star product]] via [[geometric quantization]] of [[symplectic groupoid]]**
  {#MoyalStarProductViaGeometricQuantization}

+-- {: .num_prop #IntegralRepresentationOfStarProduct}
###### Proposition
**([[integral]] representation of [[star product]])**

If $\pi$ skew-symmetric and invertible, in that there exists $\omega \in V^\ast \otimes V^\ast$ with $\pi^{i j}\omega_{j k} = \delta^i_k$, and if the functions $f,g$ admit [[Fourier transform|Fourier analysis]] (are [[functions with rapidly decreasing partial derivatives]]), then  their [[star product]] (def. \ref{StarPoduct}) is equivalently given by the following [[integral]] expression:

$$
  \begin{aligned}
  \left(f \star_\pi g\right)(x)
   &=
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{ \tfrac{1}{i \hbar} \omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

=--

([Baker 58](Moyal+deformation+quantization#Baker58))

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
  \left(f \star_\pi g\right)(x)
  & \coloneqq
  prod
    \circ \exp\left(
       \hbar \pi^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)(f, g)
  \\
  & =
  \frac{1}{(2 \pi)^{2n}}
  \frac{1}{(2 \pi)^{2n}}
  \int
  \int
    \underbrace{
      e^{ i \hbar \pi(k,q) }
    }
    \underbrace{
      e^{i k \cdot (x-y)}
      f(y)
    }
    \underbrace{
      e^{i q \cdot (x- \tilde y)}
      g(\tilde y)
    }
   \,
   d^{2 n} k
   \,
   d^{2 n} q
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
   \\
   & =
  \frac{1}{(2 \pi)^{2n}}
  \int
    \delta\left( x - \tilde y + \hbar \pi \cdot k \right)
    e^{i k \cdot (x-y)}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} k
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
   \\
   & = 
  \frac{1}{(2 \pi)^{2n}}
  \int
    \delta\left( x - \tilde y + z \right)
    e^{ \tfrac{i}{\hbar} \omega(z, (x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} z
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \\
  & =
  \frac{(det(\pi)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{\tfrac{1}{i \hbar}\omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

Here in the first step we expressed $f$ and $g$ both by their [[Fourier transform]] (inserting the Fourier expression of the [[delta distribution]] from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution)) and used that under this transformation the [[partial derivative]] $\pi^{a b} \frac{\partial}{\partial\phi^a}{\frac{\partial}{\phi^b}}$ turns into the product with $i \pi^{i j} k_i k_j$ ([this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)).
Then we identified again the Fourier-expansion of a [[delta distribution]]
and finally we applied the [[change of integration variables]] $k = \tfrac{1}{\hbar}\omega \cdot z$ and then evaluated the [[delta distribution]].

=--

Next we express this as the [[groupoid convolution product]] of polarized sections of the [[symplectic groupoid]]. To this end, we first need the following definnition:


+-- {: .num_defn #SymplecticGroupoidOfSymplecticVectorSpace}
###### Definition
**([[symplectic groupoid]] of [[symplectic vector space]])**

Assume that $\pi$ is the inverse of a [[symplectic form]] $\omega$ on $\mathbb{R}^{2n}$. Then the [[Cartesian product]] 

$$
  \array{
    && \mathbb{R}^{2n} \times \mathbb{R}^{2n}
    \\
    & {}^{\mathllap{pr_1}}\swarrow && \searrow^{\mathrlap{pr_2}}
    \\
    \mathbb{R}^{2n} && && \mathbb{R}^{2n}
  }
$$

inherits the symplectic structure

$$
  \Omega
  \;\coloneqq\;
  \left(
    pr_1^\ast \omega - pr_2^\ast \omega
  \right)
$$

given by

$$
  \begin{aligned}
    \Omega 
    & = 
    \omega_{i j} d x^i \wedge d x^j - \omega_{i j} d y^i \wedge d y^j
    \\
    & =
    \omega_{i j} ( d x^i - d y^i ) \wedge ( d x^j +  d y^j )
  \end{aligned}
  \,.
$$

The [[pair groupoid]] on $\mathbb{R}^{2n}$ equipped with this [[symplectic form]] on its space of [[morphisms]] is a [[symplectic groupoid]].

A choice of potential form $\Theta$ for $\Omega$, hence with $\Omega = d \Theta$, is given by

$$
  \Theta 
   \coloneqq
   -\omega_{i j} ( x^i + y^i ) d (x^j - y^j) )  
$$

Choosing the [[real polarization]] spanned by $\partial_{x^i} - \partial_{y^i}$ a polarized section is function $F = F(x,y)$ such that

$$
  \iota_{\partial_{x^j} - \partial_{y^j}}(d F - \tfrac{1}{i \hbar} \tfrac{1}{4} \Theta F) = 0
$$

hence

$$
  \label{PolarizedSectionOnMorphismsOfSymplecticGroupoid}
  F(x,y) 
   = 
  f\left( \tfrac{x + y}{2} \right) e^{ \tfrac{1}{i \hbar} \omega\left(  \tfrac{x - y}{2} , \tfrac{x + y}{2} \right)}
  \,.
$$

=--

+-- {: .num_prop #PolarizedSymplecticGroupoidConvolutionProductOfSymplecticVectorSpaceIsMoyalStarProduct}
###### Proposition
**(polarized [[symplectic groupoid|symplectic]] [[groupoid convolution product]] of [[symplectic vector space]] is given by [[Moyal star product]])**

Given a [[symplectic vector space]] $(\mathbb{R}^{2n}, \omega)$, then 
the [[groupoid convolution product]] on polarized sections (eq:PolarizedSectionOnMorphismsOfSymplecticGroupoid) on its [[symplectic groupoid]] (def. \ref{SymplecticGroupoidOfSymplecticVectorSpace}), given by [[convolution product]] followed by averaging ([[integration]]) over the polarization [[fiber]], is given by the [[star product]] (def. \ref{StarPoduct}) for the corresponding [[Poisson tensor]] $\pi \coloneqq \omega^{-1}$, in that

$$
  \begin{aligned}
    \int \int 
      F(x,t) G(t,y) \, d^{2n} t \, d^{2n} (x-y)
    & = 
    (f \star_\pi g)((x+y)/2)
  \end{aligned} 
  \,.
$$

=--

([Weinstein 91, p. 446](Moyal+deformation+quantization#Weinstein91), [Garcia-Bondia & Varilly 94, section V](Moyal+deformation+quantization#GBV), [Hawkins 06, example6.2](Moyal+deformation+quantization#EH))

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
    &
    \int \int 
      F(x,t) G(t,y) \, d^{2n} t \, d^{2n} (x-y)
    \\
    & \coloneqq
    \int \int f((x + t)/2) g( (t + y)/2 ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( x-t, x+t ) + \tfrac{1}{i \hbar} \tfrac{1}{4} \omega(t-y, t + y)  }
    \, d^{2n} t
    \, d^{2n} (x-y)
    \\
    & = 
    \int \int 
      f(t/2) g( (t - (x - y))/2 ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) + (x - y) - t, t ) + \tfrac{1}{i \hbar} \tfrac{1}{4} \omega(t-(x+y), t - (x-y))  }
    \, d^{2n} t
    \, d^{2n} (x-y)   
    \\
    & =  
    \int \int 
      f(t/2) g( \tilde t / 2) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) - \tilde t, t ) - \tfrac{1}{i \hbar} \tfrac{1}{4} \omega((x+y)-t, \tilde t)  }
    \, d^{2n} t
    \, d^{2n} \tilde t
    \\
    & = 
    \int \int 
      f(t) g( \tilde t ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) - 2 \tilde t, 2 t ) - \tfrac{1}{ii \hbar} \tfrac{1}{4} \omega((x+y)- 2 t, 2 \tilde t)  }
    \, d^{2n} t
    \, d^{2n} \tilde t
    \\
    \\
    & = 
    \int \int
       f(t) g(\tilde t )
      e^{ \tfrac{1}{i \hbar} \omega\left( \tfrac{1}{2}(x+y) - \tilde t, \tfrac{1}{2}(x + y) - t  \right)}   
     \, d^{2n} t
     \, d^{2n} \tilde t
    \\
    & = 
    (f \star_\omega g)((x+y)/2)
  \end{aligned} 
$$

The first line just unwinds the definition of polarized sections from def. \ref{SymplecticGroupoidOfSymplecticVectorSpace}, the following lines each implement a [[change of integration variables]] and 
finally in the last line we used prop. \ref{IntegralRepresentationOfStarProduct}.

=--

$\,$

**Example: [[Wick algebra]] of [[normal ordered products]] on [[Kähler vector space]]**
 {#WickAlgebraOfNormalOrderedProductsOnKählerVectorspace}



+-- {: .num_defn #AlmostKaehlerVectorSpace}
###### Definition
**([[Kähler vector space]])**

An _[[Kähler vector space]]_ is a [[real vector space]] $V$ equipped with a [[linear complex structure]] $J$ as well as two [[bilinear forms]] $\omega, g \;\colon\; V \otimes_{\mathbb{R}} V \longrightarrow \mathbb{R}$ such that the following equivalent conditions hold:

1. $\omega(J v, J w) = \omega(v,w)$ and $g(v,w) = \omega(v,J w)$;

1. with $V$ regarded as a [[smooth manifold]] and with $\omega, g$ regarded as constant [[tensors]], then $(V, \omega, g)$ is an [[almost Kähler manifold]].

=--

+-- {: .num_example #StandardAlmostKaehlerVectorSpaces}
###### Example
**(standard [[Kähler vector spaces]])**

Let $V \coloneqq \mathbb{R}^2$ equipped with the [[complex structure]] $J$ which is given by the canonical identification $\mathbb{R}^2 \simeq \mathbb{C}$, hence, in terms of the canonical [[linear basis]] $(e_i)$ of $\mathbb{R}^2$, this is

$$
  J = (J^i{}_j) 
  \coloneqq 
  \left( 
    \array{
      0 & -1
      \\
      1 & 0
    }
  \right)
  \,.
$$

Moreover let 

$$
  \omega = (\omega_{i j}) \coloneqq \left( \array{0 & 1 \\ -1 & 0} \right)
$$ 

and 

$$
  g = (g_{i j}) \coloneqq \left( \array{ 1 & 0 \\ 0 & 1}  \right)
  \,.
$$ 

Then $(V, J, \omega, g)$ is a [[Kähler vector space]] (def. \ref{AlmostKaehlerVectorSpace}).

The corresponding [[Kähler manifold]] is $\mathbb{R}^2$ regarded as a [[smooth manifold]] in the standard way and equipped with the [[bilinear forms]] $J, \omega g$ extended as constant rank-2 [[tensors]] over this manifold.

If we write 

$$
  x,y \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for the standard [[coordinate functions]] on $\mathbb{R}^2$ with 

$$
  z \coloneqq x + i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

and

$$
 \overline{z} \coloneqq x - i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

for the corresponding complex coordinates, then this translates to 

$$
  \omega
  \in
  \Omega^2(\mathbb{R}^2)
$$ 

being the [[differential 2-form]] given by

$$
  \begin{aligned}
    \omega
    & =
    d x \wedge d y
    \\
    & =
    \tfrac{1}{2i} d z \wedge d \overline{z}
  \end{aligned}
$$

and with [[Riemannian metric]] [[tensor]] given by

$$
  g = d x \otimes d x + d y \otimes d y
  \,.
$$

The [[Hermitian form]] is given by

$$
  \begin{aligned}
    h 
    & = 
    g - i \omega
    \\
    & = 
    d z \otimes d \overline{z}
  \end{aligned}
$$


=--

(for more see at _[[Kähler vector space]]_ [this example](Kähler+vector+space#StandardAlmostKaehlerVectorSpaces)).

+-- {: .num_defn #WickAlgebraOfAlmostKaehlerVectorSpace}
###### Definition
**([[Wick algebra]] of a [[Kähler vector space]])**

Let $(\mathbb{R}^{2n},\sigma, g)$ be a [[Kähler vector space]] (def. \ref{AlmostKaehlerVectorSpace}). Then its _Wick algebra_ is the [[formal power series]] vector space $\mathbb{C}[ [ \mathbb{R}^{2n}  ] ] [ [ \hbar ] ]$ equipped with the [[star product]] (def. \ref{StarPoduct})
which is given by the [[bilinear form]]

$$
  \label{InStarProductTensorInvertingHermitianForm}
  \pi \coloneqq \tfrac{i}{2} \omega^{-1} + \tfrac{1}{2} g^{-1}
  \,,
$$

hence:

$$
  \begin{aligned}
    A_1 \star_\pi A_2
    & \coloneqq
    ((-)\cdot (-)) \circ \exp \left( \hbar\underoverset{k_1, k_2 = 1}{2 n}{\sum}\pi^{a b} \partial_a \otimes  \partial_b \right)  (A_1 \otimes A_2)
    \\
    & =
    A_1 \cdot A_2 + \hbar \underoverset{k_1, k_2 = 1}{2n}{\sum}\pi^{k_1 k_2}(\partial_{k_1} A_1) \cdot (\partial_{k_2} A_2)
    + \cdots
  \end{aligned}
$$

=--

(e.g. [Collini 16, def. 1](star+product#Collini16))


+-- {: .num_prop #StarProductAlgebraOfKaehlerVectorSpaceIsStarAlgebra}
###### Proposition
**([[star product]] [[associative algebra|algebra]] of [[Kähler vector space]] is [[star-algebra]])**

Under [[complex conjugation]] the [[star product]] $\star_\pi$ of a [[Kähler vector space]] structure (def. \ref{WickAlgebraOfAlmostKaehlerVectorSpace}) is a [[star algebra]] in that for all $A_1, A_2 \in \mathbb{C}[ [\mathbb{R}^{2n}] ][ [\hbar] ]$ we have

$$
  \left( A_1 \star_\pi A_2 \right)^\ast
  \;=\;
  A_2^\ast \star_\pi A_1^\ast
$$

=--

+-- {: .proof}
###### Proof

This follows directly from that fact that in $\pi = \tfrac{i}{2} \omega^{-1} + \tfrac{1}{2} g^{-1}$ the [[imaginary part]] coincides with the skew-symmetric part, so that

$$
  \begin{aligned}
    (\pi^\ast)^{a b}
    & =
    -\tfrac{i}{2} (\omega^{-1})^{a b}
    + \tfrac{1}{2} (g^{-1})^{a b}
    \\
    & = 
    \tfrac{i}{2} (\omega^{-1})^{b a}
    +   
    \tfrac{1}{2} (g^{-1})^{b a}
    \\
    & = \pi^{b a}
    \,.
  \end{aligned}
$$



=--


+-- {: .num_example #WickAlgebraOfASingleMode}
###### Example
**([[Wick algebra]] of a single mode)**

Let $V \coloneqq \mathbb{R}^2 \simeq Span(\{x,y\})$ be the standard [[Kähler vector space]] according to example \ref{StandardAlmostKaehlerVectorSpaces}, with canonical coordinates denoted $x$ and $y$. We discuss its Wick algebra according to def. \ref{WickAlgebraOfAlmostKaehlerVectorSpace} and show that this reproduces the traditional definition of products of "normal ordered" operators as [above](#Idea).

To that end, consider the complex linear combination of the coordinates to the canonical complex coordinates 

$$
  z \;\coloneqq\; x + i y
  \phantom{AAA} 
    \text{and} 
  \phantom{AAA}
  \overline{z} \coloneqq x - i y
$$ 

which we use in the form

$$
  a^\ast \;\coloneqq\; \tfrac{1}{\sqrt{2}}(x + i y)
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  a \;\coloneqq\; \tfrac{1}{\sqrt{2}}(x - i y)
$$

(with "$a$" the traditional symbol for the _[[amplitude]]_ of a field mode).

Now

$$
  \omega^{-1}
  =
  \frac{\partial}{\partial y} \otimes \frac{\partial}{\partial x}  
  -
  \frac{\partial}{\partial x} \otimes \frac{\partial}{\partial y}
$$

$$
  g^{-1} 
  =
  \frac{\partial}{\partial x} 
  \otimes
  \frac{\partial}{\partial x} 
  +
  \frac{\partial}{\partial y} 
  \otimes
  \frac{\partial}{\partial y} 
$$

so that with

$$
  \frac{\partial}{\partial z}
  =
  \tfrac{1}{2}
  \left(
     \frac{\partial}{\partial x}
     -i
     \frac{\partial}{\partial y}
  \right)
  \phantom{AAAA}
  \frac{\partial}{\partial \overline{z}}
  =
  \frac{1}{2}
  \left(
    \frac{\partial}{\partial x}
    +
    i
    \frac{\partial}{\partial y}
  \right)
$$

we get

$$
  \begin{aligned}
    \tfrac{i \hbar}{2}\omega^{-1} + \tfrac{\hbar}{2} g^{-1}
    & =
    2 \hbar
    \frac{\partial}{\partial \overline{z}}
      \otimes 
    \frac{\partial}{\partial z}
    \\
    & =
    \hbar \frac{\partial}{\partial a} \otimes \frac{\partial }{\partial a^\ast}
  \end{aligned}
$$

Using this, we find the [[star product]] 

$$
  A \star_\pi B
  \;=\;
  prod \circ \exp\left( \hbar \frac{\partial}{\partial a} \otimes \frac{\partial }{\partial a^\ast}  \right)
$$

to be as follows (where we write $(-)\cdot (-)$ for the plain commutative product in the [[formal power series algebra]]):

$$
  \begin{aligned}
    a \star_\pi a & = a \cdot a
    \\
    a^\ast \star_\pi a^\ast & = a^\ast \cdot a^\ast
    \\
    a^\ast \star_\pi a & = a^\ast \cdot a
    \\
    a \star_\pi a^\ast
    & =
    a \cdot a^\ast + \hbar
  \end{aligned}
$$

and so forth, for instance

$$
  \array{
    (a \cdot a ) \star_\pi (a^\ast \cdot a^\ast)
    & =
    a^\ast \cdot a^\ast \cdot a \cdot a
    +
    4 \hbar a^\ast \cdot a
    +   
    \hbar^2
  }
$$

If we instead indicate the commutative pointwise product by colons and the star product by plain juxtaposition

$$
  :f g: \;\coloneqq\; f \cdot g
  \phantom{AAAA}
  f g \;\coloneqq\; f \star_\pi
$$

then this reads

$$
  \array{
    :a a: \, :a^\ast a^\ast:
    & =
    : a^\ast a^\ast a  a :
    +
    4 \hbar \, : a^\ast a :
    +   
    \hbar^2
  }
$$

This is the way the _[[Wick algebra]]_ with its _[[operator product]]_ $\star_\pi$  and _[[normal-ordered product]]_ $:-:$ is traditionally presented. 

=--

$\,$

**[[star products]] on [[regular polynomial observables]] in [[field theory]]**
  {#RegularPolynomialFieldTheoryStarProduct}


+-- {: .num_prop #PropagatorStarProduct}
###### Proposition
**([[star products]] on [[regular polynomial observables]] induced from [[propagators]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] with [[field bundle]] $E \overset{fb}{\to} \Sigma$, and let $\Delta \in \Gamma'_\Sigma((E \boxtimes E)^\ast)$ be a [[distribution of two variables]] on [[field histories]].  

On the [[off-shell]] [[regular polynomial observables]] with a [[formal power series|formal paramater]] $\hbar$ adjoined consider the bilinear map

$$
  PolyObs(E)_{reg}[ [\hbar] ]
    \otimes
  PolyObs(E)_{reg} [ [ \hbar ] ]
    \overset{\star_{\Delta}}{\longrightarrow} 
  PolyObs(E)_{reg}[ [\hbar] ]
$$

given as in def. \ref{StarPoduct}, but with [[partial derivatives]] replaced by [[functional derivatives]]

$$
  A_1 \star_{\Delta} A_2
  \;\coloneqq\;
  ((-)\cdot(-))
  \circ
  \exp\left(
    \int_\Sigma \Delta^{a b}(x,y)
    \frac{\delta}{\delta \Phi^a(x)}
      \otimes
    \frac{\delta}{\delta \Phi^b(y)}
  \right)
  (A_1 \otimes A_2)
$$

As in prop. \ref{AssociativeAndUnitalStarProduct} this defines a [[unital algebra|unital]] and [[associative algebra]] [[structure]].

If the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] $P\Phi ) = 0$ induced by the [[Lagrangian density]] $\mathbf{L}$ are [[Green hyperbolic differential equations]] and if $\Delta$ is a _homogeneous_ [[propagator]] for these [[differential equations]] in that $P \Delta = 0$, then this [[star product]] algebra descends to the [[on-shell]] [[regular polynomial observables]]

$$
  PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
    \otimes
  PolyObs(E, \mathbf{L})_{reg} [ [ \hbar ] ]
    \overset{\star_{\Delta}}{\longrightarrow} 
  PolyObs(E, \mathbf{L})_{reg}[ [\hbar] ]
  \,.
$$

=--


+-- {: .proof}
###### Proof

The proof of prop. \ref{AssociativeAndUnitalStarProduct} goes through verbatim in the present case, as long as all [[products of distributions]] that appear when the [[propagator]] is multiplied with the [[coefficients]] of the [[polynomial observables]] are well-defined, in that [[Hörmander's criterion]] (prop. \ref{HoermanderCriterionForProductOfDistributions}) on the [[wave front sets]] (def. \ref{WaveFrontSet}) of the [[propagator]] and of these [[coefficients]] is met. But the definition the [[coefficients]] of [[regular polynomial observables]] are [[non-singular distributions]], whose wave front set is necessarily empty (example \ref{NonSingularDistributionTrivialWaveFrontSet}), so that their [[product of distributions]] is always well-defined.


=--


+-- {: .num_cor #FreeGaugeFixedLagrangianFieldTheoryQuantizationOfRegularObservables}
###### Corollary
**([[quantization]] of [[regular polynomial observables]] of [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]])**

Consider a [[gauge fixing|gauge fixed]] (def. \ref{GaugeFixingLagrangianDensity}) [[free field theory|free]] [[Lagrangian field theory]] (def. \ref{FreeFieldTheory}) with BV-BRST-extended [[field bundle]] (remark \ref{FieldBundleBVBRST})

$$
  E_{\text{BV-BRST}}
  \;\coloneqq\;
  T^\ast_{\Sigma,inf}[-1]
  \left( 
     E 
      \times_\Sigma 
     \mathcal{G}[1] 
       \times_\Sigma 
     A 
       \times_\Sigma 
     A[-1]  
  \right)
$$

and with [[causal propagator]] (eq:CausalPropagator)

$$
  \Delta 
    \;\in\; 
  \Gamma'_{\Sigma \times \Sigma}( E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}} )
  \,.
$$

Then the [[star product]] $\star_\Delta$ (def. \ref{StarPoduct}) is well-defined on [[off-shell]] (as well as [[on-shell]]) [[regular polynomial observables]] (def. \ref{PolynomialObservables})

$$
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
    \otimes
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \overset{\star_{\tfrac{i}{2}\Delta}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

and the resulting [[non-commutative algebra]] [[structure]]

$$
  \left(
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \,,\,
    \star_\Delta
  \right)
$$

is a [[formal deformation quantization]] (def. \ref{FormalDeformationQuantization}) of the [[Peierls-Poisson bracket]] on the [[covariant phase space]] (theorem \ref{PPeierlsBracket}), restricted to [[regular polynomial observables]].

=--

([Dito 90](deformation+quantization#Dito90), [Dütsch-Fredenhagen 00](deformation+quantization#DuetschFredenhagen00) [Dütsch-Fredenhagen 01](deformation+quantization#DuetschFredenhagen01), [Hirshfeld-Henselder 02](deformation+quantization#HirschfeldHenselder02))

+-- {: .proof}
###### Proof

As in prop. \ref{PropagatorStarProduct}, the vanishing of the [[wave front set]] of the [[coefficients]] of the [[regular polynomial observables]] implies that all arguments go through as for [[star products]] on [[polynomial algebras]] on [[finite dimensional vector spaces]]. By theorem \ref{PPeierlsBracket} the [[causal propagator]] is the [[integral kernel]] of the [[Peierls-Poisson bracket]], so that the tensor $\pi$ from the definition of the [[Moyal star product]] (example \ref{MoyalStarProduct}) now is

$$
  \pi = \Delta
  \,.
$$

With this the statement follows by example \ref{MoyalStarProductIsFormalDeformationQuantization}.

=--


+-- {: .num_remark #TowardsQuantizationExtendingBeyondRegularPolynomialObservables}
###### Remark
**(extending [[quantization]] beyond [[regular polynomial observables]])**

While cor. \ref{FreeGaugeFixedLagrangianFieldTheoryQuantizationOfRegularObservables} provides a [[quantization]] of the [[regular polynomial observables]] of any [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]], the [[regular polynomial observables]] are too small a subspace of that of all [[polynomial observables]]: 

By example \ref{RegularPolynomialLocalObservablesAreNecessarilyLinear} the only [[local observables]] (def. \ref{LocalObservables}) contained among the [[regular polynomial observables]] are the [[linear observables]] (def. \ref{LinearObservables}). But in general it is necessary to consider also non-linear polynomial [[local observables]]. Notably the [[interaction]] [[action functionals]] $S_{int}$ induced from interaction [[Lagrangian densities]] $\mathbf{L}_{int}$ (example \ref{ActionFunctional}) are non-linear polynomial observables.

For example:

* For [[quantum electrodynamics]] on [[Minkowski spacetime]] (example \ref{LagrangianQED}) the [[adiabatic switching|adiabatically switched]] [[action functional]] (example \ref{ActionFunctional}) which is the [[transgression of variational differential forms|transgression]] of the [[electron-photon interaction]] is a cubic [[local observable]]

  $$
    S_{int} 
      \;=\; 
    i
    \underset{\Sigma}{\int}
      g_{sw}(x)
      \,
      (\gamma^\mu)^{\alpha}{}_\beta
      \,
      \overline{\mathbf{\Psi}}_\alpha(x) 
      \cdot \mathbf{\Psi}^\beta(x) 
      \cdot \mathbf{A}^a(x)
      \, dvol_\Sigma(x) 
  $$

* For [[scalar field]] [[phi^n theory]] (example \ref{phintheoryLagrangian}) the [[adiabatic switching|adiabatically switched]] [[action functional]] (example \ref{ActionFunctional}) which is the [[transgression of variational differential forms|transgression]] of the [[phi^n interaction]]

  $$
    S_{int} 
     \;=\;
   \underset{\Sigma}{\int} 
     g_{sw} 
     \,
     \underset{
       n \, \text{factors}
     }{
     \underbrace{
       \mathbf{\Phi}(x)
        \cdot
       \mathbf{\Phi}(x)
         \cdots
       \mathbf{\Phi}(x)
         \cdot
       \mathbf{\Phi}(x)
     }
     }
   \, 
   dvol_\Sigma(x)
  $$ 

  is a [[local observable]] of order $n$.

Therefore one needs to extend the [[formal deformation quantization]] provided by corollary \ref{FreeGaugeFixedLagrangianFieldTheoryQuantizationOfRegularObservables} to a larger subspace of [[polynomial observables]] that includes at least the [[local observables]].

But prop. \ref{SymmetricContribution} characterizes the freedom in choosing a [[formal deformation quantization]]: We may shift the [[causal propagator]] by a symmetric contribution. In view of prop. \ref{PropagatorStarProduct} and in view of of  [[Hörmander's criterion]] for the [[product of distributions]] (prop. \ref{HoermanderCriterionForProductOfDistributions}) to be well defined, we are looking for symmetric [[integral kernels]] $H$ such that the sum

$$
  \label{ShiftingCausalPropagatorBySymmetricContribution}
  \Delta_H = \tfrac{i}{2}\Delta + H
$$

has a _smaller_ [[wave front set]] (def. \ref{WaveFrontSet}) than $\tfrac{i}{2}\Delta$ itself has. The smaller $WF(\tfrac{i}{2}\Delta + H)$, the larger the subspace of [[polynomial observables]] on which the corresponding [[formal deformation quantization]] exists.

Now by prop. \ref{SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime} the [[Wightman propagator]] $\Delta_H$ is of the form (eq:ShiftingCausalPropagatorBySymmetricContribution) and by prop. \ref{WaveFronSetsForKGPropagatorsOnMinkowski} its [[wave front set]] is only "half" that of the [[causal propagator]]. It turns out that $\Delta_H$ does yield a [[formal deformation quantization]] of a subspace of [[polynomial observables]] that includes all [[local observables]]: this is the _[[Wick algebra]]_ on [[microcausal polynomial observables]]. We discuss this in detail in the chapter _[Free quantum fields](#FreeQuantumFields)_.

With such a [[formal deformation quantization]] of the [[local observables]] [[free field theory]] in hand, we may then finally obtain also a formal deformation quantization of [[interaction|interacting]] [[Lagrangian field theories]] by [[perturbative quantum field theory|perturbation theory]]. This we discuss in the chapters _[Scattering](#Scattering)_ and _[Quantum observables](#QuantumObservables)_.

=--

$\,$



This concludes our discussion of some basic concepts of [[quantization]]. In the [next chapter](#FreeQuantumFields) we apply this to discuss the [[algebra of quantum observables]] of [[free field theories|free]] [[Lagrangian field theories]]. Further below in the chapter _[Quantum observables](#QuantumObservables)_ we then discuss also the quantization of the [[interaction|interacting]] [[Lagrangian field theories]], [[perturbation theory|perturbatively]].
