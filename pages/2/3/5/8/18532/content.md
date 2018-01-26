

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


+-- {: .num_prop #ExtensionUniqueNonPositiveDegreeOfDivergence}
###### Proposition
**(unique [[extension of distributions]] with negative [[degree of divergence of a distribution|degree of divergence]])**

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] on the [[complement]] of the origin, with [[negative number|negative]] [[degree of divergence of a distribution|degree of divergence]] at the origin

$$
  deg(u) \lt 0
  \,.
$$

Then $u$ has a _unique_ [[extension of distributions]] $\hat u \in \mathcal{D}'(\mathbb{R}^n)$ to the origin with the same degree of divergence

$$
  deg(\hat u) = deg(u)
  \,.
$$

=--

([Brunetti-Fredenhagen 00, theorem 5.2](#BrunettiFredenhagen00), [Dütsch  18, theorem 3.35 a)](#Duetsch18))

+-- {: .proof}
###### Proof

Regarding uniqueness:

Suppose $\hat u$ and ${\hat u}^\prime$ are two extensions of $u$ with $deg(\hat u) = deg({\hat u}^\prime)$. Both being extensions of a distribution defined on $\mathbb{R}^n \setminus \{0\}$, this difference has [[support of a distribution|support]] at the origin $\{0\} \subset \mathbb{R}^n$. By [this prop.](point-supported+distribution#PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions) this implies that it is a linear combination of [[derivative of a distribution|derivatives]] of the [[delta distribution]] [[support of a distribution|supported]] at the origin:

$$
  {\hat u}^\prime - \hat u
  \;=\;
  \underset{
    {\alpha \in \mathbb{N}^n}
  }{\sum}
  c^\alpha \partial_\alpha \delta_0
$$

for constants $c^\alpha \in \mathbb{C}$. But by [this example](scaling+degree+of+a+distribution#DerivativesOfDeltaDistributionScalingDegree) the [[degree of divergence of a distribution|degree of divergence]] of these [[point-supported distributions]] is non-negative

$$
  deg( \partial_\alpha \delta_0)
  =
  {\vert \alpha\vert} \geq 0  
  \,.
$$

This implies that $c^\alpha = 0$ for all $\alpha$, hence that the two extensions coincide.


Regarding existence: 


Let

$$
  b \in C^\infty_{cp}(\mathbb{R}^n)
$$

be a [[bump function]] which is $\leq 1$ and [[constant function|constant]] on 1 over a [[neighbourhood]] of the origin. Write

$$
  \chi \coloneqq 1 - b \;\in\; C^\infty(\mathbb{R}^n)
$$

<center>
<img src="https://ncatlab.org/nlab/files/PointExtensionOfDistributions.png" > 
</center>

> graphics grabbed from [Dütsch 18, p. 108](#Duetsch18)

and for $\lambda \in (0,\infty)$ a [[positive real number]], write

$$
  \chi_\lambda(x)
  \coloneqq
  \chi(\lambda x)
  \,.
$$

Since the [[product of distributions|product]] $\chi_\lambda u$ has [[support of a distribution]] on a [[complement]] of  a [[neighbourhood]] of the origin, we may extend it by zero to a distribution on all of $\mathbb{R}^n$, which we will denote by the same symbols:

$$
  \chi_\lambda u \in \mathcal{D}'(\mathbb{R}^n)
  \,.
$$

By construction $\xhi_\lambda u$ coincides with $u$ away from a neighbourhood of the origin, which moreover becomes arbitrarily small as $\lambda$ increases.  This means that if the following [[limit of a sequence|limit]] exists

$$
  \hat u
  \;\coloneqq\;
  \underset{\lambda \to \infty}{\lim}
   \chi_\lambda u
$$

then it is an extension of $u$.

To see that the limit exists, it is sufficient to observe that we have a [[Cauchy sequence]], hence that for all $b\in C^\infty_{cp}(\mathbb{R}^n)$ the difference

$$
  (\chi_{n+1} u - \chi_n u)(b)
  \;=\;
  u(b)( \chi_{n+1} + \chi_n )
$$

becomes arbitrarily small.

Finally to see that the unique extension $\hat u$ thus established has the same scaling degree as $u$:

(...)

=--


+-- {: .num_prop #SpaceOfPointExtensions}
###### Proposition
**(space of [[point-extensions of distributions]])

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] of [[scaling degree of a distribution|degree of divergence]] $deg(u) \lt \infty$. 

Then $u$ does admit at least one [[extension of distributions|extension]] (def. \ref{ExtensionOfDistributions}) to a distribution $\hat u \in \mathcal{D}'(\mathbb{R}^n)$, and every choice of extension has the same [[degree of divergence of a distribution|degree of divergence]] as $u$

$$
  deg(\hat u) = deg(u)
  \,.
$$

Moreover, any two such extensions $\hat u$ and ${\hat u}^\prime$ differ by a linear combination of [[partial derivatives|partial]] [[derivatives of distributions]] of order $\leq deg(u)$ of the [[delta distribution]] $\delta_0$ [[support of a distribution|supported]] at the origin:

$$
  {\hat u}^\prime
  -
  \hat u
  \;=\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha\vert} \leq deg(u) }
  }{\sum}
  q^\alpha
  \partial_\alpha \delta_0
  \,,
$$

for a finite number of constants $q^\alpha \in \mathbb{C}$.

=--

This is essentially ([Hörmander 90, thm. 3.2.4](#Hoermander90)). We follow ([Brunetti-Fredenhagen 00, theorem 5.3](#BrunettiFredenhagen00)), which was inspired by ([Epstein-Glaser 73, section 5](#EpsteinGlaser73)). Review of this approach is in ([Dütsch 18, theorem 3.35 (b)](#Duetsch18)), see also remark \ref{WExtensions} below.


+-- {: .proof}
###### Proof


For $f \in C^\infty(\mathbb{R}^n)$ a [[smooth function]], and $\rho \in \mathbb{N}$, we say that _$f$ vanishes to order $\rho$_ at the origin if all [[partial derivatives]] with multi-index $\alpha \in \mathbb{N}^n$ of total order ${\vert \alpha\vert} \leq \rho$ vanish at the origin:

$$
  \partial_\alpha f (0) = 0
  \phantom{AAA}
  {\vert \alpha\vert} \leq \rho
  \,.
$$

By [[Hadamard's lemma]], such a function may be written in the form

$$
  \label{ForVanishingOrderRhoHadamardExpansion}
  f(x)
  \;=\;
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha \vert} = \rho + 1 }
  }{\sum}
  x^\alpha
  r_\alpha(x)
$$

for [[smooth functions]] $r_\alpha \in C^\infty_{cp}(\mathbb{R}^n)$.

Write

$$
  \mathcal{D}_\rho(\mathbb{R}^n)
    \hookrightarrow
  \mathcal{D}(\mathbb{R}^n)
    \coloneqq
  C^\infty_{cp}(\mathbb{R}^n)
$$

for the subspace of that of all [[bump functions]] on those that vanish to order $\rho$ at the origin.

By definition this is equivalently the joint [[kernel]] of the [[partial derivative|partial]] [[derivatives of distributions]] of order ${\vert \alpha\vert}$ of the [[delta distribution]] $\delta_0$ [[support of a distribution|supported]] at the origin:

$$
  b \in \mathcal{D}_\rho(\mathbb{R}^n)
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \underset{ 
    {\alpha \in \mathbb{N}^n} 
      \atop 
    { {\vert \alpha\vert} \leq \rho }  
  }
  {\forall}  
    \left\langle \partial_\alpha \delta_0, b \right\rangle 
  = 0
  \,.
$$

Therefore every [[continuous linear map|continuous linear]] [[projection]]

$$
  p_\rho
   \;\colon\;
  \mathcal{D}(\mathbb{R}^n)
    \longrightarrow
  \mathcal{D}_\rho(\mathbb{R}^n)
$$

may be obtained from a choice of _dual basis_ to the $\{\partial_\alpha \delta_0\}$, hence a choice of smooth functions

$$
  \left\{
    w^\beta \in C^\infty_{cp}(\mathbb{R}^n)
  \right\}_{ { \beta \in \mathbb{N}^n } \atop { {\vert \beta\vert} \leq \rho } }
$$

such that

$$
  \left\langle
    \partial_\alpha \delta_0
    \,,\,
    w^\beta
  \right\rangle
  \;=\;
  \delta_\alpha^\beta
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \partial_\alpha w^\beta(0)
    \;=\;
  \delta_\alpha^\beta
  \phantom{AAAA}
  \text{for}\, {\vert \alpha\vert} \leq \rho
  \,,
$$

by setting

$$
  \label{SpaceOfSmoothFunctionsOfGivenVaishingOrderProjector}
  p_\rho
  \;\coloneqq\;
  id
  \;-\;
  \left\langle
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  w^\alpha \partial_\alpha \delta_0
  \,,\,
  (-)
  \right\rangle
  \,,
$$

hence

$$
  p_\rho
  \;\colon\;
  b
    \mapsto
  b 
    - 
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  (-1)^{{\vert \alpha\vert}} w^\alpha \partial_\alpha b(0)
  \,.
$$

Together with [[Hadamard's lemma]] in the form (eq:ForVanishingOrderRhoHadamardExpansion) this means that every $b \in \mathcal{D}(\mathbb{R}^n)$ is decomposed as

$$
  \label{ForExtensionOfDistributionsTestFunctionDecomposition}
  \begin{aligned}
  b(x)
  & =
  p_\rho(b)(x)
  \;+\;
  (id - p_\rho)(b)(x)
  \\
  & =
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert}  \rho + 1 }
  }{\sum}
  x^\alpha r_\alpha(x)
  \;+\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert} \leq \rho }
  }{\sum}
  (-1)^{{\vert \alpha \vert}}
  w^\alpha \partial_\alpha b(0)
  \end{aligned}
