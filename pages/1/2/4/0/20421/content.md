
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

An _$(n \times k)$-category_ (read "n-by-k category") is an $n$-category internal to a $k$-category.

For example:

* A $(1 \times 0)$-category, as well as a $(0 \times 1)$-category, are precisely [[categories]].
* A $(1 \times 1)$-category is precisely a [[double category]].
* A $(1 \times 1 \times 1)$-category is precisely a [[triple category]] (that is, a category internal to a double category).
* An $(n \times 1)$-category is what Batanin calls a [[monoidal n-globular category]].

An $(n \times k)$-category has $(n + 1)(k + 1)$ kinds of cells.

Under suitable fibrancy conditions, a $(n \times k)$-category will have an underlying $(n + k)$-category (where here, $n + k$ is to be read arithmetically, rather than simply as notation). Fibrant $(1 \times 1)$-categories are known as [[framed bicategories]].

## Examples

* [[commutative ring|Commutative rings]], [[algebras]] and [[modules]] form a symmetric monoidal $(2 \times 1)$-category.
* [[conformal net|Conformal nets]] form a symmetric monoidal $(2 \times 1)$-category.

## Relationships

* $(2 \times 1)$-categories subsume ($1 \times 2)$-categories (**[DH10](#DH10)**)


## Related concepts

* [[internal category]]

* [[n-fold category]]


## References ##

* [[Mike Shulman]], Constructing symmetric monoidal bicategories, arXiv preprint arXiv:1004.0993 (2010)

* [[Michael Batanin]], _Monoidal globular categories as a natural environment for the theory of weak $n$-categories_ , Advances in Mathematics 136 (1998), no. 1, 39&#8211;103.

The following paper contains some discussion on the relationship between various (weak) $(n \times k)$-categories for $n, k \leq 3$.

* {#DH10} C. Douglas, and A.G. Henriques, Internal bicategories, arXiv preprint arXiv:1206.4284 (2012)

There is some discussion on [this n-Category Café post](https://golem.ph.utexas.edu/category/2010/04/symmetric_monoidal_bicategorie.html) as well as [this one](https://golem.ph.utexas.edu/category/2011/03/liang_kong_on_levinwen_models.html).


[[!redirects n-by-k category]]
[[!redirects n-by-k categories]]