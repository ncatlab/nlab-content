
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

In $SU(n)$-[[Yang-Mills theory]] an _[[instanton]]_ is a field configuration with non-vanishing second [[Chern class]] that minimizes the Yang-Mills energy.


## Definition

Let $(X,g)$ be a [[compact space|compact]] [[Riemannian manifold]] of [[dimension]] 4. Let $G$ be a compact [[Lie group]].

A [[configuration space|field configuration]] of $G$-[[Yang-Mills theory]] on $(X,g)$ is a $G$-[[principal bundle]] $P \to X$ with [[connection on a bundle|connection]] $\nabla$.

For $G = SU(n)$ the [[special unitary group]], there is canonically an [[associated bundle|associated]] complex [[vector bundle]] $E = P \times_G \mathbb{C}^n$.

Write $F_\nabla \in \Omega^2(X,End(E))$ for the [[curvature]] [[differential form|2-form]] of $\nabla$. 

One says that $\nabla$ is an **instanton configuration** if $F_\nabla$ is [[Hodge star operator|Hodge]]-self dual

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

is called the **instanton number** or the **instanton sector** of $\nabla$.

Notice that therefore any connection, even if not self-dual, is in some instanton sector, as its underlying bundle has some second Chern class, meaning that it can be obtained from shifting a self-dual connection. The self-dual connections are a convenient choice of "base point" in each instanton sector.

## Properties

### As gradient flows between flat connections.

We discuss how Yang-Mills instantons may be understood as trajectories of the [[gradient flow]] of the [[Chern-Simons theory]] [[action functional]].

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

These must be such that there is $t_1 \lt t_2 \in \mathbb{R}$ such that $F_\nabla(t \lt t_1) = 0$ and $F_\nabla(T \gt t_2) = 0$, hence these must be solutions interpolating between two [[curvature|flat]] connections $\nabla_{t_1}$ and $\nabla_{t_2}$.

For $A \in \Omega^1(U\times \mathbb{R}, \mathfrak{g})$ the [[Lie algebra valued 1-form]] corresponding to $\nabla$, we can always find a [[gauge transformation]] such that $A_{\partial_t} = 0$ ("[[temporal gauge]]"). In this gauge we may hence equivalently think of $A$ as a 1-parameter family

$$
  t \mapsto A(t) \in \Omega^1(\Sigma, \mathfrak{g})
$$

of connections on $\Sigma$. Then the self-duality condition on a Yang-Mills instanton 

$$
  F_\nabla = - \star F_\nabla
$$

reads equivalently

$$
  \frac{d}{d t} A = -\star_{g} F_A
  \,\,\,
  \in 
  \Omega^1(\Sigma, \mathfrak{g})
  \,.
$$

