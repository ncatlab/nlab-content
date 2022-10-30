
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### $(\infty,1)$-topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

According to the general pattern on [[(n,r)-category]], an $(\infty,1)$-category is a (weak) [[∞-category]] in which all $n$-morphisms for $n \geq 2$ are [[equivalences]]. This is the joint generalization of the notion of _[[category]]_ and _[[∞-groupoid]]_.

More precisely, this is the notion of _[[category]]_ up to [[coherence|coherent]] [[homotopy]]:
an $(\infty,1)$-category is equivalently 

* an [[internal category in an (∞,1)-category|internal category]] in [[∞-groupoids]]/basic [[homotopy theory]] (as such usually modeled as a [[complete Segal space]]). 

* a category [[enriched (infinity,1)-category
|homotopy enriched]] over [[∞Grpd]] (as such usually modeled as a [[Segal category]]).


Among all [[(n,r)-category|(n,r)-categories]], $(\infty,1)$-categories are special in that they are the simplest structures that at the same time:

* admit a [[higher category theory|higher version]] of [[category theory]] ([[limit]]s, [[adjunction]]s, [[Grothendieck construction]], etc, [[sheaf and topos theory]], etc.) : [[(infinity,1)-category theory]]

* and know everything about higher [[equivalences]].

Notably for understanding the collections of all [[(n,r)-category|(n,r)-categories]] for arbitrary $n$ and $r$, which in general is an $(n+1,r+1)$-category, the knowledge of the underlying $(n,1)$- (and hence $(\infty,1)$-)category already captures much of the information of interest: it allows to decide if two given $(n,r)$-categories are equivalent and allows to obtain new $(n,r)$-categories from existing ones by universal constructions.

The collection of all $(\infty,1)$-categories forms the [[(∞,2)-category]] [[(∞,1)Cat]].

## Definitions

There are a number of different ways to make the idea of an $(\infty,1)$-category precise, including [[quasi-categories]], [[simplicial set|simplicially]] [[enriched categories]], topologically enriched categories, [[Segal categories]], [[complete Segal spaces]], and $A_\infty$-[[A-infinity categories|categories]] (most of which can be done either simplicially or topologically).  Additionally, any notion of [[∞-category]] can be specialized to a notion of $(\infty,1)$-category by simply requiring all $n$-cells for $n\gt 1$ to be invertible.


Unlike the case for general notions of $n$-category, almost all the definitions of $(\infty,1)$-category are known to form [[model categories]] that are [[Quillen equivalence|Quillen equivalent]].  See also [[n-category]] for a summary of the state of the art about definitions of $n$-category and comparisons between them.

### Quasi-categories

We start with the definition of "$(\infty,1)$-category" that was promoted by [[Andre Joyal]] as a good model for the theory. This goes back to Boardman-Vogt in the 1970s and was further developed, by [[Jean-Marc Cordier]] and [[Tim Porter]] in the early 1980s.

This is a [[geometric definition of higher category]] which conceives an $(\infty,1)$-category as a [[simplicial set]] with extra [[stuff, structure, property|property]]. It is a straightforward generalization of the definition of [[∞-groupoid]] as a [[Kan complex]], and, in fact, one alternative term used early on was 'weak Kan complex';  see below.

Recall that a [[Kan complex]] is a [[simplicial set]] in which every [[horn]] $\Lambda^k[n]$, $0 \leq k \leq n$ has a _filler_. This condition may be read in words as: every collection of adjacent $n$-cells has a composite $n$-cell, even if the orientations of the cells don't match. This implicitly encodes the _invertibility_ of every cell: if the orientation does not match, we can invert the cell and then compose.

From this perspective one observes, by looking closely at the combinatorics, that the invertibility of the 1-cells in the simplicial set is enforced particularly by the condition that the [[horn|outer horns]] $\Lambda^0[n]$ and $\Lambda^n[n]$ have fillers.

Therefore in a [[simplicial set]] in which _only the inner horns_ $\Lambda^k[n]$ for $0 \lt k \lt n$ have fillers all cells are required to have a kind of inverse, except the 1-cells. (They may have inverses, too, but are not required to).

This is evidently a realization of the idea of an [[(n,r)-category]] with $n = \infty$ and $r = 1$.


