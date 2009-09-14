# Idea #

The _Landweber exactness criterion_ determins if a given [[formal group law]] does arise as the formal group law defined by a [[weakly periodic cohomology theory]].

Notice that since every [[formal group law]] over a [[ring]] $R$ is classified by a ring homomorphism $f : MP({*}) \to R$ where $MP({*})$ is the [[Lazard ring]]. So for every formal group one obtains a contravariant [[functor]] on [[topological space]]s given by the assignment

$$
  X \mapsto A_f^n(X) := MP^n(X) \otimes_{MP({*})} R
  \,,
$$

where $MP^\bullet$ denotes the [[complex cobordism cohomology theory]] and where the tensor product is taken using the $R$-module structure on $MP({*})$ induced by $f$.

The point of Lazard-exactness is that if $f$ is Lazard exact (i.e. if the corresponding formal group law is) then this construciton defines a [[cohomology theory]] $A^\bullet(-)$.
 

#Definition#

**Landweber criterion**  Let $f(x,y)$ be a [[formal group law]] and $p$ a prime,
$v_i$ the coefficient of $x^{p^i}$ in $[p]_f(x)=x+_f\cdots+_fx$.
If $v_0,\ldots,v_i$ form a regular sequence for all $p$ and $i$ then $f(x,y)$ is Lazard exact and hence gives a 
[[cohomology theory]] via the the formula above.

**Example.**  $g_a(x,y)=x+y$, $[p]_a(x)=px$, $v_0=p$, $v_i=0$ for all $i\ge1$;
regularity condtions imply that
the zero map $R/(p)\to R/(p)$ must be injective.  The last statement implies that
$R$ contains the rational numbers as a subring.

Note that $HP^*(X,R)=\prod_k H^{n+2k}(X,R)$ is a [[cohomology theory]] over any [[ring]] $R$.

**Example.**  $g_m(x,y)=xy$, $[p]_m(x)=(x+1)^p-1$, $v_0=p$, $v_1=1$, $v_i=0$ for all $i \gt 1$.
The regularity conditions are trivial.
Hence we know that $K^*(X)=MP^*(X)\otimes_{MP(\bullet)} \mathbb{Z}$ is a cohomology theory.


#related entries#

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]


[[!redirects Landweber exactness criterion]]
[[!redirects Landweber criterion]]

---
&lt;http://mathoverflow.net/questions/97682/a-homotopyish-landweber-exact-functor-theorem>

&lt;http://ncatlab.org/nlab/show/Landweber+exactness>

nLab page on [[nlab:Landweber exactness]]