+-- {: .num_defn #HodgeInnerProduct}
###### Definition

On the linear [[configuration space]] $\Omega^1(\Sigma, \mathfrak{g})$ of [[Lie algebra valued forms]] on $\Sigma$ define the [[Hodge inner product]] [[metric]]

$$
  G(\alpha, \beta) := \int_{\Sigma} \langle \alpha \wedge \star_g \beta \rangle
  \,,
$$

where $\langle-,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$ is the [[Killing form]] [[invariant polynomial]] on the [[Lie algebra]] $\mathfrak{g}$.

=--

+-- {: .num_prop}
###### Proposition

The instanton equation 

$$
  \frac{d}{d t} A = 
  -\star_{g} F_A
$$

is the equation characterizing trajectories of the [[gradient flow]] of the [[Chern-Simons action functional]]

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
  \star \star A = (-1)^{1(3+1)} A = A
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

Often this is interpreted as saying that "a Yang-Mills instanton describes the [[tunneling]] between two [[Chern-Simons theory]] [[vacua]]".

## Examples

* In $SU(2)$-YM theory: see _[[BPTS instanton]]_ .

* In $SU(3)$-YM theory, [[QCD]]/[[strong nuclear force]]: see _[[instanton in QCD]]_



## Related concepts

* [[non-perturbative effect]]

* [[instanton Floer homology]]

* [[self-dual higher gauge field]]

* [[magnetic monopole]]

  [[Dirac monopole]], [[Yang monopole]]

## References

Introductions and surveys include

* J. Zinn-Justin, _The principles of instanton calculus_, Les Houches (1984)

* M.A. Shifman et al., _ABC of instantons_, Fortschr.Phys. 32,11 (1984) 585

For a fairly comprehensive list of literature see the bibliography of 

* Marcus Hutter, _Instantons in QCD: Theory and Application of the Instanton Liquid Model_ ([arXiv:hep-ph/0107098](http://arxiv.org/abs/hep-ph/0107098))

The multi-instantons in $SU(2)$-Yang-Mills theory ([[BPTS instantons]]) were discovered in

* A. A. Belavin, A.M. Polyakov, A.S. Schwartz, Yu.S. Tyupkin, _Pseudoparticle solutions of the Yang-Mills equations_, Phys. Lett. B 59 (1), 85-87 (1975) <a href="http://dx.doi.org/10.1016/0370-2693(75)90163-X">doi</a>

* A. A. Belavin, V.A. Fateev, A.S. Schwarz, Yu.S. Tyupkin, _Quantum fluctuations of multi-instanton solutions_, Phys. Lett. B 83 (3-4), 317-320 (1979) <a href="http://dx.doi.org/10.1016/0370-2693(79)91117-1">doi</a>

See also

* [[Michael Atiyah]], [[Nigel Hitchin]], J. M. Singer, _Deformations of instantons_, Proc. Nat. Acad. Sci. U.S. __74__, 2662 (1977)

* [[Edward Witten]], _Some comments on the recent twistor space constructions_, Complex manifold techniques in theoretical physics (Proc. Workshop, Lawrence, Kan., 1978), pp. 207&#8211;218, Res. Notes in Math., 32, Pitman, Boston, Mass.-London, 1979. 

Methods of algebraic geometry were introduced in

* M. F. Atiyah, R. S. Ward, _Instantons and algebraic geometry_, Comm. Math. Phys. __55__, n. 2 (1977), 117-124, [MR0494098](http://www.ams.org/mathscinet-getitem?mr=0494098), [euclid](http://projecteuclid.org/euclid.cmp/1103900980)

The more general [[ADHM construction]] in terms of linear algebra of vector bundles on projective varieties is proposed in 

* M.F. Atiyah, N.J. Hitchin, V.G. Drinfeld, Yu.I. Manin, _Construction of instantons_, Physics Letters 65 A, 3, 185--187 (1978) [pdf](http://www.new.ox.ac.uk/system/files/ADHM.pdf)

Monographs with the standard material include

* [[Dan Freed]], [[Karen Uhlenbeck]], _Instantons and four-manifolds_, Springer-Verlag, (1991) 

* [[Robbert Dijkgraaf]], _Topological gauge theories and group cohomology_ ([ps](staff.science.uva.nl/~rhd/papers/group.ps))

* Nicholas Manton, Paul M. Sutcliffe, _Topological solitons_, Cambridge Monographs on Math. Physics, [gBooks](http://books.google.com/books?id=e2tPhFdSUf8C)

Yang-Mills instantons on spaces other than just spheres are explicitly discussed in 

* [[Gabor Kunstatter]], _Yang-mills theory in a multiply connected three space_, Mathematical Problems in Theoretical Physics: Proceedings of the VIth International Conference on Mathematical Physics Berlin (West), August 11-20,1981. Editor: R. Schrader, R. Seiler, D. A. Uhlenbrock, Lecture Notes in Physics, vol. 153, p.118-122 ([web](http://adsabs.harvard.edu/abs/1982LNP...153..118K))

based on 

* [[Chris Isham]] [[Gabor Kunstatter]], Phys. Letts. v.102B, p.417, 1981.

* [[Chris Isham]] [[Gabor Kunstatter]], J. Math. Phys. v.23, p.1668, 1982.


In 

* Henrique N. S&aacute; Earp, _Instantons on $G_2$&#8722;manifolds_ PhD thesis (2009) ([pdf](http://www.ime.unicamp.br/~hqsaearp/index_files/HENRIQUE_SA_EARP_THESIS_UPDATED.PDF))

is a discussion of Yang-Mills instantons on a 7-dimensional [[manifold with special holonomy]].

* [[Michael Atiyah]], [[R. Bott]], _The Yang-Mills equations over Riemann surfaces_, Philos. Trans. Roy. Soc. London Ser. A 308 (1983), no. 1505, 523&#8211;615, [MR85k:14006](http://www.ams.org/mathscinet-getitem?mr=702806), [doi](http://dx.doi.org/10.1098/rsta.1983.0017). 

[[!redirects Yang-Mills instantons]]

[[!redirects instanton number]]
[[!redirects instanton numbers]]
