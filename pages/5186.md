
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _relativistic particle_ in [[physics]] is a model for the dynamics of a single [[brane|particle]] that is propagating in a [[spacetime]] subject to [[force]]s such as [[gravity]] and (if it is charged) the [[electromagnetic field]].

The generalization to [[supergeometry]] is the [[superparticle]].

## Definition

The **relativistic particle** is described by the [[sigma-model]] whose

* [[target space]] is a [[spacetime]] $(X,g)$,

  where the [[pseudo-Riemannian metric]] $g$ -- or rather the [[Levi-Civita connection]] $\nabla$ that it induces on the [[tangent bundle]] $T X$ -- encodes the background field of [[gravity]] acting on the particle;

* [[worldvolume]] is the [[real line]] $\Sigma = \mathbb{R}$ or the [[circle]] $\Sigma = S^1$, the _[[worldline]]_;

* [[background gauge field]] is [[connection on a bundle|connection]] $\nabla$ on a [[circle group]]-[[principal bundle]] over $X$, encoding a field of [[electromagnetism]] acting by [[Lorentz force]] on the particle;

* [[configuration space]] is the [[quotient]]

  $$
    Conf := C^\infty(\Sigma, X)// Diff(\Sigma)
  $$

  of the space (naturally a [[diffeological space]]) of [[smooth function]]s $\Sigma \to X$ ("trajectories"); 

* the exponentiated [[action functional]] is for given parameters $m \in \mathbb{R}$ (the particle's [[mass]]) and $q \in \mathbb{R}$ (the particle's [[charge]])

  $$
    \exp(i S(-))
     : 
   [\gamma] 
       \mapsto
     \exp(
     i m \int dvol(\gamma^* g))
     \;\;
     hol(\nabla,\gamma)
     \,,
  $$

  where the first terms is the integral of the [[volume form]] of the pullback of the background metric, and where the second term is the [[holonomy]] of the [[circle n-bundle with connection|circle bundle with connection]] around $\gamma$. In the case that the underlying [[circle]]-[[principal bundle]] is trivial, so that the [[connection on a bundle|connection]] is given by a [[differential forms|1-form]] $A \in \Omega^1(X)$, the [[action functional]] is
   
  $$
    \begin{aligned}
     S : 
     [\gamma]
      \mapsto
      & 
      S_{kin}([\gamma]) + S_{gauge}([\gamma])
      \\
      & =
      \int m dvol(\gamma^* g)
      +
      \int q \gamma^* A
    \end{aligned}
      \,,
  $$

  where the first summand is the _kinetic action_ and the second the _gauge interaction_ term.

The above action functional is called the [[Nambu-Goto action]] in dimension 1. Alternatively (and mandatorily for vanishing [[mass]] parameter), the kinetic action is replaced by the corresponding [[Polyakov action]].


## Properties

### Covariant phase space

We determine the [[covariant phase space]] of the theory: the space of solutions to the [[equations of motion]] and the [[presymplectic structure]].


We assume for simplicity that the class of the background circle bundle is trivial, so that the connection is equivalently given by a 1-form $A \in \Omega^1(X)$. Write $F = d A$ for its [[curvature]] 2-form: the [[field strength]] of the [[electromagnetic field]].

+-- {: .num_prop}
###### Proposition

The [[variational calculus|variation]] of the gauge interaction term is

$$
  \delta \int_\Sigma \gamma^* A
  =
  - \int_\Sigma F(\dot \gamma, \delta \gamma)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $\mathbb{R}^d \stackrel{\simeq}{\to} U \hookrightarrow X$ be a local [[coordinate patch]] with coordinates $\{x^\mu\}$ and assume that $\gamma$ takes values in $U$ (or at least that its variation is supported there, which we can assume without restriction of generality).
Then the variation is given by
is

$$
  \begin{aligned}
    \delta \int_\Sigma \gamma^* A
    & =
     \delta \int_\Sigma A_\mu(\gamma) \dot \gamma^\mu d \tau
    \\
    & = \int_\Sigma 
        \left(
           (\partial_{\nu} A_\mu)(\gamma) \dot \gamma^\mu
           -
           \frac{d}{d\tau} (A_\nu(\gamma))
        \right)
        \delta \gamma^\nu
        d \tau
    \\
    & = \int_\Sigma
        \left(
           (\partial_{\nu} A_\mu)(\gamma) \dot \gamma^\mu
           -
           (\partial_\mu A_\nu)(\gamma)) \dot \gamma^\mu
        \right)
        \delta \gamma^\nu  
        d\tau
  \end{aligned}
  \,.
$$

=--


The variation of the kinetic terms is slightly subtle due to the square root in 

$$
  dvol(\gamma^* g) = \sqrt{g(\dot \gamma, \dot \gamma)} d\tau
  \,.
$$

