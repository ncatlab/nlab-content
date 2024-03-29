
> This entry contains one chapter of the material at _[[geometry of physics]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## **Differentiation**
 {#Differentiation}


So far we have dealt with _cohesive_ structures for which there is a notion of _smooth variation_, say of the position of a [[particle]] along a [[trajectory]] in [[spacetime]]. The idea of _differentiation_ is to measure the _[[difference]]_ between the position of two points on a cohesive trajectory in space as the difference between their [[worldline]] coordinates "tends to 0" without actually becoming 0. One also says that differentiation is forming "[[infinitesimal space|infinitesimal]] differences" of a cohesive process -- and we will make precise here what this means.

There are two stages to the theory of differentiation:

1. We may think of differentiation as just a means to analyze more in detail the [[cohesive topos|cohesive structure]] already given, without adding new [[structure]], hence without a priori refining our notion of what a "[[cohesion|cohesive]] [[trajectory]]" is. Indeed, given any [[line object]] $\mathbb{R}$ in a [[cohesive ∞-topos]], there is canonically a homomorphism of cohesive spaces

   $$
      \mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl}(-,\mathbb{R})
   $$

   from the line to the cohesive moduli space of closed [[differential 1-forms]], which is such that it sends a cohesive curve on the line to the differential form on this curve whose value at each point is the _differential_ of the curve, its rate of infinitesimal change at that point.

   Below in _[Differentiation of smooth functions and differetial forms](#DifferentiationOfSmoothFunctionsAndDifferentialForms)_ we discuss this construction in the standard model of [[smooth infinity-groupoid|smooth cohesion]] for [[smooth spaces]], where it reproduces what traditionally is called the _[[de Rham differential]]_ $\mathbf{d}$. 

   Further below in _[Maurer-Cartan forms -- Cohesive differentiation](#CohesiveDifferentiation)_ we show how $\mathbf{d}$ comes out from just the abstract axioms of cohesionn.

1. We may think of differentiation as reflecting a refinement of smooth cohesion such that [[infinitesimal space|infinitesimal]] cohesive trajectories actually exist. Here, on top of having a _measure_ for how a cohesive trajectory changes infinitesimally at a given point, it makes sense to ask concretely if two points on a trajectory are infinitesimally close to each other. In this approach the very notion of cohesion is refined to include _explicitly_ a way to speak not just about a "cohesive blob of points", but to decide whether it is in fact just an "infinitesimal cohesive blob of points" -- an _[[infinitesimally thickened point]]_.

   [[differential geometry|Differential geometry]] with such an explicit notion of [[infinitesimal space|infinitesimals]] is known as _[[synthetic differential geometry]]_: the [[axioms]] here allow one to _synthesize_ an [[infinitesimally thickened point]] and not just to reason about it _as if_ it existed. 

   In such a synthetic differential context then the differential $\mathbf{d}$ from above not just exists as a whole, but we can "take it apart and re-synthesize it" by realizing its value at each point literally as the ordinary [[difference]] between two _infinitesimally close_ points. Similarly, various other fundamental constructions in [[differential geometry]], such as that of [[tangent bundles]] and [[jet bundles]] have a usefully transparent axiomatic characterization in the presence of synthetic infinitesimals. ([[Sophus Lie]], one of the founding fathers of [[differential geometry]] [famously said](synthetic+differential+geometry#SophusLieQuote) that he indeed found his theorems using such synthetic reasoning intuitively, and just did not publish them this way due to a lack of formalization of this language -- at his time. ) This we discuss in the Mod Layer in _[D-geometry](#DGeometry)_ below.

In the [Differentiation semantic layer](#DifferentiationLayerSem) below we formalize differentiation, and these two aspects of it, by adding to the notion of _[[cohesive topos]]_ that of an _[[infinitesimal cohesion|infinitesimal cohesive neighbourhood]]_.

Recalling that a [[cohesive topos]] is an abstract _cohesive blob_, an infinitesimal cohesive neighbourhood is accordingly an infinitesimally thicked cohesive blob (which is itself again a cohesive blob):


$$
  \array{
    CohesiveBlob &&\hookrightarrow&& InfinitesimallyThickenedCohesiveBlob
    \\
    & \searrow && \swarrow
    \\
    && Point
  }
  \;\;\;\;\;\;\;\;
  \array{
    \mathbf{H} &&\stackrel{}{\hookrightarrow}&& \mathbf{H}_{th}
    \\
    & \searrow && \swarrow
    \\
    && DiscSpaces
  }
  \,.
$$

### Model Layer
 {#DifferentiationLayerMod}

We discuss 

* [Differentiation of smooth functions and differential forms](#DifferentiationOfSmoothFunctionsAndDifferentialForms)

  * first just _[on coordinate patches](#DifferentiationOnCoordinatePatches)_

  * and then _[on general smooth spaces](#DifferentiationOnSmoothSpaces)_.

By considering [[fiber products]] of smooth [[mapping spaces]] with [[discrete spaces]] of boundary configurations, we obtain from this the differentiation theory called 

* _[Variational calculus](#VariationalCalculus)_

  * with the notion of _[Smooth functional](#SmoothFunctionals)_

  * and _[Variational derivative](#FunctionalDerivative)_ of smooth functionals.

  * The central class of examples of this of interest in physics is the variation of [[action functionals]] that yields the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] in [[classical field theory]]. This we discuss in _[Euler-Lagrange equations](#EulerLagrangeEquations)_.

#### Differentiation of smooth functions and differential forms
 {#DifferentiationOfSmoothFunctionsAndDifferentialForms}

##### Differentiation on coordinate patches
 {#DifferentiationOnCoordinatePatches}

By definition to [[smooth function]] $f \colon \mathbb{R} \to \mathbb{R}$ is associated its [[derivative]], a smooth function $f' \colon \mathbb{R} \to \mathbb{R}$. And more generally to a smooth function $f \colon \mathbb{R}^n \to \mathbb{R}$ are associated its [[partial derivatives]], smooth functions

$$
  \frac{\partial f}{\partial x^i} \colon \mathbb{R}^n \to \mathbb{R}
$$

for $1 \leq i \leq n $.

The [[de Rham differential]] collects all partial derivatives of a function into a single [[differential 1-form]]

+-- {: .num_defn #DeRhamDifferentialOn1Forms}
###### Definition

For $n \in \mathbb{N}$,  The **[[de Rham differential]]** on [[smooth functions]] in $C^\infty(\mathbb{R}^n)$ is the [[function]]

$$
  \mathbf{d} \colon C^\infty(\mathbb{R}^n) \to \Omega^1(\mathbb{R}^n)
$$

which takes $f \in C^\infty(\mathbb{R}^n)$ to

$$
  \mathbf{d}f \coloneqq \sum_{i = 1}^n \frac{\partial f}{\partial x^i} \mathbf{d} x^i
  \,.
$$

=--

+-- {: .num_example}
###### Example

For $x^i \colon \mathbb{R}^n \to \mathbb{R}$ one of the [[coordinate]] functions, the de Rham differential $\mathbf{d} x^i$ indeed coincides with the basis element of the same name according to def. \ref{Differential1FormsOnCartesianSpaces}, using that 

$$
  \frac{\partial x^i}{\partial x^{j}} = 
  \left\{
    \array{
      1 & | i = j
      \\
      0 & | otherwise
    }
  \right.
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The de Rham differentials $\mathbf{d} \colon C^\infty(\mathbb{R}^n) \to \Omega^1(\mathbb{R}^n)$ for all $n \in \mathbb{N}$ are compatible with [[pullback of differential forms|pullback of differential 1-forms]], def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces}, in that for each coordinate transformation $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^{k}$ the [[diagram]]

$$
  \array{
     C^\infty(\mathbb{R}^k) 
      &\stackrel{\mathbf{d}}{\to}& 
    \Omega^1(\mathbb{R}^k)
     \\
     \downarrow^{\mathrlap{\phi^\ast}} && \downarrow^{\mathrlap{\phi^\ast}}
     \\
     C^\infty(\mathbb{R}^{\tilde k}) 
       &\stackrel{\mathbf{d}}{\to}&   
     \Omega^1(\mathbb{R}^{\tilde k})    
  }
$$

[[commuting diagram|commutes]].

=--

+-- {: .proof}
###### Proof

This is equivalently the statement of the _[[chain rule]]_ of [[differentiation]]: For any $f \in C^\infty(\mathbb{R}^k)$ we have on the one hand, by def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces} and def. \ref{DeRhamDifferentialOn1Forms}

$$
  \begin{aligned}
    \mathbf{d} \phi^\ast f
    & = 
    \mathbf{d} (f \circ \phi)
    \\
    & =
    \sum_{j = 1}^{\tilde k} \frac{\partial (f \circ \phi)}{\partial x^j}\mathbf{d} x^j
  \end{aligned}
$$

and on the other hand, applying the definition in the other order,

$$
  \begin{aligned}
    \phi^* \mathbf{d}f
    & = 
    \phi^* \sum_{i = 1}^k \frac{\partial f}{\partial x^i} \mathbf{d}x^i
    \\
    & = \sum_{i = 1}^k \sum_{j = 1}^{\tilde k} 
     \left(\frac{\partial f}{\partial x^i}\circ \phi \right)
    \cdot 
    \left(\frac{\partial \phi^i}{\partial x^j}\right) \mathbf{d}x^j
  \end{aligned}
  \,.
$$

Both expressions agree precisely if for all $j$ we have

$$
  \frac{\partial (f \circ \phi)}{\partial x^j}
   =
  \sum_{i = 1}^k \left(\frac{\partial f}{\partial x^i}\circ \phi\right) \cdot \left(\frac{\partial \phi^i}{\partial x^j}\right)
  \;\;\;
  \in 
  C^\infty(\mathbb{R}^{\tilde k})
  \,.
$$

This is precisely the statement of the _[[chain rule]]_ for [[differentiation]].

=--

Notice that as smooth spaces $\mathbb{R} = \Omega^0 = C^\infty(-)$, by prop.  \ref{SpaceOf0FormsIsRealLine}. Therefore the above says that

+-- {: .num_prop}
###### Proposition

The [[de Rham differential]], def. \ref{DeRhamDifferentialOn1Forms}, constitutes a homomorphism of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}

$$
  \mathbf{d} \colon \mathbb{R} \to \Omega^1
$$

from the [[real line]] to the universal smooth moduli space of differential 1-forms, def. \ref{SmoothModuliSpaceOfnForms}.

=--

+-- {: .num_remark}
###### Remark

Below in _[Maurer-Cartan form on a Lie group](#MaurerCartanFormOnLieGroup)_ we discuss a more general abstract origin of $\mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl}$.

=--

We now extend the de Rham differential to differential forms of higher degree.

+-- {: .num_defn #DeRhamDifferentialInGeneralDegreeOverCartesianSpaces}
###### Definition

For all $n \in \mathbb{N}$ let 

$$
  \mathbf{d} 
    \colon 
  \Omega^\bullet(\mathbb{R}^n)
   \to 
  \Omega^\bullet(\mathbb{R}^n)
$$

be the unique extension of $\mathbf{d} \colon C^\infty(-) \to \Omega^1(-)$ to a degree-1 [[derivation]] with 

$$
  \mathbf{d}\mathbf{d}x^i = 0
  \,.
$$


=--

(...)

+-- {: .num_prop #DeRhamDifferentialAsMorphismOfSmoothSpacesInEachDegree}
###### Proposition

For each $n \in \mathbb{N}$ the de Rham differential of def. \ref{DeRhamDifferentialInGeneralDegreeOverCartesianSpaces} constitutes a homomorphism of smooth spaces

$$
  \mathbf{d} \colon \Omega^n \to \Omega^{n+1}
$$

form the universal smooth moduli space of differental $n$-forms to that of differential $n+1$-forms.

=--

##### Differentiation on smooth spaces
 {#DifferentiationOnSmoothSpaces}

We now extend the notion of [[derivatives]] and [[de Rham differentials]] from [[smooth functions]] on [[Cartesian spaces]] to smooth functions on general [[smooth spaces]].

Recall from def. \ref{DifferentialnFormOnSmoothSpace} that the set of differential $n$-forms on a [[smooth space]] $X$ is $\Omega^n(X) \coloneqq Hom(X, \Omega^n)$. 

+-- {: .num_defn #DeRhamDifferentialOverSmoothSpaces}
###### Definition

For $X \in Smooth0Type$ a smooth space and $n \in \mathbb{N}$, the **[[de Rham differential]]** on $n$-forms over $X$ is the [[function]]

$$
  \mathbf{d} \colon \Omega^n(X) \to \Omega^{n+1}(X)
$$

which is the postcomposition with the homomorphism of smooth spaces of prop. \ref{DeRhamDifferentialAsMorphismOfSmoothSpacesInEachDegree}:
 
$$
  Hom(X,\mathbf{d}) \colon Hom(X,\Omega^n) \to Hom(X,\Omega^{n+1})
  \,.
$$

=--


In particular the [[derivative]] of a smooth function $f \colon X \to \mathbb{R}$ is the [[composition|composite]]

$$
  \mathbf{d}f \colon X \stackrel{f}{\to} \mathbb{R} \stackrel{\mathbf{d}}{\to} \Omega^1_{cl} \hookrightarrow \Omega^1
  \,.
$$

Below in _[Variation is differentiation on smooth spaces](#VariationIsDifferentiationOnSmoothSpaces)_ we find that this notion of differentiation of smooth functions on smooth spaces subsumes what traditionally is called _[[variational calculus]]_ of [[functionals]] on [[mapping spaces]].

##### Example: The electromagnetic field strength
 {#ElectromagneticFieldStrength}

for instance [[electromagnetic potential]]

$$
  A = \phi \mathbf{d}t + A_1 \mathbf{d}x^1 + A_2 \mathbf{d}x^2 + A_3 \mathbf{d}x^3
$$

then the [[electromagnetic field strength]] is

$$
  F 
    \coloneqq
  \mathbf{d}A 
    = 
   E_1 \mathbf{d}x^1 \wedge \mathbf{d}t 
    + 
   E_2 \mathbf{d}x^2 \wedge \mathbf{d}t 
    + 
   E_3 \mathbf{d}x^3 \wedge \mathbf{d}t
    + 
    B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3 
    + 
    B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1 
    + 
    B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2 
$$

with 

$$
  E_i = \frac{\partial \phi}{\partial x^i} - \frac{\partial A_i}{\partial t}
$$

and

$$
  B_1 = \frac{\partial A_2}{\partial x^3} - \frac{\partial A_3}{\partial x^2}
$$

etc


This are the first 2 of 4 [[Maxwell equations]]: $\mathbf{d} F = 0$

(the other 2 are discussed below in [Riemannian geometry](#RiemannianGeometry))

for

$$
  A,A' : X \to \Omega^1(-)
$$

a [[gauge transformation]] $A \to A'$
is $\lambda : X \to \mathbb{R}$ with

$$
  A' = A + \mathbf{d} \lambda
$$



#### Variational calculus
 {#VariationalCalculus}

Traditionally a _[[functional]]_ is a [[function]] which is sufficiently like a [[smooth function]], but defined not on a [[manifold]], but on a [[mapping space]] between manifolds. Also traditionally, a _[[variational derivative]]_ of such a functional is something aking to a [[derivative]], generalized to this context, and subject to the condition that all variations _preserve some boundary conditions_. 

We formulate this classical theory in the context of [[smooth spaces]]. Here a [[nonlinear functional|functional]] is simply a homomorphism of smooth spaces out of a smooth [[mapping space]], as in def. \ref{SmoothFunctionSpace}. We may impose _respect for boundary conditions_ by forming the [[fiber product]] of this mapping space with a _discrete smooth space inclusion_, given in def. \ref{MapFromDiscretizationOfSmooth0Type} below. Then the _variational derivative_ is simply the ordinary derivative of def. \ref{DeRhamDifferentialOverSmoothSpaces}.


##### Discrete points of a smooth space

+-- {: .num_defn #DiscretizationOfSmooth0Type}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], write

$$

  \Gamma X
  \coloneqq
  Hom(*,X)
  \in Set
$$

for its _set of points_, the set of homomorphisms, def. \ref{HomomorphismOfSmoothSpaces}, from the point to $X$. 

Write

$$
  \flat X \coloneqq Disc (\Gamma(X))
$$

for the discrete smooth space, def. \ref{DiscreteSmoothSpace}, on this set of points. 

=--

+-- {: .num_defn #MapFromDiscretizationOfSmooth0Type}
###### Definition

For every smooth space $X$ there is a canonical homomorphism of smooth spaces

$$
  \flat X \to X
  \,.
$$

This sends a plot $U \to \flat X$, which by definition of $Disc(-)$ is a point in $\Gamma X$, hence a homomorphism $x \colon * \to X$, to the plot $U \to * \stackrel{x}{\to} X$ of $X$.

=--


##### Smooth functionals
 {#SmoothFunctionals}

Let $X$ be a [[smooth manifold]].
Let $\Sigma$ be a [[smooth manifold|smooth]] [[manifold with boundary]] $\partial \Sigma \hookrightarrow \Sigma$. 

Write 

$$
  [\Sigma, X] \in Smooth0Type
$$

for the [[smooth space]] (a [[diffeological space]]) which is the [[mapping space]] from $\Sigma$ to $X$, hence such that for each $U \in $ [[CartSp]] we have

$$
  [\Sigma, X](U) = C^\infty(U \times \Sigma, X)
  \,.
$$


+-- {: .num_defn #MappingSpaceWithNonVaryingBoundary}
###### Definition

Write

$$
  [\Sigma, X]_{\partial \Sigma}
  \coloneqq
  [\Sigma, X] \times_{[\partial \Sigma,X]} \flat [\partial \Sigma,X]
$$

for the [[pullback]] in smooth spaces

$$
  \array{
    [\Sigma,X]_{\partial \Sigma}
    &\to&
    \flat [\partial \Sigma, X]
    \\
    \downarrow && \downarrow
    \\
    [\Sigma,X] &\stackrel{(-)|_{\partial \Sigma}}{\to}& [\partial \Sigma,X]
  }
  \,,
$$

where

* the bottom morphism is the restriction $[\partial \Sigma \hookrightarrow \Sigma, X]$ of configurations to the boundary;

* the right vertical morphism is the homomorphism from def. \ref{MapFromDiscretizationOfSmooth0Type}.
=--

+-- {: .num_prop #PlotsOfMappingSpaceWithNonVaryingBoundary}
###### Proposition

The [[smooth space]] $[\Sigma, X]_{\partial \Sigma}$ is a [[diffeological space]] whose underlying set is $C^\infty(\Sigma,X)$ and whose $U$-plots for $U \in $ [[CartSp]] are smooth functions
$\phi \colon U \times \Sigma \to X$ such that $\phi(-,s) \colon U \to X$ is the constant function for all $s \in \partial \Sigma \hookrightarrow \Sigma$.

=--


+-- {: .num_defn #SmoothFunctional}
###### Definition

A **[[nonlinear functional|functional]]** on the mapping space $[\Sigma, X]$ is a [[homomorphism]] of smooth spaces

$$
  S \colon [\Sigma, X]_{\partial \Sigma} \to \mathbb{R}
  \,.
$$

=--

##### Functional derivative / variational derivative
 {#FunctionalDerivative}

Write

$$
  \mathbf{d} \colon \mathbb{R} \to \Omega^1
$$

for the [[de Rham differential]] incarnated as a [[homomorphism]] of [[smooth spaces]] from the [[real line]] to the smooth [[moduli space]] of [[differential 1-forms]].


+-- {: .num_defn}
###### Definition

The **functional derivative** 

$$
  \mathbf{d}S
  \in 
  \Omega^1([\Sigma,X]_{\partial \Sigma})
$$ 

of a functional $S$, def. \ref{SmoothFunctional}, is simply its [[de Rham differential]] as a homomorphism of smooth spaces, hence the composite

$$
  \mathbf{d} S \colon [
  \Sigma, X]_{\partial \Sigma} 
     \stackrel{S}{\to} 
  \mathbb{R}   
    \stackrel{\mathbf{d}}{\to}
  \Omega^1
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

This means that for each smooth parameter space $U \in $ [[CartSp]] and for each smooth $U$-parameterized collection 

$$
  \phi \colon U \times \Sigma \to X
$$

of smooth functions $\Sigma \to X$, constant in the parameter $U$ in some neighbourhood of the boundary of $\Sigma$, 

$$
  S_\phi \colon [\Sigma,X]_{\partial \Sigma}(U) \to C^\infty(U,\mathbb{R})
$$

is the function that sends each such $U$-collection of configurations to the $U$-collection of their values under $S$. Then

$$
  (\mathbf{d}S)_\phi \in \Omega^1(U)
$$

is the smooth [[differential 1-form]]

$$
  (\mathbf{d}S)_\phi = \mathbf{d}(S(\phi))
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $\Sigma = [0,1] \hookrightarrow \mathbb{R}$ be the standard [[interval]]. Let 

$$
  L(-,-) \mathbf{d}t \in \Omega^1([0,1], C^\infty(\mathbb{R}^2))
$$ 

and consider the functional

$$
  S
  \colon
  ([0,1] \stackrel{\gamma}{\to} X)
  \mapsto
  \int_{0}^1 L(\gamma(t), \dot \gamma(t)) d t
  \,.
$$

Then for $U = \mathbb{R}$ and any smooth $U$-parameterized collection $\{\gamma_{u} \colon \Sigma \to X\}_{u \in U}$ the functional derivative takes the value

$$
  \begin{aligned}
   \mathbf{d}S_{\gamma_{(-)}}
   & =
   \left(
     \frac{d}{d u} \int_0^1 L(\gamma_u(t), \dot \gamma_u(t)) dt
   \right)
   \mathbf{d}u
   \\
    & = 
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial \dot \gamma_u(t)}{\partial u}
     \right) dt
     \mathbf{d} u
     \\
     & =
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial }{\partial t}\frac{\partial \gamma_u(t)}{\partial u}
     \right) dt
     \mathbf{d} u
     \\
     & =
     \int_{0}^1
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
      - 
       \frac{\partial}{\partial t}\frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
     \right)
     \frac{\partial \gamma_u(t)}{\partial u} dt
     \mathbf{d}u
  \end{aligned}
  \,.
$$

Here we used [[integration by parts]] and used that the boundary term vanishes

$$
  \begin{aligned}
    \int_{0}^1 \frac{\partial}{\partial t} 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(s), \dot \gamma_u(s))
      \frac{\partial \gamma_u(s)}{\partial u}
    \right)
    d s
    & = 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(1), \dot \gamma_u(1))
      \frac{\partial \gamma_u(1)}{\partial u}
    \right)
    - 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(0), \dot \gamma_u(0))
      \frac{\partial \gamma_u(0)}{\partial u}
    \right)
    \\
    & = 0
  \end{aligned}
$$

since by prop. \ref{PlotsOfMappingSpaceWithNonVaryingBoundary} $\gamma_{(-)}(1)$ and $\gamma_{(-)}(0)$ are constant.

=--

##### Euler-Lagrange equations
 {#EulerLagrangeEquations}

* [[critical locus]]

* [[Euler-Lagrange equation]]

* [[equations of motion]]

#### $\mathcal{D}$-geometry
 {#DGeometry}

* [[D-geometry]]

##### Infinitesimal smooth loci

+-- {: .num_defn #SmoothL}
###### Definition

Write

$$
  SmoothLoci \coloneqq SmoothAlgebras^{op} \coloneqq Func^\times(CartSp,Set)
$$

for the category of [[spaces]] which are [[Isbell duality|formally dual]] to [[smooth algebras]]: the [[opposite category]] of that of [[smooth algebras]]. This is called the category of **[[smooth loci]]**.

=--

+-- {: .num_defn #InfinitesimalAlgebra}
###### Definition

A **[[Artin ring|smooth Artin algebra]]** (also called a "Weil algebra" in the [[synthetic differential geometry]]-literature) is a [[smooth algebra]] $A$ whose underlying $\mathbb{R}$-[[vector space]] is a [[direct sum]] of the form

$$
  A = \mathbb{R} \oplus V
  \,,
$$

where $V$ is of finite [[dimension]] and such that every element $v \in V \subset A$ is nilpotent, in that there is $n \in \mathbb{N}$ such that the $n$-fold product of $v$ with itself in $A$ vanishes: $v^n = 0$.

=--

+-- {: .num_example }
###### Example

The smallest smooth Artin algebra is the [[ring of dual numbers]], 
def. \ref{DualNumbers}, for which $V = \mathbb{R}$. 

=--

+-- {: .num_defn #InfinitesimallyThickenedPoints}
###### Definition

Write 

$$
  InfPoint \hookrightarrow SmoothLoci
$$

for the [[full subcategory]] of $SmoothLoci$, def. \ref{SmoothL}, of those that are duals of Artin algebras, def. \ref{InfinitesimalAlgebra}.

We call this the category of **[[infinitesimally thickened points]]**.

=--

##### de Rham space

* [[de Rham space]]

##### Jet bundles

* [[jet bundle]]


### Semantic Layer
 {#DifferentiationLayerSem}

#### Synthetic differential geometry

* [[synthetic differential geometry]]



We have two [[full and faithful functors]]

$$
  CartSp \hookrightarrow SmoothLoci
$$


$$
 InfPoint \hookrightarrow SmoothLoci
 \,.
$$

+-- {: .num_defn #InfinitesimallyThickenedCartesianSpaces}
###### Definition

Write [[CartSp]]${}_{th} \hookrightarrow SmoothLocus$ for the [[full subcategory]] of that of [[smooth loci]], def. \ref{SmoothL}, on those of the form 

$$
  \mathbf{U} = U \times D
$$ 

with $U \in CartSp \hookrightarrow SmoothLoci$ and $D \in InfPoint \hookrightarrow SmoothLoci$.

We may call this the category of **infinitesimally thickened Cartesian spaces** or or **[[formal smooth manifold|formal smooth Cartesian spaces]]**.

=--

The category $CartSp_{th}$ carries several [[coverages]] of interest. One is this:

+-- {: .num_defn #CahiersTopos}
###### Definition

For $\mathbf{U} = U \times D \in CartSp_{th}$ say that a [[covering family]] is a set of morphisms in $CartSp_{th}$ of the form $\{ U_i \times D \stackrel{(\phi_i, id_D)}{\to} U \times D\}_i$ such that 
$\{ U_i \stackrel{\phi_i}{\to} U\}_i$ is a [[covering]] family in [[CartSp]]. 

The corresponding [[sheaf topos]] $Sh(CartSp_{th})$ is known as the **[[Cahiers topos]]**.

=--

+-- {: .num_prop }
###### Proposition

The [[Cahiers topos]] $Sh(CartSp_{th})$, def. \ref{CahiersTopos},  
is a [[cohesive topos]].

=--

+-- {: .num_defn }
###### Definition

We write

$$
  SynthDiff0Type \coloneqq Sh(CartSp_{th})
  \,.
$$

=--

* [[synthetic differential infinity-groupoid]]

##### Tangent bundle

Write $D \in Sh(CartSp_{th})$ for the [[smooth locus]]
formally dual to the [[ring of dual numbers]], def. \ref{}.
Write

$$
  i \colon * \to D
$$

for the unique point inclusion.

+-- {: .num_defn }
###### Definition

For $X \in SynthDiff0Type$, the [[internal hom]]

$$
  T X \coloneqq [D,X] \in SynthDiff0Type
$$ 

equipped with the morphism

$$
  [i,X] \colon [D,X] \to [*,X] \simeq X
$$

is the **[[tangent bundle]]** of $X$.

=--

+-- {: .num_defn }
###### Definition

For $X \in SynthDiff0Type$, a **[[vector field]]** $v$ on $X$ is a [[section]] 

$$
  \array{
     X &&\stackrel{v}{\to}&& T X
     \\
     & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{[i,D]}}
     \\
     && X
  }
  \,.
$$

The **smooth space of vector fields** is the [[internal hom]] in the [[slice topos]] over $X$

$$
  \mathbf{\Gamma}_X(T X ) \coloneqq [X,T X]_X
  \,.
$$

=--

##### Differential equations

* [[equation]]

* [[differential equation]]


#### Differential cohesion of the topos of smooth spaces
 {#DifferentialCohesionOfToposOfSmoothSpaces}

Recall the sites 

* [[CartSp]], def. \ref{TheDifferentiallyGoodOpenCoverCoverage};

* [[infinitesimally thickened point|InfPoint]], def. \ref{InfinitesimallyThickenedPoints};

* [[formal smooth manifold|CartSp]]${}_{th}$, def. \ref{InfinitesimallyThickenedCartesianSpaces}.



+-- {: .num_defn #TheMorphismsOfSitesForCartSpInfinitesimalNeighbourhood}
###### Definition

Define [[functors]]

$$
  CartSp
   \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\leftarrow}}
  CartSp_{th}
   \stackrel{\iota}{\leftarrow}
  InfPoint
$$

by

* $i \colon U \mapsto U \times *$;

* $p \colon U \times D \mapsto U$

* $\iota \colon D \mapsto * \times D$

=--

+-- {: .num_prop #DifferentialCohesiveStructureOfSmoothSpaces}
###### Proposition

All three functors in def. \ref{TheMorphismsOfSitesForCartSpInfinitesimalNeighbourhood} are [[morphisms of sites]]. The induced [[geometric morphism]] of [[sheaf toposes]] is of the form


$$
  Sh(CartSp)
   \stackrel{}{\stackrel{\overset{Lan_i}{\hookrightarrow}}{\stackrel{\overset{(-)\circ i}{\leftarrow}}{\stackrel{\overset{(-)\circ p}{\hookrightarrow}}{\underset{Ran_p}{\leftarrow}}}}}
  Sh(CartSp_{th})
   \stackrel{\overset{Lan_\iota}{\leftarrow}}{\underset{(-)\circ \iota}{\to}}
  Sh(InfPoint)
$$

where hence the morphism on the left is in particular an [[essential geometric morphism|essential]] [[geometric embedding]]. 

=--

+-- {: .num_prop }
###### Proposition

The sequence of [[geometric morphisms]]

$$
  Sh(CartSp) \stackrel{p^*}{\to} Sh(CartSp_{th}) \stackrel{\iota^*}{\to} Sh(InfPoint)
$$

exhibit a [[homotopy cofiber sequence]] in the [[(2,1)-category]] [[Topos]].

=--

+-- {: .proof}
###### Proof

By the discussion at _[(∞,1)Topos -- Existence of limits and colimits](%28infinity%2C1%29Topos#ExistenceOfLimitsAndColimits)_ the statement is equivalently that the [[inverse image]] functors

$$
  Sh(CartSp) 
    \stackrel{Lan_p}{\leftarrow}
  Sh(CartSp_{th})
    \stackrel{Lan_\iota}{\leftarrow}
  Sh(InfPoint)
$$

form a [[homotopy fiber sequence]] in [[(∞,1)Cat]]. Computing this in the [[model structure for quasi-categories]] after passing to [[nerves]], the morphism $N(Lan_p)$ is clearly an [[inner Kan fibration]] because of the [[subcategory]] inclusion $Sh(CartSp) \hookrightarrow Sh(CartSp_{th})$. So by the general discussion at [[homotopy pullback]] the homotopy fiber is given by the 1-categorical fiber of $N(Lan_p)$ in [[sSet]]. By the discussion at _[Left Kan extension - on representables](http://ncatlab.org/nlab/show/Kan+extension#LeftKanOnRepresentables)_ $Lan_p$ acts as $p$ on [[representable functor|representables]]. The 1-categorical fiber of $N(p) \colon N(CartSp_{th}) \to N(CartSp)$ is evidently $N(InfPoint)$. Since $Lan_\iota$ is a [[left adjoint]] it preserves colimits and since ever sheaf is a colimit of representables, this is sufficient to imply the claim.

=--

#### Differential cohesion
 {#DifferentialCohesion}


We axiomatize the existence of infinitesimals by further [[modal logic|modalities]] on a [[cohesive topos]].


+-- {: .num_defn #DifferentialCohesiveTopos}
###### Definition

Given a [[cohesive topos]] $\mathbf{H} = Cohesive0Type$ over a [[base topos]] [[Disc∞Grpd|Discrete0Type]], a structure of **[[differential cohesion]]** on $\mathbf{H}$ is an [[geometric embedding]] into a [[cohesive topos]] $\mathbf{H}_{th} = InfThickenedCohesive0Type$ with an extra [[left eadjoint]] that preserves the terminal object:

$$
  \array{
  Cohesive0Type
   &&\stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\hookrightarrow}}}&&
   InfThickenedCohesive0Type
   \\
   & {}_{\mathllap{\Gamma}}\searrow \nwarrow^{\mathrlap{Disc}} && {}^{\mathllap{\Gamma_{th}}}\swarrow \nearrow_{\mathrlap{Disc_{th}}}
   \\
   && Discrete0Type
  }
$$

=--


+-- {: .num_defn }
###### Definition

Given [[differential cohesion]], def. \ref{DifferentialCohesiveTopos}, define the [[monad]]/[[comonad]] [[adjunction]]

$$
  (Red \dashv \Pi_{inf})
  \colon
  \mathbf{H}_{th}
  \stackrel{\overset{i_*}{\leftarrow}}{\underset{i^*}{\to}}
  \mathbf{H}
  \stackrel{\overset{i_!}{\leftarrow}}{\underset{i_*}{\to}}
  \mathbf{H}
  \,.
$$

We call $Red(X)$ the **[[reduced type]]** of $X$ and $\Pi_{inf}(X)$ the [[infinitesimal path ∞-groupoid]] of $X$.


For the $(i_* \dashv i^*)$-[[unit of an adjunction|unit]] we write

$$
  InfinitesimalPathInclusion_X \colon X \to \Pi_{inf}(X)
$$

and call it the **constant infinitesimal path inclusion** on $X$.

The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]] 

$$
  Red X \to X
$$

we call the **inclusion of the reduced part** of $X$.

=--



+-- {: .num_defn }
###### Definition

Given a [[geometric embedding]] of [[(∞,1)-topos|∞-toposes]] 

$$
  CohesiveType \stackrel{i}{\hookrightarrow} InfThickenedCohesiveType
$$

exhibiting [[differential cohesion]], write 

$$
  CohesiveType 
    \stackrel{i}{\hookrightarrow} 
  InfThickenedCohesiveType
   \to 
  InfinitesimalType
$$

for the corresponding [[homotopy cofiber sequence]] in [[(∞,1)-topos]]. The [[full sub-(∞,1)-category]] that is the [[kernel]] of the [[global section geometric morphism]] of $InfininitesimalType$ we call the [[(∞,1)-category]] of **synthetic [[∞-Lie algebras]]**

$$
  L_\infty Algebra \coloneqq ker(\Gamma) \hookrightarrow InfinitesimalType \stackrerl{\Gamma}{\to} DiscreteType
  \,.
$$


=--

+-- {: .num_example }
###### Example

For the moment see at _[Synthetic differential infinity-groupoid -- Lie differentiation](synthetic%20differential%20infinity-groupoid#LieDifferentiation)_.

=--









+-- {: .num_prop }
###### Proposition

Setting

* $\mathbf{H}_{th} \coloneqq Sh(CartSp_{th})$

* $\mathbf{H} \coloneqq Sh(CartSp)$

* $\mathbf{H}_{inf} \coloneqq Sh(InfPoint)$

makes prop. \ref{DifferentialCohesiveStructureOfSmoothSpaces}
exhibit [[differential cohesion|differential cohesive structure]].

=--

##### de Rham space
 {#DifferentiationSemLayerDeRhamSpace}

+-- {: .num_defn }
###### Definition

For $X \in \mathbf{H}_{th}$ we call $\Pi_{inf}(X) \in \mathbf{H}$ the
**[[de Rham space]] object** of $X$.

=--


##### Jet bundle
 {#DifferentiationSemLayerJetBundle}

+-- {: .num_defn }
###### Definition

For $X \in \mathbf{H}$

$$
  Jet_X 
    \coloneqq 
  (InfinitesimalPathInclusion_X)_*
  \colon
  \mathbf{H}_{th}/X \to \mathbf{H}_{th}/\Pi_{inf}(X)
  \,.
$$

=--

For $(E \to X) \in \mathbf{H}_{th}/X$, $Jet_X(E)$ is the **[[jet bundle]]** of $E$.


##### Formally &#233;tale / formally unramified / formally smooth

+-- {: .num_defn #FormallyEtaleMap}
###### Definition

A morphism $f \;\colon\; X \to Y$ in $\mathbf{H}$ is called a **[[formally étale morphism]]** if the naturality square of the $\mathbf{\Pi}_{inf}$-[[unit of a monad|unit]] 

$$
  \array{
    X &\stackrel{}{\to}& \mathbf{\Pi}_{inf}(X)
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\mathbf{\Pi}_{inf}(f)}}
    \\
    Y &\to& \mathbf{\Pi}_{inf}(Y)
  }
$$

is an [[(∞,1)-pullback]]. 

=--


+-- {: .num_prop }
###### Proposition

If $X, Y \in $ [[SmoothMfd]] $\hookrightarrow$ $\mathbf{H} \stackrel{i_!}{\to} \mathbf{H}_{th}$ then for $f \colon X \to Y$ any morphism

1. $f$ is [[formally étale morphism]] precisely if $f$ is a [[submersion]] of smooth manifolds;

1. $f$ is a [[formally unramified morphism]] precisely if it is an [[immersion]] of smooth manifolds;

1. $f$ is a [[formally smooth morphism]] precisely if it is a [[diffeomorphism]].

=--



### Syntactic Layer

#### Differential homotopy type theory

* [[differential homotopy type theory]]

(...)
