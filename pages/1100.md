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
(recall the notion of [[(n,r)-category]] and see the general discussion at [[infinity-topos]]):

* Working in the $(\infty,1)$-[[(infinity,1)-category|category]] 
[[Infinity-Grpd]]
of $(infinity,0)$-[[infinity-groupoid|categories]] 
is the same as 
doing [[topology]]. The point of 
[[infinity-stack]]s
is to pass to _parameterized_ 
$(infinity,0)$-[[infinity-groupoid|categories]], 
namely 
[[(infinity,1)-presheaf]] categories: 
these [[(infinity,1)-topos|(infinity,1)-topoi]]
behave much like the $(\infty,1)$-category 
[[Infinity-Grpd]]
but their objects are generalized 
[[space and quantity|spaces]] 
with higher [[homotopy|homotopies]]
that may carry 
more structure, for instance they may
be $\infty$-[[differentiable stack]]s if one considers
[[infinity-stack]]s on [[Diff]].




#Definition#

A Grothendieck--Rezk--Lurie **$(\infty,1)$-topos** is an [[(infinity,1)-category]] $X$ satisfying the following equivalent conditions:
 

* $X$ is an [[(infinity,1)-category of (infinity,1)-sheaves]]: in other words, there exists a small [[(infinity,1)-category]] $S$ and an accessible left [[exact (infinity,1)-functor|exact]] [[(infinity,1)-functor]] $\bar {(-)} : PSh(S) \to X$
from [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on $X$, which has a [[(infinity,1)-fully faithful functor|fully faithful]] [[adjoint (infinity,1)-functor|right adjoint]].

* $X$ satisfies the $(\infty,1)$-categorical analogs of [[Giraud's axioms]]:
  * $X$ is [[presentable category|presentable]];
  * [[(infinity,1)-colimit]]s in $X$ are universal;
  * [[coproduct]]s in $X$ are [[disjoint coproducts|disjoint]];
  * every [[groupoid object]] in $X$ is [[quotient object|effective]]. 

#References#

Section 6.1 of

* [[Jacob Lurie]], [[Higher Topos Theory]]
