

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

Let $E$ be a [[locally small category]] with all small [[colimit]]s. An object $e$ of $E$ is called **tiny** or **small-[[projective object]]** ([Kelly, &#167;5.5](#Kelly)) if the [[hom-functor]] $E(e, -) : E \to Set$ preserves small colimits.

More generally, for $V$ a [[cosmos]] and $E$ a $V$-[[enriched category]], $e \in E$ is called tiny if $E(e,-) : E \to V$ preserves all small colimits.
=--


## Remarks

* Since being an [[epimorphism]] is a "colimit-property" (a morphism is epic iff its pushout with itself consists of identities), if $e$ is tiny then $E(e,-)$ preserves epimorphisms, which is to say that $e$ is [[projective object|projective]] (with respect to epimorphisms).  This is presumably the origin of the term "small-projective", i.e. the corepresentable functor preserves small colimits instead of just a certain type of finite one.

* If $E$ is [[cartesian closed category|cartesian closed]] and the inner hom $(-)^e$ has a [[right adjoint]] (and hence preserves all colimits), $e$ is called [[infinitesimal object|atomic]] or [[infinitesimal object|infinitesimal]]. The right adjoint is sometimes called an [[amazing right adjoint]], particularly in the context of [[synthetic differential geometry]]. If $E$ is a sheaf topos, then tiny objects and infinitesimal objects coincide, by the [[adjoint functor theorem]].


## Examples

* In a [[presheaf]] category every [[representable functor|representable]] is a tiny object: since colimits of presheaves are computed objectwise (see [[limits and colimits by example]]) and using the [[Yoneda lemma]] we have for $U$ a [[representable]] functor and $F : J \to PSh$ a diagram that

  $$
    Hom(U, \lim_\to F) \simeq (\lim_\to F)(U) \simeq \lim_\to F(U)
  $$

  where now the last [[colimit]] is in [[Set]].


* Any [[retract]] of a tiny object is tiny, since [[split idempotent|splitting of idempotents]] is an [[absolute colimit]] (see also [Kelly, prop. 5.25](#Kelly)).  Thus, in a presheaf category, any retract of a representable functor is tiny.

  In fact the converse also holds: any tiny object in a presheaf category is a retract of a representable.  Thus, if the domain category is [[Cauchy complete category|Cauchy complete]] (has split idempotents), then every tiny presheaf is representable; and more generally the Cauchy completion or [[Karoubi envelope]] of a category can be defined to consist of the tiny presheaves on it.


## References

The term _small projective object_ is used in  section 5.5. of 

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))
{#Kelly}

[[!redirects small-projective object]]
[[!redirects small-projective objects]]
[[!redirects small-projective]]

[[!redirects tiny objects]]
[[!redirects tiny]]
