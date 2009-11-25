#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

An _allegory_ is a category with properties meant to reflect the properties one expects of a category of [[Rel|relations]]. The notion was first introduced in the book _Categories, Allegories_ by Freyd and Scedrov. 

## Definition

An **allegory** is a [[(1,2)-category]] $A$ equipped with an [[involution]] $(-)^o \colon A^{op} \to A$ which is the identity on objects, such that

* each hom-poset $A(x,y)$ has binary [[intersections]], and
* the *modular law* holds: for $\phi\colon x\to y$, $\psi\colon y\to z$, and $\chi\colon x\to z$, we have $\psi \phi \cap \chi \le \psi (\phi \cap \psi^o \chi)$.

## See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[bicategory of relations]] (a special sort of [[cartesian bicategory]])

* [[1-category equipment]]

## References

* [[Categories, Allegories]]

* The [[Elephant]], chapter A3.

* [Wikipedia](http://en.wikipedia.org/wiki/Allegory_%28category_theory%29).

* [blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) showing that any bicategory of relations is an [[allegory]].

[[!redirects tabular allegory]]
[[!redirects union allegory]]
[[!redirects division allegory]]
[[!redirects power allegory]]

[[!redirects allegories]]