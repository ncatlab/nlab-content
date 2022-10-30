<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>

#Contents#

* automatic table of contents goes here
{:toc}


## Idea

The notion of quasi-category is a [[geometric definition of higher category]] that relaxes the [[Kan complex|Kan condition]] on a simplicial set.

Just as a [[Kan complex]] is a model in terms of [[simplicial set]]s of an [[∞-groupoid]] -- also called an [[(∞,0)-category]] --  a [[quasi-category]] is a model in terms of [[simplicial set]]s of an [[(∞,1)-category]].


## Definition


A quasi-category is a [[simplicial set]] in which all _inner_ [[horn]]s have fillers. This means that the lifting condition given at [[Kan complex]] is imposed only for horns $\Lambda^i[n]$ with $0 \lt i \lt n$.

+-- {: .query}
_Stephen Gaito_: If we want to weaken this even further to provide a simplicial model of, for example, a [[(∞,2)-category]], how would we do this?

Would we apply the lifting condition on all but three of the indicies... and if so which three?  (The first, last and ????)

[[Mike Shulman]]: You may be looking for something along the lines of a [[weak complicial set]].

=--

## Remarks

* Compare with the definition of a [[Kan complex]] in which _all_ horns are required to have fillers: a quasi-category is a structure slightly weaker than a Kan complex. Indeed, while we can think of a Kan complex as an [[∞-groupoid]] (that is an $(\infty,0)$-category), in which _all_ morphisms are [[equivalence]]s, a quasi-category is a model for an [[(∞,1)-category]], in which only all [[k-morphism]]s for $k \geq 2$ are required to be [[equivalence]]s.  

* As the quasi-category condition is a weakening of the Kan complex condition, they have also been called **weak Kan complexes** and the corresponding condition, the **weak Kan condition**.

* The [[nerve]] of an ordinary [[category]] is always a quasi-category, while the nerve of a category is a [[Kan complex]] iff the category is a [[groupoid].  In this sense quasi-categories are a "minimal common generalization" of Kan complexes and nerves of categories.

### Higher associahedra in quasi-categories

While the geometric definition of [[(∞,1)-category]] in terms of quasi-categories eleganty captures all the higher categorical data automatically, it may be of interest in applications to explicitly extract the associators and higher associators encoded by this structure, that would show up any any algebraic definition of the same categorical structure. 

For a discussion of this see

* [[Emily Riehl]], _Associativity data in an $(\infty,1)$-category_ ([pdf](http://math.uchicago.edu/~eriehl/associativity.pdf) [blog](http://golem.ph.utexas.edu/category/2009/10/associativity_data_in_an_1cate.html))


## Constructions in quasi-categories 

The point of quasi-categories is that they are supposed to provide a fully [[homotopy theory|homotopy-theoretic]] refinement of the ordinary notion of [[category]]. In particular, all the familiar constructions of [[category theory]] have natural analogs in the context of quasi-categories. See for instance

* [[limit in quasi-categories]]

* [[over quasi-category]]

* [[terminal object in a quasi-category]]

* [[join of quasi-categories]]


## References

Quasi-categories have originally been defined in

* J.M. Boardman and R.M. Vogt, _Homotopy invariant algebraic structures on topological
spaces_, Lecture Notes in Mathematics, Vol. 347. Springer-Verlag, 1973._

They occured as  weak Kan complexes in 

* R. Vogt, _Homotopy limits and colimits_, Math. Z., 134, (1973), 11&#8211;52.

Vogt's main theorem involved a category of [[homotopy coherent diagram|homotopy coherent diagrams]] defined on a topologically enriched category and showed it was equivalent to a quotient category of the category of (commutative) diagrams on the same category. 


Cordier in

* J.-M. Cordier, _Sur la notion de diagramme homotopiquement coh&#233;rent_, Cahiers de Top. 
G&#233;om. Diff., 23, (1982), 93 &#8211;112,

defined a [[homotopy coherent nerve]] of any [[simplicially enriched category]], which generalised the [[nerve]] of an ordinary category. In 

* J.-M. Cordier and T. Porter, _Vogt's theorem on categories of homotopy coherent diagrams_, 
Math. Proc. Cambridge Philos. Soc., 100, (1986), 65&#8211;90, 

it was shown that this homotopy coherent nerve was a quasi-category if the simplicial enrichment was by Kan complexes.
 
Their importance as a basis for [[category theory]] has been emphasized in the work by [[André Joyal]]

* A. Joyal, _Quasi-categories and Kan complexes_, J. Pure Appl. Algebra, 175 (2002), 207-222.

For several years Joyal has been preparing a textbook on the subject. This still doesn't quite exist, but an extensive writup of lecture notes does:

* [[Andre Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

Meanwhile [[Jacob Lurie]], building on Joyal's work, has considerably pushed the theory further. A comprehensive discussion of the theory of $(\infty,1)$-categories in terms of the models [[quasi-category]] and [[simplicially enriched category]] is

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The relation between [[quasi-category|quasi-categories]] and [[simplicially enriched categories]] was discussed in detail in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))


[[!redirects quasi-categories]]
[[!redirects quasicategory]]
[[!redirects quasicategories]]
