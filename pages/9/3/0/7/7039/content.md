
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


# Analytic functions
* table of contents
{: toc}

## Idea

An _analytic function_ is a [[function]] that is locally given by a converging [[power series]].


## Definitions

Let $V$ and $W$ be [[complete space|complete Hausdorff]] [[topological vector spaces]], let $W$ be [[locally convex space|locally convex]], let $c$ be an [[element]] of $V$, and let $(a_0,a_1,a_2,\ldots)$ be an [[infinite sequence]] of [[homogeneous operator]]s from $V$ to $W$ with each $a_k$ of degree $k$.

Given an element $c$ of $V$, consider the [[infinite series]]

$$ 
  \sum_k a_k(x - c)
$$

(a [[power series]]).  Let $U$ be the [[interior]] of the set of $x$ such that this series converges in $W$; we call $U$ the __domain of convergence__ of the power series.  This series defines a [[function]] from $U$ to $W$; we are really interested in the case where $U$ is [[inhabited set|inhabited]], in which case it is a [[balanced neighbourhood]] of $c$ in $V$ (which is Proposition 5.3 of [Bochnak--Siciak](#BS)).

Let $D$ be any [[subset]] of $V$ and $f$ any [[continuous function]] from $D$ to $W$.  This function $f$ is __analytic__ if, for every $c \in D$, there is a power series as above with inhabited domain of convergence $U$ such that
$$ f(x) = \sum_k a_k(x - c) $$
for every $x$ in both $D$ and $U$.  (That $f$ is continuous follows automatically in many cases, including of course the finite-dimensional case.)


## Generalisation

The vector spaces $V$ and $W$ may be generalised to [[analytic manifold]]s and (more generally) [[analytic space]]s. However, these are [[manifolds]] and [[varieties]] modelled on vector spaces using analytic [[transition functions]], so the notion of an analytic function between vector spaces is the most fundamental.


## Complex-analytic functions of one variable

If $W$ is a vector space over the [[complex numbers]], then we have this very nice theorem, due essentially to [[Édouard Goursat]]:

+-- {: .un_theorem}
###### Theorem
A function from $D \subseteq \mathbb{C}$ to $W$ is [[differentiable function|differentiable]] if and only if it is analytic.
=--

(Differentiability here is in the usual sense, that the difference quotient converges in $W$.)  See [[holomorphic function]] and [[Goursat theorem]].


## Related concepts

* [[analytic geometry]]

* [[holomorphic function]], [[meromorphic function]]

* [[smooth function]]

* [[analytic (∞,1)-functor]]

* [[Fabius function]]

* [[HoTT book real numbers]]

## References

The theory of analytic function was constructed to some extent by

* M. Krasner (1940)

and in full generality by

* [[John Tate]] (1961)

Textbook accounts:

* {#GunningRossi} [[Robert C. Gunning]], [[Hugo Rossi]], *Analytic functions of several complex variables*, Prentice-Hall Inc., Englewood Cliffs (1965)

* {#BS} Jacek Bochnak and J&#243;zef Siciak, _Analytic functions in topological vector spaces_; Studia Mathematica 39 (1971);  ([pdf](http://matwbn.icm.edu.pl/ksiazki/sm/sm39/sm3916.pdf)).
 

* {#Schanuel} [[Stephen Schanuel]], _Continuous extrapolation to triangular matrices characterizes smooth functions_, J. Pure App. Alg. 24, Issue 1 (1982), 59&#8211;71. [web](http://www.sciencedirect.com/science/journal/00224049/24/1)

[[!redirects analytic function]]
[[!redirects analytic functions]]
[[!redirects analytic map]]
[[!redirects analytic maps]]
[[!redirects complex analytic]]