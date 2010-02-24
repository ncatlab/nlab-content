
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

$\Fin\Set$ is the [[category]] of [[finite set]]s and all [[function]]s between them: the [[full subcategory]] of [[Set]] on finite sets.  


(For [[constructive mathematics|constructive]] purposes, take the strictest sense of 'finite'.)

It is easy (and thus common) to make $\Fin\Set$ [[skeleton|skeletal]]; there is one [[object]] for each [[natural number]] $n$ (including $n = 0$), and a [[morphism]] from $m$ to $n$ is an $m$-tuple $(f_0, \ldots, f_{m-1})$ of numbers satisfying $0 \leq f_i \lt n$.  This amounts to identifying $n$ with the set $\{0, \ldots, n - 1\}$.  (Sometimes $\{1, \ldots, n\}$ is used instead.)

## Subcategories of $FinSet$

The [[simplex category]] $\Delta$ embeds into $\Fin\Set$ as a category with the same objects but fewer morphisms. The category of [[cyclic set]]s introduced by Connes lies in between. All the three are special cases of extensions of $\Delta$ by a group in a particularly nice way. Full classification of allowed "skewsimplical groups" has been given by Krasauskas and independently by Loday and Fiedorowicz.


## In topos theory

The category $FinSet$ is a [[topos]] and the inclusion $FinSet \hookrightarrow Set$ is a [[logical morphism]] of toposes. ([[Elephant|Elephant, example 2.1.2]]).

Mathematics done within or about $\Fin\Set$ is [[finite mathematics]].

A [[presheaf]] of sets on $\Fin\Set$ is a [[symmetric set]]; one generally uses the skeletal version of $\Fin\Set$ for this.

The [[copresheaf]] category $[FinSet,Set]$ is the [[classifying topos]] for the [[theory]] _of objects_ (the empty theory over the signature with one sort and no primitive symbols except equality). ([[Elephant|Elephant, D3.2]]).


category: category