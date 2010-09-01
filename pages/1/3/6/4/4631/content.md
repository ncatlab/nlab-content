
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

# Augmented simplicial sets
* table of contents
{: toc}

## Idea

An _augmented simplicial set_ $X$ is a [[presheaf]] on the augmented [[simplex category]] $\Delta_+$,

$$
  X : \Delta^{op}_+ \to Set
  \,.
$$

So its [[restriction]] along $\Delta \hookrightarrow \Delta_+$ is an ordinary [[simplicial set]].

This can also be described as a simplicial set $X$ with a map (a [[natural transformation]]) to a [[constant functor|constant]] simplicial set $X_{-1}$; we say that the simplicial set is _augmented_ over $X_{-1}$.


## Definitions

Explicitly, an __augmented simplicial set__ consists of

*  for each [[integer]] $n \geq -1$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_{-1},X_0,X_1,X_2,\ldots)$ of sets),
*  for each integer $n \geq -1$ and each [[natural number]] $m \leq n$, a __face map__ $s^n_m\colon X_n \to X_{n-1}$,
*  for each integer $n \geq -1$ and each natural number $m \leq n$, a __degeneracy map__ $d^n_m\colon X_n \to X_{n+1}$,
*  satisfying the [[simplicial identities]].

Above, we use the traditional system of numbering for a [[simplicial set]].  However, part of the motivation behind augmented simplicial sets is that this is a more sensible numbering system:

*  for each [[natural number]] $n$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_0,X_1,X_2,\ldots)$ of sets),
*  for each natural number $n$ and each natural number $m \leq n$, a __face map__ $s^n_m\colon X_{n+1} \to X_n$,
*  for each natural number $n$ and each natural number $m \lt n$, a __degeneracy map__ $d^n_m\colon X_n \to X_{n+1}$,
*  satisfying the [[simplicial identities]].

While this numbering is very nice for augmented simplicial sets, it is not standard and is can be easily misunderstood, so we don\'t use it in this article.


## Properties

Anything that applies to [[simplicial sets]] should also apply to augmented simplicial sets, if one properly takes care of the [[negative thinking]] necessary to deal with $X_{-1}$.

Every augmented simplicial set has an underlying unaugmented simplicial set found by forgetting the bottom level.  Conversely, every unaugmented simplicial set gives rise to a [[free object|free]] augmented simplicial set by augmentation over $\pi_0(X_0)$ (the set of [[connected component]]s of $X_0$) and a [[cofree object|cofree]] augmented simplicial set by augmentation over the [[point]] (the [[singleton set]]).  This defines [[adjunctions]]:

![\xymatrix{\operatorname{Aug}\operatorname{Simp}\operatorname{Set}\ar[d]^{\vdash}_{\vdash}\\\operatorname{Simp}\operatorname{Set}\ar@/^1pc/[u]\ar@/_1pc/[u]}](http://latex.codecogs.com/gif.latex?\xymatrix{\operatorname{Aug}\operatorname{Simp}\operatorname{Set}\ar[d]^{\vdash}_{\vdash}\\\operatorname{Simp}\operatorname{Set}\ar@/^1pc/[u]\ar@/_1pc/[u]})


[[!redirects augmented simplicial set]]
[[!redirects augmented simplicial sets]]
