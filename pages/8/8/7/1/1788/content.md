

#Contents#
* table of contents
{:toc}

Throughout we use the case of the real [[scalar field]] as an illustrative running example, which we develop alongside with the theory. The discussion of other [[field (physics)|field]] species that are of more genuine interest in applications is postponed to dedicated sections below.

### A first idea of quantum fields

We introduce here the basic concepts of _[[Lagrangian field theory]]_, first for [[prequantum field theory]] and then for its [[deformation quantization]] to [[perturbative quantum field theory]]. 

In full beauty these concepts are extremely general; but in this section the aim is to give a first good idea of the subject, and therefore we present for the moment only a restricted setup, notably assuming that [[spacetime]] is [[Minkowski spacetime]], that the [[field bundle]] (see below) is an ordinary and [[trivial bundle|trivial]] [[fiber bundle]] and we consider its [[jet bundle]] only to second order.. 

(This does subsume what is considered in most traditional texts on the subject. In subsequent sections we will eventually discuss more general situations, notably we will eventually allow spacetime to be any [[globally hyperbolic Lorentzian manifold]] and the [[field bundle]] to be an [[infinity-Lie algebroid]]. This is sufficient generality to capture the established perturbative [[BV formalism|BRST-BV quantization]] of [[gauge theory]] [[AQFT on curved spacetime|on curved spacetimes]]. It is however still not the most general setup that may be considered.)

#### Spacetime

Thoughout, let

$$
  p \in \mathbb{N}
$$

be a [[natural number]] and write

$$
  \Sigma \coloneqq \mathbb{R}^{p,1} \coloneqq (\mathbb{R}^{p+1}, \eta)
$$

for [[Minkowski spacetime]] of [[dimension]] $p+1$, hence for the [[smooth manifold]] which is the [[Cartesian space]] $\mathbb{R}^{p+1}$ of dimension $p+1$ equipped with the [[left invariant differential form|constant]] [[pseudo-Riemannian metric]] $\eta$ which at the origin is given by the standard [[quadratic form]] of [[signature of a quadratic form|signature]]

$$
  (-, +, \cdots, +)
$$

in terms of the canonical [[coordinate functions]] 

$$
  x^k \;\colon\; \mathbb{R}^{p+1} \longrightarrow \mathbb{R}
$$

which we index starting at zero: $(x^k)_{k = 0}^p$.

We write

$$
  dvol_\Sigma
   \;\coloneq\; 
  d x^0 \wedge d x^1 \wedge \cdots d x^p
  \in \Omega^{p+1}(\mathbb{R}^{p,1})
$$

for the induced [[volume form]], and we call

$$
  d x^0 \in \Omega^1(\Sigma)
$$

the canonical representative of the canonical [[time orientation]] on Minkowski spacetime.


#### Fields

A _[[field (physics)|field]] configuration_ on a given [[spacetime]] $\Sigma$ is meant to be some kind of [[quantity]] assigned to each point of spacetime (each [[event]]), such that this assignment varies smoothly with spacetime points. For instance an _[[electromagnetic field]]_ configuration is at each point of spacetime a collection of [[vectors]] that encode the direction in which a [[charged particle]] passing through that point will feel a [[force]] (the [[Lorentz force]]).

This is readily formalized: If 

$$
  F \in SmthMfd
$$

is the [[smooth manifold]] of "values" that the the given kind of field may take at any spacetime point, then a field configuration $\phi$ is modeled as a [[smooth function]] from spacetime to this space of values

$$
  \Phi
    \;\colon\;
   \Sigma
     \longrightarrow
   F
  \,.
$$

It will be useful to unify spacetime and the space of field values into a single space, the [[Cartesian product]] 

$$
  E \;\colon\; X \times \Sigma
$$ 

and to think of this equipped with the [[projection]] map onto the first factor as a [[fiber bundle]] of spaces of field values over spacetime


$$
  \array{
     E &\coloneqq& \Sigma \times F
     \\
     {}^{\mathllap{p}}\downarrow & \swarrow_{\mathrlap{pr_1}}
     \\
     \Sigma
  }
  \,.
$$

