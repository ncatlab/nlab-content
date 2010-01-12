
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

By regarding a [[simplicial set]] as an [[object]] in the standard [[model structure on simplicial sets]], one effectively identifies it (up to weak equivalence) with that [[∞-groupoid]] that it presents under [[Kan fibrant replacement]].

If the original simplicial set is the [[nerve]] of a [[category]], the corresponding Kan fibrant replacement is something like the _$\infty$-groupoidification_ of that category.

This way each ordinary category models an [[∞-groupoid]]. The _Thomason_ [[model category]] structure on [[Cat]] exhibits this: in this [[model category]] a morphism between two categories is a weak equivalence, precisely if it induces a weak equivalence of the corresponding $\infty$-groupoids.

It turns out the Thomason model structure on [[Cat]] is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on simplicial sets]].

This is remarkable, in that it says that every [[homotopy n-type|homotopy type]], i. e. every weak equivalence class of $\infty$-groupoids, is obtained by $\infty$-groupoidifying just categories.

In fact, every cofibrant object in this structure is a [[poset]]. Since every object in a model category is weakly equivalent to a cofibrant one, this means that even the [[nerve]]s of just posets are sufficient to model all homotopy types.


This is a rather curious aspect of the Thomason model on [[Cat]]: it does not really have anything intrisically to do with [[category|categories]], but rather uses these as a way to present [[∞-groupoid]]s. It particular, it does not see the [[equivalence of categories|equivalences of categories]]. 
There is a _different_ model structure on [[Cat]] in which weak equivalences are the "true" weak [[equivalence of categories|equivalences of categories]] (not of anything constructed from them). This is called the [[folk model structure on Cat]].

## References

The original reference is

* R. W. Thomason, _Cat as a closed model category_,
Cahiers Topologie G&#233;om. Diff&#233;rentielle **21**, no. 3 (1980), pp. 305--324. MR0591388 (82b:18005) <a href="http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_3_305_0">numdam scan</a>

A correction to this article was made in

* [[Denis-Charles Cisinski]], _Les morphisme de Dwyer ne sont pas stables par r&eacute;tractes_, Cahiers Topologie et G&eacute;om. Diff&eacute;rrentielle Cat&eacute;goriques, **40** no. 3 (1999), pp. 227--231. ([Numdam](http://www.numdam.org/item?id=CTGDC_1999__40_3_227_0))

There it was clarified that every cofibrant object in the Thomason model structure is a [[poset]]. 

A useful review of the Thomason model structure and a generalization of the model structure to [[n-fold category|n-fold categories]] is given in 

* Thomas M. Fiore, [[Simona Paoli]], _A Thomason Model Structure on the Category of Small n-fold Categories_ ([arXiv](A Thomason Model Structure on the Category of Small n-fold Categories))