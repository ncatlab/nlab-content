## Definition ##

A $*$-autonomous category \[1\] is a [[symmetric monoidal
category|symmetric]] [[closed monoidal category]] $\langle
C,\otimes, I\rangle$ with a _dualizing object_: an object
$\bot$ such that the canonical morphism

$$d_A:\A\to(A\multimap\bot)\multimap\bot$$

which is the transpose of the evaluation map
$ev_{A,\bot}:(A\multimap\bot)\otimes A\to \bot$, is an
isomorphism for all $A$.

Define a functor $(-)^*=(-)\multimap\bot$.  The map $d_A$
is natural in $A$, so that there is a natural isomorphism
$d:1\Rightarrow(-)^{**}$.  We also have

$$\begin{aligned}
\hom(A\otimes B,C^*)& =\hom(A\otimes B, C\multimap\bot) \\
& \cong\hom((A\otimes B)\otimes C,\bot) \\
& \cong\hom(A\otimes(B\otimes C), \bot) \\
& \cong\hom(A,(B\otimes C)\multimap\bot) \\
&=\hom(A,(B\otimes C)^*)
\end{aligned}$$

The functor $(-)^*$, together with these two isomorphisms,
can be taken as an alternative definition of a
$*$-autonomous category.  The dualizing object $\bot$ is then defined as $I^*$.

## Examples ##

The standard example of a $*$-autonomous category is the category of finite-dimensional [[vector space]]s over some field $k$.  In this case $k$ itself plays the role of the dualizing object, so that for an f.d. vector space $V$, $V^*$ is the usual dual space of linear maps into $k$.

More generally, any [[compact closed category]] is $*$-autonomous with the unit $I$ as the dualizing object.

+--{: .query}
[[Mike Shulman|Mike]]: Can someone fill in some examples of $*$-autonomous categories that are not compact closed?
=--

Models of [[linear logic]] are based on $*$-autonomous
categories.


## References ##

1. Barr, Michael, _$*$-Autonomous Categories_. LNM 752,
   Springer-Verlag 1979.
