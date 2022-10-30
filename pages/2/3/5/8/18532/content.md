

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

Given a suitable [[subspace]] inclusion $X \hookrightarrow \hat X$ and a [[distribution]] $u$ on $X$, then an _extension_  of $u$ to $\hat X$ is a distribution $\hat u$ on $\hat X$ whose [[restriction of distributions]] to $X$ coincides with $u$. If $u$ comes from an ordinary [[smooth function]] or else if $u$ is properly understood as a [[generalized function]], then this corresponds to an ordinary [[extension]]

$$
  \array{
    X &\overset{u}{\longrightarrow}& \mathbb{R}
    \\
    \downarrow & \nearrow_{\mathrlap{\hat u}}
    \\
    \hat X
  }
$$

Regarding that we the distributions are not the maps from the underlying space we need to replace pre-composition $X\to\tilde{X}$ by the appropriate [[pullback of distributions]] always defined say if $X\to\tilde{X}$ is
a submersion; in the case of an [[open embedding]]  (see [this example](pullback+of+a+distribution#RestrictionOfDistributions)) this operation is the _restriction of distributions_, the operation dual to the operation of extension by zero of test functions. 

## Definition

For an inclusion of two open sets on a manifold $U\subset V$ there is an operator of _extension by zero_ $E_{V U}: C^\infty_0(U)\to C^\infty_0(V)$ where $E_{V U}(f)(x) = f(x)$ if $x\in U$ and $E_{U V}(f)(x) = 0$ otherwise. 
The __[[restriction of distributions]]__ $\rho_{U V} : \mathcal{D}'(V)\to \mathcal{D}'(U)$ is then defined by 
$$
\langle \rho_{U V}(\phi), f\rangle = \langle \phi, E_{V U} f\rangle,
\,\,\,\,\,\,\,f\in C^\infty_0(U),\,\phi\in \mathcal{D}'(V).
$$

([this example](pullback+of+a+distribution#RestrictionOfDistributions)).

Now the diagram in the idea section makes sense in the following way:
for an open embedding $X\hookrightarrow\hat{X}$, $\hat{u}\in\mathcal{D}'(\hat{X})$ __extends__ $u\in \mathcal{D}'(X)$ if $\rho_{X\hat{X}}(\hat{u}) = u$.  

+-- {: .num_defn #ExtensionOfDistributions}
###### Definition
**([[extension of distributions]])**

Let $X \overset{\iota}{\subset} \hat X$ be an inclusion of [[open subsets]] of some [[Cartesian space]]. This induces the operation of [[restriction of distributions]]

$$
  \mathcal{D}'(\hat X) 
    \overset{\iota^\ast}{\longrightarrow}
  \mathcal{D}'(X)
  \,.
$$

Given a [[distribution]] $u \in \mathcal{D}'(X)$, then an _[[extension]]_ of $u$ to $\hat X$ is a distribution $\hat u \in \mathcal{D}'(\hat X)$ such that 

$$
  \iota^\ast \hat u 
  \;=\;
  u
  \,.
$$

=--



## Properties

### Point-extensions
 {#SolutionSpaceOfPointExtensions}

Of particular interest is the special case of [[extension of distributions]] to a single point $p \in \hat X$, hence where $X = \hat X \setminus \{p\}$ is the [[complement]] of that point. 

Contrary to ordinary [[smooth functions]], distributions ([[generalized functions]]) in general have more than one extension to a point, where the freedom is in choosing a [[distribution with point support]] at that point, hence some [[derivative of a distribution|derivative]] of the [[delta distribution]] [[support of a distribution|supported]] at that point. 

However, if one requires that the [[scaling degree of a distribution|scaling degree]] of the extended distribution at the given point is compatible with that of the original distribution, then there is only a [[finite set]] of possible extensions, parameterized by the [[coefficients]] of a finite number of derivatives of the delta-distribution (prop. \ref{SpaceOfPointExtensions} below).

In the construction of [[perturbative quantum field theories]] via [[causal perturbation theory]], where the ("[[operator-valued distributions|operator-valued]]") distributions in questions are [[time-ordered product]] coefficients in the [[scattering matrix]] and where the point being extended to corresponds to the point where an [[interaction]] happens, this finite set of choices is identified with the [[renormalization|("re"-)normalization]] freedom.

We discuss specifically the space of solutions of extending a distribution on the [[complement]] $\mathbb{R}^n \setminus \{0\}$ of the origin inside a [[Cartesian space]] to the full space $\mathbb{R}^n$.


+-- {: .num_prop #SpaceOfPointExtensions}
###### Proposition
**(space of [[point-extensions of distributions]])

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] of [[scaling degree of a distribution|degree of divergence]] $deg(u) \lt \infty$. 

Then $u$ does admit an [[extension of distributions|extension]] (def. \ref{ExtensionOfDistributions}) to a distribution $\hat u \in \mathcal{D}'(\mathbb{R}^n)$ with the same [[degree of divergence of a distribution|degree of divergence]] 

$$
  deg(\hat u) = deg(u)
  \,.
$$

Moreover, any two such extensions differ by a [[point-supported distribution]] at the origin of [[order of a distribution|order]] $\leq deg(u)$.

=--

([Hörmander 90, thm. 3.2.4](#Hoermander90), [BrunettiFredenhagen 00, theorem 5.2, 5.3](#BrunettiFredenhagen00), following [Epstein-Glaser 73, section 5](#EpsteinGlaser73))

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

## Examples

### Powers of Feynman propagators

Extension of powers of [[Feynman propagators]] on [[globally hyperbolic spacetimes]] to the [[diagonal]] are worked out explicitly in ([Hollands 07, section 3.4](#Hollands07)).

## References

The argument for the characterization of the point extension of distributions goes back to 

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], section 5 of _[[The role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

thereby laying the foundation for [[causal perturbation theory]]. A textbook account in [[functional analysis]] is in

* {#Hoermander14} [[Lars Hörmander]], theorem 3.2.4 of _The Analysis of Linear Partial Differential Operators I_ (Springer, 1990, 2nd ed.)




A more concise formulation and proof is due to

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 5.2 of _Microlocal analysis and interacting quantum field theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

Exposition of the application to [[renormalization]] of [[Feynman diagrams]] is in

* {#Brouder10} [[Christian Brouder]], _Multiplication of distributions_, 2010 ([[BrouderProductOfDistributions.pdf:file]])


The refinement to the point-extension problem for distributions in the solution space of a given system of [[differential equations]] is discussed in

* {#BahnsWrochna12} Dorothea Bahns, Micha&#322; Wrochna, _On-shell extension of distributions_, [arXiv:1210.5448](https://arxiv.org/abs/1210.5448)

Examples and applications to [[renormalization]] in [[perturbative quantum field theory]] are discussed for instance in

* {#Hollands07} [[Stefan Hollands]], sections 3.3 and 3.4 of _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

For more on extension of distributions in [[renormalization]] see the references at _[[causal perturbation theory]]_ and _[[locally covariant perturbative quantum field theory]]_.


[[!redirects extensions of distributions]]
[[!redirects extension of a distribution]]

[[!redirects point-extension of a distribution]]
[[!redirects point-extensions of distributions]]

[[!redirects point-extension of distributions]]
[[!redirects point-extensions of distributions]]
