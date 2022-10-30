

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a suitable [[subspace]] inclusion $X \hookrightarrow \hat X$ and a [[distribution]] $u$ on $X$, then an _extension_  of $u$ to $\hat X$ is an distribution $\hat u$ on $\hat X$ whose restriction to $X$ coincdes with $u$. If $u$ comes from an ordinary [[smooth function]] or else if $u$ is properly understood as a [[generalized function]], then this corresponds to an ordinary [[extension]]

$$
  \array{
    X &\overset{u}{\longrightarrow}& \mathbb{R}
    \\
    \downarrow & \nearrow_{\mathrlap{\hat u}}
    \\
    \hat X
  }
$$



## Point-extensions
 {#SolutionSpaceOfPointExtensions}

Of particular interest is the special case of extension of distributions to a single point $p \in \hat X$, hence where $X = \hat X \setminus \{p\}$. Contrary to ordinary functions, distributions in general have more than one extension to a point, where the freedom is in choosing a [[distribution with point support]] at that point, hence some [[derivative of a distribution|derivative]] of the [[delta distribution]] at that point. However, if one requires that the [[scaling degree of a distribution|scaling degree]] of the extended distribution at the given point is compatible with that of the original distribution, then there is only a [[finite set]] of possible extensions, parameterized by the [[coefficients]] of a finite number of derivatives of the delta-distribution (prop. \ref{SpaceOfPointExtensions} below).

In the construction of [[perturbative quantum field theories]] via [[causal perturbation theory]], where the ("[[operator-valued distributions|operator-valued]]") distributions in questions are coefficients in the [[scattering matrix]] and where the point being extended to corresponds to the point where an [[interaction]] happens, this finite set of choices is identified with the [[renormalization]] freedom at each loop order (i.e. the choice of counter-terms).

We discuss specifically the space of solutions of extending a distribution on the [[complement]] $\mathbb{R}^n \setminus \{0\}$ of the origin inside a [[Cartesian space]] to the full space $\mathbb{R}^n$.


+-- {: .num_prop #SpaceOfPointExtensions}
###### Proposition
**(space of point-extensions)

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] of [[scaling degree of a distribution|degree of divergence]] $deg(u) \lt \infty$. Then it does admit an extension to a distribution $\hat u \in \mathcal{D}'(\mathbb{R}^n)$ with $deg(\hat u) = deg(u)$. Moreover, any two such extensions differ by a [[point-supported distribution]] at the origin of [[order of a distribution|order]] $\leq deg(u)$.

=--

([BrunettiFredenhagen 00, theorem 5.2, 5.3](#BrunettiFredenhagen00), following [Epstein-Glaser 73, section 5](#EpsteinGlaser73))

We unwind this statement a little:

+-- {: .num_remark }
###### Remark

Given $u \in \mathcal{D}'(\mathbb{R} \setminus \{0\})$ with $deg(u) \lt \infty$, write 

$$
  PointExt(u)
  \;\coloneqq\;
  \left\{
    \hat u \in \mathcal{D}'(\mathbb{R}^n)
    \;\vert\;
    \hat u\vert_{\mathbb{R}^n \setminus \{0\}} = u
    \,\,,
    deg(\hat u) = deg(u)
  \right\}
$$

for the space of point extensions, and write

$$
  \mathcal{D}'(\mathbb{R}^n)^{ord \leq k}_{supp = \{0\}}
$$ 

for the vector space of [[point-supported distributions]] at the origin of [[order of a distribution|order]] $\leq k \in \mathbb{Z}$. 

Prop. \ref{SpaceOfPointExtensions} says that the set $PointExt(u)$ is a [[torsor]] over the additive [[abelian group]] underlying $\mathcal{D}'(\mathbb{R}^n)^{ord \leq k}_{supp = \{0\}}$, hence that there is a (non-canonical) [[bijection]] of sets

$$
  PointExt(u)
   \;\simeq\;
  \mathcal{D}'(\mathbb{R}^n)^{ord \leq deg(u)}_{supp = \{0\}}
$$


Now by [this prop.](supported+distribution#PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions) the point-supported distributions are precisely the sums of multiples [[derivative of a distribution|derivatives]] of the [[delta distribution]] at the given point:

$$
  \mathcal{D}'(\mathbb{R}^n)^{ord \leq k}_{supp = \{0\}}
  \;\simeq\;
  \left\{
     \underset{ {\alpha \in \mathbb{N}^n} \atop { {\vert \alpha\vert \leq k  } } }{\sum} c^\alpha (\partial_\alpha \delta)(0)
    \;\vert\;
    c^\alpha \in \mathbb{R}
  \right\}
  \,.
$$

In particular for $k \lt 0$ this is a [[singleton]]:

$$
  \mathcal{D}'(\mathbb{R}^n)^{ord \lt 0}_{supp = \{0\}} = \{0\}
  \,.
$$

Hence prop. \ref{SpaceOfPointExtensions} says in particular that a distribution with _[[negative number|negative]]_ [[scaling degree of a distribution|degree of divergence]] has a _unique_ point extension with the same degree of divergence. 


=--


## References

The argument for the characterization of the point extension of distributions goes back to 

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], section 5 of _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

thereby laying the foundation for [[causal perturbation theory]]. A more concise formulation and proof is due to

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 5.1 of _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

The refinement to the point-extension problem for distributions in the solution space of a given system of [[differential equations]] is discussed in

* Dorothea Bahns, Micha&#322; Wrochna, _On-shell extension of distributions_ ([arXiv:1210.5448](https://arxiv.org/abs/1210.5448))

[[!redirects extensions of distributions]]

[[!redirects point-extension of a distribution]]
[[!redirects point-extensions of distributions]]