Such a simplicial set with fillers for all inner horns

* Boardman and Vogt called a _weak Kan complex_ ; 

* [[Andre Joyal]] called a [[quasi-category]];

* [[Jacob Lurie]] called an $\infty$-category.
 
Here we follow Joyal and say [[quasi-category]] when we mean concretely the simplicial sets with extra property. We use the more general term 
"$(\infty,1)$-category" for this or any of its equivalent models, discussed below, in order to distinguish from the term [[∞-category]] or [[∞-category]] that is more traditionally understood to generically mean an $\infty$-category with no conditions on invertibility 
(in terms of [[(n,r)-category]]: an $(\infty,\infty)$-category).


With [[quasi-category|quasi-categories]] being just [[simplicial sets]] with extra property, there are evident and simple definitions of 

* the [[(infinity,1)-category of (infinity,1)-functors|quasi-category of (∞,1)-functors|]] between two [[quasi-categories]] $C$ and $D$;

* the quasi-category of all [[∞-groupoids]];

* the [[(infinity,1)-category of (infinity,1)-categories|quasi-category of all quasi-categories]].

Similarly, [[Andre Joyal]] and [[Jacob Lurie]] have shown that all other constructions in [[category theory]] have good generalizations to quasi-categories, which usually have conceptually simple formulations: see [[Higher Topos Theory]] for more.


### $Top$-, $Kan$- and simplicially enriched categories 

Despite the conceptual simplicity of [[quasi-category|quasi-categories]],
for computations and in particular for obtaining examples, 
it is often useful to pass to a slightly different model.

Recall that we said at the beginning that an $(\infty,1)$-category is supposed to be like an  [[enriched category]] which is enriched over the category of [[∞-groupoids]]. 
This turns out to make sense literally
if one takes care to remember that $\infty$-groupoids
themselves form a higher category.

As discussed at  [[homotopy hypothesis]] there is a Quillen equivalence of the [[model category|model categories]] of 

* the [[model structure on topological spaces|standard model structure]] on the [[nice category of spaces|nice category]] of compactly generated weakly Hausdorff [[topological spaces]];

* the [[model structure on simplicial sets|standard model structure]] on the category of [[Kan complex]]es.

In fact, this is also equivalent to

* the [[model structure on simplicial sets|standard model structure]] on the category [[SimpSet|SSet]] of [[simplicial sets]].

If we take the notion of [[Kan complex]] to be the most manifest incarnation of the idea "[[∞-groupoid]]", then under these equivalences one may think of

* a [[simplicial set]] as representing the [[Kan complex]] which is obtained from it by "freely throwing in the missing inverses" of cells (technically: as representing its fibrant replacement);

* a [[topological space]] $X$ as representing the [[Kan complex]] $\Pi(X)$, whose 

  * 0-cells are the points of $X$;
  
  * 1-cells are the paths in $X$;
  
  * 2-cells are the triangles in $X$;
  
  * etc.
  
With this interpretation understood (i.e. with these model structures understood), [[SimpSet|SSet]]-enriched categories do model $(\infty,1)$-categories. 

For more see

* [[relation between quasi-categories and simplicial categories]]


### Homotopical categories

A [[homotopical category]] is a category $C$
equipped with a class $W$ of [[category with weak equivalences|weak equivalences]].
Every homotopical category $(C,W)$ has a _quasi-localisation_ $C[W(-1)]$
which is a [[quasi-category]]. The simplicial set $C[W(-1)]$ is
obtained from the [[nerve]] of $C$ by freely gluing a [[homotopy]] inverse to each [[morphism]] in $W$, and then, by adding simplices to turn it into a quasi-category (this last step is called a fibrant completion).

The [[quasi-category]] $C[W(-1)]$ is equivalent to the [[Dwyer-Kan localisation]] of $C$ with respect to $W$, via the equivalence between [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicial categories]] mentioned above.


Conversely, every quasi-category is equivalent to
the quasi-localisation of a homotopical category.
This gives a representation of all $(\infty,1)$-categories
in terms of [[homotopical category|homotopical categories]].
It follows that many aspects of the theory of $(\infty,1)$-categories
can be expressed in terms of [[category theory]].



