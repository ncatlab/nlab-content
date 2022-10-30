
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea 


The notion of _$\Theta_n$-space_ is one model for the notion of _[[(∞,n)-category]]_. A $\Theta_n$-space may be thought of as a [[globe category|globular]] $n$-category _up to coherent homotopy_, a globular $n$-category _[[internalization|internal]]_ to the [[(∞,1)-category]] [[∞Grpd]].

Concretely, a _$\Theta_n$-space is a [[simplicial presheaf]] on the [[Theta category|Theta_n category]], hence a "[[cellular object|cellular space]]" that satisfies 

1. the globular [[Segal condition]] as a [[weak homotopy equivalence]];

1. and a completeness condition analogous to that of [[complete Segal spaces]]. 

In fact for $n = 1$ $\Theta_n = \Delta$ is the simplex category and a $\Theta_1$-space is the same as a [[complete Segal space]]. 

Noticing that a presheaf of _sets_ on $\Theta_n$ which satisfies the cellular [[Segal condition]] is equivalently a [[strict n-category]], $Theta_n$-spaces may be thought of as [[n-categories]] [[internal category in an (infinity,1)-category|internal to]] the [[(∞,1)-category]] [[∞Grpd]], defined in the [[cell category|cellular]] way.


## Overview 

There is a [[cartesian closed category|cartesian closed]] [[category with weak equivalences]] $\Theta_n Sp_k^{fib}$ of **$(n+k,n)$-$\Theta$-spaces** for all 

* $0 \leq n \leq \infty$;

* $-2 \leq k \leq \infty$

as the [[category of fibrant objects]] in a [[model category]] $\Theta_n Sp_k$,  
being a [[Bousfield localization of model categories|left Bousfield localization]] of the injective [[model structure on simplicial presheaves]] on the $n$th [[Theta category]].

The [[weak equivalences]] in $\Theta_n Sp_k^{fib}$ are then (by the standard result discussed at [[Bousfield localization of model categories]]) just the objectwise weak equivalences in the standard [[model structure on simplicial sets]] $sSet_{Quillen}$.

## Definition 

For $J$ a [[category]], write $\Theta J$ for the [[categorical wreath product]] over the [[simplex category]] $\Delta$ [Ber05](http://arxiv.org/abs/math/0512575).

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



## Properties 

### Special values of $(n,k)$

+-- {: .query}
  I would have started $k$ at $-1$.  What does Rezk\'s notion do with $k = -2$?  ---Toby

  $-1$-groupoids are spaces which are either empty or contractible.  $-2$-groupoids are spaces which are contractible.  So $k=-2$ is the completely trivial case; it's included for completeness.  -- Charles

  I do know what a $(-2,0)$-category is, a triviality as you say.  But for $n \gt 0$, an $(n-2,n)$-category is the same as an $(n-2,n-1)$-category as far as I can see.  (Note: I say this *without* having worked through your version, but just thinking about what $(n,r)$-categories should be, as at [[(n,r)-category]].)  ---Toby

  I would say: $(n-2,n)$-category is a trivial concept, for every $n$, though $(n-2,n-1)$ isn't.  An $(n+1+k,n+1)$-category should amount to a category enriched over $(n+k,n)$-categories.  An $(-2,0)$-category is trivial (a point); an $(-1,1)$-category is a category enriched over the point, and so equivalent to the terminal category; an $(0,2)$-category is a category enriched over categories which are equivalent to the terminal category (and so equivalent to the terminal $2$-category, etc.) -- Charles R.

  <del>H\'m, that is a good argument.</del>

  (Sorry for not noticing before that you *are* Charles Rezk; for some reason I though of [[Charles Wells]].)  ---Toby

  [[David Roberts]]: I'm a little confused. The way I think about it, and I may have the indexing wrong, is that in an $(n,n+2)$-category $C$, for _all_ pairs of $n$-arrows $x,y$, there is a unique $n+1$-arrow between them. This implies that $x$ and $y$ are parallel, in particular, that $C$ has a single $(n-1)$-arrow. 

  _Toby_:  Wait, I don\'t buy Charles\'s argument after all.  Yes, a $(-1,1)$-category is a category enriched over the point, but that doesn\'t make it necessarily the terminal category; it makes it a truth value.  If it has an object, then it\'s trivial, but it might be empty instead.  The difference between a $(-1,1)$-category and a $(-1,0)$-category is that every $0$-morphism in the latter must be invertible, which is no difference at all; that\'s why we have this repetition.  (And thereafter it propagates indefinitely.)

  Similarly, with David\'s argument, what if $C$ has no $n$-arrows at all?

  [[David Roberts]]: Yes - that should then be \'Assuming $C$ has an object, then it has a single $(n-1)$-arrow\'. Assuming I got the indexing right, I must stress. I think I grasp $(n,n+1)$-categories, but I'm not solid on these new beasties.

  Toby, I guess you are right.  I don't know what I was thinking.  -- Charles R.

  Thanks for joining, in, Charles. Toby is, by the way, our esteemed expert for -- if not the inventor of -- [[negative thinking]]. :-) - [[Urs Schreiber|USc]]

  _Toby_:  All right, so we allow $k = -2$, since $n$ might be $0$; but for an $(n-2,n)$-$\Theta$-space is the same as an $(n-1,n)$-$\Theta$-space for $n \gt 0$.  OK, I\'m happy with that; now to understand the definition!  (^_^)
  =--

