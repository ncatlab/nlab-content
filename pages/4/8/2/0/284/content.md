#Idea#

According to the general pattern on [[(n,r)-category]], an $(\infty,1)$-category is a (weak) [[infinity-category]] in which all $n$-morphisms for $n \geq 2$ are [[equivalence]]s.

To some extent an $(\infty,1)$-category can be thought of as a [[enriched category|category enriched in]] [[(infinity,0)-category|(infinity,0)]]-categories, namely in [[infinity-groupoid]]s.

For a discussion of the motivation and purpose of $(\infty,1)$-categories see [[why (infinity,1)-categories?]].


#Definition#

## quasi-categories ##

We start with the definition of "$(\infty,1)$-category" that was promoted by [[Andre Joyal]] as a good model for the theory. This goes back to Boardman-Vogt.

This is a [[geometric definition of higher category]] which conceives an $(\infty,1)$-category as a [[simplicial set]] with extra [[stuff, structure, property|property]]. It is a straightforward generalization of the definition of [[infinity-groupoid]] as a [[Kan complex]]. 

Recall that a [[Kan complex]] is a [[simplicial set]] in which every [[horn]] $\Lambda^k[n]$, $0 \leq k \leq n$ has a _filler_. This condition may be read in words as: every collection of adjacent $n$-cells has a composite $n$-cell, even if the orientations of the cells don't match. This implicitly encodes the _invertibility_ of every cell: if the orientation does not match, we can invert the cell and then compose.

