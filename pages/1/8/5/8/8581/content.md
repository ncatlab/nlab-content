
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _smooth groupoid_ is the first generalization of the notion of _[[smooth space]]_ to [[higher differential geometry]].
A _smooth groupoid_ is a [[stack]] on the [[site]] [[CartSp]]${}_{smooth}$. This is equivalently an [[n-truncated object in an (infinity,1)-topos|1-truncated]] [[smooth infinity-groupoid]].


## Definition


A _[[smooth stack]]_ or _[[smooth groupoid]]_ is a [[stack]] on the site [[SmoothMfd]] of [[smooth manifolds]] or equivalently (and often more conveniently) on its [[dense subsite]] [[CartSp]] of just [[Cartesian spaces]] $\mathbb{R}^n, n \in \mathbb{N}$ and [[smooth functions]] between them, equipped with the standard [[coverage]] of [[good open covers]].

We write 

$\;\;\; $[[SmoothGrpd]] $\coloneqq Sh_{(2,1)}(CartSp) \simeq L_{lhe} Func(CartSp^{op}, Grpd) $ 

for the [[(2,1)-category]] of [[stacks]] on this site, equivalently the result of taking [[groupoid]]-valued [[presheaves]] and then  [[simplicial localization|universally]] turning local (as seen by the [[coverage]]) [[equivalences of groupoids]] into global [[equivalence in an (infinity,1)-category]].

By generalizing here [[groupoids]] to general [[Kan complexes]] and [[equivalences of groupoids]] to [[homotopy equivalences]] of Kan complexes, one obtains _smooth [[∞-stacks]]_ or _[[smooth ∞-groupoids]]_, which we write 

$\;\;\; $[[Smooth∞Grpd]] $\coloneqq Sh_{(\infty,1)}(CartSp) \simeq L_{lhe} Func(CartSp^{op}, KanCplx) $. 

We often write $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] for short.

By the [[(∞,1)-Yoneda lemma]] there is a sequence of [[full and faithful (∞,1)-functor|faithful inclusions]]

$\;\;\;$ [[SmoothMfd]] $\hookrightarrow$ [[SmoothGrpd]] $\hookrightarrow$ [[Smooth∞Grpd]].

This induces a corresponding inclusion of [[simplicial objects]] and hence of [[groupoid objects in an (∞,1)-category|groupoid objects]]

$$
  LieGrpd \hookrightarrow Grpd_\infty(SmoothMfd)  \hookrightarrow  Grpd_\infty(Smooth\infty Grpd)
  \,.
$$

For $\mathcal{G}_\bullet \in Grpd_\infty(\mathbf{H})$ a groupoid object we write 

$$
  \mathcal{G}_0 \to \mathcal{G} \coloneqq \underset{\longrightarrow}{\lim}_{n} \mathcal{G}_n
$$

for its [[(∞,1)-colimit|(∞,1)-colimiting]] [[cocone]], hence $\mathcal{G} \in \mathbf{H}$ (without subscript decoration) denotes the [[realization]] of $\mathcal{G}_\bullet$ as a single object in $\mathbf{H}$.

By the [[Giraud-Rezk-Lurie axioms]] of the [[(∞,1)-topos]] $\mathbf{H}$ this morphism $\mathcal{G}_0 \to \mathcal{G}$ is a [[1-epimorphism]] -- an [[atlas]] -- and its construction establishes is an [[equivalence of (∞,1)-categories]] $Grpd_\infty(\mathbf{H}) \simeq \mathbf{H}^{\Delta^1}_{1epi}$, hence morphisms $\mathcal{G}_\bullet \to \mathcal{K}_\bullet$ in $Grpd_\infty(\mathbf{H})$ are equivalently [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    \mathcal{G}_0 &\to& \mathcal{K}_0
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathcal{G} &\to& \mathcal{K}
  }
  \,.
$$

This is evidently more constrained that just morphisms 

$$
  \mathcal{G} \to \mathcal{K}$ in $\mathbf{H}
$$

by themselves. The latter are the "generalized" or [[Morita morphisms]] between the groupoid objects $\mathcal{G}_\bullet$, $\mathcal{K}_\bullet$. These can be modeled as $\mathcal{G}_\bullet$-$\mathcal{K}_\bullet$-[[bibundles]].




## Examples

Every [[Lie groupoid]] presents a smooth groupoids. Those of this form are also called [[differentiable stacks]].

A [[0-truncated]] smooth groupoid is equivalently a [[smooth space]]. 

For $G$ a [[smooth group]], its [[delooping]] $\mathbf{B}G$ is a smooth groupoid, the [[moduli stack]] of smooth $G$-[[principal bundles]].

## Related concepts

* [[moduli stack]]

* [[centrally extended groupoid]]

[[!redirects smooth groupoids]]

[[!redirects smooth group]]
[[!redirects smooth groups]]

[[!redirects smooth stack]]
[[!redirects smooth stacks]]

[[!redirects SmoothGrpd]]
