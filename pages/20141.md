# Enriched over-categories

* table of contents
{: toc}

## Idea

The generalization of an [[over-category]] to [[enriched categories]].

## Definition

Let $(V,\otimes,I)$ be a [[monoidal category]] with [[pullbacks]], $C$ a $V$-[[enriched category]], and $x\in C$ an [[object]].  The **enriched over-category** (or **enriched slice category**) $C/x$ is the following $V$-category:

* its objects are the morphisms $f:y\to x$ in (the [[underlying ordinary category]] of) $C$, i.e. morphisms $I\to C(y,x)$ in $V$.

* its [[hom-object]] from $f:y\to x$ to $g:z\to x$ is the [[pullback]] in $V$:

\begin{center}
\begin{tikzcd}
  (C/x)(f,g) \ar[r] \ar[d] \ar[dr,phantom,near start,"\lrcorner"] & C(y,z) \ar[d,"{g\circ -}"]\\
  I \ar[r,"\ulcorner f \urcorner"'] & C(y,x)
\end{tikzcd}
\end{center}

The dual concept is the **enriched under-category** or **enriched co-slice category**.

## Properties

* $C/x$ can be described as the [[comma object]] of $Id:C\to C$ and $x : I \to C$ in the [[2-category]] $V Cat$, where $I$ denotes the [[unit enriched category]].

* All hom-objects of $C/x$ are [[augmentation|augmented]], i.e. come with a map to the unit object.  This seems somewhat curious unless $V$ is [[cartesian monoidal category|cartesian monoidal]] (or at least [[semicartesian monoidal category|semicartesian]]) in which case $I$ is the [[terminal object]] $1$.

* Any morphism $f:x\to y$ in $C$ induces a $V$-functor $f_!:C/x \to C/y$.  If $C$ has $V$-enriched pullbacks, then $f_!$ has a right $V$-adjoint $f^*$.  If $C$ is a [[locally cartesian closed enriched category]], then $f^*$ has a further right $V$-adjoint $f_*$.

## References

* [Enriched slice categories, MO](https://mathoverflow.net/q/259829)

[[!redirects enriched over category]]
[[!redirects enriched over categories]]
[[!redirects enriched over-category]]
[[!redirects enriched over-categories]]

[[!redirects enriched under category]]
[[!redirects enriched under categories]]
[[!redirects enriched under-category]]
[[!redirects enriched under-categories]]

[[!redirects enriched slice category]]
[[!redirects enriched slice categories]]
[[!redirects enriched coslice category]]
[[!redirects enriched coslice categories]]
[[!redirects enriched co-slice category]]
[[!redirects enriched co-slice categories]]
