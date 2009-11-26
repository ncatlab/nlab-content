# Bicategories of relations
* tic
{: toc}


## Idea

A *bicategory of relations* is a [[(1,2)-category]] which behaves like the 2-category of internal [[relations]] in a [[regular category]].  The notion is due to Carboni and Walters.


## Definition

A **bicategory of relations** is a [[cartesian bicategory]] which is [[locally posetal 2-category|locally posetal]] and in which for every object $X$, the [[diagonal morphism|diagonal]] $\Delta\colon X\to X\times X$ and [[codiagonal]] $\nabla\colon X\times X\to X$ satisfy the [[Frobenius condition]]:
$$\nabla\Delta = (1\times \Delta)(\nabla \times 1).$$

+--{: .query}
There is also the dual Frobenius condition $\nabla\Delta = (\Delta\times 1)(1\times \nabla)$, and the "separable axiom" $\Delta\nabla = 1$, which as far as I can tell are not in the original paper, but appear in the blog post.  Do they follow from the rest of the definition?
=--

Of course, in the locally posetal case the definition of [[cartesian bicategory]] can be simplified.  (Should say something about that.)


## See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegories]]

* [[1-category equipments]]


## References

* Carboni and Walters, "Cartesian Bicategories, I"

* [blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) showing that any bicategory of relations is an [[allegory]].


[[!redirects bicategories of relations]]