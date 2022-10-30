
> this page is going to contain one chapter of _[[geometry of physics]]_

> previous chapters: _[[geometry of physics -- differential forms|differential forms]]_, _[[geometry of physics -- smooth homotopy types]]_


***

#Contents#
* table of contents
{:toc}

## Integration

By the discussion in _[Differential forms](#DifferentialForms)_ and _[Principal connections](#PrincipalConnections)_, [[differential forms]] and more generally [[connection on a bundle|connections]] may be regarded as [[infinitesimal space|infinitesimal]] [[measures]] of _change_, of _displacement_. The discussion in _[Differentiation](#Differentiation)_ showed how to extract from a _finite_ but [[cohesion|cohesive]] (e.g. smoothly continuous) displacement all its infinitesimal measures of displacements by [[differentiation]]. 

Here we discuss the reverse operation: _[[integration]]_ is a construction from a [[differential form]] of the corresponding finite cohesive displacement. More generally this applies to any [[connection on a bundle|connection]] and is then called the _[[nLab:parallel transport]]_ of the connection, a term again referring to the idea that a finite displacement proceeds pointwise in parallel to a given infinitesimal displacement.

Under good conditions this construction can proceed literally by "adding up all the infinitesimal contributions" and therefore [[integration]] is traditionally thought of as a generalization of forming [[sums]]. Therefore one has the notation "$\int_{\Sigma} \omega$"
for the [[integral]] of a [[differential form]] $\omega$ over a space $\Sigma$, as a variant of the notation "$\sum_{S} f$" for the [[sum]] of values of a [[function]] on a [[set]] $S$. For the case of integrals of connections the corresponding parallel transport expression is often denoted by an exponentiated integral sign "$\mathcal{P} \exp(\int_\Sigma \omega)$", referring to the fact that the passage from infinitesimal to finite quantities involves also the passage from [[Lie algebra]] data to [[Lie group]] data ("[[Lie integration|exponentiated Lie algebra data]]"). 

However, both from the point of view of [[gauge theory]] [[physics]] as well as from the [[general abstract]] perspective of [[cohesive homotopy type theory]] another characterization of integration is more fundamental: the [[integral]] $\int_\Sigma \omega$ of a [[differential form]] $\omega$ (or more generally of a [[circle n-bundle with connection|connection]]) is an [[invariant]] under those [[gauge transformations]] of $\omega$ that are trivial on the [[boundary]] of $\Sigma$, and it is the _[[universal construction|universal]]_ such invariant, hence is uniquely characterized by this property.

In traditional accounts this fact is referred to via the _[[Stokes theorem]]_ and its generalizations (such as the [[nonabelian Stokes theorem]]), which says that the [[integral]]/[[parallel transport]] is indeed _[[invariant]]_ under gauge transformations of differential forms/connections. That this invariance actually characterizes the integral and the parallel transport is rarely highlighted in traditional texts, but it is implicit for instance in the old "path method" of [[Lie integration]] (discussed below in _[Lie integration](#LieIntegration)_) as well as in the famous characterization of [[flat connections]], discussed above in _[Flat 1-connections](#Flat1Connections)_: 

for $X$ a [[connected topological space|connected]] [[manifold]] and for $G$ a [[Lie group]], the operation of sending a [[flat connection|flat]] $G$-[[principal connection]] $\nabla$ to its [[parallel transport]] $\gamma \mapsto hol_{\gamma}(\nabla)$ around [[loops]] $\gamma\colon S^1 \to X$, hence to the [[integral]] of the connection around all possible loops (its [[holonomy]]),  for any fixed basepoint

$$
  hol \coloneqq \mathcal{P} \exp(\int_{(-)} (-)) 
  \;\colon\; 
  H^1_{conn, flat}(X,G) 
   \stackrel{\simeq}{\to} 
  Hom_{Grp}(\pi_1(X) , G)/G
$$

exhibits a [[bijection]] between gauge  [[equivalence classes]] of connections and [[group]] homomorphisms from the [[fundamental group]] $\pi_1(X)$ of $X$ to the [[gauge group]] $G$ (modulo [[adjoint action|adjoint]] $G$-action from gauge transformations at the base point, hence at the integration boundary). This is traditionally regarded as a property of the definition of the [[parallel transport]] $\mathcal{P} \exp(\int_{(-)}(-))$ by [[integration]]. But being a [[bijection]], we may read this fact the other way round: it says that forming equivalence classes of flat $G$-connections is a way of computing their [[integral]]/[[parallel transport]]. 

We saw a generalization of this fact to non-closed forms and non-flat connections already in the discussion at _[Differential 1-forms as smooth incremental path measures](##1FormsAsSmoothFunctors)_, where gauge equivalence classes of differential forms are shown to be equivalently assignments of [[parallel transport]] to [[path groupoid|smooth paths]].

This is also implied by the above discussion: for $\nabla \in H^1_{conn}(X,G) $ any non-flat connection and $\gamma \colon S^1 \to X$ a trajectory in $X$, we may form the [[pullback of differential forms|pullback]] of $\nabla$ to $S^1$. There it becomes a necessarily flat connection $\gamma^* \nabla \in H^1_{conn, flat}(S^1,G)$, since the [[curvature]] [[differential 2-form]] necessarily vanishes on the 1-[[dimension|dimensional]] [[manifold]] $S^1$. Accordingly, by the above bijection, forming the gauge [[equivalence class]] of $\gamma^* \nabla$ means to find a group homomorphism

$$
  \mathbb{Z} \simeq \pi_1(S^1) \to G
$$  

modulo conjugation (modulo nothing if $G$ is [[abelian group|abelian]], such as $G = U(1)$) and since $\mathbb{Z}$ is the [[free group]] on a single generator this is the same as finding an element 

$$
  hol_\gamma(\nabla)
  = 
  \mathcal{P} \exp(\int_\gamma \gamma^*\nabla)
  \in 
  G
  \,.
$$

This total operation of first pulling back the connection and then forming its [[integration]] (by taking gauge equivalence classes) is called the _[[transgression]]_ of the original 1-form connection on $X$ to a 0-form connection on the [[loop space]] $[S^1,X]$.

Below in the [Model Layer](#IntegrationModelLayer) we discuss the classical examples of [[integration]]/[[parallel transport]] and their various generalizations in detail. Then in the [Semantic Layer](#IntegrationSemanticLayer) we show how indeed all these constructions are obtained forming [[equivalence classes]] in the [[(∞,1)-topos]] of [[smooth ∞-groupoids|smooth homotopy types]], hence by _[[truncated object in an (∞,1)-category|truncation]]_ (followed, to obtain the correct cohesive structure, by _concretification_, def. \ref{ConcreteObjectsAndConcretification}). 





 
### Model Layer
 {#IntegrationModelLayer}

#### Integration

##### Integration over a coordinate patch

For $n \in \mathbb{N}$ let

$$
  C^n 
  \coloneqq
  \{
    \vec x \in \mathbb{R}^n
    |
    \forall_i (0 \leq x_i \leq 1)
  \}
  \hookrightarrow
  \mathbb{R}^n
$$

be the standard unit [[cube]]. 

Let 

$$
  \omega \in \Omega^n(\mathbb{R}^n)
$$

be a [[differential n-form]]. 

$$
  \omega = f \mathbf{d} x^1 \wedge \mathbf{d} x^2 \wedge \cdots \wedge \mathbf{d} x^n
  \,.
$$


Let $Partitions(C^k)$ be the [[poset]] whose elements are partitions of the unit $n$cube $C^n$ into $N^n$ subcubes, for $N \in \mathbb{N}$, ordered by inclusion. 

Let 

$$
  \sum_{(-)} \omega
  \colon
  Partitions(C^k)
  \to 
  \mathbb{R}
$$

be the function that sends

$$
  \frac{1}{N^n}
  \sum_{x^1 = 0}^N
  \sum_{x^2 = 0}^N
  \cdots
  \sum_{k^n = 0}^N
  f( x^1, \cdots, x^n )
  \,.
$$

Then 

$$
  \int_{C^k} \omega \colon \lim_{N} \sum_N \omega
  \,. 
$$

##### Integration of differential forms over a manifold
 {#IntegrationOfDifferentialFormsOverASmoothManifold}

Let $\Sigma$ be a [[closed manifold|closed]] [[orientation|oriented]] [[smooth manifold]] of [[dimension]] $k$

+-- {: .num_defn #IntegrationOfDifferentialFormsInTermsOfSmoothModuli}
###### Definition

For $n \in \mathbb{N}$, $n \geq k$, define the 
morphism of [[smooth spaces]]

$$
  \int_{\Sigma} \colon [\Sigma, \Omega^n] \to \Omega^{n-k}
$$

by declaring that over a [[coordinate chart]] $U \in$ [[CartSp]] 
it is the ordinary [[integration of differential forms]] over smooth manifolds

$$
  \int_{\Sigma, U} : \Omega^n(\Sigma\times U) \to \Omega^{n-k}(U)
  \,.
$$

=--

##### Integration in ordinary differential cohomology

* [[fiber integration in ordinary differential cohomology]]


#### Holonomy

##### Parallel transport

given $A \in \Omega^1(\Delta^1, \mathfrak{g})$

we say $f \in C^\infty(\Delta^1, G)$ is the [[parallel transport]] of $A$ if 

1. $f(0) = 1$

1. $f$ satisfies the [[differential equation]]

   $$
     \mathbf{d}f = A f
   $$

where on the right we have the differential of the left action of the group on itself.

In this case one writes

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} A \right)
  \coloneqq
  f(1) 
$$

and calls it the _[[path ordered integral]]_ of $A$. Here the enire left hand side is primitive notation.

In the case that $G = U(1)$ this reproduces the ordinary [[integral]]

$$
  \left(G = \mathbb{R}\right)
  \Righarrow
  \mathcal{P} \exp(\int_{\Delta^1} A)
  = 
  \exp(i \int_{\Delta^1} A)
  \in 
  U(1)
$$

There is another way to express this [[parallel transport]],
related to [[Lie integration]]:

Define an [[equivalence relation]] on $\Omega^1(\Delta^1, \mathfrak{g})$ as follows: two 1-forms $A,A'$ are taken to be equivalent if there is a flat 1-form $\hat A \in \Omega^1_{flat}(D^2, \mathfrak{g})$ on the 2-[[disk]] such that its restriction to the upper semicircle is $A$ and the restriction to the lower semicircle is $\tilde A$.

If $G$ is [[simply connected topological space|simply connected]], then the [[equivalence classes]] of this relation form

$$
  \Omega^1(\Delta^1,\mathfrak{g})_{/\sim} \simeq
  G
$$

and the [[quotient]] map coincides with the [[parallel transport]]

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} \left(-\right)\right)
  \colon
  \Omega^1(\Delta^1, \mathfrak{g})
  \to 
  \Omega^1(\Delta^1, \mathfrak{g})_{/\sim}
  \simeq
  G  
$$

Finally yet another perspective is this: consider the [[equivalence relation]] on $\Omega^1(\Delta^1, \mathfrak{g})$ where two 1-forms are regarded as equivalent if there is a [[gauge transformation]] $\lambda \in C^\infty(\Delta^1, G)$ with $\lambda(0) = e$ and $\lambda(1) = e$, then again 

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} \left(-\right)\right)
  \colon
  \Omega^1(\Delta^1, \mathfrak{g})
  \to 
  \Omega^1(\Delta^1, \mathfrak{g})_{/\sim}
  \simeq
  G  
$$

is the parallel transport


##### Holonomy of a flat principal connection

if $X$ is connected then forming the [[holonomy]] of flat $G$-connections

$$ 
  hol
  \colon
  G Bund_{\nabla, flat}(X)
  \stackrel{\simeq}{\to}
  Hom_{Grp}(\pi_1(X), G)
$$

is an [[equivalence]], $\pi_1(X)$ the [[fundamental group]]. If $X$ is not connected then 

$$ 
  hol
  \colon
  G Bund_{\nabla, flat}(X)
  \stackrel{\simeq}{\to}
  Hom_{Grpd}(\Pi_1(X), \mathbf{B}G)
$$

is an equivalence.


#### Transgression
 {#Transgression}

What is called _[[transgression]]_ is the combination of 

1. passing a [[cocycle]] on some space $X$ with [[coefficients]] in some $A$ to a [[cocycle]] on a [[mapping space]] $[\Sigma,X]$ with coefficients in $[\Sigma,A]$ and 

1. [[integration|integrating]] the resulting coefficient over $\Sigma$ to obtain a $B$-valued cocycle on the mapping space, where $B$ is some recipient of an integration map of $A$-cocycles over $\Sigma$.

##### Transgression of differential forms
 {#TransgressionOfDifferentialForms}

Let $\Sigma_k$ be a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $k$.

+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}$, the **[[transgression]] of [[differential forms]]** on $X$ to the [[mapping space]] $[\Sigma,X]$ is the morphism

$$
  \int_\Sigma [\Sigma,-]
  : 
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

given on a differential form

$$
  (X \stackrel{\omega}{\to} \Omega^n) \in \Omega^n(X)
$$

as the [[composition]] of the [[mapping space]] operation with the [[integration of differential forms]], def. \ref{IntegrationOfDifferentialFormsInTermsOfSmoothModuli}:

$$
  \int_{\Sigma} [\Sigma,\omega]
   \;\colon\;
  [\Sigma, X] 
    \stackrel{[\Sigma, \omega]}{\to}  
  [\Sigma, \Omega^n]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^{n-k}
  \,.
$$

=--

We discuss some examples and applications:

* [Gauge coupling action functional of charged particle](#GaugeCouplingActionFunctionalOfChargedParticle)

* [Transgression of Killing form to symplectic form of Chern-Simons theory](#TransgressionOfKillingFormToSymplecticFormOfChernSimons)

###### Gauge coupling action functional of charged particle
 {#GaugeCouplingActionFunctionalOfChargedParticle}

Let $X \in \mathbf{H}$ and consider a [[circle group]]-[[principal connection]] $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ over $X$. By the discussion in _[Dirac charge quantization and the electromagnetic field](#DiracChargeQuantizationAndElectromagneticField)_ above this encodes an [[elecrtromagnetic field]] on $X$. Assume for simplicity here that the underlying [[circle principal bundle]] is trivialized, so that then the connection is equivalently given by a differential 1-form

$$
  \nabla = A \colon X \to \Omega^1
  \,,
$$

the [[electromagnetic potential]].

Let then $\Sigma = S^1$ be the [[circle]].  The [[transgression]] of the electromagnetic potential to the [[loop space]] of $X$ 

$$
  \int_{S^1} [S^1, A]
   \;\colon\;
  [S^1, X]
    \stackrel{[S^1, A]}{\to}
  [S^1 , \Omega^1]
    \stackrel{\int_{S^1}}{\to}
  \Omega^0
  \simeq
  \mathbb{R}
$$

is the [[action functional]] for an [[electron]] or other electrically charged [[particle]] in the [[background gauge field]] $A$ is $S_{em} = \int_{S^1} [S^1, A]$.

The [[variational calculus|variation]] of this contribution in addition to that of the [[kinetic action]]  of the electron gives the _[[Lorentz force]]_ law describing the [[force]] exerted by the [[background gauge field]] on the electron.

###### Transgression of Killing form to symplectic form of Chern-Simons theory
 {#TransgressionOfKillingFormToSymplecticFormOfChernSimons}

Let $\mathfrak{g}$ be a [[Lie algebra]] with 
binary [[invariant polynomial]] 
$\langle -,-\rangle \colon \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$.

For instance $\mathfrak{g}$ could be a [[semisimple Lie algebra]] and $\langle -,-\rangle$ its [[Killing form]]. In particular if $\mathfrak{g} = \mathfrak{su}(n)$ is a [[matrix Lie algebra]] such as the [[special unitary Lie algebra]], then the Killing form is given by the [[trace]] of the product of two matrices.

This pairing $\langle -,-\rangle$ defines a differential 4-form on the [[smooth space]] of [[Lie algebra valued 1-forms]]

$$
  \langle F_{(-)} \wedge F_{(-)} \rangle
  \colon
  \Omega^1(-,\mathfrak{g})
   \stackrel{F_{(-)}}{\to}
  \Omega^2(-, \mathfrak{g})
   \stackrel{(-)\wedge (-)}{\to}
  \Omega^4(-, \mathfrak{g}\otimes \mathfrak{g})
   \stackrel{\langle-,-\rangle}{\to}
  \Omega^4
$$

Over a [[coordinate patch]] $U \in $ [[CartSp]] this sends a differential 1-form $A \in \Omega^1(U)$ to the differential 4-form

$$
  \langle F_A \wedge F_A \rangle \in \Omega^4(U)
  \,.
$$

The fact that $\langle -, - \rangle$ is indeed an _[[invariant polynomial]]_ means that this indeed extends to a 4-form on the smooth [[groupoid of Lie algebra valued forms]]

$$
  \langle F_{(-)} \wedge F_{(-)}\rangle
  \colon
  \mathbf{B}G_{conn}
  \to 
  \Omega^4
  \,.
$$

Now let $\Sigma$ be an [[orientation|oriented]] [[closed manifold|closed]] [[smooth manifold]].  The [[transgression]] of the above 4-form to the [[mapping space]] out of $\Sigma$ yields the 2-form

$$
  \omega
    \coloneqq
  \int_{\Sigma} \langle F_{(-)}\wedge F_{(-)}\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma,\mathfrak{g})
   \hookrightarrow
  [\Sigma, \mathbf{B}G_{conn}]
    \stackrel{[\Sigma, \langle F_{(-)}\wedge F_{(-)}\rangle]}{\to}
  [\Sigma, \Omega^4]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^2
$$

to the [[moduli stack]] of [[Lie algebra valued 1-forms]] on $\Sigma$.

Over a [[coordinate chart]] $U = \mathbb{R}^n \in $ [[CartSp]] an element $A \in \mathbf{\Omega}^1(\Sigma,\mathfrak{g})(\mathbb{R}^n)$ is a $\mathfrak{g}$-valued 1-form $A$ on $\Sigma \times U$ with no leg along $U$. Its [[curvature]] 2-form therefore decomposes as

$$
  F_A = F_A^{\Sigma} + \delta A
  \,,
$$

where $F_A^{\Sigma} $ is the curvature component with all legs along $\Sigma$ and where

$$
  \delta A
  \coloneqq 
  - \sum_{i = 1}^n \frac{\partial}{\partial x^i} A \wedge \mathbf{d}x^i
$$

is the [[variational calculus|variational]] derivative of $A$.

This means that in the 4-form

$$
  \langle F_A \wedge F_A\rangle
  = 
  \langle F_A^\Sigma \wedge F_A^\Sigma \rangle
  + 
  2 \langle F_A^\Sigma \wedge \delta A\rangle 
  + 
  \langle \delta A \wedge \delta A\rangle 
  \in
  \Omega^4(\Sigma \times U)
$$

only the last term gives a 2-form contribution on $U$. Hence we find that the transgressed 2-form is

$$
  \omega = \int_\Sigma \langle \delta A \wedge \delta A\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma, \mathfrak{g})
   \to
  \Omega^2
  \,.
$$

When restricted further to flat forms

$$
  \mathbf{\Omega^1}_{flat}(\Sigma,\mathfrak{g})
  \hookrightarrow
  \mathbf{\Omega^1}(\Sigma,\mathfrak{g})  
$$

which is the [[phase space]] of $\mathfrak{g}$-[[Chern-Simons theory]], then this is the corresponding [[symplectic form]] (by the discussion at _[Chern-Simons theory -- covariant phase space](Chern-Simons theory#CovariantPhaseSpace)_).




##### Transgression of circle $n$-bundles with connection


* [[fiber integration in ordinary differential cohomology]]

##### Action functionals from transgression

(...)

#### Lie integration
 {#LieIntegration}

* [[Lie integration]]


### Semantic Layer
 {#IntegrationSemanticLayer}

#### Integration and higher holonomy

[[integration]]/[[higher holonomy]] is

$$
  \exp(2 \pi i \int_{\Sigma}(-))
  \colon
  [\Sigma_n, \mathbf{B}^n U(1)_{conn}]
  \to
  Conc \tau_0 [\Sigma, \mathbf{B}^n U(1)]
  \simeq
  U(1)
$$

#### Transgression

[[transgression]] is 

$$
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi i \int_{\Sigma_k}) (-) }{\to}
  \mathbf{B}^{n-k} U(1)_{conn}
$$

#### Action functionals from Lagrangeans
 {#SemLayerActionFunctionalsFromLagrangeans}

and [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons]] [[action functionals]] induced from

$$
  \mathbf{L} \colon \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}
$$

are

$$
  \exp\left(i S\left(-\right)\right)
  \coloneqq
  \exp(2 \pi \in \int_{\Sigma_k} [\Sigma_k, \mathbf{L}] )
  \colon
  [\Sigma_k, \mathbf{B}G]
  \stackrle{[\Sigma_k, \mathbf{L}]}{\to}
  [\Sigma_k, \mathbf{B}^n U(1)]
  \stackrel{\exp(2 \pi i\left(-\right))}{\to}
  \mathbf{B}^{n-k} U(1)_{conn}
$$


here $\mathbf{L}$ is the [[Lagrangean]].

### Syntactic Layer

(...)

