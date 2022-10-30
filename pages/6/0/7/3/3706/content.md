
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A _Lagrangian submanifold_ of a [[symplectic manifold]] is a submanifold which is a maximal [[isotropic submanifold]], hence a [[submanifold]] on which the [[symplectic form]] vanishes, and which is maximal with this property.


In the archetypical example of an even dimensional [[Cartesian space]] $X = \mathbb{R}^{2n}$ equipped with its canonical symplectic form  $\omega = \sum_{i = 1}^n d q_i \wedge d p^i$, standard Lagrangian submanifolds are the submanifolds $\mathbb{R}^n \hookrightarrow \mathbb{R}^{2n}$ of fixed values of the $\{q_i\}_{i = 1}^n$ [[coordinates]]. Indeed _locally_, every Lagrangian submanifold looks like this. 

Lagrangian submanifolds are of central importance in [[symplectic geometry]] where they constitute [[leaves]] of [[real polarizations]] and are closely related to [[quantum states]]: 

If one thinks of a [[symplectic manifold]] as a [[phase space]] of a [[physical system]], then a Lagrangian submanifold may be thought of (locally) as the space of "all [[canonical momenta]] (= parameterization of a [[leaf]]) at fixed [[canonical coordinate]] (= parameterization of [[leaf space]])". 

