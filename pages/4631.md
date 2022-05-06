
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

Where an ordinary [[simplicial set]] $X$ may be thought of a [[space]] made up of $n$-[[simplices]] $\sigma \in X_n$ for all $n \in \{0,1,2,3, \cdots \}$, an _augmented simplicial set_ in addition has a set $X_{-1}$ of "$(-1)$-simplices" such that each 0-simplex has a single $(-1)$-dimensional face and such that the $(-1)$-dimensional faces of the two faces of any $1$-simplex coincide.

Equivalently this may be thought of as the data that encodes a [[morphism]] $X \to const X_{-1}$ in [[sSet]] between ordinary simplicial sets from an _underlying_ simplicial set to a _constant_ simplicial set with $X_{-1}$ as its set of $k$-simplices for all $k$.

It is in this latter form that augmented simplicial sets maybe mostly arise in practice, whereas the former incarnation offers a more succinct way of thinking about them.

For instance a major source of augmented [[simplicial object]]s are given by [[colimit]]s or rather [[homotopy colimit]]s over simplicial diagrams in a [[model category]]: for $X\colon \Delta^{op} \to C$ a simplicial object in a category with colimits, its colimit [[cocone]] may be thought of as a morphism 

$$
  X_\bullet \to const \lim_{\to} X_\bullet 
$$

into the constant simplicial object.


## Definitions

Denote by $\Delta_+$ (also denoted $\Delta_a$) the [[augmented simplex category]], which may be defined as the [[full subcategory]] of [[Cat]] on [[free categories]] over finite and _possibly empty_ linear [[directed graphs]], which are

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

where the only new [[simplicial identity]] satisfied by the new face map in degree $-1$ is that it coequalizes the degree-$0$ face maps in that

$$
  d^{-1}\circ d^0_1 = d^{-1}\circ d^0_0
  \,.
$$

It follows that $d^{-1}$ coequalizes in fact every pair of composites of face maps $X_n \to X_0$, so that equivalently an augmented simplicial set $X_\bullet$ is a morphism of ordinary simplicial sets

$$
  U(X_\bullet) \to const X_{-1}
  \,.
$$

We say that that $U(X_\bullet)$ is _augmented_ over $X_{-1}$.

More explicitly, an __augmented simplicial set__ consists of

*  for each [[integer]] $n \geq -1$, a [[set]] $X_n$ (so an [[infinite sequence]] $(X_{-1},X_0,X_1,X_2,\ldots)$ of sets),
*  for each integer $n \geq -1$ and each [[natural number]] $m \leq n + 1$, a __face map__ $d^n_m\colon X_{n+1} \to X_n$,
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

Every augmented simplicial set has an underlying unaugmented simplicial set found by forgetting $X_{-1}$ (and $d^{-1}_0$).  Conversely, every unaugmented simplicial set gives rise to a [[free object|free]] augmented simplicial set by augmentation over $\pi_0(X)$ (the set of [[connected component]]s of $X$) and a [[cofree object|cofree]] augmented simplicial set by augmentation over the [[point]] (the [[singleton set]]).  This defines [[adjunctions]]:
$$
\vdash\mathclap{\underoverset{\textsize{\operatorname{AugSimpSet}}}{\textsize{\operatorname{SimpSet}}}{\begin{matrix}\begin{svg}
<svg width="47" height="66" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="12691">
 <g>
  <title>Layer 1</title>
  <path fill="none" stroke="#000000" d="m15.14844,3c-21,22.035261 -18,43.469551 0,62.5" id="svg_12691_1" marker-start="url(#se_marker_start_svg_12691_1)"/>
  <path fill="none" stroke="#000000" d="m31.500429,65.25c21.000002,-21.947319 18.000002,-43.295465 0,-62.25" id="svg_12691_2" marker-end="url(#se_marker_end_svg_12691_2)"/>
  <line fill="none" stroke="#000000" x1="23.148436" y1="0.500004" x2="23.148436" y2="63.504595" id="svg_12691_3" marker-end="url(#se_marker_end_svg_12691_3)"/>
 </g>
 <defs>
  <marker id="se_marker_start_svg_12691_1" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_12691_4" d="m0,50l100,40l-30,-40l30,-40l-100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
  <marker id="se_marker_end_svg_12691_2" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_12691_5" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
  <marker id="se_marker_end_svg_12691_3" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_12691_6" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
 </defs>
</svg>
\end{svg}\includegraphics[width=35]{vertarrows}\end{matrix}}}\vdash
$$

## Examples

* For $C$ a [[site]], $\{U_i \to X\}$ a [[covering]] family we have the [[Cech nerve]] [[simplicial presheaf]] $C(U) \in [C^{op}, sSet]$. This comes canonically equipped with a morphism of simplicial presheaves to the one represented by $X\colon C(U) \to X$. This is an augmented simplicial object in the category of presheaves $[C^{op}, Set]$. Morover, over each object $V \in C$ its component

  $$
    C(U)(V) \to X(V)
  $$

  is an augmented simplicial set.

  More generally this applies to [[hypercover]]s.


## Related concepts

* [[augmentation]], [[augmentation ideal]]

* [[augmented algebra]]


[[!redirects augmented simplicial set]]
[[!redirects augmented simplicial sets]]
