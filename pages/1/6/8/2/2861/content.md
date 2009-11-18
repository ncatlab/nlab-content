<div class="rightHandSide toc">
[[!include higher category theory - contents]]
***
[[!include model category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##


$(n+k,n)$-$\Theta$-spaces are a model for the notion of (weak) [[(n,r)-category|(n+k,n)-category]] proposed by
[[Charles Rezk]].

The $(n+k,n)$-$\Theta$-spaces are, roughly, presented as the fibrant objects of a certain [[model category]] structure on the category of [[simplicial presheaf|presheaves of simplicial sets]] on [[Andre Joyal|Joyal]]'s [[disk category]] $\Theta_n$. This notion is a generalization of that of [[complete Segal spaces]] (which are precisely the $(\infty,1)$-$\Theta$-spaces). 

## Overview ##

There is a [[cartesian closed category|cartesian closed]] [[category with weak equivalences]] $\Theta_n Sp_k^{fib}$ of **$(n+k,n)$-$\Theta$-spaces** for all 

* $0 \leq n \leq \infty$;

* $-2 \leq k \leq \infty$
  +-- {: .query}
  I would have started $k$ at $-1$.  What does Rezk\'s notion do with $k = -2$?  ---Toby

  $-1$-groupoids are spaces which are either empty or contractible.  $-2$-groupoids are spaces which are contractible.  So $k=-2$ is the completely trivial case; it's included for completeness.  -- Charles

  I do know what a $(-2,0)$-category is, a triviality as you say.  But for $n \gt 0$, an $(n-2,n)$-category is the same as an $(n-2,n-1)$-category as far as I can see.  (Note: I say this *without* having worked through your version, but just thinking about what $(n,r)$-categories should be, as at [[(n,r)-category]].)  ---Toby

  I would say: $(n-2,n)$-category is a trivial concept, for every $n$, though $(n-2,n-1)$ isn't.  An $(n+1+k,n+1)$-category should amount to a category enriched over $(n+k,n)$-categories.  An $(-2,0)$-category is trivial (a point); an $(-1,1)$-category is a category enriched over the point, and so equivalent to the terminal category; an $(0,2$-category is a category enriched over categories which are equivalent to the terminal category (and so equivalent to the terminal $2$-category, etc.) -- Charles R.

  H\'m, that is a good argument.  (Sorry for not noticing before that you *are* Charles Rezk; for some reason I though of [[Charles Wells]].)  ---Toby
  =--

as the [[category of fibrant objects]] in a [[model category]] $\Theta_n Sp_k$. The underlying [[category]] of this is the category $SPSh(\Theta_n)$ on a certain category $\Theta_n$, equipped with a model structure obtained as a left [[Bousfield localization]] of the global injective [[model structure on simplicial presheaves]].

The weak equivalences in $\Theta_n Sp_k^{fib}$ are then (by the standard result discussed at [[Bousfield localization]]) just the objectwise weak equivalences in [[SSet]].

For low values of $n,k$ this reproduces the following cases:

* for $n=0$ we have $\Theta_0 Sp_\infty = SSet$ with its [[model structure on simplicial sets|standard model structure]] and hence $\Theta_0 Sp_\infty^{fib} = $ [[∞Grpd]].

* for $n=1$ objects in $\Theta_1 Sp_\infty^{fib} $ are [[complete Segal spaces]], hence [[(∞,1)-category|(∞,1)-categories]].

## Definition ##

For $J$ a [[category]], write $\Theta J$ for the [[categorical wreath product]] over the [[simplex category]] $\Delta$ [Ber05](http://arxiv1.library.cornell.edu/abs/math/0512575).

Then with $\Theta_0 := {*}$ we have inductively

$$
  \Theta_n = \Theta \Theta_{n-1}
  \,.
$$

For $D = SPSh(C)^{inj}_{S}$ a [[model structure on simplicial presheaves]] on a category $C$ obtained by left [[Bousfield localization]] at a set of morphisms $S \subset Mor(SPSh(C)^{inj})$ from the global injective model structure, write

$$
  D-\Theta Sp := SPSh(\Theta C)^{inj}_{S_\Theta}
  \,,
$$

where $S_\Theta$ is the set of morphisms given by .... .


Set 

$$
  \Theta_0 Sp_k := SSet_k
  \,,
$$

the left [[Bousfield localization]] of the standard [[model structure on simplicial sets]] such that fibrant objects are the [[Kan complex]]es that are [[homotopy n-type|homotopy k-type]]s. Then finally define inductively

$$
  \Theta_{n+1} Sp_k := (\Theta_n Sp_k)-\Theta Sp
  \,.
$$

Unwinding this definition we see that 

$$
  \Theta_{n} Sp_k = SPSh(\Theta_n)^{inj}_{S_{n}}
  \,,
$$

for some set $S_n \subset Mor(SPSh(C))$ of morphisms.





## Properties ##

### Cartesian monoidal and enriched structure ###

The [[model category]] $\Theta_n Sp_k$ is a [[cartesian monoidal category|cartesian]] [[monoidal model category]].

The idea is that $\Theta_n Sp_k$ is naturally an [[enriched model category]] over itself.

### $(n+1,r+1)$-$\Theta$-space of $(n,r)$-$\Theta$-spaces ###

Here is the idea on how to implement the notion $(n+1,r+1)$-category of all $(n,r)$-categories in the context of Theta-spaces. At the time of this writing, this hasn't been spelled out in total.

As mentioned above regard $\Theta_k Sp_n$ as a category enriched over itself. Then define a presheaf $\mathbf{X}$ on $\Theta_{n+1}$ by setting

* $\mathbf{X}[0] = $ collection of objects of $\Theta_n Sp_k$

* $\mathbf{X}([m](\theta_1, \cdots, \theta_m))
   = \coprod_{a_0, \cdots, a_m}
     C(a_0,a_1)(\theta_1) \times \cdots \times
     C(a_{m-1},a_m)(\theta_m)
  $

This object satisfies the Segal conditions (its descent conditions) in all degrees except degree 0. A suitable localization operation ca-n fix this. The resulting object should be the "$(n+1,k+1)$-$\Theta$-space of $(n,k)$-$\Theta$-spaces".

### Homotopy hypothesis ###

The definition of weak $(n,r)$-categories modeled by $\Theta$-spaces does satisfy the [[homotopy hypothesis]]: there is an evident notion og groupoid objects in $\Theta_n Sp_k$ and the full subcategory on these models [[homotopy n-types]].

See [Rez09, 11.25](http://arxiv.org/PS_cache/arxiv/pdf/0901/0901.3602v2.pdf#page=35).

## References ##

The theory of $\Theta$-spaces has been proposed in

* [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_ ([arXiv](http://arxiv.org/abs/0901.3602))

The definition of the categories $\Theta_n$ goes back to [[Andre Joyal]] who also intended to define [[n-category|n-categories]] using it.

The note on the $(n+1,k+1)$-$\Theta$-space of all $(n,k)$-$\Theta$-spaces comes from communication with [[Charles Rezk]] [here](http://mathoverflow.net/questions/5867/n1-r1-theta-space-of-n-r-theta-spaces).


[[!redirects Theta-Space]]
[[!redirects ? Space]]
[[!redirects ∞-Space]]
[[!redirects Theta spaces]]
[[!redirects Theta-Spaces]]
[[!redirects ? Spaces]]
[[!redirects ∞-Spaces]]