When the homotopical category (C,W) is obtained from a Quillen
model structure (by forgetting the cofibrations and the fibrations)
the quasi-category C[W^(-1)] has finite limits and colimits.
Conversely, I conjecture that every quasi-category
with finite limits and colimits is equivalent to the quasi-localisation
of a model category. In fact, every locally presentable quasi-category
is a quasi-localisation of a combinatorial model by a result of Lurie.
More can be said: the underlying category can taken to be
a category of presheaves by a result of Daniel Dugger.

http://arxiv.org/abs/math/0007070



### Model categories

A specific notion of [[homotopical category]] is that of a [[model category]]. $(\infty,1)$-categories obtained as the Dwyer-Kan simplicial localizations of model categories have for instance finite $(\infty,1)$-[[limit]]s and $(\infty,1)$-[[colimit]]s. The [[presentable (∞,1)-category|locally presentable (∞,1)-categories]] are precisely those presented this way by [[combinatorial model category|combinatorial model categeories]]. 

At the very beginning, a [[model category]] was understood as a "model for the category [[Top]] of topological spaces," or more precisely [[homotopy types]]: some [[category]] with extra [[stuff, structure, property|structure and properties]] which allows one to perform all operations familiar of the [[homotopy theory]] of [[topological spaces]].

As mentioned above, from the point of view of [[(∞,1)-categories]], [[Top]] may naturally be regarded an as [[(∞,1)-category]] and is in fact the archetypical example, analogous to how [[Set]] is the archetypical example of an ordinary [[category]].

This indicates that, more generally, a [[model category]] should actually be a means to model (i.e. encode) in 1-categorical terms an $(\infty,1)$-category, and of course this is true since indeed any [[category with weak equivalences]] presents an $(\infty,1)$-category via Dwyer-Kan simplicial localization.  In the case of a model category, however, or at least a [[simplicial model category]], this $(\infty,1)$-category has a different, simpler construction.

* A [[simplicial model category]] $\mathbf{A}$ is, in particular, a [[simplicially enriched category]].

* the full [[SSet]]-[[subcategory]] $\mathbf{A}^\circ$ on the fibrant-cofibrant objects of $\mathbf{A}$ happens to be [[Kan complex]]-[[enriched category|enriched]];

* the [[homotopy coherent nerve]] $N(\mathbf{A}^\circ)$ of $\mathbf{A}^\circ$ is the [[quasi-category]] _presented_ by $A$.

Up to equivalence, this gives the same $(\infty,1)$-category as the Dwyer-Kan hammock localization.  With the relation between [[simplicially enriched categories]] and [[quasi-category|quasi-categories]] via [[homotopy coherent nerve]] understood, we shall here often not distinguish between $\mathbf{A}^\circ$ and $N(\mathbf{A}^\circ)$ as the $(\infty,1)$-category [[presentable (infinity,1)-category|presented]] by a [[model category]] $A$.



### Segal categories and complete Segal spaces

Other models for $(\infty,1)$-categories are

 * [[Segal categories]];

 * [[complete Segal spaces]].
 
Segal categories can be thought of as categories which are
_weakly_ enriched in topological spaces/simplicial sets/Kan complexes,
where the definition of "weak" makes use of the notion of [[homotopy]]
and [[homotopy limit]] in [[Top]] or [[SimpSet|SSet]].

Complete Segal spaces are like [[internal categories in an (∞,1)-category]].

This construction principle in particular lends itself
to iteration and hence to an inductive definition of 
[[(∞,n)-category]] via [[Segal n-categories]] and [[n-fold complete Segal spaces]].



### $A_\infty$-categories

An $A_\infty$-[[A-infinity category|category]] can also be thought of as a category "weakly enriched" in spaces (i.e. $\infty$-groupoids), except that in contrast to the Segal approaches the "weakness" is specified [[algebraic definition of higher category|algebraically]] and parametrized by an [[operad]].  This approach can be generalized to the [[Trimble n-category|Trimble]] definition of $n$-category or $(\infty,n)$-category.

## Properties

### $(\infty,1)$-Category theory

A crucial point about the notion of _$(\infty,1)$-category_ is that it supports all the standard constructions and theorems of [[category theory]], if only the consistent replacements are made ([[isomorphism]] becomes [[equivalence]], etc.).