$$

Now let

$$
  \rho
  \;\coloneqq\;
  deg(u)
  \,.
$$

Observe that (by [this prop.](scaling+degree+of+a+distribution#ScalingDegreeOfDistributionsBasicProperties)) the [[degree of divergence of a distribution|degree of divergence]] of the [[product of distributions]] $x^\alpha u$ with ${\vert \alpha\vert} = \rho + 1$ is [[negative number|negative]]


$$
  \begin{aligned}
    deg\left(
      x^\alpha u
    \right)
    & =
    \rho - {\vert \alpha \vert}
    \leq
    -1
 \end{aligned}
$$

Therefore prop. \ref{ExtensionUniqueNonPositiveDegreeOfDivergence} says that each $x^\alpha u$ for ${\vert \alpha\vert} = \rho + 1$ has a unique extension $\widehat{ x^\alpha u}$ to the origin. Accordingly the composition $u \circ p_\rho$ has a unique extension, by (eq:ForExtensionOfDistributionsTestFunctionDecomposition):

$$
  \begin{aligned}
  \left\langle
    \hat u
    \,,\,
    b
  \right\rangle
  & =
  \left\langle
    \hat u
    ,
    p_\rho(b)
  \right\rangle
  + 
  \left\langle
    \hat u
    ,
    (id - p_\rho)(b)
  \right\rangle
  \\
  & =
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert} = \rho + 1 }
  }{\sum}
  \underset{
    \text{unique}
  }{
  \underbrace{
    \left\langle
     \widehat{x^\alpha u}  
      \,,\,
      r_\alpha
    \right\rangle
  }
  }
  \;+\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  \underset{
    \text{choice}
  }{
  \underbrace{
  \langle
    \hat u
    \,,\,
    w^\alpha
  \rangle
  }
  }
  \left\langle
    \partial_\alpha \delta_0
    \,,\,
    b
  \right\rangle
  \end{aligned}
