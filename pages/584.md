#Idea#

$n$-Dimensional [[manifold]]s (possibly and usually equipped with certain structure, notably for instance with orientation) should naturally form an [[(infinity,n)-category]] of [[extended cobordism]]s whose

* [[object]]s are 0-dimensional (oriented) manifolds (disjoint unions of (oriented) points);

* 1-[[morphism]]s are (oriented) [[cobordism]]s between disjoint unions of (oriented) points;

* 2-morphisms are cobordisms between 1-dimensional cobordisms

* etc.

* (n+1)-morphims are _diffeomorphisms_ between $n$-dimensional cobordisms;

* (n+2)-morphisms are smooth homotopies of these;

* etc.

A specific realization of this idea has recently been proposed in

* [[Jacob Lurie]], _On the classification of Topological Field Theories_ ([pdf](http://www-math.mit.edu/~lurie/papers/cobordism.pdf))

(definition 2.2.9 [page 36](http://www-math.mit.edu/~lurie/papers/cobordism.pdf#page=36))

in the context of [[(infinity,n)-category|(infinity,n)-categories]] modeled essentially as categories $n$-fold [[homotopy coherent category theory|homotopically]] [[enriched category|enriched]] over $Top$.

The definition uses the idea of classifying manifolds and cobordisms by equipping the manifolds with _Morse functions_ and analysing the critial points of these functions: these indicate, roughly, where "handles" branch off a manifold.

In Lurie's definition the collection of critical points on a $n$-dimensional manifold is naturally organized into an $n$-fold simplicial structure, whose points are manifolds $X$ with $n$ Morse functions $X \to \mathbb{R}$ with specified ordered lists of values of critical points. Given that the [[simplex category]] $\Delta$ is just that of totally ordered sets, this naturally forms an $n$-fold simplicial structure. And it can be completed into an honest [[(infinity,n)-category]].

For details on how this kind of construction works in low dimensions see also

* Chris Schommer-Pries _The classification of 2-dimensional extended TFT_ ([pdf]())
