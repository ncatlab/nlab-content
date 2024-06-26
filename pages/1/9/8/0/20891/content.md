+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}

## Idea

Just as the notion of an [[elementary topos]] is an [[axiom|axiomatization]] of basic [[category theory|category-theoretic]] properties of the [[Set|category of sets]], the notion of a "*category with class structure*" or "*category of classes*" is an axiomatization of the basic category theoretic properties of the category of [[classes]].  

In contrast to the situation for elementary toposes, however, there is no unique such axiomatization with a privileged status in the literature; the field of [[algebraic set theory]] includes many variations.  Here we describe the first such axiomatization due to [Joyal-Moerdijk](#JM).

## Definition

We work in a category $C$ that is assumed to be a [[Heyting pretopos]]
with a [[natural numbers object]]. Following [Joyal-Moerdijk](#JM), we have the following definition. 

\begin{definition}
A __class of open maps__ (with collection) in $C$
is a [[class]] $S$ of morphisms in $C$ that satisfies the following properties:

* $S$ contains all isomorphisms and is closed under compositions;
* $S$ is closed under [[base changes]];
* if $g\in S$ is a [[base change]] of $f$ along an [[epimorphism]], then $f\in S$;
* the canonical maps $0\to 1$ and $1\sqcup 1\to 1$ belong to $S$;
* $S$ is closed under binary [[coproducts]] in the [[category of morphisms]] of $C$;
* if $g=f\circ p$, where $p$ is an [[epimorphism]] and $g\in S$, then also $f\in S$;
* (collection axiom) for any [[epimorphism]] $p\colon Y\to X$ and $f\colon X\to A$ such that $f\in S$ there is an [[epimorphism]] $h\colon B\to A$, a morphism $g\colon Z\to B$ such that $g\in S$, and a morphism $w:Z\to Y$ such that $h g=f p w$ and the induced map $Z\to B\times_A X$ is an [[epimorphism]].

\end{definition}

\begin{definition}
A __class of small maps__ in $C$ is a class of open maps $S$ in $C$
such that every map in $S$ is [[exponential object|exponentiable]]
and there is a universal map $\pi\colon E\to U$ in $S$
with the following property: for any $f\in S$ we can [[base change]] $f$ along some [[epimorphism]] $p$ such that the resulting morphism $f'$ is a 
[[base change]] of $\pi$ along some morphism in $C$.
Elements of $S$ are known as __small maps__.
An object $X$ of $C$ is __small__ if the map $X\to 1$ is small.
\end{definition}

Intuitively, small maps are maps $X\to Y$ for which preimages
of any element of $Y$ are sets as opposed to proper classes.

In any [[Heyting pretopos]] the class of [[exponential object|exponentiable maps]]
satisfies all the axioms of a class of open maps
with a possible exception of the collection axiom.

The collection axiom can be reformulated by saying
that the _small powerset_ functor preserves [[epimorphisms]].
One way to define the small powerset of $X$ is as the free $S$-complete
[[suplattice]] generated by $X$.

\begin{definition}
A category with a class of small maps admits __powerclasses__
if for any object $C$ there is an object $P C$
with a small relation $\in\subset C\times P C$
such that any object $X$ and any small relation $R\subset C\times X$
there is a unique morphism $r\colon X\to P C$
such that $R\to C\times X$ is the [[base change]] of $\in\to C\times P C$
along the map $id_C \times r$.
Furthermore, the internal subset relation on $P C$ must be small.
\end{definition}

\begin{definition}
A __universal class__ is an object $U$
such that any object $C$ admits a [[monomorphism]] $U\to C$.
\end{definition}

\begin{definition}
A __category of classes__ or a __class category__
is [[Heyting category]] with a class of small maps
that admits small powerclasses and a universal class.
\end{definition}

The full subcategory of small objects and small maps
of any class category is an [[elementary topos]].

## Related notions

* [[class]]

* [[proper class]]

* [[large category]]

* [[category of classes]]

* [[algebraic set theory]]

## References

* {#JM} [[André Joyal]], [[Ieke Moerdijk]], _Algebraic set theory_.  Cambridge University Press, 1995.  ISBN 0-521-55830-1. 

* [[Steve Awodey]], _An outline of algebraic set theory_.  [PDF](https://www.phil.cmu.edu/projects/ast/Papers/awodey_outline.pdf)

[[!redirects category with class structure]]
[[!redirects categories with class structure]]

[[!redirects regular category with class structure]]
[[!redirects regular categories with class structure]]

[[!redirects coherent category with class structure]]
[[!redirects coherent categories with class structure]]

[[!redirects Heyting category with class structure]]
[[!redirects Heyting categories with class structure]]