$$

That says that $\hat u$ is of the form

$$
  \hat u
  \;=\;
  \underset{
    \text{unique}
  }{
  \underbrace{
    \widehat{
      u \circ p_\rho
    }
  }
  }
  + 
  \underset{
    { \alpha \in \mathbb{N}^n  }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  c^\alpha
  \,
  \partial_\alpha \delta_0
$$

for a finite number of constants $c^\alpha \in \mathbb{C}$.

Notice that for any extension $\hat u$ the exact value of the $c^\alpha$ here depends on the arbitrary choice of dual basis $\{w^\alpha\}$ used for this construction. But the uniqueness of the first summand means that for any two choices of extensions $\hat u$ and ${\hat u}^\prime$, their difference is of the form

$$
  {\hat u}^\prime - \hat u
  \;=\;
  \underset{
    { \alpha \in \mathbb{N}^n  }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  ( (c')^\alpha - c^\alpha )
  \,
  \partial_\alpha \delta_0  
  \,,
$$

where the constants $q^\alpha \coloneqq ( (c')^\alpha - c^\alpha ) \in \mathbb{C}$ are independent of any choices.


It remains to see that all these $\hat u$ in fact have the same degree of divergence as $u$.

By [this example](scaling+degree+of+a+distribution#DerivativesOfDeltaDistributionScalingDegree) the degree of divergence of the point-supported distributions on the right is $deg(\partial_\alpha \delta_0) = {\vert \alpha\vert} \leq \rho$. 

Therefore to conclude it is now sufficient to show that

$$
  deg\left(
    \widehat{
      u \circ p_\rho
    }
  \right)
  \;=\;
  \rho
  \,.
$$

(...)

=--


+-- {: .num_remark #WExtensions}
###### Remark
**("W-extensions")**

Since in [Brunetti-Fredenhagen 00, (38)](#BrunettiFredenhagen00) the projectors (eq:SpaceOfSmoothFunctionsOfGivenVaishingOrderProjector) are denoted "$W$", the construction of [[extensions of distributions]] via the proof of prop. \ref{SpaceOfPointExtensions} has come to be called "W-extensions" (e.g [Dütsch 18](#Duetsch18)).

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

reviewed in

* {#Duetsch18} [[Michael Dütsch]], theorem 3.35 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


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
