
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

A _schematic homotopy type_ is a [[geometric ∞-stack]] over a site of [[formal duality|formal duals]] of $k$-[[associative algebras|algebras]] that models a [[homotopy type]] in generalization to how a [[dg-algebra]] models a [[rational space]] in [[rational homotopy theory]] (via the [[fundamental theorem of dg-algebraic rational homotopy theory]]): schematic homotopy types in particular model more general [[fundamental groups]]

(...)

## Definition


Let $k$ be a [[commutative ring]], $T$ the [[Lawvere theory]] of commutative $k$-[[associative algebras]]. Let $\mathbb{U} \subset \mathbb{V}$ be an inclusion of [[universes]]. Let

$$
  T \hookrightarrow C = T Alg_{\mathbb{U}} \hookrightarrow T Alg_{\mathbb{V}}
$$

be the [[site]] on [[formal duality|formal duals]] of small $k$-algebras equipped with the [[fpqc-topology]]. 

By the general discussion at [[function algebras on ∞-stacks]] we have then  the [[Isbell duality]] [[pair]] of [[adjoint (∞,1)-functors]]

$$
  (\mathcal{O} \dashv Spec) : (T Alg_{\mathbb{V}}^{\Delta})^{op}
    \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  Sh_\infty(C) =: \mathbf{H}
$$

(due to [To&#235;n 2006](#Toen06)) where the [[(∞,1)-topos]] $\mathbf{H}$ is the [[(∞,1)-category of (∞,1)-sheaves]] on $C$.


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

This appears as ([To&#235;n 2006, def 3.1.2](#Toen06))

## Properties

+-- {: .num_prop}
###### Proposition

A schematic homotopy type is in particular a [[geometric ∞-stack]] over $C$.

=--

## Examples

### de Rham schematic homotopy type

For a [[connected]] [[scheme]] $X$ let $X_{dR}$ be its [[de Rham space]]. According to [To&#235;n 2006, sect. 3.5.1](#Toen06) one finds that the functor

$$
 Ho(SchHoType/\mathbb{C}) \to Set
$$

$$
  F \mapsto Ho_{Sh_{(\infty,1)}(Alg_\mathbb{C}^{op})}(X_{dR}, F)
$$

is co-[[representable functor|representable]] by a schematic homotopy type $X^{dR}$. This is the **de Rham schematic homotopy type**. The [[cohomology]] of $X^{dR} \in Sh_{(\infty,1)}$ is the algebraic [[de Rham cohomology]] of $X$.


+-- {: .un_remark}
###### Remark

A similar construction exists in every [[cohesive (∞,1)-topos]]. See the discussion in the section <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">cohesive (∞,1)-topos -- de Rham cohomology</a>.

=--

## Related concepts

* [[real homotopy theory]]

## References

An introduction to the general theory

* [[Ludmil Katzarkov]], [[Tony Pantev]], [[Bertrand Toën]], _Schematic homotopy types and non-abelian Hodge theory_, [math.AG/0107129](http://arxiv.org/abs/math/0107129)


* {#Toen06} [[Bertrand Toën]], _Champs affines_, Selecta Math. new series **12** (2006), no. 1, 39-135 ([arXiv:math/0012219](https://arxiv.org/abs/math/0012219), [doi:10.1007/s00029-006-0019-z](https://doi.org/10.1007/s00029-006-0019-z))


The stack $Perf$ of [[perfect complexes]] is discussed for instance in section 21 of 

* {#HirschowizSimpson} [[Andre Hirschowicz]], [[Carlos Simpson]], _Descente pour les n-champs_ ([arXiv:math/9807049](http://arxiv.org/abs/math/9807049))


[[!redirects schematic homotopy types]]

[[!redirects de Rham schematic homotopy type]]

