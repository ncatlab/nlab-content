<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall the following familiar 1-categorical statement:

* Working in the 1-[[category]] 
[[Set]]
of [[0-category|0-categories]] is the same as 
doing [[set theory]]. The point of 
[[Categories and Sheaves|categories and sheaves]]
is to pass to _parameterized_ 
[[0-category|0-categories]], namely 
[[presheaf]] categories: these [[topos|topoi]]
behave much like the category [[Set]]
but their objects are generalized 
[[space and quantity|spaces]] that may carry 
more structure, for instance they may
be [[generalized smooth space]]s if one considers
(pre)[[sheaf|sheaves]] on [[Diff]].

One can think of 
$(\infty,1)$-topoi as
the generalization of the above situation
from $1$ to $(\infty,1)$ 
(recall the notion of [[(n,r)-category]] and see the general discussion at [[∞-topos]]):

* Working in the [[(∞,1)-category]] 
[[∞Grpd]]
of [[infinity-groupoid|(∞,0)-categories]] 
is the same as 
doing [[topology]]. The point of 
[[∞-stacks]]
is to pass to _parameterized_ [[infinity-groupoid|(∞,0)-categories]], 
namely 
[[(∞,1)-presheaf]] categories: 
these [[(∞,1)-topoi]]
behave much like the $(\infty,1)$-category 
[[∞Grpd]]
but their objects are generalized 
[[space and quantity|spaces]] 
with higher [[homotopies]]
that may carry 
more structure, for instance they may
be $\infty$-[[differentiable stacks]] if one considers
[[∞-stacks]] on [[Diff]].

## Definition

A [[Alexander Grothendieck|Grothendieck]]--[[Charles Rezk|Rezk]]--[[Jacob Lurie|Lurie]] **$(\infty,1)$-topos** is an [[(∞,1)-category]] $X$ satisfying the following equivalent conditions:
 

* $X$ is an [[(∞,1)-category of (∞,1)-sheaves]] (meaning: of [[∞-stack]]s): 

  * there exists a small [[(∞,1)-category]] $S$ and an accessible left [[exact (infinity,1)-functor|exact]] [[(∞,1)-functor]] $\bar {(-)} : PSh(S) \to X$ from [[(∞,1)-presheaves]] on $X$, which has a [[(infinity,1)-fully faithful functor|fully faithful]] [[right adjoint]].

* $X$ satisfies the $(\infty,1)$-categorical analogs of [[Giraud's axioms]]:
  * $X$ is [[presentable (infinity,1)-category|presentable]];
  * [[limit in quasi-categories|(∞,1)-colimits]] in $X$ [[universal colimits|are universal]];
  * [[coproduct]]s in $X$ are [[disjoint coproduct|disjoint]];
  * every [[groupoid object in an (infinity,1)-category|groupoid object]] in $X$ is [[quotient object|effective]] (i.e. has a [[delooping]]). 

The equivalence of these two characterizations is one of the main theorems of [[Higher Topos Theory|HTT]].

The second characterization is derived from the following equivalent one:

an [[(∞,1)-topos]] is

* a [[presentable (∞,1)-category]]

* with [[universal colimits]]

* and with [[object classifier]]s.

## Types of $(\infty,1)$-toposes

### Topological localizations / $(\infty,1)$-sheaf toposes

for the moment see

* [[topological localization]]

### Hypercomplete $(\infty,1)$-toposes

for the moment see 

* [[hypercomplete (∞,1)-topos]]

## Models 

Another main theorem about $(\infty,1)$-toposes is that
[[models for ∞-stack (∞,1)-toposes]] are given by the [[model structure on simplicial presheaves]]. See there for details


## $(\infty,1)$-topos theory {#ToposTheory}

Most of the standard constructions in [[topos theory]] have or should have  immediate generalizations to the context of $(\infty,1)$-toposes, since all notions of [[category theory]] exist for [[(∞,1)-categories]].

For instance there are evident notions of

* [[geometric morphism]]s between $(\infty,1)$-toposes, such as the [[global section]] geometric morphism to the [[terminal object|terminal]] [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]] $(\infty,1)$-topos [[? Grpd]].

Moreover, it turns out that $(\infty,1)$-toposes come with plenty of internal structures, more than canonically present in an ordinary topos. 
Every $(\infty,1)$-topos comes with its intrinsic notion of

* [[cohomology|cohomology in an (∞,1)-topos]]

and with an intrinsic notion of

* [[homotopy groups in an (∞,1)-topos|homotopy in an (∞,1)-topos]].


In classical topos theory, cohomology and homotopy of a topos $E$ are defined in terms of [[simplicial object]]s in $C$. If $E$ is a [[sheaf topos]] with [[site]] $C$ and [[point of a topos|enough point]]s, then  this classical construction is secretly really a model for the intrinsic cohomology and homotopy in the above sense of the  [[hypercomplete (∞,1)-topos]] of [[∞-stack]]s on $C$.

The beginning of a list of all the structures that exist intrinsically in an $(\infty,1)$-topos is at

* [[schreiber:structures in an (∞,1)-topos]].

But **$(\infty,1)$-topos theory** in the style of an $\infty$-analog of the [[Elephant]] is only barely beginning to be conceived. 

There are some indications as to what the

* [[internal logic of an (∞,1)-topos]]

should be.



## References

In retrospect it turns out that the [[homotopy category of an (∞,1)-category|homotopy categories]] of [[(∞,1)-topos]]es have been known since

* [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_ .

And the [[model category]] theory models have been known since [[Andre Joyal]] proposed the [[model structure on simplicial sheaves]] in his letter to [[Alexander  Grothendieck]].

This work used 1-categorical [[site]]s. The generalization to [[(∞,1)-category|(∞,1)categorical sites]] -- modeld by [[model site]]s -- was discussed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math.AG/0207028))

The intrinsic category-theoretic definition of an [[(∞,1)-topos]] was given in section 6.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

building on ideas by [[Charles Rezk]]. There is is also proven that the Brown-Joyal-Jardine-To&euml;-Vezzosi models indeed precisely model $\infty$-stack $(\infty,1)$-toposes. Details on this relation are at [[models for ∞-stack (∞,1)-toposes].



[[!redirects (infinity,1)-topoi]]
[[!redirects (infinity,1)-toposes]]
[[!redirects (∞,1)-topos]]
[[!redirects (∞,1)-topoi]]
[[!redirects (∞,1)-toposes]]