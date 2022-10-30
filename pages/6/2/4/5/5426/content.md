
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _schematic homotopy type_ is a [[geometric ∞-stack]] over a site of formal duals of $k$-algebras that models a [[homotopy type]] in generalization to how a [[dg-algebra]] models a [[rational space]] in [[rational homotopy theory]]: schematic homotopy type can in particular model more general [[fundamental group]]s.

(...)

## Definition


Let $k$ be a commutative [[ring]], $T$ the [[Lawvere theory]] of commutative $k$-[[associative algebra]]s. Let $\mathbb{U} \subset \mathbb{V}$ be an inclusion of [[universe]]s Let

$$
  T \hookrightarrow C = T Alg_{\mathbb{U}} \hookrightarrow T Alg_{\mathbb{V}}
$$

be the [[site]] on formal duals of small $k$-algebras equipped with the [[fpqc-topology]]. 

By the general discussion at [[function algebras on ∞-stacks]] we have then  the [[Isbell duality]] pair of [[adjoint (∞,1)-functor]]s

$$
  (\mathcal{O} \dashv Spec) : (T Alg_{\mathbb{V}}^{\Delta})^{op}
    \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  Sh_\infty(C) =: \mathbf{H}
$$

(due to [To&#235;n](#Toen)) where the [[(∞,1)-topos]] $\mathbf{H}$ is the [[(∞,1)-category of (∞,1)-sheaves]] on $C$.


+-- {: .un_def}
###### Definition

(...) Let $Perf \in \mathbf{H}$ be the stack of [[perfect complex]]es of modules on $C$. (...)

Write $P \subset Mor(\mathbf{H})$ for the [[class]] of [[morphism]]s such that for all $p \in P$ we have that $\mathbf{H}(p,Perf)$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

This is discussed in ([HirschowitzSimpson, paragraph 21](#HirschowizSimpson)).


+-- {: .un_def}
###### Definition

A [[pointed object|pointed]] **schematic homtopy type** is the [[delooping]] $\mathbf{B}G \in \mathbf{H}$ of an [[∞-group]] $G \in \mathbf{H}$ such that

* $G$ is in the image of $Spec$, in that there is $A \in T Alg^\Delta$ such that $G \simeq Spec A$;

* $\mathbf{B}G$ is a $P$-[[local object]].

=--

This appears as ([To&#235;n, def 3.1.2](#Toen))

## Properties

+-- {: .un_lemma}
###### Observation

A schematic homotopy type is in particular a [[geometric ∞-stack]] over $C$.

=--

## Examples

### de Rham schematic homotopy type

For a [[connected]] [[scheme]] $X$ let $X_{dR}$ be its [[de Rham space]]. According to [To&#235;n, sect. 3.5.1](#Toen) one finds that the functor

$$
 Ho(SchHoType/\mathbb{C}) \to Set
$$

$$
  F \mapsto Ho_{Sh_{(\infty,1)}(Alg_\mathbb{C}^{op})}(X_{dR}, F)
$$

is co-[[representable functor|representable]] by a schematic homotopy type $X^{dR}$. This is the **de Rham schematic homotopy type**. The [[cohomology]] of $X^{dR} \in Sh_{(\infty,1)}$ is the algebraic [[de Rham cohomology]] of $X$.

## References

An introduction to the general theor

* [[Ludmil Katzarkov]], [[Tony Pantev]], [[Bertrand Toën]]], _Schematic homotopy types and non-abelian Hodge theory_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0107/0107129v5.pdf))

* [[Bertrand Toën]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

The stack $Perf$ of [[perfect complex]]es is discussed for instance in section 21 of 

* [[Andre Hirschowicz]], [[Carlos Simpson]], _Descente pour les n-champs_ ([arXiv:math/9807049](http://arxiv.org/abs/math/9807049))
{#HirschowizSimpson}

[[!redirects schematic homotopy types]]

[[!redirects de Rham schematic homotopy type]]