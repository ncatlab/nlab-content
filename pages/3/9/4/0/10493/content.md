
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]].

+-- {: .num_defn #StronglyCoCartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{C}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{C}$, is called _strongly homotopy co-cartesian_ or just _strongly co-cartesian_, if all its 2-dimensional square faces are [[homotopy pushout]] [[diagrams]] in $\mathcal{C}$.

=--

+-- {: .num_defn #Cartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{D}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{C}$, is called _homotopy cartesian_ or just _cartesian_, if its "first" object exhibits a [[homotopy limit]]-[[cone]] over the remaining objects.

=--

+-- {: .num_defn}
###### Definition

An [[(∞,1)-functor]] $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ is **$n$-excisive** for $n \in \mathbb{N}$ (or polynomial of degree at most $n$) if whenever $X$ is a strongly cocartesian $(n + 1)$-[[cube]] in $\mathcal{C}$, def. \ref{StronglyCoCartesian}, then $F(X)$ is a cartesian cube in $\mathcal{D}$, def. \ref{Cartesian}. 
 
A 1-excisive (∞,1)-functor is called just _[[excisive (∞,1)-functor|excisive]]_ for short.

=--

+-- {: .num_remark}
###### Remark

This notion is comparable to how a [[polynomial]] of degree at most $n$ is determined by its values on $n + 1$ distinct points. This comparison is developed by the concept of a [[polynomial (∞,1)-functor]].

=--

## Properties

### $n$-Excisive approximation and reflection
 {#nExcisiveApproximation}

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]] and a [[terminal object in an (∞,1)-category|terminal object]], and let $\mathcal{D}$ be a [[Goodwillie-differentiable (∞,1)-category]]. 

+-- {: .num_defn #InclusionOfNExcisive}
###### Definition

For $n \in \mathbb{N}$

$$
  Exc^n(\mathcal{C}, \mathcal{D})
  \hookrightarrow
  Func(\mathcal{C}, \mathcal{D})
$$

for the [[full sub-(∞,1)-category]] of the [[(∞,1)-functor (∞,1)-category]] on those [[(∞,1)-functors]] which are $n$-excisive.

=--

+-- {: .num_prop}
###### Proposition

The inclusion of def. \ref{InclusionOfNExcisive} is [[left exact (∞,1)-functor|lex]] [[reflective sub-(∞,1)-category|reflective]], hence the inclusion functor has a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  P_n \;\colon\; Func(\mathcal{C}, \mathcal{D}) \longrightarrow
  Exc^n(\mathcal{C}, \mathcal{D})
$$

which preserves [[finite (∞,1)-limits]].

=--

This is essentially the statement of ([Goodwillie 03, theorem 1.8](#Goodwillie03)). In the above form it appears explicitly as ([Lurie, theorem 7.1.1.10](#HigherAlg)).

+-- {: .num_cor}
###### Corollary

For $\mathcal{D} = \mathbf{H}$ am [[(∞,1)-topos]], then for all $n \in \mathbb{N}$ we have that

$$
  Exc^n(\mathcal{C}, \mathbf{H}) \in (\infty,1)Topos
$$

is an [[(∞,1)-topos]].

=--

This observation is due to [[Charles Rezk]]. It appears as ([Lurie, remark 7.1.1.11](#HigherAlg)).

+-- {: .num_example}
###### Example

For $\mathbf{H}$ an [[(∞,1)-topos]] we have that

* $Exc^0(\mathbf{H}^{\ast/},\mathbf{H}) \simeq \mathbf{H}$ is the collection of constant functors, hence the original [[(∞,1)-topos]] itself;

* $Exc^1(\mathbf{H}^{\ast/},\mathbf{H}) \simeq T\mathbf{H}$ is the collection of [[parameterized spectra]] in $\mathbf{H}$, hence the [[tangent (∞,1)-topos]] of $\mathbf{H}$.

Hence one might refer to the tower of toposes

$$
  \cdots \to J^n \mathbf{H} \to \cdots \to J^2 \mathbf{H} \to T \mathbf{H} \to \mathbf{H}
$$

with 

$$
  J^n \mathbf{H} \coloneqq Exc^n(\mathbf{H}^{\ast/}, \mathbf{H})
$$

the tower of "[[Goodwillie calculus|Goodwillie]] [[jet (∞,1)-categories]]" of $\mathbf{H}$.

=--



## Related concepts

* [[Goodwillie calculus]]
* [[polynomial (∞,1)-functor]]


## References

The notion of $n$-excisive functors was introduced in 

* [[Thomas Goodwillie]], _Calculus II, Analytic functors_, K-Theory 5 (1991/92), no. 4, 295-332

The [[Taylor tower]] formed by $n$-excisive functors was then studied in

* [[Thomas Goodwillie]], _Calculus III: Taylor Series_, Geom. Topol. 7(2003) 645-711 ([arXiv:math/0310481](http://arxiv.org/abs/math/0310481))
 {#Goodwillie03}

A discussion in the general abstract context of [[(∞,1)-category theory]] is in section 7.1.1 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
  {#HigherAlg}

A [[model category]] presentation of $\infty$-categories of $n$-excisive functors is given in 

* [[Georg Biedermann]], Boris Chorny, Oliver R&#246;ndigs, _Calculus of functors and model categories_, Advances in Mathematics 214 (2007) 92-115 ([arXiv:math/0601221](http://arxiv.org/abs/math/0601221))

* [[Georg Biedermann]], Oliver R&#246;ndigs, _Calculus of functors and model categories II_ ([arXiv:1305.2834v2](http://arxiv.org/abs/1305.2834v2))

[[!redirects n-excisive (∞,1)-functors]]

[[!redirects n-excisive (infinity,1)-functor]]
[[!redirects n-excisive (infinity,1)-functors]]

[[!redirects n-excisive functor]]
[[!redirects n-excisive functors]]

[[!redirects n-excisive approximation]]
[[!redirects n-excisive approximations]]