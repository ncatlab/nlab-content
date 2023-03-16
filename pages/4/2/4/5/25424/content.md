
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Multi-adjoints

* table of contents
{: toc}

## Idea

A **multimonad** is to a [[multiadjunction]] what a [[monad]] is to an [[adjunction]].

(Note that this is **not** related to monads on [[multicategories]].)

## Definition

\begin{defn}
A **multimonad** on a category $C$ comprises a [[presheaf]] on $C$ together with a monad on its [[category of elements]].
\end{defn}

## Multimonadic categories

Multi-monadic categories on $Set$ can be characterized in the following way: they are regular, with connected limits, with coequalizers of coequalizable pairs, their equivalence relations are effective, their forgetful functors preserve coequalizers of equivalence relations and reflect isomorphisms. Unlike  monadic categories they need not have products. Examples include local rings, fields, inner spaces, locally compact spaces, locally compact groups, and complete ordered sets. ([Diers 80, p.153](#Diers1980))

The forgetful functor from a multimonadic category [[created limit|creates]] [[connected limits]].

## References

* {#Diers1980} [[Yves Diers]], _Multimonads and multimonadic categories_, Journal of Pure and Applied Algebra 17 (1980) 153-170 ([pdf](https://core.ac.uk/download/pdf/82552386.pdf))