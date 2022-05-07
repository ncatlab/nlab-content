+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A [[category]] $C$ is **well-powered** if every object has a [[small category|small]] [[partial order|poset]] of [[subobject]]s.

Assuming that by 'subobject' we mean (an [[equivalence class]] of) [[monomorphism|monomorphisms]], this means that for every object $X$, the (generally [[large category|large]]) [[preorder]]ed set of monomorphisms with codomain $X$ is equivalent to a small poset, or equivalently that this preordered set is essentially small.  Variations exist that use notions of subobject other than monomorphisms.

If $C^{op}$ is well-powered, we say that $C$ is **well-copowered** (although "cowell-powered" is also common).

## Properties

### Relation to local smallness 

A well-powered category with binary [[product|products]] is always [[locally small category|locally small]], since morphisms $f: A \to B$ can be identified with particular subobjects of $A \times B$ (their [[graph of a function|graph]]s).

Conversely, any locally small category with a [[subobject classifier]] must obviously be well-powered.  In particular, a [[topos]] is locally small if and only if it is well-powered.

There are interesting conditions and applications of the preorder on the sets of subobjects in well-powered categories, cf. e.g. [[property sup]]. 

## Examples

* Every [[Grothendieck topos]] (indeed, every [[locally small category|locally small]] [[elementary topos]]) is well-powered (by the existence of a [[subobject classifier]] and the smallness of [[hom sets]]).

* More generally, every [[locally presentable category]] is well-powered, since it is a full reflective subcategory of a presheaf topos, so its subobject lattices are subsets of those of the latter.

* Indeed, every category $C$ with a small [[dense subcategory]] $A$ is well-powered, since the [[restricted Yoneda embedding]] $C \to [A^{op},Set]$ is then fully faithful and preserves monomorphisms, so it embeds the subobject posets of $C$ as sub-posets of those of $[A^{op},Set]$.  This includes in particular all [[accessible categories]].

* On the other hand, a locally small category with a [[strong generator]] can fail to be well-powered; a counterexample is [here](https://math.stackexchange.com/a/254794).

* Every locally presentable category, indeed every [[accessible category]] with [[pushouts]], is well-*copowered*.  This is shown in [Adamek-Rosicky, Proposition 1.58 and Theorem 2.49](#AR).  Whether this is true for all accessible categories depends on what [[large cardinal]] properties hold: by Corollary 6.8 of Adamek-Rosicky, if [[Vopenka's principle]] holds then all accessible categories are well-copowered, while by Example A.19 of Adamek-Rosicky, if all accessible categories are well-copowered then there exist arbitrarily large [[measurable cardinals]].

## References

* {#AR} [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)


[[!redirects well powered category]]
[[!redirects well-copowered category]]
[[!redirects co-well-powered category]]