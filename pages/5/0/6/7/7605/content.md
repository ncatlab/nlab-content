

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Type-theoretic model categories

* table of contents
{: toc}

## Idea

[[homotopy type theory|Homotopy type theory]] has [[categorical semantics]] in suitable [[homotopical categories]] which in turn present certain [[(infinity,1)-categories]].  The additional structure of type theory corresponds to structure on these homotopical categories that makes them into a certain kind of [[fibration category]], known as a [[type-theoretic fibration category]] or a [[tribe]].

In practice, however, semantic examples of tribes naturally sit inside certain [[Quillen model categories]].  The concept of _type-theoretic model category_ refers to a model category with additional structure that in particular ensures that its subcategory of fibrant objects is a tribe, but also includes additional conditions that make it easier to use model-categorical tools to prove things about the type-theoretic behavior of that tribe.  At present it is not clear whether there is a unique "correct" notion of "type-theoretic model category"; instead there is a range of stronger or weaker hypotheses that are often useful in proofs of this sort.

Regardless, one purpose of the notion(s) is to ensure that all [[(∞,1)-categories]] with sufficient structure can be presented by a type-theoretic model category, and hence provide higher [[categorical semantics]] for [[homotopy type theory]] (without possibly [[univalence]]).  Specifically, every [[locally presentable (∞,1)-category|locally presentable]] [[locally cartesian closed (∞,1)-category]] has a presentation by a type-theoretic model category.  For more on this see also the respective sections at _[[relation between type theory and category theory]]_.

## Definitions

Some of the additional assumptions on a model category $M$ that are often useful to include when constructing semantics of type theory are:

* $M$ is [[right proper]].

* $M$ is a [[locally cartesian closed category]], or at least that pullback along [[fibrations]] has a right adjoint.

* $M$ is [[combinatorial model category|combinatorial]], or at least [[accessible model category|accessible]] and/or [[cofibrantly generated model category|cofibrantly generated]].

* The cofibrations in $M$ are the monomorphisms; or at least that they are closed under limits, preserved by pullbacks, all monomorphisms are cofibrations, and/or all fibrant objects are cofibrant.

* Acyclic cofibrations are preserved by pullback along fibrations.

* The underlying category of $M$ is a [[Grothendieck topos]], or even a [[presheaf topos]].

* $M$ is a [[simplicial model category]].

Definitions in the literature include:

