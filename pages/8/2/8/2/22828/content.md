
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc} 

## Idea

For $\mathcal{X}$ an [[orbifold]], (or, more generally, any [[differentiable stack]] or yet more generally a [[smooth ∞-groupoid]]), its *free loop orbifold* (*free loop stack*) is the [[mapping stack]] into it out of the [[circle]] $S^1$ (the latter regarded as a [[smooth manifold]] and hence as an [[orbifold]]/[[differentiable stack]] in the canonical way):

$$
  \mathcal{L} \mathcal{X}
  \;\coloneqq\;
  \big[
    S^1, \, \mathcal{X} 
  \big]
  \,.
$$

For $\mathcal{X} = X$ a [[smooth manifold]], this reduces to the [[smooth loop space]] of $X$, which is still a [[Fréchet manifold]]. 

More generally, for 

$$
  \label{GoodOrbifoldQuotientPresentation}
  \mathcal{X} \simeq X \!\sslash\! G
$$ 

a [[good orbifold]] equivalent to a [[global quotient orbifold]] of $X$ be a [[discrete group|discrete]] [[group action]], the free loop orbifold combines the properties of the [[smooth loop space]] of $X$ with the properties of the *[[inertia orbifold]]* of $\mathcal{X}$ (see Remark \ref{DifferentNotionsOfLoopOrbifolds}).

Concretely, for $\mathcal{U}_{S^1} \xrightarrow{\;\;\simeq\;\;} S^1 $ the [[Cech groupoid]] of a  [[good open cover]] of the circle, the free loop orbifold of a [[good orbifold]] (eq:GoodOrbifoldQuotientPresentation) has [[plots]] of shape $\mathbb{R}^n$ given by the following [[hom-groupoid]] of [[Lie groupoids]]:

\[
  \label{PlotsOfTheFreeLoopOrbifold}
  \mathbf{H}
  \big(
    \mathbb{R}^n,\,
    \mathcal{L}\mathcal{X}
  \big)
  \;\simeq\;
  LieGroupoids
  \big(
    \mathcal{U}_{S^1} \times \mathbb{R}^n,
    \,
    (X \times G \rightrightarrows X)
  \big)
  \,.
\]

Here $\mathbf{H}$ denotes the correct [[(2,1)-category]] of [[differentiable stacks]] (see at [[Smooth∞Groupoid]]), while $LieGroupoids$ is its presentation by [[Lie groupoids]] ([[groupoid objects]] [[internalization|internal]] to [[SmoothManifolds]], where [[Morita morphisms]] are not [[localization|inverted]]).

Notice here how:

* the [[morphisms]] in the [[Cech groupoid]] detect the non-trivial morphisms in $\mathcal{X}$ as for an [[inertia orbifold]],

* while the [[cohesion|cohesive]] smooth structure on the space of objects of the Cech groupoid detects smooth [[paths]] in $X$.

A general plot (eq:PlotsOfTheFreeLoopOrbifold) is a circular sequence of smooth paths in $X$ whose endpoints are cyclically related by the [[group action]] of $G$.





\begin{remark}\label{DifferentNotionsOfLoopOrbifolds}
**(different notions of loop orbifolds)** \linebreak
For the case of [[orbifolds]], the [[cohesion]] of the loops leads to a distinction between various in-equivalent notions of "[[free loop spaces]]" of orbifolds:

Let:

* $\mathcal{X} \,\in\, SmoothGroupoids_\infty$ be an [[orbifold]], regarded as a [[smooth groupoid]], regarded as a [[differentiable stack]].

