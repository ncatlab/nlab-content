
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn }
###### Definition

A **pre-abelian category** is an [[additive category]] (an [[Ab-enriched category]] with finite [[biproduct|biproducts]]) such that every [[morphism]] has a [[kernel]] and a [[cokernel]].  

=--

Equivalently:

+-- {: .num_defn }
###### Definition

A **pre-abelian category** is an [[Ab-enriched category]] with all [[finite limits]] and finite [[colimits]]. 

=--

+-- {: .num_prop }
###### Proposition

These two definitions are indeed equivalent. 

=--

+-- {: .proof}
###### Proof

By the discussion [here](finite+limit#Properties) the existence of finite limits is equivalent to that of finite [[products]] and [[equalizers]]. But an [[equalizer]] of two morphisms $f$ and $g$ in an [[Ab]]-[[enriched category]] is the same as a [[kernel]] of $f-g$. Dually for finite colimits, coequalizers and cokernels.

=--

## Properties

+-- {: .num_prop}
###### Proposition

For every object $c\in C$ in a pre-abelian category, the operations of [[kernel]] and [[cokernel]] form a [[Galois connection]] between the [[preorders]] $Sub(c)$ of [[monomorphisms]] ([[subobjects]]) into $c$ and $Quot(c)$ of [[epimorphisms]] out of $c$.  

In particular, $f:b\to c$ is a [[kernel]] iff $f = ker(coker(f))$ and dually.  

=--

+-- {: .num_prop #DecompositionOfMorphisms}
###### Proposition

Every [[morphism]] $f:A\to B$ in a pre-abelian category has a canonical decomposition

$$
  A\stackrel{p}\to \coker(\ker f)\stackrel{\bar{f}}\to\ker(\coker f)\stackrel{i}\to B
$$

where $p$ is a [[cokernel]], hence  an [[epimorphism|epi]], and $i$ is a [[kernel]], and hence [[monomorphism|monic]].

=--

+-- {: .num_remark}
###### Remark

If $\bar f$ in the above decomposition is always an [[isomorphism]], then the pre-abelian category is called an _[[abelian category]]_.

=--


## Examples 

* Of course every [[abelian category]] is pre-abelian.

* The category $TF$ of [[torsion subgroup|torsion-free]] [[abelian groups]] is [[reflective subcategory|reflective]] in all of [[Ab]].  Therefore, it is a complete and cocomplete $Ab$-enriched category, and therefore in particular pre-abelian.  However, it is not abelian; the monomorphism $2:\mathbb{Z}\to \mathbb{Z}$ is not a kernel.

## Related concepts

The concept "pre-abelian category" is part of a sequence of concepts of [[additive and abelian categories]].

[[!redirects pre-abelian categories]]
[[!redirects preabelian categories]]
[[!redirects preabelian category]]
