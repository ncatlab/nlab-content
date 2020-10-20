+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Chern-Weil theory
+-- {: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

## Examples

### $SU(2)$-instantons from the correct maths to the traditional physics story
 {#FromTheMathsToThePhysicsStory}

[[!include SU2-instantons from the correct maths to the traditional physics story]]


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

### As Dp-D(p+4)-brane bound states
 {#AsDpDpPlus4BraneBoundStates}

Due to the [[higher WZW term]] $\propto \int_{D_{p+4}} C_{p+1} \wedge \langle F \wedge F \rangle$ in the [[Green-Schwarz sigma model]] for [[D-brane|D(p+4)-branes]], [[Yang-Mills instantons]] in the [[Chan-Paton gauge field]] on $D (p+4)$-branes are equivalently [[Dp-D(p+4)-brane bound states]] (see e.g. [Polchinski 96, 5.4](#Polchinski96), [Tong 05, 1.4](#Tong05)).

The lift to [[M-theory]] as [[M5-MO9 brane bound states]] is due to [Strominger 90](#Strominger90), [Witten 96](#Witten96).

[[!include Dp-D(p+4)-brane bound states -- contents]]

## Examples

* In $SU(2)$-YM theory: see _[[BPST instanton]]_ .

* In $SU(3)$-YM theory, [[QCD]]/[[strong nuclear force]]: see _[[instanton in QCD]]_



## Related concepts

* [[theta vacuum]], [[instanton sea]]

* [[instanton]]

* [[Bogomolny equation]], [[Nahm transform]]

* [[small instanton]]

* [[caloron]]

* [[non-perturbative effect]]

* [[instanton Floer homology]]

* [[self-dual higher gauge field]]

* [[magnetic monopole]]

  [[Dirac monopole]], [[Yang monopole]]

* [[fiber bundles in physics]]

* [[Dirac charge quantization]]

* [[gravitational instanton]]

## References

### General

Introductions and surveys include

* J. Zinn-Justin, _The principles of instanton calculus_, Les Houches (1984)

* M.A. Shifman et al., _ABC of instantons_, Fortschr.Phys. 32,11 (1984) 585

* [[Tohru Eguchi]], [[Peter Gilkey]], [[Andrew Hanson]], Section 10.2 of: _Gravitation, gauge theories and differential geometry_, Physics Reports Volume 66, Issue 6, December 1980, Pages 213-393 (<a href="https://doi.org/10.1016/0370-1573(80)90130-1">doi:10.1016/0370-1573(80)90130-1</a>)



* {#Tong05} [[David Tong]], _TASI Lectures on Solitons_ ([arXiv:hep-th/0509216](https://arxiv.org/abs/hep-th/0509216)), _Lecture 1: Instantons_ ([pdf](http://www.damtp.cam.ac.uk/user/tong/tasi/instanton.pdf))

A survey in view of the [[asymptotic series|asymptotic]] nature of the [[Feynman perturbation series]] is in

* {#Suslov05} [[Igor Suslov]], section 4.5 of _Divergent perturbation series_, Zh.Eksp.Teor.Fiz. 127 (2005) 1350; J.Exp.Theor.Phys. 100 (2005) 1188 ([arXiv:hep-ph/0510142](https://arxiv.org/abs/hep-ph/0510142))


For a fairly comprehensive list of literature see the bibliography of 

* Marcus Hutter, _Instantons in QCD: Theory and Application of the Instanton Liquid Model_ ([arXiv:hep-ph/0107098](http://arxiv.org/abs/hep-ph/0107098))

Detailed argument for the [[theta-vacuum]] structure from [[chiral symmetry breaking]] is offered in 

* [[Curtis Callan]], R.F. Dashen, [[David Gross]], _The Structure of the Gauge Theory Vacuum_, Phys.Lett. 63B (1976) 334-340 ([spire](http://inspirehep.net/record/3673?ln=en))

* G. Morchio, [[Franco Strocchi]], _Chiral symmetry breaking and theta vacuum structure in QCD_, Annals Phys.324:2236-2254, 2009 ([arXiv:0907.2522](https://arxiv.org/abs/0907.2522))

The multi-instantons in $SU(2)$-Yang-Mills theory ([[BPST instantons]]) were discovered in

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

* [[Chris Isham]], [[Gabor Kunstatter]], Phys. Letts. v.102B, p.417, 1981. ([doi](http://dx.doi.org/10.1016/0370-2693%2881%2991244-2))

* [[Chris Isham]] [[Gabor Kunstatter]], J. Math. Phys. v.23, p.1668, 1982. ([doi](http://dx.doi.org/10.1063/1.525552))

In 

* Henrique N. S&aacute; Earp, _Instantons on $G_2$&#8722;manifolds_ PhD thesis (2009) ([pdf](http://www.ime.unicamp.br/~hqsaearp/index_files/HENRIQUE_SA_EARP_THESIS_UPDATED.PDF))

is a discussion of Yang-Mills instantons on a 7-dimensional [[manifold with special holonomy]].

* [[Michael Atiyah]], [[R. Bott]], _The Yang-Mills equations over Riemann surfaces_, Philos. Trans. Roy. Soc. London Ser. A 308 (1983), no. 1505, 523&#8211;615, [MR85k:14006](http://www.ams.org/mathscinet-getitem?mr=702806), [doi](http://dx.doi.org/10.1098/rsta.1983.0017). 

### As Dp-D(p+4)-brane bound states

The argument that [[Yang-Mills instantons]] in the [[Chan-Paton gauge field]] on a [[D-brane|D(p+4)-brane]] are equivalent to [[Dp-D(p+4) brane bound states]] goes back to 

* {#Witten96} [[Edward Witten]], _Small Instantons in String Theory_, Nucl. Phys. B460:541-559, 1996 ([arXiv:hep-th/9511030](https://arxiv.org/abs/hep-th/9511030))

* [[Michael Douglas]], _Branes within Branes_, In: Baulieu L., Di Francesco P., Douglas M., Kazakov V., Picco M., Windey P. (eds.) _[Strings, Branes and Dualities](https://link.springer.com/book/10.1007/978-94-011-4730-9)_ NATO ASI Series (Series C: Mathematical and Physical Sciences), vol 520. Springer, Dordrecht ([arxiv:hep-th/9512077](https://arxiv.org/abs/hep-th/9512077), [doi:10.1007/978-94-011-4730-9_10](https://doi.org/10.1007/978-94-011-4730-9_10))

* [[Michael Douglas]], _Gauge Fields and D-branes_, J. Geom. Phys. 28 (1998) 255-262 ([arXiv:hep-th/9604198](https://arxiv.org/abs/hep-th/9604198))

following

* {#Strominger90} [[Andrew Strominger]], _Heterotic solitons_, Nucl. Phys. B343 (1990) 167-184 (<a href="https://doi.org/10.1016/0550-3213(90)90599-9">doi:10.1016/0550-3213(90)90599-9</a>) Erratum: Nucl. Phys. B353 (1991) 565-565 (<a href="https://doi.org/10.1016/0550-3213(91)90349-3">doi:10.1016/0550-3213(91)90349-3</a>) ([spire:27900](http://inspirehep.net/record/27900))



Review is in:

* {#Polchinski96} [[Joseph Polchinski]], Section 5.4 of: _TASI Lectures on D-Branes_ ([arXiv:hep-th/9611050](https://arxiv.org/abs/hep-th/9611050))

* {#Tong05} [[David Tong]], Section 1.4 of _TASI Lectures on Solitons_ ([hep-th/0509216](https://arxiv.org/abs/hep-th/0509216))

Discussion specifically of [[D0-D4-brane bound states]]:

* [[Cumrun Vafa]], _Instantons on D-branes_, Nucl. Phys. B463 (1996) 435-442 ([arXiv:hep-th/9512078](https://arxiv.org/abs/hep-th/9512078))

with emphasis to the resulting [[configuration spaces of points]], as in

* [[Cumrun Vafa]], [[Edward Witten]], Section 4.1 of: _A Strong Coupling Test of S-Duality_, Nucl. Phys. B431:3-77, 1994 ([arXiv:hep-th/9408074](https://arxiv.org/abs/hep-th/9408074))

Discussion specifically of [[D1-D5-brane bound states]]

* [[Neil Lambert]], _D-brane Bound States and the Generalised ADHM Construction_, Nucl. Phys. B519 (1998) 214-224 ([arXiv:hep-th/9707156](https://arxiv.org/abs/hep-th/9707156))

Discussion specifically of [[D4-D8-brane bound states]]: 

In the [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineering]] [[QCD]], where the [[D4-branes]] get interpreted as [[baryons]]:

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], Section 5.7 of: _Low energy hadron physics in holographic QCD_, Prog. Theor. Phys.113:843-882, 2005 ([arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141))





[[!redirects Yang-Mills instantons]]

[[!redirects instanton number]]
[[!redirects instanton numbers]]
