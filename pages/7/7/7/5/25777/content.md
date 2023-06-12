
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Recall that *$A$-algebras*, in the usual sense of [[associative algebras]] over a [[commutative ring]] $A$, are [[rings]] $R$ equipped with ring [[homomorphisms]] $\eta \colon A\to Z(R)$ from $A$ to their [[center]] (and a plain [[unital ring]] $R$ is an [[associative algebra]] over the [[integers]] $\mathbb{Z}$).

By the term *$A$-rings* one refers to the generalization of this notion to the case where $A$ is not necessarily commutative or the [[image]] of $\eta$ is not necessarily in the center of $R$. Hence $A$-rings are general objects in the [[coslice category]] $A/Rings$ (also denoted $A \downarrow Ring$) for arbitrary $A$.

In some sense a dual notion is of an $A$-coring.

## Details

If $K$ is a commutative ring (or especially a [[field]]), then an [[associative algebra]] over $K$ is a monoid object in $K$-[[Mod]]; this is a special case of the previous section.

If $A$ is a noncommutative ring, then a __ring over $A$__, or simply an __$A$-ring__, is a monoid object $R$ in $A$-[[Bimod]] (that is, in $_A Mod _A$).  Every $A$-ring is a ring in the usual sense, in the sense that there is an obvious [[forgetful functor]] to the usual rings. In fact the unit map $A \to R$ is a morphism of rings, and the category of $A$-rings is precisely the [[coslice category]] or under-category $A/Ring$. Thus by category-theoretic rules, one might be led to unconventionally call $A$-rings "rings *under* $A$". Unfortunately, standard name for $A$-rings is "rings *over* $A$", like conventionally calling $k$-algebras the "algebras *over* $K$". 

Unlike for the $k$-algebras, the multiplication $R\times R\to R$ which is the morphism of $A$-[[bimodules]], is not (left) $A$-linear in the *second* factor, but only $A^{op}$-linear (that is, $A$-linear on the right). In other words, the axiom for $K$-algebras $k (r s) = r (k s)$ is not true, for $k\in A$, $r,s\in R$, although $k (r s) = (k r) s$ and $(r s) k = r (s k)$ do hold.  

Both for a discussion for under-over and also for this difference between $K$-algebras and $A$-rings see the Caf&#233;\'s [quick algebra quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html).

## $A\otimes A^{op}$-rings

The structure of an $A\otimes A^{op}$-ring $(R,\mu,\eta)$ is determined by
the structure of $A$ as a ring, together with the two natural homomorphisms
of rings
$s = \eta(-\otimes 1_A):A\to R$ and $t=\eta(1_A\otimes -):A^{op}\to R$ which have commuting images ($s(a)t(a')=t(a')s(a)$, for all $a,a'\in A$). In theory of [[associative bialgebroid]]s these are the dual versions of the source and target maps from the study of [[groupoid]]s.

There is (not always associative) product of $A$-rings, and especially useful in the study of $A\otimes A^{op}$-rings, given by certain [[coend]], so called [[Takeuchi product]].


## Literature

* [[Mitsuhiro Takeuchi]], _Groups of algebras over $A \times \bar{A}$, J. Math. Soc. Japan __29__, 459--492, 1977, [MR0506407](https://www.ams.org/mathscinet-getitem?mr=0506407), [euclid](http://projecteuclid.org/euclid.jmsj/1240432948)

An introduction to $A$-rings and $A\otimes A^{op}$-rings is at the beginning of survey

* [[Gabriella Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_{R}$-bialgebras and duality_, J. Algebra 251: 279-294, 2002, [math.QA/0012164](http://arxiv.org/abs/math/0012164)
* P. Schauenburg, _Bialgebras over noncommutative rings and a structure theorem for Hopf bimodules_, Appl. Categ. Structures __6__ (1998), 193&#8211;222, [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/bnrsthb.ps) [doi](http://dx.doi.org/10.1023/A:1008608028634)
