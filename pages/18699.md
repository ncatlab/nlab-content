
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Local colimits

* table of contents
{: toc}

## Definition

A **local colimit** in a [[bicategory]] is a [[colimit]] in a [[hom-category]] that is [[preserved limit|preserved]] by the [[composition]] [[functor]].  A bicategory **has local colimits** of some shape if its hom-categories have colimits of those shapes that are preserved in each variable by the composition functors.  A bicategory with all (small) local colimits is called **locally cocomplete**.

## Examples

* In the [[delooping]] $\mathbf{B} V$ of a [[monoidal category]] $V$, any colimit preserved in each variable by the tensor product gives a local colimit.  In particular, in the delooping of a [[closed monoidal category]] all colimits are local colimits.
* More generally, in a [[closed bicategory]] all colimits in hom-categories are local colimits.
* If $B$ has local coproducts, then we can construct its bicategory $Mat(B)$, whose objects are families of objects of $B$ and whose morphisms are  [[matrices]], which also has local coproducts.
* If $B$ has local coequalizers, then we can construct its bicategory $Mod(B)$, whose objects are [[monads]] in $B$ and whose morphisms are [[bimodules]], which also has local coequalizers.
* Thus, if $B$ is locally cocomplete, we can construct its bicategory $Prof(B) = Mod(Mat(B))$, whose objects are [[category enriched in a bicategory|categories enriched in]] $B$ and whose morphisms are profunctors, which is also locally cocomplete.  In particular, [[Prof]] = $Prof(\mathbf{B} Set)$ is locally cocomplete.

[[!redirects local colimits]]
[[!redirects bicategory with local colimits]]
[[!redirects bicategories with local colimits]]
[[!redirects locally cocomplete bicategory]]
[[!redirects locally cocomplete bicategories]]
