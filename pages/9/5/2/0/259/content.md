

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The notion of _quasi-category_ is a [[geometric definition of higher categories|geometric model]] for [[(∞,1)-category]].
 
In analogy to how a [[Kan complex]] is a model in terms of [[simplicial set]]s of an [[∞-groupoid]] -- also called an [[(∞,0)-category]] --  a [[quasi-category]] is a model in terms of [[simplicial set]]s of an [[(∞,1)-category]].


## Definition

+-- {: .un_defn}
###### Definition

A **quasi-category** or **[[weak Kan complex]]** is a [[simplicial set]] $C$ satisfying the following equivalent conditions

* all _inner_ [[horn]]s in $C$ have fillers. This means that the lifting condition given at [[Kan complex]] is imposed only for horns $\Lambda^i[n]$ with $0 \lt i \lt n$.

* the morphism of simplicial sets

  $$
    sSet(\Delta[2],C) \to sSet(\Lambda[2]_1,C)
  $$

  (induced from the inner [[horn]] inclusion $\Lambda[2]_1 \to \Delta[2]$)
  is an acyclic [[Kan fibration]].

=--

The equivalence of these two definitions is due to [[Andre Joyal]] and recalled as [[Higher Topos Theory|HTT, corollary 2.3.2.2]].

+-- {: .un_remark}
###### Remark

The second condition says manifestly that a quasi-category is a simplicial set in which composition of any two composable edges is defined up to a contractible space of choices. This is the [[coherence law]] on compositon.

=--

+-- {: .un_defn}
###### Definition

An **[[algebraic quasi-category]]** is a quasi-category equipped with a _choice_ of inner horn fillers. 

=--

While quasi-categories provide a [[geometric definition of higher categories]], algebraic quasi-categories provide an [[algebraic definition of higher categories]]. For more details on this see [[model structure on algebraic fibrant objects]].




+-- {: .un_remark}
###### Remark on terminology

In older literature, such as [[The Joy of Cats]], the term "quasicategory" was sometimes used for a "very large" category whose objects are [[large categories]] or otherwise built out of [[proper classes]], but nowadays this usage is fairly archaic.  See also [[metacategory]]

=--

## Properties

### Relation to simplicially enriched categories

The [[homotopy coherent nerve]] relates quasi-categories with another model for $(\infty,1)$-categories: [[simplicially enriched categories]].

See [[relation between quasi-categories and simplicial categories]] for more.

### Higher associahedra in quasi-categories

While the geometric definition of [[(∞,1)-category]] in terms of quasi-categories elegantly captures all the higher categorical data automatically, it may be of interest in applications to explicitly extract the associators and higher associators encoded by this structure, that would show up in any [[algebraic definition of higher categories|algebraic definition of the same categorical structure]], such as [[algebraic quasi-categories]].

For a discussion of this see

