<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

Let $E$ be a small, cocomplete category. An object $e$ of $E$ is **tiny** if the hom-functor $E(e, -) : E \to Set$ preserves small colimits.

Tiny objects are also sometimes called **small-[[projective object]]s**. 

+--{.query} 

_Todd_: Hm, I'm not familiar with that term. Who calls it that? (The link to [[projective object]] only mentions preservation of epimorphisms or perhaps regular epimorphisms = coequalizer maps.) 

[[Mike Shulman]]: Kelly, _Basic Concepts of Enriched Category Theory_, &#167;5.5.

Owen Biesel: Being an epimorphism can be described by a pushout diagram (take the pushout of the morphism with itself - that morphism's epic iff the two pushout legs are equal iff they are identities).  Is that why tiny objects are called "small-projective" (they preserve "small" colimits instead of just a certain finite one?)?

=--

If homming out of a tiny object even has a [[right adjoint]] and hence preserves _all_ colimits, it is called an [[infinitesimal object|atomic object]]. The right adjoint is sometimes called an [[amazing right adjoint]], particularly in the context of [[synthetic differential geometry]]. If $E$ is a sheaf topos, then tiny objects and infinitesimal objects coincide. 


#Examples#

* In a [[presheaf]] category every [[representable functor|representable]] is a tiny object: since colimits of presheaves are computed objectwise (see [[limits and colimits by example]]) and using the [[Yoneda lemma]] we have for $U$ a [[representable]] functor and $F : J \to PSh$ a diagram that

  $$
    Hom(U, \lim_\to F) \simeq (\lim_\to F)(U) \simeq \lim_\to F(U)
  $$

  where now the last [[colimit]] is in [[Set]].

In the context of [[Cauchy complete category|Cauchy completion]] of categories, every tiny object may be construed as a representable presheaf, provided that we change the site from a small category $C$ to its Cauchy completion or [[Karoubi envelope]] $\bar{C}$, which gives the same presheaves up to equivalence. 

[[!redirects small-projective object]]
