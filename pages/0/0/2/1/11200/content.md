
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[sheaf of spectra]] on the [[site]] of all [[smooth manifolds]] may be thought of as a [[spectrum]] equipped with generalized [[smooth structure]], in just the same way as an [[(∞,1)-sheaf]] on this site may be thought of as a [[smooth ∞-groupoid]]. Therefore one might speak of the [[stable (∞,1)-category]]

$$
  Sh_\infty(SmoothMfd, Spectra)
  \simeq
  Stab(Sh_\infty(SmoothMfd))
  =
  Stab(Smooth \infty Grpd)
$$

which is the [[stabilization]] of that of [[smooth ∞-groupoids]] as being the $\infty$-category of _smooth spectra_, just as the [[stable (∞,1)-category of spectra]] itself is the [[stabilization]] of that of bare [[∞-groupoids]].

Together with [[smooth ∞-groupoids]] smooth spectra sit inside the [[tangent cohesive (∞,1)-topos]] over smooth manifolds. By the discussion [there](tangent+cohesive+∞-topos#CohesiveAndDifferentialRefinement), every smooth spectrum sits in a hexagonal [[differential cohomology diagram]] which exhibits it ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)) as the moduli of a generalized [[differential cohomology]] theory  (in generalization of how every ordinary spectrum, via the [[Brown representability theorem]], corresponds to a bare [[generalized (Eilenberg-Steenrod) cohomology theory]]).

## Properties

### From chain complexes of smooth modules
 {#FromChainComplexesOfSmoothModules}

+-- {: .num_defn}
###### Definition

Write 

* $Smooth0Type \coloneqq Sh(SmthMfd)$ for the [[topos]] of [[smooth spaces]];

* $\mathbf{R} \in Smooth0Type$ for the sheaf of [[real number]]-valued [[smooth functions]] (the canonical [[line object]] in $Smooth0Type$);

* $\mathbf{R} Mod$ for the category of [[abelian sheaves]] over smooth manifolds which are $\mathbf{R}$-[[modules]].

=--

+-- {: .num_defn #RModulesAsInfinityPresheaves}
###### Definition (Notation)

Let $C_\bullet \in Ch_\bullet(\mathbf{R}Mod)$ be a [[chain complex]] (unbounded) of [[abelian sheaves]] of $\mathbf{R}$-modules. Via the projective [[model structure on functors]] this defines an [[(∞,1)-presheaf]] of [[chain complexes]]

$$
  Ch_\bullet(\mathbf{R}Mod)
  \longrightarrow
  Sh(SmthMfd, Ch_{\bullet})
  \longrightarrow
  L_{qi} PSh(SmthMfd, Ch_\bullet)
  \simeq
  PSh_\infty(SmthMfs, Ch_\bullet)
  \,.
$$

We still write $C_\bullet\in PSh_\infty(SmthMfd, Ch_\bullet)$ for this [[(∞,1)-presheaf]] of chain complexes. 

=--

+-- {: .num_prop}
###### Proposition

Under the [[stable Dold-Kan correspondence]]

$$
  DK \;\colon\; Ch_\bullet \longrightarrow Spectra
$$

a chain complex of $\mathbf{R}$-modules $C_\bullet \in Ch_\bullet(\mathbf{R}Mod)$, regarded as an [[(∞,1)-presheaf]] of spectra on $SmthMfd$ as in def. \ref{RModulesAsInfinityPresheaves}, is already an [[(∞,1)-sheaf]], hence a smooth spectrum (i.e. without further [[∞-stackification]]).

=--

This appears as ([Bunke-Nikolaus-V&#246;lkl 13, lemma 7.12](#BunkeNikolausVoelkl13)).

## Examples

### De Rham spectra
 {#ExamplesDeRhamSpectra}

Write $Ch_\bullet$ for the [[(∞,1)-category of chain complexes]] (of [[abelian groups]], hence over the [[ring]] $\mathbb{Z}$ of [[integers]]). It is convenient to choose for $A_\bullet \in Ch_\bullet$ the grading convention

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    A_{-1}
    \\
    \downarrow
    \\
    A_0
    \\
    \downarrow
    \\
    A_1
    \\
    \downarrow
    \\
    \vdots
   }
$$

such that under the [[stable Dold-Kan correspondence]] 

$$
  DK \;\colon\; Ch_\bullet \stackrel{}{\longrightarrow} Spectra
$$

the [[homotopy groups]] of spectra relate to the [[homology groups]] by

$$
  \pi_n(DK(A_\bullet)) \simeq  H_{-n}(A_\bullet)
  \,.
$$

In particular for $A \in $ [[Ab]] an [[abelian group]] then $A[n]$ denotes the chain complex concentrated on $A$ in degree $-n$ in this counting.

The grading is such as to harmonize well with the central example of a sheaf of chain complexes over the site of [[smooth manifolds]], which is the [[de Rham complex]], regarded as a [[smooth spectrum]] via the discussion at _[smooth spectrum -- from chain complexes of smooth modules](smooth+spectrum#FromChainComplexesOfSmoothModules)_

$$
  \Omega^\bullet \in Sh_\infty(SmthMfd, Ch_\bullet) \longrightarrow Sh_\infty(SmthMfd, Spectra) \hookrightarrow T \mathbf{H}
$$

$$
  \Omega^{\bullet} \;\colon\;  X\mapsto (\cdots \to 0 \to 0 \to \Omega^0(X) \stackrel{\mathbf{d}}{\to} \Omega^1(X)\stackrel{\mathbf{d}}{\to} \cdots)
$$

with $\Omega^0(X) = C^\infty(X, \mathbb{R})$ in degree 0.

We also need for $n \in \mathbb{N}$ the truncated sheaf of complexes

$$
  \Omega^{\bullet \geq n} \in Sh_\infty(SmthMfd, Ch_\bullet) \longrightarrow Sh_\infty(SmthMfd, Spectra) \hookrightarrow T \mathbf{H}
$$

$$
  \Omega^{\bullet \geq n} \;\colon\;  X\mapsto (\cdots \to 0 \to 0 \to \Omega^n(X) \stackrel{\mathbf{d}}{\to} \Omega^{n+1}(X)\stackrel{\mathbf{d}}{\to} \cdots)
$$

with $\Omega^n(X)$ in degree $n$.

More genereally, for $C \in Ch_\bullet$ any [[chain complex]], there is $(\Omega \otimes C)^{\bullet \geq n}$ given over each manifold $X$ by the [[tensor product of chain complexes]] followed by truncation.

Hence

$$
  (\Omega \otimes C)^{\bullet \geq n}
  = 
  (\cdots \to 0 \to 0 \to \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-k} \stackrel{\mathbf{d} \pm d_{C}}{\to} \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-k+1}\stackrel{\mathbf{d}\pm d_{C}}{\to} \cdots)
 \,.
$$

### Algebraic K-theory of smooth manifolds

see at _[[algebraic K-theory of smooth manifolds]]_


## References

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

[[!redirects smooth spectra]]