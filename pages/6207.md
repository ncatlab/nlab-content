
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Terminology

A twisted arrow category is an alternative name for a [[category of factorisations]]. That latter name is applied when discussing natural systems  and [[Baues-Wirsching cohomology]], whilst the name _twisted arrow category_ is more often used in discussing Kan extensions and within the categorical literature[^Law]. 

[^Law]: [[Lawvere]] ('Equality in hyperdoctrines', 1970) uses the term 'twisted _morphism_ category'.


## Definition

The twisted arrow category $Tw(C)$ of $C$ a category is the [[category of elements]] of its [[hom-functor]]: 
\[ 
Tw(C) = el(hom) = * / hom 
\]


### Explicit description

Unpacking the well-known explicit construction of [[comma object|comma objects]] in $\mathbf{Cat}$ as [[comma category|comma categories]], we get that $Tw(C)$ has

* objects: $f$ an arrow in $C$, and

* morphisms: between $f$ and $g$ are pairs of arrows $(p,q)$ such that the following diagram commutes:
\[
\begin{matrix}
  A             & \overset{p}{\leftarrow}   & C            \\
  f \downarrow  &                           & \downarrow g \\
  B             & \underset{q}{\to}         & D
\end{matrix}
\]
you could view then morphisms from $f$ to $g$ as *factorizations* of $g$ through $f$: $g = q f p$.

From the description above, $Tw(C)$ is the same as $Arr(C)$ the [[arrow category]] of $C$, but with the direction of $p$ above in the definition of morphism *reversed*, hence the twist. 

### As a lax colimit

The (opposite of the) category $Tw(C)$ can be described as the [[2-limit#lax|lax colimit]] of the diagram $C \to Cat\colon c\mapsto C/c$.

## Example

If $C$ is a partially ordered set, then $Tw(C)$ is isomorphic to the set of nonempty [[interval|intervals]] $[a,b]=\{c\in C| a\leq c\leq \b\}$ with $a\leq b$ in C ordered by inclusion (cf. [Johnstone 1999](#JT99)).

## Properties

* From its definition as a comma category, there is a functor (a [[discrete opfibration]], in fact) 
\[ 
\pi_C \colon Tw(C) \to C^{op} \times C 
\] 
which at the level of objects forgets the arrows:
\[
\pi_C(f \colon A \to B) = (A,B) 
\] 
and keeps everything at the morphisms level. 


### $Tw(C)$ and wedges

One could say that $Tw(C)$ *classifies* [[wedge|wedges]], in the sense that for any functor $F \colon C^{op} \times C \to B$,

* [[extranatural transformation|extranatural transformations]] $ e \stackrel{\bullet}{\to} F $ 

are the same as

* [[natural transformation|natural transformations]] $ e \to F \circ \pi_C $ 

This can be used to give a proof of the reduction of [[end|ends]] to [[conical limit|conical limits]] in the $\mathbf{Set}$-enriched case, and is used in the construction of [[ends in a derivator]].

## Generalizations

* The twisted arrow category is a special case of a **category of judgments** in the sense of ([Melli&#232;s-Zeilberger 15](#MZ15)).

* The construction generalizes to $(\infty,1)$-categories (cf. [Lurie 11](#DAGX), sec.4.2).

## Related entries

* [[category of factorizations]]
* [[twisted arrow (∞,1)-category]]

## References

* {#BN00}[[Marta Bunge|M. Bunge]], [[Susan Niefield|S. Niefield]], _Exponentiability and single universes_ , JPAA **148** (2000) pp.217-250.

* L. Errington, _Twisted Systems_ , PhD thesis Imperial College London 1999.  ([doi](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.6369))

* [[Peter Johnstone]], _A Note on Discrete Conduch&#233; Fibrations_ , TAC **5** no.1 (1999) pp.1-11. ([pdf](http://www.tac.mta.ca/tac/volumes/1999/n1/n1.pdf))

* [[Fred Linton]], _Autonomous categories and duality of functors_ , J. Algebra **2** no.3 (1965) pp.315-349.

* [[Jacob Lurie]], _Derived Algebraic Geometry X: Formal Moduli Problems_ , ms. (2011). {#DAGX}

* [[Saunders Mac Lane]], _Categories for the Working Mathematician_ , Springer Heidelberg 1998&#178;. (cf. exercise IX.6.3, p.227)

* [[Paul-André Melliès]], [[Noam Zeilberger]], _Isbell Duality for Refinement Types_ , [arXiv:1501.05115](http://arxiv.org/abs/1501.05115) (2015). {#MZ15}

[[!redirects twisted arrow category]]
[[!redirects twisted arrow categories]]
