
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $\infty$-Chern-Weil theory
+-- {: .hide}
[[!include infinity-Chern-Weil theory - contents]]
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

In [[Yang-Mills theory]] an _[[instanton]]_ is a field configuration with non-vanishing second [[Chern class]] that minimizes the Yang-Mills energy.


## Definition

Let $(X,g)$ be a [[compact space|compact]] [[Riemannian manifold]] of [[dimension]] 4. Let $G$ be a compact [[Lie group]].

A [[configuration space|field configuration]] of $G$-[[Yang-Mills theory]] on $(X,g)$ is a $G$-[[principal bundle]] $P \to X$ with [[connection on a bundle|connection]] $\nabla$.

For $G = SU(n)$ the [[special unitary group]], there is canonically an [[associated bundle|associated]] complex [[vector bundle]] $E = P \times_G \mathbb{C}^n$.

Write $F_\nabla \in \Omega^2(X,End(E))$ for the [[curvature]] [[differential form|2-form]] of $\nabla$. 

We say that $\nabla$ is an **instanton configuration** if 

$$
  \star F_\nabla = - F_\nabla
  \,,
$$

where $\star : \Omega^k(X) \to \Omega^{4-k}(X)$ is the [[Hodge star operator]] induced by the [[Riemannian metric]] $g$.

The second [[Chern class]] of $P$, which by the [[Chern-Weil homomorphism]] is given by

$$
 c_2(E) = \int_X Tr(F_\nabla \wedge F_\nabla)
  =
  k
  \in H^4(X, \mathbb{Z})
$$

is called the **instanton number** of $\nabla$.

## Properties

### As gradient flows between flat connections.

We discuss how Yang-Mills instantons may be understood a trajectories of the [[gradient flow]] of the [[Chern-Simons theory]] [[action functional]].

Let $(\Sigma,g_\Sigma)$ be a [[compact space|compact]] 3-[[dimensional]] [[Riemannian manifold]] . 

Let the [[cartesian product]]

$$
  X = \Sigma \times \mathbb{R}
$$ 

of $\Sigma$ with the [[real line]] be equipped with the product metric of $g$ with the canonical metric  on $\mathbb{R}$. 


Consider field configurations $\nabla$ of [[Yang-Mills theory]] over $\Sigma \times \mathbb{R}$ with finite Yang-Mills action 

$$
  S_{YM}(\nabla) = \int_{\Sigma \times \mathbb{R}} F_\nabla \wedge \star F_\nabla
  \,\,\lt  \infty
  \,.
$$

These must be such that there is $t_1 \lt t_2 \in \mathbb{R}$ such that $F_\nabla(t \lt t_1) = 0$ and $F_\nabla(T \gt t_2) = 0$, hence these must be solutions interpolating between two [[curvature|flat]] connections.

Observe that on a [[coordinate patch]] $U\times \mathbb{R} \subset \Sigma \times \mathbb{R}$ where $\nabla$ is given by a [[Lie algebra valued 1-form]] $A \in \Omega^1(U\times \mathbb{R}, \mathfrak{g})$ we can always find a [[gauge transformation]] such that $A_{\partial_t} = 0$ ("[[temporal gauge]]"). In this gauge the self-duality condition on a Yang-Mills instanton 

$$
  F_\nabla = - \star F_\nabla
$$

reads equivalently

$$
  \frac{d}{d t} A = -\star_{g_{\Sigma}} F_A
  \,\,\,
  \in 
  \Omega^1(\Sigma, \mathfrak{g})
  \,.
$$

+-- {: .num_defn #HodgeInnerProduct}
###### Definition

On the linear [[configuration space]] $\Omega^1(U, \mathfrak{g})$ of [[Lie algebra valued forms]] on $U$ define the [[Hodge inner product]] [[metric]]

$$
  G(\alpha, \beta) := \int_{U} \langle \alpha \wedge \star \beta \rangle
  \,,
$$

where $\langle-,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$ is the [[Killing form]] [[invariant polynomial]] on the [[Lie algebra]] $\mathfrak{g}$.

=--

+-- {: .num_prop}
###### Proposition

The instanton equation 

$$
  \frac{d}{d t} A = 
  -\star_{g_{\Sigma}} F_A
$$

is the equation characterizing the [[gradient flow]] of the [[Chern-Simons action functional]]

$$
  S_{CS} : \Omega^1(\Sigma, \mathfrak{g}) \to \mathbb{R}
$$

$$
  A \mapsto \int_\Sigma CS(A)
$$

with respect to the [Hodge inner product metric](#HodgeInnerProduct) on $\Omega^1(\Sigma,\mathfrak{g})$.

=--

+-- {: .proof}
###### Proof

The [[variational calculus|variation]] of the Chern-Simons action is

$$
  \delta S_{CS}(A) = \int_\Sigma \langle \delta A \wedge F_A\rangle
$$

(see [[Chern-Simons theory]] for details).

In other words, we have the 1-form on $\Omega^1(\Sigma,\mathfrak{g})$:

$$
  \delta S_{CS}(-)_A
  = 
  \int_\Sigma \langle - \wedge F_A \rangle
  \,.
$$

The corresponding [[gradient vector field]]

$$
  \nabla S_{CS}
   :=
  G^{-1} \delta S_{CS}
$$

is uniquely defined by the equation

$$
  \begin{aligned}
    \delta S_{CS}(-) 
     & = G(-,\nabla S_{CS})
    \\
    \int_\Sigma \langle - , \star \nabla S_{CS}\rangle
  \end{aligned}
  \,.
$$

With the formula (see [[Hodge star operator]])

$$
  \star \stat A = (-1)^{1(3+1)} A = A
$$

we find therefore

$$
  \nabla S_{CS} = \star_g F_A
  \,.
$$

Hence the [[gradient flow]] equation

$$
  \frac{d}{d t} A + \nabla S_{CS}_A = 0
$$

is indeed

$$
  \frac{d}{d t} A =  - \star_g F_A
  \,.
$$


=--


Since [[curvature|flat]] connections are the [[critical loci]] of $S_{CS}$ this says that a finite-action Yang-Mills instanton on $\Sigma \times \mathbb{R}$ is a gradient flow trajectory between two _Chern-Simons theory [[vacuum|vacua]]_ .

Often this is interpreted as saying that "a Yang-Mills instanton describes the [[tunneling]] between two Chern-Simons vacua".


## Related concepts

* [[instanton Floer homology]]

## References

Monographs with the standard material include

* [[Dan Freed]], [[Karen Uhlenbeck]], _Instantons and four-manifolds_, Springer-Verlag, (1991) 

* [[Robbert Dijkgraaf]], _Topological gauge theories and group cohomology_ ([ps](staff.science.uva.nl/~rhd/papers/group.ps))

In 

* Henrique N. S&#225; Earp, _Instantons on $G_2$&#8722;manifolds_ PhD thesis (2009) ([pdf](http://www.ime.unicamp.br/~hqsaearp/index_files/HENRIQUE_SA_EARP_THESIS_UPDATED.PDF))

is a discussion of Yang-Mills instantons on a 7-dimensional [[manifold with special holonomy]].
[[!redirects Yang-Mills instantons]]