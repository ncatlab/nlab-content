
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


> For the concept in [[computer science]] see [[polymorphism]]. For the concept introduced by [[Shinichi Mochizuki]] in [[inter-universal Teichmüller theory]], see [[poly-morphism]].

#Contents#
* table of contents
{:toc}

## Idea

Universe polymorphism is the ability for [[definitions]] to be implicitly duplicated at different [[universe]] levels, with the [[types]] they contain. Both Russell and Tarski style universes can be polymorphic or not. 

## Examples and applications

* [[Coq]] uses Russell style universes and used to have a sort of "fake" universe polymorphism, but recent versions of Coq have real universe polymorphism (thanks to Mathieu Sozeau). 

* [[Agda]] uses non-cumulative Russell style universes with universe polymorphism.

* The [[HoTT Book]] (first edition) uses Russell style universes with universe polymorphism.

## Related concepts

* [[universe enlargement]]

* [[typical ambiguity]]

## References

* [[Robert Harper]], Rober Pollack, _Type Checking with Universes_ (1991) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.38.8166))

* [[Mike Shulman]], [Universe Polymorphism and Typical Ambiguity](https://golem.ph.utexas.edu/category/2012/12/universe_polymorphism_and_typi.html), blog post 2012

* Matthieu Sozeau and Nicolas Tabareau, *Universe polymorphism in Coq*, In: Klein G., Gamboa R. (eds) Interactive Theorem Proving. ITP 2014. Lecture Notes in Computer Science, vol 8558. Springer, Cham. [doi](https://doi.org/10.1007/978-3-319-08970-6_32)

* András Kovács, *Generalized Universe Hierarchies and First-Class Universe Levels*, 2021, [arxiv:2103.00223](https://arxiv.org/abs/2103.00223).

[[!redirects universe polymorphisms]]

