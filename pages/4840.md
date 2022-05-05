
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The __Stokes theorem__ (also _Stokes\' theorem_ or _Stokes\'s theorem_) asserts that the [[integration of differential forms|integral]] of an [[exterior differential form]] on the boundary of an [[orientation|oriented]] [[manifold with boundary]] (or [[submanifold]] or [[chain]] of such) equals the integral of the [[de Rham differential]] of the form on the manifold itself.  (The theorem also applies to exterior pseudoforms on a chain of pseudoriented submanifolds.)


## Statement

### Traditional statement

Let 

$$
  \Delta_{Diff} : \Delta \to Diff
$$

be the [[cosimplicial object]] of standard $k$-[[simplices]] in [[SmoothMfd]]: in degree $k$ this is the standard $k$-[[simplex]] $\Delta^k_{Diff} \subset \mathbb{R}^k$ regarded as a [[smooth manifold]] [[manifold with corners|with boundary and corners]]. This may be parameterized as

$$
  \Delta^k = \{ t^1, \cdots, t^k \in \mathbb{R}_{\geq 0} | \sum_i t^i \leq 1\}
  \subset \mathbb{R}^k
  \,.
$$

In this parameterization the coface maps of $\Delta_{Diff}$ are 

$$
  \partial_i : (t^1, \cdots, t^{k-1}) \mapsto
  \left\{
    \array{
       (t^1, \cdots, t^{i-1}, t^{i+1} , \cdots, t^{k-1}) & | i \gt 0
       \\
       (1- \sum_{i=1}^{k-1} t^i, t^1, \cdots, t^{k-1})
    }
  \right.
  \,.
$$

For $X$ any [[smooth manifold]] a **smooth $k$-simplex in $X$** is a [[smooth function]]

$$
  \sigma : \Delta^k \to X
  \,.
$$

The **boundary** of this simplex in $X$ is the [[chain]] (formal linear combination of smooth $(k-1)$-simplices)

$$
  \partial \sigma = \sum_{i = 0}^k (-1)^i \sigma \circ \partial_i
  \,.
$$


Let $\omega \in \Omega^{k-1}(X)$ be a degree $(k-1)$-[[differential form]] on $X$.

+-- {: .num_theorem}
###### Theorem
**(Stokes theorem)**

The [[integral]] of $\omega$ over the boundary of the simplex equals the integral of its [[de Rham differential]] over the simplex itself

$$
  \int_{\partial \sigma} \omega = \int_\sigma d \omega
  \,.
$$

=--

It follows that for $C$ any $k$-[[chain]] in $X$ and $\partial C$ its boundary $(k-1)$-chain, we have

$$
  \int_{\partial C} \omega = \int_{C} d \omega
  \,.
$$

More generally:


+-- {: .num_prop #StokesTheoremForFiberIntegration}
###### Proposition
**(Stokes theorem for [[fiber integration]])**

If $U$ is any [[smooth manifold]] and $\omega \in \Omega^\bullet(U \times \sigma)$ is a differential form on the [[Cartesian product]], then with respect to [[fiber integration|fiber-wise]] [[integration of differential forms]] 

$$
  \int_\sigma \;\colon\;
  \Omega^{\bullet + dim(\sigma)}(U \times \sigma)
    \longrightarrow
  \Omega^\bullet(U)
$$

along $U \times \sigma \overset{pr_1}{\to} U$ we have

$$
  \int_\sigma d \omega
  \;=\;
  \int_{\partial_\sigma} \omega
  +
  (-1)^{dim(\sigma)} d \int_\sigma \omega 
  \,.
$$

=--

(e.g. [Gomi-Terashima 00, remark 3.1](fiber+integration+in+ordinary+differential+cohomology#GomiTerashima00))


### Abstract formulation in cohesive homotopy-type theory
 {#FormulationInCohesiveHomotopyTypeTheory}

We discuss here a general abstract formulation of differential forms, their integration and Stokes theorem in the axiomatics of [[cohesive homotopy type theory]] (following [Bunke-Nikolaus-V&#246;lkl 13, theorem 3.2](#BunkeNikolausVoelkl13)).


Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] and write $T \mathbf{H}$ for its [[tangent cohesive (∞,1)-topos]].

Assume that there is an [[interval object]] 

$$
  \ast \cup \ast \stackrel{(i_0, i_1)}{\longrightarrow}  \Delta^1
$$ 

"exhibiting the cohesion" (see at _[[continuum]]_) in that there is a (chosen) [[equivalence]] between the [[shape modality]] $\Pi$ and the [[localization of an (∞,1)-category|localization]] $L_{\Delta^1}$ at the the [[projection]] maps out of [[Cartesian products]] with this line $\Delta^1\times (-) \to (-)$

$$
  \Pi \simeq L_{\Delta^1}
  \,.
$$ 

This is the case for instance for the "standard [[continuum]]", the [[real line]] in $\mathbf{H} = $ [[Smooth∞Grpd]].

It follows in particular that there is a chosen [[equivalence of (∞,1)-categories]] 

$$
  \flat(\mathbf{H})\simeq L_{\Delta^1}\mathbf{H}
$$

between the [[flat modality|flat]] [[modal types|modal homotopy-types]] and the $\Delta^1$-homotopy invariant homotopy-types.

Given a [[stable homotopy type]] $\hat E \in Stab(\mathbf{H})\hookrightarrow T \mathbf{H}$ [[cohesion]] provides two objects 

$$
  \Pi_{dR} \Omega \hat E \,,\;\;  \flat_{dR}\Sigma \hat E
  \;\;
  \in Stab(\mathbf{H})
$$

which may be interpreted as [[de Rham complexes]] with [[coefficients]] in $\Pi(\flat_{dR} \Sigma \hat E)$, the first one restricted to negative degree, the second to non-negative degree. Moreover, there is a canonical map

$$
  \array{
    \Pi_{dR}\Omega \hat E && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}\Sigma \hat E
    \\
    & {}_{\mathllap{\iota}}\searrow && \nearrow_{\mathrlap{\theta_{\hat E}}}
    \\
    && 
    \hat E
  }
$$

which interprets as the [[de Rham differential]] $\mathbf{d}$. See at _[[differential cohomology diagram]]_ for details. 

Throughout in the following we leave the "inclusion" $\iota$ of "differential forms regarded as $\hat E$-connections on trivial $E$-bundles" implicit.

+-- {: .num_defn #CohesiveIntegrationOfDifferentialForms}
###### Definition

[[integration of differential forms|Integration of differential forms]] is the map

$$
  \int_{\Delta^1} \;\colon\;  [\Delta^1, \flat_{dR}\Sigma \hat E] \longrightarrow \Pi_{dR}\Omega \hat E
$$

which is induced via the [[homotopy cofiber]] property of $\flat_{dR}\Omega \hat E$ from the [[counit of a comonad|counit]] naturality square of the [[flat modality]] on $[(\ast \coprod \ast \stackrel{(i_0, i_1)}{\to} \Delta ^1 ), -]$, using that this square exhibits a [[null homotopy]] due to the $\Delta^1$-homotopy invariance of $\flat \hat E$.

=--

+-- {: .num_prop}
###### Proposition

Stokes' theorem holds:

$$
  \int_{\Delta^1} \circ \mathbf{d} 
  \;\simeq\; 
  i_1^\ast - i_0^\ast
  \,.
$$

=--

([Bunke-Nikolaus-V&#246;lkl 13, theorem 3.2](#BunkeNikolausVoelkl13))


## Classical forms

In early 20th-century [[vector analysis]] (and even today in undergraduate Calculus courses), the Stokes theorem took various classical forms about [[vector fields]] in the [[Cartesian space]] $\mathbb{R}^n$:

* if $n = 1$ and $k = 1$, then this is the second [[FTC|Fundamental Theorem of Calculus]]: $\int_{[a,b]} f' = f(b) - f(a)$, where $a \leq b$ are [[real numbers]] and $f$ is a [[continuously differentiable function]] on a [[neighbourhood]] of the [[interval]] $[a,b]$;

* if $k = 1$ more generally, then this is a generalized form of the FTC: $\int_C grad f \cdot \mathbf{T} = f(Q) - f(P)$, where $C$ is a continuously differentiable oriented [[curve]] in $\mathbb{R}^n$, $P$ and $Q$ are the beginning and ending points (respectively) of $C$, $\mathbf{T}$ is the [[unit vector]] field on $C$ tangent to $C$ in the direction given by its orientation, and $f$ is a continuously differentiable function on a neighbourhood of $C$;

* if $n = 2$ and $k = 2$, then this is [[Green's Theorem]] (see there for other forms): $\int\int_R (\partial{v}/\partial{x} - \partial{u}/\partial{y}) = \int_C (u \,\mathrm{d}x + v \,\mathrm{d}y)$, where $C$ is a continuously differentiable [[simple closed curve]] in $\mathbb{R}^2$ (oriented using the standard orientation on $\mathbb{R}^2$), $R$ is the region that it encloses (guaranteed by the [[Jordan curve theorem|Jordan Curve Theorem]]), and $u$ and $v$ are continuously differentiable functions of the coordinates $x$ and $y$ on a neighbourhood of $R$;

* if $n = 3$ and $k = 2$, then this is the __Kelvin--Stokes Theorem__ or __Curl Theorem__: $\int\int_R curl \mathbf{F} \cdot \mathbf{n} = \int_C \mathbf{F} \cdot \mathbf{T}$, where $R$ is a continuously differentiable [[pseudoorientation|pseudooriented]] [[surface]] in $\mathbb{R}^3$ with a continuously differentiable boundary $C$ (oriented to match the pseudoorientation of $R$ using the standard orientation on $\mathbb{R}^3$), $\mathbf{n}$ is the unit [[normal vector]] field on $R$ in the direction given by the pseudoorientation of $R$, $\mathbf{T}$ is the unit tangent vector field on $C$, and $\mathbf{F}$ is a continuously differentiable [[vector field]] on a neighbourhood of $D$;

* if $n = 3$ and $k = 3$, then this is the __Ostrogradsky--Gauss Theorem__ or __Divergence Theorem__: $\int\int\int_D div \mathbf{F} = \int\int_R \mathbf{F} \cdot \mathbf{n}$, where $R$ is a continuously differentiable closed surface in $\mathbb{R}^3$, $D$ is the region that it encloses (guaranteed by the [[Jordan-Brouwer separation theorem|Jordan--Brouwer Separation Theorem]]), $\mathbf{n}$ is the outward-pointing unit normal vector field on $R$, and $\mathbf{F}$ is a continuously differentiable vector field on a neighbourhood of $D$;

* if $k = n$ more generally, then this is the generalized [[Divergence Theorem]]: $\int_D div \mathbf{F} = \int_R \mathbf{F} \cdot \mathbf{n}$, where $R$ is a continuously differentiable closed [[hypersurface]] in $\mathbb{R}^n$, $D$ is the region that it encloses, $\mathbf{n}$ is the outward-pointing unit normal vector field on $R$, and $\mathbf{F}$ is a continuously differentiable vector field on a neighbourhood of $D$.


## Related concepts

* [[Poincaré lemma]]

* **Stokes theorem**

  * [[nonabelian Stokes theorem]]

* [[de Rham theorem]]

* [[Hodge theorem]]

* a special case is [[Cauchy's integral theorem]]


## References
 {#References}

A standard account is for instance in

* Reyer Sjamaar, _Manifolds and differential forms_, [pdf](http://www.math.cornell.edu/~sjamaar/papers/manifold.pdf)

Discussion of [[chains]] of smooth [[singular simplices]]

* _Stokes' theorem on chains_ (<a href="http://idv.sinica.edu.tw/ftliang/diff_geom/*diff_geometry(II)/3.25/deRham_theorem/stokes_on_chains.pdf">pdf</a>)

Discussion of Stokes theorem on [[manifolds with corners]] is in 

* [[Brian Conrad]], _[Differential geometry](http://math.stanford.edu/~conrad/diffgeomPage/handouts.html)_ _Math 396. Stokes' theorem with corners_ ([pdf](http://math.stanford.edu/~conrad/diffgeomPage/handouts/stokescorners.pdf))

Discussion for manifolds with more general singularities on the boundary is in 

* Friedrich Sauvigny, _Partial Differential Equations: Vol. 1 Foundations and Integral Representations_

Discussion in [[cohesive homotopy type theory]] is in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))


[[!redirects Stokes Theorem]]
[[!redirects Stokes theorem]]
[[!redirects Stokes theorems]]

[[!redirects Stokes' theorem]]
[[!redirects Stokes' Theorem]]
[[!redirects Stokes’ theorem]]
[[!redirects Stokes’ Theorem]]
[[!redirects Stokes\' theorem]]
[[!redirects Stokes\' Theorem]]
[[!redirects Stokes's theorem]]
[[!redirects Stokes's Theorem]]
[[!redirects Stokes’s theorem]]
[[!redirects Stokes’s Theorem]]
[[!redirects Stokes\'s theorem]]
[[!redirects Stokes\'s Theorem]]

[[!redirects Kelvin-Stokes theorem]]
[[!redirects Kelvin-Stokes Theorem]]
[[!redirects Kelvin–Stokes theorem]]
[[!redirects Kelvin–Stokes Theorem]]
[[!redirects Kelvin--Stokes theorem]]
[[!redirects Kelvin--Stokes Theorem]]
