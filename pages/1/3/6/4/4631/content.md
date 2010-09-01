
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

Where an ordinary [[simplicial set]] $X$ may be thought of a [[space]] made up of $n$-[[simplices]] $\sigma \in X_n$ for all $n \in \{0,1,2,3, \cdots \}$, an _augmented simplicial set_ in addition has a set $X_{-1}$ of "$(-1)$-simplices" such that each 0-simplex has a single $(-1)$-dimensional face and such that the two (-1)-dimensional faces of the two ends of any 1-simplex coincide.

Equivalently this may be thought of as the data that encodes a morphism $X \to const X_{-1}$ between ordinary simplicial sets from the underlying simplicial set to the simplicial set with $X_{-1}$ as its set of 0-simplices and otherwise only degenerate $k$-simplices for $k \geq 1$.

It is in this latter form that augmented simplicial sets maybe mostly arise in practice, whereas the former incarnation offers a more succinct way of thinking about them.

For instance a major source of augmented [[simplicial object]]s are given by [[colimit]]s or rather [[homotopy colimit]]s over simplicial diagrams in a [[model category]]: for $X : \Delta^{op}  \to C$ a simplicial object in a category with colimits, its [[colimit]] [[cocone]] may be thought of as a morphism 

$$
  X_\bullet \to const \lim_{\to} X_\bullet 
$$

into the constant simplicial object.


## Definitions

Denote by $\Delta_+$ the [[augmented simplex category]], which may be defined as the [[full subcategory]] of [[Cat]] on [[free categories]] over finite and _possibly empty_ linear [[directed graphs]], which are

* $[-1] := \emptyset$;

* $[0] := (0)$;

* $[1] := (0 \to 1)$;

* $[2] := (0 \to 1 \to 2)$;

* and so on.

An **augmented simplicial set** $X$ is a [[presheaf]] on $\Delta_+$ and the [[category]] of augmented simplicial sets is the presheaf category

$$
  sSet_+ := [\Delta_+^{op}, Set]
  \,.
$$


There is a canonical inclusion $\Delta \hookrightarrow \Delta_+$ of the ordinary [[simplex category]] and that the [[restriction]] of an augmented simplicial set along this inclusion is a simplicial set. This gives a [[forgetful functor]]

$$
  U : sSet_+ \to sSet
  \,.
$$

A cartoon of an augmented simplicial set, showing just the face maps, looks like

$$
  X_\bullet = 
  \left(
  \cdots
  X_2 \stackrel{\to}{\stackrel{\to}{\to}} X_1 \stackrel{\overset{d^0_1}{\to}}{\underset{d^0_0}{\to}} X_0 \stackrel{d^{-1}}{\to} X_{-1}
  \right)
$$

where the only new [[simplicial identity]] satisfied by the new face map in degree -1 is that it coequalizes the degree-0 face maps in that

$$
  d^{-1}\circ d^0_1 = d^{-1}\circ d^0_0
  \,.
$$

It follows that $d^{-1}$ coequalizes in fact every pair of composites of face maps $X_n \to X_{0}$, so that equivalently an augmented simplicial set $X_\bullet$ is a morphism of ordinary simplicial sets

$$
  U(X_\bullet) \to const X_{-1}
  \,.
$$

We say that that $U(X_\bullet)$ is _augmented_ over $X_{-1}$.

More explicitly, an __augmented simplicial set__ consists of

*  for each [[integer]] $n \geq -1$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_{-1},X_0,X_1,X_2,\ldots)$ of sets),
*  for each integer $n \geq -1$ and each [[natural number]] $m \leq n$, a __face map__ $d^n_m\colon X_n \to X_{n-1}$,
*  for each integer $n \geq -1$ and each natural number $m \leq n$, a __degeneracy map__ $s^n_m\colon X_n \to X_{n+1}$,
*  satisfying the [[simplicial identities]].

Above, we use the traditional system of numbering for a [[simplicial set]].  However, part of the motivation behind augmented simplicial sets is that this is a more sensible numbering system:

*  for each [[natural number]] $n$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_0,X_1,X_2,\ldots)$ of sets),
*  for each natural number $n$ and each natural number $m \leq n$, a __face map__ $d^n_m\colon X_{n+1} \to X_n$,
*  for each natural number $n$ and each natural number $m \lt n$, a __degeneracy map__ $s^n_m\colon X_n \to X_{n+1}$,
*  satisfying the [[simplicial identities]].

While this numbering is very nice for augmented simplicial sets, it is not standard and is can be easily misunderstood, so we don\'t use it in this article.


## Properties

Anything that applies to [[simplicial sets]] should also apply to augmented simplicial sets, if one properly takes care of the [[negative thinking]] necessary to deal with $X_{-1}$.

Every augmented simplicial set has an underlying unaugmented simplicial set found by forgetting the bottom level.  Conversely, every unaugmented simplicial set gives rise to a [[free object|free]] augmented simplicial set by augmentation over $\pi_0(X_0)$ (the set of [[connected component]]s of $X_0$) and a [[cofree object|cofree]] augmented simplicial set by augmentation over the [[point]] (the [[singleton set]]).  This defines [[adjunctions]]:

![\xymatrix{\operatorname{Aug}\operatorname{Simp}\operatorname{Set}\ar[d]^{\vdash}_{\vdash}\\\operatorname{Simp}\operatorname{Set}\ar@/^1pc/[u]\ar@/_1pc/[u]}](http://latex.codecogs.com/gif.latex?\xymatrix{\operatorname{Aug}\operatorname{Simp}\operatorname{Set}\ar[d]^{\vdash}_{\vdash}\\\operatorname{Simp}\operatorname{Set}\ar@/^1pc/[u]\ar@/_1pc/[u]})

## Examples

* For $C$ a [[site]], $\{U_i \to X\}$ a [[covering]] family we have the [[Cech nerve]] [[simplicial presheaf]] $C(U) \in [C^{op}, sSet]$. This comes canonically equipped with a morphism of simplicial presheaves to the one represented by $X$ : $C(U) \to X$. This is an augmented simplicial object in the category of presheaves $[C^{op}, Set]$. Morover, over each object $V \in C$ its component

  $$
    C(U)(V) \to X(V)
  $$

  is an augmented simplicial set.

  More generally this applies to [[hypercover]]s.


[[!redirects augmented simplicial set]]
[[!redirects augmented simplicial sets]]
