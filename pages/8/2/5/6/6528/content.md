
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

Let $(\Sigma,g_\Sigma)$ be a [[compact space|compact]] 3-[[dimensional]] [[Riemannian manifold]] . 

Consider in [[Yang-Mills theory]] on the [[product]] space $X = \Sigma \times \mathbb{R}$ (with metric the product metric of $g$ with the canonical metric  on $\mathbb{R}$) field configurations $\nabla$ with finite Yang-Mills action 

$$
  S_{YM}(\nabla) = \int_{\Sigma \times \mathbb{R}} F_\nabla \wedge \star F_\nabla
  \lt \infty
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

This equation may be interpreted as characterizing the [[gradient flow]] of the [[Chern-Simons action functional]]

$$
  S_{CS} : \Omega^1(\Sigma, \mathfrak{g}) \to \mathbb{R}
$$

$$
  A \mapsto \int_\Sigma CS(A)
$$

with respect to $g_\Sigma$, because the [[variational calculus|variation]] of the Chern-Simons action is

$$
  \delta S_{CS}(A) = \int_\Sigma \langle \delta A \wedge F_A\rangle
$$

(see [[Chern-Simons theory]] for details).

Since (therefore) flat connections are the [[critical loci]] of $S_{CS}$ we find that a finite-action Yang-Mills instanton on $\Sigma \times \mathbb{R}$ is a [[gradient flow]] between two "Chern-Simons theory vacua".

Often this is interpreted as saying that "a Yang-Mills instanton describes the [[tunneling]] between two Chern-Simons vacua".


## Related concepts

* [[instanton Floer homology]]

## References

Monographs with the standard material include

* [[Dan Freed]], [[Karen Uhlenbeck]], _Instantons and four-manifolds_, Springer-Verlag, (1991) 

* [[Robbert Dijkgraaf]], _Topological gauge theories and group cohomology_ ([ps](staff.science.uva.nl/~rhd/papers/group.ps))

In 

* Henrique N. S&#180;a Earp, _Instantons on $G_2$&#8722;manifolds_ PhD thesis (2009) ([pdf](http://www.ime.unicamp.br/~hqsaearp/index_files/HENRIQUE_SA_EARP_THESIS_UPDATED.PDF))

is a discussion of Yang-Mills instantons on a 7-dimensional [[manifold with special holonomy]].
[[!redirects Yang-Mills instantons]]