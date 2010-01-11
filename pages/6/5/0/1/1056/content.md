
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

By regarding a [[simplicial set]] as an object in the standard [[model structure on simplicial sets]], one effectively identifies it (up to weak equivalence) with that [[∞-groupoid]] that it presents under [[Kan fibrant replacement]].

If the original simplicial set is the [[nerve]] of a [[category]], the corresponding Kan fibrant replacement is something like the _$\infty$-groupoidification_ of that category.

This way each ordinary category models an [[∞-groupoid]]. The _Thomason_ [[model category]] structure on [[Cat]] exhibits this: in this [[model category]] two categories are weakly equivalent, if the $\infty$-groupoids that they present are equivalent.

It turns out the Thomason model structure on [[Cat]] is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on simplicial sets]].

This is remarkable, in that it says that every [[homotopy n-type|homotopy type]], i. e. every weak equivalence class of $\infty$-groupoids, is obtained by $\infty$-groupoidifying just categories.

In fact, Thomason claimed that cofibrant objects in his structure are [[poset]]s, which would mean that even just posets are already sufficient to model all homotopy types via Kan fibrant replacement of their nerves. However, apparently somebody observed some problem with Thomasson's original claim to this effect. [[Urs Schreiber|I]] am not sure what the status of the claim is.

There is also a model structure on [[Cat]] in which weak equivalences are the "true" weak [[equivalence of categories|equivalences of categories]] (not of anything constructed from). This is called the [[folk model structure on Cat]].

## References

The original reference is

* R. W. Thomason, _Cat as a closed model category_ .
Cahiers Topologie G&#233;om. Diff&#233;rentielle 21 (1980), no. 3, 305--324. MR0591388 (82b:18005) <a href="http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_3_305_0">numdam scan</a>

A useful review of this and a generalization of the model structure to [[n-fold category|n-fold categories]] is given in 

* Thomas M. Fiore, Simona Paoli, _A Thomason Model Structure on the Category of Small n-fold Categories_ ([arXiv](A Thomason Model Structure on the Category of Small n-fold Categories))