From this perspective one observes, by looking closely at the combinatorics, that the invertibility of the 1-cells in the simplicial set is enforced particularly by the condition that the [[horn|outer horns] $\Lambda^0[n]$ and $\Lambda^n[n]$ have fillers.

Therefore in a [[simplicial set]] in which _only the inner horns_ $\Lambda^k[n]$ for $0 \lt k \lt n$ have fillers all cells are required to have a kind of inverse, except the 1-cells. (They may have inverses, too, but are not required to).

This is evidently a realization of the idea of an [[(n,r)-category]] with $n = \infty$ and $r = 1$.


Such a simplicial set with fillers for all inner horns

* Boardman and Vogt called a _weak Kan complex_ ; 

* [[Andre Joyal]] called a [[quasi-category]];

* [[Jacob Lurie]] called an $\infty$-category.
 
Here we follow Joyal and say [[quasi-category]] when we mean concretely the simplicial sets with extra property. We use more generally term 
"$(\infty,1)$-category" for this or any of its equivalent models, discussed below, in order to distinguish from the term [[infinity-category]] or [[omega-category]] that is more traditionally understood to generically mean an $\infty$-category with no conditions on invertibility 
(in terms of [[(n,r)-category]]: an $(\infty,\infty)$-category).


With [[quasi-category|quasi-categories]] being just [[simplicial set]]s with extra property, there are evident and simple definitions of 

* the [[quasi-category of (infinity,1)-functors|(infinity,1)-category of (infinity,1)-functors]] between two [[quasi-category|quasi-categories]] $C$ and $D$;

* the quasi-category of all [[infinity-groupoid]]s;

* the [[quasi-category of all quasi-categories|(infinity,1)-category of (infinity,1)-categories]].

Similarly, [[Andre Joyal]] and [[Jacob Lurie]] have shown that all other constructions in [[category theory]] have good generalizations to quasi-categories, which usually have conceptually simple formulations: see [[Higher Topos Theory]] for more.


## model categories ##

At the very beginning, a [[model category]] was understood as a "model for the category [[Top]] of topological spaces": some [[category]] with extra [[stuff, structure, property|structure and property]] which allows to perform all operations familiar of the [[homotopy theory]] of [[topological space]]s.

As mentioned above, from the point of view of [[(infinity,1)-category|(infinity,1)-categories]], [[Top]] may naturally be regarded an as [[(infinity,1)-category]] and is in fact the archetypical example, analogous to how [[Set]] is the archetypical examples of an ordinary [[category]].

This indicates that, more generally, a [[model category]] should actually be a means to model (i.e. encode) in 1-categorical terms an $(\infty,1)$-category.

This indeed turns out to be true: there is a precise sense in which every [[model category]] [[presentable (infinity,1)-category|presents]] an $(\infty,1)$-category:

* given a model category $A$;

* it bcomes canonically an [[SSet]]-[[enriched category]] making it a [[simplial model category]] $\mathbf{A}$;

* the full [[SSet]]-[[subcategory]] $\mathbf{A}^\circ$ on the fibrant-cofibrant objects of $\mathbf{A}$ happens to be [[Kan complex]]-[[enriched category|enriched]];

* the [[simplicial nerve]] $N(\mathbf{A}^\circ)$ of $\mathbf{A}^\circ$ is the [[quasi-category]] _presented_ by $A$.

With the relation between [[simplicial category|simpliical categories]] and [[quasi-category|quasi-categories]] via [[simplicial nerve]] understood, we shall here often not distinguish between $\mathbf{A}^\circ$ and $N(\mathbf{A}^\circ)$ as the $(\infty,1)$-category [[presentable (infinity,1)-category|presented]] by the [[model category]] $A$.


The following analogy (appearing in this way on [p. 44 of Ben-Zvi/Nadler07]()) might illustrate how model categories, $(\infty,1)$-categories and homotopy categories relate

$$
 \array{
   model category &\to& (\infty,1)-category &\to& homotopy category
   \\
   vector space with basis &\to& vector space &\to& dimension of vector space
 }
$$


## Top-, Kan- and simplicially enriched categories ##

As the above example of presentations by [[model category|model categories]]
already indicates,
despite the conceptual simplicity of [[quasi-category|quasi-categories]],
for computations and in particular for obtaining examples, 
it is often useful to pass to a slightly different model.

Recall that we said at the beginning that an $(\infty,1)$-category is supposed to be like an  [[enriched category]] which is enriched over the category of [[infinity-groupoid]]s. 
This turns out to make sense literally
if one takes care to remember that $\infty$-groupoids
themselves form a higher category.

As discussed at  [[homotopy hypothesis]] there is a Quillen equivalence of the [[model category|model categories]] of 

* the [[model structure on topological spaces|standard model structure]] on the category [[Top]] of compactly generalted weakly Hausdorff [[topological space]]s;

* the [[model structure on simplicial sets|standard model structure]] on the category of [[Kan complex]]es.

In fact, this is also equivalent to

* the [[model structure on simplicial sets|standard model structure]] on the category [[SSet]] of [[simplicial set]]s.

If we takes a [[Kan complex]] to most manifestly be an incarnation of the idea "[[infinity-groupoid]]", then under these equivalences one should think of

* a [[simplicial set]] as representing the [[Kan complex]] which is obtained from it by "freely throwing in the missing inverses" of cells (technically: as representing its fibrant replacement);

* a [[topological space]] $X$ as representing the [[Kan complex]] $\Pi(X)$, whose 

  * 0-cells are the points of $X$;
  
  * 1-cells are the paths in $X$;
  
  * 2-cells are the triangles in $X$;
  
  * etc.
  
With this interpretation understood (i.e. with these model structures understood), [[SSet]]-enriched categories do model $(\infty,1)$-categories. 

For more see

* [[relation between quasi-categories and simplicial categories]]



## Segal categories and complte Segal spaces ##

Other models for $(\infty,1)$-categories are

 * [[Segal category|Segal categories]];

 * [[complete Segal space]]s.
 
A complete Segal space may be thought of as a category which is
_weakly_ enriched in topological spaces/simplicial sets/Kan complexes,
where the definition of "weak" makes use of the notion of [[homotopy]]
and [[homotopy limit]] in [[Top]] or [[SSet]].

This construction principle in particular lends itself
to iteration and hence to an inductive definition of 
[[(infinity,n)-category]].


#References#



A comprehensive discussion of the theory of $(\infty,1)$-categories in terms of the models [[quasi-category]] and [[simplicially enriched category]] is

* [[Jacob Lurie]], [[Higher Topos Theory]].

A comparison of the four [[model category]] structures on

 * [[quasi-category|quasi-categories]];

 * [[simplicially enriched category|simplicially enriched categories]];

 * [[Segal category|Segal categories]];

 * [[complete Segal space]]s.

is in 

* Julia E. Bergner, _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))



More discussion of the other two models can be found at

* [[Jacob Lurie]], _On the classification of topological field theories_ ([pdf](http://www-math.mit.edu/~lurie/papers/cobordism.pdf)).