### Cartesian monoidal and enriched structure 

The [[model category]] $\Theta_n Sp_k$ is a [[cartesian monoidal category|cartesian]] [[monoidal model category]].

The idea is that $\Theta_n Sp_k$ is naturally an [[enriched model category]] over itself.

### $(n+1,r+1)$-$\Theta$-space of $(n,r)$-$\Theta$-spaces 
 {#OfAll}

Here is the idea on how to implement the notion $(n+1,r+1)$-category of all $(n,r)$-categories in the context of Theta-spaces. At the time of this writing, this hasn't been spelled out in total.

As mentioned above regard $\Theta_k Sp_n$ as a category enriched over itself. Then define a presheaf $\mathbf{X}$ on $\Theta_{n+1}$ by setting

* $\mathbf{X}[0] = $ collection of objects of $\Theta_n Sp_k$

* $\mathbf{X}([m](\theta_1, \cdots, \theta_m))
   = \coprod_{a_0, \cdots, a_m}
     C(a_0,a_1)(\theta_1) \times \cdots \times
     C(a_{m-1},a_m)(\theta_m)
  $

This object satisfies the [[Segal conditions]] (its descent conditions) in all degrees except degree 0. A suitable localization operation ca-n fix this. The resulting object should be the "$(n+1,k+1)$-$\Theta$-space of $(n,k)$-$\Theta$-spaces".

### Homotopy hypothesis 

The definition of weak $(n,r)$-categories modeled by $\Theta$-spaces does satisfy the [[homotopy hypothesis]]: there is an evident notion of groupoid objects in $\Theta_n Sp_k$ and the full subcategory on these models [[homotopy n-types]].

([Rez09, 11.25](#Rezk)).

### Relation to cellular sets

There is a [[model structure on cellular sets]] (see there), hence on set-valued presheaves on $\Theta_n$ (instead of simplicial presheaves) which  is [[Quillen equivalence|Quillen equivalent]] to the Rezk model structure on $\Theta_n$-spaces.

In factm the Theta-space model structure is the [simplicial completion](Cisinski+model+structure#SimplicialCompletion) of the [[Cisinski model structure]] on presheaves on $\Theta_n$ ([Ara](#Ara))


## Examples

For low values of $n,k$ this reproduces the following cases:

* for $n=0$ we have $\Theta_0 Sp_\infty = sSet_{Quillen}$ with its [[model structure on simplicial sets|standard model structure]] and hence $\Theta_0 Sp_\infty^{fib} = $ [[∞Grpd]].

* for $n=1$ objects in $\Theta_1 Sp_\infty^{fib} $ are [[complete Segal spaces]], hence [[(∞,1)-category|(∞,1)-categories]].

## Related concepts

* [[cellular set]]

* [[omega-category]]

* [[globular operad]], [[globular theory]], 

## References 

The notion of $\Theta$-spaces was introduced in

* [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_ Geom. Topol. 14 (2010), no. 1, 521&#8211;571 ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602))

  _Correction to "A cartesian presentation of weak $n$-categories"_ Geom. Topol. 14 (2010), no. 4, 2301&#8211;2304. MR 2740648 ([pdf](http://www.math.uiuc.edu/~rezk/cs-objects-correction.pdf))
 {#Rezk}


* [[Charles Rezk]], _Cartesian presentations of weak n-categories
An introduction to $\Theta_n$-spaces_ (2009) ([pdf](http://www.math.uiuc.edu/~rezk/northwestern-2009-n-cat-handout.pdf))
 

The definition of the categories $\Theta_n$ goes back to [[Andre Joyal]] who also intended to define [[n-category|n-categories]] using it.

Discussion comparing $\Theta_{n+1}$-spaces to [[enriched (infinity,1)-categories]] in $\Theta_n$-spaces is in 


* {#BergnerRezk} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories_ ([arXiv:1204.2013](http://arxiv.org/abs/1204.2013))
 
* {#BergnerRezk14} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories II_ ([arXiv:1406.4182](http://arxiv.org/abs/1406.4182))


The note on the $(n+1,k+1)$-$\Theta$-space of all $(n,k)$-$\Theta$-spaces comes from communication with [[Charles Rezk]] [here](http://mathoverflow.net/questions/5867/n1-r1-theta-space-of-n-r-theta-spaces).

Relation to simplicial completion of the [[Cisinski model structure]] [[model structure on cellular sets|on cellular sets]] is in 

* [[Dimitri Ara]], _Higher quasi-categories vs higher Rezk spaces_ ([arXiv:1206.4354](http://arxiv.org/abs/1206.4354))
 {#Ara}



[[!redirects theta space]]
[[!redirects theta-space]]
[[!redirects theta spaces]]
[[!redirects theta-spaces]]

[[!redirects Theta space]]
[[!redirects Theta-Space]]
[[!redirects ? Space]]
[[!redirects ∞-Space]]
[[!redirects ? space]]
[[!redirects ∞-space]]

[[!redirects Theta spaces]]
[[!redirects Theta-Spaces]]
[[!redirects Theta-spaces]]
[[!redirects ? Spaces]]
[[!redirects ∞-Spaces]]
[[!redirects ? spaces]]
[[!redirects ∞-spaces]]

[[!redirects Theta_n space]]
[[!redirects Theta_n spaces]]

