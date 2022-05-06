
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Just as a [[derivator]] is a notion which lies in between a [[model category]] or a [[(∞,1)-category]] and its [[homotopy category]], a *stable* (or *triangulated*) *derivator* is a notion which lies in between a [[stable model category]] or a [[stable (∞,1)-category]] and its homotopy [[triangulated category]].

Stable derivators are a useful refinement of triangulated categories, since they contain enough information so that [[homotopy limit]] and colimit constructions can be performed "coherently" and desired maps and objects can be specified by true universal properties.  This resolves many common issues with triangulated categories stemming from the fact that at the level of a homotopy category, certain desirable maps can only be stipulated to exist with some weak properties, but not characterized precisely among the class of maps that have those properties.

## Definition
 {#Definition}

As is the case for [[stable (∞,1)-categories]], being stable is a [[stuff, structure, property|property]] of a derivator rather than a structure (or more precisely, it is a [[property-like structure]]).  In fact, an $(\infty,1)$-category is stable precisely when its underlying derivator is.

Write $\square$ for the "free-living commutative square"
$$\array{ & \overset{}{\to} & \\
  \downarrow && \downarrow\\
  & \underset{}{\to} & }$$
and let $L$ and $R$ denote the upper-left [[span]] and the lower-right [[cospan]] as subcategories of $\square$, with inclusions $i\colon L\to \square$ and $j \colon R\to \square$.  For a [[derivator]] $D$, an object $X\in D(\square)$ is said to be **cartesian** if the unit $X\to j_* j^* X$ is an isomorphism, and dually **cocartesian** if the counit $i_! i^* X\to X$ is an isomorphism.  Since $i$ and $j$ are fully faithful, it follows from a general theorem about derivators that $i_!$ and $j_*$ are also fully faithful; thus being cartesian is equivalent to being of the form $j_* Y$ for some $Y\in D(R)$, and likewise being cocartesian is equivalent to being of the form $i_! Z$.

A derivator $D$ is **stable** (or **triangulated**) if it is [[pointed derivator|pointed]], and moreover an $X\in D(\square)$ is cartesian if and only if it is cocartesian.  Such a square is then called **bicartesian**.

## Properties

### Triangulation

One of the central facts about stable derivators is:

+-- {: .un_theorem}
###### Theorem (Maltsiniotis)
If $D$ is a stable derivator, then each category $D(X)$ is a [[triangulated category]] in a canonical way.
=--

We describe the constructions when $X=1$.  The shift/suspension functor $S\colon D(1)\to D(1)$ is defined by 
$$ S = b^* i_! a_* $$
where $a\colon 1\to L$ is the inclusion of the top-left vertex of the span, and $b\colon 1\to \square$ is the inclusion of the bottom-right vertex of the square.  In other words, for an object $X\in D(1)$ its suspension is defined by the [[homotopy pushout]]
$$\array{X & \overset{}{\to} & 0\\
  \downarrow && \downarrow\\
  0 & \underset{}{\to} & S X.}$$
This makes sense in the more general context of any [[pointed derivator]], but the stability axiom guarantees that $S$ is actually an equivalence of categories.  Its inverse being given by the obvious dual "loop space" construction (which in a general pointed derivator is only right adjoint to it).  This provides a motivation for the stability axiom: it is a generalization of the statement that every object is the loop space of its suspension and the suspension of its loop space.

One can also prove that $S$ is also a [[copower]] with the pointed [[circle]] $S^1$ in a suitable sense.  In particular, since every object is isomorphic to a double suspension, it is a cogroup object; thus $D(X)$ is canonically an [[Ab-enriched category]].

Let $Q$ denote the category
$$\array{ & \overset{}{\to} & & \to &\\
  \downarrow && \downarrow && \downarrow\\
  & \underset{}{\to} & & \to &}$$
with inclusions $m,n,p\colon \square \to Q$ of the left and right squares and the outer rectangle, respectively.  An object $X\in D(Q)$ is **bicartesian** if $m^*X$, $n^*X$, and $p^*X$ are all bicartesian.

Now consider a bicartesian object $X\in D(Q)$ of the form:
$$\array{A & \overset{f}{\to} & B & \to & 0\\
  \downarrow && \downarrow^g && \downarrow\\
  0 & \to & C & \underset{h}{\to} & D.}$$
In other words, we stipulate that the restrictions to $D(1)$ along the inclusions of the lower-left and upper-right vertices be zero objects.  Now since $X$ is bicartesian, the outer square
$$\array{A & \overset{}{\to} & 0\\
  \downarrow && \downarrow\\
  0& \underset{}{\to} & D}$$
is bicartesian, and thus induces an isomorphism $D \cong S A$.  Thus, from $X$ we can extract a "triangle"
$$ A \overset{f}{\to} B \overset{g}{\to} C \overset{h}{\to} S A$$
and we define the *distinguished triangles* in $D(1)$ to be those isomorphic to triangles obtained in this way.

One can then prove the axioms of a triangulated category.

+-- {: .un_remark}
###### Remark
If $ A \overset{f}{\to} B \overset{g}{\to} C \overset{h}{\to} S A$ is a distinguished triangle in a triangulated category, then $ A \overset{f}{\to} B \overset{g}{\to} C \overset{-h}{\to} S A$ is also an "exact" triangle in the sense that it induces [[long exact sequences]] in [[homology]] and [[cohomology]], but it is not in general distinguished.  On the other hand, if 
$$\array{A & \overset{f}{\to} & B & \to & 0\\
  \downarrow && \downarrow^g && \downarrow\\
  0 & \to & C & \underset{h}{\to} & D.}$$
is bicartesian in an $(\infty,1)$-category, then so is
$$\array{A & \overset{f}{\to} & B & \to & 0\\
  \downarrow && \downarrow^g && \downarrow\\
  0 & \to & C & \underset{-h}{\to} & D.}$$
This seeming paradox is resolved by noticing that although these two bicartesian diagrams have the same object $D$ at their lower-right-hand corner, the different maps $h$ and $-h$ cause these diagrams to induce different isomorphisms $D \cong S A$.  The isomorphism for the latter diagram incorporates an extra minus sign, relative to the first one, causing these two diagrams to both induce the *same* triangle $ A \overset{f}{\to} B \overset{g}{\to} C \overset{h}{\to} S A$ in the homotopy category.
=--

## Related concepts

* [[triangulated category]]

* [[pretriangulated dg-category]], [[enhanced triangulated category]]

* **stable derivator**

* [[stable (∞,1)-category]]


## References

See [[derivator]] for general references about derivators, and also [[pointed derivator]].  References particularly pertaining to the stable version include:

* [[Alex Heller]], "Stable homotopy theories and stabilization" [MR](http://www.ams.org/mathscinet-getitem?mr=1431157)

* [[Denis-Charles Cisinski]] and Amnon Neeman, "Additivity for derivator K-theory", [MR](http://www.ams.org/mathscinet-getitem?mr=2382732)

* Jens Franke, _Uniqueness theorems for certain triangulated categories with an Adams spectral sequence_, [K-theory archive](http://www.math.uiuc.edu/K-theory/0139/)

* [[Moritz Groth]], _Derivators, pointed derivators, and stable derivators_ ([pdf](http://www.math.uni-bonn.de/~mgroth/groth_derivators.pdf))

* [[Ian Coley]], _Stabilization of derivators revisited_, 2018, [arxiv](https://arxiv.org/abs/1802.04343)

[[!redirects stable derivators]]
[[!redirects triangulated derivator]]
[[!redirects triangulated derivators]]
