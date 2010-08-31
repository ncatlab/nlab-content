
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

An _augmented simplcial set_ $X$ is a [[presheaf]] on the augmented [[simplex category]] $\Delta_+$,

$$
  X : \Delta^{op}_+ \to Set
  \,.
$$

So its restriction along $\Delta \hookrightarrow \Delta_+$ is an ordinary [[simplicial set]].


## Definitions

Explicitly, an __augmented simplicial set__ consists of

*  for each [[integer]] $n \geq -1$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_{-1},X_0,X_1,X_2,\ldots)$ of sets),
*  for each integer $n \geq -1$ and each [[natural number]] $m \leq n$, a __face map__ ...,
*  for each integer $n \geq -1$ and each natural number $m \leq n$, a __degeneracy map__ ...,
*  satisfying the [[simplicial identities]].

Above, we use the traditional system of numbering for a [[simplicial set]].  However, part of the motivation behind augmented simplicial sets is that this is a more sensible numbering system:

*  for each [[natural number]] $n$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_0,X_1,X_2,\ldots)$ of sets),
*  for each natural number $n$ and each natural number $m \lt n$, a __face map__ ...
*  for each natural number $n$ and each natural number $m \lt n$, a __degeneracy map__ ...
*  satisfying the [[simplicial identities]].


## Properties

Anything that applies to [[simplicial sets]] should also apply to augmented simplicial sets, if one properly takes care of the [[negative thinking]] necessary to deal with $X_{-1}$ (which is $X_0$ in the more sensible numbering system).


[[!redirects augmented simplicial set]]
[[!redirects augmented simplicial sets]]
