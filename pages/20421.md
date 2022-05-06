
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _$(n \times k)$-category_ (read "n-by-k category") is an [[n-category]] [[internalization|internal]] to a $k$-category.  The term is "generic" in that it does not specify the level of strictness of the $n$-category and the $k$-category.

For example:

* A $(1 \times 0)$-category, as well as a $(0 \times 1)$-category, is precisely a [[category]].  More generally, $(n\times 0)$-categories and $(0\times n)$-categories are precisely $n$-categories.
* A $(1 \times 1)$-category is precisely a [[double category]] (either strict or weak).
* Generalizing to a 3rd axis, a $(1 \times 1 \times 1)$-category is precisely a [[triple category]], that is, a category internal to (categories internal to categories), i.e. a catgory internal to double categories, or a double category internal to categories --- which again could be strict or weak.
* An $(n \times 1)$-category is what [[Michael Batanin|Batanin]] calls a [[monoidal n-globular category]].

An $(n \times k)$-category has $(n + 1)(k + 1)$ kinds of cells.

Under suitable [[fibrant object|fibrancy]] conditions, a $(n \times k)$-category will have an underlying $(n + k)$-category (where here, $n + k$ is to be read arithmetically, rather than simply as notation). Fibrant $(1 \times 1)$-categories are known as [[framed bicategories]].

## Examples

* [[commutative ring|Commutative rings]], [[algebras]] and [[modules]] form a symmetric monoidal $(2 \times 1)$-category.
* [[conformal net|Conformal nets]] form a symmetric monoidal $(2 \times 1)$-category.

## Relationships

At least in some cases, if the structure is sufficiently strict or sufficiently fibrant, we can shift cells from $k$ to $n$.  For instance:

* A sufficiently strict $(1 \times 2)$-category canonically gives rise to a $(2 \times 1)$-category. (Cor. 3.11 in **[DH10](#DH10)**)

* Any double category (i.e. a $(1\times 1)$-category) has an underlying 2-category.

* A sufficiantly fibrant $(2\times 1)$-category has an underlying tricategory (i.e. $(3\times 0)$-category).


## Related concepts

* [[internal category]]

* [[higher category]]

* [[n-fold category]]

* [[(n,r)-category]]


## References ##

* [[Mike Shulman]], Constructing symmetric monoidal bicategories, arXiv preprint arXiv:1004.0993 (2010)

* [[Michael Batanin]], _Monoidal globular categories as a natural environment for the theory of weak $n$-categories_ , Advances in Mathematics 136 (1998), no. 1, 39&#8211;103.

The following paper contains some discussion on the relationship between various (weak) $(n \times k)$-categories for $n, k \leq 3$.

* {#DH10} [[Chris Douglas]], and [[Andre Henriques]], _Internal bicategories_ ([arXiv:1206.4284](https://arxiv.org/abs/1206.4284)) (2012)

There is some discussion on [this n-Category Café post](https://golem.ph.utexas.edu/category/2010/04/symmetric_monoidal_bicategorie.html) as well as [this one](https://golem.ph.utexas.edu/category/2011/03/liang_kong_on_levinwen_models.html).


[[!redirects n-by-k category]]
[[!redirects n-by-k categories]]