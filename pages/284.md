
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

There are a number of different ways to make the idea of an $(\infty,1)$-category precise, including [[quasi-categories]], [[simplicial set|simplicially]] [[enriched categories]], [[topologically enriched categories]], [[Segal categories]], [[complete Segal spaces]], and $A_\infty$-[[A-infinity categories|categories]] (most of which can be done either simplicially or topologically).  Additionally, any notion of [[∞-category]] can be specialized to a notion of $(\infty,1)$-category by simply requiring all $n$-cells for $n\gt 1$ to be invertible.


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

* the [[(infinity,1)-category of (infinity,1)-functors|quasi-category of (∞,1)-functors]] between two [[quasi-categories]] $C$ and $D$;

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

## A model-independent approach

In practice, it can be useful to be able to treat all "presentations of $(\infty,1)$-categories" on the same equal footing (e.g. relative categories and topologically-enriched categories).  While truly model-independent foundations of $(\infty,1)$-category theory do not (yet) exist, this can be accomplished _within_ any model of $(\infty,1)$-categories, which we proceed to describe.  As quasicategories are by far the most well-developed, we use them as an ambient framework.  We also take care to make as few choices (even "contractible" ones) as possible.  However, we do not explicitly mention set-theoretic issues, though these are easily handled using Grothendieck universes.

1. Consider the $Kan$-enriched category $\underline{QCat}$ of quasicategories; for quasicategories $C$ and $D$, the Kan complex of morphisms between them is $\underline{hom}_{\underline{QCat}} = \iota(\underline{hom}_{sSet}(C,D))$, the largest Kan complex contained in their internal hom simplicial set.

1. Define a _relative quasicategory_ to be a quasicategory equipped with a full sub-quasicategory of "weak equivalences" containing all equivalences.  For relative quasicategories $(C,W_C)$ and $(D,W_D)$, write $\underline{hom}_{\underline{RelQCat}}((C,W_C),(D,W_D)) \subset \underline{hom}_{\underline{QCat}}(C,D)$ for the sub-Kan complex consisting of those maps which take $W_C$ into $W_D$.  Note that using this definition, this is actually the inclusion of a disjoint union of connected components among Kan complexes (in the strictest possible sense).

1. There is an evident inclusion $min : \underline{QCat} \to \underline{RelQCat}$, which takes a quasicategory $C$ to the relative quasicategory $(C,C^\simeq)$.

