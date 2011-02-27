
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

**Variational calculus** is a version of [[differential calculus]] that deals with local extremization of nonlinear [[functionals]]: extremization of differentiable functions on non-finite dimensional spaces such as [[mapping space]]s. 

Specifically, it studies the _critical points_ , i.e. the points where the first variational derivative of a functional vanishes, for functionals on spaces of [[section]]s of [[jet bundle]]s. The kinds of equations specifying these critical points are [[Euler-Lagrange equation]]s.

This applies to, and is largely motivated from, the study of [[action functional]]s in [[physics]]. In [[classical physics]] the critical points of a specified action functional on the space of field configurations encode the physically observable configurations.

There are strong [[cohomology|cohomological]] tools for studying variational calculus, such as the [[variational bicomplex]] and [[BV-BRST formalism]].


## Definition

### In the category of diffeological spaces


We discuss variational calculus in the [[category]] $DiffSp$ of [[diffeological space]]. Discussion along these lines appears also in ([Iglesias-Zemmour, section 1.56](#PIZ)) and ([Paugam10, section 2.4](#Paugam)). 

We shall find it convenient to consider $DiffSp$ under its canonical embedding

$$
  DiffSp \hookrightarrow Sh(CartSp) \hookrightarrow Smooth \infty Grpd
$$

first as the [[quasitopos]] of [[concrete sheaves]] into the full [[cohesive topos]] of all [[sheaves]] on [[CartSp]]$_{smooth}$, and then further into the [[cohesive (∞,1)-topos]] of [[(∞,1)-sheaves]] on [[CartSp]]. This allows the following natural definition.


+-- {: .num_defn}
###### Definition

Let $X \in DiffSp$ be a [[diffeological space]] and $f : X \to \mathbb{R}$ be a morphism in $DiffSp$. The **differential** of $f$ is the composite morphism in [[Smooth∞Grpd]]

$$
  d f : 
   X 
    \stackrel{f}{\to} 
   \mathbb{R}
    \stackrel{\theta}{\to} 
   \mathbf{\flat}_{dR}\mathbf{B}\mathbb{R}
$$

with the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature form</a> on $\mathbb{R}$. 

=--

+-- {: .num_note}
###### Observation

By <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CanonicalFormOnLieGroup">this theorem</a> this is equivalently postcomposition with the morphism $\theta : \mathbb{R} \to \Omega^1_{cl}(-)$ in $Sh(CartSp)$ that acts on $U \in CartSp$ by sending a [[smooth function]] $(g : U \to \mathbb{R}) \in \mathbb{R}(U)$ to its [[de Rham complex|de Rham]] [[differential]] $d g \in \Omega^1_{cl}(U)$

$$
  \theta_U : g \in C^\infty(U,\mathbb{R})   
    \mapsto 
   d g \in \Omega^1_{cl}(U)
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

The **critical locus** $P_f$ of $f : X \to \mathbb{R}$ is the [[fiber]] of $d f$ over $0$, hence the [[pullback]]

$$
  \array{
    P_f &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{0}}
    \\
    X &\stackrel{d f}{\to}& \mathbf{\flat}_{dR} \mathbf{B}\mathbb{R}
  }
$$

in $Sh(CartSp)$.

=--

+-- {: .num_defn}
###### Terminology


If $X$ is the [[configuration space]] of a system of [[physics]] and $ f : X \to \mathbb{R}$ an [[action functional]], then $P_f$ is called the [[covariant phase space]] of the system.

=--
## Examples

Let $X$ be a [[Riemannian manifold]], $\Sigma = [0,1]$ the standard interval and write $[\Sigma,X]_{a,b} \hookrightarrow [\Sigma,X]$ for the subobject of the [[diffeological space]] of smooth functions $\gamma : \Sigma \to X$ on those for which $\gamma(0) = a$ and $\gamma(1) = b$ for $a,b \in X$ 

Let then $L : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ be any smooth function and

$$
  S_{a,b}: [\Sigma,X]_{a,b} \to \mathbb{R}
$$

be the standard [[action functional]] associated to $L$ thought of as a [[Lagrangian]]: the map that sends a family $\gamma : U \to P X$ of paths to the family

$$
  u \mapsto \int_{\Sigma} L(\gamma_u, \gamma'_u) d t
  \,.
$$

Then 

$$
  d S : \in \Omega^1_{a,b}([\Sigma,X]_{a,b})
$$

is a smooth closed 1-form that vanishes on all the solutions of the [[Euler-Lagrange equation]] for $L$.

See also ([Iglesias-Zemmour, page 65](#PIZ)).


## Referenes

Fundamental texts of variational calculus include

* Ian Anderson, _The variational bicomplex_ ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))

* Peter Olver, _Applications of Lie groups to differential equations_, Springer; _Equivalence, invariants, and symmetry_, Cambridge Univ. Press 1995.

* Olga Krupkov&#225;, _The geometry of ordinary variational equations_, Springer 1997, 251 p.

A long list of discussion of examples of variational problems arising in the [[classical mechanics]] and [[quantum field theory]] is collected in

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))

The formulation of variational calculus in terms of [[diffeological space]]s is mentioned for instance in section 1.65 of

* [[Patrick Iglesias-Zemmour]], _Diffeology_ ([pdf](http://math.huji.ac.il/~piz/documents/Diffeology.pdf#page=64))
{#PIZ}

and in section 2.4 of 

* [[Frédéric Paugam]], _Histories and observables in covariant field theory_ ([arXiv:1010.3210](http://arxiv.org/abs/1010.3210))
{#Paugam}
[[!redirects calculus of variations]]