* [[Emily Riehl]], _Associativity data in an $(\infty,1)$-category_ ([pdf](http://math.uchicago.edu/~eriehl/associativity.pdf) [blog](http://golem.ph.utexas.edu/category/2009/10/associativity_data_in_an_1cate.html))

## Examples

The two basic examples for quasi-categories are

* Every [[Kan complex]] is, in particular, a quasi-category.

* The [[nerve]] of a [[category]] is a quasi-category.

Since the nerve of a category is a [[Kan complex]] iff the category is a [[groupoid], quasi-categories are a minimal common generalization of Kan complexes and nerves of categories.

By the [[homotopy hypothesis]]-theorem every Kan complex arises, up to equivalence, as the [[fundamental ∞-groupoid]] of a [[topological space]]. 

Analogously, every [[directed topological space]] $X$ has naturally a [[fundamental (∞,1)-category]] given by a quasi-category whose $k$-cells are maps $\Delta^k_{Top} \to X$ that map the 1-[[simplicial skeleton|skeleton]] of the topological simplex in an order-preserving way to directed paths in $X$.

The [[directed homotopy theory]] that would state that this or a similar construction exhausts all quasicategories up to equivalence, does not quite exist yet.


## Constructions in quasi-categories 

The point of quasi-categories is that they are supposed to provide a fully [[homotopy theory|homotopy-theoretic]] refinement of the ordinary notion of [[category]]. In particular, all the familiar constructions of [[category theory]] have natural analogs in the context of quasi-categories. See for instance

* [[hom-object in a quasi-category]]

* [[equivalence in a quasi-category]]

* [[equivalence of quasi-categories]]

* [[join of quasi-categories]]

* [[over quasi-category]]

* [[terminal object in a quasi-category]]

* [[monomorphism in an (∞,1)-category]]

* [[limit in quasi-categories]]

* [[sub-quasi-category]]

* [[opposite quasi-category]]

* [[fibrations of quasi-categories]]

  * [[inner Kan fibration]]

  * [[Cartesian fibration]]

  * [[left Kan fibration]]/[[right Kan fibration]]

  * [[minimal Joyal fibration]]




## Related concepts

* One may try to further weaken the filler conditions in order to describe [[(∞,n)-categories]] for $n \gt 1$. One approach along these lines is the theory of [[weak complicial set]]s.



## References

Quasi-categories were originally  defined in

* [[Michael Boardman]], [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological
spaces_, Lecture Notes in Mathematics, Vol. 347. Springer-Verlag, 1973.

They occured as  [[weak Kan complex]]es in 

* [[Rainer Vogt]], _Homotopy limits and colimits_, Math. Z., 134, (1973), 11&#8211;52.

Vogt's main theorem involved a category of [[homotopy coherent diagram|homotopy coherent diagrams]] defined on a topologically enriched category and showed it was equivalent to a quotient category of the category of (commutative) diagrams on the same category. 

Cordier in

* J.-M. Cordier, _Sur la notion de diagramme homotopiquement coh&#233;rent_, Cahiers de Top. 
G&#233;om. Diff., 23, (1982), 93 &#8211;112,

defined a [[homotopy coherent nerve]] of any [[simplicially enriched category]], which generalised the [[nerve]] of an ordinary category. In 

* J.-M. Cordier and [[Tim Porter]], _Vogt's theorem on categories of homotopy coherent diagrams_, 
Math. Proc. Cambridge Philos. Soc., 100, (1986), 65&#8211;90, 

it was shown that this homotopy coherent nerve was a quasi-category if the simplicial enrichment was by Kan complexes.

A systematic study of SSet-enriched categories in this context is in

* J-M Cordier, [[Tim Porter]] _Homotopy coherent category theory_ Trans. Amer. Math. Soc. 349
(1997), no. 1, 1-54. ([pdf](http://www.ams.org/tran/1997-349-01/S0002-9947-97-01752-2/S0002-9947-97-01752-2.pdf))

 
The importance of quasi-categories as a basis for [[category theory]] has been particularly emphasized in the work by [[André Joyal]]

* [[André Joyal]], _Quasi-categories and Kan complexes_, J. Pure Appl. Algebra, 175 (2002), 207-222.

For several years Joyal has been preparing a textbook on the subject. This still doesn't quite exist, but an extensive writeup of lecture notes does:

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

and more recently, with more details

* [[André Joyal]], _Notes on quasi-categories_ ([pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf)).


Meanwhile [[Jacob Lurie]], building on Joyal's work, has considerably pushed the theory further. A comprehensive discussion of the theory of $(\infty,1)$-categories in terms of the models [[quasi-category]] and [[simplicially enriched category]] is in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The relation between [[quasi-category|quasi-categories]] and [[simplicially enriched categories]] was discussed in detail in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))


## Discussion

A previous version of this entry led to the following discussion.

+-- {: .query}
_Stephen Gaito_: If we want to weaken this even further to provide a simplicial model of, for example, a [[(∞,2)-category]], how would we do this?

Would we apply the lifting condition on all but three of the indices... and if so which three?  (The first, last and ????)

[[Mike Shulman]]: You may be looking for something along the lines of a [[weak complicial set]].

=--




[[!redirects quasi-categories]]
[[!redirects quasicategory]]
[[!redirects quasicategories]]

[[!redirects inner Kan complex]]
[[!redirects inner Kan complexes]]
