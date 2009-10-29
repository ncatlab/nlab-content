<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

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

#Definition#

A Grothendieck--Rezk--Lurie **$(\infty,1)$-topos** is an [[(∞,1)-category]] $X$ satisfying the following equivalent conditions:
 

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


# Models #

Another main theorem about $(\infty,1)$-toposes is that
[[models for ∞-stack (∞,1)-toposes]] are given by the [[model structure on simplicial presheaves]].


#References#

Section 6.1 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects (infinity,1)-topoi]]
[[!redirects (infinity,1)-toposes]]
[[!redirects (∞,1)-topos]]
[[!redirects (∞,1)-topoi]]
[[!redirects (∞,1)-toposes]]