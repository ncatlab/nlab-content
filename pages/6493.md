
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

_Inertia orbifold_ is a particular model for the [[free loop space object]] of an [[orbifold]] $X$ (or plain [[groupoid]] or [[smooth groupoid]]/[[stack]] etc.): the [[smooth groupoid]] whose [[objects]] are [[automorphisms]] in $X$ and whose [[morphisms]] are [[conjugation]] of automorphisms by morphisms in $X$. In fact for each fibered category one can construct another fibered category, its inertia and the inertia stacks are a special case of this construction.


## Definition
 {#Definition}

### For bare groupoids

\begin{definition}\label{InertiaGroupoid}
**(inertia groupoid)** \linebreak
Given a [[groupoid]] $\mathcal{G} \coloneqq (\mathcal{G}_1 \rightrightarrows \mathcal{G}_0)$ ([[internal groupoid|internal to]] [[Sets]]) with 

* set of [[objects]] $\mathcal{G}_0$ 

* set of [[morphisms]] $\mathcal{G}_1$, 

one defines its __inertia groupoid__ $\Lambda \mathcal{G}$ as the groupoid whose 

* set of objects is the set of [[automorphisms]] in $\mathcal{G}$, i.e. the [[equalizer]] of the [[source]] and [[target]] maps $s,t \colon G_1\to G_0$:

  $$
    (\Lambda \mathcal{G})_0 
    \;\coloneqq\;
    \underset{x \in \mathcal{G}_0}{\coprod}
    Aut_{\mathcal{G}}(x)
  $$

* whose [[hom-set]] from $f \colon a \to a$ to $g\colon b \to b$ consists of the [[commutative squares]] with the same vertical maps of the form 

$$
  \array{
    a 
      &\stackrel{f}{\longrightarrow}& 
    a
    \\
    {}^{\mathllap{u}}
    \big\downarrow 
      && 
    \big\downarrow {}^{\mathrlap{u}}
    \\  
    b 
    &\stackrel{g}{\longrightarrow}& 
    b
  }
$$

i.e. of the morphisms $u \colon a\to b$ in $\mathcal{G}_1$ such that $u^{-1}\circ g\circ u = f$.
\end{definition}

\begin{proposition}
The inertia groupoid (Def. \ref{InertiaGroupoid}) is [[equivalence of categories|equivalent]] (in fact [[isomorphism|isomorphic]] as [[groupoid objects]]) to the [[functor groupoid]] 

$$
  \Lambda \mathcal{G}
  \;\simeq\;
  \big[
    \mathbf{B}\mathbb{Z}, \mathcal{G}
  \big]
  \,,
$$ 

where

$$
  \mathbf{B}\mathbb{Z}
  \;\coloneqq\;
  \big(
    \mathbb{Z} \rightrightarrows \ast
  \big)
$$

denotes the [[delooping groupoid]] of the additive group of [[integers]], i.e. the [[free construction|free]] groupoid on a single object with a single [[automorphism]].
\end{proposition}

\begin{proposition}
The inertia groupoid (Def. \ref{InertiaGroupoid}) is also [[equivalence of categories|equivalent]] to the [[free loop space object]] of $\mathcal{G}$ in the [[(2,1)-category]] of groupoids.

$$
  \Lambda \mathcal{G}
  \;\simeq\;
  \mathcal{L} \mathcal{G}
  \;\coloneqq\;
  \mathcal{G} \times^h_{\mathcal{G} \times \mathcal{G}} \mathcal{G}
  \,.
$$

\end{proposition}


### For internal groupoids

The same construction can be performed for [[groupoid objects]] [[internalization|internal]] to any [[finitely complete category]], or more generally whenever the relevant [[limits]] exist.  

### For orbifolds

If a ([[differentiable stack|differential]], [[topological stack|topological]] or [[algebraic stack|algebraic]]) stack (or, in particular, an [[orbifold]]) is represented by a groupoid, then the inertia groupoid of that groupoid represents its [[inertia stack]].  In particular, an [[orbifold]] corresponds to a [[Morita equivalence]] [[equivalence class|class]] of a proper [[étale groupoid]]. The inertia groupoid $\Lambda G$ of $G$ is the Morita equivalence class of the (proper &#233;tale) [[action groupoid]] for the [[conjugation action]] of $\mathcal{G}_1$ on the subspace $S\subset G_1$ of closed loops.  

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

1. The *cohesive free loop space-orbifold* of $\mathcal{X}$ is 

   $$
     \mathcal{L}\mathcal{X}
     \;=\;
     \big[ S^1, \, \mathcal{X} \big]
     \,.
   $$

1. The *inertia orbifold* of $\mathcal{X}$ is

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


The [[shape modality]]-[[unit of a monad|unit]] $\mathcal{A} \xrightarrow{ \eta_{\mathcal{A}}} &#643; \mathcal{A}$ induced a canonical comparison morphism between the two

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

When $\mathcal{X} \simeq X \!\sslash\! G$ is a [[global quotient orbifold]] of a [[smooth manifold]] $X$ (for instance for a [[good orbifold]], but $X$ could more generally be a [[diffeological space]] for the present discussion), then this inclusion is the [[n-truncated object of an (infinity,1)-category|faithful inclusion]] of the *cohesively constant loops*, namely those that factor through points in the covering space $X$.
\end{remark}

\begin{remark}
For [[quantum field theory]] on orbifolds, or rather [[string theory]] on orbifolds, the inertia orbifold is related to so called _twisted sectors_ of the corresponding QFT.  (...)
\end{remark}


## Properties

### Skeleton for global quotient orbifolds
 {#SkeletonForGlobalQuotientOrbifolds}

\begin{proposition}\label{SkeletonOfInertiaOfProperGoodOrbifolds}
**([[skeleton]] of [[inertia orbifold]] for [[proper action|proper]] [[good orbifolds]])** \linebreak
  If $\mathcal{X} \,\simeq\, X \!\sslash\! G $ is a [[good orbifold]] presented as the [[global quotient orbifold]] of a [[smooth manifold]] with [[smooth function|smooth]] [[proper action|proper]] [[group action]] by a [[discrete group]] $G$, then its inertia orbifold is equivalent to the following [[disjoint union]] of [[global quotient orbifolds]]

$$
  \Lambda
  \big(
    X \!\sslash\! G
  \big)
  \;\simeq\;
  \underset{ [g] \in ConjCl(G) }{\coprod}
  X^g \!\sslash\! C_g
  \,,
$$

where

* $ConjCl(G) \coloneqq G /_{ad} G$ is the set of [[conjugacy classes]] of $G$;

* $X^g \coloneqq X^{\langle g\rangle}$ is the [[fixed locus]] of the action of (the [[cyclic group]] generated by) $g \in G$ (which is again a [[smooth manifold]] by the discussion [here](equivariant+differential+topology#FixedSubmanifolds));

* $C_g \subset G$ is the [[centralizer]] of $\{g\} \subset G$.

\end{proposition}


### Convolution algebra and Relation to Drinfeld double

At least for a [[finite group]] $G$, the [[groupoid convolution algebra]] of the inertia groupoid of the [[delooping groupoid]] $\mathbf{B}G$ is the [[Drinfeld double]] of the [[group convolution algebra]] of $G$.

## Related concepts

* [[Huan's inertia orbifold]]

* [[free loop space]], [[derived loop space]]


## References

Original articles:

* Tetsuro Kawasaki, _The signature theorem for V-manifolds_, Topology __17__ (1978), no. 1, 75&#8211;83 (<a href="https://doi.org/10.1016/0040-9383(78)90013-7">doi:10.1016/0040-9383(78)90013-7</a>)

Review and further development:

* [[Ernesto Lupercio]], [[Bernardo Uribe]], Section 4 of: _Inertia orbifolds, configuration spaces and the ghost loop space_, Quarterly Journal of Mathematics __55__, Issue 2, pp. 185-201 ([arxiv/math.AT/0210222](http://arxiv.org/abs/math/0210222), [doi:10.1093/qmath/hag053](https://doi.org/10.1093/qmath/hag053))

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Loop groupoids, gerbes, and twisted sectors on orbifolds_, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.), *[[Orbifolds in Mathematics and Physics]]*, Madison, WI, 2001, in: Contemp. Math. __310__, Amer. Math. Soc., Providence, RI, 2002, pp. 163&#8211;184, ([math.AT/0110207](http://arxiv.org/abs/math/0110207), [ISBN:978-0-8218-2990-5](https://bookstore.ams.org/conm-310), [MR2004c:58043](http://www.ams.org/mathscinet-getitem?mr=1950946))

* {#Moerdijk02} [[Ieke Moerdijk]], Section 6 in: _Orbifolds as Groupoids: an Introduction_, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

See also:

* [[The Stacks Project]], *[The inertia stack](https://stacks.math.columbia.edu/tag/036X)* ([more](https://stacks.math.columbia.edu/tag/034H), [more](https://stacks.math.columbia.edu/tag/034I))

In relation to [[Drinfeld doubles]]:

* [[Vladimir Hinich]], _Drinfeld double for orbifolds_, Contemporary Math. __433__, AMS Providence, 2007, 251-265,
[arXiv:math.QA/0511476](http://arxiv.org/abs/math/0511476)

In view of the [[Chern character]] for [[twisted K-theory|twisted]] [[orbifold K-theory]]:

* [[Jean-Louis Tu]], [[Ping Xu]], _Chern character for twisted K-theory of orbifolds_, Advances in Mathematics __207__ (2006) 455&#8211;483, [pdf](http://www.math.univ-metz.fr/~tu/publi/orb.pdf) (cf. sec. 2.3)


A Fréchet–Lie groupoid presenting the cohesive free loop space-orbifold is given in

* [[David Michael Roberts]], [[Raymond Vozzo]], _Smooth loop stacks of differentiable stacks and gerbes_, [[Cahiers de Topologie et Géométrie Différentielle Catégoriques]], Vol LIX no 2 (2018) pp 95-141 [journal version](http://cahierstgdc.com/index.php/volume-lix-2018/), [arXiv:1602.07973](https://arxiv.org/abs/1602.07973).


[[!redirects inertia orbifolds]]

[[!redirects inertia stack]]
[[!redirects inertia stacks]]

[[!redirects inertia groupoid]]
[[!redirects inertia groupoids]]



category: Lie theory