To deal with this, we first look at variations of trajectories in a small region where $g(\dot \gamma, \dot \gamma)$ is non-zero. For such we can always find a [[diffeomorphism]] $\Sigma \stackrel{\simeq }{\to} \Sigma$ such that this term is constantly $= 1$ in this region (recall that configurations are diffeomorphism classes of smooth [[curve]]s, so we may apply such a diffeomorphism at will to compute the variation). 

+-- {: .num_prop}
###### Proposition

With the above choice of diffeomorphism gauge, the equations of motion are

$$
  g(\nabla_{\dot \gamma} \dot \gamma / {\vert \dot \gamma}\vert ,-)  = \iota_{\dot \gamma} F
  \,,
$$

where $\nabla$ is the [[covariant derivative]] with respect to the [[Levi-Civita connection]] of the metric $g$.

=--

+-- {: .proof}
###### Proof


Computing as before in local coordinates and parameterization such that $g(\dot \gamma, \dot \gamma) = 1$, the variation of the kinetic terms is

$$
  \begin{aligned}   
    \delta \int_\Sigma dvol(\gamma^* g)
     & =
     \delta \int_\Sigma \sqrt{g(\dot \gamma, \dot \gamma)} d\tau
     \\
     & = 
     \int_\Sigma 
      \left(
          \frac{1}{2}(\partial_\mu g_{\nu \lambda}) \dot \gamma^\nu \dot \gamma^\lambda 
          -
          \frac{d}{d\tau}(g_{\mu \nu} \dot \gamma^\nu) 
      \right)
      \delta \gamma^\mu
d \tau
    \\
    & =
     \int_\Sigma 
      \left(
          \frac{1}{2}(\partial_\mu g_{\nu \lambda}) \dot \gamma^\nu \dot \gamma^\lambda 
          -
          2 (g_{\mu\nu}\ddot \gamma^\nu + 
     (\partial_\lambda g_{\mu\nu}) \dot \gamma^\nu \dot \gamma^\lambda)
      \right)
      \delta \gamma^\mu
      d \tau
   \\
    & = 
    - \int_\Sigma
     g_{\mu \mu}(
      \ddot \gamma^\nu + \Gamma^\nu{}_{\alpha \beta} \dot \gamma^\alpha \dot \gamma^\beta
    )
   \delta \gamma^\mu
   \\
    & = 
    - \int_\Sigma
     g_{\mu \mu}(
      \nabla_{\dot \gamma} \dot \gamma^\nu
    )
   \delta \gamma^\mu
   \\
   & = -\int_\Sigma g(\nabla_{\dot \gamma} \dot \gamma, \delta \gamma)
  \end{aligned}
  \,.
$$

(Here $\Gamma^\cdot{}_{\cdot \cdot}$ are the [[Christoffel symbols]].)

This gives the equations of motion as claimed. 

=--

+-- {: .num_remark}
###### Remark

The [[norm]] of the tangent vector along a physical trajectory is preserved:

$$
  \begin{aligned}
    \frac{d}{d \tau} \sqrt{g(\dot \gamma, \dot \gamma)}
     & \propto
     2 \frac{d}{d \tau} g(\nabla_{\dot \gamma} \dot \gamma, \dot \gamma) 
     \\
    & \propto 
     F(\dot \gamma, \dot \gamma)
     \\
     & 0
  \end{aligned}
  \,.
$$

Therefore if the assumption $g(\dot \gamma, \dot \gamma) \neq 0$ is satisfied at one instant, is is so everywhere along the curve. 

=--

+-- {: .num_remark}
###### Remark

For vanishing [[background gauge field]] strength, $F = 0$, the equations of motion 

$$
  \nabla_{\dot \gamma} \dot \gamma = 0
$$

express the [[parallel transport]] of the tangent vector along a physical trajectory. This identifies these trajectories with the [[geodesics]] of $X$.

=--

## Related concepts

* [[sigma model]], [[brane]]

  * [[particle]], 

    **relativistic particle**, [[non-relativistic particle]],

    [[spinning particle]], [[superparticle]]


  * [[string]], [[spinning string]], [[superstring]]

  * [[membrane]]

* [[relativistic field theory]]
 
## References

* Giulio Ruffini, _Four approaches to quantization of the relativistic particle_ ([arXiv:gr-qc/9806058](http://arxiv.org/abs/gr-qc/9806058))

Discussion in terms of [[BV-formalism]] includes

* Jean M. L. Fisch and [[Marc Henneaux]], _Antibracket&#8212;antifield formalism for constrained hamiltonian systems_ ([doi](http://dx.doi.org/10.1016/0370-2693%2889%2990292-X))

* [[Alberto Cattaneo]], Michele Schiavina, _On time_ ([arXiv:1607.02412](http://arxiv.org/abs/1607.02412))

See also

* Benjamin Koch, Enrique Muñoz, _Path integral of the relativistic point particle in Minkowski space_ ([arXiv:2012.15242](https://arxiv.org/abs/2012.15242))



[[!redirects relativistic particles]]

[[!redirects quantum relativistic particle]]
[[!redirects quantum relativistic particles]]