* $S^1 \,\in\, SmoothManifolds \hookrightarrow SmoothGroupoids_\infty$ be the [[circle]] with its standard [[cohesion|cohesive]] structure as a [[smooth manifold]], and hence as a [[differentiable stack]].

  Notice that the [[shape modality|shape]] of $S^1$ (in the [[cohesive (infinity,1)-topos|cohesive]]) [[(2,1)-topos]] of [[smooth ∞-groupoids]] is the [[delooping groupoid]] of the [[integers]], regarded as a [[discrete object|discrete]] smooth groupoid

  $$
    &#643;S^1
    \;\simeq\;
    \mathbf{B}\mathbb{Z}
    \;\;\;
    \in
    Groupoids
    \xrightarrow{ \; Disc\; }
    SmoothGroupoids
     \;
    \,.
  $$

* $[-,-]$ denote the [[mapping stack]]-construction.

Then we have:

1. The *cohesive [[free loop orbifold]]* of $\mathcal{X}$ is 

   $$
     \mathcal{L}\mathcal{X}
     \;=\;
     \big[ S^1, \, \mathcal{X} \big]
     \,.
   $$

1. The *[[inertia orbifold]]* of $\mathcal{X}$ is

   $$
     \Lambda \mathcal{X}
     \;\simeq\;    
     \big[ &#643;S^1, \, \mathcal{X} \big]
     \;\simeq\;
     \big[ \mathbf{B}\mathbb{Z}, \, \mathcal{X} \big]
     \;\simeq\;
     \mathcal{X} \times^h_{\mathcal{X} \times \mathcal{X}} \mathcal{X}
     \,,
   $$

   which is the actual [[free loop space object]] formed in [[smooth groupoids]].


The [[shape modality]]-[[unit of a monad|unit]] $\mathcal{A} \xrightarrow{ \eta_{\mathcal{A}}} &#643; \mathcal{A}$ induces a canonical comparison morphism between the two

$$
  \Lambda \mathcal{X}
  \;=\;
  \big[ &#643;S^1, \, \mathcal{X} \big]
    \xrightarrow{ \; [\eta_{S^1},\mathcal{X}]\; }
  \big[ S^1, \, \mathcal{X} \big]
  \;=\;
  \mathcal{L} \mathcal{X}
  \,.
$$

When $\mathcal{X} \simeq X \!\sslash\! G$ is a [[global quotient orbifold]] of a [[smooth manifold]] $X$ (for instance for a [[good orbifold]], but $X$ could more generally be a [[diffeological space]] for the present discussion), then this inclusion is the [[n-truncated object of an (infinity,1)-category|faithful inclusion]] of the *cohesively constant loops*, namely those that map to points in the naive quotient space of $\mathcal{X}$.
\end{remark}

## Related concepts

* [[inertia orbifold]], [[Huan's inertia orbifold]]

* [[free loop space]], [[derived loop space]]

## References

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Loop groupoids, gerbes, and twisted sectors on orbifolds_, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.), *[[Orbifolds in Mathematics and Physics]]*, Madison, WI, 2001, in: Contemp. Math. __310__, Amer. Math. Soc., Providence, RI, 2002, pp. 163&#8211;184, ([math.AT/0110207](http://arxiv.org/abs/math/0110207), [ISBN:978-0-8218-2990-5](https://bookstore.ams.org/conm-310), [MR2004c:58043](http://www.ams.org/mathscinet-getitem?mr=1950946))

A [[Fréchet–Lie group|Fréchet–Lie]] groupoid presenting the cohesive free loop orbifold:

* [[David Michael Roberts]], [[Raymond Vozzo]], _Smooth loop stacks of differentiable stacks and gerbes_, [[Cahiers de Topologie et Géométrie Différentielle Catégoriques]], Vol LIX no 2 (2018) pp 95-141 [journal version](http://cahierstgdc.com/index.php/volume-lix-2018), [arXiv:1602.07973](https://arxiv.org/abs/1602.07973).




[[!redirects free loop orbifolds]]

[[!redirects free loop stack]]
[[!redirects free loop stacks]]

[[!redirects loop orbifold]]
[[!redirects loop orbifolds]]

[[!redirects loop stack]]
[[!redirects loop stacks]]