This is then called the _[[field bundle]]_, which specifies the kind of values that the given field species may take at any point of spacetime. Since the space $F$ of field values is the [[fiber]] of this [[fiber bundle]], it is sometimes also called the _[[field fiber]]_. 


Regarded this way, then a _[[field (physics)|field]] configuration_ is a _smooth [[section]]_ of this [[bundle]], namely a [[smooth function]] of the form
$\phi \colon \Sigma \longrightarrow E$ such that compsed with the projection map it is the [[identity function]] $p \circ \phi = id$:

$$
  \array{
    && E
    \\
    & \nearrow & \downarrow
    \\
    \Sigma &=& \Sigma
  }
  \,.
$$

Given such a [[fiber bundle]] regarded as a [[field bundle]], we write

$$
  \Gamma_\Sigma(E) \in SmoothSet
$$

for its [[smooth space|smooth]] [[space of smooth sections]].


+-- {: .num_example #TrivialVectorBundleAsAFieldBundle}
###### Example
**([[trivial vector bundle]] as a [[field bundle]])**

In applications the [[field fiber]] $F$ is often a [[finite number|finite]] [[dimension|dimensional]] [[Euclidean space]] and equipped with the structure of a [[vector space]]. In this case the trivial field bundle with fiber $F$ is of course a _[[trivial vector bundle|trivial]] [[vector bundle]]_.

Choosing any [[linear basis]] $(\phi^a)_{a = 1}^s$ of the field fiber, then over [[Minkowski spacetime]] we have canonical [[coordinates]] on the total space of the field bundle

$$
  ( \{x^\mu\}_{\mu = 0}^p, \{ \phi^a \}_{a = 1}^s )
  \,.
$$

=--


+-- {: .num_example #RealScalarFieldBundle}
###### Example
**([[real scalar field]])**

If $\Sigma$ is a [[spacetime]] and if 

$$
  F \coloneqq \mathbb{R}
$$

is simply the [[real line]], then the corresponding trivial [[field bundle]]

$$
  \array{
    \Sigma \times \mathbb{R}
    \\
    {}^{\mathllap{pr_1}}\downarrow
    \\
    \Sigma
  }
$$

is the _[[trivial fiber bundle|trivial]] [[real line bundle]]_ (a special case of example \ref{TrivialVectorBundleAsAFieldBundle}) and the corresponding [[field (physics)|field]] is called the _[[real scalar field]]_ on $\Sigma$. A configuration of this field is simply a [[smooth function]] on $\Sigma$ with values in the [[real numbers]]:

$$
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
    \;\simeq\;
  C^\infty(\Sigma)
  \,.
$$

=--

#### Variational calculus

Given a [[field bundle]] as above, we know what type of quantities the corresponding fields assign to a given spacetime point. Among all consistent such field configurations, some are to qualify as those that "may occur in reality" (if we think of the field theory as a means to describe parts of the [[observable universe]]). Moreover, if the reality to be described does not exhibit "[[action at a distance]]" then admissibility of its field configurations should be determined over arbitrary small spacetime regions,in fact over the [[infinitesimal neighbourhood]] of any point. This means equivalently that the "real" field configurations should be those that satisfy a given [[differential equation]], hence an [[equation]] between the value of its [[derivatives]] at any spacetime point.

In order to formalize this, it is clearly useful to first collect all the possible derivatives that a field may have at any given point into one big space of "field derivatives at spacetime points". This collection is called the _[[jet bundle]]_ of the [[field bundle]], given as def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below.

Moving around in this space means to change the possible value of fields and their derivatives, hence to _vary_ the fields. Accordingly [[variational calculus]] is just [[differential calculus]] on a [[jet bundle]], this we consider in def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime} below..


+-- {: .num_defn #JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[jet bundle]] of a [[trivial vector bundle]] over [[Minkowski spacetime]])**

Given a [[vector space]] $F = \mathbb{R}^s$ with [[linear basis]] $(\phi^a)_{a = 1}^s$, then the _second order [[jet bundle]]_ over [[Minkowski spacetime]] $\Sigma$ of the trivial vector bundle

$$
  E \coloneqq \Sigma \times F
$$

is the [[Cartesian space]] 

$$
  J^k_{\Sigma}( E )
    \coloneqq
  \mathbb{R}^{ (p+1) + s( 1 + (p+1) + (p+1)(p+2)/2) }
$$

equipped with canonical coordinates

$$
  \left(
     (x^\mu)
     \,,\,
     (\phi^a )
     \,,\,
     ( \phi^a_{,\mu} )
     \,,\,
     ( \phi^a_{,\mu_1 \mu_2} )
  \right)
$$    

where the indices $\mu_i$ range from 0 to $p$ and are symmetric, while the index $a$ ranges from $1$ to $s$, and equipped with the corresponding [[projection]] map.


Given such a second order jet bundle then the _second order [[jet prolongation]]_ is the function from the [[space of sections]] of the original bundle to the jet bundle which records the field and all its [[derivatives]] up to order 2:

$$
  \array{
    \Gamma_\Sigma(E)
      &\overset{j^2}{\longrightarrow}&
    \Gamma(\Sigma)(J^2 E)
    \\
    (\Phi^a)_{a = 1}^s
    &\mapsto&
    \left(
      (\Phi^a),
      ( \partial_\mu \Phi^a ),
      ( \partial_{\mu_1} \partial_{\mu_2} \Phi^a  )
    \right)
  }
  \,.
$$

=--


+-- {: .num_defn #VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[variational bicomplex]])**

Given a second order [[jet bundle]] $J^2_\Sigma(E)$ of a [[trivial vector bundle]] over [[Minkowski spacetime]] as in def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then its
 _[[horizontal derivative]]_ (or "[[total derivative]]") is the map

$$
  \mathbf{d}_h
  \;\colon\;
  \Omega^\bullet( J^2_\Sigma(E) )
  \longrightarrow
  \Omega^{\bullet+1}( J^2_\Sigma(E) )
$$

which on functions (0-forms) $f \colon J^2_\Sigma(E) \to \mathbb{R}$ is defined by

$$
  \mathbf{d}_h f
    \;\coloneqq\;
  \underoverset{p}{\mu = 0}{\sum}
  \left(
    \frac{\partial f}{\partial x^\mu}
    + 
    \frac{\partial f}{\partial \phi^a}
    \phi^a_{,\mu}
    + 
    \frac{ \partial f }{ \partial \phi^a_{,\nu}}
    \phi^a_{,\nu \mu }
  \right)
  \mathbf{d} x^\mu
$$

and extended to all forms by the graded [[Leibniz rule]], hence  as a [[derivation]] of degree +1. 

The _[[vertical derivative]]_ is 

$$
  \mathbf{d}_v \coloneqq \mathbf{d} - \mathbf{d}_h
  \,.
$$

This defines a bigrading on the [[de Rham complex]] on $J^2_\Sigma(E)$ 

$$
  \Omega^\bullet\left( J^2_\Sigma(E) \right)
  \;\coloneqq\;
  \underset{r,s}{\oplus} \Omega^{r,s}(E)
  \,.
$$


=--

+-- {: .num_defn #LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[local Lagrangian density]])**

Given a [[field bundle]] $E$ over a $(p+1)$-dimensional [[Minkowski spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}, then a _[[local Lagrangian density]]_ $L$ (for the field species thus defined) is a [[horizontal differential form]] of degree $(p+1)$ on the corresponding [[jet bundle]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  \mathbf{L} \;\in \; \Omega^{p+1,0}(E)
  \,.
$$

Since there is a specified [[volume form]] $dvol_{\Sigma}$ and since every [[horizontal differential form]] of degree equal to the the spacetime dimension is necessarily proportional to this volume form, any such Lagrangian density may uniquely be written as

$$
  \mathbf{L} = L dvol_\Sigma
$$

with $L \;\colon\; J^2_\Sigma(E) \to \mathbb{R}$ a smooth function on the jet bundle.


=--

+-- {: .num_prop #EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}
###### Proposition
**([[Euler-Lagrange operator]])**

If a [[Lagrangian density]] $\mathbf{L}$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) depends at most on first order jets, then its de Rham differential has a _unique_ decomposition as a sum of two terms

$$
  \mathbf{d} \mathbf{L}
  =
  \delta_{EL} \mathbf{L}
  + 
  \mathbf{d}_h \theta  
$$

such that

1. $\delta_{EL} \mathbf{L} \in \Omega^{p+1,0}(E) \otimes \mathbf{d}_v \Omega^{0,0}(E) \subset \Omega^{p+1,1}(E)$

1. $\mathbf{d_h} \theta \in \mathbf{d}_h \Omega^{p,1}(E)$.

The map

$$
   \delta_{EL} \;\colon\; \Omega^{p+1,0}(E) \longrightarrow \Omega^{p+1,1}_s(E)
$$

thus defined is called the _[[Euler-Lagrange operator]]_ and is given by

$$
  \delta_{EL} L dvol_\Sigma
  \;=\;
  \left(
    \frac{\partial L}{\partial \phi^a}
    -
    \frac{\partia}{\partial x^\mu}
    \frac{\partial L}{\partial \phi^a_{,\mu}}
  \right)
  dvol_\Sigma
$$



=--


+-- {: .proof}
###### Proof

Regarding existence, we claim that one possible choice is

$$
  \theta 
  \;=\;
  \frac{\partial L}{\partial \phi^a_{,\mu}}
  \mathbf{d}_v \phi^a \wedge \iota_{\partial_\mu} dvol_\Sigma
$$

hence

$$
  \mathbf{d}_h \theta
  \;=\;
  -
  \frac{\partial}{\partial x^\mu}
  \frac{\partial L}{\partial \phi^a_{,\mu}}
  \mathbf{d}_v \phi^a \wedge dvol_\Sigma
  -
  \frac{\partial L}{\partial \phi^a_{,\mu}}
  \mathbf{d}_v \phi^a_{,\mu} \wedge dvol \Sigma
$$

To see this, first notice that due to $\mathbf{L} = L dvol_\Sigma$
we have

$$
  \begin{aligned}
    \mathbf{d}\mathbf{L}
    & =
    \frac{\partial L}{\partial \phi^a} \mathbf{d}_v\phi^a \wedge dvol_{\Sigma}
    + 
    \frac{\partial L}{\partial \phi^a_{,\mu}} \mathbf{d}_v \phi^a_{,\mu} \wedge dvol_{\Sigma}
    \\
    & = 
    \frac{\partial L}{\partial \phi^a} \mathbf{d}_v\phi^a \wedge dvol_{\Sigma}
    -
    \frac{\partial}{\partial x^\mu}
    \frac{\partial L}{\partial \phi^a_{,\mu}}
    \mathbf{d}_v \phi^a \wedge dvol_\Sigma
     -
    \mathbf{d}_h \theta    
  \end{aligned}  
$$




=--



#### Equations of motion


+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition


=--


* [[field bundle]], [[jet bundle]], [[field (physics)|field]]

* [[local Lagrangian density]]

* [[Euler-Lagrange complex]], [[presymplectic current]]

* [[Cauchy surface]], [[covariant phase space]]

* [[Hamiltonian forms]], [[observables]], [[Poisson bracket]]

* [[algebra of observables]], [[states]]

[[formal deformation quantization]]

* [[Planck's constant]] $\hbar$

* example: [[Moyal deformation quantization]]

  $\mathcal{F}_{loc} \overset{:-:}{\longrightarrow} \mathcal{F}_{mc}[ [ \hbar ] ]$

* [[algebra of quantum observables]]

* [[quantum states]]


[[S-matrix]]

* [[causal additivity]]

* [[time-ordered product]]

* [[causally local net of quantum observables]]

...

running example: 

* [[scalar field]]

* [[Klein-Gordon operator]]

...

[[free field theory]]

* [[differential operator]], [[normally hyperbolic differential operator]]

* [[Green function]], [[distribution]], [[wave front set]]

* [[causal propagator]], [[advanced propagator]], [[retarded propagator]]

* [[Hadamard state]]

* [[Wick algebra]]

[[Feynman diagrams]]

* [[Feynman propagator]]

* [[loop order]]

[[renormalization]]

* [[extension of distributions]]

* [[main theorem of perturbative renormalization]]

...
