<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>



## Idea

$n$-Dimensional [[manifolds]] (possibly and usually equipped with certain structure, notably for instance with orientation) should naturally form an [[(∞,n)-category]] of [[extended cobordisms]] whose

* [[objects]] are 0-dimensional (oriented) manifolds (disjoint unions of (oriented) points);

* 1-[[morphisms]] are (oriented) [[cobordisms]] between disjoint unions of (oriented) points;

* 2-morphisms are cobordisms between 1-dimensional cobordisms

* etc.

* (n+1)-morphims are _diffeomorphisms_ between $n$-dimensional cobordisms;

* (n+2)-morphisms are smooth homotopies of these;

* etc.

The $(\infinity,n)$-category of cobordisms is the subject of the [[cobordism hypothesis]].


## Definition

### Lurie's definition

Here is an outline of the idea of the definition of 
$Bord_{(\infty,n)}$ as given in 

*  [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

where the main point, apart from the [[(∞,n)-category]] machinery in the background, is definition 2.2.9.

The idea is to start with thinking of $n$-dimensional cobordisms as forming something like an [[n-fold category]] by simply saying that the collection of compositites of cobordisms is given by big cobordisms with markings on them, indicating where we think of them as being composed.

Let's first do this for composition in one direction, as in an ordinary 1-category of $n$-dimensional cobordisms.

consider a [[manifold]] $X \hookrightarrow V \times \mathbb{R}$ embedded in a [[vector space]] of the form $V \times \mathbb{R}$. We can think of this as a manifold canonically equipped with a coordinate function $\phi : X \hookrightarrow V \times \mathbb{R} \to \mathbb{R}$ that measures the "height" or maybe better the "length" of the embedded manifold. 

We can pick a bunch of numbers $\{t_i \in \mathbb{R}\}$ and think of these as marking a bunch of slices of $X$, the preimages $\phi^{-1}(t_i)$. We can think of these slices as being the $(n-1)$-dimensional boundary manifolds at which a sequence of manifolds have been glued together to produce $X$. 

In this way an embedded manifold $X \hookrightarrow V \times \mathbb{R} $ and a set of $k$-numbers $\{t_i\}$ ...




## References

A specific realization of this idea in terms of [[(∞,n)-category]] modeled as [[n-fold complete Segal space]] is in (definition 2.2.9, page 36)

*  [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

In that article a proof of the [[cobordism hypothesis]] is indicated.

A detailed construction of the [[(n,r)-category|(2,2)-category]] of cobordisms is

* [[Chris Schommer-Pries]], [[2-category of 2-dimensional cobordisms]] .

Other descriptions of higher categories of cobordisms are

* [[Marco Grandis]], _[[Cospans in Algebraic Topology]]_

* Eugenia Cheng and Nick Gurski, _Toward an $n$-category of cobordisms_ , Theory and Applications of Categories 18 (2007), 274-302. ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))


[[!redirects (∞,n)-category of cobordisms]]



