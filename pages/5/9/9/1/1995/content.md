
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _differential bimodule_ over a [[ring]] $R$ is a [[bimodule]] that behaves like a collection of [[differential operator]]s $R \to R$.

## Definition

Given a [[commutative unital ring]] $R$, a [[filtration]] $M_n$ ($n\geq -1$) on a $R$-$R$-[[bimodule]] $M$ is a __differential filtration__ if the commutator $[r,P]$ for any $P$ in $M_n$ is in $M_{n-1}$, and $M_{-1} = 0$. A bimodule is __differential__ if it has an exhaustive ($\bigcup_n M_n = M$) differential filtration. Every $R$-$R$-bimodule has a __differential part__, i.e. the maximal differential submodule of $M$. The principal example of a differential bimodule is the ring of [[regular differential operators]] defined by [[Grothendieck]]. 

There is a generalization in categorical setup developed by Lunts and Rosenberg in

* V. Lunts, A. L. Rosenberg, _Differential calculus in noncommutative algebraic geometry I. D-calculus on noncommutative rings_

If a noncommutative [[scheme]]-like geometric object $X$ is represented by an [[abelian category]], $C_X$ then morphism of schemes should correspond to pairs of [[adjoint functors]], in fact bimodules (cf. the [[Eilenberg-Watts theorem]]). Then one considers thickenings of the diagonal ...

to continue... 

## Examples

Let $X$ be a [[smooth manifold]] and let $R = C^\infty(X)$ be the ring of smooth functions. Consider inside $End(R)$ all [[differential operator]]s, for instance 

* multiplication operators by elements in $R$;

* operators that take the differential with respect to a [[vector field]],

* etc. 

Then we have a D-filtration by _order_ of the differential operator. For instance the commutator of a vector field $v$ with a multiplication operator $a$ is $[v,a] = v(a)$, which is a multiplication operator. And since $R$ is commutative we have for $a,b$ two multiplication operators that $[a,b] = 0$.

