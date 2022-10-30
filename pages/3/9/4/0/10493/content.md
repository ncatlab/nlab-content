
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### (Co-)Cartesian cubical diagrams

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]].

+-- {: .num_defn #StronglyCoCartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{C}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{C}$, is called _strongly homotopy co-cartesian_ or just _strongly co-cartesian_, if all its 2-dimensional square faces are [[homotopy pushout]] [[diagrams]] in $\mathcal{C}$.

=--

+-- {: .num_defn #Cartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{D}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{D}$, is called _homotopy cartesian_ or just _cartesian_, if its "first" object exhibits a [[homotopy limit]]-[[cone]] over the remaining objects.

=--

(e.g. [Lurie, def. 6.1.1.2 with prop. 6.1.1.15](#HigherAlg))

### $n$-Excisive functors

+-- {: .num_defn}
###### Definition

An [[(∞,1)-functor]] $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ is **$n$-excisive** for $n \in \mathbb{N}$ (or _polynomial_ of degree at most $n$) if whenever $X$ is a strongly cocartesian $(n + 1)$-[[cube]] in $\mathcal{C}$, def. \ref{StronglyCoCartesian}, then $F(X)$ is a cartesian cube in $\mathcal{D}$, def. \ref{Cartesian}. 
 
A 1-excisive (∞,1)-functor is often just called _[[excisive (∞,1)-functor]]_ for short.

An $(\infty,1)$-functor which is $n$-excisive for some $n \in \mathbb{N}$ is also called a _[[polynomial (∞,1)-functor]]_.

=--

+-- {: .num_remark}
###### Remark

This notion is comparable to how a [[polynomial]] of degree at most $n$ is determined by its values on $n + 1$ distinct points. 

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

+-- {: .num_prop #nExcisiveApproximations}
###### Proposition

The inclusion of def. \ref{InclusionOfNExcisive} is [[left exact (∞,1)-functor|lex]] [[reflective sub-(∞,1)-category|reflective]], hence the inclusion functor has a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  P_n \;\colon\; Func(\mathcal{C}, \mathcal{D}) \longrightarrow
  Exc^n(\mathcal{C}, \mathcal{D})
$$

which moreover is [[left exact (infinity,1)-functor|left exact]] (preserves [[finite (∞,1)-limits]]).

=--

This is essentially the statement of ([Goodwillie 03, theorem 1.8](#Goodwillie03)). In the above form it appears explicitly as ([Lurie, theorem 6.1.1.10](#HigherAlg)). The construction of the reflector$P_n$ is in ([Lurie, constrution 6.1.1.27](#HigherAlg)).

+-- {: .num_cor}
###### Corollary

For $\mathcal{D} = \mathbf{H}$ an [[(∞,1)-topos]], then for all $n \in \mathbb{N}$ we have that

$$
  Exc^n(\mathcal{C}, \mathbf{H}) \in (\infty,1)Topos
$$

is an [[(∞,1)-topos]]. (For $n  \gt 1$ this is in general _not_ a  [[hypercomplete (∞,1)-topos]], even if $\mathbf{H}$ is.)

=--

This observation is due to [[Charles Rezk]]. It appears as ([Lurie, remark 6.1.1.11](#HigherAlg)).

+-- {: .num_remark}
###### Remark

As $n$ ranges, the tower of $n$-excisive approximations of an  $(\infty,1)$-functor, accordding to prop. \ref{nExcisiveApproximations}, forms a tower [[analogy|analogous]] to the the [[Taylor series]] of a [[smooth function]]. This is called the [[Goodwillie-Taylor tower]]

$$
  \cdots \to P_{n+1} F \to P_n F \to \cdots \to P_1 F \to P_0 F
  \,.
$$

If this converges to $F$, then $F$ is analogous to an [[analytic function]] and is called an _[[analytic (∞,1)-functor]]_.

=--

+-- {: .num_defn}
###### Definition

In the situation of def. \ref{nExcisiveApproximations}, the functors $F$ for which $P_{n-1}F \simeq \ast$  (hence the $P_{n-1}$ [[anti-modal types]]) are called $n$-[[reduced (∞,1)-functors]].

=--

(e.g. [Lurie, def. 6.1.2.1](#HigherAlg))

### Homogeneous pieces

(...)

+-- {: .num_prop}
###### Proposition


Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]] and with [[terminal object in an (∞,1)-category|terninal object]]. Let $\mathcal{D}$ be a [[pointed category|pointed]] [[Goodwillie-differentiable (∞,1)-category]]. Write $\mathcal{C}^{\ast/}$ for the [[pointed objects]] in $\mathcal{C}$.

Then for all natural numbers $n \geq 1$ composition with the [[forgetful functor]] $\mathcal{C}^{\ast/} \to \mathcal{C}$ induces an [[equivalence of (∞,1)-categories]]

$$
  Homog^n(\mathcal{C},\mathcal{D}) \stackrel{\simeq}{\longrightarrow} Homog^n(\mathcal{C}^{\ast/}, \mathcal{D})
$$

=--

([Lurie, prop. 6.1.2.11](#HigherAlg))


## Examples

### Goodwillie $n$-jets
 {#GoodwillienJets}

Write $\infty Grpd_{fin}$ for the [[(∞,1)-category]] of [[finite homotopy types]], hence those freely generated by [[finite (∞,1)-colimits]] from the point. Write $\infty Grpd_{fin}^{\ast/}$ for the [[pointed object|pointed]] finite homotopy types.


+-- {: .num_example}
###### Example

For $\mathbf{H}$ an [[(∞,1)-topos]] we have that

* $Exc^0(\infty Grpd_{fin}^{\ast/},\mathbf{H}) \simeq \mathbf{H}$ is the collection of constant functors, hence the original [[(∞,1)-topos]] itself;

* $Exc^1(\infty Grpd_{fin}^{\ast/},\mathbf{H}) \simeq T\mathbf{H}$ is the collection of [[parameterized spectra]] in $\mathbf{H}$, hence the [[tangent (∞,1)-topos]] of $\mathbf{H}$.

Hence one might refer to the tower of toposes

$$
  \cdots \to J^n \mathbf{H} \to \cdots \to J^2 \mathbf{H} \to T \mathbf{H} \to \mathbf{H}
$$


with 

$$
  J^n \mathbf{H} \coloneqq Exc^n(\infty Grpd^{\ast/}, \mathbf{H})
$$

the tower of "[[Goodwillie calculus|Goodwillie]] [[jet (∞,1)-categories]]" of $\mathbf{H}$.

=--

see ([Lurie, def. 1.4.2.8 and around p. 823](#HigherAlg))



## Related concepts

* [[Goodwillie calculus]]

  * [[Goodwillie-Taylor tower]]

  * [[analytic (∞,1)-functor]]

* [[polynomial (∞,1)-functor]]


## References

The notion of $n$-excisive functors was introduced in 

* [[Thomas Goodwillie]], _Calculus II, Analytic functors_, K-Theory 5 (1991/92), no. 4, 295-332

The [[Taylor tower]] formed by $n$-excisive functors was then studied in

* {#Goodwillie03} [[Thomas Goodwillie]], _Calculus III: Taylor Series_, Geom. Topol. 7(2003) 645-711 ([arXiv:math/0310481](http://arxiv.org/abs/math/0310481))
 

See also 

* {#Rezk08} [[Charles Rezk]], _A streamlined proof of Goodwillie's $n$-excisive approximation_ ([arXiv:0812.1324](http://arxiv.org/abs/0812.1324))

A discussion in the general abstract context of [[(∞,1)-category theory]] is in  

* {#HigherAlg} [[Jacob Lurie]], section 6.1.1 of _[[Higher Algebra]]_ 
  

A [[model category]] presentation of $\infty$-categories of $n$-excisive functors is given in 

* [[Georg Biedermann]], [[Boris Chorny]], Oliver R&#246;ndigs, _Calculus of functors and model categories_, Advances in Mathematics 214 (2007) 92-115 ([arXiv:math/0601221](http://arxiv.org/abs/math/0601221))

* [[Georg Biedermann]], Oliver R&#246;ndigs, _Calculus of functors and model categories II_ ([arXiv:1305.2834v2](http://arxiv.org/abs/1305.2834v2))

[[!redirects n-excisive (∞,1)-functors]]

[[!redirects n-excisive (infinity,1)-functor]]
[[!redirects n-excisive (infinity,1)-functors]]


[[!redirects n-excisive functor]]
[[!redirects n-excisive functors]]

[[!redirects n-excisive approximation]]
[[!redirects n-excisive approximations]]