1. Although a Quillen equivalence $M_1 \rightleftarrows M_2$ between model categories determines an equivalence of homotopy categories, note that neither adjoint functor need preserve weak equivalences.  On the other hand, the restrictions $M_1^c \hookrightarrow M_1 \rightarrow M_2$ and $M_1 \leftarrow M_2 \hookleftarrow M_2^f$ (to the cofibrant objects of $M_1$ and the fibrant objects of $M_2$) do preserve weak equivalences, and these determine a hexagonal diagram of weak equivalences between relative categories (in the Barwick--Kan model structure), as in [MazelGee16, Figure 1](http://nyjm.albany.edu/j/2016/22-4.html).

1. Using the previous observation, expand the diagram in the introduction of [BarwickSchommerPries](http://arxiv.org/abs/1112.0040) (relating a great many Quillen equivalent model categories presenting "the homotopy theory of $(\infty,1)$-categories") into a diagram of weak equivalences between relative categories.  As relative categories are particular examples of relative quasicategories, this defines a functor $F : K \to \underline{RelQCat}$ among fibrant objects of $(Cat_{sSet})_{Bergner}$.

1. Now, apply the right Quillen equivalence $N^{hc} : (Cat_{sSet})_{Bergner} \to sSet_{Joyal}$ (the homotopy-coherent nerve) to this cospan $\underline{QCat} \xrightarrow{min} \underline{RelQCat} \leftarrow K$.

1. The morphism $N^{hc}(min)$ of quasicategories admits a contractible Kan complex worth of quasicategorical left adjoints, any of which presents the _localization_ of relative quasicategories.  Choose one, and denote this quasicategorical adjunction by $L : N^{hc} (\underline{RelQCat}) \rightleftarrows N^{hc} ( \underline{QCat}) : min$.

1. It follows from the main theorem of [Toen](http://arxiv.org/abs/math/0409598) that the composite map $L \circ N^{hc}(F) : N(K) \cong N^{hc}(K) \to N^{hc}(\underline{RelQCat}) \to N^{hc}(\underline{QCat})$ is "essentially contractible" in the quasicategorical sense.  More precisely, for any cofibration into an acyclic object $i : N(K) \to K' \approx pt$ in $sSet_{Joyal}$, there exists a contractible Kan complex worth of extensions of $L \circ N^{hc}(F)$ over $i$.

1. Define $(The(\infty,1)Cats) \subset N^{hc}(\underline{QCat})$ to be the maximal sub-Kan complex generated by the image of $L \circ N^{hc}(F)$.  We write $Cat_{(\infty,1)} \in (The(\infty,1)Cats)$ for _any_ vertex, and propose that to work "model-independently" is to work _within_ $Cat_{(\infty,1)}$.

This sequence of maneuvers balances twin aims.  On the one hand, Toen's theorem asserts that after choosing a basepoint, this Kan complex is a model for $B(\mathbb{Z}/2)$.  Thus, any sort of object which might be considered as "a presentation of an $(\infty,1)$-category" canonically determines an object of $Cat_{(\infty,1)}$ (where "canonical" must still be taken in the quasicategorical sense).  On the other hand, it is completely independent of which vertex of $(The(\infty,1)Cats)$ we choose.

[This diagram](http://ncatlab.org/nlab/files/relcats-modelcats-qcats-inftycats.jpg), taking place in $N^{hc}(\underline{QCat})$, elaborates on certain salient aspects of the passage from models of $(\infty,1)$-categories to a model-independent approach.  (For a small amount of explanation of this diagram, see [here](https://nforum.ncatlab.org/discussion/7029/a-diagram-relating-different-models-of-inftycategories/#Item_0).)


## Related concepts

* [[table - models for (∞,1)-categories]]

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]], [[(2,1)-category]]

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

* {#Joyal08} [[André Joyal]], _The theory of quasicategories and its applications_ lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008 ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]])

Further notes (where the term "[[logos]]" is used instead of [[quasi-category]]) are in

* {#Joyal08} [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf), [[JoyalOnLogoi2008.pdf:file]])
  

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

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_,  In: [[John Baez]], [[Peter May]] (eds.),  _[[Towards Higher Categories]]_, The IMA Volumes in Mathematics and its Applications, vol 152, Springer 2007 ([arXiv:math/0610239](http://arxiv.org/abs/math/0610239), [doi:10.1007/978-1-4419-1524-5_2](https://doi.org/10.1007/978-1-4419-1524-5_2))

* [[Julia Bergner]], _Equivalence of models for equivariant $(\infty,1)$-categories_, Glasgow Mathematical Journal, Volume 59, Issue 1 (2016) ([arXiv:1408.0038](https://arxiv.org/abs/1408.0038), [doi:10.1017/S0017089516000136](https://doi.org/10.1017/S0017089516000136))

More discussion of the other two models can be found at

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

and in the references listed at _[[(∞,n)-category]]_.

The relation between [[quasi-category|quasi-categories]] and [[simplicially enriched categories]] was discussed in detail in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_, Algebraic & Geometric Topology 11 (2011) 263–325 ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469), [doi:10.2140/agt.2011.11.263](http://dx.doi.org/10.2140/agt.2011.11.263))

The presentation of $(\infty,1)$-categories by [[homotopical categories]] and [[model categories]] is discussed in

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]],  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories and Homotopical Categories]]_ , volume 113 of Mathematical Surveys and Monographs

A model by [[stratified spaces]] is in 

* {#AyalaFrancisRozenblyum15} [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], _A stratified homotopy hypothesis_ ([arXiv:1502.01713](http://arxiv.org/abs/1502.01713))

A more model-independent abstract formulation is discussed in

* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]], _Infinity category theory from scratch_, Higher Structures Vol 4, No 1 (2020) ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314), [pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))


And is being developed in a book in progress, regularly being updated:

* [[Emily Riehl]] and [[Dominic Verity]], _Elements of $\infty$-Category Theory_, (2019) ([pdf](http://www.math.jhu.edu/~eriehl/elements.pdf))

For discussion in [[homotopy type theory]] see _[[internal category in homotopy type theory]]_ and see

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], _A type theory for synthetic $\infty$-categories_ ([arXiv:1705.07442](https://arxiv.org/abs/1705.07442))

* {#Riehl18} [[Emily Riehl]], _The synthetic theory of ∞-categories vs the synthetic theory of ∞-categories_, talk at [Vladimir Voevodsky Memorial Conference 2018](http://www.math.ias.edu/vvmc2018) ([pdf](http://www.math.jhu.edu/~eriehl/Voevodsky.pdf))

### Surveys and lecture notes 
 {#LectureNotes}

An introduction to [[higher category theory]] through $(\infty,1)$-categories is

* Omar Antol&#237;n Camarena, _A whirlwind tour of the world of $(\infty,1)$-categories_, 2013 ([arXiv:1303.4669](http://arxiv.org/abs/1303.4669))

A foundational set of lecture notes:

* [[Denis-Charles Cisinski]], _Higher category theory and homotopical algebra_,  Cambridge University Press 2019 ([doi:10.1017/9781108588737](https://doi.org/10.1017/9781108588737), [pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))

A survey with an eye towards [[higher algebra]] is in 

* [[Moritz Groth]], _A short course on $\infty$-categories_ ([pdf](http://www.math.uni-bonn.de/~mgroth/InfinityCategories.pdf))

A survey on various notions of [[homotopical categories]]:

* [[Emily Riehl]], _Homotopical categories: from model categories to (∞,1)-categories_, in: [[Andrew J. Blumberg]], [[Teena Gerhardt]], [[Michael A. Hill]] (eds,) *Stable categories and structured ring spectra*,  MSRI Book Series, Cambridge University Press ([arXiv:1904.00886](https://arxiv.org/abs/1904.00886))

Also:

* [[Markus Land]], *Introduction to Infinity-Categories*, Birkh&auml;user 2021 ([doi:10.1007/978-3-030-61524-6](https://link.springer.com/book/10.1007/978-3-030-61524-6))

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