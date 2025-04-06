
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of a _premodel category_ is a relaxation of the notion of a [[model category]].
[[combinatorial model category|Combinatorial]] premodel categories form a [[2-category]]
that has all ([[small diagram|small]]) [[limits]] and [[colimits]] and has [[representing objects]] for [[Quillen bifunctors]].

The [[2-category]] of combinatorial $V$-[[enriched category|enriched]] premodel categories is the category of [[modules over a monoid]] $V$ in this [[2-category]].
It inherits the same set of properties
and additionally admits a [[model 2-category]] structure.
In this model structure, a [[left Quillen functor]] is a [[weak equivalence]]
if and only if it is a [[Quillen equivalence]].

## Definition

A __premodel category__ is a [[bicomplete category]]
equipped with a [[pair]] of [[weak factorization systems]]
$(C,AF)$ and $(AC,F)$ such that $AC\subset C$ (equivalently, $AF\subset F$).

The members of AC are called __anodyne cofibrations__ and the members of AF are called __anodyne fibrations__ (as in _[[anodyne morphism]]_).

## Criteria for model categories

[[model category|Model categories]] can be singled out among premodel categories by imposing the additional requirement that the [[class]] 

$$
  W
  \coloneqq
  AF \circ AC
  \,,
$$

obtained by [[composition|composing]] [[elements]] of $AC$ with those of $AF$, is closed under the [[2-out-of-3 property]]. To check this condition, it suffices to check certain specialized cases of 2-out-of-3 (see [Cavallo & Sattler 2022, Theorem 3.8](#csElegance)):

+-- {: .num_prop #CriteriaCases}
###### Proposition

In a premodel category, $W$ satisfies the 2-out-of-3 property if and only it the following conditions are satisfied:

1. If $g,f$ are cofibrations such that $g f$ and $g$ are anodyne cofibrations, then $f$ is an anodyne cofibration. If $g,f$ are fibrations such that $g f$ and $f$ are anodyne fibrations, then $g$ is an anodyne fibration.

1. Any (cofibration, anodyne fibration) factorization or (anodyne cofibration, fibration) factorization of a map in $W$ is an (anodyne cofibration, anodyne fibration) factorization.

1. Any composite of an anodyne fibration followed by an anodyne cofibration is in $W$.

=--

## Anodyne and trivial (co)fibrations

The notion of premodel category doesn't come with a good general notion of weak equivalence. But if a particular premodel category has a good notion of weak equivalence, such as one of [Barton](#Barton)'s _relaxed premodel categories_, one needs to distinguish between two types of cofibrations (and analogously between two types of fibrations):

* An __anodyne cofibration__ is a member of the class AC
* A __trivial cofibration__ is a cofibration that is also a weak equivalence

In principle one must also distinguish a third class of cofibrations that have the left lifting property with respect to fibrations between fibrant objects. However, in a relaxed premodel category, these are trivial cofibrations. ([Barton, Prop 3.5.2](#Barton))

## Cylindrical premodel categories
  {#Cylindrical}

A **cylindrical** premodel category is one equipped with well-behaved [[cylinder]] and [[cocylinder]] functors.
In the following, we assume that $\mathcal{E}$ is a [[finitely complete]] and [[finitely cocomplete]] category.

+-- {: .num_defn}
###### Definition

An **adjoint functorial cylinder** on $\mathcal{E}$ is a [[cylinder functor]] with a [[right adjoint]]: a pair of [[adjoint functors]] $\mathcal{E} : C \dashv P : \mathcal{E}$ together with [[natural transformations]] 
\begin{tikzcd}
Id_{\mathcal{E}} \ar[dr,"id"{below left}] \ar[r,"\delta_0"] & C \ar[d,"\epsilon"] & \ar[l,"\delta_1"{above}] Id_{\mathcal{E}} \ar[dl,"id"{below right}] \\
& Id_{\mathcal{E}}
\end{tikzcd}

=--

+-- {: .num_defn}
###### Notation

Given a cylinder functor $C \colon \mathcal{E} \to \mathcal{E}$, write $\partial \colon Id_{\mathcal{E}} + \Id_{\mathcal{E}} \to C$ for the [[copairing]] $\partial = [\delta_0,\delta_1]$.

=--

+-- {: .num_defn}
###### Definition
  {#WFSCylindrical}

Let $C \dashv P$ be an adjoint functorial cylinder on $\mathcal{E}$.
A [[weak factorization system]] $(L,R)$ on $\mathcal{E}$ is **cylindrical** if $L$ is closed under the [[pushout-product#PushoutApplication|pushout application]] $\widehat{ev}(\partial,-) \colon \mathcal{E}^{\mathbf{2}} \to \mathcal{E}^{\mathbf{2}}$.

=--

+-- {: .num_defn}
###### Definition

Let $C \dashv P$ be an adjoint functorial cylinder on $\mathcal{E}$.
A premodel category (C,AF) and (AC,F) is **cylindrical** when (C,AF) and (AC,F) are cylindrical and the [[pushout-product#PushoutApplication|pushout applications]] $\widehat{ev}(\delta_0,-), \widehat{ev}(\delta_1,-) \colon \mathcal{E}^{\mathbf{2}} \to \mathcal{E}^{\mathbf{2}}$ send cofibrations to anodyne cofibrations.

=--

+-- {: .num_defn}
###### Note

This notion is distinct from [[Richard Williamson|Richard Williamson's]] [[cylinder functor#CylindricalModelStructures|cylindrical model structures]].

=--

In a cylindrical premodel structure, the first condition of Proposition \ref{CriteriaCases} implies the second ([Cavallo & Sattler 2022, Lemma 3.22](#csElegance)), yielding a simplified recognition theorem:

+-- {: .num_prop #CriteriaCasesCylindrical}
###### Proposition

In a cylindrical premodel category, $W$ satisfies the 2-out-of-3 property if and only if the following conditions are satisfied:

1. If $g,f$ are cofibrations such that $g f$ and $g$ are anodyne cofibrations, then $f$ is an anodyne cofibration. If $g,f$ are fibrations such that $g f$ and $f$ are anodyne fibrations, then $g$ is an anodyne fibration.

1. Any composite of an anodyne fibration followed by an anodyne cofibration is in $W$.

=--

## Related concepts

* [[model category]]

* [[weak model category]]

## References

* {#Barton} [[Reid William Barton]], _A model 2-category of enriched combinatorial premodel categories_. Doctoral dissertation. ([arXiv:2004.12937](https://arxiv.org/abs/2004.12937))

* {#csElegance} [[Evan Cavallo]] and [[Christian Sattler]], _Relative elegance and cartesian cubes with one connection_, 2022. ([arXiv:2211.14801](https://arxiv.org/abs/2211.14801))

[[!redirects premodel categories]]