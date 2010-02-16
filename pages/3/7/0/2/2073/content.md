
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Marked simplicial sets are [[simplicial set]]s with a little bit of extra [[stuff, structure, property|structure]] that allows to model [[Cartesian fibration]]s of [[simplicial set]]s precisely as the fibrations in the [[model structure on marked simplicial over-sets]]: the marked edges in a (fibrant) marked simplicial set are the [[Cartesian morphism]]s in the coprresponding [[(∞,1)-category]].


## Definition 


A **marked simplicial set** is 

* a pair $(S,E)$ consisting of 

  * a [[simplicial set]] $S$ 

  * and a subset $E \subset S_1$ of edges of $S$, called the _marked edges_, 

* such that

  * all degenerate edges are marked edges.

A morphism $(S,E) \to (S',E')$ of marked simplicial sets is a morphism $f : S \to S'$ of [[simplicial set]]s that carries marked edges to marked edges in that $f(E) \subset E'$.

# Notation #

* The category of marked simplicial sets is denoted $Set^+$.

* for $S$ a [[simplicial set]] let

  * $S^\flat$ or $S^{min}$ be the minimally marked simplicial set: only the degenerate edges are marked;

  * $S^#$ or $S^{max}$ be the maximally marked simplicial set: every edges is marked.

* for $p : X \to S$ a [[Cartesian fibration]] of [[simplicial set]]s let

  * $X^\sharp$ or $X^{cart}$ be the cartesian marked simplicial set: precisely the $p$-[[cartesian morphism]]s are marked

* For $X$ and $Y$ marked simplicial sets let

  * $Map^\flat(X,Y)$ be the [[simplicial set]] underlying the [[internal hom]] $Y^X$

  * $Map^#(X,Y)$ the simplicial set consisting of all simplices $ \sigma \in Map^\flat(X,Y)$ such that every edge of $\Sigma$ is a marked edge of $Y^X$.

# Applications #

The main point of marked simplicial sets is to carry the [[model structure on marked simplicial over-sets]]. This is a model for the [[(∞,1)-category]] of [[cartesian fibration]]s of [[(infinity,1)-category|(∞,1)-categories]].


## References 

Section 3.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
