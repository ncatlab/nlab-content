
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



# Contents
* automatic table of contents goes here
{:toc}

## Idea

A **lax functor** or **lax $n$-[[n-functor|functor]]** is a morphism of $n$-[[n-category|categories]] that is allowed to have structural cells -- compositors, associators, etc -- that need not be invertible (not even [[weak inverse|weakly]]).

This is to distinguish from [[pseudofunctor]] for which all these cells are required to be [[equivalences]].

This means that the definition of lax functor involves a choice of orientation of these structural cells which is not visible for pseudofunctors. The choice is such that cells map composites of images to images of composite. With the opposite choice one speaks of an **oplax** (or sometimes **colax**) functor**.

The term lax functor can be used for $n$-functors $F : C \to D$ whose domain $C$ is an ordinary [[category]] (regarded as an $n$-category with only trivial higher morphisms), while the codomain $D$ is often taken to be a [[2-category]].

A **normal lax functor** (sometimes called *strictly unitary*) preserves identities strictly.

There exist a similar concept for [[double category|double]] and [[multiple categories]].

## Definition

See the definition at [[pseudofunctor]], and let the [[natural isomorphisms]] in that definition be merely [[natural transformations]].

## Properties

One of the most important properties is that lax functors compose associatively and unitally: we have a category $\mathbf{BiCat}$ with [[bicategories]] as objects and lax functors as morphisms.
If we add [[icons]] as 2-cells, this becomes a [[2-category]].

## Examples

* Any [[lax monoidal functor]] gives an example. In fact [[monoidal categories]] can be presented as bicategories with one object (see [[delooping]]), and thus a lax functor $\mathbf{B}M \to \mathbf{B} N$ corresponds to a lax monoidal functor $M \to N$.

* For $D$ a [[bicategory]], lax functors $F : {*} \to D$ from the [[point]] category to $D$ are equivalent to [[monad]]s in $D$.

  The compositor of the lax functor is the monad product, the unitor is the monad unit.

  * So in particular for $V$ a [[monoidal category]] and $\mathbf{B}V$ its one-object [[delooping]] [[bicategory]], lax functors ${*} \to \mathbf{B}V$ are equivalent to [[monoid]]s in $V$.
 
* Similarly, oplax functors ${*} \to D$ are equivalent to [[comonad]]s in $D$.

* If $C$ is the [[codiscrete category]] on a set $S$, and $D$ is a [[bicategory]], lax functors $F : C \to D$ are the same as categories enriched in $D$ having $S$ as their set of objects.  

   * In particular, if $C = {*}$, then this example reduces to the first one.  

   * Another special case arises when $D = \mathbf{B}V$ for some monoidal category $V$.  Then lax functors $F : C \to D$ are the same as categories enriched in the monoidal category $V$.  

* It makes sense to ask that a functor is lax _and_ oplax in a compatible way such that ${*} \to D$ yields [[Frobenius algebra|Frobenius]] monads.

  This is of relevance in [[conformal field theory]] where Frobenius algebra objects in [[modular tensor category|modular tensor categories]] and bimodules over them play a central role.

  Some old remarks on this case are in [Note on lax functors and bimodules](http://www.math.uni-hamburg.de/home/schreiber/LaxFunc.pdf).

  This relation between lax-oplax functors and [[conformal field theory]] was developed in detail in

  * Liang Kong, Ingo Runkel, _Cardy algebras and sewing constraints, I_ ([arXiv](http://arxiv.org/abs/0807.3356))

  A general discussion of lax-oplax functors is in section 2.1 there.

+--{.query}
Isn't it odd not to require any extra condition at all on the coherence morphisms? I would have expected a definition where they are required to be split epi, or require that the codomain be a subobject of the domain. Is there a name for something like that?

[[Mike Shulman]]: One could certainly add that as a condition, but I don't think I've ever heard of anyone having a use for it, or giving it a name.  The interesting examples listed above (and others) don't use any such condition.
=--

## See also
* [[lax double functor]]

## References

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 4.1 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

* R. Street, _Two constructions on lax functors_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 13 (1972) no. 3 , p. 217-264 [numdam](http://www.numdam.org/item?id=CTGDC_1972__13_3_217_0 )

[[!redirects lax functors]]
[[!redirects oplax functor]]
[[!redirects oplax functors]]
[[!redirects colax functor]]
[[!redirects colax functors]]
[[!redirects lax n-functor]]
[[!redirects lax n-functors]]
[[!redirects oplax n-functor]]
[[!redirects oplax n-functors]]
[[!redirects colax n-functor]]
[[!redirects colax n-functors]]
[[!redirects lax 2-functor]]
[[!redirects lax 2-functors]]
[[!redirects oplax 2-functor]]
[[!redirects oplax 2-functors]]
[[!redirects colax 2-functor]]
[[!redirects colax 2-functors]]
[[!redirects normal lax functor]]
[[!redirects normal lax functors]]
