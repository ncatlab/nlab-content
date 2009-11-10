<div class="rightHandSide toc">
[[!include higher category theory - contents]]

***

[[!include higher algebra - contents]]

</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The notion of _$(\infty,1)$-operad_ is to that of [[(∞,1)-category]] as [[operad]] is to [[category]].

So, roughly, an $(\infty,1)$-operad is an algebraic structure that has for each given type of input and one type of outpout an [[∞-groupoid]] of operations that take these inputs to that output.

#Definition#

Two models for $(\infty,1)$-operads exist to date, one by Cisinski-[[Ieke Moerdijk|Moerdijk]], the other by [[Jacob Lurie|Lurie]].

##in terms of dendroidal sets##

Here [[simplicial set]]s are generalized to [[dendroidal set]]s. The theory of $(\infty,1)$-operads is then formulated in terms of dendroidal sets in close analogy to how the theory of [[(∞,1)-category|(∞,1)-categories]] is formulated in terms of [[simplicial set]]s.

There is a [[model  structure on dendroidal sets]] whose fibrant objest are the **quasi-operad**s in direct analogy to the notion of [[quasi-category]]. 

Here are two blog entries on talks on this stuff:

* [Dendroidal Sets and Infinity-Operads](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* [Moerdijk on Infinity Operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)

##in terms of $(\infty,1)$-categories fibred over Segal's category##

In this approach an $(\infty,1)$-operad $C^\otimes$ is regarded as an [[(∞,1)-category]] $C$ -- the unary part of the $(\infty,1)$-operad to be described-- with extra structure that determines [[(∞,1)-functor]]s $C^{\times n} \to C$.

This and the conditions on these are encoded in requiring that $C^\otimes$ is an $(\infty,1)$-functor $C^\otimes \to \Gamma$ over [[Segal's category]] $\Gamma$ of pointed finite sets, satisfying some conditions.

In particular, any [[symmetric monoidal (∞,1)-category]] yields an example of an $(\infty,1)$-operad in this sense.  In fact, symmetric monoidal $(\infty,1)$-categories can be *defined* as $(\infty,1)$-operads such that the functor $C^\otimes \to \Gamma$ is a [[coCartesian fibration]].  (For the moment, see [[monoidal (infinity,1)-category]] for more comments and references on higher operads in this context.)

This is the approach described in (the new version of !)

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www-math.mit.edu/~lurie/papers/DAG-III.pdf))


[[!redirects (∞,1)-operad]]