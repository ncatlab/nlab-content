
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--



> This is a subentry of [[sigma-model]]. See there for background and context.

***

#Contents#
* table of contents
{:toc}


## Exposition of classical $\sigma$-models

We survey, starting from the very basics, [[classical field theory]] aspects of $\sigma$-models that describe dynamics of [[particles]], [[strings]] and [[branes]] on geometric [[target spaces]].


### The Newtonian particle
 {#ExpositionNewtonianParticle}

With hindsight, the earliest $\sigma$-model ever considered was also the very origin of the science of [[physics]]:

In order to describe the motion of matter [[particles]] in [[space]], [[Isaac Newton]] wrote down a [[differential equation]] with the famous symbols

$$
  \vec F = m \vec a 
  \,.
$$

More in detail, this is meant to describe the following situation:

* write $X := \mathbb{R}^3$ for the [[Cartesian space]] of [[dimension]] 3; think of this as a model for physics space;

* write $\Sigma := \mathbb{R}$ for the [[Cartesian space]] of [[dimension]] 1; think of this as the abstract trajectory of a point particle;

* write $\gamma : \Sigma \to X$ for a [[smooth function]]; think of this as an actual trajectory of a point particle in $X$;

  write furthermore

  * $\vec v := \dot \gamma \in Hom(T \Sigma, T X)$ for the [[derivative]] of $\gamma$; think of this as the [[velocity]] of the particle; and

  * $\vec a := \ddot \gamma$ for the second [[derivative]], the [[acceleration]] of the particle (strictly speaking this is the [[covariant derivative]] with respect to the trivial [[connection on a bundle|connection]] on the (canonically trivialized) [[tangent bundle]] on $\mathbb{R}^3$, see [below](#RelativisticParticle) for the fully fledged discussion).

We call then the collection of all [[smooth function]]s

$$
  Conf := C^\infty(\Sigma, X)
$$

the [[configuration space]] of a physical model of a point particle propagating on $X$. 


In order to define the model -- the model of some physical situation -- 

* pick a [[vector field]] $\vec F \in \Gamma(T X)$ on $X$. Think of this as expressing at each point a [[force]] acting on the particle with trajectory.

  For instance $\vec F := q \vec E$ could be an [[electromagnetic field|electric field]] $\vec E$ influencing the propagation of an electrically charged particle of [[charge]] $q$.

In modern language we may say:

* $\Sigma$ is the [[worldline]] of the particle;

* $X$ is the [[target space]] (expressing the fact that it is the [[codomain]] of a function $\gamma : \Sigma \to X$)

* $\vec F$ is the [[background gauge field]];

and the collection $(\Sigma, X, \vec F)$ of all three is a _$\sigma$-model_ . 

Given this data, the space of solutions to the original [[differential equation]]

$$
  P := \{ \gamma \in Conf | \forall t \in \mathbb{R} : \vec F_{\gamma(t)} = m \vec a(t) \}
$$

is called the [[covariant phase space]] of the model. The configurations in $P \subset Conf$ have the interpretation of being those potential configurations, that describe actual trajectories of [[particle]]s observed in nature.

Notice that in the case of vanishing [[force]] field $\vec F = 0$, the [[equations of motion]] of the [Newtonian particle](#ExpositionNewtonianParticle)

$$
  \vec a = 0
$$

may be read as characterizing precisely the [[geodesic]]s in $\mathbb{R}^3$ regarded as a [[Riemannian manifold]] using the canonical [[metric]]. This is a special and limiting case of the [relativistic particle](#RelativisticParticle) discussed below.

A cautionary note is in order. While the Newtonian particle may serve as an introductory example for motivating the concept of $\sigma$-models, it in general lacks some of the nice properties that later on we shall take to be characteristic of $\sigma$-models. Mainly this is due to the fact that the Newtonian particle is but a limiting approximation to the [[relativistic particle]] to which we turn next.


### The relativistic particle
 {#RelativisticParticle}


The Newtonian particle propagating on $\mathbb{R}^3$, discussed [above](#ExpositionNewtonianParticle), is a special and limiting case of a particle propagating on a 4-dimensional [[pseudo-Riemannian manifold]]: [[spacetime]]. For historical reasons (the same that led to the theory of [[gravity]] being called a theory of _[[general relativity|relativity]]_) this is called the _[[relativistic particle]]_.

The $\sigma$-model describing the relativistic particle is the following.

* [[target space|Target space]] is a  [[pseudo-Riemannian manifold]] $(X,g)$, thought of as [[spacetime]].

* Parameter space $\Sigma = \mathbb{R}$ is the [[real line]], thought of as the abstract [[worldline]] of the particle.

* The [[background gauge field]] is given by a [[circle n-bundle with connection|circle bundle with connection]], which for the moment we shall assume to be topologically trivial and hence be equivalently given by a smooth [[differential form|1-form]] $A \in \Omega^1(X)$. Its [[curvature]] [[exterior derivative]] $F := d A$ is the [[field strength]] of an [[electromagnetic field]] on $X$. 

* The [[configuration space]] is the [[quotient]] (or rather [[action groupoid]])

  $$
    Conf = C^\infty(\mathbb{R}, X)//Diff(\mathbb{R})
    \,,
  $$

  of [[smooth function]]s $\Sigma \to X$ by [[diffeomorphism]]s $\Sigma \stackrel{\simeq}{\to} \Sigma$. Each [[object]] in [[configuration space]] is a trajectory $\gamma : \Sigma \to X$ of a particle in spacetime, each morphism/equivalence $\gamma_1 \stackrel{\simeq}{\to} \gamma_2$ : a [[gauge transformation]].

* The [[covariant phase space]] -- the subspace of the configuration space of those configurations that satisfy the [[equations of motion]] -- is defined to be

  $$
    P =
    \{ [\gamma] \in Conf
     |\;\;
    m g(\nabla_{\dot \gamma} \dot \gamma/{\vert \dot \gamma}\vert , - ) =  q F(\dot \gamma, -)
    \;\; \}
    \subset Conf
    \,,
  $$

  where 

  * $\nabla$ denotes the [[covariant derivative]] of the [[Levi-Civita connection]] of the background metric $g$ on the [[tangent bundle]] $T X$ of $X$;

  * the equation is taken to hold in each [[cotangent space]] $T^*_{\gamma(\tau)} X$ for each $\tau \in \mathbb{R}$.

To see what this means, consider some special cases. First regard the case that the background field strength vanishes, $F = 0$. Then the equations of motion reduce to

$$
  \nabla_{\dot \gamma} \dot \gamma = 0 
  \,.
$$

This says that the trajectory $\gamma$ exhibits [[parallel transport]] of its tangent vectors with respect to the [[Levi-Civita connection]] of the background metric. These curves are precisely the _[[geodesics]]_ of the background geometry. This models motion under the [[force]] exerted by the field of [[gravity]] on our particle.

In the even more special case that $X$ is [[Minkowski spacetime]], where we may find a global [[coordinate chart]] $(\mathbb{R}^4, \eta) \simeq (X,g)$, these are exactly the straight lines in $\mathbb{R}^4$. Given any such, there is precisely one representative in the diffeomorphism class for which $\mathbb{R} \stackrel{\gamma}{\to} \mathbb{R}^4 \stackrel{x^0}{\to} \mathbb{R}$ is the identity, hence for which the [[worldline]] parameter coincides precisely with the chosen global time coordinate $t := x^0$ on $\mathbb{R}^4$. For these the equations of motions are again those of the free Newtonian particle $\vec a = 0$.

Remaining in the case that $X$ is [[Minkowski space]] but allowing now a nontrivial background field, notice that we may write the 2-form $F$ always as

$$
  F = \vec E_i \cdot d x^i \wedge d t + \vec B^i \epsilon_{i j k} d x^j \wedge d x^k
  \,,
$$

where $\vec E \in \mathbb{R}^3$ is the electric field strength vector and $\vec B \in \mathbb{R}^3$ the magnetic field strength vector. The spatial part of the above equations of motion are in this case again as for a Newtonian particle

$$
  m \vec a = q \vec E + q \vec v \times \vec B
  \,,
$$

where in the second term we have the [[cross product]] of vectors in $\mathbb{R}^3$. The [[force]] on the right is the _[[Lorentz force]]_ exerted by an electromagnetic field on a charged particle.

Notice that the equations of motion imply, generally, that the [[norm]] of $\dot \gamma$ is constant along the trajectory

$$
  \begin{aligned}
    \frac{d}{d \tau} g(\dot \gamma, \dot \gamma)
    &= 2 g(\nabla_{\dot \gamma} \dot \gamma, \dot \gamma)
    \\
    & = 
    2 g(g^{-1}(F(\dot \gamma,-), -), \dot \gamma)
    \\
    & \propto F(\dot \gamma, \dot \gamma)
    \\
    & = 
    0
  \end{aligned}
   \,.
$$

Therefore a trajectory that solves the equations of motion and whose tangent vector is [[timelike]] or [[spacelike]] or [[lightlike]], respectively, at any instant is so throughout. In particular, no choice of gravitational and electromagnetic background field strength can accelerate a physical particle from being timelike to being light-like.

Experiments around the second half of the 19th and the beginning of the 20th century established that this covariant phase space correctly describes the dynamics of gravitationally and electromagnetically charged relativistic particles. But also formally this phase space is not a randomly chosen space; instead, it is the [[critical locus]] of a (mathematically) natural [[action functional]].

The points in the [[covariant phase space]]

$$
  P := \{ [\gamma] \in Conf | 
   m g(\nabla_{\dot \gamma} \dot \gamma / {\vert \dot \gamma}\vert,-) =  q\iota_{\dot \gamma} F
    \}
  \subset Conf 
$$

happen to be the local critical points of the [[nonlinear functional|functional]]

$$
  S : Conf \to \mathbb{R}
$$

given by

\[
  \label{ParticleActionForGlobalA}
  \begin{aligned}
    S([\gamma]) 
     & := 
     S_{kin}([\gamma])
     +
     S_{gauge}([\gamma])
     \\
     & 
     := 
     m \int_\Sigma dvol(\gamma^*g)  + q \int_\Sigma \gamma^* A
  \end{aligned}
  \,,
\]

where on the left we have the integral of the [[volume form]] of the pullback $\gamma^* g \in Sym^2 T^* \Sigma$ of the metric on target space to the [[worldline]].

This is called the _[[action functional]]_ of the relativistic particle $\sigma$-model. The first summand is called the _kinetic action_, the second is called the _gauge coupling_  action. 

Typically one characterizes $\sigma$-models in terms of such action functionals, so that the [[covariant phase space]] is then given as their [[critical locus]]. This usually yields a simpler and deeper description of the model. 

Notably the above action functional has an evident generalization to the case where the background [[electromagnetic field]] is not given by a globally defined 1-form, but more generally by a [[circle n-bundle with connection|circle bundle with connection]] $\nabla$: if we pass to the exponentiated action functional

$$
  \exp(i S(-)) : Conf \to U(1)
$$

$$
  \exp(i S(\gamma)) = 
  \exp(S_{kin}(\gamma))
   \;\;
  \exp(i q \int_\Sigma \gamma^* A)
$$

the second factor is precisely the [[holonomy]] of $\nabla$ over the worldline. Hence for general electromagnetic background gauge fields the action functional is (assuming for simplicity now closed curves with $\Sigma = S^1$)

$$
  \exp(i S(\gamma))   
  = 
  \exp(S_{kin}(\gamma))
   \;\;
  hol(\nabla, \gamma)
  \,.
$$

This is the beginning of an important pattern: most $\sigma$-models are determined by a kind of higher [[gauge field]] $\nabla$ on [[target space]] (a cocycle in the [[differential cohomology]] of [[target space]]) and their dynamics is determined by an [[action functional]] that is the [[higher parallel transport|higher holonomy]] functional of this gauge field. 

At the same time the kinetic action functional factor is usually to be understood as part of the [[measure]] on [[configuration space]] $Conf$. For the particle this has been made precise: the [[path integral]] 

$$
 \int_{\gamma \in Conf} hol(\nabla,\gamma) \;\;\exp(i S_{kin}(\gamma)) [d \gamma]
  :=
 \int_{\gamma \in Conf} hol(\nabla,\gamma) d \mu_{Wien}
$$

can be interpreted as the [[integral]] with respect to the [[Wiener measure]] on path space (after [[Wick rotation]], at least). The kinetic part of the action functional is then absorbed into the Wiener measure $d \mu_{Wien}$

$$
  \exp(i S_{kin}(\gamma)) [d\gamma] := d \mu_{Wien}
  \,;
$$

(at least after replacing the kinetic [[Nambu-Goto action]] by the classically equivalent [[Polyakov action]])
and the path integral is just the "expectation value" (after Wick rotation) of the holonomy, taken over all trajectories.

Since there is a good general abstract theory of higher gauge fields and their higher holonomies (see [[differential cohomology]] and [[cohesive (infinity,1)-topos|differential cohomology in a cohesive topos]]), this suggests that there should be a general abstract theory of $\sigma$-models. Aspects of this are discussed [below](Exposition).


### The relativistic $(n-1)$-brane
 {#RelativisticNBrane}

It is hard not to consider the following generalization of the relativistic particle $\sigma$-model, that we discussed [above](#RelativisticParticle):

notice that nothing in the structure of the relativistic particle's [[action functional]] (eq:ParticleActionForGlobalA) relies on the [[dimension]] of $\Sigma$ being $1$. Instead, it is just the degree-1 case of the following family of types of classical $\sigma$-models, that make sense for all $n \in \mathbb{N}$:

* let $\Sigma$ be of [[dimension]] $n$;

* let [[target space]] be a [[pseudo-Riemannian manifold]] $(X,g)$ as before;

* let the [[background gauge field]] be given by a smooth [[differential form|differential n-form]] $A \in \Omega^n(X)$.

* let [[configuration space]] be the [[action groupoid|weak quotient]]

  $$
    Conf_\Sigma := C^\infty(\Sigma, X)//Diff(\Sigma)   
    \,.
  $$

* let then finally the [[action functional]] be given by

  $$
    S([\gamma]) = \int_\Sigma dvol(\gamma^* g) + \int_\Sigma \gamma^* A
    \,.
  $$

This is the same formula as for the relativistic particle as before, only that now the differential forms are taken to be of degree $n$ and integrals to be over $n$-dimensional spaces.

Moreover, for each $n \in \mathbb{N}$ there is an analog of the generalization 

$$
  \{1-forms\} \hookrightarrow \{circle bundles with connection\}
$$

to the generalization

$$
  \{n-forms\} \hookrightarrow \{circle n-bundles with connection\}
  \,.
$$

Given any [[circle n-bundle with connection]] $\nabla$ and closed $\Sigma$ of dimension $n$, there is a [[higher parallel transport|higher]] [[holonomy]] [[nonlinear functional|functional]]

$$
  hol(\nabla, -) : (\Sigma \stackrel{\gamma}{\to} X) \mapsto 
  hol(\nabla, \gamma) \in U(1)
$$

that extends the functional $A \mapsto \exp(i \int_\Sigma \gamma^* A)$.

Therefore, generally, we may take for $n \in \mathbb{N}$

* the [[background gauge field]] on $X$ to be a [[circle n-bundle with connection]] $\nabla$;

* the exponentiated [[action functional]] to be

  $$
    [\gamma] \mapsto \exp(i \int_\Sigma dvol(\gamma^* )) \;\;\; hol(\nabla,\gamma)
   \,.
  $$


For $n = 3$ such a $\sigma$-model describes an analog of a relativistic particle which is not point-like, but 2-dimensional (with 3-dimensional trajectory) hence which reminds one of a [[membrane]]. Inspired by this term, the general case has come to be known as the _relativistic $(n-1)$-[[brane]]_. 

The case $n = 2$ is called the relativistic [[string]], which we consider in more detail [below](#RelativisticString). This has received a lot of attention (in _[[string theory]]_) not just because it is the next simplest in an infinite hierarchy of cases, but also because its quantum theory turns out to have various interesting features that seem to make it special. Moreover, many of the $(n-1)$-branes for other $n$ re-appear in one way or other in the study of the string (as its boundary [[D-brane]]s in all dimensions $0 \leq n \leq 10$, as its "strongly coupled" version: the [[M-theory membrane]], or as its [[electric-magnetic duality|electric-magnetic dual]]: the [[NS5-brane]]). If nothing else, the seemingly innocent step from $n = 1$ to $n = 2$ in the $\sigma$-model shows that there is a rich pattern of higher dimensional ($\sigma$-model) quantum field theories that are all interrelated in intricate ways.

Another important special case for the general discussion of $\sigma$-models is the case of the [[membrane]], $n = 3$, for which the [[background gauge field]] is a _[[Chern-Simons circle 3-bundle]]_ for some $G$-[[principal bundle]] on $X$, for $G$ some suitable [[Lie group]]. In this case the gauge-coupling [[Lagrangian]] of the $\sigma$-model is, locally, the [[Chern-Simons form]] $CS(\nabla_\mathfrak{g})$ of a $G$-[[connection on a bundle|connection]] $\nabla_{\mathfrak{g}}$, hence the [[action functional]] is (locally) the [[Chern-Simons theory|Chern-Simons functional]]

$$
  (\Sigma \stackrel{\gamma}{\to} X) \mapsto \int_\Sigma CS(\gamma^* \nabla_\mathfrak{g})
  \,.
$$

Below we will see that when $\sigma$-models are considered [[internalization|internal to]] a suitable [[cohesive (∞,1)-topos]], then there are _universal_ $\sigma$-models of this Chern-Simons type, whose [[target space]] is no longer a [[smooth manifold]], but a [[smooth ∞-groupoid]] incarnation of a [[classifying space]] $B G$. 


### The relativistic string
 {#RelativisticString}

The important case $n = 2$ of the general [(n-1)-brane sigma-model](RelativisticNBrane) that we considered above is called the [[string]]-$\sigma$-model. Even though this is just the first step after the relativistic particle, the theory of this $\sigma$-model is already considerably richer classically and all the more so after quantization. For the purposes of this exposition here we only briefly indicate the physical interpretation of the $\sigma$-model and then consider some qualitatively new higher [[gauge theory]] aspects, that appear in this dimension.


First notice that by the general reasoning of relativistic $(n-1)$-branes, the [[background gauge field]] is now given (if we assume for the moment a topological trivial class) by a 2-form, which is traditionally denoted $B \in \Omega^2(X)$ and called the _[[B-field]]_. Its 3-form [[curvature]] [[field strength]] is traditionally denoted $H := d B$.

The [[action functional]] of the [[string]]'s $\sigma$-model for a [[pseudo-Riemannian manifold|pseudo-Riemannian]] [[target space]] $(X,g)$ with background gauge field $B$ is

$$
  [\gamma] \mapsto \int_\Sigma dvol(\gamma^* g) + \int_\Sigma \gamma^* B
  \,.
$$

To gain insight into the physical meaning of this, consider the simple case that [[target space]] $(X,g)$ is [[Minkowski spacetime]] and that the [[worldsheet]] $\Sigma = \mathbb{R} \times S^1$ is the [[cylinder]]. With $(\tau,\sigma)$ the two canonical [[coordinate]]s on $\Sigma$, we still write 

$$
  \dot \gamma := \partial_\tau \gamma
$$

for the derivative "along the trajectory" (along the $\mathbb{R}$-factor), but now we also have the derivative $\partial_\sigma \gamma$ which we may think of as being _tangential to the string_ at any instant of its trajectory. A field configuration $\gamma : \Sigma \to X$ may be thought of as the trajectory of a [[circle]] propagating in $X$.

The critical trajectories $\gamma : \Sigma \to X$ are found to be those that satisfy the 2-dimensional [[wave equation]]

$$
  g(\ddot \gamma,-)  - g(\partial_\sigma^2 \gamma,-)
  = 
  H(\dot \gamma, \partial_\sigma \gamma,-)
$$

on the [[worldsheet]]. Comparison with the equation of motion of the  [relativistic particle](#RelativisticParticle) shows that $H(\partial_\sigma \gamma, -,-)$ plays the role of an electromagnetic [[field strength]] 2-form.  Hence the string behaves as if electric [[charge]] is spread out evenly along it. 

For _point particle limit configurations_  $\gamma$, where the string has vanishing extension in that $\partial_\sigma \gamma = 0$, the above equation reduces again to free motion

$$
  \ddot \gamma = \vec a = 0
$$

and for general $(X,g)$ to the corresponding [[geodesic]] motion.

Therefore close to these point particle configurations the string looks like a little oscillating loop whose dynamics is that of its "center of mass" point, but slightly modified by the energy in the oscillations and the way these interact with the background fields. After quantization of the $\sigma$-model, these oscillations have a discrete ( quantized!) set of possible frequencies, and indeed each of the oscillation modes makes the string appear in the point particle limit as one species or other of a relativistic particle. (For more on this see _[[string theory]]_.)

Next we have a look at aspects of higher [[gauge theory]] that appears in $n = 2$.

The above 2-form $B$ is in general just the local connection form of a _[[circle n-bundle with connection|circle 2-bundle with connection]]_ $\nabla$ on $X$, given (as its [[homotopy fiber]]) by a morphism of [[smooth ∞-groupoid]]s $\alpha : X \to \mathbf{B}^2 U(1)$. Equivalently this is a $U(1)$-[[bundle gerbe]] with connection.

There is a canonical 1-dimensional [[infinity-representation|2-representation]] of the [[circle n-group|circle 2-group]] $\mathbf{B} U(1)$ on [[2-vector space]]s:

$$
  \rho : \mathbf{B} \mathbf{B}U(1) \to 2 Vect
  \,.
$$

Hence the corresponding [[associated infinity-bundle|associated 2-bundle]] is classified by a morphism

$$
  \rho(g) : X \stackrel{g}{\to} \mathbf{B}^2 U(1)
   \stackrel{\rho}{\to}
  2 Vect
  \,.
$$

One can consider the string $\sigma$-model for [[worldsheet]]s with [[boundary]]. A careful analysis then shows that the consistent Dirichlet-type boundary conditions that can be added correspond, roughly,  to certain subspaces of [[target space]] -- called [[D-brane]]s -- that are equipped with a section $V : \mathbf{1} \to \rho(g)|_{D-brane}$ of the background gauge field 
[[n-vector bundle|2-vector bundle]] restricted to the $D$-brane. Such a section is precisely a [[twisted bundle|twisted vector bundle]] on the brane, where the twist is the class in [[integral cohomology]] $H^3(X, \mathbb{Z})$ of the background gauge field. More generally, these twisted bundles are cocycles in [[twisted K-theory]] and [[differential K-theory]]. Hence more [[differential cohomology]] appears on the target space for the string in the presence of string boundaries.

More generally, the structure [[2-group]] of the background [[principal 2-bundle]] need not be $\mathbf{B}U(1)$, which is given by the [[crossed module]] $[U(1) \to 1]$. Instead, it can be the [[automorphism 2-group]] $AUT(U(1))$, which is given by the crossed module $(U(1) \to Aut(U(1)) \simeq \mathbb{Z}_2)$. An $AUT(U(1))$-[[principal 2-bundle]] on $X$ is equivalently a double cover of $X$, equipped with a circle 2-bundle that has a twisted [[equivariant cohomology|equivariance]] under the $\mathbb{Z}_2$-[[action]].  Such a background gauge field structure is called a _string [[orientifold]]_ background. This is a kind of [[higher category theory|higher structure]] that the relativistic particle alone cannot see.

More such higher structure appears as one passes to the [[supergeometry]] analogs of the $\sigma$-models that we have considered so far: the [[superstring]]. The presence of the additional [[fermion]] fields that this brings with it (both on [[target space]] as well as on the [[worldsheet]]) influences all the structures that we have considered so far. For instance, a phenonemon called a fermionic [[quantum anomaly]] forces the above background [[circle n-bundle|circle 2-bundle]] to become a [[twisted cohomology|twisted 2-bundle]], where the twist is given by a [[fivebrane]] [[charge]] [[Chern-Simons circle 3-bundle]]. This is discussed in detail at _[[differential string structure]]_

These are the first examples of a general phenomenon: as $n$ increases, a background gauge $n$-bundle with connection may constitute considerably more structure then one might naively expect from a generalization of the ordinary notion of a connection. More examples of this phenomenon arise when we allow our [[target space]]s to be general [[smooth ∞-groupoid]]s, below.

## Related concepts

* [[harmonic map]]
