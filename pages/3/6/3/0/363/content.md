
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A *$Gray$-category* (or *Gray category*) is a certain type of [[semi-strict infinity-category|semi-strict]] [[3-category]], in which [[composition]] is strictly [[associativity|associative]] and [[unitality|unital]], but the [[interchange law]] holds only up to [[coherence|coherent]] [[isomorphism]].


## Definition

A **$Gray$-category** is a category [[enriched category|enriched]] over the [[symmetric monoidal category]] $Gray$, which is the category of [[strict 2-category|2-categories]] and [[strict 2-functors]] with the [[Gray tensor product]].


## Properties

### Coherence theorem

Gordon, Power, and Street proved that every [[tricategory]] (that is, weak 3-category) is equivalent to a $Gray$-category.  Not every tricategory is equivalent to a fully [[strict 3-category]]; any doubly-degenerate [[braided monoidal category]] which is not [[symmetric monoidal category|symmetric]] is an example.  So this is "the best one can do" in one sense, although there are other incomparable paths one can take, such as [[Simpson's conjecture|weakening units]] but keeping interchange strict.

The inclusion of $Gray$-categories into tricategories is not uniquely determined -- there is a left and right-hand version (from a remark in Example 9.3.9 of Leinster's book cited below).  However, the two possible ways are canonically equivalent as tricategories.

### Canonical model structure

Gray-categories support a [[canonical model structure]] ([Lack](#Lack))



## $Gray$-groupoids

A $Gray$-category that is a [[3-groupoid]] is a [[Gray-groupoid]].


## Examples

* The prototypical Gray-category is [[Gray]], which consists of [[strict 2-categories]], strict 2-functors, pseudonatural transformations, and modifications.

* A Gray-category with one object is called a Gray-monoid, and is a semi-strict version of a [[monoidal bicategory]].

* A doubly-degenerate Gray-category is the same as a category with two [[monoidal category|monoidal structures]] satisfying an [[exchange law]].  This is essentially the same as a [[braided monoidal category]]. ([Gurski & Cheng](#GurskiCheng))

* Since any tricategory is equivalent to a Gray-category, one can obtain examples of Gray-categories in this way.  For example, the tricategory [[Bicat]] of bicategories, pseudofunctors, pseudonatural transformations, and modifications is equivalent to some Gray-category.

  It is important to note that Bicat is *not* equivalent to Gray, due to the absence of pseudofunctors in the latter.  It is equivalent to the sub-Gray-category of Gray determined by the "flexible" or "cofibrant" 2-categories, however, since between such 2-categories any pseudofunctor is equivalent to a strict one.

* Since pseudofunctors between strict 2-categories compose strictly associatively, and between any 2-categories $A$ and $B$ there is a strict 2-category $Ps(A,B)$ of pseudofunctors, pseudonatural transformations, and modifications, one might hope that there is a Gray-category consisting of strict 2-categories, *pseudofunctors*, pseudonatural transformations, and modifications, despite the fact that the prototypical example $Gray$ contains only strict 2-functors.  However, this is false, because in a Gray-category the [[whiskering]] of 2-cells by a 1-cell is strictly functorial relative to composition of 2-cells along 1-cells, but this fails for whiskering of pseudonaturals by a pseudofunctor.

## Related pages

* [[intercategory]]

## References

* [[Robert Gordon]], [[John Power]], [[Ross Street]], _Coherence for tricategories_, Memoirs of the American Mathematical Society, **117**, 1995. ([doi:10.1090/memo/0558](http://dx.doi.org/10.1090/memo/0558))

* [[Nick Gurski]], _An algebraic theory of tricategories_, PhD thesis (2007) &lbrack;[pdf](https://dokumen.tips/documents/an-algebraic-theory-of-tricategories.html), [[Gurski-AlgebraicTricategories.pdf:file]]&rbrack;

* [[Tom Leinster]], _Higher operads, higher categories_, Cambridge University Press, 2004. ([arXiv:math/0305049](https://arxiv.org/abs/math/0305049), 
[doi:10.1017/CBO9780511525896](https://doi.org/10.1017/CBO9780511525896))

*  {#Lack} [[Steve Lack]], _A Quillen model structure for Gray-categories_, Journal of K-Theory, **8**, 2011. ([arxiv:1001.2366](http://arxiv.org/abs/1001.2366), [doi:10.1017/is010008014jkt127](https://doi.org/10.1017/is010008014jkt127))

*  {#GurskiCheng} [[Nick Gurski]], [[Eugenia Cheng]], _The periodic table of n-categories II: degenerate tricategories_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, **52**, 2011. ([link](http://www.numdam.org/item/?id=CTGDC_2011__52_2_82_0), [arxiv:0706.2307](https://arxiv.org/abs/0706.2307))

* Peter Guthmann, _The tricategory of formal composites and its strictification_, [arXiv:1903.05777](https://arxiv.org/abs/1903.05777)

* {#DiVittorio2023} [[Nicola Di Vittorio]], _A Gray-categorical pasting theorem_, Theory and Applications of Categories **39** 5 (2023) 150-171 &lbrack;[tac:39-05](http://www.tac.mta.ca/tac/volumes/39/5/39-05abs.html)&rbrack;


[[!redirects Gray category]]
[[!redirects Gray-categories]]
[[!redirects Gray categories]]
