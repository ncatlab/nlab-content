<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

In [[supergeometry]] the idea is to define everything in sight in terms of the algebras of local coordinate functions. (One really proceeds precisely as physicists do and always did, only difference being that before doing so one spends a minute to wonder about what doing so really means.) This means that the deRham complex of differential forms on a [[supermanifold]] is defined in the obvious way:

let $C^\infty(U)$ be the algebra of functions on patch $U$ of your supermanifold. Then the corresponding deRham complex over $U$ is the [[Lie infinity-algebroid|qDGCA]] which as a free graded-commutative algebra is generated over $C^\infty(U)$ by $C^\infty(U)[1]$. 

+-- {: .query}
I think the notation $C^\infty(U)[1]$ is very unusual here. If we have a complex or graded space then $C[1]$ is the complex or space with degree shifted by 1. In this case $C^\infty(U)[1]$ not something that differs from $C^\infty(U)$ just by a degree shift, it is a module over $C^\infty(U)$ of rank p|q if we are dealing with a supermanifold of dimension p|q. Instead of $C^\infty(U)[1]$
I would suggest just using $\Omega_1(U)$.
=--


This means that for each element $f \in C^\infty(U)$ we add a new element denoted $d f \in C^\infty(U)[1]$ which we take to be "shifted in degree by 1" with respect to $f$. If we are just in the usual $\mathbb{Z}_2$-graded context of supermanifolds, this just means that $d f$ is of odd or even grade if $f$ is of even or odd grade, respective.

On the free graded-commutative algebra $\Omega^\bullet(U) := \wedge^\bullet_{C^\infty(U)} C^\infty(U) = S^\bullet_{C^\infty(U)} C^\infty(U)[1]$ obtained this way we naturally obtain an odd degree algebra derivation 
$$
  d : \Omega^\bullet(U) \to \Omega^\bullet(U)
$$
by taking it on generators $f \in C^\infty(U)$ to be given by
$
  d : f \mapsto d f
$, 
naturally, and extended that as an odd graded derivation to all of $\Omega^\bullet(U)$. This defines the qDGCA $(\Omega^\bullet(U), d)$. This construction glues on intersections of different patches $U_1$, $U_2$ and hence defines a qDGCA $(\Omega^\bullet(X),d)$, the **de Rham complex of the supermanifold $X$**.

#Definition#

For $\mathbf{X}$ a supermanifold, the [[Lie infinity-algebroid|qDGCA]] $\Omega^\bullet(X)$ of differential forms on $X$ is the [[Weil algebra]] of $\mathbf{X}$.

#Remarks#

* Being a $\mathbb{Z}_2$-graded locally free algebra itself, one can regard $\Omega^\bullet(X)$ itself (even for $X$ a usual manifold!) as the "algebra of functions" (more precisely inner hom, i.e. mapping space into the line) on another supermanifold. That supermanifold is called $T[1] X$, the **shifted tangent bundle** of $X$. By definition we have $C^\infty(T[1]X) = \Omega^\bullet(X)$. From this point of view, the existence of the differential $d$ on the graded algebra $\Omega^\bullet(X)$ translates into the existence of a special odd vector field on $T[1]X$. This is a **homological vector field** in that it is odd and the super Lie bracket of it with itself vanishes: $[d,d] = 0$.

* In the context of [[NQ-supermanifolds]], where one may regard $C^\infty(X)$ as the Chevalley-Eilenberg algebra of an $L_\infty$-[[Lie infinity-algebroid|algebroid]] it is useful to notice that $\Omega^\bullet(X)$ is the corresponding [[Weil algebra]]. If $X$ is a Lie $n$-algebroid then $T[1]X$ is a Lie $(n+1)$-algebroid.


[[!redirects differential forms on supermanifolds]]
[[!redirects super differential form]]