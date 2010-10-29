#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _dualizing object_ is an object $a$ which can be regarded as being an object of two different categories $A$ and $B$, such that the concrete [[duality]] which is induced by homming into that object induces duality adjunctions between $A$ and $B$, schematically:

$$
  T : A^{op} \stackrel{Hom_A(-,a)}{\to} B
$$
$$
  S: B^{op} \stackrel{Hom_B(-,a)}{\to} A
  \,.
$$

Many famous dualities are induced this way, for instance [[Stone duality]] and [[Gelfand-Naimark duality]].

## Remark on terminology

There are various different terms for "dualizing objects". As recalled on p. 112 of the article by Porst and Tholen below

* Isbell speaks of _objects keeping summer and winter homes_;

* Lawvere speaks of _objects sitting in two categories_;

* Simmons speaks of _schizophrenic objects_.

It has been convincingly argued by [[Tom Leinster]] (blog comment [here](http://golem.ph.utexas.edu/category/2007/01/more_on_duality.html#c007089)) that the term "schizophrenic" should not be used. [[Todd Trimble]] then suggested the term "ambimorphic object."  Another suggestion was "Janusian object."

## Definition


Let $A$ and $B$ be two [[concrete category|concrete categories]], i.e. categories equipped with faithful functor to [[Set]]

$$
  U : A \to Set
$$
$$
  V : B \to Set
  \,.
$$

Then consider pairs of objects $(a \in A, b \in B)$ with the same underlying set,  $U(a) \simeq V(b)$. Then ... (see reference below).

## Examples

Examples appear at 

* [[Chu construction]]

* [[rational homotopy theory]]

## References

* H.-E. Porst, W. Tholen, _Concrete Dualities_ in _Category Theory at Work_, Herrlich, Porst (eds.) ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf))

* Michael Barr, John F. Kennison, R. Raphael, _Isbell Duality_ ([pdf](http://www.tac.mta.ca/tac/volumes/20/15/20-15.pdf))


[[!redirects ambimorphic object]]