A Lagrangian submanifold equipped with a [[half-density]] is a model for a [[state]] of the physical system in [[semiclassical approximation]] (see e.g. [Bates-Weinstein, p. 14](#BatesWeinstein)). A [[quantum state]] given by a [[wave function]] (see there) is a refinement of this concept.



## Definition

+-- {: .num_defn }
###### Definition

A (**Lagrangean** or) **lagrangian submanifold** of a [[symplectic manifold]] $(X,\omega)$ is a [[submanifold]] $L \hookrightarrow X$ such that the following equivalent conditions hold

* at each point $\ell \in L the $[[tangent space]] $T_\ell L \hookrightarrow T_\ell X$ is a [[Lagrangian subspace]] (hence a simultanously [[isotropic subspace]] and [[cosisotropic subspace]]) of $T_\ell X$ equiiped with the [[symplectic form]] $\omega_x$;

* $L \hookrightarrow X$ is a maximal [[isotropic submanifold]].

=--


+-- {: .num_remark #LambdaStructures}
###### Remark

More generally one can consider Lagrangian submanifolds of symplectic structures in [[higher geometry]], such as [[symplectic Lie n-algebroids]] equipped with their canonical [[invariant polynomials]], thought of as [[dg-manifolds]] (via their [[Chevalley-Eilenberg algebra]]) and equipped with graded symplectic forms. Lagrangian dg-submanifolds of such symplectic dg-manifolds have been called **$\Lambda$-structures** in ([&#352;evera, section 4](#Severa)).

=--

## Examples in higher differential geometry

We discuss classes of examples of Lagrangian dg-submanifolds, remark \ref{LambdaStructures}, of [[symplectic Lie n-algebroids]].

### Of a Poisson Lie algebroid
 {#OfAPoissonLieAlgebroid}

A [[Poisson Lie algebroid]] $\mathfrak{P}$ is a [[symplectic Lie n-algebroid]] for $n = 1$. Regarding its [[Chevalley-Eilenberg algebra]] as the algebra of functions on a [[dg-manifold]], that dg-manifold carries a graded [[symplectic form]] $\omega$. One can then say

+-- {: .num_defn #ForPoissonLieAlgebroidyByLagrangianFoliation}
###### Definition

A dg-[[Lagrangian submanifold]] of $(\mathfrak{P}, \omega)$ is a Lagrangian dg-submanifold, also called a **$\Lambda$-structure**. ([&#352;evera, section 4](#Severa)).

=--

+-- {: .num_remark}
###### Remark

A [[foliation]] by such [[leaves]] is a Lagrangian _[[foliation of a Lie algebroid]]_.

=--

+-- {: .num_prop}
###### Proposition

For $(X, \pi)$ the [[Poisson manifold]] underlying a [[Poisson Lie algebroid]] $(\mathfrak{P}, \omega)$, a dg-Lagrangian submanifold of $(\mathfrak{P}, \omega)$ corresponds to a [[coisotropic submanifold]] of $(X, \pi)$.

=--

([&#352;evera, section 4](#Severa))

+-- {: .proof}
###### Proof

As a [[vector bundle]] with bracket structure, the [[Poisson Lie algebroid]] $\mathfrak{P}$ is

$$
  \array{
    T^* X &&\stackrel{\pi}{\to}&& T X
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

where the horizontal morphism is given by contraction/pairing with the [[Poisson tensor]].

It is sufficient to consider this locally over a [[coordinate chart]] and hence we set without essential restriction of generality 
$X = \mathbb{R}^n$ with the [[invariant polynomial]]/graded [[symplectic form]] on $CE(\mathfrak{P})$ being

$$
  \omega = \mathbf{d} x^i \wedge \mathbf{d} p_i
  \,,
$$

where the $\{q_i\}_{i = 1}^n$ are the canonical [[coordinates]] on $\mathbb{R}^n$ and where the $\{p_i\}$ are the canonical coordinates on $T^*_x \mathbb{R}^n \simeq \mathbb{R}^n$, regarded as being in degree 1.

Consider then a sub-Lie algebroid of $\mathfrak{P}$ over a [[submanifold]] $S \hookrightarrow \mathbb{R}^n$. That the corresponding subbundle 

$$
  \array{
    E &\hookrightarrow& T^* X
    \\
    \downarrow && \downarrow
    \\
    S &\hookrightarrow & X
  }
$$

over $S$ is [[Lagrangian subspace|Lagrangian]] with respect to the above $\omega$ means that $E$ consists of precisely those [[cotangent vectors]] to $X$ which vanish when evaluated on [[tangent vectors]] of $S$. Hence 

$$
  E = N^* S
$$

is the [[conormal bundle]] to $S \hookrightarrow X$. The inclusion $N^* S \hookrightarrow T^*_S X$ of vector bundles is an inclusion of [[Lie algebroids]] over $S$ precisely if the [[anchor map]] restricts to an anchor on $S$, hence that contraction with the Poisson tensor restricted to conormal vectors  of $S$ lands in tangent vectors of $S$:

$$
 \pi(N^* S) \subset T S
  \,.
$$

This is the standard definition for what it means for $S$ to be a [[coisotropic submanifold]].

=--

+-- {: .num_remark}
###### Remark

The dg-Lagrangian submanifolds also correspond to [[branes]] in the [[Poisson sigma-model]] (see there) on $(\mathfrak{P}, \omega)$. 

=--



### Of a Courant Lie 2-algebroid
 {#OfACourantLie2Algebroid}

A [[Courant Lie algebroid]] $\mathfrak{C}$ is a [[symplectic Lie n-algebroid]] for $n = 2$. Regarding its [[Chevalley-Eilenberg algebra]] as the algebra of functions on a [[dg-manifold]], that dg-manifold carries a graded [[symplectic form]] $\omega$. One can then say

+-- {: .num_defn #ForPoissonLieAlgebroidyByLagrangianFoliation}
###### Definition

A dg-[[Lagrangian submanifold]] of $(\mathfrak{C}, \omega)$ is also called a **$\Lambda$-structure**. ([&#352;evera, section 4](#Severa)).

Hence we might say **real polarization** of $(\mathfrak{C}, \omega)$ is a foliation by dg-Lagrangian submanifolds.

=--

+-- {: .num_prop}
###### Proposition

The dg-Lagrangian submanifolds of a Courant Lie 2-algebroid $(\mathfrak{C}, \omega)$ correspond to [[Dirac structures]] on $(\mathfrak{C}, \omega)$.

=--

([&#352;evera, section 4](#Severa))

## Related concepts

* [[Lagrangian correspondence]], [[prequantized Lagrangian correspondence]]

* [[Lagrangian cobordism]]

* [[Lagrangian subspace]]

* [[isotropic submanifold]]

* [[polarization]]

* [[Legendrean submanifold]]

[[!include (co)isotropic subspaces - table]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

The concept of lagrangian submanifold has been defined/named by Maslov. 

An introduction with an eye towards [[geometric quantization]] is for instance in
 
* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)
 {#BatesWeinstein}

(pages 10 and onward and then section 4.3).

Lagrangian submanfolds of symplectic [[dg-manifolds]] are called "$\Lambda$-structures" in 

* [[Pavol Ševera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:0105080](http://arxiv.org/abs/math/0105080))
 {#Severa}


[[!redirects lagrangian submanifold]]
[[!redirects lagrangian submanifolds]]
[[!redirects Lagrangian submanifold]]
[[!redirects Lagrangian submanifolds]]
[[!redirects lagrangean submanifold]]
[[!redirects lagrangean submanifolds]]
[[!redirects Lagrangean submanifold]]
[[!redirects Lagrangean submanifolds]]

[[!redirects lagrangian manifold]]
[[!redirects lagrangian manifolds]]
[[!redirects Lagrangian manifold]]
[[!redirects Lagrangian manifolds]]
[[!redirects lagrangean manifold]]
[[!redirects lagrangean manifolds]]
[[!redirects Lagrangean manifold]]
[[!redirects Lagrangean manifolds]]


[[!redirects Lagrangian dg-submanifold]]
[[!redirects Lagrangian dg-submanifolds]]
[[!redirects dg-Lagrangian submanifold]]
[[!redirects dg-Lagrangian submanifolds]]
