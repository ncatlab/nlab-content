<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

Let $E$ be a small, cocomplete category. An object $e$ of $E$ is **tiny** if the hom-functor $E(e, -) : E \to Set$ preserves small colimits.

Tiny objects are also sometimes called **small-[[projective object]]s**.

If homming out of a tiny object even has a [[right adjoint]] and hence preserves _all_ colimits it is called an [[infinitesimal object|atomic object]]. The right adjoint is called an [[amazing right adjoint]].


#Examples#

* In a [[presheaf]] category every [[representable functor|representable]] is a tiny object: since colimits of presheaves are computed objectwise (see [[limits and colimits by example]]) and using the [[Yoneda lemma]] we have for $U$ a [[representable]] functor and $F : J \to PSh$ a diagram that

  $$
    Hom(U, \lim_\to F) \simeq (\lim_\to F)(U) \simeq \lim_\to F(U)
  $$

  where now the last [[colimit]] is in [[Set]].

  This is the example of tiny objects that appear in the context of [[Cauchy complete category|Cauchy completetion]] of categories.

[[!redirects small-projective object]]
