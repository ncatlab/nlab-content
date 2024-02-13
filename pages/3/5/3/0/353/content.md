
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In broad generality, under *$n$-categories* one understands [[higher categories]] with non-trivial [[higher morphisms]] up to dimension $n \in \mathbb{N} \sqcup \{\infty\}$. For $n = 1$ these are the ordinary [[categories]] (or *[[1-categories]]*, for emphasis) of [[category theory]], for $n = 2$ they are the [[2-categories]] (traditionally: "[[bicategories]]") and/or [[double categories]] of [[2-category theory]], for $n = 3$ one also speaks of [[tricategories]], etc. The case $n = \infty$ would broadly refer to the most general notion of [[infinity-categories|$\infty$-categories]] where there is no constraint on the dimensionality of [[higher morphisms]]. 

Especially as $n$ increases, there is a plethora of different definitions of $n$-categories, some differing in generality others different-looking but secretly equivalent. 
A (woefully incomplete) list is given [below](#ListOfDefinitions), with pointers to dedicated entries. Part of the subject of [[higher category theory]] is to understand, organize, systematize and, last not least, apply these definitions. (It is the "$n$" in "$n$-category" that gives the *[[HomePage|nLab]]* its name.)

Often it is important to consider the more fine-grained notion of *[[(n,r)-categories|$(k,n)$-categories]]*, where now $n$ refers only to the maximal dimension of non-[[invertible morphisms|invertible]] [[higher morphisms]] (non-[[equivalences]]) while the [[invertible morphisms|invertible]] [[higher morphisms]] are allowed to range in dimension up to $k \in \mathbb{N} \sqcup \{\infty\}$.

Particularly important here is the limiting case ($k = \infty$) of [[(infinity,n)-categories|$(\infty,n)$-categories]]:
Since [[(infinity,0)-categories|$(\infty,0)$-categories]] aka *[[infinity-groupoids|$\infty$-groupoids]]* are the bare [[homotopy types]] of "spaces" as considered in [[homotopy theory]], [[(infinity,n)-categories|$(\infty,n)$-categories]] are the natural notion of $n$-categories [[internalization|internal]] to [[homotopy theory]] (also: internal to [[homotopy type theory]], up some technical issues) where the notoriously intricate [[coherence laws]] of [[higher category theory]] typically have a particularly natural (if maybe non-explicit) formulation. Therefore many authors these days use "$\infty$-category" as a pseudonym for *[[(infinity,1)-category|$(\infty,1)$-category]]* and some use "$n$-category" as a tacit pseudonym for [[(infinity,n)-categories|$(\infty,n)$-categories]].

In this [[homotopy theory|homotopy theoretic]]-perspective on $n$-categories they are naturally understood as (models for)
*[[directed spaces]]* (with an $n$-fold notion of "direction") and in principle the topics of *[[directed homotopy theory]]* (and *[[directed homotopy type theory]]*) ought to be thought of as essentially synonymous to [[(infinity,n)-categories|$(\infty,n)$-category]] theory, though a genuine perspective of [[directed homotopy theory|directed homotopy]]/[[directed homotopy type theory]] is still in its infancy.

Conversely, for concrete computations it is at times convenient to have *less* flexible and more rigid definitions or at least presentations/models of $n$-categories. In as far as these are still suitably equivalent to the general notion one speaks of *[[semi-strict n-categories]]* and much of [[higher category theory]] revolves around identifying and comparing such *rigidifications*. On the other hand, perfectly *[[strict n-categories|strict $n$-categories]]* are typically too rigid to play more than a niche role in [[higher category theory]].


Finally, it is sometimes useful to subsume degenerate cases in the general pattern of $n$-categories, such as [[0-categories]] ([[sets]]), [[(0,1)-categories]] ([[posets]]) and even *[[(-1)-categories]]* ([[truth values]]) and *[[(-2)-categories]]* (the singleton).


## Categories of $n$-categories 

Just as the collection of all ([[small category|small]]) sets is the prototypical example of a category, so the collection of all small $n$-categories is the prototypical example of an $(n+1)$-category.

Actually, if you define things cleverly, then you can get an $(n+1)$-category of *all* $n$-categories.  If one assumes the [[Grothendieck universe|Axiom of Universes]], then there is a sequence of Grothendieck universes
$$U_0 \subset U_1 \subset U_2 \subset \cdots$$
and we can say a set is **$U_i$-small** if it is an element of $U_i$.  This allows us to make the following definitions:

* $\Set$ is the category of all $U_0$-small sets;
* $\Cat$ is the 2-category of all $U_1$-small categories;
* $2\Cat$ is the 3-category of all $U_2$-small 2-categories;
* etc.

This is a convenient way to settle size questions once and for all for finite $n$, but it doesn\'t really work for $\infty$-categories.

For more, see the discussion at [sci.logic](http://groups.google.com/group/sci.logic/browse_thread/thread/6891c85c2d9b2caf).

## Definitions {#defn}

Here is a list of (some of) the proposed definitions of (weak) $n$-category, with references, and also a list of (some of) the comparisons that have been done.

### List of definitions
 {#ListOfDefinitions}

Many of these definitions are actually "truncations" of definitions of (weak) [[∞-categories]] (aka [[∞-categories]]).  Some others are truncations of a definition of [[(∞,n)-categories]].  A nice overview of (many) of these can be found in Tom Leinster's paper "A survey of definitions of $n$-category."

* Classical explicit definitions of "fully weak" $n$-category exist for $n\le 4$.  Weak 0-categories are [[sets]], weak 1-categories are simply [[categories]] (due to [[Sammy Eilenberg|Eilenberg]] and [[Saunders Mac Lane|Mac Lane]]), weak 2-categories are [[bicategories]] (due to [[Jean Benabou|Benabou]]), weak 3-categories are [[tricategories]] (due to [[Robert Gordon|Gordon]]--[[John Power|Power]]--[[Ross Street|Street]]), and weak 4-categories are [[tetracategories]] (due to [[Todd Trimble]]).  Going on in this way is generally admitted to be infeasible beyond $n=4$.

* [[Ross Street|Street's]] definition: an $n$-category is a [[simplicial set]] satisfying certain horn-filling conditions.  See [[weak complicial set]] and [[simplicial model for weak ∞-categories]].  This is a truncation of a definition of $\omega$-category.  It can be specialized to yield a notion of $(\infty,n)$-category.  The resulting notion of $(\infty,1)$-category is a [[quasicategory]], and the resulting notion of $\infty$-groupoid is a [[Kan complex]].

* [[John Baez|Baez]]--[[James Dolan|Dolan]] definition: an $n$-category is an [[opetopic set]] having enough $n$-universal fillers.  Alternate definitions of opetopes (aka multitopes) have been given by [[Claudio Hermida|Hermida]]--[[Michael Makkai|Makkai]]--[[John Power|Power]] and [[Tom Leinster|Leinster]]; a comparison is due to [[Eugenia Cheng]], see [these](http://arxiv.org/abs/math.CT/0304277) [three](http://arxiv.org/abs/math.CT/0304279) [papers](http://arxiv.org/abs/math.CT/0304284).  Makkai's version can do $\omega$.

* [[Jacques Penon|Penon]]'s definition: (someone describe this please!)  Penon's original definition turned out to be too strict (see [Batanin](http://web.science.mq.edu.au/~mbatanin/Penon1.ps) and [Cheng--Makkai](http://arxiv.org/abs/0907.3961)) because it used [[reflexive globular set|reflexive globular sets]], but a modification of it using [[globular sets]] is still a contender.

* [[Michael Batanin|Batanin]]--[[Tom Leinster|Leinster]] definition: an $n$-category is an $n$-[[globular set]] with an action of a suitable [[globular operad]].  This is a truncation of a definition of $\omega$-category; see [[Batanin ∞-category]].

* [[Todd Trimble|Trimble]]-style definition: An $n$-category is a category weakly enriched over $(n-1)$-categories, where the weakness is parametrized by an [[operad]].  This definition is inductive and thus cannot do $\omega$ in an obvious way, but it has been accomplished using terminal coalgebras; see [[Trimble n-category]].  Alternately, by starting with enrichment in [[spaces]] or [[simplicial sets]], one can obtain directly a notion of [[(∞,n)-category]].  The resulting notion of [[(∞,1)-category]] is an $A_\infty$-[[A∞-category|category]].

* [[Tamsamani]]--[[Carlos Simpson|Simpson]] definition: An $n$-category is a simplicial object in $(n-1)$-categories satisfying object-discreteness and the [[Segal condition]].  This definition is inductive (it is a different way of formalizing "iterated weak enrichment") and thus cannot do $\omega$ in an obvious way.  It does have a natural extension to $(\infty,n)$-categories, and the resulting notion of [[(∞,1)-category]] reduces to a [[Segal category]].  The iterated version of this is that of [[Segal n-category]]. This notion of "weak enrichment" in a [[cartesian model category]] is studied carefully in Simpson's book [[Homotopy Theory of Higher Categories]].

* [[Ieke Moerdijk|Moerdijk]] and [[Ittay Weiss|Weiss]]'s definition uses yet another way of formalizing "iterated weak enrichment," using [[dendroidal sets]] and [[quasi-operad]]s.

* [[Andre Joyal|Joyal]]'s definition: An $n$-category is an $n$-[[cellular set]] satisfying horn-filling conditions.  This definition can do $\omega$ by using $\omega$-cellular sets instead of $n$-cellular sets, and it can do $(\infty,n)$ by requiring different horn-filling conditions on $n$-cellular sets.  The notion of [[(∞,1)-category]] one obtains in this way is a [[quasicategory]], and the resulting notion of $\infty$-groupoid is a [[Kan complex]].  For $n\gt 1$, however, the obvious "horn-filling conditions" are not quite right; [[Dimitri Ara]] has shown how to correct them (albeit not very explicitly), obtaining a definition he calls an [[n-quasicategory]], which form a model category Quillen equivalent to Rezk's definition (below).

* [[Clark Barwick|Barwick]]'s definition (popularized by [[Jacob Lurie|Lurie]] in solving the Baez--Dolan [[cobordism hypothesis]]): an $(\infty,n)$-category is an $n$-fold [[simplicial object|simplicial]] [[topological space]] satisfying completeness and the [[Segal condition]].  See [[n-fold complete Segal space]].  An $n$-category is again defined as an $(\infty,n)$-category in which all $k$-cells are essentially unique for $k\gt n$.  It is not clear whether this definition can do $\omega$.  An $(\infty,1)$-category with this definition is also the same as a [[complete Segal space]].

* [[Charles Rezk|Rezk]]'s definition: An $(\infty,n)$-category is a *simplicial* $n$-cellular set satisfying [[fibrancy]], completeness, and the [[Segal condition]].  An $n$-category can then be defined as an $(\infty,n)$-category in which all $k$-cells are essentially unique for $k\gt n$.  This definition can potentially do $\omega$, although it seems not to have been written down yet.  An $(\infty,1)$-category with this definition is the same as a [[complete Segal space]]. See [[Theta space]].

* [[Georges Maltsiniotis|G. Maltsiniotis]] has apparently extracted a definition of $\infty$-groupoid from [[Pursuing Stacks]] and generalized it to a definition of $\infty$-category; see [this](http://people.math.jussieu.fr/~maltsin/ps/infgrart.pdf) and [this](http://people.math.jussieu.fr/~maltsin/ps/infctart.pdf).

* [[Simona Paoli]]: [[weakly globular n-fold categories]]

### Comparisons

* All definitions produce the correct well-known notion of [[1-category]], up to minor inessential details.

* Since all the common definitions of [[(∞,1)-category]] are known to be equivalent (give references!), the definitions of Street, Trimble, Tamsamani--Simpson, Joyal, Barwick, and Rezk can be said to agree for $(\infty,1)$-categories.

* Julie Bergner has [shown](http://arxiv.org/abs/0710.2254) that all the notions of $\infty$-groupoid obtained from the common notions of $(\infty,1)$-category are equivalent, so the definitions of Street, Trimble, Tamsamani--Simpson, Joyal, Barwick, and Rezk can also be said to agree for $(\infty,0)$-categories.

* It is known that the notions of $(n,0)$-category obtained from categories, bicategories, and tricategories model all [[homotopy n-types]] for $n\le 3$.  Thus, in these cases, the classical definitions can be said to agree with those listed in the previous example.

* In Tom Leinster's paper, proofs are sketched showing that the notion of [[2-category]] obtained in each case looks somewhat like the notion of [[bicategory]].

* Nick Gurski has shown in "Nerves of bicategories as stratified simplicial sets" that Street's definition is correct for $n=2$ (that is, it agrees with bicategories).

* Eugenia Cheng has [shown](http://arxiv.org/abs/math/0304285) that the opetopic definition is correct for $n=2$ (that is, it agrees with bicategories).

* Eugenia Cheng has more recently also [shown](http://arxiv.org/abs/0809.2070) that from any sequence of operads used for iterated enrichment in a Trimble-style definition, one can construct a Batanin--Leinster-style globular operad whose algebras are the $n$-categories obtained in the Trimblean inductive manner.  Not all globular operads can be obtained in this way, however, since those that arise have strict interchange.

## Related concepts

* [[0-category]], [[(0,1)-category]], [[Set]]

* [[category]]

  * [[category object in an (∞,1)-category]]

* [[2-category]], [[bicategory]]

* [[3-category]], [[tricategory]]

* [[4-category]], [[tetracategory]]

* **$n$-category**

  * [[n-category object in an (∞,1)-category]]

* [[(n,1)-category]]

* [[(∞,1)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]

## References

See also the references at *[[higher category theory]]* and especially at *[[(infinity,n)-category]]*.

Exposition of the original [[algebraic definition of higher categories|algebraic notions]] of $n$-categories:

* [[John Baez]], *[The Tale of <em>n</em>-Categories](http://math.ucr.edu/home/baez/week73.html#tale)*

* [[John Baez]], *An Introduction to $n$-Categories*,  in *7th Conference on Category Theory and Computer Science*, Lecture Notes in Computer Science **1290**. Springer (1997) 

* [[Eugenia Cheng]], [[Aaron Lauda]], *Higher-Dimensional Categories: An Illustrated Guidebook* &lbrack;[pdf](http://eugeniacheng.com/wp-content/uploads/2017/02/cheng-lauda-guidebook.pdf)&rbrack;

* [[Tom Leinster]], _A Survey of Definitions of $n$-Category_ &lbrack;[arXiv:math.CT/0107188](http://arxiv.org/abs/math.CT/0107188)&rbrack;

* [[Tom Leinster]], _Higher Operads, Higher Categories_ &lbrack;[arXiv:math/0305049](http://arxiv.org/abs/math/0305049)&rbrack;



[[!redirects $n$-category]]
[[!redirects n-categories]]
[[!redirects weak n-category]]
[[!redirects weak n-categories]]
