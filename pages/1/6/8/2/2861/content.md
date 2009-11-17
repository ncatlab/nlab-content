<div class="rightHandSide toc">
[[!include higher category theory - contents]]
***
[[!include model category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

[[Charles Rezk]] has proposd a notion of weak [[(n,r)-category|(n+k,n)-category]], which he calls **$(n+k,n)$-Theta-spaces** . The $(n+k,n)$-$\Theta$-spaces are precisely the fibrant objects of a certain [[model category]] structure on the category of [[simplicial presheaf|presheaves of simplicial sets]] on [[Andre Joyal|Joyal]]'s [[disk category]] $\Theta_n$. This notion is a generalization of that of [[complete Segal spaces]] (which are precisely the $(\infty,1)$-$\Theta$-spaces). 

## Overview ##

There is a [[cartesian closed category|cartesian closed]] [[category with weak equivalences]] $\Theta_n Sp_k^{fib}$ of **$(n+k,n)$-$\Theta$-spaces** for all 

* $0 \leq n \leq \infty$;

* $-2 \leq k \leq \infty$
  +-- {: .query}
  I would have started $k$ at $-1$.  What does Rezk\'s notion do with $k = -2$?  ---Toby
  =--

as the [[category of fibrant objects]] in a [[model category]] $\Theta_n Sp_k$. The underlying [[category]] of this is the category $SPSh(\Theta_n)$ on a certain category $\Theta_n$, equipped with a model structure obtained as a left [[Bousfield localization]] of the global injective [[model structure on simplicial presheaves]].

The weak equivalences in $\Theta_n Sp_k^{fib}$ are then (by the standard result discussed at [[Bousfield localization]]) just the objectwise weak equivalences in [[SSet]].

For low values of $n,k$ this reproduces the following cases:

* for $n=0$ we have $\Theta_0 Sp_\infty = SSet$ with its [[model structure on simplicial sets|standard model structure]] and hence $\Theta_0 Sp_\infty^{fib} = $ [[∞Grpd]].

* for $n=1$ objects in $\Theta_1 Sp_\infty^{fib} $ are [[complete Segal spaces]], hence [[(∞,1)-category|(∞,1)-categories]].

## Definition ##

...

## Properties ##

### Homotopy hypothesis ###

The definition of weak $(n,r)$-categories modeled by $\Theta$-spaces does satisfy the [[homotopy hypothesis]]: there is an evident notion og groupoid objects in $\Theta_n Sp_k$ and the full subcategory on these models [[homotopy n-types]].

See [Rez09, 11.25](http://arxiv.org/PS_cache/arxiv/pdf/0901/0901.3602v2.pdf#page=35).

## References ##

The theory of $\Theta$-spaces has been proposed in

* [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_ ([arXiv](http://arxiv.org/abs/0901.3602))


The definition of the categories $\Theta_n$ goes back to [[Andre Joyal]] who also intended to define [[n-category|n-categories]] using it.

[[!redirects Theta-Space]]
[[!redirects ? Space]]
[[!redirects ∞-Space]]
[[!redirects Theta spaces]]
[[!redirects Theta-Spaces]]
[[!redirects ? Spaces]]
[[!redirects ∞-Spaces]]