* In [Arndt-Kapulkin](#AK) a "logical model category" was defined to be a model category in which pullback along any fibration has a right adjoint and acyclic cofibrations are preserved by pullback along fibrations.

* In [Shulman 15](#Shulman15) a "type-theoretic model category" was defined to be a right proper model category in which pullback along any fibration has a right adjoint and cofibrations are closed under limits.

* In [Gepner-Kock](#GK) a "combinatorial type-theoretic model category" was defined to be a right proper combinatorial locally cartesian closed model category whose cofibrations are the monomorphisms.

* In [Lumsdaine-Shulman](#LS) a "good model category" was defined to be a simplicial, right proper, locally cartesian closed model category in which every monomorphism is a cofibration and cofibrations are closed under limits, while an "excellent model category" (no relation to the similarly-named [[excellent model category]]) was defined to be a good model category that is additionally combinatorial.

## Examples

* The [[classical model structure on simplicial sets]] satisfies *all* the above properties, as does the [[injective model structure on simplicial presheaves]].

* Every [[presentable (∞,1)-category|locally presentable]] [[locally Cartesian closed (∞,1)-category]] (by the discussion <a href="locally+cartesian+closed+(infinity,1)-category#PresentationTheorem">there</a>) has a presentation by a [[right proper model category|right proper]] [[Cisinski model category]] (a combinatorial model structure on a Grothendieck topos whose cofibrations are the monomorphisms), indeed one whose underlying category is a presheaf topos.  Thus very strong conditions may be assumed without significantly restricting the class of (∞,1)-categories that can be presented.

* Another (counter-)example to keep in mind, however, is the [[canonical model structure on groupoids]], which is combinatorial and simplicial, all objects are fibrant and cofibrant, pullback along fibrations has a right adjoint, cofcibrations are closed under limits, and all monomorphisms are cofibrations; but the category $Gpd$ is not locally cartesian closed (hence not a Grothendieck topos), and not every cofibration is a monomorphism.

## Properties

### Modeling type theory

* Since fibrations are closed under composition, $M$ always models [[Σ-types]].

* If cofibrations are preserved by pullback (such as if they are the monomorphisms), then acyclic cofibrations are preserved by pullback along fibrations if and only if $M$ is right proper.  And by adjointness, if pullback $f^*$ along any fibration $f$ has a right adjoint $f_*$, then acyclic cofibrations are preserved by pullback along fibrations if and only if the functors $f_*$ (for $f$ a fibration) preserve fibrations.  This implies that $M$ models [[Π-types]].

* These $\Pi$-types satisfy [[function extensionality]] if and only if $f_*$ also preserves acyclic fibrations, or equivalently if $f^*$ preserves cofibrations ([Shulman 15, lemma 5.9](#Shulman15)).  In particular, if $M$ is right proper, cofibrations are preserved by pullback, and pullback along any fibration has a right adjoint, then $M$ models $\Pi$-types with function exensionality.

* If acyclic cofibrations are preserved by pullback along fibrations, then for any map $f:x\to y$ between fibrant objects, the functor $f^*: M/y \to M/x$ preserves acyclic cofibrations between fibrant objects of $M/y$ (i.e. fibrations over $y$); see e.g. [Shulman 17, lemma 7.2](#Shulman17) (originally due to Joyal).  This "Frobenius condition" implies that the [[path objects]] of $M$ model [[identity types]].

* [Lumsdaine-Shulman](#LS) shows that an excellent model category (in their sense, see above) models a wide class of [[higher inductive types]].

### Model-categorical constructions

* By [Gepner-Kock, Proposition 7.8](#GK), a [[semi-left-exact reflection|semi-left-exact]] [[left Bousfield localization]] of a combinatorial type-theoretic model category (in their sense, see above) is again a combinatorial type-theoretic model category.

## References

* {#AK} [[Peter Arndt]] and [[Krzysztof Kapulkin]], *Homotopy-Theoretic Models of Type Theory*, In: Ong L. (eds) Typed Lambda Calculi and Applications. TLCA 2011. Lecture Notes in Computer Science, vol 6690. Springer, Berlin, Heidelberg, [doi](https://doi.org/10.1007/978-3-642-21691-6_7)

* {#Shulman15} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))

* {#Shulman12a} [[Mike Shulman]], _[Minicourse on Homotopy Type Theory](https://home.sandiego.edu/~shulman/hottminicourse2012/)_ part 3, _Categorical models of homotopy type theory_, April 2012 ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf))

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ ([arXiv:1406.0058](http://arxiv.org/abs/1406.0058))

* {#Shulman17} [[Mike Shulman]], _Univalence for inverse EI diagrams_.  Homology, Homotopy and Applications, 19:2 (2017), p219–249, [DOI](http://dx.doi.org/10.4310/HHA.2017.v19.n2.a12), [arXiv:1508.02410](https://arxiv.org/abs/1508.02410).

* {#LS} [[Peter LeFanu Lumsdaine]] and [[Mike Shulman]], _Semantics of higher inductive types_, [arxiv:1705.07088](https://arxiv.org/abs/1705.07088).

* {#GK} [[David Gepner]] and [[Joachim Kock]], *Univalence in locally cartesian closed categories*, [arxiv:1208.1749](https://arxiv.org/abs/1208.1749)


[[!redirects presentation of homotopy type theory]]
[[!redirects categorical semantics of homotopy type theory]]

[[!redirects type-theoretic model category]]
[[!redirects type-theoretic model categories]]
[[!redirects type-theoretic model cateory]]
