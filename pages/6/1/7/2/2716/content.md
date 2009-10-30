
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

An _$n$-symplectic manifold_ is to an ordinary [[symplectic manifold]] as an [[L-infinity algebroid|Lie n-algebroid]] is to an ordinary [[manifold]].

#Definition#

Traditionally, $n$-symplectic manifolds are thought of as [[supermanifold]]s with extra structure. More particularly, as [[NQ-supermanifold]]s with extra structure. 

One can argue that a more conceptual way to talk about them is in terms of [[Lie ∞-algebroid]]s. Technically it means precisely the same thing, but amplifying the [[Lie theory]] context should be helpful.

## in supermanifold language ##

An $n$-symplectic manifold is a [[NQ-supermanifold]] $X$ with an  $\mathbb{N}$-graded symplectic form $\omega$ of grading-degree $n$ 

$$
  \omega : (C(X)\wedge C(X))^\bullet \to C(X)^{\bullet -n}
  \,.
$$

So $\omega$ is a closed nondegenerate [[super differential form]] that respects the $\mathbb{N}$-refined grading of the underlying $\mathbb{Z}_2$-garded [[supermanifold]] as indicated.

## in $\infty$-Lie algebroid language ##

An $n$-symplectic manifold is a [[Lie ∞-algebroid]] $\mathcal{a}$ equipped with a choice of binary degree $(n+2)$ invariant polynomial $\omega \in inv(\mathcal{a})$.



#Examples#

## $n=0$: symplectic manifold ## 

A $0$-symplectic manifold is an ordinary [[symplectic manifold]].


## $n=1$: Poisson manifold ## 

A $1$-symplectic manifold is an ordinary [[Poisson manifold]].



## $n=2$: Courant algebroid ## 

A $2$-symplectic manifold is a [[Courant algebroid]].

Consider first a 2-symplectic point. This is a [[semifree dga]] generated on some graded vector space $V$ and equipped with a _symmetric_ non-degenerate bilinear form on $V_1$. (An odd-graded skew form is a symmetric form!).

This is essentially the [[String Lie 2-algebra]].

#References#

The notion originates somewhere in the school of [[Alan Weinstein]]'s school of [[higher category theory|higher categorial]] [[symplectic geometry]]. The first published appearance of the notion at least for $0 \leq n \leq 3$ is

* [[Dmitry Roytenberg]], _Couran algebroids, derived brackets and even symplectic supermanifolds_ PhD thesis ([arXiv](http://arxiv.org/abs/math/9910078))

The idea for all $n$ was then sketched, together with many other ideas about [[L-infinity algebroid]]s in the article with the nice title

* [[Pavol Severa]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math/0105080))

What we call $n$-symplectic manifold here is called $\Sigma_n$-manifold there.

> [[Urs Schreiber]]: I find $\Sigma_n$ too undescriptive. But logically I should then be speaking of _$n$-Poisson manifolds_ so that for $n=1$ we get the ordinary version, not for $n=0$. But I find _symplectic_ still much nicer descriptive than "Poisson", so the above choice of terminology follows aesthetics a little bit more than established terminology. But only slightly. Only by a difference of 1.

> _Toby_:  What if you changed the numbering by $1$?  Must your $n$ match the $n$ in $\Sigma_n$?