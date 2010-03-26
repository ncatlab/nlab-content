[[!redirects partially ordered category]]
_Partially ordered category_ is a category together with [[partial order]]ing $\subseteq$ of each its Hom-set such that
$$ f_1 \subseteq f_2 \;\wedge\; g_1 \subseteq g_2 \;\Rightarrow\; g_1 \circ f_1 \subseteq g_2 \circ f_2 $$
for any morphisms $f_1$, $g_1$, $f_2$, $g_2$ such that the composites above are defined.

>[[VictorPorton|Victor]]: I changed the earlier notion of partial ordered category where I was requiring partial order on the entire set of morphisms.

Compare the notion of [[locally partially ordered category]].  A partially ordered category in which the [[source]] and [[target]] maps preserve the partial order is a category *[[internal category|internal]] to* the category [[Pos]] of [[poset]]s, while a locally partially ordered category is a category *[[enriched category|enriched]] over* $Pos$.  Similarly, such a partially ordered category is a special kind of [[double category]], while a locally partially ordered category is a special kind of $2$-[[2-category|category]].

## Partially ordered dagger categories ##

For a partially ordered dagger (pre)category I will additionally require (for any morphisms $f$ and $g$)
\[ f^{\dagger} \subseteq g^{\dagger} \Leftrightarrow f \subseteq g. \]

  For a partially ordered dagger category I will call
  _monovalued_ morphism such a morphism $f$ that $f \circ f^{\dagger}
  \subseteq 1_{\mathrm{Dst} f}$.

  For a partially ordered category with inverses I will call _entirely defined morphism_ such a morphism $f$ that $f^{\dagger} \circ f \supseteq
  1_{\mathrm{Src} f}$.

+--{: .query}
[[Tim Porter|Tim]]: The particular case of an ordered groupoid (in which each $f^{-1}$ is the inverse of $f$) is called an ordered groupoid.  This has been studied extensively by Mark Lawson, for instance see

Lawson, Mark V.
Constructing ordered groupoids. Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 2 (2005), p. 123-138,
URL stable: http://www.numdam.org/item?id=CTGDC_2005__46_2_123_0

or his book: M.V. Lawson,  Inverse semigroups: the theory of partial symmetries, World Scientific, 1998. 

He makes the point that they were initially studied by Ehresmann and are very closely related to inverse semi-groups.  
=--

See more in [Funcoids and Reloids article](http://www.mathematics21.org/binaries/funcoids-reloids.pdf). Feel free to copy the information from this my article to nLab wiki.

## See also ##
* [[generalized continuity]]
