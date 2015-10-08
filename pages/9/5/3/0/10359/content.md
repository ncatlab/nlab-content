
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[symplectic manifold]] $(X,\omega)$ and given a [[Hamiltonian]] [[function]] $H \colon X \longrightarrow \mathbb{R}$, there is a [[Poisson bracket]] on an [[algebra of functions]] on the [[smooth space|smooth]] [[path space]] $[I,X]$  -- the "space of histories" or "space of [[trajectories]]" -- for $I = [0,1]$ the closed [[interval]], which is such that its [[symplectic leaves]] are each a copy of $X$, but regarded as the space of initial conditions for evolution with respect to $H$ with a [[source]] term added.

The first statement was first observed for the [[Peierls bracket]] of [[local prequantum field theory]] in ([Marolf 93, section II](#Marolf93)), but the construction there is not specific to the [[Peierls bracket]]. That the construction provides a [[foliation]] of trajectory space by [[symplectic leaves]] labeled by [[level sets]] of the [[Euler-Lagrange equation|Euler-Lagrange function]] was explicitly pointed out at ([Brunetti-Fredenhagen-Ribeiro 12, top of p. 4](#BrunettiFredenhagenRibeiro12)). (Again for the [[Peierls bracket]], but the statement holds more generally.) These references and that this means a symplectic foliation by [[source]] terms was highlighted out by ([Khavkine 13](#Khavkine13)).

## On paths in a symplectic manifold

We describe here the [[off-shell]] Poisson bracket in the context of [[mechanics]], hence for [[mechanical systems]] with [[finite set|finite]]-[[dimension|dimensional]] [[phase space]]. The basic idea is that sketched in ([Marolf 93, section II](#Marolf93)), but we try to make it precise. Then we similarly look into the [[foliation]] by [[symplectic leaves]] as suggested by ([Khavkine 13](#Khavkine13)).

### The trajectory space of a symplectic manifold

Let $(X,\omega)$ be a [[symplectic manifold]]. We write 

$$
  \{-,-\} \;\colon\; C^\infty(X)\otimes C^\infty(X) \longrightarrow C^\infty(X)
$$

for the [[Poisson bracket]] induced by the [[symplectic form]] $\omega$, hence by the [[Poisson bivector]] $\pi \coloneqq \omega^{-1}$.

For notational simplicity we will restrict attention to the special case that 

$$
  X = \mathbb{R}^2 \simeq T^\ast \mathbb{R}
$$ 

with canonical [[coordinates]] 

$$
  q,p \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
$$ 

and symplectic form 

$$
  \omega = \mathbf{d}q \wedge \mathbf{d}p
  \,.
$$ 

The general case of the following discussion is a straightforward generalization of this, which is just notationally more inconvenient. 

Write $I \coloneqq [0,1]$ for the standard [[interval]] regarded as a [[smooth manifold]] [[manifold with boundary|with boundary]]. The [[mapping space]] 

$$
  P X \coloneqq [I, X]
$$

canonically exists as a [[smooth space]], but since $I$ is [[compact topological space|compact]] this structure canonically refines to that of a [[Fréchet manifold]] (see at _[[manifold structure of mapping spaces]]_). This implies that there is a good notion of [[tangent space]] $T P X$. The task now is to construct a certain [[Poisson bivector]] as a [[section]] $\pi \in \Gamma^{\wedge 2}(T P X)$.

Among the [[smooth functions]] on $P X$ are the [[evaluation maps]] 

$$
  ev \;\colon\; P X \times I = [I,X] \times I \stackrel{}{\longrightarrow} X
$$

whose components we denote, as usual, for $t \in I$ by

$$
  q(t) \coloneqq q \circ ev_t \;\colon\; P X \longrightarrow \mathbb{R}
$$

and

$$
  p(t) \coloneqq p \circ ev_t \;\colon\; P X \longrightarrow \mathbb{R}
  \,.
$$

Generally for $f \colon X \to \mathbb{R}$ any [[smooth function]], we write $f(t) \coloneqq f \circ ev_t \in C^\infty(P X)$. This defines an embedding

$$
  C^\infty(X) \times I \hookrightarrow C^\infty(P X)
  \,.
$$

Similarly we have 

$$
  \dot q(t) \;\colon\; P X \longrightarrow \mathbb{R}
$$

and

$$
  \dot q(t) \;\colon\; P X \longrightarrow \mathbb{R}
$$

obtained by [[differentiation]] of $t \mapsto q(t)$ and $t \mapsto p(t)$.

### Hamiltonian evolution

Let now 

$$
  H \;\colon\; X \times I \longrightarrow \mathbb{R}
$$ 

be a [[smooth function]], to be regarded as a time-dependent [[Hamiltonian]]. This induces a time-dependent function on trajectory space, which we denote by the same symbol

$$
  H
  \;\colon\;
  P X \times I
   \stackrel{(ev,id)}{\longrightarrow}
  X \times X
   \stackrel{H}{\longrightarrow}
  \mathbb{R}
  \,.
$$

Hence for $t \in I$ we write

$$
  H(t) 
  \;\colon\;
  P X \times \{t\}
  \stackrel{(ev, id)}{\longrightarrow}
  X \times \{t\}
  \stackrel{H}{\longrightarrow}
  \mathbb{R}
$$

for the function that assigns to a trajectors $(q(-),p(-)) \colon I \longrightarrow X$ its [[energy]] at (time) parameter value $t$.

Define then the [[Euler-Lagrange equation|Euler-Lagrange density]] induced by $H$ to be the functions

$$
  EL(t)
  \;\colon\;
  P X
  \longrightarrow 
  \mathbb{R}^2
$$

with components

$$
  EL(t)
  = 
  \left(
    \array{
      \dot q(t) - \frac{\partial H}{\partial p}(t)
      \\
      \dot p(t) + \frac{\partial H}{\partial p}(t)
    }
  \right)
  \,.
$$


The [[trajectories]] $\gamma \colon I \to X$ on which $EL(t)$ vanishes for all $t \in I$ are equivalently those 

* for which the [[tangent vector]] $\dot \gamma \in T_{\gamma}X$ is a [[Hamiltonian vector field|Hamiltonian vector]] for $H$;

* which satisfy [[Hamilton's equations]] [[equations of motion|of motion]] for $H$.

Since the [[differential equations]] $EL = 0$ have a unique solution for given initial data $(q(0), p(0))$, the evaluation map

$$
  \left\{
    \gamma \in P X | \forall_{t \in I}\; EL_\gamma(t) = 0 
  \right\}
  \stackrel{\gamma \mapsto \gamma(0)}{\longrightarrow}
  X
$$

is an [[equivalence]] (an [[isomorphism]] of [[smooth spaces]]).


### The off-shell Poisson bracket
 {#TheOffShellPoissonBracketOnSpaceOfPathsInSymplecticManifold}

Write 

$$
  Poly(P X) \hookrightarrow C^\infty(P X)
$$

for the [[subalgebra]] of [[smooth functions]] on [[path space]] which are

* [[polynomials]] 

* of [[integrals]] over $I$

* of the smooth functions in the image of $C^\infty(X) \times I \hookrightarrow C^\infty(P X)$

* and all their [[derivatives]] along $I$.

Define a [[bilinear function]]

$$
  \{-,-\}
  \;\colon\;
  Poly(P X) \otimes Poly(P X)
  \longrightarrow Poly(P X)
$$

as the unique function which is a [[derivation]] in both arguments and moreover is a solution to the [[differential equations]]

$$
  \frac{\partial}{\partial t_2}
  \left\{f(t_1), q(t_2)\right\}
  =
  \left\{
    f(t_1), \frac{\partial H}{\partial p}(t_2)
  \right\}
$$

$$
  \frac{\partial}{\partial t_2}
  \left\{f(t_1), p(t_2)\right\}
  =
  -
  \left\{
    f(t_1), \frac{\partial H}{\partial q}(t_2)
  \right\}
$$

subject to the initial conditions

$$
  \{f(t), q(t)\} = \{f,q\}
$$

$$
  \{f(t), p(t)\} = \{f,p\}
$$

for all $t \in I$, where on the right we have the original [[Poisson bracket]] on $X$.

This bracket directly inherits skew-symmetry and the [[Jacobi identity]] from the [[Poisson bracket]] of $(X, \omega)$, hence equips the [[vector space]] $Poly(P X)$ with the structure of a [[Lie bracket]]. Since it is by construction also a [[derivation]] of  $Poly(P X)$ as an [[associative algebra]], we have that 

$$
  \left(
    Poly\left(P X\right),
    \;
    \left\{
      -,-
    \right\}
  \right)
  \;\;\;
  \in P_1 Alg
$$

is a [[Poisson algebra]]. This is the "off-shell Poisson algebra" on the space of [[trajectories]] in $(X,\omega)$.


### The symplectic leaves

Observe that by construction of the off-shell Poisson bracket, 
specifically by the [[differential equations]] defining it, the
[[Euler-Lagrange equation|Euler-Lagrange function]] $EL$
generate a [[Poisson reduction|Poisson ideal]]. 

For instance 

$$
 \left(
  \array{
  \frac{\partial}{\partial t_2}
  \left\{f(t_1), q(t_2)\right\}
  &=&
  \left\{
    f(t_1), \frac{\partial H}{\partial p}(t_2)
  \right\}
  \\
  \frac{\partial}{\partial t_2}
  \left\{f(t_1), p(t_2)\right\}
  &=&
  -
  \left\{
    f(t_1), \frac{\partial H}{\partial q}(t_2)
  \right\}
  }
  \right)
  \;\;\;
  \Leftrightarrow
  \;\;\;
  \left(
    \left\{
      f(t_1), \;
      EL(t)
    \right\}
    =  
    0
  \right)
  \,.
$$

Moreover, since $\{EL(t) = 0\}$ are  [[equations of motion]] the [[Poisson reduction]] defined by this Poisson idea is the subspace of those [[trajectories]] which are solutions of [[Hamilton's equations]], hence the "on-shell trajectories".

As remarked above, the initial value map canonically identifies this on-shell trajectory space with the original [[phase space]] manifold $X$. Moreover, by the very construction of the off-shell Poisson bracket as being the original Poisson bracket at equal times, hence in particular at time $t = 0$, it follows that restricted to the [[zero locus]] $EL = 0$ the off-shell Poisson bracket becomes [[symplectic manifold|symplectic]].

All this clearly remains true with the function $EL$ replaced by the function $EL - J$, for  $J \in C^\infty(I)$ any function of the (time) parameter (since $\{J,-\} = 0$). Any such choice of $J$ hence defines a symplectic subspace 

$$
  \left\{
    \gamma \in P X
    \;|\;
    \forall_{t \in I}\; EL_\gamma(t) = J
  \right\}
$$

of the off-shell Poisson structure on trajectory space. Hence $\left(O X, \left\{-,-\right\}\right)$ has a [[foliation]] by [[symplectic leaves]] with the [[leaf space]] being the [[smooth space]] $C^\infty(I)$ of [[smooth functions]] on the interval. 

Notice that changing $EL \mapsto EL - J$ corresponds changing the time-dependent [[Hamiltonian]] $H$ as

$$
  H \mapsto H - J q
  \,.
$$

Such a term linear in the [[canonical coordinates]] (the [[field (physics)|fields]]) is a _[[source]] term_. (The [[action functionals]] with such [[source]] terms added serve as [[integrands]] of [[generating functions]] for [[correlators]] in [[statistical mechanics]] and in [[quantum mechanics]].)

### Boundary field theory interpretation
 {#BoundaryFieldTheoryInterpretation}

Hence in conclusion we find the following statement:

The [[trajectory]] space (history space) of a [[mechanical system]] carries a natural [[Poisson manifold|Poisson structure]] whose [[symplectic leaves]] are the subspaces of those trajectories which satisfy the [[equations of motion]] with a fixed [[source]] term and hence whose symplectic [[leaf space]] is the space of possible sources. 
 
Notice what becomes of this statement as we consider the the [[2d Chern-Simons theory]] induced by the off-shell Poisson bracket (the [[non-perturbative field theory|non-perturbative]] [[Poisson sigma-model]]) whose [[moduli stack]] of [[field (physics)|fields]] is the [[symplectic groupoid]] $SG\left(P X, \left\{-,-\right\}\right)$ induced by the Poisson structure. 

By the discussion at [[motivic quantization]] in the section _[The Poisson manifold at the boundary of the 2d Chern-Simons theory](motivic%20quantization#PoissonManifoldAtTheBoundaryOf2dChernSimonsTheory)_, the Poisson space $\left(P X, \left\{-,-\right\}\right)$ defines a  [[boundary field theory]] (in the sense of [[local prequantum field theory]]) for this [[2d Chern-Simons theory]], exhibited by a boundary [[correspondence]] of the form

$$
  \array{
    && P X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\xi} && SG\left(P X, \left\{-,-\right\}\right)
    \\
    & \searrow && \swarrow_{\mathrlap{\chi}}
    \\
    && \mathbf{B}^2 U(1)
    \\
    && \downarrow^{\mathrlap{\rho}}
    \\
    && KU Mod
  }
  \,.
$$

Notice that the [[symplectic groupoid]] is a version of the [[symplectic leaf|symplectic]] [[leaf space]] of the given [[Poisson manifold]] (its [[0-truncation]] is exactly the leaf space). Hence in the case of the off-shell Poisson bracket, the [[symplectic groupoid]] is the space of _[[source field|sources]]_ of a mechanical system. At the same time it is the [[moduli space]] of [[field (physics)|fields]] of the [[2d Chern-Simons theory]] of which the mechanical system is the [[boundary field theory]].
Hence the [[field (physics)|fields]] of the [[bulk field theory]] are identified with the [[sources]] of the [[boundary field theory]]. Hence conceptually the above boundary correspondence diagram is of the following form

$$
  \array{
    && Fields
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{} && Sources
    \\
    & \searrow && \swarrow_{\mathrlap{}}
    \\
    && Phases
  }
  \,.
$$


Such a relation 

|  [[bulk field theory]]  |  [[boundary field theory]]  |
|---|----|
| [[field (physics)|field]] | [[source]] |

between bulk fields and boundary sources is the characteristic feature of what is called the _[[holographic principle]]_ in its realization as the [[AdS-CFT correspondence]].


## References

The off-shell extension of the [[Peierls bracket]] is observed in section II of

* [[Don Marolf]],  _Poisson Brackets on the Space of Histories_ Annals of Physics Volume 236, Issue 2, December 1994, Pages 374-391 ([arXiv:hep-th/9308141](http://arxiv.org/abs/hep-th/9308141))
  {#Marolf93}

The observation that the off-shell bracket has a symplectic foliation by the level sets of the Euler-Lagrange functions appears on the top of p. 4 of

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Pedro Ribeiro]], _Algebraic Structure of Classical Field Theory I: Kinematics and Linearized Dynamics for Real Scalar Fields_ ([arXiv:1209.2148](http://arxiv.org/abs/1209.2148))
  {#BrunettiFredenhagenRibeiro12}

All this and the interpretation of the resulting symplectoc foliation as a foliation by source terms has been highlighted by

* [[Igor Khavkine]], personal communication
  {#Khavkine13}

[[!redirects off-shell Poisson brackets]]
