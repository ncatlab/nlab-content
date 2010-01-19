

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Given a [[topological group]] $G$ the __orbit category__ $\mathrm{Or}\, G$ (denoted also $\mathcal{O}_G$) is the [[category]] whose 

* objects are the [[homogeneous space]]s ($G$-orbit types) $G/H$, where $H$ is a closed [[subgroup]] of $G$, 

* and whose morphisms are $G$-equivariant maps.  

It is a [[small category|small]] [[enriched category|topologically enriched]] category (though of course if $G$ is a discrete group, the enrichment of $\mathrm{Or}\, G$ is likewise discrete).  

Of course, like any category, it has a [[skeleton]], but as usually defined it is not itself skeletal, since there can exist distinct subgroups $H$ and $K$ such that $G/H\cong G/K$.

More generally, given a family $F$ of subgroups of $G$ which is closed under conjugation and taking subgroups one looks at the full subcategory $\mathrm{Or}_F\,G \subset \mathrm{Or}\,G$ whose objects are those $G/H$ for which $H\in F$.

## Applications

Orbit categories are used often in the treatment of [[Mackey functor]]s from the theory of [[locally compact group]]s and in the definition of [[Bredon cohomology]]. 

It appears in [[equivariant stable homotopy theory]], where the $H$-fixed [[homotopy group]]s of a space form a [[presheaf]] on the [[homotopy category]] of the orbit category (e.g. [page 8, 9 here](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf#page=8)).

## Warning 

This should not be confused with the situation where a group $G$ acts on a groupoid $\Gamma$ so that one obtains the  [[orbit groupoid]].   
