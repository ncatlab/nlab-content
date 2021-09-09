
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **locally partially ordered category** is a [[category]] together with [[partial order]] $\subseteq$ on each of its [[hom-set|hom-sets]] such that
$$ f_1 \subseteq f_2 \;\wedge\; g_1 \subseteq g_2 \;\Rightarrow\; g_1 \circ f_1 \subseteq g_2 \circ f_2 $$
for any morphisms $f_1$, $g_1$, $f_2$, $g_2$ such that the composites above are defined. In other words, a category enriched in [[Pos]], the category of [[posets]].

Compare this to the notion of category [[internal category|internal]] to [[Pos]].

Similarly, such a partially ordered category can be considered as a special kind of [[double category]], while a [[locally posetal 2-category|locally partially ordered category]] can be considered as a special kind of $2$-[[2-category|category]].

>Old discussion:

+--{: .query}
[[Sridhar Ramesh]]: Is there meant to also be a partial ordering on the objects in addition to those on the Hom-sets? (Without this, I cannot make sense of the source and target maps preserving the partial order. Indeed, as it stands, I don't see how this definition is any different from that of a locally partially ordered category.)

[[David Roberts]]: I agree: the first definition is of a category enriched in [[Pos]], whereas the reference to source and target maps clearly talks about an internal category. I've edited it.
=--


## Partially ordered $\dagger$-categories ##

For a partially ordered $\dagger$-[[dagger-category|category]] we can (optionally?) require that
\[ 
  f^{\dagger} \subseteq g^{\dagger} \Leftrightarrow f \subseteq g
\]
for any morphisms $f$ and $g$.

>The following nomenclature points were raised by one of the previous contruibutors. What do people think? Are they justified or in conflict with existing terminology? Are there examples where the conditions come up naturally?


 * For a partially ordered $\dagger$-category I will call _monovalued_ morphism such a morphism $f$ that $f \circ f^{\dagger} \subseteq 1_{\mathrm{Dst} f}$.

 * For a partially ordered category with inverses I will call _entirely defined morphism_ such a morphism $f$ that $f^{\dagger} \circ f \supseteq
1_{\mathrm{Src} f}$.




## Partially ordered groupoids

The particular case of an ordered groupoid (in which each $f^{-1}$ is the inverse of $f$) is called an ordered groupoid.  This has been studied extensively by Mark Lawson, for instance see

* [[ Mark V. Lawson]],  _Constructing ordered groupoids_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 2 (2005), p. 123-138,
([numdam](http://www.numdam.org/item?id=CTGDC_2005__46_2_123_0))

or his book: 

* [[M.V.Lawson]], _Inverse semigroups: the theory of partial symmetries_, World Scientific, 1998. 

He makes the point that they were initially studied by Ehresmann and are very closely related to inverse semi-groups.  


## See also ##
* [[generalized continuity]]


[[!redirects partially ordered category]]
[[!redirects partially ordered dagger-category]]
[[!redirects partially ordered dagger category]]
[[!redirects partially ordered †-category]]
