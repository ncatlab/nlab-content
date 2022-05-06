
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Geometric quantization is one formalization of the notion of _[[quantization]]_ of a [[classical mechanical system]]/[[classical field theory]] to a [[quantum mechanical system]]/[[quantum field theory]]. In comparison to _[[deformation quantization]]_ it focuses on [[spaces of states]], hence on the [[Schrödinger picture]] of [[quantum mechanics]].

### Ingredients

With a [[symplectic manifold]] regarded as a [[classical mechanical system]], _geometric quantization_ produces [[quantization]] of this to a [[quantum mechanical system]] by 

1. realize the [[symplectic form]] as the [[curvature]] of a $U(1)$-[[principal bundle]] with [[connection on a bundle|connection]] (which requires the form to have integral [[periods]]): called the [[prequantum circle bundle]];

1. choose a [[polarization]] -- a splitting of the abstract [[phase space]] into "coordinates" and "momenta";

and then form

1. a [[Hilbert space]] of [[states]] as the space of [[sections]] of the [[associated bundle|associated]] [[line bundle]] which depend only on the "coordinates" (not on the "momenta");

1. associate with every function on the symplectic manifold -- every [[Hamiltonian]] -- a [[linear operator]] on this Hilbert space.

### History and variants
 {#HistoryAndVariants}

The approach is due to [[Alexandre Kirillov]] ("[[orbit method]]"), [[Bertram Kostant]] and [[Jean-Marie Souriau]]. See the [References](#ReferencesGeneral) below. It is closely related to [[Berezin quantization]] and the subject of [[coherent states]].


<img src="http://ncatlab.org/nlab/files/SouriauPrequantumFlowChart.jpg" alt="Prequantum flow chart" />

([Souriau 74, fig 1](#Souriau74))


In a long term project [[Alan Weinstein]] and many of his students have followed the idea that the true story behind geometric quantization crucially involves [[symplectic Lie groupoids]]: [[higher symplectic geometry]]. See [[geometric quantization of symplectic groupoids]] for more on this. 

More generally, there is _[[higher geometric quantization]]_.


### Overview 

> This overview is taken from ([Baez](#Baez)).

_Geometric quantization_ is a tool for understanding the relation between [[classical physics]] and [[quantum field theory|quantum physics]]. Here's a brief sketch of how it goes. 

1. We start with a *classical [[phase space]]*: mathematically, this is a [[manifold]] $X$ with a [[symplectic geometry|symplectic structure]] $\omega$.

1. Then we do *prequantization*: this gives us a Hermitian [[line bundle]] $L$ over $X$, equipped with a $U(1)$ [[connection on a bundle|connection]] $D$ whose curvature equals $i \omega$. $L$ is called the **[[prequantum line bundle]]**.

   **Warning:** we can only do this step if $\omega$ satisfies the *Bohr--Sommerfeld condition*, which says that $\omega/2\pi$ defines an [[integral cohomology]] class. If this condition holds, $L$ and $D$ are determined up to [[isomorphism]], but not canonically.

1. The [[Hilbert space]] $H_0$ of square-integrable [[section]]s of $L$ is called the *prequantum Hilbert space*. This is not yet the Hilbert space of our quantized theory -- it's too big. But it's a good step in the right direction. In particular, we can *prequantize classical observables*: there's a map sending any smooth function on $X$ to an operator on $H_0$. This map takes [[Poisson bracket]]s to [[commutator]]s, just as one would hope. The formula for this map involves the [[connection on a bundle|connection]] $D$.

1. To cut down the prequantum Hilbert space, we need to choose a *[[polarization]]*, say $P$. What's this? Well, for each point $x \in X$, a polarization picks out a certain subspace $P_x$ of the complexified [[tangent bundle|tangent space]] at $x$. We define the *quantum Hilbert space*, $H$, to be the space of all square-integrable sections of $L$ that give zero when we take their [[covariant derivative]] at any point $x$ in the direction of any vector in $P_x$. The quantum Hilbert space is a subspace of the prequantum Hilbert space.

   **Warning:** for $P$ to be a polarization, there are some crucial technical conditions we impose on the subspaces $P_x$. First, they must be *isotropic*: the complexified symplectic form $\omega$ must vanish on them. Second, they must be *Lagrangian*: they must be maximal isotropic subspaces. Third, they must vary smoothly with $x$. And fourth, they must be *integrable*.

1. The easiest sort of polarization to understand is a *real polarization*. This is where the subspaces $P_x$ come from subspaces of the tangent space by complexification. It boils down to this: a [[real polarization]] is an [[integrable distribution]] $P$ on the classical phase space where each space $P_x$ is [[Lagrangian subspace]] of the [[tangent space]] $T_x X$.

1. To understand this rigamarole, one must study examples! First, it's good to understand how good old *Schr&#246;dinger quantization* fits into this framework. Remember, in Schr&#246;dinger quantization we take our classical [[phase space]] $X$ to be the [[cotangent bundle]] $T^* M$ of a [[manifold]] $M$ called the *classical configuration space*. We then let our quantum Hilbert space be the space of all [[square-integrable functions]] on $M$.

   Modulo some technical trickery, we get this example when we run the above machinery and use a certain god-given real polarization on $X = T^*M$, namely the one given by the vertical vectors.

1. It's also good to study the *Bargmann--Segal representation*, which we get by taking $X = \mathbb{C}^n$ with its god-given symplectic structure (the imaginary part of the inner product) and using the god-given *K&#228;hler polarization*. When we do this, our quantum Hilbert space consists of analytic functions on $\mathbb{C}^n$ which are square-integrable with respect to a Gaussian measure centered at the origin.

1. The next step is to *quantize classical observables*, turning them into linear operators on the quantum Hilbert space $H$. Unfortunately, we can't quantize all such observables while still sending [[Poisson bracket]]s to [[commutator]]s, as we did at the prequantum level. So at this point things get trickier and my brief outline will stop. Ultimately, the reason for this problem is that quantization is not a [[functor]] from the [[category]] of symplectic manifolds to the category of Hilbert spaces -- but for that one needs to learn a bit about [[category theory]]. 

### Basic Jargon 

Here are some definitions of important terms. Unfortunately they are defined using other terms that you might not understand. If you are really mystified, you need to read some books on [[differential geometry]] and the math of [[classical mechanics]] before proceeding.

* **complexification**: We can tensor a real vector space with the complex numbers and get a complex vector space; this process is called complexification. For example, we can complexify the tangent space at some point of a manifold, which amounts to forming the space of complex linear combinations of tangent vectors at that point.

* **distribution**: The word "distribution" means many different things in mathematics, but here's one: a "distribution" $V$ on a manifold $X$ is a choice of a subspace $V_x$ of each tangent space $T_p X$, where the choice depends smoothly on $x$.

* **Hamiltonian vector field**: Given a manifold $X$ with a symplectic structure $\omega$, any smooth function $f: X \to \mathbb{R}$ can be thought of as a "Hamiltonian", meaning physically that we think of it as the energy function and let it give rise to a flow on $X$ describing the time evolution of states. Mathematically speaking, this flow is generated by a vector field $v(f)$ called the "Hamiltonian vector field" associated to $f$. It is the unique vector field such that

  $$
    \omega(-, v(f)) = d f
  $$

  In other words, for any vector field $u$ on $X$ we have

  $$
    \omega(u,v(f)) = d f(u) = u f
  $$


  The vector field $v(f)$ is guaranteed to exist by the fact that $\omega$ is nondegenerate.

* **[[integrable distribution]]**: A [[distribution of subspaces]] of the [[tangent bundle]] on a [[smooth manifold]] $X$ is "integrable" if at least locally, there is a [[foliation]] of $X$ by submanifolds such that $V_x$ is the tangent space of the submanifold containing the point $x$.

* **[[integral cohomology]] class**: Any closed [[differential p-form]] on a [[smooth manifold]] $M$ defines an element of the $p$th [[de Rham cohomology]] of $M$. This is a finite-dimensional vector space, and it contains a lattice called the $p$th integral [[cohomology group]] of $M$. We say a cohomology class is integral if it lies in this lattice. Most notably, if you take any $U(1)$ [[connection on a bundle|connection]] on any Hermitian line bundle over $M$, its curvature $2$-form will define an integral cohomology class once you divide it by $2 \pi i$. This cohomology class is called the first [[Chern class]], and it serves to determine the line [[bundle]] up to [[isomorphism]].

* **[[Poisson bracket]]s**: Given a symplectic structure on a manifold $M$ and given two smooth functions on that manifold, say $f$ and $g$, there's a trick for getting a new smooth function $\{f,g\}$ on the manifold, called the Poisson bracket of $f$ and $g$.

  This trick works as follows: given any smooth function $f$ we can take its differential $d f$, which is a $1$-form. Then there is a unique vector field $v(f)$, the Hamiltonian vector field associated to $f$, such that

  $$
    \omega(-,v(f)) = d f
  $$

   Using this we define

   $$
     \{f,g\} = \omega(v(f),v(g))
   $$

   It's easy to check that we also have $\{f,g\} = d g(v(f)) = v(f) g$. So $\{f,g\}$ says how much $g$ changes as we differentiate it in the direction of the Hamiltonian vector field generated by $f$.

   In the familiar case where $M$ is $\mathbb{R}^{2n}$ with momentum and position coordinates $p_i$, $q_i$, the Poisson brackets of $f$ and $g$ work out to be

   $$
     \{f,g\} = \sum_i \frac{d f}{d p_i} \frac{d g}{d q_i} - \frac{d f}{d q_i}\frac{d g}{d p_i}
   $$

* **square-integrable sections**: We can define an inner product on the sections of a Hermitian line bundle over a manifold $X$ with a symplectic structure. The symplectic structure defines a volume form which lets us do the necessary integral. A section whose inner product with itself is finite is said to be square-integrable. Such sections form a Hilbert space $H_0$ called the "prequantum Hilbert space". It is a kind of preliminary version of the Hilbert space we get when we quantize the classical system whose phase space is $X$.

* **symplectic structure**: A symplectic structure on a manifold $M$ is a closed $2$-form $\omega$ which is nondegenerate in the sense that for any nonzero tangent vector $u$ at any point of $M$, there is a tangent vector $u$ at that point for which $w(u,v)$ is nonzero.

* **$U(1)$ [[connection on a bundle|connection]]**: The [[group]] $U(1)$ is the group of unit complex numbers. Given a complex line bundle $L$ with an inner product on each fiber $L_x$, a $U(1)$ connection on $L$ is a connection such that parallel translation preserves the inner product.

* **vertical vectors**: Given a bundle $E$ over a manifold $M$, we say a tangent vector to some point of $E$ is vertical if it projects to zero down on $M$. 



## Definition

Geometric quantization involves two steps

1. [Geometric prequantization](#GeometricPrequantization)

1. [Geometric quantization proper](#GeometricQuantizationProper).

### Geometric prequantization 
 {#GeometricPrequantization}

#### Prequantum line bundle

Given the [[symplectic form]] $\omega$, a 
[[prequantum circle bundle]] for it is a 
[[circle n-bundle with connection|circle bundle with connection]] whose [[curvature]] is $\omega$. 

In other words, prequantization is a lift of $\omega$ through the curvature-[[exact sequence]] of [[ordinary differential cohomology]] (see there).

The multiple of the [[Chern class]] of this line bundle is identified with the inverse _[[Planck constant]]_.


#### Prequantum states

A _prequantum state_ is a [[section]] of the [[prequantum bundle]].

This becomes a _[[quantum state]]_ or [[wavefunction]] if [[polarization|polarized]] (...).

#### Prequantum operators

Let $\nabla : X \to \mathbf{B} U(1)_{conn}$ be a
[[prequantum line bundle]] $E \to X$ [[connection on a bundle|with connection]] for $\omega$. Write $\Gamma_X(E)$ for its space of smooth [[sections]], the _[[prequantum space of states]]_.


+-- {: .num_defn #PrequantumOperator}
###### Definition
**([[prequantum operators]])**

For $f \in C^\infty(X, \mathbb{C})$ a function on phase space, the corresponding **[[quantum operator (in geometric quantization)|quantum operator]]** is the linear map

$$
  \hat f \colon \Gamma_X(E) \to \Gamma_X(E)
$$

given by

$$
  \label{FormulaForPrequantumOperator}
  \psi \mapsto -i \nabla_{v_f} \psi + f \cdot \psi
  \,,
$$

where 

* $v_f$ is the [[Hamiltonian vector field]]
corresponding to $f$;

* $\nabla_{v_f} : \Gamma_X(E) \to \Gamma_X(E)$ is the [[covariant derivative]] of sections along $v_f$ for the given choice of prequantum connection;

* $f \cdot (-) : \Gamma_X(E) \to \Gamma_X(E)$ is the operation of degreewise multiplication pf sections.

=--

+-- {: .num_remark #OriginOfTheFormulaForPrequantumOperators}
###### Remark
**(origin of the formulas for [[prequantum operators]])*+

The formula (eq:FormulaForPrequantumOperator) may look a bit mysterious on first sight. The correction term to the [[covariant derivative]] appearing in this formula is ultimately due to the fact that with $v$ the [[Hamiltonian vector field]] corresponding to a [[Hamiltonian]] $H_v$ via

$$
  \iota_v \omega = d H_v
$$

then the [[Lie derivative]] of $\theta$ (the symplectic potentiation, related by $d \theta = \omega$) is

$$
  \mathcal{L}_v \theta = d \tilde H_v
$$

for 

$$
  \tilde H_v = H_v + \iota_v \theta
  \,.
$$

Here the second term on the right is what yields the [[covariant derivative]] in (eq:FormulaForPrequantumOperator), while the first summand is the correction term in (eq:FormulaForPrequantumOperator).

A derivation of these formulas from first principles is given in ([Fiorenza-Rogers-Schreiber 13a](#FiorenzaRogersSchreiber13a), example 3.2.3 and remark 3.3.16).

=--

### Geometric quantization
 {#GeometricQuantizationProper}

Given a [[prequantum bundle]] as above, the actual step of genuine _geometric quantization_ consists first of forming _half_ its space of sections in a certain sense. Physically this means passing to the space of [[wavefunctions]] that depend only on [[canonical coordinates]] but not on [[canonical momenta]]. Second, [[subgroups]] of the group of (exponentiated) [[prequantum operators]] are made to descend to this space of quantum states, these are the [[quantum operators]] or [[quantum observables]].

#### Quantum states
 {#QuantumStates}

Historically, the traditional way to formalize the formation of the [[space of quantum states]] is as a 3-step process

1. choose a [Polarization](#Polarizations);

1. choose a [Metaplectic correction](#MetaplecticCorrection);

1. form the induced [[space of quantum states]] as the space of polarized sections of the [[prequantum line bundle]] tensored a certain half-form bundle.

This we discuss at 

* _[Quantum state space as space of polarized sections](#Polarizations)_

This traditional route via polarizations and metaplectic corrections has the disadvantage that mathematically it is not a very natural operation.  However, under mild conditions it turns out to be [[equivalence|equivalent]] to the following mathematically very natural construction

1. choose a [[KU-orientation]], hence a  [[spin^c structure]] of $X$ compatible with the given prequantum bundle;

1. take the space of quantum states to be the [[push-forward in generalized cohomology|push-forward]] in [[complex K-theory]] of the [[prequantum line bundle]] to the point, hence the [[index]] of the [[spin^c Dirac operator]] twisted by the [[prequantum line bundle]].

This general _[[geometric quantization by push-forward]]_ is discussed below at  

* _[Quantum space of states as index of a Dirac operator](#AsIndexOfSpinCDiracOperator)_.

In the special case that the [[prequantum line bundle]] admits a [[Kähler polarization]] this [[geometric quantization by push-forward|push-forward quantization]] has a direct expression in terms of the [[complex geometry|complex]] [[abelian sheaf cohomology]] and of the [[Dolbeault operator]] of the prequantum [[holomorphic line bundle]]. Now the choice of [[metaplectic correction]] is precisely a  [[spin structure]] (a "[[Theta characteristic]]") and the [[index]] is now that of the [[Dolbeault-Dirac operator]] which is equivalently just the [[Euler characteristic]] of the holomorphic [[abelian sheaf cohomology]] of the [[prequantum line bundle]]. This complex Dolbeault quantization case we discuss in 

* _[Quantum state space as Euler characteristic of prequantum sheaf cohomology](#EulerCharacteristicOfSheafCohomology)_

and

* _[Quantum state space as index of the Dolbeault-Dirac operator](#IndexOfDolbeaultDiracOperator)_.


##### Quantum state space as space of polarized sections 
 {#Polarizations}

For $(X, \omega)$ a [[symplectic manifold]], choose a [[Kähler polarization]], hence an involutive Lagrangian subbundle $\mathcal{P} \subset T_{\mathcal{C}} X$ such that $\mathcal{P} \cap \overline{\mathcal{P}} = 0$.
Choose moreover a [[metaplectic correction]] of $\mathcal{P}$. This defines the [[half-density]] bundle $\sqrt{\Omega \mathcal{P}}$ along $\mathcal{P}$. 

Let now $(L,\nabla)$ be a [[prequantum line bundle]] for $(X,\omega)$.

+-- {: .num_defn #PolarizedQuantumStates}
###### Definition

The [[space of quantum states]] of the prequantum bundle defined by the choice of [[Kähler polarization]] $\mathcal{P}$ and [[metaplectic correction]] $\sqrt{\Omega \mathcal{P}}$ is the space of [[sections]] of the [[tensor product]] $L \otimes \sqrt{\Omega \mathcal{P}}$ which are [[covariant derivative]] covariantly constant with respect to $\nabla$ along $\overline{\mathcal{P}}$ and square integrable with respect to the induced [[integration]] over $X/\overline{\mathcal{P}}$:

$$
  \mathcal{H}_{pol}
  \colon
  L^2
  \left(
  \left\{
   \psi \in \Gamma(L \otimes \sqrt{\Omega \mathcal{P}})
   \;|\;
   \nabla_{\overline{\mathcal{P}}} \psi = 0
  \right\}
  \right)
  \,.
$$

=--

For instance ([Bates-Weinstein, def. 7.17](#BatesWeinstein)).

+-- {: .num_remark}
###### Remark

In the case of [[Kähler polarization]] it is useful to write $\Omega^{n,0}$ for the [[canonical line bundle]] of the polarization and $\sqrt{\Omega^{n,0}}$ for the corresponding choice of [[metaplectic correction]]/[[Theta characteristic]].

=--

##### Quantum state space as Euler characteristic of prequantum sheaf cohomology
 {#EulerCharacteristicOfSheafCohomology}

Let $(X,\omega)$ be a _[[compact topological space]]_ [[symplectic manifold]], $L_\omega$ a [[prequantum line bundle]], $\mathcal{P}$ a [[Kähler polarization]] and $\sqrt{\Omega^{n,0}}$ a [[metaplectic correction]].

+-- {: .num_defn #EulerQuantumStates}
###### Definition

The corresponding Euler quantum Hilbert space  is the [[virtual vector space]]

$$
  \mathcal{H}_{Euler}
  \coloneqq
  \bigoplus_{k = 0}^{n} (-1)^k \, H^{0,k}(X,L_\omega \otimes \sqrt{\Omega^{n,0}})
  \,,
$$

which is the alternating [[direct sum]] of the [[Dolbeault cohomology]] space of $X$ with [[coefficients]] in the [[tensor product]] $L_\omega \otimes \sqrt{\Omega^{n,0}}$ of the [[prequantum line bundle]] with the [[metaplectic correction]]/[[Theta characteristic]].

=--


+-- {: .num_remark #SectionsAndEulerQuantizationCoincidesOnPositiveBundles}
###### Remark

The [[Kodaira vanishing theorem]] asserts that if $L_\omega \sqrt{\Omega^{n,0}}^{-1}$ is a [[positive line bundle]] 
then all the higher [[cohomology groups]] in the above expression vanish. Therefore in this case the definition coincides with that via polarizations in def. \ref{PolarizedQuantumStates} above.

$$
  \left(
    L_\omega \otimes \sqrt{\Omega^{n,0}}^{-1}
    \;
    positive
  \right)
  \Rightarrow
  \left(
    \mathcal{H}_{pol} \simeq \mathcal{H}_{Euler}
  \right)
  \,.
$$

=--



##### Quantum state space as index of Dolbeault-Dirac operator
 {#IndexOfDolbeaultDiracOperator}

Suppose again that $(X,\omega, L_\omega)$ is equipped with a [[Kähler polarization]]. 

We need the following general fact on [[spin structures]] over [[Kähler manifolds]].

+-- {: .num_prop #SpinStructuresOnKaehlerManifolds}
###### Proposition

A choice of [[spin structure]] on the [[Kähler manifold]] $X$ (of real dimension $2n$) is equivalently a choice of [[square root]] ("[[Theta characteristic]]") $\sqrt{\Omega^{n,0}}$ of the [[canonical line bundle]] $\Omega^{n,0}$. 

Given such a choice, there is a [[natural isomorphism]] between the [[spinor bundle]] $S_X$ and the (anti-)holomorphic form bundle tensored by this square root

$$
  S \simeq \Omega^{0,\bullet} \otimes \sqrt{\Omega^{n,0}}
 \,.
$$

Finally, the corresponding [[Dirac operator]] is the [[Dolbeault-Dirac operator]] $\overline{\partial} + \overline{\partial}^\ast$.

=--

See at _[spin structure -- Over a K&#228;hler manifold](spin+structure#OverAKahlerManifold)_.

+-- {: .num_remark}
###### Remark

It follows that the [[Dirac operator]] on $X$ which is twisted by the [[connection on a bundle|connection]] $\nabla$ on the [[prequantum line bundle|prequantum]] [[holomorphic line bundle]] $L_\omega$ is of the form

$$
  \overline{\partial}_\nabla + \overline{\partial}^\ast_\nabla
  \;\colon\;
  \Omega^{0,even/odd}\left(X, \;L_\omega \otimes \sqrt{\Omega^{n,0}}\right)
  \to 
  \Omega^{0,odd/even}\left(X, \; L_\omega \otimes \sqrt{\Omega^{n,0}}\right)
  \,.
$$

Observe how from the point of view of just the [[Dolbeault operator]], this is twisting not just by the prequantum line bundle itself but by the _[[metaplectic correction|metaplectically corrected]]_ prequantum line bundle $L_\omega \otimes \sqrt{\Omega^{n,0}}$, while from the point of view of the [[Dirac operator]] it is just twisting by $L_\omega$, since tensoring with the square root line bundle $\sqrt{\Omega^{n,0}}$ induces the isomorphism between the antiholomorphic differential form bundle and the actual [[spinor bundle]] over the [[Kähler manifold]].

=--

+-- {: .num_defn #DolbeaultDiracSpacesOfStates}
###### Definition

The *Dolbeault-Dirac* space of quantum states of $(X,\omega, L_\omega)$ is the [[index]] of the $L_\omega$-twisted [[Dolbeault-Dirac operator]] (the [[Todd genus]])

$$
  \mathcal{H}_{DolbDir} 
    \coloneqq
  index( \overline{\partial}_\nabla + \overline{\partial}_\nabla^\ast )
  \,.
$$

=--

+-- {: .num_remark #DolbeaultDiracAgreesWithEuler}
###### Remark

This definition agrees with that by [[abelian sheaf cohomology]] in def. \ref{EulerQuantumStates}

$$
  \mathcal{H}_{Euler} \simeq \mathcal{H}_{DolbDirac}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

What before in the quantization prescription [by polarization](#Polarizations) and [by abelian sheaf cohomology](#EulerCharacteristicOfSheafCohomology) was the "[[metaplectic correction]]" introduced "by hand" is now naturally part of the [[isomorphism]] of prop. \ref{SpinStructuresOnKaehlerManifolds} which identifies the [[Dirac operator]] with the [[Dolbeault-Dirac operator]].

=--


##### Quantum state spaces as index of the $Spin^c$-Dirac operator
 {#AsIndexOfSpinCDiracOperator}

Finally we come to the true definition of geometric quantization, the most general and at the same time most natural one which contains the above as special cases. 

The actual definition is def. \ref{KTheoreticQuantization} below. Here we lead up to it by spelling out the ingredients. 

We need the following general facts about [[spin^c Dirac operators]].

+-- {: .num_defn #SpinCAndDeterminantLineBundle}
###### Definition

For $n \in \mathbb{N}$, the [[spin^c]]-[[Lie group]] $Spin^c(n)$  is equivalently

* the [[tensor product]] of the ordinary [[spin group]] $Spin(n)$ with the [[circle group]] over the [[group of order 2]]

  $$
    Spin^c \simeq Spin(n) \underset{\mathbb{Z}_2}{\times} U(1)
  $$

* the [[loop space object]] 

  $$
    Spin^c \simeq \Omega \mathbf{B} Spin^c
  $$

  of the [[homotopy fiber product]] of the universal smooth [[second Stiefel-Whitney class]] and the mod-2 reduction of the universal [[first Chern class]] in [[smooth infinity-groupoids]]:

  $$
    \array{
      \mathbf{B}Spin^c(n) &\stackrel{det}{\to}& \mathbf{B}U(1)
      \\
      \downarrow &\swArrow_\simeq& \downarrow^{\mathrlap{\mathbf{c}_1 \, mod \, 2}}
      \\
      \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    }
    \,.
  $$

Here the top horizontal map is called the universal _[[determinant line bundle]]_ map.

=--

See at _[[spin^c group]]_ for more details.

+-- {: .num_remark #SpinCInComponents}
###### Remark

It follows that if we represent elements of $Spin^c(n) \simeq SO(n) \underset{\mathbb{Z}_2}{\times} U(1)$ as [[equivalence classes]] of pairs $(g,c)$, then the [[determinant line bundle]] map of def. \ref{SpinCAndDeterminantLineBundle} is given by

$$
  det \;\colon \; (g,c) \mapsto 2c
  \,,
$$

where on the right we write the group operation in the [[abelian group]] $U(1)$ additively.

This factor of 2 on the right is crucial in all of the following. 

=--

+-- {: .num_defn #SpinCStructure}
###### Definition

Let $X$ be an [[orientation|oriented]] [[smooth manifold]]. A smooth [[spin^c structure]] on $X$ is a lift $\hat \tau_X$ of the classifying map $\tau_X \colon X \to \mathbf{B} SO(n)$ of its [[tangent bundle]] through the left vertical map in def. \ref{SpinCAndDeterminantLineBundle}

$$
  \array{
    && \mathbf{B} Spin^c(n)
    \\
    & {}^{\mathllap{\hat \tau_X}}\nearrow & \downarrow
    \\
    X &\stackrel{\tau_X}{\to}& \mathbf{B}SO(n)
  }
  \,.
$$

=--

+-- {: .num_remark #SpinCWithDivisibleDetIsSpinTensorLine}
###### Remark

In words this says that a [[spin^c structure]] on an oriented manifold $X$ is a choice of [[circle group]]-[[principal bundle]] or equivalenty of hermitian [[complex line bundle]] such that its [[first Chern class]] modulo 2 equals the [[second Stiefel-Whitney class]] $w_2$ of $X$. If this second Stiefel-Whitney class vanishes (as an element in $H^2(X,\mathbb{Z}_2)$) this means that $X$ has a genuine _[[spin structure]]_. So in other words whenever the [[determinant line bundle]] of a [[spin^c structure]] (in the sens of def. \ref{SpinCAndDeterminantLineBundle}) has a [[first Chern class]] that is divisible by 2, then there is an actual [[spin^c structure]].

We can formalize this statement as follows: there is a [[commuting square]] of the form

$$
  \array{
     \mathbf{B}( Spin(n) \times U(1) ) &\stackrel{((2 \cdot)\circ p_2}{\to}&
     \mathbf{B}U(1)
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 \, mod\, 2}}
     \\
     \mathbf{B}SO(n) &\stackrel{\mathbf{w}^2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
$$

similar to the one in def. \ref{SpinCAndDeterminantLineBundle} but crucially different in that here we have just the [[cartesian product]] of $Spin(n)$ with $U(1)$ in the top left. In the standard presentation of these objects this diagram commutes on the nose (filled by a canonical [[homotopy]]) simply because both ways to go from the top left to the bottom right hit $0 \in \mathbb{Z}_2$: the left-bottom one because $\mathbf{B}Spin(n)$ is essentially by definition such that the second SW class trivializes on it, and the top-right one because first multiplying by 2 and then reducing mod 2 is 0. 

Since the diagram commutes, the [[universal property]] of the above [[homotopy pullback]] says that there is a canonically induced map

$$
  (p_1, p_2) \;\colon\; Spin(n) \times U(1) \to Spin^c(n)
  \,.
$$

Of course this is just the evident [[quotient]] [[projection]] which on elements is simply the identity

$$
  (g,c) \mapsto (g,c)
  \,,
$$

only that on the right we regard the pair $(g,c)$ as a placeholder for its [[equivalence class]] in the [[tensor product]] over $\mathbb{Z}_2$.

Moreover, the [[universal property]] of the [[homotopy pullback]] says that every [[spin^c structure]] $\hat \tau_c$ whose underlying [[determinant line bundle]] is such that its [[first Chern class]] is divisible by 2 actually factors through this map, hence that _it is just the product of an ordinary $Spin$-principal bundle with a circle bundle_.

$$
  \array{
    \mathbf{B}(Spin(n) \times U(1)) &\stackrel{p_2}{\to}& \mathbf{B}U(1)
    \\
    {}^{\mathllap{(p_1,p_2)}}\downarrow && \downarrow^{\mathbf{B}(2 \cdot)}
    \\
    \mathbf{B}Spin^c(n) &\stackrel{det}{\to}& \mathbf{B}U(1)
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{c_1\,mod\,2}}
    \\
    \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

This is the crucial relation by which the K-theoretic quantization will harmonize with the above Euler- and Dolbeault- quantization, discussed below.

=--

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ an even number, write 

$$
  \Delta_n \simeq \mathbb{C}^{2^{n/2}}
$$ 

for the canonical complex [[spin representation]], which decomposes into two chiral [[irreducible representations]]

$$
  \Delta_n \simeq \Delta_n^+ \oplus \Delta_n^-
  \,.
$$

Then the **canonical [[spin^c]]-[[representation]]** 

$$
  \rho \colon Spin^c(n) \times \Delta_n \to \Delta_n
$$

is the one given in the components of remark \ref{SpinCInComponents} by

$$
  ((g,c), \psi) \mapsto (g(\psi)) \cdot c
$$

(first act with the spin-component in the usual way and then multiply by $c \in U(1) \hookrightarrow \mathbb{C}$).


=--

As discussed at _[[representation]]_ we may think of this as a morphism of [[smooth groupoids]] ([[stacks]]) of the form

$$
  \rho \colon \mathbf{B} Spin^c(n) \to \mathbb{C}\mathbf{Mod} \simeq \mathbb{C}\mathbf{Vect}
  \,.
$$
 
+-- {: .num_defn #SpinCSpinorBundle}
###### Definition

Given a [[spin^c structure]] $\hat \tau_X \colon X \to \mathbf{B}Spin^c(n)$, def. \ref{SpinCStructure}, the **[[associated bundle|associated]] [[spinor bundle]]** is the one modulated by

$$
  S^c
  \colon
  X \stackrel{\hat \tau_X}{\to} \mathbf{B}Spin^c(n)
  \stackrel{\rho}{\to} \mathbb{C}\mathbf{Vect}
  \,.
$$

=--

Crucial for the comparison of the K-theoretic quantization to be defined in a moment and the above Euler/Dolbeault quantization is the following:

+-- {: .num_remark #SpinCSpinorsAsTensorProductWhenDetDivisible}
###### Remark

By remark \ref{SpinCWithDivisibleDetIsSpinTensorLine} it follows that in the case that the [[determinant line bundle]] of the [[spin^c structure]] is divisible by 2, hence in the case that $c_1(det(\hat \tau_X)) = 0 \,mod\, 2 \in H^2(X,\mathbb{Z}_2)$, then the $Spin^c$-[[spinor bundle]] of def. \ref{SpinCSpinorBundle} is just the [[tensor product]] of the ordinary underlying [[spinor bundle]] with _half_ the [[determinant line bundle]]:

$$
  \left( c_1(det(\hat \tau_X)) = 0 \,mod\, 2 \right)
  \;\Rightarrow\;
  \left(S^c \simeq S \otimes \sqrt{det(\hat \tau_X)}\right)
  \,.
$$

=--



Let now $(X,\omega)$ be a ([[presymplectic manifold|pre-]])[[symplectic manifold]] and let $(L_{\omega}, \nabla)$ be a [[prequantum line bundle]]. 


+-- {: .num_defn #KTheoreticQuantization}
###### Definition

Given a [[spin^c structure]] $\hat \tau_X$ on $X$ whose underlying [[determinant line bundle]] coincides, up to equivalence, with $(L_\omega)^{\otimes^2}$, then the _[[spin^c quantization]]_ of this prequantum data is the [[index]] of the corresponding [[spin^c Dirac operator]] $D_{\mathbf{c}}$:

$$
  \mathcal{H}_{K} \coloneqq index(D_{\mathbf{c}})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is equivalently the [[fiber integration in generalized cohomology|push-forward]] in [[complex K-theory]] of the [[prequantum line bundle]] to the point. 

Moreover, on [[cocycles]] this push-forward is expressed by the traditional construction of [[Hilbert spaces]] [[space of quantum states|of quantum states]]:

let $X$ be a manifold equipped with a [[Riemannian metric]], a  [[spinor bundle]] and a [[Dirac operator]] $D \colon \Gamma(S) \to \Gamma(S)$. Then the corresponding [[K-homology]] cycle is:

1. the [[Hilbert space]] $L^2(S)$ of [[square integrable function|square integrable]] [[sections]] of the [[spinor bundle]];

1. equipped with the [[action]] by fiberwise multiplication of the [[C*-algebra]] $C_0(X)$ [[algebra of functions|of functions]] [[vanishing at infinity]] 

   $$
     C_0(X) \to \mathcal{B}(L^2(S))
   $$

   (which is by [[bounded operators]])

1. and equipped with the [[Dirac operator]] $D$ as the $\mathbb{Z}_2$-graded [[Fredholm operator]] defining the [[K-homology]] class.

Together with is equivalent an element

$$
  [D, L^2(S)] \in KK(C_0(X), \mathbb{C})
  \,.
$$

Postcomposition of K-theory classes $[\xi] \in KK(\mathbb{C}, C_0(X))$ with this map is the [[fiber integration in generalized cohomology|push-forward]]/[[index]] map in K-theory.

=--

+-- {: .num_remark}
###### Remark

This definition does not assume any choice of [[polarization]], nor any choice of [[complex structure]] etc. On the other hand, every choice of [[almost complex structure]] (hence in particular of [[Kähler polarization]]) does induce a [[spin^c structure]], as discussed there. See also ([Borthwick-Uribe 96](#BorthwickUribe96)).

=--

So then we can compare:

+-- {: .num_prop}
###### Proposition

If a choice of [[Kähler polarization]] exists on the [[compact topological space|compact]] [[prequantum geometry]] $(X,L_\omega)$, then the K-theoretic quantization of def. \ref{KTheoreticQuantization} coincides with the Dolbeault-Dirac quantization of def. \ref{DolbeaultDiracSpacesOfStates} and hence, by remark \ref{DolbeaultDiracAgreesWithEuler}, with the Euler-characteristic definition, def. \ref{EulerQuantumStates}, so that all the respectives [[spaces of quantum states]] agree:

$$
  \left(\left(X,\omega\right) \; Kaehler\right)
  \;\Rightarrow\;
  \left(
  \mathcal{H}_K 
   \simeq 
  \mathcal{H}_{DolbDirac} 
   \simeq 
  \mathcal{H}_{Euler}
  \right)
  \,.
$$

=--

This is to some extent discussed for instance in ([Hochs 08, lemma 3.32](#Hochs08), [Paradan 09, prop. 2.2](#Paradan09)).

+-- {: .proof}
###### Proof

Let $\sqrt{\Omega^{n,0}}$ be a choice of [[square root]] ([[Theta characteristic]]) of the [[canonical line bundle]], which according to \ref{SpinStructuresOnKaehlerManifolds} is a choice of [[spin structure]] in the [[Kähler manifold]]. Then by that same proposition the corresponding [[spinor bundle]] is [[isomorphism|isomorphic]] to 

$$
  S \simeq \Omega^{0,\bullet} \otimes \sqrt{\Omega^{n,0}}
$$

and so the corresponding $L_\omega$-twisted spinor bundle is

$$
  \begin{aligned}
   S \otimes L_\omega & \simeq
   \left(\Omega^{0,\bullet} \otimes \sqrt{\Omega^{n,0}}\right)
    \otimes L_\omega
    \\
    & \simeq
   \Omega^{0,\bullet} \otimes \left(\sqrt{\Omega^{n,0}}
    \otimes L_\omega\right)
  \end{aligned}
  \,,
$$

where we have re-bracheted just for emphasis of how the [[metaplectic correction]] appears as part of the [[spinor bundle]].

At the same time, by remark \ref{SpinCSpinorsAsTensorProductWhenDetDivisible} we have that under this assumption that an actual spin structure exists, the $Spin^c$-[[spinor bundle]] is isomorphic to 

$$
  S^c \simeq S \otimes L_\omega
  \,.
$$

So the two spinor bundles agree. It is now sufficient to observe that under this identification both the [[Dolbeault-Dirac operator]] as well as the [[spin^c Dirac operator]] have the same [[symbol of a differential operator|symbol]] to conclude that they have the same [[index]].


=--

+-- {: .num_remark}
###### Remark

The assumption in the above that we do have a [[spin structure]] is only for comparison with the Euler-/ Dolbeault-quantization. It is not necessary for the K-theoretic geometric quantization by [[spin^c structure]]. 

In the general case the [[determinant line bundle]] of the [[spin^c structure]] may not admit a square root. (Its failure of having a square root will be compensated precisely by the failure of there being a genuine [[spin structure]].) Still, by the above discussion the [[index]] of the corresponding [[spin^c structure]] is like a quantization of a would-be square root of the determinant line bundle in this case.  

=--


#### Quantum operators / observables
 {#QuantumOperators}


Given a [[Hamiltonian action]] on the [[symplectic manifold]] by a [[Lie group]] $G$, we can apply the above [[geometric quantization by push-forward|K-theoretic quantization by push-foward]] in $G$-[[equivariant K-theory]], to 

$$
  K_G(\ast) \simeq K(\ast//G) \simeq R(G)
$$ 

This is the [[representation ring]] of $G$ and hence yields not just a [[Hilbert space]], but a Hilbert space equipped with a $G$-[[action]]. This is the action by [[quantum operators]], quantizing the $G$-actions. Generalized orientation theory give the necessary condition for this quantization to exist: $X$ needs to be oriented not just in [[K-theory]] ([[spin^c structure]]) but in $G$-[[equivariant K-theory]] (equivariant [[spin^c structure]]).

So the geometric quantization of observables is essentially what mathematically is known as [[Dirac induction]].


## Properties

### Functorial dependence on choices
 {#DependenceOnChoiceOfPolarization}

* [[Knizhnik-Zamolodchikov connection]]

* [[Hitchin connection]]

* L. Charles, _Semi-classical properties of geometric quantization with metaplectic correction_ ([arXiv:math/0602168](http://arxiv.org/abs/math/0602168))

Chapter 3 of

* Lauridsen, _Aspects of quantum mathematics  -- Hitchin connections and the AJ conjecture_, PhD thesis Aarhus 2010 ([pdf](http://pure.au.dk/portal/files/41741925/imf_phd_2010_mrl.pdf))
 {#Lauridsen10}


### Compatibility of quantization with symplectic reduction

On the relation between geometric quantization and [[symplectic reduction]]:

* [[Guillemin-Sternberg geometric quantization conjecture]]

### Characteristic central extensions

To a large extent geometric quantization is realized by [[central extension]] of various Lie groups arising in [[classical mechanics]]/[[symplectic geometry]].

[[!include geometric quantization extensions - table]]




## Examples


### Schrödinger representation
 {#ExamplesSchroedingerRepresentation}

We discuss how the standard [[Schrödinger representation]] of the 
[[canonical commutation relation]] $\{q,p\} = -1$ arises via geometric quantization:

Consider the [[Cartesian space]] $\mathbb{R}^2$ with canonical [[coordinate functions]] denoted $\{q,p\}$ and to be called the _[[canonical coordinate]]_ $q$ and its [[canonical momentum]] $p$ and equipped with the [[left invariant differential form|constant]] [[differential 2-form]] given in in (eq:CanonicalMomentumPresymplecticCurrent) by

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

a [[smooth function]] (an [[observable]]), we say that a _[[Hamiltonian vector field]]_ for it (as in def. \ref{HamiltonianForms}) is a [[tangent vector field]] $v_A$  whose contraction into the [[symplectic form]] (eq:R2SymplecticForm) is the [[de Rham differential]] of $A$:

$$
  \label{HamiltonianVectorFieldOnR2}
  \iota_{v_A} \omega = d A
  \,.
$$

Consider the [[foliation]] of this phase space by constant-$q$-slices

$$
  \label{ConstantqSlicesOnR2}
  \Lambda_q = \subset \mathbb{R}^2
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

### K&#228;hler manifolds

If the [[symplectic manifold]] $(X, \omega)$ happens to be also 
a [[Kähler manifold]] there are natural choices of prequantization:

* the [[prequantum line bundle]] is a [[holomorphic line bundle]] since its [[curvature]] is $\omega in T^*_{(1,1)}X$;

* a [[polarization]] is given by the anti-holomorphic tangent bundle $T^{0,1}X$;

* a polarized section is a [[holomorphic section]];

* the [[dimension]] of the [[space of states (in geometric quantization)]] is given by the [[Riemann-Roch theorem]], see ([Hitchin](#Hitchin)).

Applied to a [[symplectic vector space]] this yields the [[Bargmann-Fock representation]] of the [[Heisenberg group]]. 

### The 2-sphere
 {#ExampleThe2Sphere}

Consider the 2-[[sphere]] $S^2$ with its canonical round [[volume form]] as a [[symplectic manifold]]. This admits a [[complex manifold|complex structure]] $J$ such that the [[subgroup]] of the [[diffeomorphism group]] which preserves $J$ is the [[special orthogonal group]] $SO(3)$. The corresponding [[Kähler metric]] is a multiple of the standard round [[Riemannian metric]] on the 2-sphere. 

By the identification $B U(1) \simeq K(\mathbb{Z},2)$ the [[prequantum bundles]] $\mathcal{L}$ on $S^2$ are classified by $\mathbb{Z}$. 

The [[Hilbert space]] is 

$$
  \mathcal{H} = H^0(S^2, \mathcal{L})
  \,,
$$

the space of [[holomorphic sections]] of such a [[holomorphic line bundle]]. The [[universal covering space|universal cover]] $SU(2)$ of $SO(3)$ naturally acts on this Hilbert space. The canonical [[coordinate]] functions $x,y,z \colon S^2 \to \mathbb{R}$ naturally act on $\mathcal{H}$ and as such form a [[Lie algebra representation]] of the [[special orthogonal Lie algebra]]. 

A way to reduce the number of choices in this example of geometric quantization is to proceed by [[quantization via the A-model]], see ([Gukov-Witten 08, p. 6 onwards](#GulovWitten08)).

For more see _[[geometric quantization of the 2-sphere]]_.

### Tori
 {#ExamplesTori}

* G. G. Athanasiu, E. G. Floratos, [[Stam Nicolis]], _Holomorphic Quantization on the Torus and Finite Quantum Mechanics_ ([arXiv:hep-th/9509098](http://arxiv.org/abs/hep-th/9509098))

### Theta functions

See at _[[theta function]]_.

### Quantization of Chern-Simons theory

The [[geometric quantization]] of [[Chern-Simons theory]]
leads to invariants for 3-[[manifolds]].([Witten 89](#Witten)).

See at _[[quantization of Chern-Simons theory]]_ for more.

### Quantization of loop groups / of the WZW model

See at _[[quantization of loop groups]]_.

### Quantization in Gromov-Witten theory

Geometric quantization appears in [[Gromov-Witten theory]].
See ([Clader-Priddis-Shoemaker 13](#CladerPriddisShoemaker13)).

### Quantization of the bosonic string $\sigma$-model

For discussion of the geometric quantization of the 
[[bosonic string]] 2d [[sigma-model]] see at
_[string -- Symplectic geometry and geometric quantization](string#ReferencesSymplecticGeometryAndGeometricQuantization)_ . 

## Related concepts

* [[fiber bundles in physics]]

* [[prequantum geometry]]

* [[reductions deformations resolutions in physics]]

* [[Weinstein symplectic category]]

* [[prequantum field theory]]

  * [[prequantum circle n-bundle]]

* [[quantization]]

  * [[deformation quantization]]

  * **geometric quantization**, [[higher geometric quantization]]

    * [[geometric quantization of symplectic groupoids]] 
 
    * [[spin-c quantization]]
 
    * [[metaplectic quantization]]

    * [[geometric quantization of non-integral forms]]


  * [[path integral]]

  * [[semiclassical approximation]]

* [[Borel-Weil-Bott theorem]]

  * [[orbit method]]

  * [[Schubert calculus]]

[[!include Isbell duality - table]]

[[!include genera and partition functions - table]]

## References
 {#References}

### General
 {#ReferencesGeneral}

Original references include

* {#Souriau69} [[Jean-Marie Souriau]], _[Structure des systemes dynamiques](http://www.jmsouriau.com/structure_des_systemes_dynamiques.htm)_, Dunod, Paris (1970)

  Translated and reprinted as (see section V.18 for geometric quantization):

  [[Jean-Marie Souriau]], _Structure of dynamical systems - A symplectic view of physics_, Brikh&#228;user (1997) ([doi:10.1007/978-1-4612-0281-3](https://link.springer.com/book/10.1007/978-1-4612-0281-3))

* [[Bertram Kostant]], _Quantization and unitary representations_, in _Lectures in modern analysis and applications III_, Lecture Notes in Math. 170 (1970), Springer Verlag, 87&#8212;208

* {#Souriau74} [[Jean-Marie Souriau]], _Mod&#232;le de particule &#224; spin dans le champ &#233;lectromagn&#233;tique et gravitationnel_, Annales de l'I.H.P. Physique th&#233;orique, 20 no. 4 (1974), p. 315-364  ([numdam](http://www.numdam.org/item?id=AIHPA_1974__20_4_315_0))

* [[Bertram Kostant]], _On the definition of quantization_, in _G&#233;om&#233;trie Symplectique et Physique Math&#233;matique_, Colloques Intern. CNRS, vol. 237,
Paris (1975) 187&#8212;210

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Geometric Asymptotics_, Math. Surveys no. 14, Amer. Math. Soc. (1977) ([web](http://www.ams.org/online%5Fbks/surv14/))

* [[Alexandre Kirillov]], _Geometric quantization_ Dynamical systems &#8211; 4, Itogi Nauki i Tekhniki. Ser. Sovrem. Probl. Mat. Fund. Napr., 4, VINITI, Moscow, 1985, 141&#8211;176 ([web](http://mi.mathnet.ru/eng/intf35))

A fairly comprehensive textbook with modern developments is

* [[Nicholas Woodhouse]], _Geometric Quantization_, Oxford University Press (1997)
 {#Woodhouse}

Introductions and lecture notes include

* William Gordon Ritter, _Geometric Quantization_ ([arXiv:math-ph/0208008](http://arxiv.org/abs/math-ph/0208008))

* [[Matthias Blau]], _Symplectic geometry and geometric quantization_ ([[BlauGeometricQuantization.pdf:file]])
 {#Blau}

* [[Eugene Lerman]], _Geometric quantization; a crash course_ ([arXiv:1206.2334](http://arxiv.org/abs/1206.2334))
 {#Lerman}

Lecture notes with an emphasis on [[semiclassical states]] are in

* {#BatesWeinstein}Sean Bates, [[Alan Weinstein]], _[[Lectures on the geometry of quantization]]_, AMS 1997 ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))
 

A careful discussion of the polarization-step from prequantization to quantization is in 

* J. &Sacute;niatycki, _Wave functions relative to a real polarization_, Internat. J. Theoret. Phys., 14(4):277&#8211;288 (1975)

* J. &Sacute;niatycki, _Geometric Quantization and Quantum Mechanics_, volume 30 of Applied Mathematical Sciences. Springer-Verlag, New York (1980)

The special case of K&#228;hler quantization is discussed for instance in 

* {#Hitchin} [[Nigel Hitchin]], _Flat connections and geometric quantization_, Comm. Math. Phys. __131__ (1990), no. 2, 347&#8211;380.

and for almost K&#228;hler structure in

* {#BorthwickUribe96} David Borthwick, Alejandro Uribe, _Almost complex structures and geometric quantization_ ([arXiv:dg-ga/9608006](https://arxiv.org/abs/dg-ga/9608006))

Discussion with an emphasis of quantizing [[classical field theory]] on curved [[spacetime]] is in 

* [[Nicholas Woodhouse]], _Geometric quantization and quantum field theory in curved space-times_, Reports on Mathematical Physics __12__:1, (1977) 45&#8211;56

(For more on geometric quantization of quantum field theories see also at _[Quantization of multisymplectic geometry](multisymplectic+geometry#RefsonQuantization)_.)

Aspects at least of geometric prequantization are usefully discussed also in section II of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993)

Further reviews include

* A. Echeverria-Enriquez, M.C. Munoz-Lecanda, N. Roman-Roy, C. Victoria-Monge, _Mathematical Foundations of Geometric Quantization_ Extracta Math. 13 (1998) 135-238 ([arXiv:math-ph/9904008](http://arxiv.org/abs/math-ph/9904008))

* Nima Moshayedi, _Notes on Geometric Quantization_ ([arXiv:2010.15419](https://arxiv.org/abs/2010.15419))


The above "Overview" and "Basic Jargon" sections are taken from 

* [[John Baez]], _Geometric Quantization_ ([web](http://math.ucr.edu/home/baez/quantization.html))
 {#Baez}

Some useful talk notes include

* Eva Miranda, _From action-angle coordinates to geometric quantization and back_ (2011) ([pdf](http://fdis2011.uni-jena.de/Talks/Eva%20Miranda.pdf))

Discussion with an eye towards the [[philosophy of physics]] is in 

* [[Gabriel Catren]], _Towards a Group-Theoretical Interpretation of Mechanics_ ([PhilSci Archive](http://philsci-archive.pitt.edu/10116/))

### Holographic quantization

The geometric [[quantization via the A-model]] is discussed in 

* [[Sergei Gukov]], [[Edward Witten]], _Branes and Quantization_, Adv. Theor. Math. Phys. 13 (2009) 1&#8211;73, ([arXiv:0809.0305](http://arxiv.org/abs/0809.0305), [euclid](http://projecteuclid.org/euclid.atmp/1282054099))
 {#GukovWitten08}

See also the [[geometric quantization of symplectic groupoids]] below, around ([Hawkins](#Hawkins)).


### $Spin^{\mathbb{C}}$-Quantization

* [[Peter Hochs]], _Quantisation commutes with reduction for cocompact Hamiltonian group actions_ 2008 ([pdf](http://www.math.ru.nl/~landsman/ThesisPeterHochs.pdf))
 {#Hochs08}

* [[Paul-Emile Paradan]], _Spin-quantization commutes with reduction_, J. Symplectic Geom. Volume 10, Number 3 (2012), 389-422. ([arXiv:0911.1067](http://arxiv.org/abs/0911.1067), [Euclid](http://projecteuclid.org/euclid.jsg/1350392491))
 {#Paradan09}



See the references at _[[geometric quantization by push-forward]]_.

### Examples

The basic example of geometric quantization of a [[symplectic vector space]] is discussed in pretty much every text on the matter for instance [Nohara, starting with example 2.6](#Nohara).

Discussion of geometric quantization of [[Chern-Simons theory]] is for instance in 

* [[Edward Witten]] (lecture notes by Lisa Jeffrey), _New results in Chern-Simons theory_, pages 81 onwards  in: S. Donaldson, C. Thomas (eds.) _Geometry of low dimensional manifolds 2: Symplectic manifolds and Jones-Witten theory_ (1989) ([pdf](http://cs5538.userapi.com/u11728334/docs/06f79688de6f/S_K_Donaldson_Geometry_of_LowDimensional_Ma.pdf))
 {#Witten}

* Scott Axelrod, Steve Della Pietra, and [[Edward Witten]], _Geometric quantization of Chern-Simons gauge theory_,  J. Differential Geom. Volume 33, Number 3 (1991), 787-902. ([EUCLID](http://projecteuclid.org/euclid.jdg/1214446565))

Discussion of geometric quantization of [[abelian varieties]], [[toric varieties]], [[flag varieties]] and its relation to [[theta functions]] is in 

* Yuichi Nohara, _Independence of polarization in geometric quantization_ ([pdf](http://geoquant.mi.ras.ru/nohara.pdf))
 {#Nohara}
* [[Andrei Tyurin]], _Quantization, classical and quantum field theory and theta functions_ ([arXiv:math/0210466v1](http://arxiv.org/abs/math/0210466v1))
 {#Tyurin}
* N.J. Hitchin, _Flat connections and geometric quantization_, Comm. Math. Phys. __131__, n 2 (1990), 347-380, [euclid](http://projecteuclid.org/euclid.cmp/1104200841)

An appearance of geometric quantization in [[mirror symmetry]] is pointed out in 

* Andrei Tyurin, _Geometric quantization and mirror symmetry_,
([math.AG/9902027](http://arxiv.org/abs/math/9902027))

For discussion of the geometric quantization of the 
[[bosonic string]] 2d [[sigma-model]] see at
_[string -- Symplectic geometry and geometric quantization](string#ReferencesSymplecticGeometryAndGeometricQuantization)_.

Discussion of geometric quantization of [[self-dual higher gauge theory]] is in 

* Samuel Monnier, _Geometric quantization and the metric dependence of the self-dual field theory_ ([arXiv:1011.5890](http://arxiv.org/abs/1011.5890))

Discussion in the context of [[Gromov-Witten theory]]:

* Emily Clader, Nathan Priddis, Mark Shoemaker, _Geometric Quantization with Applications to Gromov-Witten Theory_ ([arXiv:1309.1150](http://arxiv.org/abs/1309.1150))
 {#CladerPriddisShoemaker13}

### Relation to deformation quantization
 {#ReferencesRelationToDeformation}

Discussion of the relation of geometric quantization to [[deformation quantization]] is in 

* [[Eli Hawkins]], _The Correspondence between Geometric Quantization and Formal Deformation Quantization_ ([arXiv:math/9811049](http://arxiv.org/abs/math/9811049))

based on

* [[Eli Hawkins]], _Geometric Quantization of Vector Bundles_ ([arXiv:math/9808116](http://arxiv.org/abs/math/9808116))

See also

* Christoph N&#246;lle, _Geometric and deformation quantization_ ([arXiv:0903.5336](http://arxiv.org/abs/0903.5336))

For a basic comparative review of both see also section 1 of 

* [[Sergei Gukov]], [[Edward Witten]], _Branes and Quantization_, Adv. Theor. Math. Phys. 13 (2009) 1&#8211;73, ([arXiv:0809.0305](http://arxiv.org/abs/0809.0305), [euclid](http://projecteuclid.org/euclid.atmp/1282054099))
 {#GukovWitten08}

(which then develops geometric [[quantization via the A-model]]).

### Relation to path integral quantization

Relation to [[path integral quantization]] is discussed in

* Laurent Charles, _Feynman path integral and Toeplitz Quantization_ ([pdf](http://ipht.cea.fr/DocsphtV2/articles/t98/093/public/publi.pdf))


### Geometric BRST quantization
 {#ReferencesBRST}

The [[Lie algebroid]] version of an [[action groupoid]] is given (dually) by a [[BRST complex]]. Quantization over a BRST complex is hence quantization over an infinitesimal action groupoid. (See at [[higher geometric quantization]]).

Geometric quantization over BRST complexes is discussed in the following articles.

* [[Takashi Kimura]], _BRST Quantization and Poisson Reduction_, PhD Thesis (1990) ([web](http://adsabs.harvard.edu/abs/1990PhDT.......142K))

* [[José Figueroa-O'Farrill]], [[Takashi Kimura]], _Geometric BRST quantization_ ([pdf](http://www.maths.ed.ac.uk/~jmf/Research/PVBLICATIONS/gq.pdf))

  _Geometric BRST quantization. I. Prequantization_, Comm. Math. Phys. Volume 136, Number 2 (1991), 209-229. ([Euclid](http://projecteuclid.org/euclid.cmp/1104202348))


* [[Gijs Tuynman]], _Geometric quantization of the BRST charge_ Comm. Math. Phys. Volume 150, Number 2 (1992), 237-265. ([Euclid](http://projecteuclid.org/euclid.cmp/1104251864), [pdf](http://math.univ-lille1.fr/~gmt/PaperFolder/GQofBRST.pdf))

* [[Ronald Fulp]], _BRST Extension of Geometric Quantization_, Foundations of Physics Volume 37, Number 1 (2007),  ([arXiv:math/0604270](http://arxiv.org/abs/math/0604270))

### Supergeometric version
 {#ReferencesSupergeometric}

One can consider geometric quantization in [[supergeometry]].

* S.-M. Fei, H. -Y. Guo und Y. Yu, _Symplectic geometry and geometric quantization on supermanifold with $U$ numbers_, Z. Phys, C - Particles and Fields 45, 339-344 (1989)

* Gijs M. Tuynman, _Super Symplectic Geometry and Prequantization_ (2003) ([arXiv:math-ph/0306049](http://arxiv.org/abs/math-ph/0306049))

### Of presymplectic manifolds

Discussion of quantization of [[presymplectic manifolds]] is in 

* C. G&#252;nther, _Presymplectic manifolds and the quantization of relativistic particles_, Salamanca 1979, Proceedings, Differential Geometrical Methods In Mathematical Physics*, 383-400 (1979)

* Izu Vaisman, _Geometric quantization on presymplectic manifolds_,  Monatshefte f&#252;r Mathematik, vol. 96, no. 4, pp. 293-310, 1983

* [[Ana Canas da Silva]], [[Yael Karshon]], Susan Tolman, _Quantization of Presymplectic Manifolds and Circle Actions_ ([arXiv:dg-ga/9705008](http://arxiv.org/abs/dg-ga/9705008))

### Of generalized complex manifolds

Discussion in [[generalized complex geometry]] is in

* [[Alan Weinstein]], [[Marco Zambon]], _Variations on Prequantization_ ([arXiv:math/0412502](http://arxiv.org/abs/math/0412502))

* Alexander Cardona, _Geometric quantization of generalized complex manifolds_ ([pdf](http://pentagono.uniandes.edu.co/~acardona/GQGCM.pdf))

### In higher differential geometry

Geometric quantization in or with tools of [[higher differential geometry]], notably with/over [[Lie groupoids]] is discussed in the following references.


* {#Bos} [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) [pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf)
 
The [[geometric quantization of symplectic groupoids]] is accomplished in

* {#Hawkins} [[Eli Hawkins]], _A groupoid approach to quantization_, J. Symplectic Geom.. 6:61&#8211;125, [arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363)

* {#Nuiten13} [[Joost Nuiten]], section 5.2.2 of _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_, MSc thesis, August 2013


Discussion of geometric prequantization in fully fledged [[higher geometry]] is in 

* {#FiorenzaRogersSchreiber13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]],  _[[schreiber:Higher geometric prequantum theory|Higher U(1)-gerbe connections in geometric prequantization]]_, Reviews in Mathematical Physics, Volume 28, Issue 06, July 2016 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FiorenzaRogersSchreiber13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]]  _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107  142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

[[!redirects geometric prequantization]]

[[!redirects geometric quantizations]]