See _[[(∞,1)-category theory]]_.


### The collection of all $(\infty,1)$-categories

The collection of all $(\infty,1)$-categories
forms an [[(∞,2)-category]] called [[(∞,1)Cat]].

Often it is useful to regard that as a (large) $(\infty,1)$-category itself, by discarding the non-invertible [[natural transformations]].

### Model category presentations

There is a wealth of different presentations of $(\infty,1)$-categories. 

See _[[table - models for (∞,1)-categories]]_.

## Related concepts

* [[table - models for (∞,1)-categories]]

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]


* [[n-category]]

* [[(∞,0)-category]]

* [[(n,1)-category]]

* **(∞,1)-category**, [[internal (∞,1)-category]], [[∞-groupoid]]

  * [[locally cartesian closed (∞,1)-category]]

  * [[(∞,1)-topos]]

  * [[semiadditive (∞,1)-category]], [[additive (∞,1)-category]]

  * [[stable (∞,1)-category]]

  * [[monoidal (∞,1)-category]]

  * [[locally presentable (∞,1)-category]], [[accessible (∞,1)-category]], [[compactly generated (∞,1)-category]]

  * [[disjunctive (∞,1)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]

## References

### General

For several years [[Andre Joyal]] -- who was one of the first to promote the idea that for studying [[higher category theory]] it is good to first study $(\infty,1)$-categories in terms of [[quasi-category|quasi-categories]] -- has been preparing a textbook on the subject. This still doesn't quite exist, but an extensive write-up of lecture notes does:

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf))

Further notes (where the term "[[logos]]" is used instead of [[quasi-category]]) are in

* {#Joyal08} [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))
  

Meanwhile [[Jacob Lurie]], building on Joyal's work, has considerably pushed the theory further. A comprehensive discussion of the theory of $(\infty,1)$-categories in terms of the models [[quasi-category]] and [[simplicially enriched category]] is

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

An brief exposition from the point of view of [[algebraic topology]] is in 

* [[Jacob Lurie]], _What is... an $\infty$-category?_, _Notices of the AMS_, September 2008 ([pdf](http://www.ams.org/notices/200808/tx080800949p.pdf)) 


A useful comparison of the four [[model category]] structures on

 * [[quasi-categories]];

 * [[simplicially enriched categories]];

 * [[Segal categories]];

 * [[complete Segal spaces]].

is in 

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

More discussion of the other two models can be found at

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

and in the references listed at _[[(∞,n)-category]]_.

The relation between [[quasi-category|quasi-categories]] and [[simplicially enriched categories]] was discussed in detail in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))

The presentation of $(\infty,1)$-categories by [[homotopical categories]] and [[model categories]] is discussed in

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], 
  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories
and Homotopical Categories]]_ , volume 113 of Mathematical Surveys and Monographs

A model by [[stratified spaces]] is in 

* {#AyalaFrancisRozenblyum15} [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], _A stratified homotopy hypothesis_ ([arXiv:1502.01713](http://arxiv.org/abs/1502.01713))

A more model-independent abstract formulation is discussed in

* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]], _Infinity category theory from scratch_, 2016 ([pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))


### Surveys and lecture notes 
 {#LectureNotes}

An introduction to [[higher category theory]] through $(\infty,1)$-categories is

* Omar Antol&#237;n Camarena, _A whirlwind tour of the world of $(\infty,1)$-categories_, 2013 ([arXiv:1303.4669](http://arxiv.org/abs/1303.4669))

A survey with an eye towards [[higher algebra]] is in 

* [[Moritz Groth]], _A short course on $\infty$-categories_ ([pdf](http://www.math.uni-bonn.de/~mgroth/InfinityCategories.pdf))

Lecture notes are in 

* [[Dylan Wilson]], _Lectures on higher categories_ ([pdf](https://sites.google.com/a/uw.edu/dwilson/notes))

* [[Emily Riehl]], _[[Categorical Homotopy Theory]]_

See also

* [[Zhen Lin Low]], _[[Notes on homotopical algebra]]_


[[!redirects (∞,1)-category]]
[[!redirects (∞,1)-categories]]
[[!redirects (infinity,1)-categories]]
[[!redirects infinity comma one category]]
[[!redirects (?%2C1)-category]]