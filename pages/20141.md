
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



# Enriched slice categories
* table of contents
{: toc}

## Idea

The notion of enriched slice categories is the generalization of the notion of [[slice categories]] from plain [[category theory]] of [[locally small categories]] to [[enriched category theory]] of $\mathcal{V}$-[[enriched categories]].

## Definition

\begin{definition}
Let 

* $(V,\otimes,I)$ be a [[monoidal category]] with [[pullbacks]] (e.g. a [[Bénabou cosmos]]), 

* $C$ a $V$-[[enriched category]], 

* $x\in C$ an [[object]].  

Then the *enriched slice category* (or *enriched over-category*) $C/x$ is the following $V$-enriched category:

* its [[objects]] are the [[morphisms]] $f \,\colon\, y\to x$ in (the [[underlying ordinary category]] of) $C$, i.e. morphisms $I \to C(y,x)$ in $V$.

* its [[hom-object]] from $f \,\colon\, y\to x$ to $g \,\colon\, z\to x$ is the [[pullback]] in $V$:

\begin{center}
\begin{tikzcd}
  (C/x)(f,g) 
   \ar[r] 
   \ar[d] 
   \ar[dr,phantom,near start,"\lrcorner"] 
   & 
   C(y,z) 
     \ar[d,"{g\circ -}"]
   \\
   I 
     \ar[r,"\ulcorner f \urcorner"'] 
   & 
   C(y,x)
\end{tikzcd}
\end{center}
\end{definition}

\begin{remark}
The [[formal duality|dual]] concept is the 
*enriched co-slice category* or *enriched under-category*, the enriched generalization of the notion of *[[co-slice category]]*.
\end{remark}

## Properties

* $C/x$ can be described as the [[comma object]] of $Id \,\colon\,C\to C$ and $x \,\colon\, I \to C$ in the [[2-category]] $V Cat$, where $I$ denotes the [[unit enriched category]].

* All [[hom-objects]] of $C/x$ are [[augmentation|augmented]], i.e. equipped with a [[morphism]] to the [[unit object]].  This seems somewhat curious unless $V$ is [[cartesian monoidal category|cartesian monoidal]] (or at least [[semicartesian monoidal category|semicartesian]]) in which case $I$ is the [[terminal object]] $1$.

* Any morphism $f \,\colon\, x\to y$ in $C$ induces a $V$-[[enriched functor]] $f_! \,\colon\, C/x \to C/y$.  If $C$ has $V$-enriched pullbacks, then $f_!$ has a [[right adjoint|right]] $V$-[[enriched adjoint]] $f^*$.  If $C$ is a [[locally cartesian closed enriched category]], then $f^*$ has a further right $V$-adjoint $f_*$.

## Related concepts

* [enriched slice model structure](slice+model+structure#ModelStructureInheritsEnriched)

* [[slice of presheaves is presheaves on slice]]

## References

* MathOverflow, *Enriched slice categories* ([MO:q/259829](https://mathoverflow.net/q/259829))

[[!redirects enriched slice categories]]
[[!redirects enriched coslice category]]
[[!redirects enriched coslice categories]]
[[!redirects enriched co-slice category]]
[[!redirects enriched co-slice categories]]


[[!redirects enriched over category]]
[[!redirects enriched over categories]]
[[!redirects enriched over-category]]
[[!redirects enriched over-categories]]

[[!redirects enriched under category]]
[[!redirects enriched under categories]]
[[!redirects enriched under-category]]
[[!redirects enriched under-categories]]

